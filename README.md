# Hearts & Skulls — first playable release candidate

Single-file, offline-capable, mobile-first web game. No build step, tracking, advertising, external fonts, libraries or connections.

## Locked rules

* Two sides, Hearts and Skulls, alternate visible moves on a 3×3 board.
* Red = Would, Blue = Could, Yellow = Should. The color dominance cycle is **Red > Blue > Yellow > Red**, equivalent to **Would > Could > Should > Would**.
* Each turn, place any color on an empty square.
* To replace an opposing piece, your placed color must beat its color, and you must already own an **adjacent piece of the same color as your attacking piece**. The eight surrounding squares (including diagonals) count as adjacent.
* Capturing does not destroy the ally enabling the capture; the challenger is a new piece placed onto the opponent's square.
* A nearby counterattacker permits recapture, but does not block the original capture.
* Three of your own side in any straight row, column, or diagonal wins, independent of colors.
* Threefold repetition or a position where the next player has no legal move is a draw.

## Prototype modes

* One player versus the local computer, or two players sharing one device.
* Single-player defaults to Hearts; tapping “Play as Skulls” swaps the human and computer sides, starting a new match.
* No online matchmaking or accounts. A mobile internet connection is not needed after the HTML is saved.
* LocalStorage keeps the current game and match scores on the same browser. New game preserves score; clearing website data resets it.

## Manual validation to finish before wider publication

* iPhone Safari: all three columns/rows visible, button targets, no scrolling in portrait.
* Try an adjacent same-color supported capture, attempted unsupported capture, one win with mixed colors, a deadlock, saving/reloading midgame, and play-as-Skulls computer opening.
* Run at least ten matches against a human; look for trivial dominant openings, repetitive exchange loops, and whether the capture rule is intelligible without coaching.

## Run locally

Open `index.html` directly in your browser, or from its folder run `python3 -m http.server 8000` and visit `http://localhost:8000`.

## Publish through GitHub Pages

Put this `index.html` into the root of a **new** GitHub repository (not Chatrajnorak's), enable GitHub Pages on `main` from the repository root, then check that the live build matches the file. Do not overwrite Chatrajnorak.
