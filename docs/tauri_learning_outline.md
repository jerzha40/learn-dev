# Tauri + TypeScript + SQLite 学习与视频教程大纲

本大纲将作为你学习构建桌面应用（Tauri + TypeScript + SQLite）的路线图，同时也是视频教程系列与 GitHub 项目的结构规划，帮助你未来具备独立承接自由职业（freelancer）项目的能力。

---

## 📘 第一章：准备阶段 — 环境配置

### 1.1 安装所有必要工具
- Node.js LTS
- Rust 工具链（rustup）
- VSCode + 必要插件（Rust、TS、Svelte/React）
- Git / GitHub Desktop

### 1.2 验证环境
```bash
node -v
npm -v
cargo -V
rustc -V
git --version
```

### 1.3 本章要产出
- 视频：环境配置 & 工具链安装
- README 小节：如何搭建开发环境

---

## 📗 第二章：Hello Tauri — 第一个桌面应用

### 2.1 创建 Tauri 项目
```bash
npm create tauri-app@latest my-ledger
cd my-ledger
npm install
npm run tauri dev
```

### 2.2 认识项目结构
- `src-tauri/` → Rust 后端
- `src/` → 前端（Svelte/React）
- `Cargo.toml` → 类比 CMakeLists.txt（Rust 依赖）
- `tauri.conf.json` → 构建配置

### 2.3 本章要产出
- 一个能启动的 Tauri 窗口
- 视频：《第一个窗口怎么跑起来？》
- GitHub 目录：`chapter1-hello-tauri/`

---

## 📙 第三章：SQLite 集成 — 本地数据库入门

### 3.1 添加 SQL 插件
```bash
npm run tauri add sql
cargo add tauri-plugin-sql --features sqlite
npm install @tauri-apps/plugin-sql
```

### 3.2 建立数据库 & 表结构
- 创建 `transactions` 表
- 写一个 `db.ts` 文件封装数据库函数

### 3.3 实现最小 Demo
- “新增交易”按钮
- “查询交易”列表

### 3.4 本章要产出
- 视频：《Tauri + SQLite 读写数据库》
- GitHub 目录：`chapter2-sql-basic/`

---

## 📒 第四章：真正的账本 — 设计数据模型

### 4.1 表设计
- `transactions`
- `accounts`
- `tags`
- `rules`（为以后 DSL 做准备）

### 4.2 多币种 & 精度管理（Decimal）

### 4.3 账本核心逻辑
- 入账
- 删除/编辑
- 分类/标签

### 4.4 本章要产出
- 视频：《设计一个真正的账本数据结构》
- GitHub 目录：`chapter3-ledger-core/`

---

## 📔 第五章：可编程会计 — 简易 DSL 引擎

### 5.1 DSL 目标
允许用户写类似：
```
rule "salary" when description ~= /工资/ => credit "INCOME.SALARY"
```

### 5.2 实现步骤
- 解析规则（正则匹配）
- 规则执行器
- 批量自动分类

### 5.3 本章要产出
- 视频：《写一个简单的规则引擎》
- GitHub 目录：`chapter4-dsl/`

---

## 📓 第六章：UI 提升 & 用户体验

### 6.1 优化界面
- Layout
- Form
- Table
- Modal

### 6.2 深色/浅色主题

### 6.3 打包正式版本
```bash
npm run tauri build
```

### 6.4 本章要产出
- 视频：《完善 UI 并打包 App》
- GitHub 目录：`chapter5-ui/`

---

## 📕 第七章：商业化准备 & Freelancer 路线

### 7.1 如何扩展为：
- 小团队内网工具
- 本地隐私账本
- 自定义财务工具
- 自动化财务审计插件

### 7.2 Freelancer 技能展示项目
你将拥有：
- 一个完整的桌面 App
- 一个带数据库和业务逻辑的真实工程
- 一个规则引擎（加分巨多）
- 完整的 GitHub 版本控制历史
- 完整的视频系列

### 7.3 如何让别人雇佣你
- Upwork 作品集怎么写
- GitHub README 怎么写项目亮点
- 你可以做哪些服务：
  - 桌面应用开发
  - SQLite/本地持久化工程
  - Tauri 构建与打包
  - 规则引擎/自动化工具

### 7.4 本章产出
- 视频：《如何把这个项目变成赚钱工具》
- GitHub：最终版 `main` 分支

---

# 📂 GitHub 项目建议目录结构

```
Tauri-Ledger-Tutorial/
│
├── chapter1-hello-tauri/
├── chapter2-sql-basic/
├── chapter3-ledger-core/
├── chapter4-dsl/
├── chapter5-ui/
│
├── docs/
│   ├── video-outline.md
│   ├── environment-setup.md
│   ├── learning-path.md
│
└── README.md
```

---

# 🎯 最终成果（你将拥有）

- 一个完整桌面 App（账本软件）
- 一个高质量视频系列（YouTube/Bilibili）
- 一个结构清晰的 GitHub 教程工程
- 一套可展示的技能（可接单）

你会具备：
- Rust/Tauri 构建能力
- TypeScript 前端能力
- SQLite 落地工程经验
- 应用架构与模块设计经验
- 做项目 → 做教程 → 做产品 的完整链条

这就是一个“技能 + 名声 + 作品集”三合一的路线。

---

如果你希望，我可以继续帮你：
- 填写 README
- 创建每个章节的详细任务
- 包含你录视频时的讲解脚本
- 或者生成 GitHub 最初的 commit 内容

