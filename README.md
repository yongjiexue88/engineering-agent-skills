# Omniverse Engineering Skillset

[![npm version](https://img.shields.io/npm/v/omniverse-engineering-skillset?color=cb3837&label=npm)](https://www.npmjs.com/package/omniverse-engineering-skillset)
![Node.js >=18](https://img.shields.io/badge/node-%3E%3D18-339933)
![Agent skill pack](https://img.shields.io/badge/agent%20skills-ready%20to%20use-7c3aed)
![Focus](https://img.shields.io/badge/focus-planning%20%7C%20reviews%20%7C%20shipping-0ea5e9)

Give your coding agent a practical engineering workflow layer: plan the work, make the change, debug failures, review production risk, verify user flows, ship clean commits, and preserve reusable project knowledge.

The skills are designed to trigger from normal engineering requests. You can ask by skill name for precision, or describe the work naturally and let the skill descriptions route the task.

## Install In One Minute

Recommended: install directly from GitHub with the open `skills` CLI:

```bash
npx skills add yongjiexue88/omniverse-engineering-skillset
```

This discovers every bundled skill from:

```txt
skills/*/SKILL.md
```

It installs them into your project skills folder, such as:

```txt
.agents/skills/
```

You can also install from npm with the package CLI:

```bash
npx --yes omniverse-engineering-skillset@latest install
```

Then use the skills in your agent:

```txt
Use omniverse-plan to plan this migration.
Use omniverse-work to implement the approved plan.
Use omniverse-code-review to review this PR before shipping.
Use architecture-audit to review this system design.
```

## What You Get

- 16 bundled skills covering planning, implementation, debugging, optimization, review, QA, proof, release communication, git handoff, feedback analysis, project memory, and architecture audits.
- Automatic routing metadata in each `SKILL.md` frontmatter so agents can select the right workflow from normal requests.
- Helper scripts for durable plan files, solution notes, browser QA reports, proof packets, and git change summaries.
- Deep architecture references for feeds, search, queues, caching, rate limiting, real-time messaging, workflows, payments, LLM serving, high-contention inventory, and other production systems.
- Multi-platform plugin metadata for Codex-style plugins plus Claude, Cursor, Kimi, OpenCode, Pi, and Agent Gateway layouts.

## Automatic Trigger Map

| Ask for this | Skill that should trigger |
| --- | --- |
| Brainstorm options, compare approaches, choose a direction | `omniverse-brainstorm` |
| Plan a feature, fix, migration, refactor, or agent workflow | `omniverse-plan` |
| Implement, fix, refactor, update docs, or run verification | `omniverse-work` |
| Debug a broken build, failing test, flaky workflow, or runtime issue | `omniverse-debug` |
| Optimize slow code, expensive calls, build time, reliability, or complexity | `omniverse-optimize` |
| Review a diff, branch, PR, generated code, or reviewer feedback | `omniverse-code-review` |
| Review README, API docs, setup guides, ADRs, runbooks, or release docs | `omniverse-doc-review` |
| Dogfood a workflow, inspect real-user friction, or verify install experience | `omniverse-dogfood` |
| Browser QA, responsive checks, frontend polish, or dev-server smoke tests | `omniverse-test-browser` |
| Build or test iOS, macOS, watchOS, tvOS, Swift, SwiftUI, or Xcode projects | `omniverse-test-xcode` |
| Prove a release claim, gather validation evidence, or prepare handoff proof | `omniverse-proof` |
| Commit, split commits, push, draft a PR, or inspect staged changes | `omniverse-commit` |
| Summarize release status, product progress, launch copy, or demo notes | `omniverse-product-pulse` |
| Reuse prior project knowledge or write a durable solution note | `omniverse-project-memory` |
| Synthesize feedback, beta notes, bug reports, support threads, or surveys | `omniverse-feedback-analysis` |
| Review architecture, system design, ADR/RFC risk, scalability, or production readiness | `architecture-audit` |

## Install Options

Preview the skills before installing:

```bash
npx skills add yongjiexue88/omniverse-engineering-skillset --list
```

Install for a specific agent target:

```bash
npx skills add yongjiexue88/omniverse-engineering-skillset --agent codex
npx skills add yongjiexue88/omniverse-engineering-skillset --agent claude-code
```

Install globally or copy files instead of symlinking:

```bash
npx skills add yongjiexue88/omniverse-engineering-skillset --global
npx skills add yongjiexue88/omniverse-engineering-skillset --copy
```

Use the npm package CLI when you want a versioned npm install path:

```bash
npx --yes omniverse-engineering-skillset@latest list
npx --yes omniverse-engineering-skillset@latest install
npx --yes omniverse-engineering-skillset@latest install --agent codex
npx --yes omniverse-engineering-skillset@latest install --agent claude-code
npx --yes omniverse-engineering-skillset@latest install --target ~/.codex/skills
```

For package-managed projects, you can pin it as a dependency:

```bash
npm install --save-dev omniverse-engineering-skillset
```

The npm install path automatically installs skills into `.agents/skills/` for the invoking project when `INIT_CWD` is available. Set `OMNIVERSE_ENGINEERING_SKILLSET_SKIP_AUTO_INSTALL=1` to skip that postinstall behavior.

## Everyday Prompts

```txt
Use omniverse-brainstorm to compare three ways to add billing.
Use omniverse-plan to write a migration plan under docs/plans.
Use omniverse-work to implement the smallest safe version of this change.
Use omniverse-debug to reproduce and fix this CI failure.
Use omniverse-code-review to review this diff for correctness and missing tests.
Use omniverse-dogfood to try the install flow like a new user.
Use omniverse-test-browser to verify signup on desktop and mobile.
Use omniverse-proof to gather evidence that this release is ready.
Use omniverse-commit to commit, push, and prepare the PR body.
Use omniverse-project-memory to capture the solution after this fix.
Use architecture-audit to design a rate limiter for this API.
```

## Durable Artifacts

Several skills can write lightweight project memory when a durable handoff is useful:

| Folder | Written by |
| --- | --- |
| `docs/plans/` | `omniverse-plan` |
| `docs/solutions/` | `omniverse-project-memory` |
| `docs/reviews/` | Review-oriented skills |
| `docs/qa/` | `omniverse-test-browser`, `omniverse-dogfood` |
| `docs/proof/` | `omniverse-proof` |

## Troubleshooting

| Problem | Fix |
| --- | --- |
| You only want one skill | `npx --yes omniverse-engineering-skillset@latest install --skill omniverse-plan` |
| Your agent uses a custom skills directory | `npx --yes omniverse-engineering-skillset@latest install --target /path/to/skills` |
| You installed the npm package but do not want postinstall copying | Set `OMNIVERSE_ENGINEERING_SKILLSET_SKIP_AUTO_INSTALL=1` before `npm install`. |
| A skill did not trigger automatically | Ask by name once, for example `Use omniverse-code-review ...`; the installed `SKILL.md` descriptions provide the routing hints for future automatic selection. |

## Repository Layout

```txt
skills/                 Runtime skill instructions
skills/*/agents/        Agent-specific metadata and default prompts
skills/*/scripts/       Skill-local helper scripts
docs/skills/            End-user skill inventory and trigger guide
docs/plans/             Optional plan artifacts
docs/solutions/         Optional reusable solution notes
docs/qa/                Optional QA reports
docs/proof/             Optional proof packets
```

## Best Fit

Use this package when you want your coding agent to work like a stronger engineering partner: clear scope, fewer hidden risks, better validation, cleaner handoffs, and practical production judgment without slowing every task into process.
