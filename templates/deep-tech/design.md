# Style 1 — Deep Tech

**Deep-space navy canvas. Cyan-blue gradient. Technical and cinematic.**

Dark navy `#060A14` canvas, card surfaces in `#0A0F1E` / `#131B2E`, primary accent is a cyan-to-blue
gradient `#22dce0 → #4DA6FF`. Section headers use a vivid `#0396FF → #ABDCFF` gradient fill.
Hard cyan glow effects (`box-shadow: 0 0 24px rgba(34,220,224,0.08)`). Typography: Outfit + Noto Sans SC.
No emoji anywhere.

Inspired by deep-space dashboards, scientific data visualization, and technical editorial design.

---

## Palette

| Token | Value | Usage |
|---|---|---|
| `--canvas` | `#060A14` | Page / body background |
| `--surface-0` | `#0A0F1E` | Board / card container fill |
| `--surface-1` | `#131B2E` | Inner cards, data panels |
| `--surface-2` | `#1E2940` | Nested surfaces, track fills |
| `--accent-cyan` | `#22dce0` | Primary accent — borders, labels, glows, dots |
| `--accent-blue` | `#4DA6FF` | Secondary accent — arrow labels, links |
| `--accent-purple` | `#8B5CF6` | Tertiary — complexity/high end of scales |
| `--gradient-header` | `linear-gradient(135deg, #0396FF 0%, #ABDCFF 100%)` | Section header fills |
| `--gradient-text` | `linear-gradient(135deg, #4DA6FF 0%, #22dce0 100%)` | Hero text highlights |
| `--gradient-fill` | `linear-gradient(135deg, #0396FF 0%, #22dce0 100%)` | CTA blocks, buttons, stat cards |
| `--ink-primary` | `#FFFFFF` | Titles, numbers on dark surfaces |
| `--ink-secondary` | `#AABBD4` | Body text on dark surfaces |
| `--ink-muted` | `#8A9BB5` | Captions, metadata |
| `--ink-dim` | `#4A6080` | Labels, subtitles, axis text |
| `--border-cyan` | `rgba(34,220,224,0.12)` | Default card border |
| `--border-cyan-active` | `rgba(34,220,224,0.3)` | Highlighted card border |
| `--warn` | `#fbbf24` | Warning / caution callouts |
| `--success` | `#34d399` | Positive / good state pills |

---

## Typography

```css
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Noto+Sans+SC:wght@400;500;700&display=swap');

font-family: 'Outfit', 'Noto Sans SC', -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif;
```

### Scale

| Role | Size | Weight | Color |
|---|---|---|---|
| Display / Hero | 56–72px | 800 | `--ink-primary`; key word uses `--gradient-text` via `-webkit-background-clip` |
| Section title | 28–36px | 700 | `--ink-primary` |
| Board eyebrow | 13px | 700 | `--accent-cyan`; letter-spacing 2.5px; uppercase |
| Card title | 18–26px | 700 | `--ink-primary` |
| Body | 16–18px | 400–500 | `--ink-secondary` |
| Label / tag | 11–13px | 700 | `--accent-cyan` or `--ink-dim`; letter-spacing 2px; uppercase |
| Caption | 13–14px | 400 | `--ink-muted` |

---

## Layout rules

- **Canvas:** `#060A14` full-width body. Content column is **1600px** centered, `padding: 48px 0 80px`.
- **Boards:** dark container `background: #0A0F1E`, `border-radius: 20px`, `border: 1px solid rgba(34,220,224,0.12)`, `padding: 56px 60px 60px`. Top accent line: `height: 2px; background: linear-gradient(90deg, #0396FF 0%, #22dce0 50%, transparent 100%)` using `::before`.
- **Board eyebrow:** `font-size: 13px; font-weight: 700; letter-spacing: 2.5px; color: #22dce0; text-transform: uppercase;` with a glowing dot `::before` (`width: 6px; height: 6px; background: #22dce0; border-radius: 50%; box-shadow: 0 0 8px #22dce0`).
- **Inner cards:** `background: #131B2E; border-radius: 10–16px; border: 1px solid rgba(34,220,224,0.12)`.
- **Section headers:** `background: linear-gradient(135deg, #0396FF 0%, #ABDCFF 100%); border-radius: 8px; padding: 18px 28px`.
- **Highlight / callout boxes:** `background: linear-gradient(135deg, rgba(3,150,255,0.2) 0%, rgba(34,220,224,0.08) 100%); border: 1px solid rgba(34,220,224,0.3); border-left: 3px solid #22dce0; border-radius: 10px`.
- **Accent fills (CTAs, stat cards, key nodes):** `background: linear-gradient(135deg, #0396FF 0%, #22dce0 100%)` with `box-shadow: 0 8px 32px rgba(3,150,255,0.2)`.
- **Pills / tags:** `background: rgba(34,220,224,0.08); border: 1px solid rgba(34,220,224,0.2); border-radius: 100px; color: #22dce0`. Variant good: `rgba(16,185,129,...)` green. Variant warn: `rgba(251,191,36,...)` yellow.
- **Dividers:** `height: 1px; background: linear-gradient(90deg, rgba(34,220,224,0.4) 0%, rgba(34,220,224,0) 100%)`.
- **Prose text between boards:** white text on `#060A14`. Use `.callout` highlight boxes for key quotes. Use `.pill-row` pill lists for pros/cons.
- **Spacing:** 8px grid. Board gap 48px. Inner card gap 16–24px. Section gap 56px.
- **Grid:** mix 2-, 3-, 5-column grids freely. Use `align-items: stretch` for equal-height cards.
- **No emoji.** No decorative emoji anywhere on the canvas.

---

## Mood reference

Deep-space navy canvas, cyan-blue gradient accents, cards with subtle cyan glow borders. Section headers
are vivid gradient bands. Arrows and connectors use `rgba(34,220,224,0.3)` lines with small SVG triangle
arrowheads (do NOT use font-based icons). Number-heavy layouts use large `font-size: 48–72px; font-weight: 800; color: #22dce0` numerals.

Think "mission control dashboard meets technical white paper."

---

## Do / Don't

| Do | Don't |
|---|---|
| Deep navy canvas `#060A14` | Light or white backgrounds |
| Cyan `#22dce0` gradient accents | Warm colors, orange, red |
| Hard cyan glow borders on key cards | Blurred shadows |
| Mix dark surface layers (#0A0F1E / #131B2E / #1E2940) | Flat single-layer dark backgrounds |
| Gradient text for hero titles | Solid color hero text |
| SVG inline arrows / triangles for flow diagrams | Emoji arrows or font icons |
| Outfit + Noto Sans SC | Serif or display fonts |
| Bold hierarchy: huge numbers, gradient headers | Uniform weight, no visual hierarchy |
