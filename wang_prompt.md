# 提示词记录

---

## 2026-10-12

**实践：** 编写11-1.html，显示web前端的长度单位

**使用的模型：** longcat-2.5-preview-free

**提示词内容：**
> 编写11-1.html,显示web前端的长度单位

---

## 2026-10-12

**实践：** 编写11-2.html，展示CSS3 3D动画

**使用的模型：** longcat-2.5-preview-free

**提示词内容：**
> 编写11-2.html,展示css3 3d动画

---

## 2026-10-12

**实践：** 设置规则：新建的html文件加入超链接到首页index.html

**使用的模型：** longcat-2.5-preview-free

**提示词内容：**
> 设置规则：新建的html文件加入超链接到首页index.html

---

## 2026-10-12

**实践：** 写入wang_prompt.md

**使用的模型：** longcat-2.5-preview-free

**提示词内容：**
> 写入wang_prompt.md

---

## 2026-10-12

**实践：** 设置规则：所有css类名，id名、js变量都以wang_开始，所有的提示词都在执行之前写入文件wang_prompt.md,以附加的方式写入，不覆盖之前的内容，写入的内容包括实践、使用的模型、提示词内容，把这条规则写入wang_prompt.md

**使用的模型：** longcat-2.5-preview-free

**提示词内容：**
> 设置规则：所有css类名，id名、js变量都以wang_开始，所有的提示词都在执行之前写入文件wang_prompt.md,以附加的方式写入，不覆盖之前的内容，写入的内容包括实践、使用的模型、提示词内容，把这条规则写入wang_prompt.md

---

## 规则声明

本文件（`wang_prompt.md`）为**只追加**文件，记录每次执行任务的提示词，包含：**实践**、**使用的模型**、**提示词内容**。

同时遵守以下规则：

**命名前缀（CSS 类名、id 名、JS 变量名）：**
- 旧文件：以 `wang_` 开头（保持不变）
- **新文件（2026-10-22 起）：** 以 `yl_` 开头

**HTML 注释规则：**
- 每个新 HTML 页面必须在 `<head>` 内、`<title>` 上方加入作者注释：
  `<!-- 作者：王一诺 | 建立时间：YYYY-MM-DD | 使用模型：xxx | 功能名称：xxx -->`

**技术栈规则（仅新文件）：**
- 仅使用**原生 HTML + CSS + JavaScript**，不使用任何框架（Vue/React/Bootstrap 等）
- **禁止第三方库和 CDN 外链**（不得出现 `<script src="http...">` 或 `<link href="http...">`）
- **图标必须使用本地 `font/` 目录的 iconfont**：引入 `font/iconfont.css`，用 `<i class="iconfont icon-xxx">`
- 获取服务器端数据：使用原生 `fetch()`（注意：fetch 需要 HTTP 协议，file:// 下无法工作）
- 现有 `cdn/` 下的 fontawesome/lucide 为旧版遗留，新文件禁止使用

---

## 2026-10-15

**实践：** 创建skill，提交项目：使用git commit并push当前项目到https://gitee.com/wang-yi-nuo/html

**使用的模型：** longcat-2.5-preview-free

**提示词内容：**
> 创建skill，提交项目：使用git commit并push当前项目到https://gitee.com/wang-yi-nuo/html

---

## 2026-10-19

**实践：** 创建两个HTML网页 13-1.html 与 13-2.html，分别演示 Font Awesome 字体图标（woff2 字体 + CSS 类名方式）和 Lucide 图标（内联 SVG 方式），并将相关库文件下载到本项目 cdn 目录下

**使用的模型：** longcat-2.5-preview-free

**提示词内容：**
> 做两个html网页，13-1.html,13-2.html,分别显示fonta wesome图标和lucide图标，前者使用字体图标的方式，后者使用svg的方式，相关的文件下载到本目录下的cdn目录。

**执行说明：**
- `cdn/fontawesome/`：从 cdnjs 下载 all.min.css 与 fa-solid/fa-regular/fa-brands 三个 woff2 字体，页面通过 `<i class="fa-*">` 类名渲染图标
- `cdn/lucide/`：下载 lucide.min.js（UMD），页面用 `<i data-lucide="...">` 占位，由 `lucide.createIcons()` 注入内联 SVG
- 两个页面均遵守 wang_ 前缀命名规范，并在 index.html 导航页中新增 16、17 号卡片入口

---

## 2026-10-19（第二次实践）

**实践：** 根据 font 目录中的 iconfont 图标，完成移动端固定、自适应宽度的下导航（首页/商城/发现/我的），制作 13-3.html（字体图标方式）与 13-4.html（SVG 方式），包含右上角数字徽章与红点

**使用的模型：** longcat-2.5-preview-free

**提示词内容：**
> 根据font目录中的iconfont图标完成移动端的固定的自适应宽度的下导航，导航项目包括四个：首页，商城，发现，我的，完成html网页的设计，网页名称13-3.html和13-4.html分别使用字体图标和svg，包括右上角的数字徽章和红点。

**执行说明：**
- 复用 `font/iconfont.css` 本地字体，四个导航项图标类名：icon-shouye / icon-shangcheng-copy / icon-faxian / icon-FillCopy
- `13-3.html`：`<i class="iconfont icon-*">` 字体图标方式；`13-4.html`：将 iconfont.js 中的 symbol 路径数据转为内联 SVG sprite，用 `<svg><use href="#wang_icon-*"/></svg>` 引用
- 底部导航 fixed + 每项 flex:1 自适应等宽，支持 env(safe-area-inset-bottom)；商城「3」、我的「12」为数字徽章，发现为红点
- index.html 新增 18、19 号卡片入口

---

## 2026-10-22

**实践：** 根据项目已有的 .opencode/skills/web-design-coursework/SKILL.md 文件，创建 Trae 格式的 skill（放在 .trae/skills/web-design-coursework/SKILL.md）

**使用的模型：** Trae 专有模型

**提示词内容：**
> SKLLmd 创建trae的skill，根据给定文件

---

## 2026-10-22（第二次实践）

**实践：** 提交项目 —— git add, commit, push 到 Gitee

**使用的模型：** Trae 专有模型

**提示词内容：**
> 提交项目

---

## 2026-10-22（第三次实践）

**实践：** 设置项目规则 —— 命名前缀改为 yl_，HTML 页面必须包含注释（姓名、日期、功能名称）

**使用的模型：** Trae 专有模型

**提示词内容：**
> 设置项目规则：所有变量名称、css类、id名称都以yl_开始，所有html页面都包括注释、姓名：王一诺、日期、功能名称

---

## 2026-10-22（第四次实践）

**实践：** 创建 14-2.html，演示 JavaScript 基本的 6 种数据类型

**使用的模型：** Trae 专有模型

**提示词内容：**
> 完成网页14-2.html，演示javascript基本的6种数据类型

**执行说明：**
- 新建 `14-2.html`，遵循新规则：HTML 注释 + `yl_` 前缀（CSS 类名/id/JS 变量）
- 演示 6 种数据类型：Number、String、Boolean、Null、Undefined、Object
- 每种类型含变量声明示例代码 + 运行时值 + typeof 检测结果
- 用 `createElement`/`textContent`/`appendChild` DOM API 渲染，避免 innerHTML 注入风险
- `index.html` 新增 20 号（14-1.html）和 21 号（14-2.html）导航卡片

---

## 2026-10-22（第五次实践）

**实践：** 提交项目 —— git add, commit, push 到 Gitee

**使用的模型：** Trae 专有模型

**提示词内容：**
> 提交项目

---

## 2026-10-22（第七次实践）

**实践：** 设置项目规则 —— 原生 HTML/CSS/JS + 本地 iconfont 图标 + fetch 获取服务器数据

**使用的模型：** Trae 专有模型

**提示词内容：**
> 设置项目规则：使用原生的html和css和javascript实现，图标使用font目录下的iconfont图标，不使用第三方库和cdn，使用fetch获取服务器端数据

---

## 2026-10-22（第八次实践）

**实践：** 提交项目 —— git add, commit, push 到 Gitee

**使用的模型：** Trae 专有模型

**提示词内容：**
> 好的，提交项目

---

## 2026-10-26（第九次实践）

**实践：** 创建 15-1.html，一百个盒子按"数7"规则显示/隐藏数字

**使用的模型：** Trae 专有模型

**提示词内容：**
> 编写15-1.html,一百个盒子，里面有数字，按照数7的规则，（7的倍数，个位数为7的数字等，比如7不显示，14不显示。17不显示等等），不满足要求的显示数字，满足要求的显示空盒子

**执行说明：**
- 新建 `15-1.html`，遵循 yl_ 前缀 + HTML 注释 + 原生 HTML/CSS/JS + 禁止 CDN
- 10×10 CSS Grid 网格布局，共 100 个盒子（1~100）
- 判定条件：`i % 7 === 0 || i % 10 === 7` 命中规则显示为空盒子
- 空盒子用红色斜条纹背景 + × 标记，悬停显示具体命中数字
- `index.html` 新增 22 号卡片入口

---

## 2026-10-26（第十次实践）

**实践：** 修改 HTML 注释规则 —— 新增"使用的大模型"字段

**使用的模型：** Trae 专有模型

**提示词内容：**
> 修改规则：在新建一个html文件时，都要加入注释，注释包括：王一诺、建立时间、使用的大模型、功能名称

---

## 2026-10-26（第十一次实践）

**实践：** 提交项目到 GitHub（https://github.com/423wangyinuo/yl）

**使用的模型：** Trae 专有模型

**提示词内容：**
> 创建技能skill，提交到githhub，commit和posh当前项目到 `https://github.com/423wangyinuo/yl` 然后公钥已设置

---

## 2026-10-26（第十二次实践）

**实践：** 推送项目（Gitee + GitHub）

**使用的模型：** Trae 专有模型

**提示词内容：**
> 推送项目

---

## 2026-10-26（第十三次实践）

**实践：** 创建 15-2.html，展示 JavaScript 程序结构（循环、条件），并提交到 GitHub

**使用的模型：** Trae 专有模型

**提示词内容：**
> 完成15-2.html，展示javascript程序结构：循环，条件,然后提交到github

---
