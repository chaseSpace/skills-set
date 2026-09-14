# Requirements intake and exact component selection

Read this when a React Bits request is not specific enough to choose a component safely. The goal is to turn a design intention into a confirmed, existing React Bits component—not to start coding from an imagined effect.

## Identify what is missing

Ask only for the unknown details. A compact, useful default is:

> To select the right complete React Bits component, please tell me: (1) the project/framework and whether it uses TypeScript and Tailwind or CSS; (2) the route, page, and exact area where it belongs; (3) what visitors should see and what triggers it; (4) whether it is a background, text treatment, or interactive UI element; and (5) any content, asset, mobile, reduced-motion, or performance constraints.

Use repository inspection for facts that files can establish (framework, TypeScript, Tailwind, SSR, shadcn), and ask the user only for the product/design decisions it cannot establish.

## Detail to resolve before code

| Area | Clarify when unknown |
| --- | --- |
| Project | Repository/path, framework, rendering model, TypeScript or JavaScript, Tailwind or CSS, and existing component conventions |
| Placement | Route/page, named section, container bounds, foreground/background stacking, whether the visual repeats or is one-off |
| Intent | The exact visual result, information hierarchy, motion/interaction trigger, and what must remain readable/clickable |
| Content | Existing copy, images/models/logos/data, asset ownership, and whether placeholders are acceptable |
| Constraints | Mobile/touch behavior, keyboard and screen-reader expectations, reduced motion, performance/GPU budget, and brand/design-system restrictions |
| Product scope | Whether the user wants a free component or has a Pro license for page blocks/app UI/templates |

When a user says only “make it cooler,” “add an animation,” “use a React Bits background,” or gives a screenshot without placement/behavior, treat it as ambiguous. Do not translate that into code or choose a random effect.

## Offer concrete, existing choices

After the outcome is clear, read only the matching category catalog and offer two or three listed identifiers. Each option must include its actual identifier and a material tradeoff.

Example for a dark developer-tool hero that needs a restrained background:

| Existing component | Why it fits | Tradeoff |
| --- | --- | --- |
| `DarkVeil` | Subtle, content-safe dark atmosphere | Less visually expressive |
| `DotGrid` | Technical grid with interaction | More active pointer behavior |
| `FaultyTerminal` | Terminal/CRT aesthetic | Deliberately retro and higher visual noise |

Ask the user to select one, or explicitly approve your recommendation. Do not use a component that is merely similar, not listed in the applicable catalog, or named from memory.

## Required handoff record

Before an installation command or source edit, state and retain this record:

```text
Selected React Bits component: <exact existing identifier>
Variant: <TS-TW | TS-CSS | JS-TW | JS-CSS>
Target: <route/page/section and layer>
Behavior: <visible result and trigger>
```

If the user changes the location, intended effect, or component choice, return to the corresponding intake item and reconfirm the named component before changing code.
