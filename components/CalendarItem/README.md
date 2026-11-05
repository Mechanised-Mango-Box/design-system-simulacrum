# CalendarItem

A calendar entry, which people can colour themselves.

Use `.sim-cal-block` for a fitted task, which defaults to `slate`. Add `--event` for events, `--ok` for a task that needs approval, and `--due` for an all-day deadline. To apply an item colour, set `background` to `steel`, `moss`, `amber`, `rust`, `plum` or `slate`.

The `hot` border on `--ok` stays on top of any item colour. Offer colours with `.sim-swatch` buttons in a `.sim-swatches` row, using `.sim-swatch--default` for the default and `aria-pressed` for the current choice. The consumer positions blocks and sets their height. Keep the minimum height at 24px.
