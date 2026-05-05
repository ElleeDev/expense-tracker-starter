# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install       # install dependencies
npm run dev       # start dev server at http://localhost:5173
npm run build     # production build
npm run preview   # preview production build
npm run lint      # run ESLint
```

No test framework is configured.

## Architecture

This is a single-component React app (Vite + React 19). All logic lives in `src/App.jsx` — there is no routing, no context, no separate components, and no backend. State is in-memory only (no localStorage, no API).

**Known bugs and intentional issues** (this is a course starter project — do not "fix" these unless instructed):
- `amount` is stored as a string, so `totalIncome` and `totalExpenses` use string concatenation instead of numeric addition
- Transaction id 4 ("Freelance Work") is typed as `"expense"` but categorized as `"salary"` — inconsistent data
- The summary cards display raw concatenated strings rather than correct dollar totals
