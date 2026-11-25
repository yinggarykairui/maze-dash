# maze-dash

A one-button maze runner: the runner never stops, and the only thing you do is choose which way it turns.

![A 13 by 13 maze in thin dark lines on off-white paper. A grey trail winds through the lower-left quarter, an L down the left side and a few back-and-forth turns, darkest where the runner is. The amber runner sits at that dark end, left of centre and just below the middle: a filled dot with a short nose pointing left, the way it is travelling. A dashed amber line leaves the runner, loops right and up and back down, and ends at an amber arrow one row below, pointing right. A small ringed cell sits against the right-hand wall a little above centre. The HUD above the board reads 0 cleared and 54.9 s left, the button below says Turn, and the hint under it reads: Space, Enter, or tap: move the arrow to the next exit.](screenshot.png)

**[Live demo](https://yinggarykairui.github.io/maze-dash/)**

## What it does

The runner moves at a fixed speed and never stops. It takes forced turns and reverses out of dead ends by itself. It needs you only at junctions. The amber runner carries a small nose that points the way it is going, so you can read its heading — and the rule below — straight off the board. An amber arrow on the junction ahead marks the exit it takes. One press (`Space`, `Enter` or a tap) moves it to the next exit. A dashed line links a distant arrow to the runner. The grey trail is the last seven seconds of its path, the only record of where you went.

One rule beats the rest. At each junction, take the exit on the runner's right as it arrives; if there is none, take the one ahead. That always reaches the ringed cell: the maze has no loops and one wall runs past every cell. Steering for the ring is the trap: it walks into dead ends and scores worse than not playing. The card on the title and results screens names the ringed cell as the goal and states the rule; the trap is only here. With the runner's heading drawn, "the runner's right" reads off the board instead of off a sentence. The hint under the button names the keys, on all three screens.

Reach the ring and the maze is cleared. The board warms towards amber for a fifth of a second, over the next maze already drawn. A run lasts 60 seconds; the score is how many mazes you cleared. Your best score and fastest maze live in `localStorage` on your own machine. There is no sound. Every mark on the board is drawn in the page: no images, no fonts, no third-party assets. The screenshot above was captured from this build.

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
