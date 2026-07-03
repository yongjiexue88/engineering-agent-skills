---
name: omniverse-work
description: Execute an engineering task end to end. Use when the user asks to implement, fix, refactor, update docs, run tests, bootstrap a repo, create or use a worktree, move quickly on a concrete task, or carry a planned change through code edits and verification.
---

# Omniverse Work

Use this skill to move from request to verified change.

## Workflow

1. Clarify only blockers that cannot be discovered locally.
2. Inspect status, setup docs, package scripts, and the relevant code before editing.
3. Make the smallest coherent change that satisfies the request.
4. Follow existing architecture, naming, and test patterns.
5. Add or update focused tests when risk justifies it.
6. Run validation and summarize changed files, behavior, and tests.

## Setup and Isolation

- For setup tasks, respect the lockfile and package manager already in use.
- Identify required tools, services, environment variables, and secrets without overwriting local env files.
- For worktree tasks, inspect `git worktree list`, current branch, and dirty state before creating or using a worktree.
- Never delete a worktree with uncommitted work unless explicitly requested.

## Rules

- Keep unrelated refactors out of the diff.
- Preserve user changes already in the worktree.
- Prefer local helpers and established patterns over new abstractions.
- Do not stop at a plan when implementation is feasible and requested.
