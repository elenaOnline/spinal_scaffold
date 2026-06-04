---
component: spinal_cord
kind: feedback
entered_at: <thoracic plan / wave id>     # the dermatome — which segment felt this
raw: "<the human's words, verbatim>"      # preserved forever; never paraphrased
lane: unclassified    # reflex-tweak | wave-amendment | send-back | new-seed | unclassified
status: received      # received | classified | dispatched | resolved
origin: human         # who sensed it (the human is the crown's oversight)
gate: none            # none | human  — an inserted human-gate
gate_reason: ""       # why a human was interposed here, if gated
routed_to: ""         # the artifact path the lane dispatched it to, once known
---

# feedback · <wave>-<nnn>

<!--
A single piece of exteroception: the column feeling the world's response to what it built.
Born at intake (../afferent-sensory/intake.md), one item per discrete concern, under the
active thoracic plan's feedback/. The cord carries it; the dorsal-horn triage sorts it.

Keep it minimal — identity is the frontmatter. `raw` is sacred: capture the human's exact
words, split a mixed suite into N items, and never paraphrase before the gate has judged.
Delete the body entirely if the frontmatter says enough.
-->

## Raw
<The verbatim feedback, if a longer transcription than the `raw` field comfortably holds.>

## Note
<Optional. Anything the triage or crown needs recorded alongside the verbatim text — never a
substitute for it.>

---
*Carried by `../afferent-sensory/`; sorted by its `triage.md`; governed by
`../../cervical_awareness/cord-stewardship.md`.*
