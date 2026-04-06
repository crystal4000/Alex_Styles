# Alex Styles — Graphic Designer Portfolio

### UI/UX Design Principles | Coursera Final Project

---

## Project Overview

This project is a fully responsive, interactive portfolio website built for **Alex Styles**, a fictional graphic designer. The goal was to apply UI/UX design principles to create a professional, client-facing website that communicates Alex's brand identity, showcases creative work, and makes it easy for potential clients to get in touch.

The project was completed across three activities, each building on the last.

---

## Project Structure

```
alex-styles-portfolio/
├── index.html       # Main HTML structure
├── styles.css       # All CSS styles (external stylesheet)
└── README.md        # Project documentation
```

---

## Activity Breakdown

### Activity 1 — CSS Foundation

The focus here was setting up the visual design system and writing the core CSS.

**What was built:**

- Full HTML structure with four sections: Hero, About Me, Portfolio, and Contact
- External stylesheet (`styles.css`) linked to `index.html`
- CSS custom properties (design tokens) for colors, typography, spacing, and transitions — all defined in `:root` so the entire site can be updated from one place
- Typography using **Cormorant Garamond** (display serif) and **Jost** (body sans-serif), loaded from Google Fonts
- A warm editorial color palette: cream background (`#F7F3EE`), deep ink (`#1C1917`), terracotta accent (`#C8553D`), and muted gold (`#B8963E`)
- CSS Grid layouts for the Hero, About, Portfolio, and Contact sections
- Flexbox for navigation, buttons, skill tags, and form rows
- Hover transitions on buttons, nav links, cards, and skill tags
- Six keyframe animations: `fadeUp`, `fadeIn`, `slideLeft`, `cardReveal` (with staggered delays), `pulseRing`, and `float`
- Scroll-triggered reveal animation using `IntersectionObserver`
- Portfolio card overlays that fade in and slide up on hover
- Unsplash images used for all project thumbnails and profile photos

**CSS techniques applied:**

- `clamp()` for fluid type scaling without breakpoints
- CSS Grid with `grid-template-columns`, `grid-column: span`, and `grid-row: span`
- `backdrop-filter` for the frosted glass navigation bar
- `linear-gradient` and `radial-gradient` for atmospheric background effects
- `transform` and `opacity` only animations for GPU-composited performance

---

### Activity 2 — Responsive Design

The focus here was making the site fully functional across all screen sizes.

**What was built:**

- Media query at `max-width: 1024px` (tablet) — hero stacks to a single column, portfolio grid adjusts to two columns, contact grid collapses
- Media query at `max-width: 768px` (mobile) — navigation links hidden, portfolio grid goes to one column, form row stacks vertically, spacing tokens reduced
- Fluid font sizes using `clamp()` that scale continuously between breakpoints, reducing the need for extra media queries
- The contact form reorganizes to a single-column layout on mobile for easier input
- Flexible Flexbox alignment that reflows naturally at smaller widths
- Portfolio header stacks vertically on mobile

**Breakpoints used:**

| Breakpoint          | Target                   |
| ------------------- | ------------------------ |
| `min-width: 1025px` | Desktop (default styles) |
| `max-width: 1024px` | Tablet                   |
| `max-width: 768px`  | Mobile                   |

---

### Activity 3 — Interactivity & UI/UX Enhancements

The focus here was adding interactive features and refining the overall user experience.

**What was built:**

**Portfolio Modal**

- Clicking any project card opens a full detail overlay
- Modal displays the project image, category, client, year, role, full description, and tags
- Closes on the X button, clicking the backdrop, or pressing `Escape`
- Smooth scale + translateY entrance animation
- Body scroll is locked while the modal is open

**Navigation Tooltips**

- Hovering over About, Work, and Contact nav links reveals a small tooltip below
- Tooltips use `attr(data-tooltip)` pulled directly from the HTML — no JavaScript needed
- Animated with `opacity` and `translateY` for a clean slide-in effect

**Filter Tabs (functional)**

- Portfolio filter buttons now actually show and hide cards by category
- Clicking "Branding" shows only branding cards, etc.

**Active Nav State**

- As the user scrolls through sections, the matching nav link highlights in the accent color
- Driven by `IntersectionObserver` and scroll event listener

**Typography refinements**

- Tighter `letter-spacing` on section titles for a more editorial feel
- Improved `line-height` on body copy for readability
- Stat numbers use a gradient fill from terracotta to warm gold for visual differentiation

**Visual hierarchy improvements**

- Skill tags show a left border accent on hover for added depth
- About section decorative frame becomes more prominent on hover
- Portfolio card gradient overlay is more directional for better text legibility over images

---

## Design Decisions

**Color Palette**
The warm cream and terracotta combination was chosen to feel premium without being cold. Most design portfolios default to white and black — the warmth here makes the site feel more personal and human, which fits a creative freelancer's brand.

**Typography**
Cormorant Garamond was chosen for headings because it has personality — it's a distinctive editorial serif that feels high-end without being stiff. Jost pairs well as a clean, geometric sans-serif for body copy and UI text. This combination avoids the overused Inter/Roboto defaults.

**Layout**
The hero uses an asymmetric two-column grid (1.1fr / 0.9fr) to give the text slightly more room than the image, which feels more editorial than a perfect 50/50 split. The portfolio grid uses a featured first card (spanning two columns) to create visual hierarchy and lead the eye.

**Animation**
Animations are intentional and minimal — they support the content rather than distract from it. Card reveals use staggered delays so the grid feels like it's being laid out in sequence, not all popping in at once.

---

## Tools & Technologies

| Tool                | Purpose                                            |
| ------------------- | -------------------------------------------------- |
| HTML5               | Semantic page structure                            |
| CSS3                | Styling, layout, animations                        |
| Vanilla JavaScript  | Modal, scroll reveal, filters, form feedback       |
| Google Fonts        | Cormorant Garamond + Jost typefaces                |
| Unsplash            | External image links for all photos                |
| Copilot (Microsoft) | AI-assisted code generation and design suggestions |

---

## How Copilot Assisted This Project

Copilot was used throughout all three activities as an AI development partner:

- **Activity 1** — Generated the full HTML structure and CSS foundation including the design token system, grid layouts, keyframe animations, and hover interactions based on the design brief.
- **Activity 2** — Identified which breakpoints to use, suggested fluid `clamp()` typography as an alternative to multiple font-size media queries, and restructured grid layouts for each screen size.
- **Activity 3** — Generated the modal component including the JavaScript data layer, CSS tooltip pattern using `attr()`, the filter tab logic, and the active nav scroll tracking. Also suggested typography and visual hierarchy refinements.

Using Copilot accelerated development significantly — complex CSS patterns like the staggered card animations, backdrop-filter nav, and modal entrance animation were generated and explained in context, making it easier to understand the reasoning behind each technique and adapt them to the project's specific needs.

---

## How to Run

No build tools or dependencies required.

1. Download `index.html` and `styles.css` into the same folder
2. Open `index.html` in any modern browser
3. Both files must be in the same directory for the stylesheet to load correctly

---

_Submitted as the final project for the UI/UX Design Principles course on Coursera._
