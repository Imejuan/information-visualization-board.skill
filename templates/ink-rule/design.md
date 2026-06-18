---
version: 1.0
name: Ink Rule
renderer: feishu-svg-whiteboard
description: >
  White canvas, text-first, editorial. Red #E62828 appears only as thin horizontal rules between
  sections — never as a fill. Typography carries the structure: large bold ink #333333 for titles,
  regular ink for body, grey #666666 for secondary labels. Blush #FFEDEB is reserved for a single
  quiet highlight box (a key quote or a data pull-quote). No color fills, no header bands —
  the red lines are the only color element on the board.

# ── COLOR ────────────────────────────────────────────────────
colors:
  white: "#FFFFFF"       # canvas — clean white page
  red: "#E62828"         # RULES ONLY — thin horizontal lines as section dividers; no fills
  blush: "#FFEDEB"       # one pull-quote or highlight box only
  ink: "#333333"         # all text — titles, body, everything
  grey: "#666666"        # secondary labels, captions, metadata
  light-grey: "#999999"  # tertiary text only
  # White page + ink type + red lines only. No fills. Typography is the structure; red rules are the only color.

# ── TEXT COLOR ───────────────────────────────────────────────
text-rules:
  on-white: "ink #333333 always; grey #666666 for secondary"
  on-blush: "ink #333333 — blush is too light for anything but dark text"
  rule: "Red is a line color, never a text color or fill color. The board has no colored fills at all except the single optional blush pull-quote box."
  note: "Text color is reliable on the live board; the exported PNG may render text color differently — judge via --output_as raw or the live board, not the PNG."

# ── STROKE & CORNERS ─────────────────────────────────────────
stroke:
  structural: "thin red horizontal rules (stroke-width 1, #E62828) as the only structural element between sections"
  rule: "no border frames; no column rules; one style of line only"
  radius: "none or minimal (rx 0–4) — crisp and editorial"
---

# Ink Rule — Brand Feishu Whiteboard Design System

The most restrained style. White page, dark ink, thin red rules. Nothing else. Structure comes
entirely from typography (size and weight contrast) and the thin red horizontal lines between
sections. Use for content-dense boards — meeting notes summaries, text-heavy analyses, or any
board where the content is the design.

## Usage pattern

- **Page:** pure white
- **Section separator:** single thin red horizontal rule (`stroke="#E62828"`, `stroke-width="1"`)
- **Section title:** large bold ink (e.g. `font-size="32" font-weight="700"`)
- **Body:** regular ink (e.g. `font-size="20" font-weight="400"`)
- **Secondary labels:** grey `#666666`
- **Pull-quote (one per board):** blush fill `#FFEDEB`, ink text, no border

## Rules

This template is the **palette + mood** only. Every medium constraint (native shapes, opacity ignored, the text-color export caveat, no gradients/filters/shadows, reflow) and the build/verify workflow live in **[`../../RULES.md`](../../RULES.md)** — read it before building.
