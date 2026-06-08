# Pages & Routes

All pages use file-based routing via Astro under `src/pages/`.

## Top-Level Routes

| Route | File | Description |
|-------|------|-------------|
| `/` | `index.astro` | Landing page |
| `/design/` | `design/index.astro` | Design portfolio index |
| `/illustration/` | `illustration/` | Illustration gallery |
| `/about/` | `about/` | About page |

## Design Case Studies (`/design/*`)

Each case study lives in its own subfolder with an `index.astro`:

| Route | Project |
|-------|---------|
| `/design/aiux/` | AI UX project |
| `/design/et-time-off/` | ET time-off feature |
| `/design/et-signup/` | ET signup flow |
| `/design/nxsass/` | NxSass project |
| `/design/pds/` | PDS project |
| `/design/pg/` | PG project |

## Layouts

- `BaseLayout.astro` — used by all interior pages; includes Nav, Footer, metadata, Google Analytics
- `LandingLayout.astro` — used by the home page; minimal chrome
