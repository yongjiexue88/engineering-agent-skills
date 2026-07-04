# Architecture Audit

Use this skill when you want a coding agent to audit non-trivial architecture or system-design risk before it ships.

## Core Uses

| Use case | What the skill contributes |
| --- | --- |
| System design | Architecture tradeoffs and design-pattern guidance for common production systems. |
| ADR/RFC review | Decision quality, tradeoffs, assumptions, and rollout risk. |
| Implementation architecture | State ownership, dependency boundaries, concurrency risk, and testability. |
| Production readiness | Security, data integrity, observability, scaling, rollback, and failure modes. |

## Invocation

```txt
Use architecture-audit to review this architecture proposal.
```

The runtime behavior is defined in `skills/architecture-audit/SKILL.md`.
