# Text animations

Read this only for animated words, headings, labels, counters, or typographic hero treatments. The components below are free React Bits registry identifiers. Select the variant via `project-routing.md`, then verify props and dependencies on the linked page before adding code.

## Choose by intent

| Need | Good starting components |
| --- | --- |
| Reveal a heading on load or scroll | `BlurText`, `SplitText`, `ScrollReveal`, `FoldText`, `FallingText` |
| Cycle product claims or statuses | `RotatingText`, `TextType`, `TextLoop`, `SplitFlapText` |
| Animate figures or metrics | `CountUp` |
| Give a brand wordmark a subtle treatment | `GradientText`, `ShinyText`, `StrokeText`, `TrueFocus` |
| Create an intentionally playful/technical effect | `DecryptedText`, `GlitchText`, `Shuffle`, `ASCIIText`, `FuzzyText` |
| Use pointer or spatial interaction | `CircularText`, `VariableProximity`, `TextPressure`, `ScrambledText`, `TextCursor` |
| Build an experimental visual hero | `ParticleText`, `DepthText`, `WarpText`, `MaskedHeading`, `CurvedLoop` |

Avoid high-motion effects for long body copy. Text must remain real, selectable, readable content; do not replace a semantic page heading with a purely decorative canvas treatment.

## Registry catalog

| Identifier | Intended effect | Documentation |
| --- | --- | --- |
| `ASCIIText` | Animated ASCII-backed text | [page](https://www.reactbits.dev/text-animations/ascii-text) |
| `BlurText` | Blur-to-sharp reveal | [page](https://www.reactbits.dev/text-animations/blur-text) |
| `CircularText` | Rotating circular characters | [page](https://www.reactbits.dev/text-animations/circular-text) |
| `CountUp` | Formatted numeric counter | [page](https://www.reactbits.dev/text-animations/count-up) |
| `CurvedLoop` | Draggable loop along a curve | [page](https://www.reactbits.dev/text-animations/curved-loop) |
| `DecryptedText` | Glyph-decryption reveal | [page](https://www.reactbits.dev/text-animations/decrypted-text) |
| `DepthText` | Pointer-parallax extruded text | [page](https://www.reactbits.dev/text-animations/depth-text) |
| `EchoText` | Trailing ghosted text | [page](https://www.reactbits.dev/text-animations/echo-text) |
| `FallingText` | Gravity and bounce entrance | [page](https://www.reactbits.dev/text-animations/falling-text) |
| `FoldText` | Unfolding lines | [page](https://www.reactbits.dev/text-animations/fold-text) |
| `FuzzyText` | Hover-responsive fuzzy text | [page](https://www.reactbits.dev/text-animations/fuzzy-text) |
| `GlitchText` | RGB/glitch distortion | [page](https://www.reactbits.dev/text-animations/glitch-text) |
| `GradientText` | Animated gradient sweep | [page](https://www.reactbits.dev/text-animations/gradient-text) |
| `MaskedHeading` | Image/mesh-filled heading | [page](https://www.reactbits.dev/text-animations/masked-heading) |
| `ParticleText` | Re-forming particle text | [page](https://www.reactbits.dev/text-animations/particle-text) |
| `RotatingText` | Rotating/flip phrase sequence | [page](https://www.reactbits.dev/text-animations/rotating-text) |
| `ScrambledText` | Cursor-local distortion | [page](https://www.reactbits.dev/text-animations/scrambled-text) |
| `ScrollFloat` | Scroll-linked float/parallax | [page](https://www.reactbits.dev/text-animations/scroll-float) |
| `ScrollReveal` | Scroll-linked blur reveal | [page](https://www.reactbits.dev/text-animations/scroll-reveal) |
| `ScrollVelocity` | Velocity-reactive marquee | [page](https://www.reactbits.dev/text-animations/scroll-velocity) |
| `ShinyText` | Reflective sheen | [page](https://www.reactbits.dev/text-animations/shiny-text) |
| `Shuffle` | Character shuffle reveal | [page](https://www.reactbits.dev/text-animations/shuffle) |
| `SplitFlapText` | Mechanical departure-board text | [page](https://www.reactbits.dev/text-animations/split-flap-text) |
| `SplitText` | Per-word/character stagger | [page](https://www.reactbits.dev/text-animations/split-text) |
| `StrokeText` | Drawn outline and fill | [page](https://www.reactbits.dev/text-animations/stroke-text) |
| `TextCursor` | Cursor-following text trail | [page](https://www.reactbits.dev/text-animations/text-cursor) |
| `TextLoop` | Curved SVG text marquee | [page](https://www.reactbits.dev/text-animations/text-loop) |
| `TextPressure` | Pointer-proximity type warp | [page](https://www.reactbits.dev/text-animations/text-pressure) |
| `TextType` | Typewriter text | [page](https://www.reactbits.dev/text-animations/text-type) |
| `TrueFocus` | Sequential focus/blur treatment | [page](https://www.reactbits.dev/text-animations/true-focus) |
| `VariableProximity` | Pointer-distance letter styling | [page](https://www.reactbits.dev/text-animations/variable-proximity) |
| `WarpText` | WebGL pointer warp | [page](https://www.reactbits.dev/text-animations/warp-text) |

For install commands and SSR rules, read `installation.md` after choosing the identifier.
