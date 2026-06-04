---
component: spinal_cord
kind: transition
direction: afferent-sensory   # afferent (up) | efferent (down) | afferent-sensory (in)
from: thoracic                # the feedback item at the active segment
to: any                       # the lane's dispatch targets an existing path
---

# triage : the four-lane sort, and the record that makes it safe

<!--
The grey matter of the dorsal horn. It consumes one `status: received` feedback item from
intake and routes it into exactly ONE of four lanes, recording the decision before any
dispatch happens. The triage is its OWN reflex/mediated gate — distinct in kind from the
artifact-promotion reflexes. Its "local frontmatter" is the feedback ITEM's own fields, not
the whole column. The promotion reflexes (transitions/) are untouched and stay purely local.
-->

## What moves
One `status: received` feedback item → the same item, `status: classified`, with exactly one
`lane` set and a line written to the append-only triage log. After classification the lane's
own dispatch (an existing transition, or a new-seed deferral) carries the item onward and sets
`status: dispatched`, then `resolved`.

The four lanes:

- **reflex-tweak** — small, local, in-aesthetic; apply *in place* on the active segment.
  ("more padding," "angle the top.") Dispatches as a reflex edit to the live wave's work.
- **wave-amendment** — larger than a tweak but still serving the *current* want; fold into the
  breathing wave as an added/modified item. Dispatches via `2-lumbar-to-3-thoracic.md` into the
  *current* plan.
- **send-back** — the built thing has **drifted from the want**. A *correction*. Dispatches as
  an **efferent send-back** — and therefore, per invariant 5, **only the crown may originate
  it**. The dorsal horn recognizes the correction; the crown emits it.
- **new-seed** — genuinely new desire. Dispatches to the **base** as a coccygeal seed and
  **ascends normally**, vertebra by vertebra. **Never** fast-tracked into the live wave.

Exactly one lane per item.

## Reflex conditions
This is the triage's *separate* reflex surface: it reads the **feedback item's own fields**
(`raw`, `entered_at`, `gate`) and the active segment — not the whole column. A lane may be
assigned by reflex only when it is decidable from the item + active segment alone, and only
toward a **safe** lane (one that cannot destabilize a live wave by *accelerating* something):

- [ ] `gate: human` is **not** set on the item (a gated item never auto-dispatches — see
      Escalation).
- [ ] Either: the text describes a small, local, cosmetic change to something *in the current
      wave* → **reflex-tweak**;
- [ ] Or: the text is unambiguously a brand-new want, unrelated to the current wave's artifacts
      → **new-seed** (the *safe default*: it slows, it cannot destabilize).

These run inline / as a deterministic step. The bias is **asymmetric**: reflex is permitted
only toward the safe lanes. When unsure between a faster and a slower lane, the fallback is
always the slower one (new-seed), never the faster (tweak).

## On promotion
Classify-and-log — **two writes, atomic with assigning the lane**:

1. **Onto the feedback item:** set `lane: <chosen>` and `status: classified`; set `routed_to:`
   once dispatch resolves the target artifact, then `status: dispatched` → `resolved`.
2. **Into the triage log** — an append-only ledger so the sort is *visible and recorded*:

   ```
   thoracic_infolding/<plan>/feedback/_triage-log.md
   ```

   Append-only. One line per item:

   ```
   - <wave>-<nnn> | <yyyy-mm-dd> | lane: <lane> | mode: <reflex|mediated> | origin: <human|...>
     | raw: "<verbatim>" | routed_to: <path> | by: <inline|crown-verdict>
   ```

Then dispatch through the lane's **existing** path — no new transition is invented:

| Lane | Dispatch | Reuses |
|------|----------|--------|
| reflex-tweak | apply edit in place on the live wave's work | reflex write (execution-topology tier 1) |
| wave-amendment | add/modify an item in the *current* plan | `../transitions/2-lumbar-to-3-thoracic.md` |
| send-back | crown emits efferent return to the drift's level | `../transitions/efferent-send-backs.md` |
| new-seed | create coccygeal seed; ascend base-up | `../transitions/0-coccygeal-to-1-sacral.md` … full climb |

The **new-seed lane forbids skipping a vertebra**: the seed enters at the base and climbs
`coccygeal → sacral → lumbar → thoracic` through the ordinary reflexes (and through the
new-desire human-gate at `0-coccygeal-to-1-sacral.md`). It is never injected mid-column and
never folded into the *live* wave. This is the want's hardest red line — *new desire slipping
in disguised as a small fix* — enforced structurally: by the time a new-seed item reaches a
wave, it is a deliberate, logged desire, not a smuggled tweak.

## Escalation
Risk is always routed to judgment. Escalate (relay up; the crown's judgment subagent rules;
the ruling returns down the cord) when:

- **send-back** is implied — asserting "the built thing drifted from the want" is a
  *correction*, which by invariant 5 is **crown-originated**. The dorsal horn never assigns
  send-back by reflex; any item that *looks* like a drift escalates, the crown judges
  drift-vs-amendment-vs-tweak, and on confirmation emits the efferent send-back itself.
- **tweak vs. wave-amendment** is not locally obvious — does this "small" change actually
  reshape the wave? Reshaping a plan's breath is already a crown matter under
  `2-lumbar-to-3-thoracic.md`'s Escalation.
- **new-want vs. amendment** is ambiguous — the dangerous case. Never default an unclassified
  item into a live-wave lane; the safe fallback is the slower lane.

Beyond crown escalation, triage may raise the **human-gate**: when uncertainty is of a kind
the crown's judgment subagent should not silently resolve (high blast-radius amendment, or
genuine new-want/amendment ambiguity), it sets `gate: human` and surfaces the intended action
for a person's assent. An item already carrying `gate: human` (from intake, or set by the
human) **always** pauses for assent before dispatch — even a reflex-tweak. See the *Movable
oversight line* in `../../cervical_awareness/cord-stewardship.md`.

---
*Governed by `../../cervical_awareness/cord-stewardship.md`.*
