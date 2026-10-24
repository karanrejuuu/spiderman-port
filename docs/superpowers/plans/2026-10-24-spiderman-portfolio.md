# Karan Reju's Spider-Man Portfolio Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a complete, highly interactive, funny Spider-Man-themed web portfolio for Karan Reju showcasing his 5 real GitHub projects, tech stack, and interactive comic UI features.

**Architecture:** Single-page application with Three.js 3D rooftop skyline and scroll-driven web shooting, combined with an HTML5/CSS3 halftone comic layout, GSAP animations, Web Audio API sound effects, and interactive mode switching (Standard, Miles Morales Venom Blast, Symbiote Dark Mode).

**Tech Stack:** HTML5, CSS3, JavaScript (ES6+), Three.js (r128), GSAP 3.12, ScrollTrigger, Web Audio API, Canvas 2D.

**Spec:** `docs/superpowers/specs/2026-10-24-spiderman-portfolio-design.md`

## Global Constraints
- Target platform: Modern browsers (desktop & mobile) with responsive design.
- Complete fidelity to Karan Reju's real profile, GitHub projects, and contact channels.
- Self-contained audio synthesizer via Web Audio API (no external MP3/WAV dependencies that could 404).
- Seamless fallback when `prefers-reduced-motion` is enabled.

## Review Focus
1. Window resize events: WebGL canvas and 2D canvas must rescale smoothly without distortion.
2. Mobile touch support: Tap-to-fire web bursts and touch navigation must work without broken hover states.
3. Audio policy: Web Audio context must initialize only after user interaction to respect browser autoplay policies.
4. Mode switcher: Standard / Miles / Symbiote themes must transition colors and effects cleanly.
5. Project links: All 5 GitHub repos and the live Waymark PWA link must be clickable and open in new tabs securely (`rel="noopener"`).

---

### Task 1: Complete HTML5 Comic Structure & Content Integration
**Files:**
- Create: `index.html` (initial semantic skeleton & comic layouts)

- [ ] Add HTML5 head tags, Google Fonts (Bangers, Archivo, JetBrains Mono), meta tags for Karan Reju (Full-Stack & AI Engineer).
- [ ] Implement Comic Loader (`#loader`) with animated web fluid progress bar and witty Spider-Man loading statuses ("BREWING CHAI IN KOCHI...", "CALIBRATING WEB-SHOOTERS...", "SYNTHESIZING ML MODELS...").
- [ ] Build Comic Nav with Logo ("KARAN REJU // EARTH-616"), links to Rogues Gallery (Projects), Arsenal (Tech Stack), Daily Bugle (Testimonials), and Contact, plus Audio SFX Toggle and Mode Switcher.
- [ ] Build Hero Section with 3D text layers, badge ("NODE: KOCHI, KERALA // FULL-STACK & AI ENGINEER"), intro copy, and CTA buttons.
- [ ] Build Rogues Gallery (5 Project Cards for Waymark, CineCloud, LLM SQL Analyst, PawConnect, Credit Risk Model) with Issue badges, live links, and tech chips.
- [ ] Build Suit Tech Arsenal grid categorized into Frontend, Backend & Cloud, and AI & ML.
- [ ] Build The Daily Bugle section featuring J. Jonah Jameson comic headline clipping.
- [ ] Build Contact section with Spider-Signal CTA and social links (Email, WhatsApp, LinkedIn, GitHub, Instagram).

### Task 2: Advanced Comic Styling, Halftone & Theme Switcher CSS
**Files:**
- Modify: `index.html` (embedded `<style>` block)

- [ ] Implement CSS custom properties for comic palette: `--paper`, `--ink`, `--red`, `--blue`, `--yellow`, `--purple` (Miles electric), `--venom` (Symbiote dark mode).
- [ ] Create halftone dot background textures and comic paper borders (solid ink strokes, hard box shadows).
- [ ] Implement comic speech bubbles, folded paper corners, tilted badges, and J. Jonah Jameson newspaper front-page styling.
- [ ] Implement Mode Switcher themes: `.theme-classic`, `.theme-miles`, `.theme-symbiote` altering CSS variables for background, webs, and glow colors.
- [ ] Add Spidey-Sense danger aura animation (`@keyframes spideySense`) with comic warning squiggles.

### Task 3: Three.js 3D Rooftop City, Silhouette Hero & Scroll-Driven Web
**Files:**
- Modify: `index.html` (Three.js WebGL script)

- [ ] Set up Three.js perspective camera, scene fog, and window-lit building skyline with ink outlines.
- [ ] Construct the crouched Spider-Man silhouette perched on the foreground skyscraper corner facing across the skyline.
- [ ] Create the giant comic moon with halftone crater details behind the hero.
- [ ] Build dynamic CatmullRom 3D web curve extruded via `TubeGeometry` that extends progressively as the user scrolls.
- [ ] Add comic clouds floating across the skyline with subtle parallax drift.
- [ ] Add pointer-down raycasting to shoot instant 3D web projectiles from Spider-Man's hand toward the user's cursor click position.

### Task 4: Interactive Sound Synthesizer (Web Audio API) & Click Bursts
**Files:**
- Modify: `index.html` (Audio & DOM FX scripts)

- [ ] Create Web Audio API oscillator synth:
  - `playThwipSound()`: Frequency sweep (1200Hz -> 300Hz) with bandpass filter for the classic Spider-Man web-shooter sound.
  - `playPunchSound()`: Low-frequency noise burst for comic hit impacts.
- [ ] Add Mute/Unmute audio toggle button in the navigation bar.
- [ ] Implement click-activated comic bursts (`THWIP!`, `POW!`, `DEBUGGED!`, `KAPOW!`, `DEPLOY!`, `404 SOLVED!`) with SVG comic explosion stars and 2D canvas web splatters.
- [ ] Add 2D canvas mouse web trail with spring-like strand physics following the cursor.

### Task 5: Suit AI Quips, Mode Switching Logic & GSAP Scroll Interactions
**Files:**
- Modify: `index.html` (Interaction & animation script)

- [ ] Implement Suit AI (Karen HUD) status bar with randomized witty developer quips updated on scroll or interval.
- [ ] Hook up the Mode Switcher (Standard, Miles Morales Shock, Symbiote Venom) to update Three.js web colors, canvas trail colors, and root theme class.
- [ ] Configure GSAP ScrollTrigger for 3D card tilt on mousemove, text scramble on hero badges, and smooth skew on scroll.
- [ ] Verify responsive behavior on mobile/tablet viewports and test `prefers-reduced-motion` compliance.
