# Spinal Cord

> *Not a vertebra. The conduit threaded through all of them — the structure that carries
> signal up and down the column and mediates the reflexes between levels.*

The vertebrae (0–4) are *places where artifacts settle*. The **spinal cord** is the
*movement between them*. It does not have its own stage number because it is not a stage;
it runs through the whole column, orthogonal to the levels it connects.

Borrowing the neuroanatomy directly: the cord is distinct from the brain. The cervical
crown (`../cervical_awareness/`) **integrates and judges**; the cord **transports and
reflexes**. Conflating the two would make the brain mediate every signal — a bottleneck and
a category error. They are complementary organs.

## Three streams

The cord carries three streams, distinguished by direction *and* origin:

- **Afferent-promotion** — *up, internal*, toward the crown. A seed becoming a want, bones
  folding into a wave, completed work surfacing for oversight.
- **Efferent send-backs** — *down, internal*, away from the crown. The crown returning flawed
  work to the level that must repair it.
- **Afferent-sensory** — *in, external*. Feedback from the world entering at the **active
  segment** via the **dorsal horn** ([`afferent-sensory/`](./afferent-sensory/)). It is
  afferent in carriage (it travels up toward judgment) but distinguished by *origin*: it
  enters from outside rather than rising from a lower vertebra. It promotes nothing and sends
  nothing back by itself; it only delivers a sensation to the gate, which then dispatches it
  through one of the existing pure-direction paths. **Direction stays pure** — this is a third
  origin, not a third direction.

## Two modes of handoff

- **Reflex** — local and fast. A handoff between two adjacent levels whose conditions can be
  evaluated *entirely from local frontmatter*, with no knowledge of the whole. The cord
  performs these without consulting the crown — like a hand withdrawing from heat before the
  brain is involved.
- **Mediated** — relayed. When a transition needs judgment about the *whole* (should this be
  promoted at all? does it still serve the original desire? does it disturb the breathing of
  the entire plan?), the cord carries the signal **up to the crown**, the crown rules, and
  the ruling travels **back down** the same conduit.

The guiding rule: **prefer reflex; escalate only when whole-system judgment is genuinely
required.** If a condition cannot be evaluated from local frontmatter alone, it is not a
reflex — it is an escalation.

These two modes also decide *who does the work*. Reflex writes run inline (or as a
deterministic hook — no model); escalations spawn a judgment subagent; thoracic waves fan out
into parallel build subagents. Cognition spent should match judgment required — see
[`../cervical_awareness/execution-topology.md`](../cervical_awareness/execution-topology.md).

## What lives here

- [`transitions/`](./transitions/) — one spec per handoff:
  - [`0-coccygeal-to-1-sacral.md`](./transitions/0-coccygeal-to-1-sacral.md) — seed → want
  - [`1-sacral-to-2-lumbar.md`](./transitions/1-sacral-to-2-lumbar.md) — want → bones
  - [`2-lumbar-to-3-thoracic.md`](./transitions/2-lumbar-to-3-thoracic.md) — bones → wave
  - [`3-thoracic-to-4-cervical.md`](./transitions/3-thoracic-to-4-cervical.md) — work → oversight
  - [`efferent-send-backs.md`](./transitions/efferent-send-backs.md) — the downward returns
- [`afferent-sensory/`](./afferent-sensory/) — the dorsal horn: the third stream. External
  feedback enters at the active segment ([`intake.md`](./afferent-sensory/intake.md)) and is
  sorted by the four-lane triage ([`triage.md`](./afferent-sensory/triage.md)) into an
  existing dispatch path. Carries its own `kind: feedback` artifact
  ([`_feedback-item.md`](./afferent-sensory/_feedback-item.md)).
- [`_template.md`](./_template.md) — the shape of a transition spec.

## Governance

The cord's rules are themselves under the crown's oversight. **When and how to change a
transition** — to keep the architecture coherent as projects evolve — is defined in
[`../cervical_awareness/cord-stewardship.md`](../cervical_awareness/cord-stewardship.md).
