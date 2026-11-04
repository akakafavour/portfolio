# AGENT IMPLEMENTATION BUILD SPECIFICATION
**Project:** Independent Portfolio for Growth Marketer & Web Designer  
**Target Execution:** Any AI Agent, Subagent, or Senior Frontend Engineer  
**Reference Files:** Must strictly read `DESIGN.md` and `COPY.md` before writing code.

---

## 1. Golden Rules for the Implementing Agent

1. **Strictly Rounded Button Geometry:** All buttons, pills, tags, and interactive cards must have rounded borders (`rounded-full` or minimum `rounded-2xl`). Never output sharp 90-degree rectangle buttons.
2. **Strictly Zero AI Slop:** 
   * Zero words from the Banned Vocabulary (*Empower, Revolutionize, Seamless, Elevate, Delve, Game-changing, Next-gen, Unleash, Streamline, Supercharge*).
   * Strictly zero em-dashes (`—`). Use periods, commas, colons, or line breaks.
   * Strictly zero fake local time clocks, zero blinking green status dots, and zero Telegram links.
3. **Typography Standard:** Use Apple SF Pro Display, SF Pro Text, and SF Mono (or Geist/Inter fallbacks with matching optical tracking).
4. **Color Distribution:** 65% Abyssal Slate (`#080A0F`), 25% Graphite Glass (`rgba(14, 17, 24, 0.72)`), 8% Warm Titanium Silver (`#EDEDEA`), 2% Specular Liquid Mercury & Chrome Shine (`#FFFFFF`).

---

## 2. Recommended Tech Stack

* **Framework:** Next.js (App Router, TypeScript) or Vite + React (TypeScript).
* **Styling:** Tailwind CSS with custom theme tokens mapped to `DESIGN.md`.
* **Smooth Scrolling:** `lenis` for inertial, momentum-based smooth scrolling.
* **Scroll Animation:** `gsap` + `ScrollTrigger` for the pinned Hero-to-Projects communicating scroll runway.
* **Interactive Canvas / Shaders:** `three` (Three.js) or native WebGL with a custom GLSL fragment shader for the Hydrodynamic Liquid Surface Tension & ASCII Matrix reveal.
* **Component Motion:** `framer-motion` for layout transitions, spirit-level nav bubble, and category filters.

---

## 3. Recommended Project Directory Structure

```text
/
├── DESIGN.md                  # Single source of truth design tokens & physics
├── COPY.md                    # Exact verbatim copy for all pages and components
├── AGENT_BUILD_SPEC.md        # This implementation blueprint
├── public/
│   ├── assets/
│   │   ├── portrait.png       # Centered side-profile portrait (dark grey/black backdrop)
│   │   └── ascii-landscape.svg# Dense ASCII stippled mountain silhouette
├── src/
│   ├── app/ (or /pages)
│   │   ├── layout.tsx         # Root layout with metadata, smooth scroll (Lenis), and fonts
│   │   ├── page.tsx           # Homepage (Hero, Sticky Seam, Services, Work, Essays, Footer)
│   │   ├── work/
│   │   │   ├── page.tsx       # Dedicated Work Archive / Gallery with category filters
│   │   │   └── [slug]/
│   │   │       └── page.tsx   # Dedicated Case Study Subpage Template
│   ├── components/
│   │   ├── nav/
│   │   │   ├── FloatingNav.tsx       # Liquid glass squircle with Spirit Level bubble
│   │   │   └── SpiritLevelBubble.tsx # Elastic stretching indicator
│   │   ├── hero/
│   │   │   ├── HeroStage.tsx         # Split tension: Bold title left, human pitch right
│   │   │   ├── LiquidAsciiCanvas.tsx # WebGL / Three.js liquid ripple & ASCII reveal
│   │   │   └── StickySeam.tsx        # GSAP ScrollTrigger pinned runway (250vh)
│   │   ├── services/
│   │   │   ├── ServicesGrid.tsx      # Modular 3-pillar layout (Web, Copy, AI)
│   │   │   └── ServiceCard.tsx       # Bold left header, hook + body right
│   │   ├── work/
│   │   │   ├── WorkShowcase.tsx      # Unified 16:9 widescreen showcase stack
│   │   │   ├── UnifiedProjectCard.tsx# Unified card chassis
│   │   │   └── WorkFilters.tsx       # Spirit-level filter pills for /work
│   │   ├── perspective/
│   │   │   ├── PerspectiveSection.tsx# 3 editorial essays
│   │   │   └── EssayCard.tsx         # Reading time + hook + excerpt
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
1. Initialize the project with TypeScript and Tailwind CSS.
2. In `tailwind.config.ts`, register the exact design tokens from `DESIGN.md`:
   * Colors: `canvas-abyssal` (`#080A0F`), `surface-glass` (`rgba(14, 17, 24, 0.72)`), `text-primary` (`#EDEDEA`), `accent-sheen` (`#FFFFFF`).
   * Border radii: `rounded-pill: '9999px'`.
   * Easing curves: `snappy: 'cubic-bezier(0.16, 1, 0.3, 1)'`, `elastic: 'cubic-bezier(0.34, 1.56, 0.64, 1)'`.

### Phase 2: The Floating Nav & Spirit Level Bubble
1. Build `FloatingNav.tsx` as a fixed, centered pill (`top: 20px`, `z-index: 50`).
2. Add backdrop blur (`blur-xl`), semi-transparent background, and hairline border.
3. Build `SpiritLevelBubble.tsx` using `framer-motion`:
   * Track the active section (via IntersectionObserver or scroll position).
   * When switching tabs, stretch the bubble horizontally by `1.15x` during transit, then snap to rest with `cubic-bezier(0.34, 1.56, 0.64, 1)`.
   * Ensure links are labeled: `Work`, `Services`, `Writing`, plus `Let's Talk` pill on right.

### Phase 3: The Hero Stage & Liquid ASCII Ripple Shader
1. Build `HeroStage.tsx`:
   * Left side: `GROWTH MARKETER. WEB DESIGNER.` in massive, heavy condensed font.
   * Right side: Human conversational narrative verbatim from `COPY.md`.
2. Build `LiquidAsciiCanvas.tsx`:
   * Center the side-profile portrait within a canvas container.
   * On CPU/GPU: Render the portrait texture. Prepare a matching grayscale luminance map.
   * Monospace ASCII matrix: Map character density (`·`, `:`, `+`, `%`, `#`, `@`) to luminance.
   * Fluid ripple physics: On mousemove or touch drag, track coordinates and velocity. Calculate a hydrodynamic displacement field ($80\text{px}\text{--}120\text{px}$ radius). Displace the photographic pixels into a wave disturbance, exposing the illuminated ASCII characters underneath with a polished silver-chrome sheen (`#FFFFFF`).
   * When the cursor leaves, lerp back to rest state over `400ms`.
   * On mobile viewports: Bind to `touchstart` and `touchmove` events; reduce ASCII grid resolution by 50% for 60fps performance.

### Phase 4: The Hero-to-Projects Sticky Communicating Seam
1. Wrap the Hero in a `250vh` container with GSAP ScrollTrigger (`pin: true`, `scrub: 1`).
2. Map scroll progress (`0.0 -> 1.0`):
   * `0.0 -> 0.5`: The headline text parts outward with opacity fade; the centered portrait gently scales down ($1.0 \to 0.88$).
   * `0.3 -> 0.8`: The liquid displacement shader ripples outward from center.
   * `0.5 -> 1.0`: The `SelectedWork` showcase stage translates upward from the bottom, overlapping the pinned hero.

### Phase 5: What I Do (Services Modular Grid)
1. Build `ServicesGrid.tsx` with the 3 unboxed pillars from `COPY.md`:
   * `Web Design & Frontend` (Includes line for existing website redesigns/SEO).
   * `Copywriting & Content` (Includes lifecycle & email funnels).
   * `AI Integration & Business Automation` (Focuses on operational time savings and routine task automation).
2. Layout: Bold headline on the left, hook and human paragraph on the right, deliverable tag pills underneath.

### Phase 6: Selected Work Showcase & Dedicated Subpages
1. Build `WorkShowcase.tsx`:
   * Vertical stack of 16:9 widescreen cards (`Horizon Goods`, `MetricFlow`, `Atelier Ops`).
   * Hover elevates card by 4px, illuminates border, and reveals `[ View Case Study -> ]` pill.
   * Clicking a card routes to `/work/[slug]`.
2. Build `/work/page.tsx` (Work Archive):
   * Category filter bar with spirit-level pills (`All Projects`, `Web & Storefronts`, `Copywriting & Strategy`, `AI & Automation`).
   * Reorganizes projects using Framer Motion layout springs.
3. Build `/work/[slug]/page.tsx` (Case Study Template):
   * 4-column Executive Horizon (Client, Year, Role, Key Outcome).
   * The Problem, The Strategy & Messaging, The Build, The Business Impact.
   * Next project bottom rail.

### Phase 7: Grounded Large Type Negative Footer
1. Build `GroundedFooter.tsx`:
   * Big callout: `HAVE A PROJECT IN MIND? LET'S TALK.`
   * `CopyEmailPill.tsx`: Clicking copies `hello@yourdomain.com` and switches label to `COPIED ✓` for 2 seconds.
   * Direct booking pill: `Book a 15-Minute Scoping Call ->`.
   * `DenseAsciiIcons.tsx`: High-density monospace ASCII matrices for **X**, **LinkedIn**, and **GitHub** inside rounded squircle pills.
   * Base layer: Dense ASCII stippled landscape silhouette SVG.
   * Negative typography: Giant `LET'S BUILD` spanning edge-to-edge with bottom 40% masked into `#080A0F`.
   * Back to top pill with smooth scroll.

---

## 5. Verification Checklist Before Marking Work Complete

* [ ] **Button Geometry:** Every single button and pill has `rounded-full` or generous rounded squircle corners. Zero sharp rectangles.
* [ ] **Vocabulary Check:** Grep the entire codebase for banned words (`Empower`, `Revolutionize`, `Seamless`, `Elevate`, `Delve`, `Game-changing`, `Next-gen`, `Unleash`, `Streamline`, `Supercharge`). Zero instances allowed.
* [ ] **Punctuation Check:** Grep the entire codebase for em-dashes (`—`). Zero allowed.
* [ ] **Trope Check:** Ensure no fake local time clocks, no blinking status dots, and no Telegram links exist.
* [ ] **Performance:** Test at 60fps on both desktop (mouse ripple) and mobile (touch drag).
* [ ] **Responsive Breakpoints:** Verify cleanly at 375px, 768px, 1280px, and 1920px.


---

## 6. Optional Easter Egg: The X-Ray ASCII Mode Switch (`AsciiModeToggle.tsx`)

* **Component:** `src/components/easter-egg/AsciiModeToggle.tsx`
* **Placement:** Bottom-right corner floating pill or integrated into `FloatingNav.tsx`.
* **Implementation Logic:**
  * Uses a global state (e.g. `isAsciiMode: boolean`).
  * When active, applies a full-screen WebGL / canvas shader pass or ASCII character-replacement overlay across rendered elements for 5 seconds.
  * Trigger pill toggles between `[ ASCII VIEW: OFF ]` and `[ ASCII VIEW: ON ]`.
  * Triggers a fast 500ms vertical liquid mercury wave across the screen during state transitions.
