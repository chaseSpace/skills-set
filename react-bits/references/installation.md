# Installation and integration

## Free React Bits registry

Use a variant-specific component URL. `<Component>` is the PascalCase identifier in the category catalog; `<LANG>` is `JS` or `TS`; `<STYLE>` is `CSS` or `TW`.

```bash
npx shadcn@latest add https://reactbits.dev/r/<Component>-<LANG>-<STYLE>
```

Example for a JavaScript component using regular CSS:

```bash
npx shadcn@latest add https://reactbits.dev/r/SplitText-JS-CSS
```

The equivalent jsrepo path is:

```bash
npx jsrepo@latest add https://reactbits.dev/r/<Component>-<LANG>-<STYLE>
```

Use shadcn when the project already has `components.json`; use jsrepo or manual copying when it does not. Run a CLI command only when the user asks to change the project. For advice-only requests, give the exact command instead.

## After installation

1. Locate the generated component and associated CSS/assets. Follow its exported name and the repository’s import aliases; do not invent an import path.
2. Read the component source and its React Bits page for required props, dependencies, image assets, and usage constraints.
3. Install only dependencies actually declared by the generated component, using the project’s package manager and lockfile convention. Common, but not universal, dependencies are `gsap`, `motion`, `three`, and `ogl`.
4. Place the component behind an appropriate client boundary in an SSR project. See `project-routing.md`.
5. Give the parent a deliberate size, stacking context, and overflow behavior. Backgrounds usually need an absolutely positioned decorative layer plus a relatively positioned foreground content layer.
6. Test keyboard use, reduced motion, narrow viewports, and production build/hydration where applicable.

## Manual source integration

Use manual copy when a CLI is unavailable or the user wants the component under a specific local directory. Copy both the selected variant and every companion stylesheet/asset it imports; preserve relative imports. Then install the source-declared dependencies, adapt aliases to local relative paths, and use the component according to its current documentation.

## Common failure modes

- **Wrong variant:** TS code in a JS project or Tailwind classes in a CSS project. Reinstall/copy the matched variant rather than converting a large component by hand.
- **Missing dependency or asset:** inspect the generated imports and the component page; add the declared package or retain its asset files.
- **`window is not defined` / hydration mismatch:** isolate browser-only source in a client component and avoid random/time-dependent markup during initial render.
- **Content cannot be clicked:** give decorative canvas/background layers `pointer-events: none` unless interaction is required; keep the content layer above them.
- **Poor animation experience:** support `prefers-reduced-motion` and avoid mounting expensive WebGL effects off-screen or in repeated list rows.
