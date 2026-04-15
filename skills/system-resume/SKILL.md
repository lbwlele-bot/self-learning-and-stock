---
name: system-resume
description: Resume the current repo system without rebuilding the framework from scratch. Use when starting a new conversation, switching back into this repository after context loss, continuing an existing topic, or deciding which workflow should run next.
---

# System Resume

Use this skill to rejoin the current system quickly and safely. The goal is to restore the active topic, relevant logic bases, current working assumptions, and the next workflow instead of starting from zero.

## Read Order

Always begin with the current repo truth layer:

1. `../../START_HERE.md`
2. `../../SYSTEM_INDEX.md`
3. `../../TOPIC_MAP.md`
4. `../../memory/logic-bases.md`
5. `../../memory/context.md`
6. `../../memory/principles.md`
7. `../../memory/open-questions.md`

Then load only the extra files needed for the current task:

- `../../CURRENT_SYSTEM.md`
- `../../OPERATING_MODEL.md`
- `../../skills/README.md`

Use `references/source-map.md` for the routing summary.

## Resume Workflow

### 1. Identify the current topic

Use the user request first.

If the user names a topic, resume that topic directly from `../../TOPIC_MAP.md`.

If the user does not name a topic, infer the most likely active topic from:

- the current request
- the latest conversation state
- the active themes in `../../CURRENT_SYSTEM.md`

Do not preload unrelated topics just because they are adjacent.

### 2. Reconnect the topic to the system backbone

For the selected topic, extract:

- current status
- related logic bases
- active working assumptions
- current execution expression

Keep the backbone explicit:

`logic base -> working hypothesis -> investment translation -> execution rule`

### 3. Decide the current working layer

Classify the user's ask as one of:

- `system resume / topic restore`
- `working hypothesis expansion`
- `discovery`
- `company research`
- `market observation / action discussion`
- `memory update`

### 4. Recommend the next workflow

Default to this chain:

`system-resume -> discovery-pipeline -> company-card-builder -> market-ops -> consent-capture -> memory-governor`

For the current mainline around `high-friction world / dollar weaponization / A-share expectation gap / retail niche`, recommend:

- `discovery-pipeline` first when the user is still narrowing beneficiaries
- `company-card-builder` when candidates already exist
- `market-ops` only when the discussion has moved into market state or action
- `consent-capture` when a conversation has produced reusable ideas that may enter the long-term system
- `memory-governor` after the promoted conclusion is approved

## Output Contract

Return a short resume with:

1. `current topic`
2. `related logic bases`
3. `active working hypotheses`
4. `current working layer`
5. `recommended next workflow`

Do not rebuild the framework in full unless the user explicitly asks for a full reorientation.
