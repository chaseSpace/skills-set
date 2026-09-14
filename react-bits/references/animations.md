# General animations and interactions

Read this only for a non-text-specific transition, hover effect, cursor effect, or decorative interaction. First choose the least expensive effect that meets the request. A wrapper or CSS-friendly hover effect is normally a better fit for product UI than a full-screen cursor trail or shader.

## Choose by intent

| Need | Good starting components |
| --- | --- |
| Reveal existing content | `AnimatedContent`, `FadeContent`, `GradualBlur`, `ScrollExpand` |
| Add a small interactive affordance | `Magnet`, `GlareHover`, `ElectricBorder`, `StarBorder`, `StickerPeel` |
| Add a logo/image presentation effect | `LogoLoop`, `OrbitImages`, `PixelTransition`, `PixelSwap` |
| Build a cursor-led campaign/portfolio moment | `BlobCursor`, `CursorGrid`, `ImageTrail`, `Ribbons`, `TargetCursor` |
| Add a canvas/physics visual | `Antigravity`, `Cubes`, `ElasticMesh`, `MetaBalls`, `Strands` |

Cursor and full-surface effects should be one intentional accent per view. Check touch behavior and provide a no-motion/degraded fallback.

## Registry catalog

| Identifier | Intended effect | Documentation |
| --- | --- | --- |
| `AnimatedContent` | Configurable mount/scroll wrapper | [page](https://www.reactbits.dev/animations/animated-content) |
| `Antigravity` | Cursor-repelled 3D particles | [page](https://www.reactbits.dev/animations/antigravity) |
| `BlobCursor` | Inertial morphing blob cursor | [page](https://www.reactbits.dev/animations/blob-cursor) |
| `ClickSpark` | Click-position particle burst | [page](https://www.reactbits.dev/animations/click-spark) |
| `Crosshair` | Custom crosshair cursor | [page](https://www.reactbits.dev/animations/crosshair) |
| `Cubes` | Rotating 3D cube cluster | [page](https://www.reactbits.dev/animations/cubes) |
| `CursorGrid` | Pointer-lit canvas grid | [page](https://www.reactbits.dev/animations/cursor-grid) |
| `ElasticMesh` | Pointer-stretched spring mesh | [page](https://www.reactbits.dev/animations/elastic-mesh) |
| `ElectricBorder` | Animated electric border | [page](https://www.reactbits.dev/animations/electric-border) |
| `FadeContent` | Directional fade/slide wrapper | [page](https://www.reactbits.dev/animations/fade-content) |
| `GhostCursor` | Trailing ghost cursor | [page](https://www.reactbits.dev/animations/ghost-cursor) |
| `GlareHover` | Pointer-following glare | [page](https://www.reactbits.dev/animations/glare-hover) |
| `GlowCursor` | Shader light trail | [page](https://www.reactbits.dev/animations/glow-cursor) |
| `GradualBlur` | Triggered progressive unblur | [page](https://www.reactbits.dev/animations/gradual-blur) |
| `HalftoneReveal` | Pointer halftone reveal | [page](https://www.reactbits.dev/animations/halftone-reveal) |
| `ImageTrail` | Cursor image trail | [page](https://www.reactbits.dev/animations/image-trail) |
| `LaserFlow` | Dynamic laser surface light | [page](https://www.reactbits.dev/animations/laser-flow) |
| `LogoLoop` | Seamless logo marquee | [page](https://www.reactbits.dev/animations/logo-loop) |
| `MagicRings` | Interactive ring visual | [page](https://www.reactbits.dev/animations/magic-rings) |
| `Magnet` | Magnetic cursor attraction | [page](https://www.reactbits.dev/animations/magnet) |
| `MagnetLines` | Pointer-bending field lines | [page](https://www.reactbits.dev/animations/magnet-lines) |
| `MetaBalls` | Liquid merging metaballs | [page](https://www.reactbits.dev/animations/meta-balls) |
| `MetallicPaint` | Liquid-metal SVG treatment | [page](https://www.reactbits.dev/animations/metallic-paint) |
| `Noise` | Animated grain overlay | [page](https://www.reactbits.dev/animations/noise) |
| `OrbitImages` | SVG-path orbiting images | [page](https://www.reactbits.dev/animations/orbit-images) |
| `PixelSwap` | Pixel assemble/swap transition | [page](https://www.reactbits.dev/animations/pixel-swap) |
| `PixelTrail` | Pixel cursor trail | [page](https://www.reactbits.dev/animations/pixel-trail) |
| `PixelTransition` | Pixel-dissolve hover transition | [page](https://www.reactbits.dev/animations/pixel-transition) |
| `Ribbons` | Physics-driven pointer ribbons | [page](https://www.reactbits.dev/animations/ribbons) |
| `RippleDistortion` | Pointer water displacement | [page](https://www.reactbits.dev/animations/ripple-distortion) |
| `ScrollExpand` | Scroll-to-full-bleed media | [page](https://www.reactbits.dev/animations/scroll-expand) |
| `ShapeBlur` | Hovering blurred geometry | [page](https://www.reactbits.dev/animations/shape-blur) |
| `SplashCursor` | Liquid splash cursor | [page](https://www.reactbits.dev/animations/splash-cursor) |
| `StarBorder` | Sparkling animated border | [page](https://www.reactbits.dev/animations/star-border) |
| `StickerPeel` | 3D sticker corner peel | [page](https://www.reactbits.dev/animations/sticker-peel) |
| `Strands` | Glowing woven strands | [page](https://www.reactbits.dev/animations/strands) |
| `SwarmCursor` | Flocking pointer particles | [page](https://www.reactbits.dev/animations/swarm-cursor) |
| `TargetCursor` | Cursor targets with corner lock | [page](https://www.reactbits.dev/animations/target-cursor) |

For install commands and SSR rules, read `installation.md` after choosing the identifier.
