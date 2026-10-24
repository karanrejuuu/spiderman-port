# Design Specification: Karan Reju's Spider-Man Themed Interactive Portfolio

**Date:** 2026-10-24  
**Author:** Antigravity  
**Subject:** Interactive, Funny Spider-Man Themed Web Portfolio for Karan Reju  

---

## 1. Intent & The "Why"
Create a high-energy, memorable, and humorous Marvel/Spider-Man comic-book-themed portfolio for **Karan Reju**, a Full-Stack & AI Engineer based in Kochi, India. The site bridges high-end web development with comic book aesthetics, combining Three.js 3D graphics, physics-inspired web mechanics, comic sound FX (Web Audio API), and J. Jonah Jameson-style humor to present Karan's technical arsenal and 5 real-world GitHub projects.

---

## 2. Goals & Non-Goals

### Goals
- **High Visual Punch:** Maintain the vintage halftone comic texture, Bangers headline typography, and Three.js 3D city rooftop with Spider-Man silhouette.
- **Accurate Real Projects:** Showcase Karan's 5 GitHub projects with accurate descriptions, live links (Waymark), and tech badges:
  1. **Waymark** (Offline-First FMCG PWA / TypeScript)
  2. **CineCloud** (Movie Ticket Platform / Go, SQLite, AWS EC2 & SES)
  3. **LLM SQL Analyst** (Natural Language to SQL Engine / Python & Streamlit)
  4. **PawConnect** (Stray Rescue & Adoption Platform / Next.js 14, Express, PostgreSQL)
  5. **Credit Risk Model** (Financial Loan Default Prediction ML / Python, Scikit-Learn)
- **Funny, Heroic Storytelling:**
  - Tagline: *"Your Friendly Neighborhood Full-Stack & AI Engineer"*.
  - Location: *Node: Kochi, Kerala // Earth-616*.
  - Daily Bugle headlines featuring J. Jonah Jameson yelling about Karan solving bugs too fast.
  - Rogues Gallery framing real engineering problems (e.g., "The Manual FMCG Chaos", "The Black-Box SQL Monster", "The Stray Rescue Disconnect").
- **Innovative Interactive Features:**
  - **Spidey-Sense Cursor:** Wavy comic danger arcs tingling near buttons or easter eggs.
  - **Web Shooter Fluid Switcher:** Standard Web, Miles Morales Venom Blast (shocking electricity), and Symbiote Dark Mode.
  - **Suit AI (Karen HUD):** Live quips in the HUD giving funny telemetry status updates.
  - **Click-to-Shoot Web Bursts:** Comic bursts (`THWIP!`, `POW!`, `DEBUGGED!`, `KAPOW!`, `DEPLOY!`) + 3D web strands + 2D web splatters.
  - **Web Audio FX Synthesizer:** Built-in retro comic sound effects (web thwip, punch kapow) with an easy Mute/Unmute toggle.
  - **Self-Contained Single File Deployment:** Zero complicated server dependencies, runs directly in browser with high performance.

### Non-Goals
- Generic boring corporate CV format.
- Heavy external sound assets that fail or take time to buffer (using Web Audio API synth oscillators instead).
- Fictional or non-existent work metrics; using witty developer/comic metrics (e.g. "5+ Missions Shipped", "4+ Core Languages", "0 Production Villains").

---

## 3. The Superhero Lore & Content

### Alter-Ego Profile
- **Name:** Karan Reju
- **Base of Operations:** Kochi, Kerala, India (Earth-616)
- **Codename / Tagline:** Full-Stack & AI Engineer · Web-Slinger
- **Bio:** "Bitten by a radioactive compiler in Kochi. By day, building high-resilience systems with Go, TypeScript, Next.js, and ML models; by night, slinging web code and automating complex workflows so businesses never miss a beat."

### Key Stats
- **05+** Core Missions Deployed
- **04** Languages Mastered (Go · TypeScript · Python · SQL)
- **99.9%** Web-Fluid / Uptime Efficiency
- **0** Unhandled Exceptions in Kochi

### Tech Arsenal (Suit Gadgets)
- **Frontend & Web:** Next.js 14, TypeScript, React, Tailwind CSS, PWA, Three.js, GSAP
- **Backend & Cloud:** Go (Golang), Express.js / Node.js, PostgreSQL, SQLite, AWS (EC2, SES)
- **AI & Data Science:** LLM SQL Generation, Streamlit, Machine Learning (Scikit-learn, Random Forest, SMOTE), Pandas

### The 5 Missions (Rogues Gallery)
1. **Waymark** — *Issue #01: "The Vanishing Stock Crisis"*
   - Offline-first FMCG delivery reminder PWA with zero-navigation daily due lists and self-correcting restock intervals.
   - Stack: TypeScript, PWA, Tailwind CSS
   - Links: GitHub Repo, Live App
2. **CineCloud** — *Issue #02: "The Box Office Rush"*
   - Full ticket reservation architecture in Go & SQLite with AWS SES automated PDF tickets and QR verification.
   - Stack: Go (Golang), SQLite, AWS EC2, AWS SES
   - Link: GitHub Repo
3. **LLM SQL Analyst** — *Issue #03: "The Black-Box Database"*
   - Zero-schema restriction natural language data analyst turning user English queries into executed SQL and visual results.
   - Stack: Python, Streamlit, LLMs, SQL
   - Link: GitHub Repo
4. **PawConnect** — *Issue #04: "The Stray Rescuer's Call"*
   - Full-stack rescue, adoption, and verified donation platform connecting stray dogs with NGOs and volunteers.
   - Stack: Next.js 14 (App Router), Express.js, PostgreSQL, TypeScript
   - Link: GitHub Repo
5. **Credit Risk Model** — *Issue #05: "The Default Domino"*
   - End-to-end financial ML classification pipeline detecting high-risk loan default with SMOTE imbalance handling.
   - Stack: Python, Scikit-learn, Random Forest, Jupyter
   - Link: GitHub Repo

### The Daily Bugle (J. Jonah Jameson Testimonial Section)
- *"HE'S A MENACE! HE AUTOMATED OUR ENTIRE PIPELINE IN GO AND BUILT A PWA BEFORE LUNCH!"* — J. Jonah Jameson, Editor-in-Chief.
- Comic clipping design with halftone printing, news ticker, and interactive stamp.

### Spider-Signal Contact
- **Email:** karanreju@gmail.com
- **WhatsApp:** +91 7356547600
- **LinkedIn:** https://www.linkedin.com/in/karanreju/
- **GitHub:** https://github.com/karanrejuuu/
- **Instagram:** https://www.instagram.com/karanreju

---

## 4. Architecture & Technical Design

### File Structure
- `index.html`: Complete, high-performance, single-file experience containing:
  - Responsive HTML5 with comic typography and semantic layout.
  - Custom CSS styling (halftone SVG patterns, 3D CSS transforms, Bangers + JetBrains Mono fonts, comic cards).
  - Three.js 3D WebGL Canvas (`#gl`): 3D city skyline, rooftop perch, crouched silhouette hero, CatmullRom web strand dynamically extruded on scroll, dynamic camera spline tracking.
  - 2D Canvas Web Trail (`#webTrail`): Physics-based rope trail behind cursor.
  - Web Audio API Sound Synthesizer: Synthesizes retro comic sound effects on click (`thwip` frequency ramp, comic punch).
  - GSAP + ScrollTrigger: Smooth scroll animations, comic balloon pop-ins, text scramble, and 3D card tilts.
  - Interactive Mode Switcher: Standard Web / Miles Shock / Symbiote Dark Mode.

---

## 5. Verification & Testing Criteria
1. **Three.js Scene:** Runs at smooth 60fps, handles window resizing without distortion, gracefully degrades with `prefers-reduced-motion`.
2. **Project Accuracy:** All 5 repos linked with correct URLs, descriptions, and tech stacks.
3. **Interactive Features:** Web shooting on click, comic sound toggle, sound synthesis working without errors, mode switcher toggling visuals seamlessly.
4. **Responsive:** Flawless layout on desktop, tablet, and mobile devices.
