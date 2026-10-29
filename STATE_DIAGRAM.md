# State Diagram — Coin Quest 2

```mermaid
stateDiagram-v2
    [*] --> Start
    Start --> Playing: Start game
    Playing --> Paused: P / Esc
    Paused --> Playing: Resume
    Paused --> Restart: Restart
    Playing --> Win: Score reaches 15
    Playing --> Lose: Timer reaches 0 OR lives reach 0
    Win --> Restart: Play again / R
    Lose --> Restart: Try again / R
    Restart --> Playing: Reset all run data
```

- **Start:** instructions show; simulation is stopped.
- **Playing:** timer, movement, collisions, score, hazards update.
- **Paused:** simulation and timer freeze.
- **Win:** collect 15 coins; game loop stops.
- **Lose:** timer expires or all three lives are lost.
- **Restart:** resets score, level, timer, lives, coins, hazards and particles before entering Playing.
