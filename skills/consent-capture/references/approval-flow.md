# Approval Flow

Use this decision order:

1. Is the idea reusable beyond this turn?
2. Which system layer does it belong to?
3. Is it already present in the likely target file?
4. If yes, should we tighten existing wording instead of adding a new bullet?
5. If no, what is the single best primary destination?
6. Does the user approve this item for storage?

## Proposal Template

Use a short numbered slate:

1. `<candidate insight>`
   - layer: `<discard | artifact | topic | system | method>`
   - type: `<classification>`
   - target: `<primary file>`
   - action: `<reject | add new | tighten existing | artifact only | defer>`
   - evidence: `<confirmed enough | working hypothesis only | question, not conclusion>`
   - reason: `<one sentence>`

Keep the slate compact. The goal is to make approval easy.

## Approval Guardrails

- No silent writes
- No batch dumping of the whole conversation
- No promotion of unverified claims into principles
- No duplicate definitions across overview files
- No creation of new summary files just to hold one idea
