# maze-dash

A one-button maze runner: the runner never stops, and the only thing you do is choose which way it turns.

![A 13 by 13 maze in thin dark lines on off-white paper. A grey trail loops through the top half of the board and doubles back on itself several times; it is darkest where the runner is and fades almost to paper at its oldest end. The amber runner is a filled dot at that dark end, above and to the right of the middle of the board. A dashed amber line runs down from the runner, steps right, drops a little further and runs left, ending at an amber arrow in the middle of the board that points up. A small ringed cell sits against the right-hand wall about four fifths of the way down. The HUD above the board reads 1 cleared and 30.2 s left, the button below it says Turn, and the hint under the button reads: Space, Enter, tap. Keep to the exit nearest your right.](screenshot.png)

**[Live demo](https://yinggarykairui.github.io/maze-dash/)**

## What it does

The runner never stops: it moves at a fixed speed, takes forced turns and reverses out of dead ends by itself, and the grey trail it leaves is the last seven seconds of its path — the only record you get of where you have already been. It needs you only at a junction, where an amber arrow marks the exit it will take, one press (`Space`, `Enter` or a tap) moves that arrow to the next exit, and a dashed line links the arrow back to the runner when that junction is more than one cell ahead. One rule beats the rest, and the hint under the button carries it: at every junction take the exit nearest your right — right if there is one, else straight, else left. That rule always reaches the ringed cell that clears the maze, because the maze has no loops and one wall runs past every cell; heading straight for the ring is the trap, since the direct line walks into dead ends and scores worse than never pressing at all. A run lasts 60 seconds and the score is how many mazes you cleared: each clear warms the whole board towards amber for about a fifth of a second, the next maze is already drawn underneath it, and your best score and fastest single maze are kept in `localStorage` on your own machine.

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
