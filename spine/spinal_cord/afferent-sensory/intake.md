---
component: spinal_cord
kind: transition
direction: afferent-sensory   # afferent (up) | efferent (down) | afferent-sensory (in)
from: world                   # outside the column
to: thoracic                  # the active segment (the breathing wave)
---

# world → active segment : feedback enters at the dermatome

<!--
The boundary crossing. Outside-the-column raw feedback becomes a typed signal the cord can
carry. Entry is deliberately a REFLEX: verbatim capture and splitting need no whole-system
knowledge, only the human's text and the active plan's status. All the risky judgment lives
one step downstream, in triage.md. This spec builds the channel, not the sort.
-->

## What moves
Raw human feedback (plain language, any quantity) on work-in-flight → one `kind: feedback`
artifact per discrete concern, created under the active thoracic plan. The human's exact words
are preserved; nothing is paraphrased before the gate has judged it.

The feedback item is born here, from the [`_feedback-item.md`](./_feedback-item.md) stencil.
Its home and shape:

```
thoracic_infolding/<plan>/feedback/<wave>-<nnn>.md
```

It lives under the active thoracic plan because feedback is sensation **at the active
segment** — it belongs to the wave that is breathing, not to a vertebra where artifacts
settle. It is cord traffic (`component: spinal_cord`), so it carries `kind`, not `stage`.
Frontmatter (load-bearing fields):

```yaml
component: spinal_cord
kind: feedback
entered_at: <thoracic plan / wave id>     # the dermatome — which segment felt this
raw: "more padding around the sacrum"     # the human's words, verbatim, preserved
lane: unclassified    # reflex-tweak | wave-amendment | send-back | new-seed | unclassified
status: received      # received | classified | dispatched | resolved
origin: human         # who sensed it (the human is the crown's oversight)
gate: none            # none | human  — an inserted human-gate (see cord-stewardship.md)
gate_reason: ""       # why a human was interposed here, if gated
routed_to: ""         # the artifact path the lane dispatched it to, once known
```

`raw` is preserved verbatim **forever**: the dorsal horn must not paraphrase the sensation
before the gate has judged it, or the record loses the ability to say *what the world actually
said*. `lane` starts `unclassified`; assigning it is triage's whole job. `gate: human` may be
set here from the human's own words (e.g. "check with me before you touch the sacrum"),
forcing the item's later dispatch to pause for human assent regardless of lane.

## Reflex conditions
Entry, not classification — these stay purely local, readable from the human's text and the
active plan's frontmatter alone:

- [ ] An active thoracic plan exists with `status: breathing` — there is a dermatome to
      receive at. (Feedback with no live wave has nowhere to enter; see Escalation.)
- [ ] The piece is recorded **verbatim** into `raw`, and split so **one item = one discrete
      concern** — a mixed suite of remarks becomes N items.

Splitting and verbatim-capture require *no whole-system knowledge*; they read only the human's
text and the plan's `status`. So **entry itself is a reflex** — cheap and fast, the reflex
speed the want asks for. The judgment that risks mis-triage lives entirely in the next step.

## On promotion
- Create the feedback item(s) under the active plan's `feedback/`.
- Set `status: received`, `lane: unclassified`, `entered_at` = the live wave, `origin: human`.
- If the human's words carry an explicit "ask me first," set `gate: human` with a
  `gate_reason`.
- Hand each item to the triage gate ([`triage.md`](./triage.md)).

## Escalation
If **no** wave is breathing, intake cannot place the sensation at a segment. It does not guess.
It escalates to the crown (oversight), which decides whether to open a segment, hold the
feedback, or treat it as a free-standing **new seed** at the base. This is the "no dermatome"
case — sensation arriving where the body is not currently in contact with the world.

---
*Governed by `../../cervical_awareness/cord-stewardship.md`.*
