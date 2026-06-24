# Style Catalogue

Two styles, same layout capability — different visual temperature and aesthetic register.

All optimized for long-form boards: technical diagrams, paper explanations, meeting notes,
document graphics, and PPT-style layouts.

---

## Style 1 — Deep Tech

**Royal blue canvas. Cyan-blue gradient. Technical and cinematic.**

Royal blue `#0057FF` canvas with multi-layer card surfaces (`#0A0F1E` / `#131B2E`). Cyan `#22dce0`
and blue `#4DA6FF` gradient accents do all the organizing work: section header fills, border glows,
label colors. Hard gradient fills for CTA blocks. Typography: Outfit + Noto Sans SC.

| Property | Value |
|---|---|
| Canvas | `#0057FF` royal blue |
| Card surfaces | `#0A0F1E` / `#131B2E` layered dark panels |
| Primary accent | `#22dce0` cyan — borders, labels, glows |
| Secondary accent | `#4DA6FF` blue — arrows, links, secondary labels |
| Gradient header | `linear-gradient(135deg, #0396FF → #ABDCFF)` — section fills |
| Gradient fill | `linear-gradient(135deg, #0396FF → #22dce0)` — CTA, stat cards |
| Body text | `#AABBD4` on dark |
| Formality | Medium — technical, cinematic |
| Vibe | Mission control meets deep-space dashboard |
| Best for | Technical diagrams, architecture explainers, AI/science content, paper breakdowns |

Template: [`templates/deep-tech/design.md`](templates/deep-tech/design.md)

---

## Style 2 — Bold Pop

**Near-black canvas. High-contrast editorial.**

Dark canvas `#1A1A1A` meets vivid orange-red `#FF4520` and warm cream/white cards. Large rounded
corners (20–24px) on every card. Hard drop shadows in accent color (no blur). Arrow icons from
Google Material Symbols. Typography: 阿里妈妈数黑体 + Noto Sans SC fallback. No emoji.
Inspired by contemporary app editorial design.

| Property | Value |
|---|---|
| Canvas | `#1A1A1A` near-black |
| Card surfaces | `#FFFFFF` white + `#F5F0E8` warm cream |
| Primary accent | `#FF4520` orange-red — header bands, chips, callout fills, arrow buttons |
| Dark panels | `#111111` / `#2D2D2D` for contrast sections |
| Body text | `#111111` on light · `#FFFFFF` on dark/accent |
| Border radius | 20–24px on cards, 12px on chips |
| Shadow | `6px 6px 0 #FF4520` (hard, no blur) |
| Formality | Low — bold, energetic, graphic |
| Vibe | Editorial magazine meets premium app UI |
| Best for | Product launches, event posters, speaker lineups, consumer reports, social cards |

Template: [`templates/bold-pop/design.md`](templates/bold-pop/design.md)
