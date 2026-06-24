# HTML Visualization — Medium Rules

These apply to **every** board, regardless of template. A template gives you a **color palette
and a mood**; this file is the **hard rules of the medium**.

## Output format

- **Single self-contained HTML file.** All CSS in a `<style>` block in `<head>`. No external
  stylesheets, no CDN links, no JavaScript (unless absolutely required for a diagram). The file
  must open correctly by double-clicking it with no internet connection.
- **No external fonts.** Use the system font stack:
  `font-family: -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif;`
  This gives clean CJK + Latin rendering on macOS, Windows, and Linux without any download.
- **Responsive width:** The page container must use `width: 100%; padding: 0 40px; box-sizing: border-box;`. Do NOT set any `max-width` or fixed `width`. Height is auto — let content define the length. Never set a fixed height on the page body.
- **No JavaScript libraries** (no Chart.js, no D3, no Vue). Use SVG inline for any chart/diagram
  shapes. Simple CSS transitions are fine if they add value; avoid heavy JS animations.

## Layout rules

- **CSS Grid and Flexbox** are the primary layout tools. Use `display: grid` for multi-column
  sections, `display: flex` for row arrangements within a section.
- **Consistent spacing system:** use multiples of 8px (8, 16, 24, 32, 40, 48, 64) for all
  padding, margin, and gap values. Never use arbitrary pixel values.
- **Generous padding inside cards/panels:** minimum 24px on all sides; 32–40px for primary panels.
- **No content flush to the page edge.** The 1400px container must have at least 40px padding on
  left and right inside it.
- **Arrows and connectors in diagrams:** use inline SVG with `<line>` + `marker-end`, or CSS
  border tricks. Never use emoji arrows (→ ➡) as structural connectors in diagrams.
- **SVG text inside shapes must be vertically centered:** set `y` to the vertical midpoint of the
  shape (e.g. rect y=38 height=28 → text y=52), and always add `dominant-baseline="middle"`.
  Never place the `y` value below the shape's bottom edge.
- **Centered text blocks must have explicit `text-align: center`** on the element itself — never
  rely on inheritance from a parent container. Hero titles, subtitles, and any centered label
  must carry their own `text-align: center` declaration.

## Typography rules

- **Hierarchy by size and weight only** — no typeface switching. Use `font-weight: 700` for
  titles and labels, `400` for body.
- **Minimum body font size: 16px.** Secondary labels minimum 13px, only on high-contrast surfaces.
- **Line height:** `1.5` for body text, `1.2` for large display titles.
- **CJK + Latin mixed text:** avoid `letter-spacing` on CJK characters (it looks wrong); apply
  `letter-spacing` only to all-caps Latin labels.
- **Text color must always contrast with its background.** Dark text on light surfaces, white text
  on dark/colored surfaces. Never put `#666` on a colored background.

## Color discipline

- Use **only the palette from the chosen template** — never introduce extra colors.
- **No CSS gradients** unless the template explicitly permits them (none of the current templates do).
- **No box-shadow with blur** on structural elements — use flat colored borders or background
  color contrast to create separation. A hard `box-shadow: 4px 4px 0 <color>` (no blur) is fine
  if the template mood calls for it.
- **No background-image, no CSS patterns.** Flat color only.
- `opacity` is fine in HTML/CSS (unlike the Feishu SVG medium) — but use it sparingly. Prefer
  solid lighter hex values over semi-transparent overlays.

## Content rules

- **Only content goes on the page — never meta text.** Do not print:
  - The user's prompt or request
  - The style/template name
  - Source citations, file names, or tool names
  - "Summary of…", "Based on…", "来源：", or any framing addressed to the reader about the artifact
  - Dates, tokens, or build metadata you were not explicitly asked to display
- A **title may name the subject** (e.g. "LLM 训练三阶段" is fine — that is the topic). Nothing
  on the page may describe the task or the source material.
- **Litmus test:** if a line is addressed to the person who asked rather than being real content
  of the artifact, delete it.

## Build and verify workflow

1. Read the chosen `templates/<slug>/design.md` for the palette and mood.
2. Write the HTML file with all styles inline. Width 1400px, auto height.
3. **Open the file in a browser (or render a screenshot) and look at it.** Fix what you see:
   - Text overflowing its container
   - Content too close to edges (padding < 24px)
   - Inconsistent spacing between sections
   - Color contrast issues
   - Any meta/process text that leaked onto the page
4. **Fix by editing the file in place with small targeted edits** — never rewrite the whole file
   to fix a local issue. Batch all fixes you see in one pass before re-checking.
5. Deliver the file path and a rendered screenshot so the user can see the result immediately.
