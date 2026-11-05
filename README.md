# Todo

A single-file Todo app: vanilla HTML, inline CSS, inline JS. No frameworks, no
dependencies, no build step, no CDN. Todos persist in `localStorage` under the
key `todo.v1.todos`.

## Run

Open `index.html` in a browser. That's it.

## Features

- Add a todo (Enter or the **Add** button — one code path)
- List todos in insertion order
- Toggle complete / incomplete
- Delete a todo
- Filter: All / Active / Completed (view-only, not persisted)
- Persistence across reloads via `localStorage`
- Accessible: labelled input, checkbox label = title, `aria-label` on delete,
  `aria-pressed` on filters, `aria-live="polite"` status line

## Files

- `index.html` — the entire app (HTML + CSS + JS)
- `README.md` — this file

## Notes

Storage access is defensive: absent, empty, corrupt, or blocked storage (e.g.
`file://` restrictions) degrades to an empty list instead of throwing, and a
failed write shows an inline notice rather than an error. Nothing else in this
repository is referenced by the app.
