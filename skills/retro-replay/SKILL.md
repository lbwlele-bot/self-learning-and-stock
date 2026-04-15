---
name: retro-replay
description: Replay historical windows without leaking future knowledge. Use when training the system on past market events, reconstructing what was knowable on each day, or building a fact layer plus validation window for a case study.
---

# Retro Replay

Use this skill to train the system on historical windows without cheating. Its job is to separate what was visible on the day from what only became clear later, then add a validation layer after the initial judgment.

## Read Order

- `../../docs/playbooks/RETROSPECTIVE_METHOD.md`
- `../../docs/frameworks/FACT_GROUNDING.md`
- relevant case files in `../../docs/cases/` only if they are part of the target window

Use `references/output-order.md` for the required output sequence.

## Replay Workflow

### 1. Define the windows

Split the case into:

- pre-window
- replay window
- validation window

Do not collapse them into one timeline.

### 2. Use only day-visible information

For each replay day, limit inputs to:

- same-day or earlier news
- same-day market reactions
- signals that would have been observable then

Do not smuggle later outcomes into earlier reasoning.

### 3. Output in layers

Always present:

1. `fact layer`
2. `layered view`
3. `reasoning layer`
4. `discussion questions`
5. `tentative judgment`

Only after that should you add:

6. `validation layer`

### 4. Persist as a case artifact

Write persistent replay outputs into `../../docs/cases/`.

If the work includes both replay and later validation, keep them as separate but connected case files.
