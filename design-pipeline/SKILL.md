---
name: design-pipeline
description: Run an automated end-to-end design pipeline for ConstructConnect prototypes. Orchestrates three agents in sequence — Planner (creates a design spec against the Blueprint design system), Generator (builds the HTML prototype), and Evaluator (scores it and loops until it passes). Use when you want a fully evaluated, Blueprint-compliant prototype from a short brief with minimal manual steps. Invoke with a 1–4 sentence brief describing what to build. For standalone prototype work outside the Blueprint system, use the prototype skill instead.
---

# Design Harness

You are orchestrating a three-agent design pipeline. Your job is to execute the agents in sequence, manage handoffs between them, enforce the gate conditions at each stage, and run the Generator–Evaluator feedback loop until the sprint passes or 5 iterations are reached.

The user's brief is: **$ARGUMENTS**

The three agent definitions live in the `/harness/` directory of this project:
- `harness/planner-agent.md` — Planner instructions
- `harness/generator-agent.md` — Generator instructions
- `harness/evaluator-agent.md` — Evaluator instructions

The `product-design-review` skill (in `skills/product-design-review/SKILL.md`) provides the accessibility, AI design pattern, and platform guidelines context. The Evaluator must use it.

Read all four files now before proceeding.

---

## Execution Order

### Stage 1 — PLANNER

Adopt the Planner persona as defined in `harness/planner-agent.md`.

Execute the Planner in full:
1. Read the Blueprint design system files as directed in `harness/planner-agent.md`.
2. Generate `design-spec.md` in the current working directory.
3. Present the full spec to the user and request explicit approval.
4. **Do not advance to Stage 2 until the user says "approved" or equivalent.**

If the user requests changes to the spec, update `design-spec.md` and ask for approval again. Repeat until approved.

---

### Stage 2 — GENERATOR

Adopt the Generator persona as defined in `harness/generator-agent.md`.

Execute the Generator in full:
1. Declare the sprint contract, then immediately begin building — no confirmation needed.
2. Build the prototype.
3. Follow all build rules: single-file or multi-file HTML/CSS/JS, real content, full interactions, visual language from spec.
4. Make and state the strategic decision (refine or pivot).
5. Hand off to Stage 3 with: file paths, sprint contract, reference to `design-spec.md`, strategic decision.

---

### Stage 3 — EVALUATOR (with feedback loop)

Adopt the Evaluator persona as defined in `harness/evaluator-agent.md`.

Also load and apply the `product-design-review` skill context for its accessibility, AI design pattern, and platform guideline sections.

**Initialize iteration counter: 1**

Execute the evaluation loop:

```
LOOP (max 5 iterations):
  1. Read the prototype file(s)
  2. Produce the three-part report (Rubric + Critique + Pass/Fail Contract Review)
  3. Make the sprint outcome decision

  IF sprint PASSES:
    - Write design-review.md
    - Output final report to user
    - EXIT LOOP

  IF sprint FAILS AND iteration < 5:
    - Append Revision Brief to report
    - Increment iteration counter
    - Hand Revision Brief back to the Generator
    - Generator revises the prototype per the Revision Brief (no new contract negotiation needed)
    - Continue to next iteration

  IF sprint FAILS AND iteration == 5:
    - Write design-review.md with persistent issues flagged
    - Output final report to user with "Maximum iterations reached" notice
    - EXIT LOOP
```

---

## Handoff Protocol

At each stage transition, explicitly announce which agent you are now embodying:

> "--- PLANNER ---"
> "--- GENERATOR ---"
> "--- EVALUATOR (Iteration N) ---"

This makes the pipeline legible to the user.

---

## File Outputs

The harness produces these files in the current working directory:

| File | Produced by | When |
|------|-------------|------|
| `design-spec.md` | Planner | After user approves spec |
| `[feature-name].html` (kebab-case, descriptive) | Generator | After sprint contract confirmed |
| `design-review.md` | Evaluator | On sprint pass or iteration 5 |

---

## Important Rules

- **Never skip a gate.** Do not advance from Planner to Generator without user spec approval. Do not advance from Generator to Evaluator without user contract confirmation.
- **Never stub interactions.** If an interaction is in the contract, it must be in the prototype.
- **Never use placeholder content.** Invent realistic domain-appropriate content.
- **Apply the anti-patterns list.** Any anti-pattern from the spec found in the prototype is an automatic Originality score of 1.
- **Be honest in evaluation.** Scores of 4–5 must be earned. The purpose of the feedback loop is to improve the work, not to declare success prematurely.
- **The Generator's strategic decision matters.** The Evaluator must engage with it explicitly in the written critique.

---

## Starting Now

Begin with Stage 1. Read `harness/planner-agent.md` and adopt the Planner persona.

The brief is: **$ARGUMENTS**

Load the Blueprint design system files now, then generate the spec.
