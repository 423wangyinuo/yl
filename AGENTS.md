# AGENTS.md

## Project
Static coursework site for a web design class (Chinese-language). Pure HTML/CSS — no build tooling, no package manager, no tests.

## Naming Convention
- Existing files: CSS class names, id names, and JS variables start with `wang_`.
- **New files (from 2026-10-22 onward)**: All CSS class names, id names, and JS variables must start with `yl_`.

## HTML Comment Rule
Every new HTML page must include an author comment inside `<head>`, placed **above** the `<title>` tag:
```html
<!-- 姓名：王一诺 | 日期：YYYY-MM-DD | 功能名称：xxx -->
```

## Prompt Logging
Before executing any task, append the prompt details to `wang_prompt.md` (append-only, never overwrite). Each entry must include:
- **实践** (practice/exercise description)
- **使用的模型** (model used)
- **提示词内容** (full prompt content)

## Files
- `index.html` — navigation hub linking to all exercise pages
- Numbered HTML files (`1.html` through `10-4.html`) — individual exercises
- Some filenames contain Chinese characters; PowerShell may display them as garbled text. Use `Get-ChildItem` with `-Filter` or tab-completion to reference them.
- `css.css` — minimal shared stylesheet (not linked by all pages; many exercises use inline `<style>`)
- `wang_prompt.md` — append-only log of all prompts

## Workflow
- Open HTML files directly in a browser; no dev server or build step needed.
- Edit inline `<style>` blocks within each HTML file for exercise styling.
- After completing each task, append a summary to `wang_prompt.md`.
