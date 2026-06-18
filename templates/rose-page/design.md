---
version: 1.0
name: Rose Page
renderer: feishu-svg-whiteboard
description: >
  Full blush #FFEDEB background with red #E62828 used boldly as the primary accent surface —
  header bands, key callout boxes, and large numerals. White #FFFFFF is used for content cards
  that float on the blush canvas, giving a layered warmth. Ink #333333 for all text. This is the
  warmest and most approachable style — blush and red together feel welcoming rather than corporate.
  Still minimal: the warmth comes from the palette, not from visual complexity.

# ── COLOR ────────────────────────────────────────────────────
colors:
  blush: "#FFEDEB"   # full page canvas — warm, welcoming background
  white: "#FFFFFF"   # content cards floating on the canvas
  red: "#E62828"     # bold fills — primary header, key callout box, large stage numerals; used more freely than in Blush Field
  ink: "#333333"     # all text
  grey: "#666666"    # secondary labels, captions
  # Blush canvas + white cards + red accents (2–3 uses). Warmest style: red contrasts against blush, reads bolder than red-on-white.

# ── TEXT COLOR ───────────────────────────────────────────────
text-rules:
  on-blush: "ink #333333 — direct text on the blush canvas (outside cards)"
  on-white-card: "ink #333333 for body; grey #666666 for secondary"
  on-red: "white #FFFFFF — all text on red fills"
  rule: "In this style, red can appear in 2–3 places (vs once in Blush Field). Still restrained — it contrasts against blush, not white, so it reads bolder."
  note: "Text color is reliable on the live board; the exported PNG may render text color differently — judge via --output_as raw or the live board, not the PNG."

# ── STROKE & CORNERS ─────────────────────────────────────────
stroke:
  structural: "no outer frames on white cards — let the color contrast (blush vs white) define edges"
  rule: "thin red divider inside a white card is fine; avoid black or grey borders"
  radius: "medium — rx 6–12 on white cards; soft and rounded"
---

# Rose Page — Brand Feishu Whiteboard Design System

The warmest brand style. A full blush `#FFEDEB` page with white cards and red `#E62828` used
boldly — header bands, a key data block, large numerals. The contrast between blush and red reads
differently from red-on-white: it feels warmer and less corporate. Use for consumer-facing content,
team culture boards, product announcements, or any context where approachability matters.

## Usage pattern

- **Page:** full blush fill `#FFEDEB`
- **Content cards:** white panels, generous padding, rounded corners (rx 8–12), ink text
- **Primary header:** red fill `#E62828`, white bold text
- **Key data block:** red fill, white large numeral + white caption
- **Secondary info on canvas (outside cards):** ink `#333333` directly on blush
- **Captions:** grey `#666666`

## Rules

This template is the **palette + mood** only. Every medium constraint (native shapes, opacity ignored, the text-color export caveat, no gradients/filters/shadows, reflow) and the build/verify workflow live in **[`../../RULES.md`](../../RULES.md)** — read it before building.
