---
component: spinal_cord
kind: transition
direction: afferent      # afferent (up) | efferent (down) | afferent-sensory (in, external)
from: <stage>            # e.g. sacral
to: <stage>             # e.g. lumbar
---

# <from> → <to> : <one-line name of the handoff>

<!--
A transition spec. It defines how an artifact moves between two adjacent levels — when the
cord may move it on reflex, and when it must escalate to the crown. Reflex conditions must
be evaluable from LOCAL FRONTMATTER ALONE; anything needing whole-system knowledge belongs
under Escalation. Delete any section that doesn't want to exist.
-->

## What moves
<The artifact that travels, and the new artifact (if any) created on arrival.>

## Reflex conditions
<The local conditions — readable from frontmatter — that make this handoff mechanically
eligible with no crown involvement. List them as checks.>

## On promotion
<What the cord does when the reflex fires: links wired, statuses flipped, artifact created.>

## Escalation
<When this transition must instead route to the crown for judgment about the whole. Name
the trigger; the cord relays up, the crown rules, the ruling returns down the cord.>

---
*Governed by `../../cervical_awareness/cord-stewardship.md`.*
