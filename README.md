# OpenCode Web Page Generator

`opencode-web-page-generator` is an OpenCode skill for orchestrating web-page work. It acts as a manager and continuously routes work across three roles instead of doing planning, implementation, or review directly.

- `planner`: creates or refreshes `product_spec.md` and `sprint_contract.md`
- `builder`: implements the current sprint and refreshes `handoff.md`
- `evaluator`: independently reviews the result and refreshes `qa_report.md`

The workflow is artifact-driven. Shared files carry the state forward across multiple subagent rounds so the work can continue cleanly even when a session needs to reset.

## Project Structure

- `SKILL.md`: manager entry point and routing rules
- `agents/planner.md`: planner subagent instructions
- `agents/builder.md`: builder subagent instructions
- `agents/evaluator.md`: evaluator subagent instructions
- `references/*.md`: templates and manager references

## Shared Artifacts

The workflow revolves around these files:

- `product_spec.md`
- `sprint_contract.md`
- `handoff.md`
- `qa_report.md`
- `design-system/MASTER.md`
- `design-system/pages/*.md`

## Installation

Copy this directory into your local OpenCode skills directory:

```bash
mkdir -p ~/.agents/skills
cp -R . ~/.agents/skills/opencode-web-page-generator
```

If the task also uses the optional `ignis` or `ignis-login` skills, make sure they are installed at:

- `~/.agents/skills/ignis`
- `~/.agents/skills/ignis-login`

## How To Use

Invoke this skill as the manager for a web-page task. A typical cycle looks like this:

1. The manager reads `agents/*.md` and checks the current artifact state.
2. If planning artifacts are missing or stale, it dispatches `planner`.
3. When the sprint is clear, it dispatches `builder`.
4. After implementation, it dispatches `evaluator`.
5. If `qa_report.md` still has blocking findings, the manager continues the next round.

This skill is a good fit when you need:

- a fresh landing page or product page built from a brief
- iterative improvement of an existing page
- explicit handoff between planning, implementation, and review
- safe continuation via `handoff.md` when context gets crowded

## Ignis References

The optional `ignis` and `ignis-login` skills in this project are intended to align with the official Ignis repository:

- https://github.com/igniscloud/ignis

## Conventions

- The manager does not replace the planner, builder, or evaluator roles.
- Reuse the shared artifacts instead of inventing parallel documents.
- Read external skills and references progressively instead of preloading everything.
- When the runtime needs an explicit local skill path, use `~/.agents/skills/...`.
