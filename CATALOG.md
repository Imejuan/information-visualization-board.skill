# Style Catalogue

Two styles, same layout capability — different visual temperature and aesthetic register.

All optimized for long-form boards: technical diagrams, paper explanations, meeting notes,
document graphics, and PPT-style layouts.

---

## Style 1 — Deep Tech

**Warm gray canvas. Vivid violet + lime green. Editorial-technical.**

Warm gray `#E8E8E3` canvas. Boards are white with bold `2px solid #1A1A1A` borders. Vivid violet
`#3D32E8` does all the accent work: key nodes, era tags, SVG connectors. Lime green `#C9F135` marks
new additions and callout highlights. Dark `#1A1A1A` blocks group related content with white text.
No gradients, no shadows. Typography: Outfit + Noto Sans SC.

| Property | Value |
|---|---|
| Canvas | `#E8E8E3` warm gray |
| Board bg | `#FFFFFF` white + `2px solid #1A1A1A` border |
| Primary accent | `#3D32E8` violet — key nodes, era tags, connectors |
| Highlight accent | `#C9F135` lime — new organs, callout borders, warning chips |
| Dark blocks | `#1A1A1A` — dept/category group containers |
| Body text | `#1A1A1A` on light · `#FFFFFF` on dark |
| Formality | Medium — technical, graphic, editorial |
| Vibe | Modern design agency meets structured information architecture |
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
