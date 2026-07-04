# Skill Documentation

End-user-facing documentation for the Omniverse Engineering Skillset plugin.

The authoritative runtime instructions live in each `skills/*/SKILL.md` file.

## Skill Inventory

| Skill | Purpose |
| --- | --- |
| [`omniverse-architecture-review`](./omniverse-architecture-review.md) | Deep senior-engineering judgment for architecture, system design, API docs, commit messages, code quality, and implementation risk. |
| `omniverse-brainstorm` | Compare options, concepts, strategies, and technical recommendations before implementation. |
| `omniverse-plan` | Create implementation plans and optional `docs/plans/` artifacts. |
| `omniverse-work` | Execute code/docs changes, repo setup, and worktree-scoped tasks through verification. |
| `omniverse-debug` | Debug failures through evidence and narrow hypotheses. |
| `omniverse-optimize` | Improve measured performance, cost, reliability, workflow, or code simplicity. |
| `omniverse-code-review` | Review diffs, PRs, and reviewer feedback for production risks. |
| `omniverse-doc-review` | Review API docs, setup guides, ADRs, runbooks, and release docs. |
| `omniverse-dogfood` | Test the product like a real user. |
| `omniverse-test-browser` | Run browser QA, product polish checks, and optional `docs/qa/` reports. |
| `omniverse-test-xcode` | Build and test Apple-platform projects. |
| `omniverse-proof` | Create evidence packets for correctness and release claims. |
| `omniverse-commit` | Prepare clean commits, pushes, and PR handoffs. |
| `omniverse-product-pulse` | Summarize project status, release notes, launch copy, or demo scripts. |
| `omniverse-compound` | Load prior repo memory or capture durable solution notes under `docs/solutions/`. |
| `omniverse-feedback-analysis` | Synthesize qualitative feedback into themes and actions. |

## Artifact Folders

| Folder | Written by |
| --- | --- |
| `docs/plans/` | `omniverse-plan` |
| `docs/solutions/` | `omniverse-compound` |
| `docs/reviews/` | Review-oriented skills when a durable review note is useful. |
| `docs/qa/` | `omniverse-test-browser`, `omniverse-dogfood` |
| `docs/proof/` | `omniverse-proof` |
