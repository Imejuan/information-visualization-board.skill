---
version: 1.0
name: Block Red
renderer: feishu-svg-whiteboard
description: >
  White canvas with bold red #E62828 filled rectangular blocks as section headers. Each section
  starts with a full-width or column-width red header block containing white text. The body content
  sits on white below. Blush #FFEDEB is used for one highlighted key data block or a secondary
  panel — distinct from the red block but warm. High contrast, punchy, and still minimal — the
  structure is very clear because red blocks announce each section visibly.

# ── COLOR ────────────────────────────────────────────────────
colors:
  white: "#FFFFFF"       # canvas and body content area
  red: "#E62828"         # section header blocks — bold, full-width or column-width fills
  blush: "#FFEDEB"       # one key highlight block (not a section header — that role belongs to red)
  ink: "#333333"         # body text, labels inside white areas
  grey: "#666666"        # secondary labels and captions
  # White body + red section headers + one blush accent. Red blocks define structure; blush adds a single warm highlight.

# ── TEXT COLOR ───────────────────────────────────────────────
text-rules:
  on-white: "ink #333333 for all body and headings"
  on-red-block: "white #FFFFFF — section header text; keep it short and bold (font-weight 700)"
  on-blush: "ink #333333"
  rule: "Red blocks are HEADERS, not content areas. No body text inside a red block — just the section title. Body content always sits on white below."
  note: "Text color is reliable on the live board; the exported PNG may render text color differently — judge via --output_as raw or the live board, not the PNG."

# ── STROKE & CORNERS ─────────────────────────────────────────
stroke:
  structural: "no extra borders needed — red header blocks already define sections clearly"
  rule: "avoid additional rules or dividers when red blocks are present; they create visual noise"
  radius: "rx 0–4 on red header blocks; sharp and architectural"
---

# Block Red — Brand Feishu Whiteboard Design System

White page structured by bold red `#E62828` header blocks. Each section is introduced by a
rectangular red band with white title text (short, bold). Body content follows on white with ink
text. One blush `#FFEDEB` panel adds warmth as a key data highlight. Works well for multi-section
reports, feature breakdowns, and anywhere a clear section structure matters.

## Usage pattern

- **Section header block:** red fill `#E62828`, full-width rect, white bold text, rx 0–4, height ≈ 48–60px
- **Body area below each header:** white, ink text `#333333`, generous padding
- **Key highlight panel:** one blush `#FFEDEB` block with ink text — used once, not repeated
- **Secondary labels:** grey `#666666`

## Rules

This template is the **palette + mood** only. Every medium constraint (native shapes, opacity ignored, the text-color export caveat, no gradients/filters/shadows, reflow) and the build/verify workflow live in **[`../../RULES.md`](../../RULES.md)** — read it before building.
