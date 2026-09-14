# Project routing and compatibility

Read this before installing a component. React Bits publishes the same free component in four source variants, so the project’s existing conventions—not a personal preference—decide which one to use.

## Detect the project profile

| Evidence in the repository | Choose | Notes |
| --- | --- | --- |
| `tsconfig.json`, `.ts`/`.tsx` source, or TypeScript configuration | `TS` | Prefer this even if a few legacy files are JS. |
| `.js`/`.jsx` application without TypeScript | `JS` | Do not add TypeScript for a single component. |
| `tailwindcss` dependency and Tailwind utility classes/configuration | `TW` | Match the repository's existing Tailwind version and conventions. |
| Global CSS, CSS Modules, Sass, or no Tailwind | `CSS` | Keep component CSS near the component or follow the project's pattern. |
| `next` dependency, especially the App Router | the matching variant plus client isolation if necessary | See SSR below. |
| `components.json` | shadcn CLI is usually the lowest-friction installer | It describes import aliases and target directories. |
| No `components.json` | use jsrepo or manual copy | Do not initialize shadcn merely for one component unless the user asks. |

The resulting matrix is `TS-TW`, `TS-CSS`, `JS-TW`, or `JS-CSS`.

## Framework-specific integration

### Next.js

The component source may use hooks or browser APIs even if its parent page is server-rendered. Put the React Bits component in a small file with `'use client'` at the top, and import that file from the server component. Avoid disabling SSR for an entire page when one visual is client-only.

For canvases, Three.js/WebGL, large image galleries, and pointer-driven effects, render a stable-size wrapper to prevent layout shift. Test production build/hydration, not just development mode.

### Vite, CRA-derived, or client-only React

Use the selected variant directly. Still ensure any component accessing browser globals only runs after mount when the project also runs tests or static rendering in Node.

### Remix, React Router, Astro islands, or another SSR-capable React host

Treat the component as client-only until its source proves otherwise. Keep browser effects inside the host framework's client boundary/island and preserve a meaningful static fallback for critical content.

## Choosing an implementation path

1. If the project has `components.json` and uses shadcn conventions, use the shadcn registry command from `installation.md`.
2. Otherwise use the jsrepo command, or manually copy the selected source and CSS when the user wants control over placement.
3. Use the project’s established package manager to add any missing declared dependency. The React Bits installer/source, not the skill, determines that dependency list.

## A question only when it is necessary

If neither repository evidence nor the user establishes a variant, ask: “Is this project TypeScript or JavaScript, and does it use Tailwind or regular CSS?” Do not ask when the files answer it.
