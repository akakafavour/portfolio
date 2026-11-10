# AGENT IMPLEMENTATION BUILD SPECIFICATION
**Project:** Independent Portfolio for Product Designer & Growth Marketer  
**Target Execution:** Any AI Agent, Subagent, or Senior Frontend Engineer  
**Reference Files:** Must strictly read `DESIGN.md` and `COPY.md` before writing code.

---

## 1. Golden Invariants for the Implementing Agent

1. **Strictly Rounded Geometry:** All buttons, pills, tags, drawer headers, and container stages must have rounded borders (`rounded-full`, `rounded-3xl`, `rounded-[36px]`). Never output sharp 90-degree rectangle buttons.
2. **Strictly Zero AI Slop:** 
   * Zero words from the Banned Vocabulary (*Empower, Revolutionize, Seamless, Elevate, Delve, Game-changing, Next-gen, Unleash, Streamline, Supercharge*).
   * Strictly zero em-dashes (`—`). Use periods, commas, colons, or line breaks.
   * Strictly zero fake local time clocks, zero blinking green status dots, and zero Telegram links.
3. **Typography Standard:** Use **Geist & Geist Mono** (by Vercel) for open-source, web-native optical density matching Apple SF Pro with tight negative tracking (`-0.04em`).
4. **Color Distribution:** 65% Abyssal Black (`#07080A`), 25% Graphite Glass (`rgba(14, 17, 24, 0.76)`), 8% Pure White (`#FFFFFF`) & Titanium Silver (`#EDEDEA`), <2% Electric Acid Lime (`#D4FF00`).

---

## 2. Recommended Tech Stack

* **Framework:** Next.js (App Router, TypeScript) or Vite + React (TypeScript).
* **Styling:** Tailwind CSS with custom theme tokens mapped to `DESIGN.md`.
* **Smooth Scrolling:** `lenis` for inertial, momentum-based smooth scrolling.
* **Scroll Animation:** `gsap` + `ScrollTrigger` for:
  * Pinned Hero with Selected Work stage sliding on top (`rounded-t-[36px]`).
  * Horizontal sideways scrub of project cards on desktop.
  * Reversible rewind when scrolling back up.
* **Interactive Canvas / Shaders:** `three` (Three.js) or native WebGL with custom GLSL fragment shader for the Hydrodynamic Liquid Surface Tension & ASCII Matrix reveal.
* **Component Motion:** `framer-motion` for Dynamic Island entrance & spread, spirit-level bubble, and expandable service drawers.

---

## 3. Recommended Project Directory Structure

```text
/
├── DESIGN.md                  # Single source of truth design tokens & physics
├── COPY.md                    # Exact verbatim copy for all pages and components
├── AGENT_BUILD_SPEC.md        # This implementation blueprint
├── README.md                  # Repository manifest and quickstart
├── public/
│   ├── assets/
│   │   ├── hero_concept.jpg   # Widescreen hero concept reference render
│   │   ├── portrait.png       # Centered side-profile portrait (dark grey/black backdrop)
│   │   ├── about-visual.png   # Candid workspace / creator visual with watermark
│   │   └── ascii-landscape.svg# Dense ASCII stippled mountain silhouette
├── src/
│   ├── app/ (or /pages)
│   │   ├── layout.tsx         # Root layout with metadata, Lenis smooth scroll, Geist fonts
│   │   ├── page.tsx           # Homepage (Hero, Work Runway, Brands, Services, About, Footer)
│   │   ├── work/
│   │   │   ├── page.tsx       # Dedicated Work Archive / Gallery with category filters
│   │   │   └── [slug]/
│   │   │       └── page.tsx   # Dedicated Case Study Subpage Template
│   ├── components/
│   │   ├── nav/
│   │   │   ├── DynamicIslandNav.tsx  # Drop, spread, scroll-contract & proximity expand
│   │   │   └── SpiritLevelBubble.tsx # Acid Lime fluid stretching indicator
│   │   ├── hero/
│   │   │   ├── HeroStage.tsx         # Split tension: Bold title left, human pitch right
│   │   │   └── LiquidAsciiCanvas.tsx # WebGL / Three.js liquid ripple & ASCII reveal
│   │   ├── work/
│   │   │   ├── PinnedWorkRunway.tsx  # Hero pin + rounded stage sliding on top + horizontal scrub
│   │   │   ├── UnifiedProjectCard.tsx# 16:9 widescreen card chassis (rounded-3xl)
│   │   │   └── WorkFilters.tsx       # Spirit-level filter pills for /work
│   │   ├── brands/
│   │   │   └── BrandStripTicker.tsx  # Infinite monochrome moving logo ribbon
│   │   ├── services/
│   │   │   ├── ServicesDrawers.tsx   # Expandable architectural drawers (01, 02, 03)
│   │   │   └── DrawerRow.tsx         # Outline number + title + animated expansion
│   │   ├── about/
│   │   │   ├── AboutSection.tsx      # Hairline pill, running about marquee, candid visual
│   │   │   └── ProofChips.tsx        # Numeric metric badges
│   │   └── footer/
│   │       ├── GroundedFooter.tsx    # Big CTA, direct actions, ASCII landscape
│   │       ├── DenseAsciiIcons.tsx   # Monospace ASCII glyph matrices for X, LI, GH
│   │       └── CopyEmailPill.tsx     # Tactile one-click copy button
│   └── lib/
│       ├── tokens.ts                 # Color hexes, easing curves, typography clamps
│       └── projectsData.ts           # Structured data for all projects
```

---

## 4. Step-by-Step Build Sequence for the Agent

### Phase 1: Environment & Token Setup
1. Initialize the project with TypeScript, Tailwind CSS, and `lenis`.
2. In `tailwind.config.ts`, register the exact design tokens from `DESIGN.md`:
   * Colors: `canvas-abyssal` (`#07080A`), `surface-glass` (`rgba(15, 17, 23, 0.42)`), `text-primary` (`#FFFFFF`), `accent-lime` (`#D4FF00`).
   * Border radii: `rounded-pill: '9999px'`, `rounded-stage: '36px'`.
   * Easing curves: `snappy: 'cubic-bezier(0.16, 1, 0.3, 1)'`, `elastic: 'cubic-bezier(0.34, 1.56, 0.64, 1)'`.

### Phase 2: The Dynamic Island Nav
1. Build `DynamicIslandNav.tsx`:
   * Fixed at `top: 20px`, `z-index: 50`.
   * Entrance animation: Drops from top center ($44\text{px} \times 44\text{px}$), clear optical refraction and specular edge highlights spread center-to-edge, expands horizontally into full squircle over $750\text{ms}$. Material: `rgba(15, 17, 23, 0.42)`, `backdrop-filter: blur(16px) saturate(180%)`, dual specular rim lighting.
   * Scroll contraction: When vertical scroll > $100\text{px}$, smoothly contracts into `[ YOUR NAME • Let's Talk ]`.
   * Proximity expansion: When cursor approaches within $80\text{px}$ of top edge, fluidly expands back to full pill.
2. Build `SpiritLevelBubble.tsx`:
   * Acid Lime fluid bubble (`rgba(212, 255, 0, 0.15)`) with an interior `#D4FF00` border.
   * Stretches by `1.15x` horizontally during transit, snaps to rest with `cubic-bezier(0.34, 1.56, 0.64, 1)`.

### Phase 3: The Hero Stage & Liquid ASCII Ripple Shader
1. Build `HeroStage.tsx`:
   * Left side: `PRODUCT DESIGNER. GROWTH MARKETER.` in massive condensed font.
   * Right side: Human conversational narrative verbatim from `COPY.md` with Acid Lime chromatic word highlights.
2. Build `LiquidAsciiCanvas.tsx`:
   * Center the side-profile portrait within a canvas container.
   * Monospace ASCII matrix: Map character density (`.`, `:`, `+`, `%`, `#`, `@`) to luminance.
   * Fluid ripple physics: On mousemove or touch drag, track coordinates and velocity. Calculate a hydrodynamic displacement field ($80\text{px}\text{--}120\text{px}$ radius). Displace photographic pixels into a wave disturbance, exposing the illuminated ASCII characters underneath with a polished silver-chrome sheen (`#FFFFFF`).
   * On mobile viewports: Bind to `touchstart` and `touchmove` events; reduce ASCII grid resolution by 50% for 60fps performance.

### Phase 4: Pinned Hero & Sliding Horizontal Work Stage
1. Build `PinnedWorkRunway.tsx` using GSAP ScrollTrigger:
   * As scroll begins, Hero pins in place (`pin: true`).
   * The Selected Work container (with `rounded-t-[36px]` and top hairline) slides smoothly upward **on top of the pinned hero**.
   * Once covering the screen, the container locks and inner 16:9 cards scrub horizontally from right to left across the screen.
   * Reverse physics: Scrolling back up scrubs the horizontal track back to Project 01, then slides the container back down to re-reveal the full Hero.
   * Mobile fallback: Disables horizontal pin on mobile viewports (<768px), converting to a smooth vertical stack.

### Phase 5: The Moving Brand Strip
1. Build `BrandStripTicker.tsx`:
   * Infinite CSS/Framer Motion horizontal marquee of client logos in monochromatic silver (`#868994`).
   * Hovering reduces velocity by $80\%$.

### Phase 6: Services: Expandable Architectural Drawers
1. Build `ServicesDrawers.tsx` & `DrawerRow.tsx`:
   * 3 full-width rows with wireframe outline numbers (`01`, `02`, `03`).
   * Clicking a row expands downward with an illuminated Acid Lime border (`#D4FF00`).
   * Renders problem/solution pitch on the left, numbered deliverable index on the right, and a direct inquiry button.

### Phase 7: The About Me Section
1. Build `AboutSection.tsx`:
   * Floating hairline pill badge: `[ About Me ]` with top gradient highlight.
   * Giant background running outline marquee: `about · about · about · about`.
   * Candid visual frame on the left with signature script watermark.
   * Hybrid edge conviction copy on the right + numeric proof chips (`+34%`, `45s`, `1 Partner`).

### Phase 8: Grounded Large Type Negative Footer
1. Build `GroundedFooter.tsx`:
   * Big callout: `HAVE A PROJECT IN MIND? LET'S TALK.`
   * `CopyEmailPill.tsx`: Clicking copies `hello@yourdomain.com` and switches label to `COPIED ✓` for 2 seconds.
   * Scoping call trigger: `Book a 15-Minute Scoping Call ->`.
   * `DenseAsciiIcons.tsx`: Monospace ASCII matrices for X, LinkedIn, and GitHub.
   * Dense ASCII stippled landscape silhouette SVG.
   * Negative typography: Giant `LET'S BUILD` spanning edge-to-edge with bottom 40% masked into `#07080A`.

---

## 5. Verification Checklist Before Marking Work Complete

* [ ] **Button & Container Geometry:** Every button, card, and stage has `rounded-full`, `rounded-3xl`, or `rounded-[36px]`. Zero sharp rectangles.
* [ ] **Vocabulary Check:** Grep the entire codebase for banned words (`Empower`, `Revolutionize`, `Seamless`, `Elevate`, `Delve`, `Game-changing`, `Next-gen`, `Unleash`, `Streamline`, `Supercharge`). Zero instances allowed.
* [ ] **Punctuation Check:** Grep the entire codebase for em-dashes (`—`). Zero allowed.
* [ ] **Trope Check:** Ensure no fake local time clocks, no blinking status dots, and no Telegram links exist.
* [ ] **Performance:** Test at 60fps on both desktop (mouse ripple) and mobile (touch drag).
* [ ] **Reversible Scroll Check:** Verify that scrolling up smoothly rewinds the horizontal work track and slides down to unmask the Hero cleanly.
