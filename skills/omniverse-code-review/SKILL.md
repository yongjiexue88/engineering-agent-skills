---
name: omniverse-code-review
description: Perform production-focused code review and PR feedback triage. Use when reviewing diffs, pull requests, branches, files, generated code, implementation changes, reviewer comments, or requested changes for correctness, security, tests, regressions, maintainability, and release risk.
---

# Omniverse Code Review

Review like a senior engineer protecting production behavior.

## Workflow

1. Inspect the diff, nearby call sites, and relevant reviewer comments before judging.
2. Identify correctness, data integrity, auth, concurrency, error handling, performance, and migration risks.
3. Check whether tests cover the risky behavior and failure modes.
4. Separate blocking findings from nits, optional refactors, and follow-ups.
5. For PR feedback, group comments into must-fix, clarify, disagree, and follow-up.
6. If a finding depends on reproducing a failure, tracing runtime behavior, or running a failing check, hand off to `omniverse-debug` with the exact signal, suspected boundary, and cheapest next check.
7. Provide actionable fixes or short reviewer replies tied to code evidence.

## Output Shape

Lead with findings:

- `Severity`: critical, high, medium, low.
- `Location`: file and line.
- `Issue`: the behavior that can fail.
- `Impact`: why it matters.
- `Fix`: the smallest safe correction.

Then include:

- `Open questions`
- `Tests or validation gaps`
- `Debug handoff`, when a finding needs runtime evidence
- `Summary`
- `Reviewer replies`, when resolving PR comments

## Rules

- Findings first. Do not start with praise or a broad summary.
- Do not flag style preferences unless they hide real risk.
- If no findings exist, say that clearly and name residual risk.
- When reviewing generated code, check integration contracts more carefully than formatting.
- When disagreeing with feedback, explain with evidence and offer a concrete alternative.
- Do not turn review into broad debugging by default; use `omniverse-debug` only when review evidence is insufficient without reproduction, logs, traces, or a failing command.
