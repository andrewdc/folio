# Conventions

## Styling

- **Tailwind** for layout, spacing, and utilities
- **Scoped `<style>` blocks** inside `.astro` files for component-specific CSS
- **CSS custom properties** defined in `global.css`:
  - `--space`, `--space-xlg` — spacing scale
  - `--font-head` — heading font (Rokkitt)
  - Body font: Raleway (Google Fonts)
- No CSS preprocessor; plain CSS in scoped blocks

## Components

- All components are `.astro` files — no React/Vue/Svelte
- Props typed inline with TypeScript interfaces in the frontmatter
- No external component library; everything is bespoke
- Prefer composing existing components over adding complexity to one

## Images & Assets

- Project images in `src/assets/galleries/`
- Illustration assets in `src/assets/draws/`
- Import images in frontmatter and pass to `<Image>` or `<img>` tags

## Adding a New Case Study

1. Create `src/pages/design/<slug>/index.astro`
2. Use `BaseLayout.astro` as the layout
3. Compose from existing components (`Hero`, `Section`, `Challenge`, `ImageGrid`, etc.)
4. Add a `ProjectCard` entry to `src/pages/design/index.astro`

## Deployment

- `npm run build` runs `astro check && astro build` — fix type errors before merging
- Netlify deploys from `main` branch automatically
- No CI/CD pipeline beyond Netlify's built-in build
