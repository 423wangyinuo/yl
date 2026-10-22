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

同时遵守以下命名规则：
- 所有 CSS 类名以 `wang_` 开头
- 所有 id 名以 `wang_` 开头
- 所有 JS 变量名以 `wang_` 开头

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
