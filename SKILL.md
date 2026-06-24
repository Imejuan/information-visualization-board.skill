---
name: information-visualization-board
version: 3.1.0
description: >
  A library of 2 styles for building clean, self-contained HTML visualization pages.
  Optimized for long-form content: long images, document graphics, technical diagrams,
  paper explanations, meeting notes, and slide-ready layouts.
  Output is a single self-contained HTML file — no dependencies, opens in any browser.
---

# Information Visualization Board

**2 styles** across different visual registers — clean professional and bold
high-contrast pop. All designed for **long-form, content-rich visuals**: long images, document
graphics, technical visualizations, paper explanations, meeting notes, and PPT-style layouts.

Output is always a **single self-contained HTML file** — all styles inline, opens directly in
any browser, ready to screenshot or print.

## When to use

- The user wants a visual infographic, diagram, explainer, or document graphic.
- The user gives content and wants it visual, shareable, and ready to screenshot.
- Suitable for: long images, document graphics, technical diagrams, paper explanations, meeting notes, PPT layouts, event posters, speaker lineups.

## No prerequisites

No tools to install. Output is pure HTML — just write the file and open it.

## Conversation flow

1. **Understand the board.** Find out what the user wants: content, purpose, audience. Ask one short
   question if unclear.
2. **Present both styles and ask the user to choose.** ALWAYS do this before building. Show the
   style menu exactly like this:

   > 请选择风格：
   >
   > | # | 风格名 | 画布 | 气质 | 适合场景 |
   > |---|--------|------|------|----------|
   > | 1 | **Deep Tech** | 深空蓝底 `#060A14` | 科技感渐变，青色光晕，沉浸感强 | 技术方案、论文讲解、架构图、AI/科技内容 |
   > | 2 | **Bold Pop** | 近黑底 `#1A1A1A` | 高对比撞色，大圆角，编辑感强 | 活动海报、嘉宾名单、产品发布、社交卡片 |
   >
   > 回复 **1** 或 **2** 即可。

   Wait for the user's reply before proceeding. Do NOT pick a style on the user's behalf.

3. **Confirm the chosen style** in one line, then proceed to build.
4. **Build it.** Read [`RULES.md`](RULES.md) and **only the chosen** `templates/<slug>/design.md`, then:
   - Write a single self-contained HTML file with all CSS inline in `<style>`.
   - **Style 1 (Deep Tech):** requires Google Fonts — include `@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Noto+Sans+SC:wght@400;500;700&display=swap');`. Font stack: `'Outfit', 'Noto Sans SC', -apple-system, "PingFang SC", sans-serif`. For flow diagram arrows use inline SVG triangles — do NOT use font-based icons.
   - **Style 2 (Bold Pop):** requires Google Fonts (`Noto Sans SC`) for CJK text — include `@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;700;900&display=swap');` in `<style>`. Font stack: `'AliMamaShuHei', 'Noto Sans SC', -apple-system, "PingFang SC", sans-serif`. For arrow icons, use **inline SVG** inside a circle button — do NOT use Material Symbols or font-based icons. Arrow path: `<path d="M5 15L15 5M15 5H7M15 5V13" stroke="#FFFFFF" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>` in a 20×20 SVG.
   - **响应式宽度**：内容列最大 **1400px**，小屏自动收窄。容器 CSS 必须使用：`max-width: 1400px; width: 100%; margin: 0 auto; padding: 0 40px; box-sizing: border-box;`。高度由内容决定，不固定。
   - Use the palette and mood from the chosen template exactly.
   - **Only content goes on the page** — never the user's prompt, the style name, source
     citations, or any process/meta text. (Full rules in `RULES.md`.)
   - **Open → look → fix** until clean: no overflow, no cramped padding, no clipped text.
     Fix in-place with targeted edits; never rewrite the whole file to fix one issue.
5. **Deliver.** Give the user the **file path** and the **rendered screenshot** so they can see
   it immediately. Then tell them they can switch to another style and you'll re-render.

## Files

- **[`RULES.md`](RULES.md)** — hard rules for HTML output. Always read this.
- **[`CATALOG.md`](CATALOG.md)** — both styles with vibe, formality, palette.
- **[`templates/deep-tech/design.md`](templates/deep-tech/design.md)** — Style 1 palette and usage rules.
- **[`templates/bold-pop/design.md`](templates/bold-pop/design.md)** — Style 2 palette and usage rules.
