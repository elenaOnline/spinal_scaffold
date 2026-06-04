# Afferent-Sensory — the dorsal horn

> *Where the column feels the world. Sensation from outside enters the cord here, at the
> active segment, and is made into a signal the cord can carry and the crown can judge.*

The cord's two original streams both carry signals that originate **inside** the column:
*afferent-promotion* (an artifact rising one vertebra) and *efferent send-backs* (the crown
returning work downward). Neither can carry a signal that originates **outside** the column.
Human feedback on work-in-flight is exactly such a signal — the system sensing the world's
response to what it built. That is exteroception, and the cord had no organ for it.

This subtree is that organ: the **afferent-sensory stream**, the cord's **dorsal horn**.
Borrowing the neuroanatomy literally — the dorsal horn is where sensory afferents from the
periphery enter the cord, distinct from the ventral (motor/efferent) side. Feedback enters
here, at the **active segment** (the breathing thoracic wave), the way sensation arrives at
its dermatome: at the level currently in contact with the world, not at the base.

## A third origin, not a third direction

The stewardship invariant **direction stays pure** (afferent promotes, efferent sends back)
is preserved. Afferent-sensory is afferent in *carriage* — it travels *up* toward judgment —
but is distinguished by **origin**: it enters from outside rather than rising from a lower
vertebra. It promotes nothing by itself and sends nothing back by itself; it only *delivers a
sensation to the gate*. What the gate then does — apply, fold, send back, set aside — flows
through the existing pure-direction transitions. The stream is the afferent *channel*; the
triage is the *grey matter* the channel feeds.

So the cord now carries **three streams**:

- **afferent-promotion** — *up, internal*: an artifact rising one vertebra (`transitions/`).
- **efferent send-backs** — *down, internal*: the crown returning flawed work
  (`transitions/efferent-send-backs.md`).
- **afferent-sensory** — *in, external*: feedback entering at the active segment via the
  dorsal horn (this subtree), then handed to the gate.

## What lives here

- [`intake.md`](./intake.md) — the dermatome entry: world → a `kind: feedback` item at the
  active segment. Entry is a **reflex** (verbatim capture + split); it escalates when there
  is no live segment to receive at.
- [`triage.md`](./triage.md) — the gate's grey matter: the four-lane sort
  (reflex-tweak · wave-amendment · send-back · new-seed) plus the append-only
  classify-and-log. A *separate* reflex/mediated organ whose local surface is the feedback
  item's own frontmatter, not the whole column.
- [`_feedback-item.md`](./_feedback-item.md) — the stencil for a `kind: feedback` artifact:
  one per discrete piece of feedback, born at intake under the active thoracic plan's
  `feedback/`. (The two transition specs reuse [`../_template.md`](../_template.md) as-is for
  their own `kind: transition` shape.)

## Direction frontmatter

The two specs here carry `direction: afferent-sensory` — a third permitted token alongside
`afferent` and `efferent`, so the stream is legible in frontmatter at a glance and the purity
invariant stays checkable.

## Governance

Like the rest of the cord, this stream is under the crown's oversight. The crown's blessing of
the stream against the coherence invariants, and the **movable, always-insertable human-gate**
that governs its dispatch, live in
[`../../cervical_awareness/cord-stewardship.md`](../../cervical_awareness/cord-stewardship.md).
How its two steps map onto the compute tiers lives in
[`../../cervical_awareness/execution-topology.md`](../../cervical_awareness/execution-topology.md).
