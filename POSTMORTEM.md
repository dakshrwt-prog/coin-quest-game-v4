# Coin Quest — Development Postmortem

## Project goal
Ship a small, playable browser game with clear controls, stable game-state transitions, satisfying feedback, accessibility options, and a simple public release process.

## What shipped
- Start, playing, paused, win, lose, and restart flow.
- Score target, timer, three lives, level progression, and increasing hazard pressure.
- Keyboard and touch controls, visible focus styling, mute toggle, reduced-motion option, and locally saved high score/preferences.
- Visual feedback for collecting coins, taking damage, changing levels, pausing, and finishing a round.
- A self-contained HTML build with no third-party runtime dependencies or external asset requests.
- A cached background canvas to avoid redrawing the static grid every frame.

## Design decisions
- **Canvas-drawn assets:** simple original shapes keep the visual language consistent and avoid licensing ambiguity or slow asset downloads.
- **Short synthesized audio cues:** feedback can be produced without shipping audio files; the mute control remains available.
- **One-file build:** opening `index.html` locally is straightforward for beginners and reduces deployment complexity.
- **Readable status UI:** score, level, timer, lives, and current state stay visible outside the playfield so effects do not obscure gameplay.
- **Progressive challenge:** every five coins increases the level and adds a faster hazard, giving players a clear sense of progression.

## Trade-offs and limitations
- The art is intentionally minimal and may not feel as expressive as a custom sprite set.
- Synthesized tones are functional cues rather than a full soundtrack; browsers may require user interaction before audio starts.
- The game uses a fixed internal canvas coordinate system scaled by CSS rather than a fully dynamic world simulation.
- Local high scores and preferences are per-browser/device and are not synced across devices.
- The project has a manual playtest template; results must be gathered from real players before making claims about usability improvements.

## Evidence-based reflection — complete after release testing
Do not fill this section with invented results. After testing with at least three people, replace the prompts below with observed evidence.

- **What players found easiest:** [Add a real observation and which tester/task it came from.]
- **Main friction point:** [Describe the observed issue, not an assumption.]
- **Change made in response:** [Name the code/UI change and connect it to the feedback.]
- **Before/after evidence:** [Reference screenshots in `evidence/` and explain what visibly changed.]
- **Accessibility check:** [Record keyboard-only, mute, reduced-motion, and narrow-screen checks actually performed.]
- **Remaining issue:** [State one limitation still present and a realistic next step.]

## Next iteration
Prioritize issues that multiple playtesters encounter, then retest the revised build using the same tasks and questions. Consider adding a dedicated pause button for touch users and testing with more screen sizes if those issues appear in feedback.
