---
version: 1.0
name: Red Label
renderer: feishu-svg-whiteboard
description: >
  White canvas with product-tag style label chips in brand red #E62828. Key terms, categories,
  status badges, and step numbers are red filled chips with white text. Section content sits on
  white with ink #333333 body text. Blush #FFEDEB is used as a soft background wash for data
  rows or alternating sections — never for chips (chips are always red). The visual language
  feels like a product tagging system: clean, organized, scannable.

# ── COLOR ────────────────────────────────────────────────────
colors:
  white: "#FFFFFF"       # canvas and card surfaces
  red: "#E62828"         # label chips, tags, step numbers, category badges — always filled with white text
  blush: "#FFEDEB"       # alternating row fills, soft panel washes
  ink: "#333333"         # body text, section titles
  grey: "#666666"        # secondary text, descriptions under labels
  light-grey: "#999999"  # metadata, timestamps, tertiary info
  # White page + red chips + blush rows. Red is the tag system; blush is the alternating surface; chips are always small.

# ── TEXT COLOR ───────────────────────────────────────────────
text-rules:
  on-white: "ink #333333 for headings and body; grey #666666 for secondary"
  on-red-chip: "white #FFFFFF always — chips are small, must be high contrast"
  on-blush: "ink #333333 — blush rows use dark text"
  rule: "Red chips should be small (pill or rect, rx 4–14). Reserve large red fills for the top header bar only, if used."
  note: "Text color is reliable on the live board; the exported PNG may render text color differently — judge via --output_as raw or the live board, not the PNG."

# ── STROKE & CORNERS ─────────────────────────────────────────
stroke:
  structural: "minimal — rely on chip color and subtle blush row fills for structure"
  rule: "thin grey #999999 border on white cards if separation is needed (stroke-width 1)"
  radius: "chips: rx 4–14 (pill feel); cards/sections: rx 0–6"
---

# Red Label — Brand Feishu Whiteboard Design System

White page with red label chips as the organizing system: step numbers, category tags, status
badges — anything that classifies or anchors content uses a small red `#E62828` filled chip with
white text. Sections may alternate between white and blush `#FFEDEB` row fills. Works well for
process flows, feature lists, comparison tables, and any board that needs a scannable label system.

## Usage pattern

- **Label chips / tags / step numbers:** red fill `#E62828`, white text, rx 8–14
- **Section header (optional):** red fill, white text, full-width band at top of section
- **Alternating rows / panels:** blush `#FFEDEB` and white, ink text
- **Body text:** ink `#333333`; secondary descriptions: grey `#666666`

## Rules

This template is the **palette + mood** only. Every medium constraint (native shapes, opacity ignored, the text-color export caveat, no gradients/filters/shadows, reflow) and the build/verify workflow live in **[`../../RULES.md`](../../RULES.md)** — read it before building.
