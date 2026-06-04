# .human — the dashboard

A window for the human, not part of the column. `spinal_column.html` is a standalone,
browser-openable dashboard (no build step) that visualizes the spine and shows what is currently
settled in each stage.

## How it works
- Open `spinal_column.html` directly in a browser.
- Click a vertebra → the right panel shows that stage's name, role, and how ascent/descent are
  handled; cards below list the items currently in that stage.

## The sync contract
The single source of truth is the **`STAGES` object** near the top of the `<script>` block. When an
artifact settles in a stage or the cord moves it, update that stage's `items` array
(`{ title, desc, status }`); the counts, badges, and cards all derive from it automatically.

This is a view only — it has no bearing on what the paradigm can build. A fresh project keeps the
dashboard shell and resets every stage's `items` to empty.
