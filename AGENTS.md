## Commands

- `npm run dev` — starts dev server (uses `--background` flag internally; see note below)
- `npm run build` — produces static site in `dist/`
- `npm run preview` — locally preview the production build
- `astro ...` — any Astro CLI command (e.g. `astro add`, `astro integrations`)

**Dev server note:** The `package.json` has `allowScripts: { esbuild: true }`. If you need to run custom esbuild commands, ensure this is preserved.

## Project structure

- `src/pages/` — page routes (Astro auto-routing)
- `src/components/` — reusable Astro/React/Vue/Svelte components
- `src/layouts/` — layout wrappers
- `src/assets/` — static images/SVGs (pixels OK)
- `package.json` — root config; `engines.node >= 22.12.0`
- `.agents/` — project skill index and lockfile; do not remove or rearrange without updating `skills-lock.json`
- `skills-lock.json` — locked skill versions; edit only with `npm ls` verification

## High-signal conventions

- Import images with `import X from '../assets/Y.svg'` — Astro treats them as assets
- Tailwind is not pre-configured; add your own build if needed
- `.agents/` and `skills-lock.json` manage project skills; changing one requires updating the other
