
# Round Goldfish — Pure CSS (HTML + CSS)

Cute, round goldfish swimming across an animated ocean with waves and bubbles.

## Structure
```text
goldfish/
├─ index.html
└─ style.css
```

## Quick Start
1. Put the HTML into `index.html` and the CSS into `style.css`.
2. In `<head>` include:
```html
<link rel="stylesheet" href="style.css" />
```
3. Open `index.html` in your browser.

## Customize
- **Fish size**: `.goldfish { --size: 190px; }`
- **Swim speed/path**: `.goldfish { animation: swim 9s linear infinite; }`
- **Tail wag**: `.tail { animation: wag .34s ease-in-out infinite alternate; }`
- **Water colors/shine**: edit `:root` → `--water1`, `--water2`, `--shine`.
- **Body palette**: edit `:root` → `--y1`, `--y2`, `--stroke`, `--cheek`.
- **Bubble speed**: `.bubble { animation: rise 7s linear infinite; }` (each `.b2..b6` overrides duration/delay).

## Notes (a11y & motion)
- Decorative items use `aria-hidden="true"`; fish has `role="img"` + `aria-label`.
- `@media (prefers-reduced-motion: reduce)` disables animations for motion‑sensitive users.

## Troubleshooting
- **No styles?** Check `<link rel="stylesheet" href="style.css" />` path.
- **Waves static?** Ensure keyframes `w` exist and `.wave` elements are present.
- **Fish off‑screen?** `.ocean { height:100vh; overflow:hidden; }` keeps the stage full‑screen; the swim anim moves from left to right.
