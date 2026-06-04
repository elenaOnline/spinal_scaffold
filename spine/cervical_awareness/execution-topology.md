---
stage: cervical        # 4 · awareness
kind: guideline
watches: the whole column — how work is executed across it
---

# Execution Topology — what runs where, and what spawns what

The column says *where artifacts settle* and the cord says *how they move*. This document
says **who does the moving** — how the work maps onto agents. The principle is one line:

> **Agent topology follows the cord's own reflex/mediated split. Never apply one execution
> model uniformly across handoffs.**

Spinning up cognition should be proportional to the judgment a step actually requires. A
reflex requires none; a mediation requires sight of the whole; a wave requires many hands.
Each gets a different mechanism.

## The three tiers

### Reflex writes — inline, deterministic, no model
The status-write *is* the reflex: flip a frontmatter field, wire a link. There is no residual
work to offload, and the conditions are evaluable from local frontmatter alone.

- **Mechanism:** the main agent performs it inline, or — preferably — a deterministic
  hook/script does, with no model in the loop at all.
- **Do not spawn a subagent.** A subagent starts cold and would re-derive the whole paradigm
  to flip one field — a separate brain servicing a reflex, which contradicts the very
  anatomy that justifies separating the cord from the crown. A reflex arc never routes
  through the brain.
- **Applies to:** the afferent on-promotion status changes in every
  [`../spinal_cord/transitions/`](../spinal_cord/transitions/) spec; and **afferent-sensory
  intake** — capturing feedback verbatim into `raw` and splitting a mixed suite into one item
  per concern ([`../spinal_cord/afferent-sensory/intake.md`](../spinal_cord/afferent-sensory/intake.md)).
  Entry reads only the human's text and the active plan's `status`, so it is a reflex write:
  inline, no model. The risky judgment lives one step downstream, in triage classification.

### Mediated escalations — a judgment subagent
When a transition escalates (a new want against the telos, a cross-cutting structural choice,
a re-choreographing of a plan's waves, any oversight finding), the work is real: it fans out
across many artifacts and needs whole-system judgment.

- **Mechanism:** spawn one subagent to perform the judgment. Its intermediate reasoning would
  pollute the main context; it returns a clean verdict (promote / hold / send back, with reason).
- **Why offload:** this is exactly the work you want *off* the main thread — and the natural
  subagent boundary. The crown thinks; the main agent stays on the transition.
- **Applies to:** every *Escalation* clause in the transition specs, and the emission of
  [efferent send-backs](../spinal_cord/transitions/efferent-send-backs.md); and **mediated
  feedback triage** — classifying an item when the lane needs sight of the whole (any
  send-back confirmation, tweak-vs-amendment by blast radius, new-want-vs-amendment ambiguity).
  The subagent returns a clean verdict: lane + reason. **Reflex** classification toward the
  *safe* lanes (an obviously-local tweak; the new-seed deferral) stays in tier 1, inline. The
  asymmetry is the safety mechanism: speed is taken only where it cannot destabilize a live
  wave; everything that *accelerates* change escalates. See
  [`../spinal_cord/afferent-sensory/triage.md`](../spinal_cord/afferent-sensory/triage.md).

### Thoracic waves — parallel build subagents
`thoracic_infolding/` promises *parallelized* wave-based implementation. A wave is a set of
items that do not block each other — the canonical fan-out.

- **Mechanism:** spawn one subagent per item within a wave, in parallel. Items within a wave
  are independent; waves remain sequenced.
- **Why offload:** parallelism is the wave's reason for existing. This is where many hands
  belong.
- **Applies to:** executing the items folded into a wave (the `building` → `built` span).

### The human-gate — atop tier 2, routing to a person

The one exception to "mediation → judgment subagent": when a `gate: human` is set — on a feedback
item, or on a **wave or plan** (`../thoracic_infolding/` frontmatter, or an inline `(gate: human)`
on a wave heading), by the human, a flagged feedback item, or the triage raising the movable line —
the mediated step routes to a **person** instead of a subagent. Before acting *within* a gated wave
or plan, the step waits for assent. The system does not act; it surfaces the intended
action + reason and waits for human assent, then proceeds or re-routes. This is the explicit
human checkpoint *atop* tier 2 — not a new tier, just the case where the verdict-giver is a
human. By default the human is gated only at the two **edges** (verifying finished work; admitting
new desire); the gate may be inserted anywhere else on demand. The mapping is otherwise
unchanged. See the *movable oversight line* in [`cord-stewardship.md`](./cord-stewardship.md).

## Reading the tiers together

| Step | Judgment required | Mechanism |
|------|-------------------|-----------|
| Reflex status-write · feedback intake | none (local frontmatter) | inline / hook · no model |
| Mediated escalation · feedback triage | whole-system | one judgment subagent |
| Raised human-gate (`gate: human`) | reserved-for-human | route to a person · assent then proceed |
| Wave execution | bounded, parallel | parallel build subagents |

The test for which tier a step belongs to is the same test the cord already uses: **can it be
decided from local frontmatter alone?** If yes, it is a reflex — keep it inline and cheap. If
it needs sight of the whole, it is a mediation — give it a subagent. If it is independent work
repeated across a wave, fan it out. Cognition spent should never exceed judgment required.

---
*Cross-referenced from [`../spinal_cord/README.md`](../spinal_cord/README.md). Changes to the
cord that alter what a handoff requires should be checked against this mapping —
see [`cord-stewardship.md`](./cord-stewardship.md).*
