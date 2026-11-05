Simulacrum is a design system for dense, dark interfaces such as dashboards, consoles and internal tools. It's a stripped-back tactical HUD where colour only appears when it means something. It takes its feel from mech-game interfaces and uses no assets from any game.

## Leanings

Simulacrum is the overall style. It comes in two leanings, which set the accent and the tint of everything around it:

- **Ayre** is the default: an icy blue `accent` over cool-tinted neutrals.
- **Pyre** is the warm leaning: a gold `accent` over warm-tinted neutrals, with `hot` shifted redder and darker so the two stay distinct.

Each leaning tints its whites, blacks and greys toward its accent, keeping the same lightness so contrast holds. The item colours `steel`, `moss`, `amber`, `rust` and `plum` stay the same in both, because people choose them. Type, spacing and every component are shared. Set the leaning on the root element with `data-theme="ayre"` or `data-theme="pyre"`.

## Using this system

Load the three Google Fonts below, then the tokens and `components/bundle.css`. Build screens from the `sim-` classes in the component cards. Never write a raw colour, radius or font stack in a screen.

```html
<link href="https://fonts.googleapis.com/css2?family=Saira+Semi+Condensed:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&family=Source+Sans+3:wght@400;500;600;700&display=swap" rel="stylesheet">
```

**Adopting it in a project.** Decide what the two signals mean in your project before building screens, and write that down with the project. Choose one leaning for the whole product.

## Content fundamentals

- Write plainly, in short sentences. Tell people what happened and what to do next.
- Address the reader as "you".
- Use sentence case in source text. Labels become uppercase through styling, so write "Save changes", not "SAVE CHANGES".
- Name things the same way everywhere. Use a project's own terms exactly and consistently.
- Show dates in full, such as "Thursday 5 November", and times in 24-hour form, such as "09:30".
- Use the middle dot to join short facts: "Due Friday · 15 min".
- Mark missing content with a visible placeholder such as `[YOUR TEXT]`.
- Use no emoji.

## Visual foundations

**Colour.** Stay neutral by default. Use `bg` for the screen, `panel` for containers and `raise` for anything lifted or selected. Set text in `ink`, `soft` and `dim`, in that order of importance.

Two signals carry all the meaning. Use `accent` for what the system is doing or has produced by itself, such as automated output, active processes and links. Use `hot` for what needs the person using it, such as required actions, errors, the current-time line and today's date. Never use either as decoration.

**Selection.** Selection is a raised row with a pale line on its outer edge, never a bright fill. Use `selected-vertical` in vertical lists and `selected-horizontal` in horizontal selects, with the line covering the container's border. White fills are reserved for the single strongest neutral action.

**Item colours.** People may colour their own items with `steel`, `moss`, `amber`, `rust`, `plum` or `slate`. Keep these dark, with `ink` text. Items default to `slate`.

**Type.** Set headings, navigation and controls in Saira Semi Condensed, uppercase and tracked: `screen-title`, `brand`, `nav-label`, `control-label`. Set anything people read in Source Sans 3: `body`, `item-title`, `meta`. Set times, labels and ports in JetBrains Mono: `time`, `readout`, `label`, `port`.

**Shape.** Keep every corner square (`radius-none`). Solid buttons take a `chamfer` on the top-right corner. Use no shadows except the two selection edges.

**Panels.** Every window takes corner brackets, top-left and bottom-right, using `.sim-panel`. Inner boxes, banners and graph nodes do not.

**Rulers.** Follow each screen heading with `.sim-ruler`. It is the only decorative line in the system.

**Layout.** Fix the sidebar at 196px and let content fill the rest. Keep the top-right of the screen header for modal selects, and put actions that belong to one panel inside that panel. Keep every control at least `control-height` tall.

**Focus.** Show a solid 2px `accent` outline on keyboard focus.

**Motion.** Keep motion subtle, and respect the reduced-motion setting. Animated pulses along graph edges are planned but not yet in the system.

**Backgrounds.** Screens are a flat `bg`. A faint 48px grid, using a line just lighter than `bg`, is parked as a possible later option.

## Iconography

Where a product has no logo, set its name in plain type using `brand`. The sidebar uses two-digit mono numbers in place of icons. Draw small functional glyphs, such as chevrons, as inline square-capped strokes in `currentColor`. Use no emoji.

## Graphs

Build every graph from `.sim-node`. Sinks are hollow squares on the left and sources are filled squares on the right, each with a mono name. Run edges port to port in `arrow`. Mark nodes where the system acts by itself with `.sim-node--accent`. Draw a blocked edge as a dashed `hot` line.
