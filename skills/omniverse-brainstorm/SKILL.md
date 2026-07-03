---
name: omniverse-brainstorm
description: Generate and narrow options, concepts, strategies, or technical recommendations before implementation. Use when the user asks to brainstorm, ideate, compare approaches, choose direction, create a technical POV, decide build-versus-buy, sequence roadmap or migration work, or produce a tradeoff-heavy recommendation.
---

# Omniverse Brainstorm

Use this skill to expand the option space, make a decision, or sequence a direction without losing engineering discipline.

## Workflow

1. State the problem, decision, or strategic objective in one sentence.
2. Name the audience, constraints, decision criteria, dependencies, and reversibility.
3. Generate distinct options, concepts, or sequences rather than minor variations.
4. Compare usefulness, feasibility, cost, risk, and validation path.
5. Recommend one path and name the next prototype, checkpoint, or revisit trigger.

## Output Shape

- `Problem or decision`: what needs to be solved or chosen.
- `Criteria and constraints`: facts that shape the answer.
- `Options`: concrete approaches, concepts, or sequences.
- `Recommendation`: the best path and why.
- `Next step`: what to inspect, prototype, decide, or revisit.

## Rules

- Separate facts from preferences and speculation.
- Keep speculation labeled.
- Prefer options that preserve optionality and can be tested cheaply.
- Avoid false balance when evidence favors one path.
- If the user wants code, continue into implementation after choosing the approach.
