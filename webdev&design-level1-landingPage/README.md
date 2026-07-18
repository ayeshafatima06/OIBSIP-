# Task 1 · Meridian — Coffee Landing Page

A single-page static landing page for **Meridian**, a fictional single-origin coffee brand sold by growing altitude. Built to demonstrate foundational, production-quality HTML/CSS layout skills — no JavaScript required.

## File

- `index.html` — the entire site (HTML + embedded CSS in one file)

## Concept

Most coffee brands lead with roast or blend name. Meridian's hook is **altitude**: every bag is sold by the exact elevation (in meters) the beans were grown at. That idea drives the whole design — a topographic contour-line illustration in the hero, an animated "elevation pin" showing a real coordinate, and origin cards that lead with altitude instead of price.

## Sections

| Section | What it contains |
|---|---|
| **Nav** | Sticky/fixed navbar with 4 links (Origins, Process, Reviews, Subscribe) |
| **Hero** | Headline, subheadline, primary + secondary CTA, topographic SVG illustration, stat bar (farm partners, elevation range, shipping time, traceability) |
| **Origins** | 3 origin cards (Ethiopia, Colombia, Burundi) each with altitude, tasting notes, and flavor tags |
| **Process** | 5-stage journey (Harvest → Process → Dry → Roast → Ship) connected by a rising SVG line |
| **Testimonials** | 3 customer quotes with avatar initials |
| **CTA band** | Secondary conversion prompt before the footer |
| **Footer** | Brand blurb, sitemap columns, contact email/phone, social link placeholders |

## Design system

- **Palette:** deep pine (`#1B211D`), parchment (`#EFE9DC`), roast brown (`#8A6A45`), moss green (`#4C6444`), gold accent (`#C9A356`) — used consistently across every section
- **Typography:** Fraunces (display/headings), Inter (body text), IBM Plex Mono (data — altitude figures, labels, eyebrows) — two clear font sizes/weights distinguish headings from body copy
- **Layout:** CSS Grid for section layouts and card grids, Flexbox for nav/rows; `box-sizing: border-box` applied globally so padding/margin never cause overlap

## Responsiveness

Two breakpoints:
- `900px` — grids collapse from 3 → 2 columns, hero stacks to a single column
- `640px` — nav collapses into a toggle menu, all grids go full-width single column, section padding shrinks

## How to run

No build step needed. Just open `index.html` in any browser, or use VS Code's **Live Server** extension for auto-reload while editing.

## Checklist coverage

- [x] Sticky nav with 4 links
- [x] Hero with headline, subheadline, CTA
- [x] 3 distinct content sections (Origins, Process, Testimonials)
- [x] Footer with contact/social placeholders
- [x] Consistent color palette
- [x] Responsive Grid/Flexbox layout
- [x] No element overlap (global `box-sizing: border-box`)
- [x] Clear typographic hierarchy (display, body, mono/data sizes)