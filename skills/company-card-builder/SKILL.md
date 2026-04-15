---
name: company-card-builder
description: Build or refresh a standardized company research card from a watchlist candidate. Use when a company has already passed theme-level screening and now needs a repeatable card with evidence, validation signals, counterarguments, and a current conclusion.
---

# Company Card Builder

Use this skill after a candidate has already passed the discovery layer. Its job is to build or refresh a reusable company card with a consistent structure and evidence hierarchy.

## Read Order

- `../../docs/stocks/README.md`
- `../../docs/playbooks/DEEP_RESEARCH_CHECKLIST.md`
- `../../docs/playbooks/WATCHLIST_TEMPLATE.md`
- relevant watchlist artifact or candidate note
- existing company card if one already exists

Use `references/card-structure.md` for the standard section order.

## Build Workflow

### 1. Confirm the object is ready

Use this skill only when the object has already passed theme-level screening.

If the object is still at the narrative stage, send it back to:

- `discovery-pipeline`

### 2. Search in evidence order

Use the repo's deep-search order:

1. official and hard disclosures
2. ecosystem and developer signals
3. customer and scene signals
4. auxiliary validation

Do not over-weight secondary media if primary materials are available.

### 3. Build the card in a stable shape

Include:

- why it enters the system
- business and profit path
- support evidence
- validation signals
- counterarguments and risks
- current conclusion

### 4. Decide the artifact location

If it is a persistent company card, write to:

- `../../docs/stocks/<ticker>-<company-name>.md`

If the object is still provisional or lacks enough identity to become a stock card, keep it in:

- `../../docs/cases/`

## Output Rule

Do not force a trading conclusion.

It is acceptable for the current conclusion to stay at:

- `normal observation`
- `priority observation`
- `worth tracking, not yet a trading action`
