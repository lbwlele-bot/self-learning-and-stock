# Promotion Tests

Check every candidate before proposing storage.

## Test 1: Reuse Horizon

- `turn-only`
  - useful only right now
- `topic-window`
  - useful while the current topic is active
- `system-durable`
  - likely useful across many future discussions

## Test 2: Scope

- `local`
  - one case, one company, one replay, one day
- `topic`
  - one named theme
- `system`
  - many themes across the repo

## Test 3: Stability

- `raw`
  - still a reaction
- `hypothesis`
  - plausible but not yet proven
- `stable`
  - mature enough to guide future work

## Test 4: Evidence State

- `confirmed enough`
  - strong enough for system or method updates
- `working hypothesis only`
  - belongs in topic tracking or as a clearly marked hypothesis
- `question, not conclusion`
  - belongs in open questions if worth keeping

## Fast Routing Heuristic

If the candidate is:

- `turn-only + local + raw`
  - reject
- `topic-window + local/topic + hypothesis`
  - artifact layer or topic layer
- `system-durable + system + stable`
  - system layer or method layer

## Anti-Bloat Rule

When unsure between two higher layers, choose the lower one.

Examples:

- topic layer before system layer
- artifact layer before topic layer
- tighten existing text before adding new text
