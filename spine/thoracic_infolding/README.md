# 3 · Thoracic Infolding

> *The ribbed cage. The breath. The rhythmic wave of motion.*

The thoracic spine articulates with the ribs — the body's apparatus of breath and rhythm.
Here, architecture is folded into **a plan for parallelized, wave-based implementation**.
"Infolding" is the gathering of independent structural pieces into coordinated waves that
can expand and contract together, like the breathing of the ribcage.

## What lives here

- Wave plans: batches of work that can proceed in parallel within a wave
- Dependency ordering between waves (which breath must precede which)
- Assignment of architectural items to waves
- Coordination notes for parallel streams of implementation

## How to work here

- A **wave** is a set of items that can be built concurrently because they don't block one
  another. Waves are sequenced; items within a wave are not.
- Draw each wave's items from the [`../lumbar_architecture/`](../lumbar_architecture/)
  write-ups. If an item isn't architected yet, it isn't ready to fold into a wave.
- Keep waves small enough to breathe — prefer more, tighter waves over few heavy ones.
- Hand executed and verified work upward to [`../cervical_awareness/`](../cervical_awareness/)
  for documentation and oversight.
- The breathing wave is the column's **active segment** — the level in contact with the world. In-flight
  feedback enters here through the cord's afferent-sensory stream
  ([`../spinal_cord/afferent-sensory/`](../spinal_cord/afferent-sensory/)) and may, once triaged, be
  folded in as a **wave amendment**.
- A wave or a whole plan can carry a **human-gate** to pause that span for human assent — `gate: human`
  in the plan frontmatter, or an inline `(gate: human — why)` on a wave heading.

This is the layer of motion. Everything below is still; everything here moves in waves.
