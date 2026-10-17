# Hearts & Skulls v0.1 — validation snapshot

Generated October 17, 2026.

## Verified automatically

- JavaScript syntax parses cleanly.
- Initial gameplay UI renders with no browser page exceptions.
- No document scrolling or horizontal overflow at Chromium viewports 390×844, 375×812, 320×568, 360×640, 430×932, 844×390, 780×420 and 1280×820.
- Two sides alternate legal turns; solo mode computer responds; selecting Skulls lets computer open with Hearts.
- Legal supported capture: an allied adjacent Red attacks an enemy Blue. A weaker color does not capture; unsupported attacks are excluded.
- Win by mixed-color, same-side three-in-a-row detected.
- Same-browser match persistence with localStorage state was simulated; a real reload of live URL remains to be tested.
- Two-player mode, rule dialog, new-match dialog and cancellation passed browser interaction tests.
- 20 simulated random-human versus search-computer matches terminated within 6 moves; this is software stress evidence, **not proof of balanced or enjoyable competitive play**.

## Pending real-player validation

- iPhone Safari portrait and landscape, including actual swipe/scroll behavior and tap accuracy.
- Rules understood without verbal explanation.
- Human versus human balance; countercapture tactics; whether the opening side dominates.
- Sound, app-store distribution, monetization, online play and licensing are not included in this intentionally minimal build.
