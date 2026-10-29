# Coin Quest — Release Build (v4)

A lightweight, single-page browser game. Collect 15 coins before the 60-second timer ends while avoiding moving hazards. Every 5 coins advances the level and increases hazard pressure.

## Run locally
Open `index.html` in a modern browser. No install, build step, external asset download, or network connection is required.

## Controls
- Move: Arrow keys or WASD
- Pause/resume: `P` or `Escape`
- Restart when not actively playing: `R`, or use the on-screen button
- Mobile: on-screen directional buttons
- Settings: **Mute sound** and **Reduced motion** checkboxes

## Release-quality notes
- The game uses a single HTML file with inline CSS and JavaScript, so there are no external scripts, fonts, images, or asset requests to delay startup.
- Player, coins, hazards, particles, and background are drawn with Canvas primitives. The background grid is rendered to a cached canvas once instead of being rebuilt every animation frame.
- The game loop caps frame delta to reduce large movement jumps after slow frames or tab switches.
- Responsive layout scales the canvas to the available width; touch controls appear on narrow screens.
- Sound is generated with the Web Audio API and can be muted. Sound failures are handled without blocking gameplay.
- High score and preference settings use local storage when available; the game still runs if storage is unavailable.
- Keyboard focus is visible, settings are labelled, and status updates use a polite live region.
- Reduced-motion mode removes particle bursts and coin pulsing. The browser's `prefers-reduced-motion` setting also disables CSS motion.

## Credits and asset licensing
See [`CREDITS.md`](CREDITS.md). The build uses original canvas-drawn shapes and system fonts; it includes no third-party images, music, sound recordings, libraries, or downloaded assets.

## Supporting materials
- `CREDITS.md` — asset and tool credits
- `POSTMORTEM.md` — reflective development postmortem (complete the evidence-based section after testing)
- `RELEASE_CHECKLIST.md` — final publication checks
- `PLAYTEST_NOTES.md` — record actual observations from at least three people; do not invent results
- `BEFORE_AFTER_EVIDENCE.md` — screenshot evidence instructions
- `STATE_DIAGRAM.md` — state transitions
- `EDGE_CASE_TESTS.md` — edge-case checklist

## Publish one proof link
1. Upload all files to the same **public** GitHub repository.
2. Open **Settings → Pages**.
3. Under build/deployment, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
4. Wait for GitHub Pages to publish and open the generated URL to verify the game loads.
5. Keep supporting Markdown files and an `evidence/` folder with real screenshots in the same repository. Submit the GitHub Pages URL; include the repository link in the project README.

The public URL does not exist until you publish the repository with GitHub Pages. Do not submit an example URL as proof.
