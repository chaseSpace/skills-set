---
name: react-bits
description: Select, install, and integrate React Bits components, animations, and backgrounds in an existing React project. Use when a user asks for React Bits UI; route by the project's JS/TS, CSS/Tailwind, framework, and desired component category. Do not use for non-React projects or general headless UI behavior.
---

# React Bits

Use React Bits as source-owned components, not as a general `react-bits` npm runtime package. Add only the components needed for the requested UI, then integrate and customize their checked-in source.

## Requirement and component-selection gate

Do not begin installation, copy code, or implement a React Bits effect when the request is ambiguous. Read [requirements intake](references/requirements-intake.md) when the user has not made the target and effect concrete.

Before any implementation, the conversation must establish all material unknowns:

- the target project/repository (or the user confirms there is no existing project), framework, and styling convention;
- the target route, page/section, and intended placement/layer of the visual;
- the visible effect, content/assets, interaction trigger, and any existing design constraints;
- responsive, accessibility, reduced-motion, and performance constraints relevant to the effect; and
- one exact, existing React Bits component identifier, such as `AcidSquares`.

If the user has not named a component, use the relevant catalog to offer two or three **existing identifiers** that fit the clarified outcome, with one-line tradeoffs, and ask the user to choose or approve one. Do not invent a component name. The selection is ready only when it can be stated unambiguously:

```text
Selected React Bits component: AcidSquares
Target: landing-page hero background, behind the existing heading and CTA
Variant: TS-TW
```

Until this selection is ready, provide discovery and questions only—never a CLI command, partial React Bits snippet, extracted animation function, or hand-recreated approximation of a Bits component.

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

After a named component is selected, read [installation and integration](references/installation.md).

## Operating rules

1. Match the component to the user outcome, density, performance budget, and existing design language. Prefer a restrained CSS/DOM effect for ordinary product UI; recommend canvas, 3D, shader, cursor, or full-screen components only when that visual impact is intentional.
2. Verify the selected component's current React Bits page before choosing props, imports, or dependencies. The catalogs provide discovery names, not an API contract. The installed/copied source and that page are authoritative.
3. Use the exact selected PascalCase CLI identifier from the catalog; page routes are kebab-case. Install through the project’s selected CLI only when the user has asked to add it. Do not install a lookalike `react-bits` package from npm.
4. Add a complete, existing React Bits component only. Use its registry installer, or manually copy its entire selected variant together with every required stylesheet, asset, and declared dependency. Never transplant only an effect hook, shader, helper, CSS fragment, or partial component implementation.
5. Adapt an installed component through documented props and its host layout. Preserve its source as a coherent local component; changes to the component internals must remain inside that complete component, not be pasted piecemeal into an unrelated file.
6. In SSR projects, isolate browser-dependent code in a client component. Check for `window`, `document`, canvas/WebGL, pointer events, requestAnimationFrame, or hooks before rendering it from a server component.
7. Preserve keyboard access, semantic controls, readable contrast, and `prefers-reduced-motion`. Ensure decorative layers cannot block pointer events or obscure foreground content.
8. After implementation, run the project’s focused checks and inspect the page at a practical viewport. Verify that the animation does not cause layout shift, hydration errors, or unbounded CPU use.
