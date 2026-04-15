# Web Fullstack Workflow Skills

[English](./README.md) | 中文

`web-fullstack-workflow` 是一组用于构建和交付全栈 Web 应用的技能集合，覆盖结构化产品分析、前端设计、Vue 实现，以及 Ignis 后端与部署工作流。

## 安装

使用 `npx skills add` 安装本仓库中的全部技能：

```bash
npx skills add https://github.com/igniscloud/web-fullstack-workflow.git
```

如果你的环境更适合使用 SSH，可以把仓库 URL 替换为对应的 SSH 地址。

## 包含的技能

- `web-dev-workflow`：编排完整的多智能体交付流程，覆盖 PRD、前端设计、开发和评审。
- `prd-analysis`：把功能请求或原始需求整理成面向产品的简洁 PRD。
- `frontend-design-spec`：把需求文档转换成可直接交给开发实现的纯文本前端设计规格。
- `vue-frontend-dev`：实现或修复 Vue 3 + Vite 前端，覆盖 vue-router、Pinia、vue-i18n 和 Tailwind CSS v4。
- `ignis`：覆盖 Ignis 项目初始化、`ignis-cli`、`ignis-sdk`、`ignis.hcl`、SQLite，以及构建、发布和部署流程。
- `ignis-login`：覆盖 Ignis 登录集成，包括 Hosted Login、PKCE、回调流程和登录冒烟测试。
- `opencode-web-page-generator`：运行面向 OpenCode 的工件驱动管理流程，包含 planner、builder 和 evaluator 角色。

## 仓库结构

```text
.
├── LICENSE
├── README.md
├── README.zh-CN.md
└── skills/
    ├── frontend-design-spec/
    ├── ignis/
    ├── ignis-login/
    ├── opencode-web-page-generator/
    ├── prd-analysis/
    ├── vue-frontend-dev/
    └── web-dev-workflow/
```

## 何时使用本仓库

当你需要以下能力时，本仓库会比较适合：

- 使用一组可复用的打包技能，而不是单个独立技能。
- 从需求到评审的完整 Web 交付流程。
- 与前端设计流程配套的 Vue 前端实现能力。
- 在同一个包里提供 Ignis 后端、登录和部署技能。
- 在 Codex 风格开发技能之外，同时使用面向 OpenCode 的页面工作流。

## 说明

- 当你需要完整的分阶段交付路径时，`web-dev-workflow` 是顶层工作流技能。
- `ignis` 和 `ignis-login` 也可以在非 Vue 或非重设计项目中独立使用。
- `opencode-web-page-generator` 面向 OpenCode 场景，和通用的多智能体 Web 工作流相互独立。
