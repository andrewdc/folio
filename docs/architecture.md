# Architecture
- [ ] Component or system area

## 2026-06-08
- [C] Ran /apply-standards: added .claudeignore, docs/architecture.md, docs/decisions.md, Session Workflow + Docs Routing sections to CLAUDE.md, and session memory entries to .gitignore — CLAUDE.md has no ## Rules section (skipped)
- [C] All major deps upgraded to latest: astro 5→6, @astrojs/netlify 6→7, tailwindcss 3→4, typescript 5→6 — build clean
- [C] Tailwind v4 integration: replaced @astrojs/tailwind with @tailwindcss/vite plugin; astro.config.mjs now uses vite.plugins instead of integrations for Tailwind; global.css has @import "tailwindcss" at top; tailwind.config.mjs deleted
- [C] Details.astro: added `: string` type annotation to .map() callbacks — required by TS6 noImplicitAny
