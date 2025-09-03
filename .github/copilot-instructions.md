## Purpose
Provide concise, actionable guidance for AI coding agents working on this Vue 2 (Vue CLI) single-page app so they can be productive immediately.

## Big picture (what this repo is)
- SPA built with Vue 2.6 + Vue CLI (see `package.json`).
- Entry: `src/main.js` — it mounts the root `App.vue` and imports `src/assets/styles/main.scss`.
- `src/App.vue` composes the page from many single-file components under `src/components/` (e.g. `HeroSection.vue`, `PostPilotSection.vue`).
- No router or global state library present (no `vue-router` / `vuex` in dependencies). Components communicate by props/events.

## How to run, build, lint (developer workflows)
- Install: `npm install` (uses npm lock not present in repo snapshot).
- Dev server (HMR): `npm run serve` — opens local dev server (Vue CLI default, usually localhost:8080).
- Production build: `npm run build` -> `dist/`.
- Linting: `npm run lint` (uses `@babel/eslint-parser` + `eslint-plugin-vue`).

Example (PowerShell):
```
npm install
npm run serve
```

## Conventions & patterns to follow (project-specific)
- Components: PascalCase filenames under `src/components/` and registered in parent components (see `src/App.vue`).
- Styling: Global SASS at `src/assets/styles/main.scss` is imported once in `src/main.js`. Prefer component-scoped <style lang="scss"> for local styles, and import global variables/mixins from the global stylesheet when needed.
- Assets: images live in `src/assets/`. Use relative imports or the `@/assets/...` alias (standard Vue CLI alias to `src`) when adding images or imports.
- No centralized store: prefer prop drilling and `$emit` for parent-child communication. Search for `props`/`$emit` in components to see established patterns.

## Integrations & external deps
- `swiper` is listed in `package.json` — search `src/components` for where it's used (likely in carousels/sliders).
- Build is driven by `@vue/cli-service` (scripts in `package.json`) and uses `vue-template-compiler` matching Vue version.

## What to look for when changing behavior
- Check `src/App.vue` to see where new sections should be mounted.
- If adding global styles, update `src/assets/styles/main.scss` import in `src/main.js` (one import only).
- When adding images, prefer `@/assets/<name>`; when importing into JS (e.g., inside script), use `import img from '@/assets/logo.png'` so webpack processes it.

## Quick examples
- Add a new component and register it in the app:

1. Create `src/components/MySection.vue` (SFC).
2. In `src/App.vue` import and add to `components` block, then place `<MySection/>` in the template where needed.

## Tests / lint / CI
- There are no unit tests in the repo by default. The repo does include ESLint config in `package.json`; use `npm run lint` to surface JS/Vue issues.

## Searchable anchors for deeper context
- Start with these files: `package.json`, `src/main.js`, `src/App.vue`, `src/components/*`, `src/assets/styles/main.scss`, `public/index.html`.

## When you can't find intent
- Prefer the existing page composition in `src/App.vue` rather than introducing new routing or global state. If a feature requires shared state, note the change and propose adding `vuex` or a minimal event bus.

---
If anything here is unclear or you want more examples (component tests, a sample component PR, or how `swiper` is used in this project), tell me which area to expand.
