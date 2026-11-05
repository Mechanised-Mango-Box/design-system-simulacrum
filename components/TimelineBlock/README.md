# TimelineBlock

One entry on the day's timeline, as an event, a fitted task or free time.

Use `.sim-block` for events, `.sim-block--task` for tasks the plan fitted, and `.sim-block--free` for free time. Put the title in `b`, metadata in `small`, and any model explanation in `em`, which renders in `accent`.

The consumer provides the time column and sets each block's height in proportion to its duration. Keep the minimum height at 68px, or 44px for free time.
