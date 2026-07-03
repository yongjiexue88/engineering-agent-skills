---
name: omniverse-test-browser
description: Test browser-based applications, UI workflows, and user-facing polish. Use when the user asks to run browser QA, inspect a page, verify a frontend change, check responsive behavior, smoke test a dev server, validate user flows, or refine copy, states, accessibility basics, and release readiness.
---

# Omniverse Test Browser

Use this skill for practical browser verification and product polish.

## Workflow

1. Start or identify the app URL.
2. Test the critical happy path first.
3. Check error, loading, empty, and permission states that are reachable.
4. Verify desktop and mobile layouts for overlap, clipped text, and broken controls.
5. Check copy, hierarchy, primary actions, keyboard basics, and screen-reader basics where practical.
6. Capture evidence: screenshots, console errors, network failures, and steps.
7. Report issues with reproduction steps and severity.

Use `scripts/create-browser-qa-report.js "<workflow>" --url <url>` when the QA findings should be saved under `docs/qa/`.

## Rules

- Do not rely only on static code review for UI behavior.
- If no browser automation tool is available, provide a manual checklist and note the gap.
- Prioritize broken workflows over visual nits.
- Match the existing design language; avoid cosmetic churn that does not improve use.
