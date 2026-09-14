# UI components

Read this only for an interactive UI element, navigation surface, layout, card, gallery, carousel, or input. React Bits is presentation-oriented source code, not a headless accessibility primitive library. Keep application state, routing, semantics, focus management, and form behavior in the host application when the component source does not already provide them.

## Choose by UI need

| Need | Good starting components |
| --- | --- |
| Navigation | `PillNav`, `CardNav`, `FlowingMenu`, `GooeyNav`, `LineSidebar`, `StaggeredMenu` |
| Cards and small interactive panels | `TiltedCard`, `SpotlightCard`, `PixelCard`, `ProfileCard`, `Folder`, `MagicBento` |
| Gallery, carousel, or image storytelling | `Carousel`, `AccordionGallery`, `CircularGallery`, `DepthCarousel`, `Masonry`, `ScrollStack` |
| Inputs and controls | `CurvedInput`, `ElasticSlider`, `OptionWheel`, `Stepper`, `Counter` |
| Spatial/3D showcase | `DomeGallery`, `Lanyard`, `ModelViewer`, `MorphSlider`, `InfiniteSpiral` |

For menus, carousels, inputs, and dialogs, test keyboard interaction, focus visibility, visible labels, touch controls, and screen-reader semantics. Avoid using a visual-only component where the product needs a robust accessible behavior primitive.

## Registry catalog

| Identifier | Intended component | Documentation |
| --- | --- | --- |
| `AccordionGallery` | Expanding image panels | [page](https://www.reactbits.dev/components/accordion-gallery) |
| `AnimatedList` | Staggered item list | [page](https://www.reactbits.dev/components/animated-list) |
| `BorderGlow` | Pointer-sensitive glow border | [page](https://www.reactbits.dev/components/border-glow) |
| `BounceCards` | Mounting animated cards | [page](https://www.reactbits.dev/components/bounce-cards) |
| `BubbleMenu` | Expanding circular menu | [page](https://www.reactbits.dev/components/bubble-menu) |
| `CardNav` | Navigation with expanding cards | [page](https://www.reactbits.dev/components/card-nav) |
| `CardSwap` | Swapping card layout | [page](https://www.reactbits.dev/components/card-swap) |
| `Carousel` | Responsive touch carousel | [page](https://www.reactbits.dev/components/carousel) |
| `ChromaGrid` | Color-revealing tile grid | [page](https://www.reactbits.dev/components/chroma-grid) |
| `CircularGallery` | Rotating circular image gallery | [page](https://www.reactbits.dev/components/circular-gallery) |
| `Counter` | General animated counter | [page](https://www.reactbits.dev/components/counter) |
| `CurvedInput` | Arc-shaped input and submit | [page](https://www.reactbits.dev/components/curved-input) |
| `DecayCard` | Disintegrating hover card | [page](https://www.reactbits.dev/components/decay-card) |
| `DepthCarousel` | 3D-rail carousel | [page](https://www.reactbits.dev/components/depth-carousel) |
| `Dock` | macOS-style magnifying dock | [page](https://www.reactbits.dev/components/dock) |
| `DomeGallery` | Immersive 3D image dome | [page](https://www.reactbits.dev/components/dome-gallery) |
| `DriftWall` | Endless perspective tile wall | [page](https://www.reactbits.dev/components/drift-wall) |
| `ElasticSlider` | Springy slider control | [page](https://www.reactbits.dev/components/elastic-slider) |
| `FlowingMenu` | Flowing active-menu indicator | [page](https://www.reactbits.dev/components/flowing-menu) |
| `FluidGlass` | Liquid-distortion glass surface | [page](https://www.reactbits.dev/components/fluid-glass) |
| `FlyingPosters` | Scroll-rotating 3D posters | [page](https://www.reactbits.dev/components/flying-posters) |
| `Folder` | Opening content folder | [page](https://www.reactbits.dev/components/folder) |
| `GlassIcons` | Frosted-glass icon set | [page](https://www.reactbits.dev/components/glass-icons) |
| `GlassSurface` | Apple-style refractive glass | [page](https://www.reactbits.dev/components/glass-surface) |
| `GooeyNav` | Morphing navigation indicator | [page](https://www.reactbits.dev/components/gooey-nav) |
| `InfiniteMenu` | Endless horizontal menu | [page](https://www.reactbits.dev/components/infinite-menu) |
| `InfiniteSpiral` | Interactive 3D image helix | [page](https://www.reactbits.dev/components/infinite-spiral) |
| `Lanyard` | Swinging 3D badge card | [page](https://www.reactbits.dev/components/lanyard) |
| `LineSidebar` | Proximity-reactive sidebar | [page](https://www.reactbits.dev/components/line-sidebar) |
| `MagicBento` | Interactive bento grid | [page](https://www.reactbits.dev/components/magic-bento) |
| `Masonry` | Animated responsive masonry | [page](https://www.reactbits.dev/components/masonry) |
| `ModelViewer` | Three.js model viewer | [page](https://www.reactbits.dev/components/model-viewer) |
| `MorphSlider` | WebGL image slider | [page](https://www.reactbits.dev/components/morph-slider) |
| `OptionWheel` | Curved, draggable option picker | [page](https://www.reactbits.dev/components/option-wheel) |
| `PillNav` | Pill navigation | [page](https://www.reactbits.dev/components/pill-nav) |
| `PixelCard` | Pixel-revealed card | [page](https://www.reactbits.dev/components/pixel-card) |
| `ProfileCard` | 3D glare profile card | [page](https://www.reactbits.dev/components/profile-card) |
| `ReflectiveCard` | Webcam/cursor reflective card | [page](https://www.reactbits.dev/components/reflective-card) |
| `ScrollStack` | Scroll-driven card stack | [page](https://www.reactbits.dev/components/scroll-stack) |
| `SpecularButton` | Shader-rim-light button | [page](https://www.reactbits.dev/components/specular-button) |
| `SpotlightCard` | Pointer spotlight card | [page](https://www.reactbits.dev/components/spotlight-card) |
| `Stack` | Swipeable/autoplay card stack | [page](https://www.reactbits.dev/components/stack) |
| `StaggeredMenu` | Animated opening menu | [page](https://www.reactbits.dev/components/staggered-menu) |
| `Stepper` | Multi-step progress UI | [page](https://www.reactbits.dev/components/stepper) |
| `TiltedCard` | Pointer-tilt card | [page](https://www.reactbits.dev/components/tilted-card) |

For install commands and SSR rules, read `installation.md` after choosing the identifier.
