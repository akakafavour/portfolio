# Digital Portfolio: Product Designer & Growth Marketer
**Architecture & Execution Blueprint**  
**Design Standard:** Atelier Creative Studio Laws (Zero Generic AI Slop, Zero Canned Templates)

---

## Overview

This repository houses the complete design system, copy suite, and engineering specification for an independent, award-winning digital portfolio. It is engineered specifically for a **Product Designer & Growth Marketer** who bridges digital product design, conversion copywriting, acquisition funnels, and operational AI automation.

The visual direction combines **monumental Geist typography**, a centered portrait featuring an interactive **Liquid ASCII Water Ripple shader**, a **pinned hero with a rounded horizontal work runway sliding on top**, a **liquid Dynamic Island nav** with center-to-edge blur spread and proximity expansion, **expandable architectural service drawers**, a **moving brand strip**, an **About Me section with kinetic running marquee**, and a **grounded large-type negative footer** with dense ASCII social matrices.

---

## Master Blueprint Files

| File | Purpose & Contents |
|---|---|
| **[`DESIGN.md`](./DESIGN.md)** | **Single Source of Truth Design System:** Exact color tokens (65% Abyssal Black `#07080A`, 25% Graphite Glass, 8% Pure White `#FFFFFF`, <2% Electric Acid Lime `#D4FF00`), Geist typography hierarchy, canonical motion curves, component state variants, GLSL liquid displacement physics, horizontal pinned scroll runway, mobile touch plan, and X-Ray ASCII mode switch. |
| **[`COPY.md`](./COPY.md)** | **Verbatim Master Copy Suite:** Complete, human, outcome-focused copy for all sections (Nav, Hero, Selected Work, Brand Strip, Service Drawers, About Me, Footer, Subpages). Zero em-dashes, zero corporate buzzwords. |
| **[`AGENT_BUILD_SPEC.md`](./AGENT_BUILD_SPEC.md)** | **Implementation Engine Blueprint:** Complete technical guide for any AI agent or engineer. Covers Next.js / Vite stack recommendation, directory structure, 8-phase build order, shader setup, GSAP scroll runway, and verification QA gates. |

---

## Whole-Site Architecture at a Glance

```
[01. The Hero Stage]
Left: Heavy bold headline `PRODUCT DESIGNER. GROWTH MARKETER.`
Center: Monumental side-profile portrait with real-time Liquid ASCII Water Ripple
Right: Human conversational pitch with Acid Lime chromatic word highlights
Top Anchor: Apple Dynamic Island nav drops from top center, liquid blur spreads center-to-edge

                      ↓ (User scrolls down)

[02. Selected Work: Pinned Horizontal Runway]
Hero pins in place. The Selected Work stage (with deep rounded corners `rounded-t-[36px]`) 
slides upward directly ON TOP of the pinned hero. Once covering the screen, the container locks 
and its inner 16:9 cards scrub HORIZONTALLY from right to left across the screen.
Scrolling back up perfectly reverses the sequence back to the Hero.

                      ↓ (Vertical scroll resumes)

[03. The Moving Brand Strip]
Infinite, smooth horizontal marquee of client logos in monochromatic silver.

                      ↓

[04. Services: Expandable Architectural Drawers]
Three full-width interactive rows with wireframe outline numbers (01, 02, 03). 
Clicking a row expands downward with an illuminated Acid Lime border to reveal 
the problem/solution pitch and numbered deliverable index.

                      ↓

[05. The About Me Section]
Hairline pill badge `[ About Me ]` • Running kinetic background marquee `about · about · about` •
Candid workspace visual with signature watermark • Hybrid edge conviction copy + numeric proof chips

                      ↓

[06. Grounded Large Type Negative Footer]
Big bold callout `HAVE A PROJECT IN MIND? LET'S TALK.` • One-click email copy pill • 
Direct scoping call trigger • Dense ASCII social icons (X, LinkedIn, GitHub) • 
Base ASCII landscape silhouette with giant negative typography

[07. Optional Easter Egg: X-Ray ASCII Mode]
Floating pill toggle `[ ASCII VIEW: OFF / ON ]` • Sweeps a 500ms liquid mercury wave to reveal full wireframe ASCII matrix
```

---

## Photography Brief for Client Asset

Before launching the build, shoot the hero profile portrait according to this brief:
* **Framing:** 90-degree side profile or 3/4 side profile looking slightly forward, centered.
* **Lighting:** High-contrast rim/key lighting from the side or slightly behind. Deep shadows across the far side of the face with sharp highlight along the profile silhouette.
* **Wardrobe:** Solid dark crewneck, high-collar jacket, or dark hood. Zero logos or bright patterns.
* **Backdrop:** Solid dark charcoal or matte black backdrop. The background feathers seamlessly into `#07080A`.
* **Destination Path:** Save the image to `public/assets/portrait.png`.

---

## How to Start the Build

When you are ready to transition from Planning Mode to Execution Mode, instruct the agent:

```bash
"Read AGENT_BUILD_SPEC.md, DESIGN.md, and COPY.md, and execute Phase 1 through Phase 8 to build the portfolio."
```
