# Simulacrum archive

Saved 6 November 2026. Open `index.html` in a browser to see the whole system. `README.md` is the brand book.

## Contents

- `index.html`: a single-file preview of the brand book, colours, type, spacing and every component, with a switch between Ayre and Pyre. It carries its own fonts and styles, and it keeps working if moved out of this folder.
- `tokens.json`: every colour, type style, spacing, radius and shadow value, for both leanings. This is the source of truth.
- `tokens.css`: the same values as CSS variables.
- `components/bundle.css`: the `sim-` component styles.
- `components/<Name>/`: a README and a preview for each component.
- `fonts/`: Latin subsets of the three typefaces, their licences, and `fonts.css`.
- `design-system.json`: the name and settings used by the design system page. Not needed outside it.

## Use it

Load these in order. No network is needed.

```html
<link rel="stylesheet" href="fonts/fonts.css">
<link rel="stylesheet" href="tokens.css">
<link rel="stylesheet" href="components/bundle.css">
```

Choose the leaning on the root element: `<html data-theme="ayre">` or `<html data-theme="pyre">`. Ayre is the default.

## Previews

Use `index.html` to view the components. The separate `preview.html` files were made to run inside the design system page, which supplied the stylesheets, so they appear unstyled if opened directly.
