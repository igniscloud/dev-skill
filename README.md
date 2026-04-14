# Web Fullstack Workflow Skills

`web-fullstack-workflow` is a skill collection for building and shipping fullstack web apps with structured product work, frontend design, Vue implementation, and Ignis backend/deploy workflows.

## Installation

Install all skills from this repository with `npx skills add`:

```bash
npx skills add https://github.com/igniscloud/web-fullstack-workflow.git
```

If your environment prefers SSH, replace the repository URL accordingly.

## Included Skills

- `web-dev-workflow`: Orchestrates a full multi-agent delivery workflow for PRD, frontend design, development, and review.
- `prd-analysis`: Converts feature requests or raw requirements into a concise product-facing PRD.
- `frontend-design-spec`: Turns a requirements document into a text-only frontend design spec that developers can implement directly.
- `vue-frontend-dev`: Implements or repairs a Vue 3 + Vite frontend with vue-router, Pinia, vue-i18n, and Tailwind CSS v4.
- `ignis`: Covers Ignis project setup, `ignis-cli`, `ignis-sdk`, `ignis.hcl`, SQLite, and build/publish/deploy workflows.
- `ignis-login`: Covers Ignis login integration with Hosted Login, PKCE, callback flows, and login smoke tests.
- `opencode-web-page-generator`: Runs an artifact-driven OpenCode manager workflow across planner, builder, and evaluator roles.

## Repository Layout

```text
.
├── LICENSE
├── README.md
└── skills/
    ├── frontend-design-spec/
    ├── ignis/
    ├── ignis-login/
    ├── opencode-web-page-generator/
    ├── prd-analysis/
    ├── vue-frontend-dev/
    └── web-dev-workflow/
```

## When To Use This Repository

This repository is a good fit when you want:

- a packaged set of reusable skills instead of one standalone skill
- a full web delivery workflow from requirements to review
- Vue frontend implementation with a matching frontend design workflow
- Ignis backend, login, and deployment skills in the same package
- an OpenCode-oriented page workflow alongside Codex-style development skills

## Notes

- `web-dev-workflow` is the top-level workflow skill when you want the full staged delivery path.
- `ignis` and `ignis-login` can also be used independently in non-Vue or non-design-heavy projects.
- `opencode-web-page-generator` is OpenCode-specific and is separate from the general multi-agent web workflow.
