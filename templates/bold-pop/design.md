# Style 3 — Bold Pop

**High-contrast editorial. Bold, punchy, graphic.**

Inspired by contemporary editorial design: near-black canvas with vivid orange-red as the primary
energy color, warm cream for content panels, and pure white text. Large rounded corners (16–24px)
on every card. Hard shadow blocks (no blur) for depth. Arrow icons from Google Material Symbols
(`north_east` ↗). Typography: 阿里妈妈数黑体 (AliMama ShuHei) via CSS @font-face / CDN —
fallback to system-ui. No emoji anywhere.

---

## Palette

| Token | Value | Usage |
|---|---|---|
| `--canvas` | `#1A1A1A` | Page background |
| `--surface-0` | `#FFFFFF` | Primary card / panel fill |
| `--surface-1` | `#F5F0E8` | Warm cream panel, secondary cards |
| `--surface-accent` | `#FF4520` | Orange-red accent fill — headers, callout blocks, tag pills, buttons |
| `--surface-dark` | `#111111` | Near-black panels for contrast |
| `--surface-mid` | `#2D2D2D` | Mid-dark panel |
| `--ink-primary` | `#111111` | Title text on light surfaces |
| `--ink-secondary` | `#444444` | Body text on light surfaces |
| `--ink-muted` | `#888888` | Metadata / caption on light surfaces |
| `--ink-on-accent` | `#FFFFFF` | Text on orange-red fills |
| `--ink-on-dark` | `#FFFFFF` | Text on near-black fills |
| `--border-radius` | `20px` | Default card radius — use 24px for large cards, 12px for small chips |
| `--shadow` | `6px 6px 0 #FF4520` | Hard drop shadow (no blur) on white cards for graphic pop |

---

## Typography

```css
@import url('https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200&display=swap');
@font-face {
  font-family: 'AliMamaShuHei';
  src: url('https://puui.qpic.cn/fans_admin/0/3_923451544_1718000000/0') format('woff2');
  /* Fallback — the user's system may have it installed */
}
/* Primary font stack */
font-family: 'AliMamaShuHei', 'Noto Sans SC', -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif;
```

> **Note on AliMama ShuHei:** Because this font may not be available via a reliable CDN, load it
> from the official Alibaba Fonts URL if available, otherwise fall back to Noto Sans SC.
> In all cases, import `Noto Sans SC` from Google Fonts as the guaranteed CJK fallback:
> `@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;700;900&display=swap');`

### Scale

| Role | Size | Weight | Color |
|---|---|---|---|
| Display / Hero | 64–80px | 900 | `--ink-primary` or `--ink-on-dark` |
| Section title | 40–48px | 700 | `--ink-primary` or `--ink-on-dark` |
| Card title | 28–32px | 700 | `--ink-primary` |
| Body | 16–18px | 400 | `--ink-secondary` |
| Label / tag | 12–14px | 700 | uppercase, letter-spacing 1–2px |
| Caption | 13px | 400 | `--ink-muted` |

---

## Layout rules

- **Canvas:** `#1A1A1A` full-width background. Content column is 1400px centered.
- **Cards:** large `border-radius: 20–24px`. White or cream surface. Hard shadow `6px 6px 0 #FF4520` for key cards. Dark cards have no shadow.
- **Grid:** use asymmetric grids — e.g. 2:1, 3-column mixed, or stacked. Avoid rigid equal grids.
- **Accent blocks:** orange-red `#FF4520` fills for header bands, numbered labels, chips, arrow buttons.
- **Arrows:** use inline SVG arrow inside a small circle button `border-radius: 50%`. On dark/accent backgrounds use white circle; on light backgrounds use accent-color circle with white arrow. Example SVG arrow path: `<path d="M5 15L15 5M15 5H7M15 5V13" stroke="#FFFFFF" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>` in a 20×20 viewBox. Do NOT use Material Symbols or any font-based icons — they may fail to load. Use SVG only.
- **No emoji.** No decorative emoji characters anywhere on the canvas.
- **Hard shadow only.** Never use `blur` in box-shadow. The signature look is `6px 6px 0 <color>`.
- **Spacing:** 8px grid. Sections separated by 40–64px gap.
- **Prose alignment:** All prose/text sections (hero, section labels, body paragraphs, tag rows) must be **left-aligned with the cards** — never centered. Use `margin: 0 0 56px` (not `margin: 0 auto`). The content column is already centered; prose inside it must align to its left edge.

---

## Mood reference

The image shows: near-black backgrounds, vivid orange-red `#FF4520` accent, cream/white cards with large rounded corners, hard shadows in accent color, black pill navigation bars, small circle arrow buttons, editorial bold typography with a mix of light and dark panels. Think "premium app UI meets editorial magazine."

---

## Do / Don't

| Do | Don't |
|---|---|
| Large rounded corners (20–24px) everywhere | Sharp corners or small radius |
| Hard drop shadows in orange-red | Blurred shadows |
| Orange-red accent on near-black canvas | Pastel colors or gradients |
| Mix dark + light panels in the same section | All-same-surface monotone layouts |
| Arrow icon from Material Symbols | Emoji arrows or unicode arrows as connectors |
| 阿里妈妈数黑体 / Noto Sans SC | Serif fonts or display fonts not in the palette |
| Bold hierarchy: huge numbers, heavy titles | Uniform weight — no hierarchy |
