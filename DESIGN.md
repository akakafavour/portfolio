# DESIGN SPECIFICATION: INDEPENDENT STUDIO & DIGITAL PORTFOLIO
**Version:** 2.0.0  
**Title:** GROWTH MARKETER. WEB DESIGNER.  
**Authority:** Atelier Creative Studio Laws (Zero Generic AI Slop, Zero Canned Templates)

---

## 1. High-Level Creative Vision & Philosophy

This portfolio is an unboxed, high-ticket digital experience for a **Growth Marketer & Web Designer**. It merges technical frontend craft with commercial acumen, conversion copywriting, and operational AI automation.

### Signature Mechanics & Invariants
1. **The Hero Left/Right Spatial Tension:** 
   * Left: Massive, bold, condensed Apple-style headline: `GROWTH MARKETER. WEB DESIGNER.`
   * Right: Clean, human conversational paragraph explaining real business outcomes (no corporate buzzwords).
2. **Monumental Centered Portrait & Liquid ASCII Ripple:**
   * A dramatic, centered side-profile photographic portrait of the creator fills the center vertical axis of the hero stage.
   * Underneath the skin and contours lies a live, real-time ASCII typography matrix rendered in monospace characters (`·`, `:`, `+`, `%`, `#`, `@`).
   * As the cursor moves across the face, it calculates a fluid disturbance field within an $80\text{px}\text{--}120\text{px}$ hydrodynamic surface-tension radius.
   * The photographic surface ripples like liquid mercury or water, parting cleanly to reveal the polished silver-chrome ASCII typography beneath.
   * When the cursor leaves, surface tension pulls the photograph back into rest state over $400\text{ms}$.
3. **Hero-to-Projects Sticky Communicating Runway:**
   * The Hero stage is bound to a pinned scroll runway (`250vh` scroll height).
   * As the user scrolls, the Hero stays pinned while scroll progress scrubs the WebGL displacement shader.
   * Headline typography unmasks and parts horizontally, the centered portrait compresses with fluid tension, and the **Selected Work Showcase** rises directly out of the dark water depths to meet the viewer.
4. **The "Spirit Level" Nav Island:**
   * Floating liquid frosted glass squircle (`border-radius: 9999px`) with an active indicator bubble that acts like fluid in a spirit level: stretching horizontally with movement velocity and snapping into pill resting state.
5. **Strict Rounded Geometry:**
   * All buttons, pills, tags, and interactive cards must feature rounded geometry (`border-radius: 9999px` or minimum `16px`). Strictly zero sharp 90-degree rectangle buttons.
6. **Banned Elements:**
   * Strictly zero em-dashes (`—`).
   * Strictly zero blinking green status dots or pulsing fake activity rings.
   * Strictly zero fake local time clocks.
   * Strictly zero Telegram links (use X, LinkedIn, GitHub, and Email only).

---

## 2. Design Tokens & Visual Distribution

### Color Hierarchy (65 / 25 / 8 / 2 Balance)

| Token Name | Hex Value | Viewport Share | Semantic Role |
|---|---|---|---|
| `canvas-abyssal` | `#080A0F` | **65%** | Deep submerged obsidian slate canvas with a faint cool oceanic undertone. |
| `canvas-depth` | `#0E1420` | Ambient radial | Center ambient lighting beneath the hero portrait and active focus regions. |
| `surface-glass` | `rgba(14, 17, 24, 0.72)` | **25%** | Liquid frosted glass island nav, project viewport cards, reading panels. |
| `border-subtle` | `rgba(255, 255, 255, 0.08)` | Structural | 1px hairline structural rules, dividers, and card outlines. |
| `border-active` | `rgba(255, 255, 255, 0.22)` | State | Illuminated border on hover or focused states. |
| `text-primary` | `#EDEDEA` | **8%** | Warm titanium silver for headlines, titles, and high-emphasis reading. |
| `text-muted` | `#868994` | Supportive | Secondary metadata, labels, and paragraph body copy. |
| `accent-sheen` | `#FFFFFF` | **2%** | Specular liquid mercury and silver-chrome reflection inside the liquid ASCII ripple. |

---

## 3. Typography Hierarchy (Apple System)

| Level | Family | Desktop Size | Mobile Size | Line Height | Tracking | Weight |
|---|---|---|---|---|---|---|
| **Display Title (Hero Left)** | SF Pro Display | `clamp(3.0rem, 7vw, 6.5rem)` | `clamp(2.2rem, 8vw, 3.2rem)` | 0.95 | `-0.04em` | 800 (Heavy) |
| **Section Title** | SF Pro Display | `clamp(2.0rem, 4vw, 3.2rem)` | `1.85rem` | 1.1 | `-0.03em` | 700 (Bold) |
| **Card Header** | SF Pro Display | `1.5rem` (24px) | `1.25rem` (20px) | 1.2 | `-0.02em` | 600 (Semibold) |
| **Body Primary** | SF Pro Text | `1.0625rem` (17px) | `1.0rem` (16px) | 1.55 | `-0.01em` | 400 (Regular) |
| **Body Muted** | SF Pro Text | `0.9375rem` (15px) | `0.875rem` (14px) | 1.5 | `0em` | 400 (Regular) |
| **Monospace / ASCII** | SF Mono | `0.8125rem` (13px) | `0.75rem` (12px) | 1.4 | `+0.02em` | 500 (Medium) |

---

## 4. Canonical Motion Curves

* **Snappy Luxury (Primary Curve):** `cubic-bezier(0.16, 1, 0.3, 1)`  
  *Used for:* Nav bubble travel, hero reveal unmasking, card hover elevations, and page transitions.
* **Liquid Bubble Elasticity (Spirit Level):** `cubic-bezier(0.34, 1.56, 0.64, 1)`  
  *Used for:* Nav indicator bubble stretch and settle.
* **Subtle Settle:** `cubic-bezier(0.25, 1, 0.5, 1)`  
  *Used for:* Button active compressions, input states, and micro-interactions.

---

## 5. Component Specifications & State Architecture

### A. The Floating Nav Island (Liquid Glass Squircle)
* **Geometry:** Floating centered pill. Height: `48px`, Width: auto (inline-flex), `border-radius: 9999px`.
* **Position:** Fixed `top: 20px`, `z-index: 50`.
* **Material:** Background `rgba(14, 17, 24, 0.72)`, backdrop blur `20px`, border `1px solid rgba(255, 255, 255, 0.12)`.
* **The Spirit Level Bubble:**
  * Active indicator sits behind the active link.
  * Size: Matches active link dimensions with `8px` horizontal padding, height `34px`, `border-radius: 9999px`.
  * Material: `rgba(255, 255, 255, 0.12)` with interior highlight border `1px solid rgba(255, 255, 255, 0.35)`.
* **State Variants:**
  * Inactive Link: Text `#868994`. Hover brings color to `#EDEDEA` over `180ms`.
  * Active Link: Text `#EDEDEA`, font-weight 500.
  * Action Button (Let's Talk): Distinct pill on the far right with background `rgba(255, 255, 255, 0.10)`, hover background `rgba(255, 255, 255, 0.18)`.
* Transition: Stretches by `1.15x` horizontally during transit, snaps to resting pill over `380ms` via `cubic-bezier(0.34, 1.56, 0.64, 1)`.

### B. Interactive Buttons (Pill Geometry)
* **Rule:** `border-radius: 9999px` always.
* *Default:* `background: rgba(255, 255, 255, 0.06)`, `border: 1px solid rgba(255, 255, 255, 0.12)`, `color: #EDEDEA`.
* *Hover:* `background: rgba(255, 255, 255, 0.14)`, `border: 1px solid rgba(255, 255, 255, 0.50)`, scale `1.02x` over `220ms`.
* *Pressed:* Scale `0.97x`, background `rgba(255, 255, 255, 0.22)`.
* *Focus:* `outline: none`, `box-shadow: 0 0 0 2px #080A0F, 0 0 0 4px rgba(255, 255, 255, 0.8)`.

### C. Project Showcase Cards (Unified Chassis)
* **Geometry:** `border-radius: 24px`, padding `28px`, background `#0E1118`, border `1px solid rgba(255, 255, 255, 0.08)`.
* **Header Auto-Layout:**
  * Left: Project Name (SF Pro Display, 24px, `#EDEDEA`).
  * Right: Scope Pill (`[ Web Design ]`, `[ Copywriting ]`, `[ AI Automation ]`, `border-radius: 9999px`).
* **One-Line Proposition:** Placed directly under header in SF Pro Text ($15\text{px}$, `#868994`).
* **Viewport Frame:** 16:9 widescreen stage, `border-radius: 16px`, overflow hidden.
* **Hover State:** Border illuminates to `rgba(255, 255, 255, 0.22)`, card translates upward by `4px`, `[ View Case Study -> ]` pill reveals smoothly.
* **Click:** Directly navigates to standalone `/work/[slug]` subpage.

---

## 6. Section Architecture

### Section 01: The Hero Stage
* Centered monumental portrait with real-time Liquid ASCII Water Ripple.
* Split tension: Bold headline on the left, conversational human thesis on the right.
* 600ms fluid unmasking intro rising from depth with one settling ripple across the face.

### Section 02: The Hero-to-Projects Sticky Communicating Seam
* `250vh` pinned scroll runway. 
* Scrollbar directly scrubs the WebGL displacement shader: headline unmasks outward, portrait compresses with liquid tension, and the Selected Work Showcase glides upward from the depths.

### Section 03: What I Do (The 3 Core Services)
* Three bold modular blocks:
  1. **Web Design & Frontend** (Custom sites, landing pages, e-commerce, SEO, speed, ongoing management for existing sites).
  2. **Copywriting & Content** (Sales copy, offer positioning, brand articles, lifecycle email funnels).
  3. **AI Integration & Business Automation** (Custom AI tools, operational delivery automation, CRM routing, onboarding).

### Section 04: Selected Work Showcase
* Clean vertical stack of unified 16:9 cards linking to dedicated subpages.
* Bottom anchor pill: `[ View Complete Work Archive -> ]` linking to `/work`.

### Section 05: The Perspective / Essays
* Three editorial essays demonstrating commercial acumen, brand voice, and lean growth.

### Section 06: Grounded Large Type Negative Footer
* Bold callout: `HAVE A PROJECT IN MIND? LET'S TALK.`
* Direct email copy pill (`hello@yourdomain.com [COPY]`).
* Direct calendar booking trigger (`[ Book a 15-Minute Scoping Call -> ]`).
* Dense ASCII social icons for **X**, **LinkedIn**, and **GitHub** inside rounded squircle pills.
* High-density ASCII stippled landscape silhouette at the base with large negative typography blending into canvas.
* Strictly zero fake local time clocks. Strictly zero Telegram links.

---

## 7. Dedicated Subpages & Work Archive

### A. Dedicated Work Archive / Gallery (`/work`)
* Filter bar with spirit-level liquid pills: `[ All Projects ]`, `[ Web & Storefronts ]`, `[ Copywriting & Strategy ]`, `[ AI & Automation ]`.
* Smooth spring layout reorganization on filter switch without page reload.

### B. Dedicated Project Subpages (`/work/[slug]`)
* Top rail: `[ <- Back to Work Archive ]` + Project Title.
* Executive 4-column horizon for skimmers: Client, Year, Role, Key Outcome.
* High-resolution visual showcase (responsive frames, copy comparisons, or workflow schematics).
* Narrative architecture: The Problem, The Strategy & Words, The Technical Build, The Business Result.
* Bottom rail to glide to next case study or start a project.

---

## 8. Mobile Plan & Touch Physics

* Touch-driven liquid ASCII ripple on tap and finger drag across the portrait.
* Smooth 400ms surface tension snap-back on finger lift.
* Fluid typography scaling with CSS clamp formulas.
* Floating bottom thumb navigation with full-screen frosted glass overlay.
* Battery-conscious 50% ASCII grid density on mobile viewports to guarantee 60fps.


---

## 9. Interactive Easter Egg (Optional / Experimental): The X-Ray ASCII Mode Switch

* **Location:** A subtle, rounded pill trigger in the bottom corner or floating nav: `[ ASCII VIEW: OFF ]`.
* **The Interaction Physics:**
  * When clicked, a fast liquid mercury wave sweeps vertically across the viewport (under 500ms).
  * The entire interface temporarily transforms into pure computational ASCII art: photographic elements, card frames, and typography render as an animated, live monospace character matrix (`.`, `:`, `+`, `%`, `#`, `@`), exposing the raw mathematical wireframe of the site.
  * Clicking the trigger again (or auto-settling) sends an expanding circular silver ripple that restores the pristine photographic and design layout.
  * Serves as an unforgettable demonstration of creative coding and technical mastery for visiting founders and engineers.
