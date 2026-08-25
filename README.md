# maze-dash

A one-button maze runner: the runner never stops, and the only thing you do is choose which way it turns.

![A 13 by 13 maze in thin dark lines on off-white paper. A grey trail fills the bottom left of the board, running back and forth along the lowest rows and doubling back on itself several times; it is darkest where the runner is and fades towards its oldest end. The amber runner is a filled dot at that dark end, in the third column from the left and about three quarters of the way down. A dashed amber line runs up from the runner, turns right, drops back down, steps right again, then drops one last cell to an amber arrow a little left of centre and about two thirds of the way down, pointing left. A small ringed cell sits against the right-hand wall about four fifths of the way down. The HUD above the board reads 1 cleared and 22.7 s left, the button below it says Turn, and the hint under the button reads: Space, Enter, or tap: move the arrow to the next exit.](screenshot.png)

**[Live demo](https://yinggarykairui.github.io/maze-dash/)**

## What it does

The runner moves at a fixed speed and never stops. It takes forced turns and reverses out of dead ends by itself. It needs you only at junctions. An amber arrow on the junction ahead marks the exit it takes. One press (`Space`, `Enter` or a tap) moves it to the next exit. A dashed line links a distant arrow to the runner. The grey trail is the last seven seconds of its path, the only record of where you went.

One rule beats the rest. At each junction, take the exit on the runner's right as it arrives; if there is none, take the one ahead. That always reaches the ringed cell: the maze has no loops and one wall runs past every cell. Steering for the ring is the trap: it walks into dead ends and scores worse than not playing. The rule is on a card on the title and results screens, the trap only here. The hint under the button names the keys, on all three screens.

Reach the ring and the maze is cleared. The board warms towards amber for a fifth of a second, over the next maze already drawn. A run lasts 60 seconds; the score is how many mazes you cleared. Your best score and fastest maze live in `localStorage` on your own machine. There is no sound.

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
