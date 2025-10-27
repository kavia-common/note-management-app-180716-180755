# Ocean Notes (Astro)

A modern, responsive notes UI built with Astro. Create, view, edit, and manage notes with a polished Ocean Professional theme.

## Features

- Two-pane layout:
  - Sidebar with searchable notes list and New button
  - Main pane with title field and Markdown editor with live preview
- Create, edit, and delete notes (with confirmation)
- Local persistence via `localStorage` under key `app_notes_v1`
- Responsive:
  - Sidebar collapses under 768px, toggle via ☰ button
  - Preview toggle for small screens
- Ocean Professional theme (primary: `#2563EB`, secondary: `#F59E0B`) with subtle gradients, shadows, and rounded corners
- Optional light/dark theme toggle

## Getting started

From this folder:

```bash
npm install
npm run dev
```

The app will be available at http://localhost:3000 (configured in `astro.config.mjs`).

To build and preview:

```bash
npm run build
npm run preview
```

## Usage

- Click "+ New" in the sidebar to create a note.
- Select a note to edit. Edit the title in the top bar and the body in the editor.
- Click "Preview" to show/hide the rendered Markdown.
- Click the trash icon to delete the selected note (confirmation required).
- Notes auto-save and persist across reloads.

## Tech notes

- This app is frontend-only; no external APIs or environment variables are used.
- State is managed via a small custom store (`src/lib/store.ts`) with pub/sub and persisted in `localStorage`.
- Simple Markdown rendering is implemented in the editor (headings, bold, italic, inline code, links, bullet list). This avoids external dependencies.

## Project structure

```
src/
  components/
    Sidebar.astro
    Editor.astro
    ThemeToggle.astro
  layouts/
    Layout.astro
  lib/
    store.ts   # localStorage-backed notes store
  pages/
    index.astro
```

## License

MIT
