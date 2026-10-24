# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

Arcade Vault: platform to play games online and compete for points. Next.js 16.4.2, React 19, TypeScript (strict), Tailwind v4, npm.

## Skills

Usa siempre /frontend-design para diseñar la interfaz del usuario.

## Next.js

@AGENTS.md

This Next.js version has breaking changes. Read the relevant guide in `node_modules/next/dist/docs/` before writing code.

`next.config.ts` enables non-standard options: `cacheComponents`, `partialPrefetching`, `experimental.agentFeedback`. Check the docs before assuming standard caching/prefetch behavior.

## Commands

- `npm run dev` / `npm run build` / `npm run start`
- `npm run lint` (ESLint 9 flat config, `next/core-web-vitals` + `next/typescript`)
- No test, typecheck or format scripts exist.

## Conventions

- The `@/*` path alias maps to the repo root, not `src/`. Code lives in `app/`.
- Tailwind v4 is processed via `@tailwindcss/turbopack` (see `next.config.ts`), not PostCSS.
- README is in Spanish. The project follows Spec Driven Design using `/spec` and `/spec-impl` (install: `npx skills@latest add Klerith/fernando-skills`).
- Ignore `references/` (leftover prototype files); don't rely on or import from it.
