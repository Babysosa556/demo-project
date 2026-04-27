# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Layout

This repo contains `expense-tracker-starter/` — a React + Vite expense tracker app used as a course starter project. The app intentionally ships with bugs and rough UI that are meant to be fixed as learning exercises.

Each subdirectory has its own `CLAUDE.md` with project-specific commands and architecture details. Start there when working inside a subdirectory.

## Tech Stack (expense-tracker-starter)

- **React 19** with JSX (not TypeScript)
- **Vite 7** — dev server, bundler
- **Plain CSS** in `src/App.css` — no CSS framework
- No test framework is configured

## Commands

Run from `expense-tracker-starter/`:

```bash
npm run dev      # Dev server at http://localhost:5173
npm run build    # Production build → dist/
npm run lint     # ESLint (JS/JSX only)
npm run preview  # Serve production build locally
```

## Code Conventions

- All source files are `.jsx` — do not introduce TypeScript unless the project explicitly migrates.
- Styling uses plain CSS class names in `App.css` — do not introduce Tailwind or CSS-in-JS.
- Keep components co-located in `src/` until the project grows enough to warrant subdirectories.
- `amount` values on transactions are stored as strings — always parse with `parseFloat()` before arithmetic.

## What to Avoid

- Do not add a test framework, routing library, or state manager without confirming it fits the course scope.
- Do not modify `vite.config.js` unless there is a clear build requirement.
