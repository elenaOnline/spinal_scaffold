---
stage: cervical        # 4 · awareness
kind: guideline
watches: the spinal cord (../spinal_cord/)
---

# Cord Stewardship — when and how to change the transitions

The spinal cord transports and reflexes; it does not govern itself. Governance belongs to the
crown, because changing a handoff rule is a change to *the whole column's* behavior, and only
the crown sees the whole. This document is the crown's standing understanding of **when a
transition should change, and how to change it without breaking coherence.**

The default posture is **stillness**. The cord is meant to be stable; most projects should
never touch it. Change it only when the evidence below appears — and then minimally.

## When to change a transition

Watch for these signals along the cord:

- **Chronic escalation.** A transition keeps escalating to the crown for the *same kind* of
  judgment. The reflex is too tight — its conditions should absorb that case, or the case
  reveals a missing local field. (Conversely: a reflex that keeps promoting things the crown
  later sends back is too loose and should tighten.)
- **Stalling.** Artifacts pile up at a level and don't promote. The reflex conditions may be
  unsatisfiable in practice, or reference frontmatter that artifacts don't actually carry.
- **Drift.** A template's frontmatter changed (a `status` value renamed, a field added) and a
  transition's reflex conditions no longer match it. The cord must be re-synced to the bones
  it reads.
- **A new concern crosses the column.** A new stage, or a cross-cutting component like the
  cord itself, needs its own handoff. Add a transition rather than overloading an existing one.
  *This signal fired for feedback intake* — the system sensing the world's response to what it
  built is exteroception, a genuinely new concern the cord could not carry. It earned the
  **afferent-sensory stream** ([`../spinal_cord/afferent-sensory/`](../spinal_cord/afferent-sensory/))
  as an *addition*, not an overload of `efferent-send-backs.md` or an afferent-promotion spec.

## How to change a transition — the invariants

A change is coherent only if it preserves every one of these. The crown's job is to refuse
changes that break them:

1. **Every transition keeps both a reflex path and an escalation point.** A handoff that is
   pure-reflex has abandoned whole-system judgment; one that is pure-escalation has made the
   brain do the cord's job. Both are regressions.
2. **Reflex conditions read only local frontmatter.** If evaluating a condition requires
   knowledge of the whole, it is not a reflex — move it under Escalation. This is the line
   that keeps the cord and the crown from collapsing into each other.
   *Two classes of reflex, each local to its own organ:* the **artifact-promotion reflexes**
   (`../spinal_cord/transitions/`) read a **vertebra's** frontmatter and are untouched by the
   afferent-sensory stream; the **sensory-triage reflex** (`afferent-sensory/triage.md`) reads
   the **feedback item's** own frontmatter (`raw`, `entered_at`, `gate`) plus the active
   segment. Both are "local" — each to its own surface — and neither reads the whole column.
   The triage is therefore a *separate organ*, not a violation: the risky judgments (send-back,
   tweak-vs-amendment, new-want-vs-amendment) are explicitly pushed to Escalation, never claimed
   as reflex.
3. **Direction stays pure.** Afferent transitions only promote; efferent transitions only
   send back. A handoff that does both is two transitions.
4. **No vertebra is skipped.** Transitions connect adjacent levels (the efferent send-backs
   may target any level, but repaired work re-ascends one vertebra at a time). A shortcut that
   skips a level breaks the load-bearing premise of the whole paradigm.
5. **Correction never becomes reflexive.** Send-backs assert a fault relative to the whole;
   they must remain crown-originated. Never grant a level the reflex right to send work back.
   *For human feedback:* corrective feedback that says "this drifted from the want" is a
   correction, and the dorsal horn may *recognize* it but must **route it to the crown**, which
   emits the send-back — the dorsal horn grows no private right to return work. Human-originated
   corrective feedback is consistent with this invariant because the human sits at the oversight
   position: it is the crown (its human oversight) speaking, not a lower level reflexively
   returning its own work.

## The movable oversight line

The afferent-sensory stream changed *who must approve what*, so the crown's standing line
between autonomy and human oversight is recorded here. The principle: **the crown's reach is
total, but its default posture is rest** — the same stillness the cord keeps.

- **Autonomy is the default posture.** The column advances **reflex promotions**, **reflex
  tweaks**, **wave amendments**, and the crown's *emission* of **send-backs** on its own. No
  approval is sought for what is, by definition, automatic. Escalations that need judgment but
  not a *person* are resolved by the crown's judgment subagent (execution-topology tier 2)
  autonomously.

- **The human is gated at two edges only** — the two things only a human should own. Both are
  *existing* escalations, now named as standing **human-gates**:
  - **(a) Verifying finished work** — `../spinal_cord/transitions/3-thoracic-to-4-cervical.md`.
    The human confirms the built thing is sound. Verification is theirs.
  - **(b) Admitting new desire** — `../spinal_cord/transitions/0-coccygeal-to-1-sacral.md`
    ("does this belong in the telos?"). New *want* needs human assent; new *mechanism for an
    existing want* does not. The four-lane triage's **new-seed lane feeds exactly here** — the
    edge-gate and the no-fast-track rule are the same wall seen from two sides.

- **The line is movable, never fixed-and-removed.** A human-gate may be inserted at **any**
  point on demand, turning an otherwise-autonomous step into one that waits for human assent.
  It is carried by a single reflex-legible field so the line can move without rewriting itself:

  ```yaml
  gate: none        # none | human   (default none = autonomous)
  gate_reason: "<why a human was inserted here>"
  ```

  This field lives on a `kind: feedback` item **and on a thoracic wave or plan**
  (`../thoracic_infolding/_template.md` frontmatter, or an inline `(gate: human — why)`
  on a wave heading) — same field, same reflex-legibility, whichever unit of work carries it.

  Three triggers may raise it: **the human directly** (mark a plan/wave/item, or the next-N
  items, as gated); **a flagged feedback item** (`gate: human` set at intake from the human's
  words — forces dispatch to pause regardless of lane, even a reflex tweak); or **the triage
  itself** (when uncertainty shouldn't be silently resolved even by the judgment subagent —
  high blast-radius amendment, or genuine new-want/amendment ambiguity). When the gate is set,
  the system **does not act**: it surfaces the intended action + reason and waits for assent,
  then proceeds or re-routes per the human's correction. The gate is *transient and local* — it
  raises a checkpoint without rewriting the standing line; when cleared, the autonomous default
  resumes. The line moved; it was not removed. See
  [`execution-topology.md`](./execution-topology.md): a raised gate routes to a *person* instead
  of the judgment subagent — the explicit human checkpoint atop tier 2.

## How to change a transition — the procedure

1. **Record it as a cervical artifact.** A cord change is an oversight/guideline document
   here in `cervical_awareness/`, answerable down the column like any other — it must name the
   desire-level purpose it ultimately serves.
2. **Check the neighbors.** A transition shares frontmatter and status vocabularies with the
   levels it joins. Changing it can desync the transitions above and below; review both, and
   any template whose frontmatter it reads.
3. **Prefer the smallest reflex.** When in doubt, leave judgment with the crown. It is cheaper
   to relax a reflex later than to recover from one that promoted the wrong thing.
4. **Re-sync the templates if needed.** If a change requires a new local field to keep a
   condition reflex-evaluable, add that field to the relevant vertebra's `_template.md` and
   note it in [`template-guide.md`](./template-guide.md).

## The standing question

Whenever the crown reviews the cord, it asks one thing: *can the column still be read as an
unbroken chain of frontmatter — seed → want → bones → wave → awareness — with every promotion
reflex-evaluable and every correction crown-judged?* If yes, the architecture is coherent and
the cord should be left alone. If no, the change above is what restores it.

The afferent-sensory stream answers this question intact: feedback items carry their own
`kind / lane / status / gate` chain, the append-only triage log records every sort, and
corrections still originate at the crown. The stream *restores* coherence the want exposed
(the column had no organ to feel the world, and no record of how it answered) rather than
breaking it.
