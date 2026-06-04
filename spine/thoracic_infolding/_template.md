---
stage: thoracic        # 3 · infolding / waves
status: planned        # planned | breathing | complete
gate: none             # none | human — raise to pause this whole plan for human assent
gate_reason:           # why the human-gate was placed (when gate: human)
---

# <name of the plan>

<!--
Fold architected items into waves that can breathe. A WAVE is a set of items buildable in
parallel because they don't block each other. Waves are sequenced; items within a wave are
not. Only fold in items that already exist as lumbar_architecture write-ups. Keep waves
small enough to breathe. Delete any section that doesn't want to exist.
-->

## Scope
<What this plan covers, in a line or two.>

## Waves
<!-- Add or remove waves freely. Each item should link to its lumbar write-up.
     A single wave may carry an inline human-gate — `### Wave 2 — name  (gate: human — why)` —
     which pauses that wave for human assent; the plan-level `gate` frontmatter field covers
     the whole plan. -->

### Wave 1 — <name>
- [ ] <item> — `../lumbar_architecture/...`
- [ ] <item> — `../lumbar_architecture/...`

### Wave 2 — <name>   (depends on: Wave 1)
- [ ] <item> — `../lumbar_architecture/...`

## Dependencies
<Optional. Which waves must precede which, and why — the order the breath must follow.>

## Coordination notes
<Optional. Anything parallel streams need to know to avoid colliding.>

---
*Executed and verified work hands upward to `../cervical_awareness/` for documentation and oversight.*
