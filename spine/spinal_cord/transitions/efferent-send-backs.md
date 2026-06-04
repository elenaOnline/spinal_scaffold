---
component: spinal_cord
kind: transition
direction: efferent
from: cervical
to: any            # thoracic | lumbar | sacral
---

# cervical → down : the efferent send-backs

<!--
The downward returns. Unlike the afferent transitions, these are NEVER reflexes: knowing
that something is wrong systemically requires sight of the whole, which only the crown has.
Every send-back originates at the crown and travels down the same cord.
-->

## What moves
An oversight finding from `cervical_awareness/` travels down the column to the level that
must repair the fault. The finding carries: the problem, the target level, a reason, and the
status change it imposes on arrival.

## The three returns
- **→ thoracic** — a flawed or incoherent **wave**. The plan resequences or refolds.
  Sets the affected thoracic plan `status: planned` (it must breathe again).
- **→ lumbar** — a missing or broken **bone**. The architecture is repaired or extended.
  Sets the affected lumbar write-up `status: draft`.
- **→ sacral** — an unmet or **drifted desire**: the realized form no longer serves the want.
  Reopens the desire. Sets the affected sacral spec `status: open`.

## On arrival
- The target artifact's status is flipped back as above.
- The send-back is recorded as a cervical artifact (`kind: oversight`) with its `watches:`
  field naming the target, so the return is traceable both ways along the cord.
- Repaired work then climbs again through the ordinary afferent transitions — **nothing
  skips a vertebra on the way back up**.

## Why never a reflex
A send-back asserts that something is wrong *relative to the whole*. That judgment cannot be
read from any single artifact's local frontmatter, so it can only originate at the crown.
This is the deliberate asymmetry of the cord: promotion can be reflexive; correction cannot.

---
*Governed by `../../cervical_awareness/cord-stewardship.md`.*
