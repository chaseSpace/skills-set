---
name: react-bits
description: Select, install, and integrate React Bits components, animations, and backgrounds in an existing React project. Use when a user asks for React Bits UI; route by the project's JS/TS, CSS/Tailwind, framework, and desired component category. Do not use for non-React projects or general headless UI behavior.
---

# React Bits

Use React Bits as source-owned components, not as a general `react-bits` npm runtime package. Add only the components needed for the requested UI, then integrate and customize their checked-in source.

## Start with the project profile

Before recommending or adding a component, inspect the target project's `package.json`, lockfile, `tsconfig.json`, `components.json`, and styling entrypoints. State the detected or assumed profile before acting. Read [project routing](references/project-routing.md) to select one of the four implementation variants and to handle Next.js/client-only constraints.

Choose the variant from repository evidence:

| Project profile | React Bits variant |
| --- | --- |
| TypeScript + Tailwind | `TS-TW` |
| TypeScript + CSS / CSS Modules | `TS-CSS` |
| JavaScript + Tailwind | `JS-TW` |
| JavaScript + CSS / CSS Modules | `JS-CSS` |

If the repository does not establish the language or styling system and the choice changes files the user must maintain, ask one brief question. Otherwise, use the existing convention; never introduce Tailwind solely to use a React Bits component.

## Route by the requested result

Read exactly one catalog first. Read another only when the user wants a composed result spanning categories.

- Animated headline, number, wordmark, or text treatment: [text animations](references/text-animations.md).
- Motion wrapper, hover effect, cursor effect, or content transition: [animations](references/animations.md).
- Navigation, cards, menus, gallery, carousel, input, or layout primitive: [UI components](references/components.md).
- Full-bleed visual or decorative canvas/WebGL scene: [backgrounds](references/backgrounds.md).
- Marketing sections, dashboards, app screens, templates, or Agent Kit content: [React Bits Pro](references/react-bits-pro.md). This is license-gated and is not a substitute for the free registry.

For every integration, then read [installation and integration](references/installation.md).

## Operating rules

1. Match the component to the user outcome, density, performance budget, and existing design language. Prefer a restrained CSS/DOM effect for ordinary product UI; recommend canvas, 3D, shader, cursor, or full-screen components only when that visual impact is intentional.
2. Verify the component's current React Bits page before choosing props, imports, or dependencies. The catalogs provide discovery names, not an API contract. The installed/copied source and that page are authoritative.
3. Use the exact PascalCase CLI identifier from the catalog; page routes are kebab-case. Install through the project’s selected CLI only when the user has asked to add it. Do not install a lookalike `react-bits` package from npm.
4. Keep each component's generated files and required CSS/assets together. Install any dependency declared by its source with the project’s existing package manager; do not guess whether it needs `gsap`, `motion`, `three`, or `ogl`.
5. In SSR projects, isolate browser-dependent code in a client component. Check for `window`, `document`, canvas/WebGL, pointer events, requestAnimationFrame, or hooks before rendering it from a server component.
6. Preserve keyboard access, semantic controls, readable contrast, and `prefers-reduced-motion`. Ensure decorative layers cannot block pointer events or obscure foreground content.
7. After implementation, run the project’s focused checks and inspect the page at a practical viewport. Verify that the animation does not cause layout shift, hydration errors, or unbounded CPU use.
