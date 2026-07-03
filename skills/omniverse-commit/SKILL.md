---
name: omniverse-commit
description: Prepare a clean git handoff. Use when the user asks to commit changes, write a commit message, inspect staged or unstaged changes, split commits, push a branch, open or update a PR, or make sure only intended files are committed.
---

# Omniverse Commit

Use this skill to turn a finished local change into an intentional commit, push, or PR handoff.

## Workflow

1. Inspect branch, remotes, and changed files.
2. Review the diff for every file that will be staged or shipped.
3. Separate unrelated changes instead of sweeping them into one commit.
4. Run relevant tests or record why they were not run.
5. Stage only the intended files.
6. Commit with a message that names behavior, scope, and validation.
7. Push the current branch only when requested, setting upstream when needed.
8. Create or update a PR when requested and GitHub tooling is available.

Use `scripts/git-change-summary.js` for a quick branch/status/diff-stat summary before staging.

## Commit Message

Use:

```text
<imperative summary>

<why this change exists, if not obvious>

Validation:
- <command or manual check>
```

## PR Body

- `Summary`: what changed.
- `Validation`: commands and outcomes.
- `Risk`: migrations, feature flags, external services, or user-visible behavior.
- `Notes`: follow-ups outside this change.

## Rules

- Never revert unrelated user changes.
- Never commit secrets, local env files, caches, or generated noise.
- If the worktree is dirty before your changes, preserve that context.
- If committing is blocked by failing tests, report the blocker instead of hiding it.
- Do not force-push unless explicitly requested.
- Report the commit hash and branch after a successful handoff.
