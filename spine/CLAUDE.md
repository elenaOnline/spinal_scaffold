# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

This is **not a software project** — it is the foundation for *how projects are developed*: a
reusable methodology called **Spinal Development**, modeled on the human spine (after the book
*Spinal Catastrophism*). The base roots in the grounded past (earth); the cervical crown reaches
a zenith (sky). Work *ascends* the column. There is no build, lint, or test toolchain. The repo
is Markdown documents plus one standalone HTML dashboard.

Read [`README.md`](./README.md) first — it is the canonical overview. This file covers only what
isn't obvious from reading the folder READMEs in order.

## The column (base → crown)

Five numbered vertebra-folders; work flows **upward** through them:

| # | Folder | Holds |
|---|--------|-------|
| 0 | `coccygeal_differentiation/` | ideation, seeds for future updates |
| 1 | `sacral_unconscious/` | desire-oriented specs (what is wanted + why, never how) |
| 2 | `lumbar_architecture/` | technical write-ups (the "how", load-bearing) |
| 3 | `thoracic_infolding/` | parallel, wave-based implementation plans |
| 4 | `cervical_awareness/` | guidelines, procedures, documentation, oversight |

Threaded through all of them (and numbered as none) is `spinal_cord/` — the **movement between**
vertebrae, not a stage itself.

## How artifacts work

- Each vertebra folder has a `README.md` (how to work there) and a `_template.md`. **Copy
  `_template.md` to make a new artifact; never edit the template itself.** The leading underscore
  marks it as a stencil.
- Every artifact carries small YAML frontmatter fixing its identity: `stage`, a stage-specific
  `status`, and link fields (`seed`, `serves`, `watches`) that wire it up/down the column. The
  whole project is meant to be readable as one unbroken chain of frontmatter: seed → want → bones
  → wave → awareness. A missing link is the first place to look when something is wrong.
- The master description of every template is `cervical_awareness/template-guide.md`.

## How work moves (the cord)

`spinal_cord/transitions/` holds one spec per handoff (`0-coccygeal-to-1-sacral.md` … plus
`efferent-send-backs.md`). The cord carries **three streams**: afferent-promotion (up, internal),
efferent send-backs (down, internal), and **afferent-sensory** (in, external) — the dorsal horn
in `spinal_cord/afferent-sensory/`, where human feedback on work-in-flight enters at the active
segment (`intake.md`, a reflex) and is sorted by a four-lane triage (`triage.md`) into an
existing dispatch path. Things to internalize:

- **Direction:** *afferent* = upward (promotion), *efferent* = downward (send-back, crown-only).
  *afferent-sensory* is a third **origin**, not a third direction — external feedback carried up
  to the gate, which dispatches it through the existing pure-direction paths. Direction stays pure.
- **Mode:** *reflex* = decidable from local frontmatter alone, done with no crown involvement;
  *mediated* = needs whole-system judgment, so it is relayed to the cervical crown to rule. Prefer
  reflex; escalate only when judgment of the whole is genuinely required. **Correction (send-backs)
  is never reflexive** — it always originates at the crown.
- Transitions are **active**: performing a promotion writes the status changes back into the
  artifacts' frontmatter (e.g. promoting 1→2 sets the sacral spec to `architected`). Nothing skips
  a vertebra, including on the way back up after a send-back.

**Oversight is autonomy-by-default with a movable human-gate.** The column advances reflexes,
tweaks, amendments, and send-back *emission* on its own; a human is gated only at two **edges**
(verifying finished work; admitting new desire), and a `gate: human` flag may be inserted anywhere
on demand to pause a step for human assent. The crown's reach is total; its default posture is rest.

Governance of the cord itself (when/how to change a transition, the coherence invariants, and the
movable oversight line) lives in `cervical_awareness/cord-stewardship.md`. Default posture toward
the cord is **stillness** — most work should never change it.

## Execution topology (which work spawns subagents)

Defined in `cervical_awareness/execution-topology.md`. Agent/compute use follows the cord's
reflex/mediated split — never uniform:

- **Reflex status-writes** → inline (or a deterministic hook). **Do not spawn a subagent** to flip
  a frontmatter field; a cold subagent re-deriving the paradigm for a one-line edit contradicts the
  reflex principle.
- **Mediated escalations + efferent send-backs** → spawn **one** judgment subagent (whole-system
  reasoning, kept off the main thread; returns a verdict).
- **Thoracic wave execution** → spawn **parallel** build subagents, one per independent item in a wave.

## The dashboard — keep it in sync

`.human/spinal_column.html` is a standalone, browser-openable dashboard (open it directly; no build).
It visualizes the column and lists the items currently in each stage.

**Its single source of truth is the `STAGES` object near the top of the `<script>` block.** When an
artifact settles in a stage or the cord moves it, update that stage's `items` array
(`{ title, desc, status }`); counts, badges, and cards derive from it automatically. The dashboard is
a window only — it has no bearing on what the paradigm can build.

## Working conventions

- Match the established voice: anatomical/`Spinal Catastrophism` metaphor fused with precise
  operational rules. Each doc grounds its metaphor, states what lives there, and defines movement.
- Templates and transitions are deliberately **light** — add identity and the minimum that makes a
  stage legible; mark everything else optional. Do not force structure where it doesn't want to be.
- When you add or move an artifact, also: write the frontmatter status change, wire its link fields,
  and update the dashboard `STAGES` data.
