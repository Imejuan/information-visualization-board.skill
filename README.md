# Information Visualization Board

A Claude Code skill for building clean, self-contained HTML visualization pages — technical explainers, paper breakdowns, meeting notes, event posters, and more.

Output is always a **single HTML file**: all styles inline, no dependencies, opens in any browser, ready to screenshot or share.

---

## Two Styles

| # | Style | Canvas | Vibe | Best For |
|---|-------|--------|------|----------|
| 1 | **Deep Tech** | `#060A14` deep space navy | Cyan-blue gradient, glowing borders, cinematic | Technical diagrams, AI/science content, architecture explainers |
| 2 | **Bold Pop** | `#1A1A1A` near-black | High-contrast orange-red, large rounded corners, editorial | Event posters, product launches, social cards |

---

## What It Produces

- Fixed **1600px** wide, height auto — designed for long-form content
- Interleaved prose + diagram boards (text between visuals)
- Inline SVG diagrams — no chart libraries, no JS dependencies
- CJK + Latin mixed typography, no render issues

---

## Usage with Claude Code

This is a [Claude Code skill](https://docs.anthropic.com/en/docs/claude-code). Drop the folder into `~/.claude/skills/` and invoke it with:

```
/information-visualization-board
```

Claude will ask what content you want to visualize, show you the two style options, then build and screenshot the HTML file.

---

## File Structure

```
information-visualization-board/
├── SKILL.md                      # Skill entry point & conversation flow
├── CATALOG.md                    # Style overview with palette tables
├── RULES.md                      # Hard rules for HTML output
└── templates/
    ├── deep-tech/design.md       # Style 1 — palette, typography, layout rules
    └── bold-pop/design.md        # Style 2 — palette, typography, layout rules
```

---

## Examples

**Deep Tech** — multi-agent coordination patterns explainer  
**Bold Pop** — same content, high-contrast editorial layout

Both outputs are single `.html` files, screenshot-ready at 1600px width.
