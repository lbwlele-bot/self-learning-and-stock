---
name: consent-capture
description: Distill reusable insights from the current conversation, decide which system layer they belong to, propose exact destinations inside the repo, and wait for explicit user approval before writing anything. Use when the user wants to save, capture, distill, summarize, or promote part of the discussion into the long-term system without polluting it.
---

# Consent Capture

Use this skill when the conversation produces potentially reusable ideas and the user wants a consent-gated path to store them locally.

This skill is a gate before `../../skills/memory-governor/`.

It does not write by default.

Its real job is not simple note taking.

Its job is to decide:

- whether the idea should be kept at all
- which layer of the system it belongs to
- which single file should own it
- whether the current wording should be added, tightened, deferred, or rejected

## Core Rule

Never write any distilled insight into repo files unless the user gives explicit approval for the current capture batch.

Valid approval examples:

- `save it`
- `store this`
- `write the approved items`
- `only save 1 and 3`

If approval is missing, stop at the proposal stage.

## Layer-First Rule

Before classifying the content type, first decide the storage layer.

Use `references/system-levels.md`.

The layer options are:

- `discard`
- `artifact layer`
- `topic layer`
- `system layer`
- `method layer`

Do not jump straight from a sentence to a file path.

First decide the layer, then the type, then the exact file.

## Promotion Threshold

Use `references/promotion-tests.md`.

Every candidate should be checked on four questions:

1. `reuse horizon`
   - only this turn
   - this topic for a while
   - reusable across many future topics
2. `scope`
   - one case or one company
   - one topic
   - the whole system
3. `stability`
   - raw reaction
   - provisional hypothesis
   - stable principle or logic anchor
4. `execution value`
   - no durable value
   - useful as an artifact
   - useful as a reusable rule or bridge

Only promote when the answers justify it.

## What To Capture

Promote only content that is both:

- reusable beyond the current turn
- specific enough to improve the system

Good candidates:

- a new logic base
- a stable working hypothesis
- a principle for how to reason
- a reusable investment translation
- a reusable execution rule
- a clarified open question
- a concise stage summary

Do not promote:

- raw emotions
- one-off phrasing
- temporary market chatter
- duplicated restatements of existing memory
- claims that are still unverified

## Workflow

### 1. Distill candidate insights

Extract only the smallest number of high-value items from the current discussion.

Default to `1-3` items.

### 2. Decide the system layer

For each candidate, pick exactly one layer first.

Use these defaults:

- `discard`
  - raw reaction
  - phrasing with no durable reuse
  - duplicate with no meaningful improvement
- `artifact layer`
  - case-specific observation
  - one-off market note
  - company-specific detail
  - session-only learning fragment
- `topic layer`
  - a current topic update
  - an active working hypothesis
  - a shift in the status of a specific theme
- `system layer`
  - a logic base
  - a principle
  - an open question
  - a stage summary that changes the system state
- `method layer`
  - a reusable research rule
  - a reusable execution bridge
  - a repeatable checklist or filter

### 3. Classify each candidate inside the chosen layer

For each item, classify it using the same buckets as `../../skills/memory-governor/`:

- `logic base`
- `working hypothesis`
- `investment translation`
- `execution rule`
- `principle`
- `open question`
- `stage summary`

Use `references/approval-flow.md` and `../../skills/memory-governor/references/routing-matrix.md` when needed.

Only use a classification that matches the chosen layer.

Examples:

- `logic base`, `principle`, `open question`, `stage summary` usually imply `system layer`
- `working hypothesis` usually implies `topic layer`
- `investment translation` usually implies `method layer`
- `execution rule` usually implies `method layer`

### 4. Check for duplication risk

Before proposing storage:

- inspect the likely target file
- see whether the idea already exists
- if it already exists, propose `tighten existing text` instead of `add new text`

### 5. Choose one write action

Each candidate must end in exactly one action:

- `reject`
- `artifact only`
- `tighten existing`
- `add new`
- `defer until more evidence`

Default to the smallest safe action.

### 6. Present a capture slate

Return a short approval slate with one numbered item per candidate:

1. candidate insight
2. storage layer
3. classification
4. proposed target file
5. write action
6. why it belongs there
7. evidence state

Use evidence state as one of:

- `confirmed enough`
- `working hypothesis only`
- `question, not conclusion`

### 7. Wait for approval

Do not edit files yet.

Wait for the user to approve:

- all items
- selected item numbers
- or a rewritten version

If the user partially approves, write only the approved items.

### 8. Hand off to memory-governor

After approval, write only the approved items and route each item to one primary destination.

If an approved item still has multiple possible homes, follow `../../skills/memory-governor/` and keep one primary home only.

When the target is `method layer`, update the closest file in:

- `../../docs/frameworks/`
- `../../docs/playbooks/`

When the target is `artifact layer`, keep it in:

- `../../docs/cases/`
- `../../docs/stocks/`
- `../../sessions/`

Do not promote artifact content upward unless the user explicitly wants that abstraction.

## Approval Modes

Support these approval styles:

- `approve all`
- `approve selected numbers`
- `approve after rewrite`
- `reject all`

If the user says only `save it` and the slate is still ambiguous, save only the clearly strongest item or ask one short follow-up.

## Output Contract

At proposal time, return:

1. `capture slate`
2. `approval needed`
3. `what will not be written yet`

After approval and write:

1. `approved items`
2. `storage layers chosen`
2. `written target files`
3. `why each write was unique`
4. `any pointers added elsewhere`
