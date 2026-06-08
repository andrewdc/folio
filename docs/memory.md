# Session Memory

Open threads and context to carry into future sessions.

---

## 2026-04-10

### Standards scaffold added
`/apply-standards` was run for the first time. Created `CODING_STANDARDS.md` and `docs/patterns.md` from templates; added `## Standards` block to `CLAUDE.md`.

**Open threads:**
- `docs/patterns.md` contains a Python section that should be deleted — this project is Astro + TypeScript + Tailwind only. No Python anywhere.
- No ADRs exist yet. Candidates for `docs/adr/`:
  - Why Astro (vs Next.js / plain HTML)
  - Why Tailwind (vs plain CSS or CSS Modules)
  - Why no component library (bespoke only)
- These ADRs would be lightweight but useful context for future AI sessions on this project.
