# Style 1 — Deep Tech

**Warm gray canvas. Vivid violet accent. High-contrast editorial-technical.**

Warm gray `#E8E8E3` canvas. Boards are white with a near-black `#1A1A1A` border (2px solid, no shadow).
Primary accent is vivid violet `#3D32E8` — used for key nodes, era/category tags, eyebrow labels, and
SVG connectors. Lime green `#C9F135` is the highlight accent — used for new/key organ labels, callout
border-lefts, and abolish/warning chips. Dark section blocks use `#1A1A1A` background with white chips.
No gradients. No glows. Typography: Outfit + Noto Sans SC.

Inspired by modern editorial design systems and clean product UI — graphic, structured, readable.

---

## Palette

| Token | Value | Usage |
|---|---|---|
| `--canvas` | `#E8E8E3` | Page / body background (warm gray) |
| `--board-bg` | `#FFFFFF` | Board / card container fill |
| `--board-border` | `#1A1A1A` | Board border — 2px solid |
| `--surface-dark` | `#1A1A1A` | Dark section blocks (dept boxes, dark cards) |
| `--surface-mid` | `#2a2a2a` | Chip bg inside dark blocks |
| `--surface-light` | `#f5f5f0` | Light inner rows, secondary panels |
| `--accent-violet` | `#3D32E8` | Primary accent — key nodes, era tags, eyebrows, SVG lines |
| `--accent-lime` | `#C9F135` | Highlight accent — new organs, callout borders, warning chips |
| `--ink-primary` | `#1A1A1A` | All body text on light surfaces |
| `--ink-on-dark` | `#FFFFFF` | Text on `--surface-dark` |
| `--ink-on-lime` | `#1A1A1A` | Text on lime green fills |
| `--ink-on-violet` | `#FFFFFF` | Text on violet fills |
| `--ink-muted` | `#666666` | Subtitles, captions |
| `--border-light` | `#dddddd` | Borders on light inner cards |

---

## Typography

```css
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Noto+Sans+SC:wght@400;500;700&display=swap');

font-family: 'Outfit', 'Noto Sans SC', -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif;
```

### Scale

| Role | Size | Weight | Color |
|---|---|---|---|
| Display / Hero | 56–72px | 800 | `--ink-primary`; key word in `--accent-violet` |
| Section title | 22–28px | 700 | `--ink-primary` |
| Board eyebrow | 11–12px | 700 | `--accent-violet`; letter-spacing 2.5px; uppercase |
| Card title / dept title | 16–20px | 700 | `--accent-lime` on dark blocks; `--accent-violet` on light |
| Body | 16–18px | 400–500 | `--ink-primary` |
| Label / tag | 12–14px | 500–700 | `--ink-primary` or `--ink-on-dark` |
| Caption / muted | 13px | 400 | `--ink-muted` |

---

## Layout rules

- **Canvas:** `#E8E8E3` full-width body. Content: `width: 100%; padding: 48px 40px 80px; box-sizing: border-box`. No `max-width`.
- **Boards:** white container `background: #FFFFFF`, `border-radius: 20px`, `border: 2px solid #1A1A1A`, `padding: 36px 44px 40px`. No top accent line, no box-shadow.
- **Board eyebrow:** `font-size: 11px; font-weight: 700; letter-spacing: 2.5px; color: #3D32E8; text-transform: uppercase;` with a small lime dot `::before` (`width: 5px; height: 5px; background: #C9F135; border-radius: 50%; border: 1px solid #1A1A1A`).
- **Dark section blocks:** `background: #1A1A1A; border-radius: 14px; padding: 22px 24px`. Use for dept groups, category containers. Title in `#C9F135`, chips inside use `background: #2a2a2a; border: 1.5px solid #444; color: #FFFFFF`.
- **Light inner rows / panels:** `background: #f5f5f0; border: 1.5px solid #ddd; border-radius: 10px`. Chips inside use `background: #FFFFFF; border: 1.5px solid #ccc; color: #1A1A1A`.
- **Key nodes (emperor, top-level):** `background: #3D32E8; border-radius: 12–14px; border: 2px solid #1A1A1A; color: #FFFFFF; font-weight: 800`.
- **Era / category tags:** `background: #3D32E8; border-radius: 20px; color: #FFFFFF; font-weight: 700; padding: 5px 16px`.
- **Accent chips — new/key:** `background: #C9F135; border: 1.5px solid #1A1A1A; color: #1A1A1A; font-weight: 700`.
- **Warning / abolished chips:** `background: #1A1A1A; border-radius: 8px; color: #C9F135; font-weight: 500`.
- **Callout boxes:** `background: #f5f5f0; border-left: 3px solid #C9F135; border-radius: 10px`.
- **SVG connectors:** lines use `stroke="#3D32E8" stroke-width="2"`. Arrow triangles use `fill="#3D32E8"`. Always place SVG arrowheads **inside** the viewBox — extend viewBox height to fit the full arrowhead; never rely on `overflow:visible` to show cut-off polygons. Use `style="display:block"` on SVG elements used as section dividers.
- **Section connectors between boards:** vertical line + downward triangle, both `#3D32E8`, `display:flex; flex-direction:column; align-items:center`.
- **No gradients** anywhere. No `box-shadow`. No `border-radius` above 20px on boards.
- **Visualize data as graphics, not text blocks.** Prefer SVG flow diagrams, timeline rows, bar indicators, and stat callouts over plain card+text. Any sequence, process, or comparison should be drawn.
- **Spacing:** 8px grid. Board gap 24px. Inner card gap 8–16px. Section gap 40–56px.
- **Grid:** mix 2-, 3-column grids. Use `align-items: stretch` for equal-height cards.
- **No emoji.** No decorative emoji anywhere.

---

## Mood reference

Warm gray page, white boards with bold black borders, vivid violet accents on key nodes and labels,
lime green for highlights and new additions. Dark near-black blocks for grouped content with white text.
Clean, graphic, editorial — like a structured brand system or product design spec sheet.

Think "modern design agency meets structured information architecture."

---

## Do / Don't

| Do | Don't |
|---|---|
| Warm gray canvas `#E8E8E3` | Dark or colored canvas |
| White boards with `2px solid #1A1A1A` border | Boards with glow / shadow / gradient top-line |
| Violet `#3D32E8` for key nodes and connectors | Cyan or blue gradients |
| Lime `#C9F135` for new/highlight chips | Warm colors (orange, red) or pastel fills |
| Dark `#1A1A1A` blocks for grouped dept/category content | Blue or colored section blocks |
| SVG arrowheads fully inside viewBox | Arrowheads cut off by viewBox edges |
| Outfit + Noto Sans SC | Serif or display fonts |
| Bold hierarchy: violet key node, dark section blocks, lime highlights | Uniform color weight, no hierarchy |
