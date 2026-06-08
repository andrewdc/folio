# Site Roadmap

_Categories are rough — priorities TBD as new project content comes together._

---

## Content

### New Projects (current job)
- [ ] Identify which new projects to document (need gathering + writing phase first)
- [ ] Define what information/artifacts are available per project
- [ ] Write case study drafts offline before building pages
- [ ] Add new project pages as content is ready

### Existing Projects — Candidates for Retirement
These older projects have limited available information and may be replaced by new work:
- `pds` — PowerSchool Design System (limited depth achievable)
- `pg` — Press Ganey Practice Performer (2011, limited artifacts)
- `nxsass` — Incomm Design System (very thin, little to expand)

Decision: retire gradually as new projects are ready to replace them, rather than investing in expanding stubs.

### Existing Projects — Keep & Maintain
- `aiux` — AI Navigation Assistant (strong, complete)
- `et-time-off` — ET Time-Off Feature (strong, complete)
- `et-signup` — ET Sign-up Refresh (solid, adequate)

### Impact & Metrics
- [ ] Add quantified outcomes to case studies where data exists (adoption, satisfaction scores, etc.)
- [ ] Uncomment/complete `<Stats>` and `<Metric>` blocks where real numbers can be supplied

---

## Presentation Format

_Invest here first — new projects can pilot the improved format._

- [ ] Audit and standardize case study structure across all pages (consistent use of `<Challenge>`, `<Section>`, `<Stats>`, etc.)
- [ ] Decide on the canonical case study template: what sections every study should have
- [ ] Improve image presentation (lightbox, captions, before/after comparisons?)
- [ ] Explore richer narrative sections (annotated screenshots, process callouts)
- [ ] Review typography and spacing consistency across case study pages

---

## Site Enhancements

- [ ] Contact/CTA flow — no form or clear next step beyond LinkedIn. Add real contact mechanism.
- [ ] Custom Open Graph image per page (currently using defaults)
- [ ] Fix footer placeholder content (`address`, `text` props in both layouts)
- [ ] Resolve commented-out `<Footer>` in `LandingLayout.astro`

---

## Clean-up

- [ ] Remove Python section from `docs/patterns.md` — not relevant to this Astro/TS/Tailwind stack
- [ ] Seed `docs/adr/` with ADR stubs for key decisions already made: Astro over other SSGs, Tailwind over plain CSS, no component library
- [ ] Remove `console.log('left:', left)` debug line in `MicroPaths.astro:4`
- [ ] Audit gallery image paths — verify all referenced images exist in `src/assets/galleries/`
- [ ] Remove or replace footer placeholder props across `BaseLayout.astro` and `LandingLayout.astro`

---

## Future / Nice-to-Have

- Writing or process notes section (blog-lite)
- Page transition animations
- Dark mode
- Case study filter/tag system on design index

---

## Planning Tasks (meta)

- [ ] **New project content planning** — for each new project: what's the story, what artifacts exist, what's the right format to present it
- [ ] **Case study template** — define the canonical structure before building new pages; pilot with first new project
