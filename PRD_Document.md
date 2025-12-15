# Product Requirements Document (PRD)  
**Hackathon Project: Personal Portfolio Website**  
**Platform:** GitHub Pages (Jekyll / Academic Pages)  
**Site Type:** Fully static, design-led portfolio

---

## 1. Objective

Build a **static personal portfolio website** adapted from the Academic Pages Jekyll repository, where **styling, interaction design, and visual identity are the primary product**, and content is structured to support that experience.

The site should communicate:
- A curious, eager learning mindset  
- Strong UX and visual design sensitivity  
- Professionalism without stiffness  
- Playfulness without gimmicks  

The portfolio is intentionally selective. It should feel **crafted, calm, and enjoyable to explore**, while remaining academically credible and technically disciplined.

---

## 2. Scope

### In Scope
- Forking and adapting `academicpages.github.io`
- Local development with Jekyll
- Deep SCSS customization (colors, typography, spacing, motion)
- Layout and component-level HTML/Liquid changes
- CSS-only interactions and micro-animations
- Static pages for:
  - Hero landing
  - About
  - CV (tri-modal)
  - Interactive paper and/or project

### Explicitly Out of Scope
- Backend or server logic
- User authentication or accounts
- Databases or APIs
- JavaScript frameworks or animation libraries
- CMS integrations
- Academic publication listings as the main focus
- Content-heavy blogging

---

## 3. Technical Stack & Constraints

### Stack
- **Static Site Generator:** Jekyll  
- **Base Theme:** Academic Pages  
- **Hosting:** GitHub Pages  
- **Markup:** Markdown, HTML (Liquid templates)  
- **Styling:** SCSS (compiled by Jekyll)  
- **Assets:** Local fonts, images, SVGs, AI-generated placeholders  

### Constraints (Hard Rules)
- SCSS is the only styling and interaction layer  
- No JavaScript frameworks or animation libraries  
- No changes that break GitHub Pages compatibility  
- No restructuring of core Jekyll architecture  
- Reuse existing layouts and includes where possible  

---

## 4. Design Foundation (Primary Focus)

The **visual system and interaction language** are the foundation of the portfolio.  
All milestones, pages, and content types must be implemented **through this lens first**.

Design decisions are evaluated in this order:
1. Visual clarity  
2. Interaction quality  
3. Emotional tone  
4. Technical simplicity  

---

## 5. Design Style Reference & Extracted Keywords

### Reference Inspiration
- https://labelbox.com/  
- https://cohere.com/solutions/technology  
- https://www.reactbits.dev (Bubble Menu, Pill Nav patterns)

### Extracted Design Keywords

**Tone**
- Calm  
- Confident  
- Human  
- Forward-looking  

**Visual Language**
- Soft but precise  
- Muted foundations with expressive accents  
- Spacious layouts  
- Controlled asymmetry  
- Subtle depth and layering  

**Interaction Language**
- Gentle  
- Discoverable  
- Responsive  
- Non-intrusive  
- Micro-interaction driven  

---

## 6. Color System & Atmosphere

### Base Palette
- Soft off-whites for backgrounds  
- Desaturated blues and purples for large surfaces  
- Dark navy or charcoal instead of pure black  

### Accent Colors
- **Warm orange-red** for energy and emphasis  
- **Brighter wine-red** for focus states and calls-to-action  

### Usage Principles
- Base colors establish calm and structure  
- Accent colors are used sparingly and intentionally  
- Accents appear mainly in:
  - Hover states  
  - Active navigation  
  - Key interaction feedback  

---

## 7. Typography System

### Fonts
- **Headlines:** The Future (Klim)  
- **Accent / UI / Navigation:** Space Grotesk  
- **Body Text:** Work Sans  

### Font Asset Requirement
- Font files must be provided (`.woff` / `.woff2`)
- Stored under `/assets/fonts/`
- Declared via `@font-face` in SCSS
- Loaded locally (no CDNs)

### Typographic Principles
- Clear hierarchy  
- Generous spacing  
- Editorial feel  
- Typography carries more personality than color  

---

## 8. Layout & Interaction Principles

- Strong vertical rhythm  
- Section-based storytelling  
- Visually re-designed lists (no default bullets)  
- Pill / bubble inspired navigation elements  
- CSS-only motion:
  - Hover reveals  
  - Subtle transforms  
  - Sticky sections  
  - Progressive disclosure  

---

## 9. Hackathon Milestones — What To Do

This section defines **exactly what must be implemented** for each milestone, and **how to achieve it efficiently**, without breaking the design system.

---

### Milestone 4 — Custom Theme

#### What Must Be Done
- Implement a **custom theme option** alongside existing light/dark themes
- Theme must reflect your personal UX brand
- Theme icon hover reveals three options:
  - Light (keep as is)
  - Dark (keep as is)
  - Custom (this one needs to be created)

#### How to Do It Efficiently
- Override theme colors and fonts via SCSS variables
- Avoid touching JavaScript
- Focus changes on:
  - Backgrounds
  - Typography
  - Accent color usage
- Reuse Academic Pages theme-switching logic

**Design Focus**
- Muted base
- Expressive accents
- Calm, modern feel

**Tag:** `Theme done`

---

### Milestone 5 — Personalized Hero Landing Page

#### What Must Be Done
- Create a hero section with:
  - Tagline / welcome message
  - Profile picture or AI-generated hero image
  - Quick access links to key sections

#### How to Do It Efficiently
- Modify the existing home layout
- Use large headline typography (The Future)
- Implement quick-access links via anchor scrolling
- Add subtle hover and focus interactions

**Design Focus**
- First-impression clarity
- Strong hierarchy
- Visual calm with personality

**Tag:** `Hero done`

---

### Milestone 6 — Accessible CV (Tri-Modal)

#### What Must Be Done
Create one CV experience with three modes:
1. **Text-based CV** (semantic, readable)
2. **Visual CV** (timeline / infographic)
3. **Audio-based CV** (embedded audio)

#### How to Do It Efficiently
- Single CV page with stacked or toggleable sections
- Visual CV:
  - Vertical timeline using CSS
- Audio CV:
  - Native HTML `<audio>` element
- Use CSS to reveal or switch modes

**Design Focus**
- Accessibility
- Multiple learning styles
- Interaction over decoration

**Tag:** `CV done`

---

### Milestone 7 — Interactive Paper Page

#### What Must Be Done
Include at least one paper with:
- Title
- Authors
- Citation
- Abstract
- Method
- Results
- Image / diagram
- PDF download
- At least one interactive element

#### How to Do It Efficiently
- Single dedicated page
- Structure content in collapsible sections
- Add interaction via:
  - Hover image swaps
  - Click-to-reveal sections
- PDF can be a placeholder

**Design Focus**
- Structured reading
- Progressive disclosure
- Calm academic tone with interaction

**Tag:** `<Paper> done`

---

### Milestone 8 — Interactive Project Page

#### What Must Be Done
Include one UX project with:
- Title
- Authors
- Institution / client
- Problem statement
- Method
- Outcomes
- Media (image / video / animation)
- PDF download
- Interactive content reveal

#### How to Do It Efficiently
- Adapt structure from existing interactive documentation
- Simplify interaction logic
- Rebuild interactions using:
  - CSS hover states
  - Scroll-based layout changes
  - Progressive content reveal

**Design Focus**
- Storytelling
- Clarity of process
- Interaction supports understanding

**Tag:** `<Project> done`

---

## 10. Acceptance Criteria (Design-Led)

The project is complete when:
- All milestones are implemented and tagged
- The site is clearly distinguishable from default Academic Pages
- Styling and interaction feel intentional and cohesive
- Typography, color, spacing, and motion work together
- The site remains fully static and accessible
- No build or deployment errors occur

---

## 11. Definition of Done

A static portfolio website that:
- Is design-led rather than template-led  
- Uses interaction as a communication tool  
- Balances playfulness with academic professionalism  
- Can grow without redesigning the foundation  
- Reflects UX sensibility more than feature count  
