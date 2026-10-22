---
name: "web-design-coursework"
description: "Covers conventions for this Chinese web design coursework site. Use when creating or editing exercise HTML files: native HTML/CSS/JS only, local iconfont icons, yl_ prefix for new files, HTML author comment, fetch for server data, append prompt logging, and Gitee publishing."
---

# Web Design Coursework Site

Static coursework site for a web design class. Pure HTML/CSS — no build tooling, no package manager, no tests.

## Naming Convention

- Existing files: CSS class names, id names, and JS variables start with `wang_`.
- **New files (from 2026-10-22 onward)**: All CSS class names, id names, and JS variables must start with `yl_`.

## HTML Comment Rule

Every new HTML page must include an author comment inside `<head>`, placed **above** the `<title>` tag:
```html
<!-- 姓名：王一诺 | 日期：YYYY-MM-DD | 功能名称：xxx -->
```

## Technology Stack (new files)

- Use **native HTML + CSS + JavaScript** only. No frameworks (Vue/React/Bootstrap/etc).
- **No third-party libraries or CDN links** (no external `<script src="http...">` or `<link href="http...">`).
- **Icons must use local `font/` directory iconfont**: include `font/iconfont.css` and use `<i class="iconfont icon-xxx">`.
- For server-side data: use native `fetch()`. Note: `fetch()` requires HTTP(S) — cannot work with `file://` protocol.
- Existing files under `cdn/` (fontawesome, lucide) are legacy — **new files must not use them**.

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

## Publishing

To publish to Gitee:
```powershell
git add -A
git commit -m "describe the changes"
git push -u origin master
```

Remote: `https://gitee.com/wang-yi-nuo/html`
