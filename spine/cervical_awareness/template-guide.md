---
stage: cervical        # 4 · awareness
kind: guideline
watches: the whole column
---

# Template Guide — the shape of each vertebra's artifacts

This document outlines the `_template.md` that lives in each folder of the column. It is
written from the crown, which is the only layer entitled to describe the whole spine.

## Principles

These templates are deliberately **light**. They exist to make an artifact *reasonably
identifiable as its stage* — no more. Spinal Development is used across many projects, so
the templates must not force structure where it doesn't want to be.

- **Two fixed parts, the rest optional.** Every template carries (a) a small frontmatter
  block that fixes its identity, and (b) one or two required prose sections that make the
  stage legible. Everything else is marked optional and should be deleted when it doesn't
  want to exist.
- **Frontmatter is the spine's nervous system.** `stage` names the vertebra; `status`
  tracks where the artifact is in its life; link fields (`seed`, `serves`, `watches`)
  record the connections up and down the column. Keep these even when prose is sparse.
- **Copy `_template.md`, don't edit it.** The underscore sorts it to the top and marks it
  as a stencil, not an artifact.
- **Movement is upward by default.** Each template ends with a footer naming where the
  artifact promotes to. Only the cervical layer sends work back down.

## The five templates

### 0 · `coccygeal_differentiation/_template.md` — the seed
- **Identity:** `stage: coccygeal`, `status: seed | promoted | dropped`.
- **Required:** *The spark* — the idea in a sentence or two.
- **Optional:** *Why it surfaced*, *Notes*.
- **Made identifiable by:** looseness. It captures, it does not commit.

### 1 · `sacral_unconscious/_template.md` — the desire
- **Identity:** `stage: sacral`, `status: open | architected | satisfied | abandoned`,
  `seed:` (link down to the originating seed).
- **Required:** *The want* and *Why*.
- **Optional:** *What satisfaction looks like*, *Tensions*.
- **Made identifiable by:** speaking in wants and reasons — never mechanism.

### 2 · `lumbar_architecture/_template.md` — the bones
- **Identity:** `stage: lumbar`, `status: draft | sound | building | built`, `serves:`
  (link down to the desire it gives structure to).
- **Required:** *What it is* and *How it's built*.
- **Optional:** *Decisions & trade-offs*, *Open questions*.
- **Made identifiable by:** prescribing *how*, with as much rigor as the thing needs.

### 3 · `thoracic_infolding/_template.md` — the waves
- **Identity:** `stage: thoracic`, `status: planned | breathing | complete`.
- **Required:** *Scope* and at least one *Wave* of items (each linked to its lumbar write-up).
- **Optional:** *Dependencies*, *Coordination notes*.
- **Made identifiable by:** items grouped into parallel waves, waves sequenced in order.

### 4 · `cervical_awareness/_template.md` — the awareness
- **Identity:** `stage: cervical`, `kind: guideline | procedure | documentation | oversight`,
  `watches:` (what part of the spine it concerns).
- **Required:** *Purpose* and *Body*.
- **Optional:** *Sends back down* — where a fault returns work along the column.
- **Made identifiable by:** governing or recording, and its right to see the whole spine.

## Beyond the vertebrae — the cord's artifacts

The cord carries its own artifacts, governed alongside the vertebra templates:

- **Transition specs** (`spinal_cord/**/_template.md`) — `component: spinal_cord`,
  `kind: transition`, and a `direction` of `afferent` | `efferent` | `afferent-sensory`. Each
  defines how a handoff fires (reflex) and when it escalates (mediated).
- **Feedback items** (`spinal_cord/afferent-sensory/_feedback-item.md`) — `component: spinal_cord`,
  `kind: feedback`. The dorsal horn's record of a single piece of sensed feedback: the human's
  words kept verbatim (`raw`), where it entered (`entered_at`), and whether a human-gate is raised
  (`gate`). Sorted by the four-lane triage into one of the existing dispatch paths.

## Reading the column through its frontmatter

Because every artifact declares its `stage`, `status`, and links, the whole project can be
read as a single chain of frontmatter: a seed that became a want that grew bones that folded
into a wave that is now watched over. When that chain is unbroken, the column bears load.
When a link is missing, that is where to look first.
