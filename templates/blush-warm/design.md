---
version: 1.0
name: Blush Warm
renderer: html
description: >
  Blush #FFEDEB full canvas, warm and layered. White #FFFFFF cards float on the blush page as
  content panels. Red #E62828 is the bold primary accent — header bands, key callout boxes, large
  stage numerals — used against blush so it reads warm rather than aggressive. Ink #333333 for
  all text. Approachable and editorial without sacrificing structure.
  Optimized for long-form boards: paper explanations, insight reports, document graphics, PPT.

# ── COLOR ────────────────────────────────────────────────────
colors:
  blush: "#FFEDEB"   # canvas — full page background; warm, welcoming base
  white: "#FFFFFF"   # card/panel surfaces that float on the blush canvas
  red: "#E62828"     # PRIMARY accent — header bands, key callout boxes, large stage numerals; 2–3 uses per board
  ink: "#333333"     # all text everywhere
  grey: "#666666"    # secondary labels, captions, metadata
  light-grey: "#999999"  # tertiary captions only
  # Blush canvas + white cards + red accents. Red pops against blush differently than against white — warmer, bolder, still restrained.

# ── TEXT COLOR ───────────────────────────────────────────────
text-rules:
  on-blush: "ink #333333 — direct text on the blush canvas (outside cards)"
  on-white-card: "ink #333333 for body; grey #666666 for secondary"
  on-red: "white #FFFFFF — all text on red fills, at any size"
  rule: "Red accent appears 2–3 times per board. More than that dilutes the warmth. Contrast between red and blush reads bolder than red-on-white — use it as the hero, not decoration."
  note: "Text color is reliable on the live board; the exported PNG may render text color differently — judge via --output_as raw or the live board, not the PNG."

# ── STROKE & CORNERS ─────────────────────────────────────────
stroke:
  structural: "no outer frames on white cards — blush vs white contrast defines edges naturally"
  rule: "thin red divider inside a white card is fine; avoid black or grey borders"
  radius: "medium — rx 6–12 on white cards; soft and rounded"
---

# Blush Warm — Information Visualization Board Design System

The warm counterpart to Signal Red. A full blush `#FFEDEB` page with white content cards and red
`#E62828` used boldly — header bands, a key data block, large stage numerals. The contrast between
blush and red reads warmer and more editorial than red-on-white.

Suited for all long-form content types: paper explanations, insight reports, consumer content,
cultural boards, document graphics, and PPT-style layouts where a warm, approachable register is
preferred. The layered blush + white card structure creates natural depth across long scrolling layouts.

## Usage pattern

- **Page background:** full blush fill `#FFEDEB`
- **Content cards / panels:** white `#FFFFFF`, generous padding (≥ 32px), rounded corners (rx 8–12), ink text
- **Primary section header:** red fill `#E62828`, white bold text, full-width, height 48–64px
- **Key data block:** red fill, white large numeral + white caption — one strong statement per section
- **Direct text on canvas** (between cards, captions, labels): ink `#333333` on blush
- **Secondary info:** grey `#666666`
- **Long images:** stack white cards vertically on the blush canvas; consistent gutter (40–60px) between cards; one red header at the very top anchors the whole board

## Rules

This template is the **palette + mood** only. Every medium constraint (native shapes, opacity ignored, the text-color export caveat, no gradients/filters/shadows, reflow) and the build/verify workflow live in **[`../../RULES.md`](../../RULES.md)** — read it before building.
