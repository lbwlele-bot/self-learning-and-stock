---
name: market-ops
description: Run the repo's market observation workflows. Use when doing a daily update, reacting to a possible major event, running a nightly or next-day attention check, or doing a weekly market scan with standardized variable checks and action output.
---

# Market Ops

Use this skill as the unified entry for market-state workflows. It replaces hand-written trigger prompts for daily updates, alert triage, nightly checks, next-day checks, and weekly scans.

## Read Order

Always load the minimum shared method layer:

- `../../docs/playbooks/README_TRADING_LOOP.md`
- `../../docs/playbooks/ACTIONS.md`
- `../../docs/playbooks/MONITORING_WORKFLOW.md`
- `../../docs/frameworks/SIGNALS.md`
- `../../templates/market-check-template.md`

Then load only the sub-workflow reference needed for the request. Use `references/workflow-map.md`.

## Workflow Selection

Choose exactly one sub-workflow:

- `daily`
  - end-of-day market update
  - standard output with information layering and action
- `alert`
  - possible major event during the day
  - decide whether to upgrade into a full market update
- `nightly`
  - determine whether tomorrow deserves more attention
- `next-day`
  - pre-window check for known meetings, policy windows, or catalysts
- `weekly`
  - higher-level scan when the pace is slower

## Shared Output Rules

Every run should produce:

1. `information layering`
   - background risk
   - same-day catalyst
   - sentiment narrative
2. `primary variables`
3. `cross-check variables`
4. `environment judgment`
5. `minimum action conclusion`

Use the existing variable logic:

- primary: `Shanghai Composite`, `Brent`
- cross-check: `CSI 300`, `US Dollar Index`

## Action Rule

When the user moves from observation into action discussion, always apply:

- `../../docs/playbooks/ACTIONS.md`
- especially:
  - `1 percent action on a 70-point judgment`
  - `loss classification`

Do not jump from macro conviction straight to a trade.

## Artifact Rule

If the user wants a persistent output, write the result into `../../docs/cases/` using a dated file name.

If persistence is not requested, return the standardized output inline.
