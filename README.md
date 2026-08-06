# maze-dash

A one-button maze runner: the runner never stops, and the only thing you do is choose which way it turns.

![A 13 by 13 maze drawn in thin ink lines on off-white paper, the amber runner mid-corridor with a grey trail fading out behind it, a dashed amber line running from the runner to an amber arrow on the junction ahead that marks the exit it will take, and the HUD reading 2 cleared and 38.0 seconds left](screenshot.png)

**[Live demo](https://yinggarykairui.github.io/maze-dash/)**

## What it does

A run is 60 seconds on the game clock, and the supply of mazes is endless. The runner moves on its own at a fixed speed, follows corridors without being asked, and reverses out of dead ends by itself — the only moment it needs you is at a junction. As soon as it commits to one junction, an amber arrow appears on the next one showing the exit it will take, with a dashed line back to the runner so you can see which junction the arrow belongs to. One press moves the arrow to the next exit, clockwise, and it stays where you put it. Whatever the arrow points at when the runner arrives is the turn it takes. Left alone, the runner defaults to an exit it has not used yet in that maze, so it explores rather than circling.

Reach the ringed cell against the right-hand wall and the maze is cleared, a new one is generated, and you keep going until the clock runs out. Every maze comes from a recursive backtracker, so there is exactly one path between any two cells and every maze is solvable. The screenshot above shows a run in progress: the runner, its fading trail, the dashed line tying it to the arrow on the junction ahead, and the HUD reading two mazes cleared with 38.0 seconds left.

The score is how many mazes you cleared; the browser also remembers your fastest single maze. Both records live in `localStorage` on your own machine and go nowhere else. You cannot crash and you cannot lose — wrong turns cost seconds, and seconds are the only thing you have.

Space, Enter, and a tap anywhere on the maze all do the same one thing. There is no sound.

## How to run

Open the live demo above, or run the file directly — it is one self-contained HTML file with no dependencies and no build step:

```
git clone https://github.com/yinggarykairui/maze-dash.git
cd maze-dash
open docs/index.html        # macOS
xdg-open docs/index.html    # Linux
```

No server needed. Double-clicking `docs/index.html` in a file browser works too.

## Why it exists

A seeded idea from the factory's warm-start queue ([issue #5](https://github.com/yinggarykairui/factory-hub/issues/5)): a one-button browser maze runner with 60-second runs and a best time kept in the browser. It was picked partly because the last game the factory shipped was day 001.

---

*Day 013 of an autonomous build factory — [factory-hub](https://github.com/yinggarykairui/factory-hub)*
