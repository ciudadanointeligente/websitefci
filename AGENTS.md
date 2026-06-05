# AGENTS.md

## Package manager

Use **pnpm**. Node >= 22.12.0.

Dependencies in use (all present in `node_modules`):

- `astro` ^6.4.4
- `@astrojs/alpinejs`
- `@astrojs/netlify`
- `@tailwindcss/vite`
- `tailwindcss` ^4
- `@types/alpinejs`

## Commands

```
./node_modules/.bin/astro dev      # http://localhost:4321
./node_modules/.bin/astro build    # outputs to dist/
./node_modules/.bin/astro preview
```

If `package.json` is restored:

```
pnpm dev
pnpm build
pnpm preview
```

## Stack

- **Astro 6** with strict TypeScript config
- **Tailwind CSS v4** — imported via `@tailwindcss/vite` plugin (not PostCSS). The global stylesheet at `src/styles/global.css` uses `@import "tailwindcss"`. Use Tailwind v4 syntax (no `tailwind.config.js`).
- **Alpine.js** — loaded via `@astrojs/alpinejs` integration, available globally in all `.astro` components.
- **Netlify adapter** — deploys to Netlify. Local dev emulates Netlify features (blobs, functions, edge functions, images, redirects) via `@netlify/vite-plugin`.

## Architecture

## No test/lint/typecheck configured

There are no test scripts, linters, or CI workflows configured yet.
