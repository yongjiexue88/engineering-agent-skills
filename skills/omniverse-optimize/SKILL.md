---
name: omniverse-optimize
description: Improve performance, cost, reliability, maintainability, or developer workflow after a baseline exists. Use when the user asks to optimize slow code, expensive calls, build times, database queries, API latency, memory use, operational overhead, duplicated logic, unnecessary abstractions, or complex code.
---

# Omniverse Optimize

Optimize or simplify with measurements, behavior boundaries, and guardrails.

## Workflow

1. Define the metric, target, or behavior that must remain unchanged.
2. Capture the baseline with tests, commands, logs, traces, query plans, or code reading.
3. Identify the dominant cost or complexity source.
4. Choose one focused optimization or simplification.
5. Verify the metric improved or behavior stayed equivalent.
6. Add a regression check when the change is easy to break.

## Common Levers

- Remove redundant work.
- Move work off critical paths.
- Batch, cache, or precompute.
- Add indexes or reduce query fanout.
- Stream large data instead of buffering.
- Replace quadratic logic with bounded structures.
- Inline needless wrappers.
- Split mixed responsibilities.
- Consolidate repeated validation or serialization.

## Rules

- Do not optimize speculative bottlenecks.
- State tradeoffs such as memory, freshness, complexity, or consistency.
- Do not simplify by deleting edge-case handling.
- Preserve readability unless measured gain justifies complexity.
