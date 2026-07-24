# Crave Kangen — React App (shadcn + Tailwind + TypeScript)

This app exists because the `animated-hero` component depends on a
**shadcn / Tailwind / TypeScript** project, and this repo had none. Rather than
give bare instructions, the project was scaffolded here and the component
integrated and themed for Crave Kangen.

## Stack

- **Vite + React 18 + TypeScript** (strict)
- **Tailwind CSS v3** with the shadcn design-token setup (CSS variables in
  `src/index.css`, mapped in `tailwind.config.js`)
- shadcn structure: `@/*` path alias → `src/`, primitives in
  `src/components/ui/`, `cn()` in `src/lib/utils.ts`, `components.json` present

## Run it

```bash
cd sites/crave-kangen-app
npm install
npm run dev       # http://localhost:5173
npm run build     # type-check + production build to dist/
npm run preview   # serve the built dist/ over HTTP
```

> Open the build over **HTTP** (`npm run preview`), not by double-clicking
> `dist/index.html` — browsers block ES-module scripts loaded from `file://`.

## What was integrated

| File | Role |
|------|------|
| `src/components/ui/button.tsx` | shadcn Button (pasted as provided) |
| `src/components/ui/animated-hero.tsx` | the `animated-hero` component |
| `src/components/ui/hero-demo.tsx` | the `demo.tsx` usage example |
| `src/App.tsx` | renders `<HeroDemo />` |

**Component notes (answers to the integration questions):**
- **Props/state:** `Hero` takes no props. It holds one piece of state
  (`titleNumber`) and cycles a `titles` array every 2s with a `setTimeout` —
  animated by Framer Motion. No providers or context required.
- **Theming:** kept the component's structure and animation identical; only the
  copy, rotating words (`hydrogen-rich / alkaline / ionized / fresh / alive`),
  and CTAs were themed for Crave Kangen. The component's `text-spektr-cyan-50`
  class is defined as a brand color in `tailwind.config.js` so it renders.
- **CTAs:** wired via `asChild` to anchor links (`#classes`, `#reserve`,
  `#story`) so they can point at the storefront site's sections.
- **Assets:** none required — the hero is type-only (no images). Icons come from
  `lucide-react` (`MoveRight`, `CalendarCheck`).
- **Responsive:** centered flex column; title scales `text-5xl → md:text-7xl`;
  verified at 390px and 1440px.

## Dependencies installed

Runtime: `lucide-react`, `framer-motion`, `@radix-ui/react-slot`,
`class-variance-authority`, `clsx`, `tailwind-merge`, `tailwindcss-animate`.
Dev: `vite`, `@vitejs/plugin-react`, `typescript`, `tailwindcss`, `postcss`,
`autoprefixer`, `@types/*`.

## Setting this up from scratch (shadcn CLI route)

If you'd rather regenerate the scaffold with the official tooling:

```bash
# 1. Create a Vite React + TS app
npm create vite@latest crave-kangen-app -- --template react-ts && cd crave-kangen-app

# 2. Tailwind
npm install -D tailwindcss@3 postcss autoprefixer
npx tailwindcss init -p

# 3. Add the @ alias in tsconfig.json + vite.config.ts (see this repo's copies)

# 4. Init shadcn (creates components.json, lib/utils, CSS variables)
npx shadcn@latest init

# 5. Add the button primitive, then drop in animated-hero.tsx
npx shadcn@latest add button
npm install framer-motion lucide-react
```

The `/components/ui` folder + `@/` alias are load-bearing: the component imports
`@/components/ui/button` and `@/lib/utils`. If the folder or alias differ, those
imports fail to resolve — which is why shadcn standardizes on exactly this path.
