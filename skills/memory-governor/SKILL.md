---
name: memory-governor
description: Route new conclusions into the correct long-term system file or artifact. Use when a discussion produces a reusable conclusion, a new working assumption, a principle, a topic update, an open question, or a stage summary and you must avoid duplicate writes.
---

# Memory Governor

Use this skill after a discussion produces a conclusion that might belong in the long-term system. Its job is to pick one primary destination, keep the write unique, and stop the repo from duplicating the same idea across multiple overview files.

When the conclusion comes from live conversation distillation, prefer running `../../skills/consent-capture/` first so the user can approve the promotion before anything is written.

## Primary Routing Rule

Every new conclusion must first be classified as one of:

- `logic base`
- `working hypothesis`
- `investment translation`
- `execution rule`
- `principle`
- `open question`
- `stage summary`

Use `references/routing-matrix.md` for the exact destinations.

## Routing Workflow

### 1. Decide whether the content is reusable

Promote only if the conclusion is reusable beyond the current turn.

Keep it out of long-term files if it is:

- a one-off market note
- a temporary data point
- a company-specific detail without system value
- a case-only observation

Those belong in:

- `../../docs/cases/`
- `../../docs/stocks/`
- `../../sessions/`

### 2. Pick one primary destination

Use these defaults:

- `logic base` -> `../../memory/logic-bases.md`
- `principle` -> `../../memory/principles.md`
- `open question` -> `../../memory/open-questions.md`
- `stage summary` -> `../../memory/context.md`
- `working hypothesis` -> `../../TOPIC_MAP.md`
- `investment translation` -> `../../docs/frameworks/INVESTMENT_TRANSLATION.md`
- `execution rule` -> `../../docs/playbooks/ACTIONS.md`

If a conclusion is only a local or case-specific version of either one, keep it as an artifact instead of promoting it upward.

### 3. Prevent duplication

If a conclusion touches multiple layers:

- write the full version once
- add at most a short pointer elsewhere
- do not redefine the same concept in two overview files

### 4. Prefer topic updates over system sprawl

When a new conclusion mainly changes the current state of a topic, prefer updating:

- `../../TOPIC_MAP.md`

Do not create a new summary file just to hold one new insight.

## Output Contract

When routing, state:

1. `classification`
2. `primary target file`
3. `why it belongs there`
4. `whether any pointer is needed elsewhere`
5. `if it should stay as an artifact instead`
