---
version: 2.1
name: Tech Dark
renderer: html
description: >
  Dark navy canvas #0A0F1E, teal accent #22DCE0 as the primary accent, white #FFFFFF for all
  text. Minimal — 3 colors only. Card surfaces use a slightly lighter dark #131B2E. Gradients are
  allowed and encouraged on header bands and accent elements: linear-gradient from #ABDCFF to
  #0396FF. Tech-feel: crisp, airy dark page with glowing teal structure. No red in this style.
  Fonts: Outfit for Latin/numbers, Noto Sans SC (思源黑体) for Chinese.

# ── COLOR ────────────────────────────────────────────────────
colors:
  dark: "#0A0F1E"        # canvas — deep dark navy, the page background
  card: "#131B2E"        # card/panel surfaces that float on the dark canvas
  accent: "#22DCE0"      # PRIMARY accent — borders, rules, callout borders, key labels
  white: "#FFFFFF"       # all primary text, heading text on dark/card surfaces
  muted: "#8A9BB5"       # secondary labels, captions on dark or card backgrounds
  # Dark page + teal structure + white text. Gradients allowed on accent elements only.
  # Gradient recipe: linear-gradient(135deg, #ABDCFF 0%, #0396FF 100%)

# ── TEXT COLOR ───────────────────────────────────────────────
text-rules:
  on-dark: "white #FFFFFF for all body and headings; muted #8A9BB5 for secondary labels"
  on-card: "white #FFFFFF for body; muted #8A9BB5 for secondary labels"
  on-gradient: "white #FFFFFF always — high contrast on the #ABDCFF-to-#0396FF gradient"
  note: "In HTML, CSS gradients render accurately in browser and screenshot alike."

# ── FONTS ─────────────────────────────────────────────────────
fonts:
  latin-and-numbers: "Outfit (Google Fonts) — import via @import in <style>"
  chinese: "Noto Sans SC (思源黑体, Google Fonts) — import via @import in <style>"
  stack: "'Outfit', 'Noto Sans SC', -apple-system, 'PingFang SC', sans-serif"
  import: |
    @import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700&family=Noto+Sans+SC:wght@400;700&display=swap');

# ── STROKE & CORNERS ─────────────────────────────────────────
stroke:
  structural: "thin teal rules (#22DCE0, 1px) for row dividers inside cards; no heavy outer frames"
  card-border: "optional 1px solid rgba(34,220,224,0.15) on cards for a subtle glow edge"
  radius: "medium — border-radius 8–12px on cards; 6px on header bands; crisp but not hard"
---

# Tech Dark — Information Visualization Board Design System

Dark navy `#0A0F1E` page with `#131B2E` card panels and teal `#22DCE0` as the single structural
accent. Gradients run from `#ABDCFF` to `#0396FF` on header bands. White text throughout.
Three colors, no more.

The mood is minimal tech: deep space, clean geometry, one glowing accent. No decoration beyond
the gradient header bands and thin teal rules. Latin text and numbers use **Outfit**; Chinese
uses **Noto Sans SC** (思源黑体).

## Usage pattern

- **Page background:** `#0A0F1E` dark navy
- **Content cards:** `#131B2E`, `border-radius: 10px`, optional `1px solid rgba(34,220,224,0.15)`
- **Section header band:** `linear-gradient(135deg, #ABDCFF 0%, #0396FF 100%)`, white bold text
- **Key labels / accent numerals:** teal `#22DCE0`, large, bold — the single color pop
- **Body text:** white `#FFFFFF`; secondary labels: muted `#8A9BB5`
- **Row dividers inside cards:** `1px solid rgba(34,220,224,0.12)`
- **Accent rule / thin line:** `#22DCE0`, 1–2px
- **Outcome / callout block:** card surface `#131B2E` with a left border `3px solid #22DCE0`
- **Font import:** always include the `@import` for Outfit + Noto Sans SC at top of `<style>`

## Rules

This template is the **palette + mood** only. HTML medium rules and the build/verify workflow
live in **[`../../RULES.md`](../../RULES.md)** — read it before building.
