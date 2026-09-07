# ProgressBoard / 项目进度看板

**A single-folder, zero-dependency weekly project tracker. Open `index.html` and go.**

**一个文件夹、零依赖的周报式项目进度管理工具。双击 `index.html` 即可使用。**

---

## 中文说明

### 这是什么

周报式的个人项目管理表格：按学年整理各项项目进度，记录日期、负责人、类型、完成度、状态、计划书、本周进展和备注，配合统计卡片和三张可视化图表（项目完成度条形图、状态分布环形图、整体完成度趋势折线图）。

### 功能特性

- **表格管理**：11 列完整字段；每行支持 ±5 快捷调整完成度、迷你进度条、状态下拉按语义着色
- **自动排序**：置顶行最前 → 学年从低到高 → 完成度 100→0 → 日期新在前
- **学年与跨学年**：每条记录归属一个学年，可勾选「跨学年」同时显示在两个学年
- **筛选与置顶**：按学年 / 状态 / 项目 / 关键词筛选，统计卡片和图表跟随筛选；置顶的行在当前筛选下始终排最前
- **自动保存**：数据写入本地数据文件（见下文），每一步修改实时保存
- **撤销**：「回退上一步」最多回退 60 步（同一格 1.5 秒内的连续输入自动合并为一步）
- **保存记录**：后台数据修改日志面板，记录每次修改的时间、项目、字段和 旧值 → 新值，可随时核验
- **导入导出**：导出 Excel（.xls）；导入支持 CSV / TSV / TXT / XLS / XLSX（中英文表头均可识别）
- **查重清理**：同名项目保留日期最新的一条
- **中英双语**：右上角一键切换界面语言，选择会被记住

### 数据保存在哪里

打开页面后点右上角「**数据文件**」，在弹出的对话框中选择本项目的 `data/` 文件夹、保存 `data.json`——之后所有修改都会自动写入这个文件（需要 Chrome 或 Edge 浏览器）。

- 首次授权之后，浏览器会记住这个文件，下次打开自动续接
- 如果浏览器不支持本地文件读写（如 Firefox / Safari），数据会自动保存在浏览器本地存储中，不会丢失
- 建议把 `data/data.json` 加入版本库忽略（本项目已附带 .gitignore）

### 快速开始

1. 下载或克隆本文件夹
2. 用 Chrome / Edge 双击打开 `index.html`
3. 点「数据文件」按钮，把 data.json 保存到 `data/` 文件夹
4. 删除示例记录，录入你自己的项目

### 文件结构

```
ProgressBoard/
├── index.html   主页面（全部逻辑内嵌）
├── style.css    样式
├── README.md    本文件
├── LICENSE      MIT 许可证
├── .gitignore   忽略本地数据文件
└── data/        数据文件夹（data.json 保存在这里）
```

### 浏览器支持

- Chrome / Edge（推荐）：完整功能，包括本地数据文件自动保存
- Firefox / Safari：全部功能可用，数据保存在浏览器本地存储（不支持文件读写 API）

---

## English

### What is this

A weekly-report-style project tracker: organize projects by school year, record dates, owners, types, completion, status, plans, progress and notes — with summary cards and three charts (per-project completion bars, status distribution donut, completion trend line).

### Features

- **Table management**: 11 columns; per-row ±5 quick completion adjust, mini progress bar, semantically colored status dropdown
- **Auto sorting**: pinned rows first → year ascending → completion 100→0 → newest date first
- **School years & cross-year**: each record belongs to a year; check "Cross-year" to show it in two years
- **Filter & pin**: filter by year / status / project / keyword — cards and charts follow; pinned rows stay on top of the current filter
- **Auto save**: every change is written to a local data file (see below) in real time
- **Undo**: up to 60 steps (rapid edits in the same cell within 1.5s merge into one step)
- **Save log**: a panel listing every data change with time, project, field and old → new values
- **Import / export**: export Excel (.xls); import CSV / TSV / TXT / XLS / XLSX (Chinese and English headers both recognized)
- **Dedupe**: keep only the newest record per project name
- **Bilingual UI**: one-click Chinese / English toggle, choice is remembered

### Where is my data stored

After opening the page, click "**Data File**" in the top bar and save `data.json` into this project's `data/` folder — from then on every change is auto-saved to that file (Chrome or Edge required).

- Once authorized, the browser remembers the file and reconnects automatically on next launch
- If the browser lacks the File System Access API (Firefox / Safari), data falls back to browser local storage — nothing is lost
- It is recommended to keep `data/data.json` out of version control (a .gitignore is included)

### Quick start

1. Download or clone this folder
2. Open `index.html` with Chrome / Edge
3. Click the "Data File" button and save data.json into the `data/` folder
4. Delete the demo records and add your own projects

### File structure

```
ProgressBoard/
├── index.html   main page (all logic inline)
├── style.css    stylesheet
├── README.md    this file
├── LICENSE      MIT license
├── .gitignore   ignores local data files
└── data/        data folder (data.json lives here)
```

### Browser support

- Chrome / Edge (recommended): full features including local data file auto-save
- Firefox / Safari: all features work; data is stored in browser local storage (no File System Access API)

---

## License / 许可证

[MIT](./LICENSE)
