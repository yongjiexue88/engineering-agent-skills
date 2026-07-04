---
name: omniverse-project-memory
description: Reuse or capture durable project knowledge. Use when the user asks to load prior solutions, review repo memory, document what was learned, preserve debugging knowledge, write a solution note, or prevent the same problem from being rediscovered later.
---

# Omniverse Project Memory

Use this skill to find useful project history and save reusable knowledge for future work.

## Workflow

1. Search `docs/solutions/`, `docs/plans/`, `docs/reviews/`, and project docs when prior knowledge may exist.
2. Read only notes relevant to the current task and verify them against current code.
3. After hard or non-obvious work, capture the root cause, failed paths, final fix, and validation.
4. Save a concise solution note under `docs/solutions/` when writing files is appropriate.
5. Link related files, commands, issues, PRs, or logs so the knowledge can be reused.

## Solution Note Shape

Use `scripts/create-solution-note.js "<problem>"` to create the standard `docs/solutions/` file when writing is appropriate.

```markdown
# <Problem>

Date: YYYY-MM-DD

## Context
## Root Cause
## Fix
## Validation
## Reuse This When
## Related Files
```

## Rules

- Capture facts and repeatable signals, not a diary.
- Do not include secrets, tokens, private customer data, or sensitive logs.
- Keep notes short enough that a future agent can scan them quickly.
- If no relevant project memory exists, say so and continue normally.
