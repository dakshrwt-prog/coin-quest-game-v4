# Edge-case Test Checklist

- [ ] Start begins with score 0, level 1, 60 seconds and 3 lives.
- [ ] P/Esc while Playing pauses timer and hazards.
- [ ] Resume continues the same run without resetting score/time/lives.
- [ ] Pause input outside Playing does not start or alter a run.
- [ ] One coin collision adds exactly one point and spawns a replacement.
- [ ] Score 5 advances to level 2; score 10 advances to level 3.
- [ ] Each level adds one hazard and increases hazard speed.
- [ ] Score 15 triggers Win and stops gameplay updates.
- [ ] Timer 0 triggers Lose.
- [ ] Losing the third life triggers Lose.
- [ ] Collision cooldown prevents one overlap from draining all lives immediately.
- [ ] Restart from Paused resets all run data.
- [ ] Restart after Win or Lose begins a clean run.
- [ ] High score updates only when beaten and survives a page refresh on the same browser/device.
- [ ] If localStorage is blocked, the game still plays (high score may not persist).
- [ ] Mobile direction buttons stop moving on release/cancel.
- [ ] Player remains inside arena boundaries.
- [ ] Diagonal movement is normalized.
