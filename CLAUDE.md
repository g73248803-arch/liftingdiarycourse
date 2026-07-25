# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Important: non-standard Next.js version

This project uses Next.js 16.2.11, which has breaking changes relative to older/training-data Next.js. **Before writing any Next.js code (routing, config, data fetching, etc.), read the relevant docs in `node_modules/next/dist/docs/`** (organized into `01-app`, `02-pages`, `03-architecture`, `04-community`). Heed deprecation notices found there.

## Commands

- `npm run dev` — start the dev server (http://localhost:3000)
- `npm run build` — production build
- `npm run start` — run the production build
- `npm run lint` — run ESLint (flat config via `eslint.config.mjs`, extends `eslint-config-next` core-web-vitals + typescript rules)

There is no test setup in this repository yet.

## Architecture

- App Router project (`src/app/`), TypeScript, React 19.
- Path alias `@/*` maps to `src/*` (see `tsconfig.json`).
- Styling via Tailwind CSS v4 (`@tailwindcss/postcss`), global styles in `src/app/globals.css`.
- Currently just the scaffolded `create-next-app` starter (`layout.tsx`, `page.tsx`) — no custom routes, data layer, or components have been built yet.
