# Release Checklist

## Build and assets
- [ ] Open `index.html` locally in at least one desktop browser.
- [ ] Open the published build on a phone or narrow browser window.
- [ ] Confirm no console errors and that the game starts, pauses, resumes, wins, loses, and restarts.
- [ ] Confirm the game still works with local storage unavailable or blocked.
- [ ] Confirm mute and reduced-motion preferences work and persist when storage is available.
- [ ] Verify there are no temporary placeholder images, uncredited external assets, or unnecessary external requests.

## Usability and accessibility
- [ ] Complete one round using only keyboard controls.
- [ ] Confirm focus outlines are visible on buttons and settings.
- [ ] Confirm touch controls work and do not remain stuck after touch cancellation.
- [ ] Check mute and reduced motion independently.
- [ ] Check text and controls on a narrow screen without horizontal page overflow.
- [ ] Ask at least three people the same playtest questions and enter their real feedback in `PLAYTEST_NOTES.md`.

## Evidence and publishing
- [ ] Capture a real screenshot of the earlier build and the release build; place them in `evidence/`.
- [ ] Complete the evidence notes and postmortem based on actual tests.
- [ ] Upload all project files to one public GitHub repository.
- [ ] Enable GitHub Pages from `main` / root.
- [ ] Open the published URL in a private/incognito window to verify public access.
- [ ] Submit one public URL that opens the game; keep supporting files in the same repository.
