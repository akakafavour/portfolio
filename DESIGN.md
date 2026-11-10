# DESIGN SPECIFICATION: INDEPENDENT STUDIO & DIGITAL PORTFOLIO
**Version:** 3.0.0  
**Title:** PRODUCT DESIGNER. GROWTH MARKETER.  
**Authority:** Atelier Creative Studio Laws (Zero Generic AI Slop, Zero Canned Templates)

---

## 1. High-Level Creative Vision & Philosophy

This portfolio is an unboxed, high-ticket digital experience for a **Product Designer & Growth Marketer**. It bridges visual product interfaces, conversion copywriting, customer acquisition funnels, and operational AI automation under one unified standard of craft.

### Signature Mechanics & Invariants
1. **The Hero Left/Right Spatial Tension:** 
   * Left: Massive, bold, condensed headline: `PRODUCT DESIGNER. GROWTH MARKETER.`
   * Right: Clean, human conversational pitch explaining real business outcomes with chromatic word highlights (zero corporate buzzwords).
2. **Monumental Centered Portrait & Liquid ASCII Ripple:**
   * A dramatic, centered side-profile photographic portrait fills the center vertical axis of the hero stage.
   * Underneath the skin and contours lies a live, real-time ASCII typography matrix rendered in monospace characters (`.`, `:`, `+`, `%`, `#`, `@`).
   * As the cursor moves across the face, it calculates a fluid disturbance field within an $80\text{px}\text{--}120\text{px}$ hydrodynamic surface-tension radius.
   * The photographic surface ripples like dark liquid mercury, parting cleanly to reveal the polished silver-chrome ASCII typography beneath.
   * When the cursor leaves, surface tension pulls the photograph back into rest state over $400\text{ms}$.
3. **The Pinned Hero & Sliding Horizontal Work Stage:**
   * As scroll begins, the Hero pins in place (`position: sticky; top: 0`).
   * The **Selected Work** stage (engineered with deep rounded corners `rounded-t-[36px]` and a $1\text{px}$ silver hairline) slides upward directly **on top of the pinned hero**.
   * Once fully covering the viewport, the stage locks and its inner 16:9 project cards scrub **horizontally (sideways from right to left)** across the screen.
   * Scrolling back up perfectly reverses the sequence: the horizontal track rewinds to Project 01, and the stage glides back down to unmask the Hero.
4. **The Apple Dynamic Island Nav (Liquid Drop, Spread, Contract & Proximity):**
   * *Entrance:* Drops from top center as a compact dark capsule. Upon landing ($20\text{px}$ from top), liquid clear glass optical refraction spreads outward from the center to the outer edges like water parting on a crystal lens, settling into an ultra-clear squircle pill.
   * *Scroll Contraction:* As the user scrolls through content, the nav smoothly contracts into a sleek micro-capsule (`[ YOUR NAME • Let's Talk ]`).
   * *Proximity Expansion:* Moving the cursor within $80\text{px}$ of the top edge causes the capsule to fluidly expand back to full size with spring physics (`cubic-bezier(0.34, 1.56, 0.64, 1)`), revealing all links.
   * *The Spirit Level Bubble:* Inside the nav, the active indicator is an **Electric Acid Lime liquid bubble** that stretches with movement velocity and snaps into resting roundness.
5. **The Moving Brand Strip (Social Proof Ticker):**
   * An infinite, smooth horizontal marquee of client and platform logos in monochromatic silver, placed directly after Selected Work. Hovering slows the ticker by $80\%$.
6. **Services: Expandable Architectural Drawers:**
   * Three full-width rows featuring giant wireframe outline numbers (`01`, `02`, `03`). Clicking a row expands downward with an illuminated Acid Lime border to reveal the problem/solution narrative and an editorial deliverable index.
7. **The About Me Section:**
   * A floating hairline pill badge (`[ About Me ]`), a background running kinetic text marquee (`about · about · about`), a distinct candid visual frame, the hybrid edge thesis, and numeric proof chips.
8. **Strict Rounded Geometry:**
   * All buttons, cards, pills, and container edges must feature rounded geometry (`rounded-full`, `rounded-3xl`, `rounded-[36px]`). Strictly zero sharp 90-degree rectangle edges.
9. **Banned Elements:**
   * Strictly zero em-dashes (`—`).
   * Strictly zero blinking green status dots or pulsing fake activity rings.
   * Strictly zero fake local time clocks.
   * Strictly zero Telegram links (use X, LinkedIn, GitHub, and Email only).

---

## 2. Design Tokens & Visual Distribution

### Color Hierarchy (65 / 25 / 8 / 2 Balance)

| Token Name | Hex Value | Viewport Share | Semantic Role |
|---|---|---|---|
| `canvas-abyssal` | `#07080A` | **65%** | Absolute pitch-black obsidian slate canvas. |
| `surface-glass` | `rgba(15, 17, 23, 0.42)` | **25%** | Liquid clear optical glass (iOS style) with dual-rim specular highlights, 16px backdrop blur, and background refraction. |
| `border-subtle` | `rgba(255, 255, 255, 0.08)` | Structural | 1px hairline structural rules, dividers, and card outlines. |
| `border-active` | `rgba(255, 255, 255, 0.25)` | State | Illuminated border on hover or active drawer states. |
| `text-primary` | `#FFFFFF` | **8%** | Absolute crisp white for headlines and high-emphasis reading. |
| `text-muted` | `#868994` | Supportive | Secondary metadata, labels, and paragraph body copy. |
| `accent-lime` | `#D4FF00` | **<2%** | Electric Acid Lime spot accent: nav fluid bubble, chromatic word highlights, and active drawer accents. |
| `accent-chrome` | `#FFFFFF` | Specular | Liquid mercury specular reflections on the ASCII ripple disturbance. |

---

## 3. Typography Hierarchy (Geist Open-Source System)

To ensure zero Apple licensing liabilities while maintaining optical density and tight tracking, the system standardizes on **Geist & Geist Mono** (by Vercel):

| Level | Family | Desktop Size | Mobile Size | Line Height | Tracking | Weight |
|---|---|---|---|---|---|---|
| **Display Title (Hero Left)** | Geist Sans | `clamp(3.0rem, 7vw, 6.5rem)` | `clamp(2.2rem, 8vw, 3.2rem)` | 0.95 | `-0.04em` | 800 (Heavy) |
| **Section Title** | Geist Sans | `clamp(2.0rem, 4vw, 3.2rem)` | `1.85rem` | 1.1 | `-0.03em` | 700 (Bold) |
| **Card Header** | Geist Sans | `1.5rem` (24px) | `1.25rem` (20px) | 1.2 | `-0.02em` | 600 (Semibold) |
| **Body Primary** | Geist Sans | `1.0625rem` (17px) | `1.0rem` (16px) | 1.55 | `-0.01em` | 400 (Regular) |
| **Body Muted** | Geist Sans | `0.9375rem` (15px) | `0.875rem` (14px) | 1.5 | `0em` | 400 (Regular) |
| **Monospace / ASCII** | Geist Mono | `0.8125rem` (13px) | `0.75rem` (12px) | 1.4 | `+0.02em` | 500 (Medium) |

---

## 4. Canonical Motion Curves

* **Snappy Luxury (Primary Curve):** `cubic-bezier(0.16, 1, 0.3, 1)`  
  *Used for:* Nav bubble travel, drawer expansion, card hover elevations, and horizontal track scrub.
* **Liquid Elasticity (Dynamic Island & Bubble):** `cubic-bezier(0.34, 1.56, 0.64, 1)`  
  *Used for:* Nav horizontal expansion, proximity spring, and spirit-level bubble stretch.
* **Subtle Settle:** `cubic-bezier(0.25, 1, 0.5, 1)`  
  *Used for:* Button active compressions, input states, and micro-interactions.

---

## 5. Component Specifications & State Architecture

### A. The Dynamic Island Nav (Liquid Glass Squircle)
* **Geometry:** Floating centered pill. Height: `48px`, Width: auto (inline-flex), `border-radius: 9999px`.
* **Position:** Fixed `top: 20px`, `z-index: 50`.
* **Material (Clear Liquid Glass / iOS Style):**
  * Fill: `rgba(15, 17, 23, 0.42)` (true optical transparency).
  * Optics: `backdrop-filter: blur(16px) saturate(180%)`.
  * Specular Rim Lighting: `box-shadow: inset 0 1px 1px 0 rgba(255, 255, 255, 0.32), inset 0 -1px 1px 0 rgba(0, 0, 0, 0.45), 0 16px 36px -8px rgba(0, 0, 0, 0.6)`.
  * Border: `1px solid rgba(255, 255, 255, 0.15)`.
  * Text Contrast Scrim: `text-shadow: 0 1px 2px rgba(0, 0, 0, 0.75)`.
* **Entrance Physics:** Drops from top center ($44\text{px} \times 44\text{px}$), clear optical refraction and specular edge highlights spread center-to-edge, expands horizontally into full squircle over $750\text{ms}$.
* **Scroll Contraction:** On vertical scroll past $100\text{px}$, contracts into micro-pill (`[ YOUR NAME • Let's Talk ]`).
* **Mouse Proximity:** Moving cursor within $80\text{px}$ of top edge fluidly expands nav back to full pill with `cubic-bezier(0.34, 1.56, 0.64, 1)`.
* **The Spirit Level Bubble:**
  * Active indicator sits behind the active link.
  * Material: `rgba(212, 255, 0, 0.15)` with an interior highlight border `1px solid #D4FF00`.
  * Transition: Stretches by `1.15x` horizontally during transit, snaps to resting pill over `380ms`.

### B. Interactive Buttons (Pill Geometry)
* **Rule:** `border-radius: 9999px` always.
* *Default:* `background: rgba(255, 255, 255, 0.06)`, `border: 1px solid rgba(255, 255, 255, 0.12)`, `color: #FFFFFF`.
* *Hover:* `background: rgba(255, 255, 255, 0.14)`, `border: 1px solid #D4FF00`, scale `1.02x` over `220ms`.
* *Pressed:* Scale `0.97x`, background `rgba(255, 255, 255, 0.22)`.
* *Focus:* `outline: none`, `box-shadow: 0 0 0 2px #07080A, 0 0 0 4px #D4FF00`.

### C. Selected Work: Rounded Horizontal Runway
* **Stage Geometry:** Full-width container with `border-radius: 36px 36px 0 0`, background `#0B0D12`, border `1px solid rgba(255, 255, 255, 0.08)`.
* **Scroll Physics:**
  * Desktop: Glides upward over the pinned hero, locks, and inner project cards scroll horizontally from right to left.
  * Mobile: Stacks into smooth vertical cards with zero locked horizontal friction.
* **Project Cards:**
  * Geometry: 16:9 widescreen stage, `border-radius: 24px`, padding `28px`, background `#12151D`.
  * Header: Project name left, scope pills right (`[ Product Design ]`, `[ Growth Strategy ]`).
  * Hover: Lifts by $4\text{px}$, border glows with silver/lime sheen, `[ View Case Study -> ]` pill reveals.
  * Click: Directly navigates to standalone `/work/[slug]` subpage.

---

## 6. Whole-Site Section Order & Mechanics

### Section 01: The Hero Stage
* Centered monumental portrait with real-time Liquid ASCII Water Ripple.
* Split tension: Bold headline on the left (`PRODUCT DESIGNER. GROWTH MARKETER.`), conversational human thesis on the right with chromatic Acid Lime word highlights.
* Dynamic Island drops in and spreads clear optical refraction and specular edge highlights center-to-edge.

### Section 02: Selected Work (Horizontal Runway on Top of Pinned Hero)
* Hero pins in place as scroll initiates.
* Selected Work stage with rounded top edges (`rounded-t-[36px]`) glides upward over the hero.
* Inner project cards scrub horizontally:
  * Project 01: Horizon Goods (Shopify Storefront & Checkout Rebuild)
  * Project 02: MetricFlow (Repositioning & Growth Launch)
  * Project 03: Atelier Ops (AI Automation & Operations)
  * Anchor Pill: `[ View Complete Work Archive -> ]` linking to `/work`.
* Scrolling back up perfectly reverses the sequence back to the Hero.

### Section 03: The Moving Brand Strip
* Infinite, smooth horizontal marquee of client logos in monochromatic silver (`#868994`).
* Bounded by 1px hairlines. Hovering slows ticker by $80\%$.

### Section 04: Services (Expandable Architectural Drawers)
* Three full-width interactive rows:
  * `01. PRODUCT & WEB DESIGN` (Custom sites, storefronts, interactive products, redesigns & SEO).
  * `02. COPYWRITING & LAUNCH STRATEGY` (Offer positioning, sales copy, lifecycle email funnels).
  * `03. AI INTEGRATION & AUTOMATION` (Custom AI tools, operational delivery automation, CRM routing).
* Giant outline wireframe numbers (`01`, `02`, `03`).
* Clicking row expands downward with illuminated Acid Lime border, revealing problem/solution pitch and numbered deliverable index.

### Section 05: The About Me Section
* Hairline pill badge floating above headline: `[ About Me ]` with top-edge gradient highlight.
* Background kinetic running marquee: `about · about · about · about` in heavy outline typography.
* Left side: High-contrast candid workspace/creator visual frame with signature script watermark.
* Right side: The hybrid edge thesis (why mastering offer + copy + design + code wins) and large numeric proof chips (`+34% Checkout Lift`, `45s AI Triage`, `1 Dedicated Partner`).

### Section 06: Grounded Large Type Negative Footer
* Big bold callout: `HAVE A PROJECT IN MIND? LET'S TALK.`
* Direct email copy pill (`hello@yourdomain.com [COPY]`).
* Direct calendar booking trigger (`[ Book a 15-Minute Scoping Call -> ]`).
* Dense ASCII social icons for **X**, **LinkedIn**, and **GitHub** inside rounded squircle pills.
* High-density ASCII stippled landscape silhouette at the base with large negative typography blending into canvas.
* Strictly zero fake local time clocks. Strictly zero Telegram links.

---

## 7. Interactive Easter Egg: The X-Ray ASCII Mode Switch

* **Location:** Subtle rounded pill trigger in the bottom corner or nav: `[ ASCII VIEW: OFF ]`.
* **Physics:** Clicking sweeps a 500ms liquid mercury wave vertically across the viewport, temporarily rendering the entire interface as an animated, live monospace character matrix (`.`, `:`, `+`, `%`, `#`, `@`). Toggling off ripples everything back to clean photographic design.
