---
version: 1.0
name: Blush Field
renderer: feishu-svg-whiteboard
description: >
  Blush #FFEDEB as the full canvas. Red #E62828 is the single accent — used sparingly for one
  title bar, one key number, or a thin rule. Body text is ink #333333; secondary text is #666666.
  White is used for card surfaces that sit on top of the blush page. This is the most restrained
  style: warm and quiet, almost monochrome in feel — the red accent makes a single strong statement.

# ── COLOR ────────────────────────────────────────────────────
colors:
  blush: "#FFEDEB"       # canvas — the full page background
  white: "#FFFFFF"       # card/panel surfaces that float on the blush canvas
  red: "#E62828"         # SINGLE accent — title bar, the one key number, or a single thin rule; use once or twice per board
  ink: "#333333"         # all body text, headings, labels
  grey: "#666666"        # secondary labels, captions
  light-grey: "#999999"  # tertiary captions only
  # Blush canvas + white cards + one red accent. Restraint is the identity: red appears once as a signature.

# ── TEXT COLOR ───────────────────────────────────────────────
text-rules:
  on-blush: "ink #333333 — the only choice on the warm canvas"
  on-white-card: "ink #333333 for body; grey #666666 for secondary"
  on-red: "white #FFFFFF only"
  rule: "Red accent appears at most twice on the whole board. Never fill large areas with red — it should feel like a signature stamp, not a paint bucket."
  note: "Text color is reliable on the live board; the exported PNG may render text color differently — judge via --output_as raw or the live board, not the PNG."

# ── STROKE & CORNERS ─────────────────────────────────────────
stroke:
  structural: "minimal or none — let color blocks do the separation work"
  rule: "thin red rule is fine as one divider; no other stroke-based decorations"
  radius: "medium — rx 4 to 10; cards feel slightly soft"
---

# Blush Field — Brand Feishu Whiteboard Design System

The warmest and quietest of the brand styles. A full blush `#FFEDEB` page, with white cards
floating on it and a single red `#E62828` accent that acts as a signature — one strong statement,
no more. All text is dark ink. This style works best for reflective, editorial content: summaries,
key insight boards, quiet reports.

## Usage pattern

- **Page background:** full blush fill
- **Content cards:** white panels on the blush, generous padding, ink text
- **The red accent:** one title bar, or one large key number, or one thin top rule — pick one role for red and use it consistently
- **Secondary text:** grey `#666666`

## Rules

This template is the **palette + mood** only. Every medium constraint (native shapes, opacity ignored, the text-color export caveat, no gradients/filters/shadows, reflow) and the build/verify workflow live in **[`../../RULES.md`](../../RULES.md)** — read it before building.
