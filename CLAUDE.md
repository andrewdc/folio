# CLAUDE.md — folio

Personal portfolio site for Andrew Colclough (UX Designer & Illustrator).
Live at [andrewdc.com](http://andrewdc.com). Deployed via Netlify.

## Stack

- **Astro 5** — static site framework, file-based routing
- **Tailwind CSS 3** — utility-first styling
- **TypeScript** — via Astro's built-in support
- **Netlify** — deployment adapter and hosting

## Commands

```bash
npm run dev      # dev server
npm run build    # type-check + build
npm run preview  # preview production build
```

## Project Layout

```
src/
  pages/          # Routes: index, /design/*, /illustration/*, /about/
  components/     # Reusable Astro components (see docs/components.md)
  layouts/        # BaseLayout.astro, LandingLayout.astro
  assets/         # Images: /draws/, /galleries/
  styles/         # global.css
public/           # Static root files
```

## Key Conventions

- Components are `.astro` files with scoped `<style>` blocks
- CSS custom properties for spacing (`--space`, `--space-xlg`) and fonts (`--font-head`)
- Tailwind used for layout and utilities; component-specific styles in scoped blocks
- No component library — everything is bespoke
- Each design case study lives in its own folder under `src/pages/design/`

## Extended Docs

- [docs/components.md](docs/components.md) — component inventory and usage
- [docs/pages.md](docs/pages.md) — page routes and structure
- [docs/conventions.md](docs/conventions.md) — styling, naming, and code conventions
- [docs/roadmap.md](docs/roadmap.md) — planned enhancements, new content, and clean-up
- [docs/memory.md](docs/memory.md) — open threads and session context

## Standards
See [CODING_STANDARDS.md](./CODING_STANDARDS.md) for code style and organization rules.
See [docs/patterns.md](./docs/patterns.md) for stack-specific patterns and ADRs.

## Session Workflow
- Mid-session: `/hotcap [tag] note` — logs decisions, patterns, failures, questions,
  and changes to `_session_hot.md` as they happen
- End of session: `/wrap` — routes hot file to /docs/, writes `_last_session.md`
- Cold start: load `CLAUDE.md` + `_last_session.md` only (~200 tokens total).
  Pull individual /docs/ files only when a task needs their history.
- Tags: `[D]` decision · `[P]` pattern · `[F]` failure · `[Q]` question · `[C]` change
- `_session_hot.md` is ephemeral — consumed and deleted by wrap
- `_last_session.md` is the rolling single-session anchor — always overwritten, never appended
- After completing work, run /hotcap to capture insights, then /wrap to route to decisions.md, architecture.md, and _last_session.md
- Delete the hot file after /wrap completes

## Docs Routing
- Before complex or structural tasks, check the Docs Index and read any
  relevant /docs/ files before proceeding
- Skip for simple edits, fixes, or tasks that need no project context
- This keeps token cost proportional to task complexity
