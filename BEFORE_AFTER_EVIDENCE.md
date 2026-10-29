# Before-and-After Evidence

## Before — v2 baseline
Use the previous commit/version of `index.html` as the baseline. It already had game states, score, levels, timer, lives, keyboard movement, and a saved high score. It had basic coin particles, but no sound/mute control or reduced-motion preference. Feedback for hits and level changes was mostly visual/textual, and keyboard focus was not clearly styled.

**Evidence to capture:** open the previous commit on GitHub (or use the v2 ZIP before replacing it), take a screenshot of the game screen, and save it as `evidence/before-v2.png` in this repository. Do not label a recreated mockup as a real screenshot.

## After — v3 revised build
The revised build adds:
- Short optional sound cues for coin collection, hits, level-up, pause, win, and loss.
- Visible “Mute sound” and “Reduced motion” settings, persisted locally.
- Reduced-motion mode disables coin pulsing and particle bursts.
- Strong visible keyboard focus outlines for buttons and settings.
- Live status text for coin collection, damage, level changes, pause, and game end.
- A pause on browser-window blur to reduce accidental background play.

**Evidence to capture:** run v3, take a screenshot of the start/settings screen and another after collecting a coin or levelling up. Save them as `evidence/after-v3-settings.png` and `evidence/after-v3-feedback.png`. Actual screenshots should be captured from the running build.

## Evidence checklist
- [ ] Before screenshot from v2 baseline added to `evidence/`
- [ ] After screenshot of v3 settings added to `evidence/`
- [ ] After screenshot of v3 gameplay feedback added to `evidence/`
- [ ] Playtest notes completed from 3 real participants
- [ ] Changes in the “Findings and action taken” table reflect what participants actually said
