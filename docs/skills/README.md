# Skill Documentation

End-user documentation for Omniverse Engineering Skillset.

Runtime behavior is controlled by each `skills/*/SKILL.md` file. The `name` and `description` frontmatter are the primary automatic-trigger signals; the `agents/openai.yaml` files provide display names and default prompts for OpenAI-style agent surfaces.

## Trigger Guide

| Skill | Use when the user asks to... |
| --- | --- |
| [`architecture-audit`](./architecture-audit.md) | Review architecture, system design, ADR/RFC risk, scalability, distributed-systems tradeoffs, or production readiness. |
| `omniverse-brainstorm` | Brainstorm, ideate, compare approaches, choose a direction, sequence roadmap work, or produce a tradeoff-heavy recommendation. |
| `omniverse-plan` | Plan a feature, refactor, migration, fix, agent workflow, or other multi-step engineering task before code changes. |
| `omniverse-work` | Implement, fix, refactor, update docs, bootstrap a repo, run tests, or carry a concrete task through verification. |
| `omniverse-debug` | Debug failing builds, tests, CI, runtime behavior, integrations, auth flows, flaky workflows, or unexpected results. |
| `omniverse-optimize` | Improve performance, cost, reliability, maintainability, developer workflow, slow code, expensive calls, build time, or complexity. |
| `omniverse-code-review` | Review diffs, pull requests, branches, files, generated code, implementation changes, reviewer comments, or release risk. |
| `omniverse-doc-review` | Review API docs, README changes, setup guides, ADRs, runbooks, release docs, design specs, or migration instructions. |
| `omniverse-dogfood` | Dogfood a workflow, try the product like a customer, inspect usability friction, verify install experience, or test end to end. |
| `omniverse-test-browser` | Run browser QA, inspect a page, verify a frontend change, check responsive behavior, smoke test a dev server, or refine UI states. |
| `omniverse-test-xcode` | Build, test, or review iOS, macOS, watchOS, tvOS, Swift, SwiftUI, Xcode schemes, simulators, or signing workflows. |
| `omniverse-proof` | Prove a behavior, gather validation evidence, audit release claims, prepare handoff proof, or mark unsupported claims as unproven. |
| `omniverse-commit` | Commit changes, write a commit message, inspect staged changes, split commits, push a branch, or prepare a PR handoff. |
| `omniverse-product-pulse` | Summarize product progress, release status, launch copy, stakeholder updates, risk digests, changelogs, or demo scripts. |
| `omniverse-project-memory` | Load prior solutions, review repo memory, document what was learned, write solution notes, or preserve debugging knowledge. |
| `omniverse-feedback-analysis` | Synthesize review comments, user feedback, beta notes, bug reports, support threads, recordings, or survey responses. |

## Artifact Folders

| Folder | Written by |
| --- | --- |
| `docs/plans/` | `omniverse-plan` |
| `docs/solutions/` | `omniverse-project-memory` |
| `docs/reviews/` | Review-oriented skills when a durable review note is useful. |
| `docs/qa/` | `omniverse-test-browser`, `omniverse-dogfood` |
| `docs/proof/` | `omniverse-proof` |

## Prompt Examples

```txt
Use omniverse-plan to plan this migration before editing code.
Use omniverse-code-review to review this PR for production risks.
Use omniverse-dogfood to verify the install flow like a new user.
Use omniverse-proof to gather evidence that this release is ready.
Use architecture-audit to review this rate-limiter design.
```
