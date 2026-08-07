# maze-dash

A one-button maze runner: the runner never stops, and the only thing you do is choose which way it turns.

![A 13 by 13 maze in thin black lines on off-white paper. A grey trail winds through the top half of the board, doubling back on itself several times, darkest where the runner has just been and fading out towards its oldest end. The amber runner sits against the right-hand wall at the dark end of that trail. A dashed amber line traces the corridor ahead of it, up and to the left and then back down to the right, ending at an amber arrow that points downward. A small ringed cell sits against the right-hand wall near the bottom. The HUD above reads 1 cleared and 31.9 seconds left, and the button below says Turn.](screenshot.png)

**[Live demo](https://yinggarykairui.github.io/maze-dash/)**

## What it does

The runner moves at a fixed speed on its own — it takes forced turns and reverses out of dead ends by itself, and the only moment it needs you is at a junction. As soon as it commits to one junction, an amber arrow appears on the next one showing the exit it will take; one press moves that arrow to the next exit clockwise, and whatever it points at when the runner arrives is the turn it takes. When that junction is more than one cell off, a dashed line runs back to the runner so you can tell which junction the arrow belongs to, and the grey trail behind the runner is the last seven seconds of its path — the only record you get of where you have already been. The screenshot above is a run in progress: one maze cleared, 31.9 seconds on the clock, the trail folded back over itself where the route went wrong. Reach the ringed cell in the right-hand wall and the maze is cleared and instantly replaced by a new one; a run lasts 60 seconds, the score is how many mazes you got through, your best score and fastest single maze are kept in `localStorage` on your own machine, `Space` and `Enter` and a tap anywhere on the maze all do the same one thing, and there is no sound.

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
