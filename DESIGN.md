---
name: "Portfolio | Nguyễn Viết Tâm"
description: "A distinct, multi-page personal portfolio for an IT student."
colors:
  night: "#111111"
  red: "#f34252"
  paper: "#f2ecdf"
  muted: "#aaa59b"
  line: "#494541"
  media: "#d7d0c3"
typography:
  display:
    fontFamily: "Kalam, cursive"
    fontSize: "clamp(52px, 8vw, 100px)"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "-0.025em"
  body:
    fontFamily: "Arial, Helvetica, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
  navigation:
    fontFamily: "Arial, Helvetica, sans-serif"
    fontSize: "clamp(16px, 1.8vw, 22px)"
    fontWeight: 400
    lineHeight: 1.35
---

# Design System: Personal Portfolio

## Overview

**Creative North Star: "A handwritten field index"**

The homepage acts as a personal index: six editorial rows lead to separate pages for the student's introduction, skills, education, devices, project, and contact details. A charcoal ground, vivid coral-red lettering, hand-drawn Kalam display type, dotted leaders, and Roman numerals make the navigation feel authored without turning it into a static résumé.

The inner pages keep that visual language while giving each subject room for real detail. Body copy and navigation remain in a familiar sans-serif for easy reading. Thin rules organize content; there are no repeated cards, decorative icons, or invented biography.

## Colors

### Primary
- **Night** (`--night`, `#111111`): Main background.
- **Coral Red** (`--red`, `#f34252`): Display type, active navigation, status labels, focus rings, and the index leaders.
- **Paper** (`--paper`, `#f2ecdf`): Main text and high-contrast type on the media placeholder.

### Supporting
- **Muted** (`--muted`, `#aaa59b`): Supporting copy, breadcrumbs, and metadata.
- **Line** (`--line`, `#494541`): Subtle structural dividers.
- **Media** (`--media`, `#d7d0c3`): Neutral placeholder surface for owner-supplied images.

## Typography

**Display:** Self-hosted Kalam, with Latin and Latin-Extended Vietnamese subsets.  
**Body and navigation:** Arial, Helvetica, sans-serif.  
**Editorial accent:** Georgia, "Times New Roman", serif.

Kalam is local and licensed under the SIL Open Font License in `fonts/OFL.txt`; no font is fetched from a third-party service. It is reserved for the name, page headings, and project title. Body copy and navigation use a consistent sans-serif so the handwritten voice does not impede comprehension.

## Layout

The home index uses a centered maximum-width column. Its desktop opening places a large two-line name opposite a concise introduction; the numbered list follows immediately. At widths below `700px`, the opening stacks and the list remains a single readable column.

Detail pages share a centered `1120px` maximum-width main column and a compact top bar. Breadcrumb, expressive page title, brief lead, open content section, and previous/home navigation form a consistent reading path. Fact grids collapse to one column and row descriptions stack below `700px`. The header navigation wraps below `420px`.

The dotted leader fills the space between each index title and its Roman numeral. Links rise slightly on hover and keyboard focus; the interaction is disabled for visitors who request reduced motion. No horizontal scrolling is required at narrow viewport widths.

## Components

### Home index
- A minimal folio-style header identifies the owner and school year.
- The hero pairs “Nguyễn Viết Tâm” with an editable student introduction; the header identifies the portfolio year as 2026.
- Six real internal links open separate HTML pages; Roman numerals make the sequence scannable.
- A featured-project row leads directly to the project detail page.

### Detail-page frame
- Shared top navigation links back to the home page and commonly visited pages.
- Breadcrumbs identify the current section.
- A Kalam heading leads into each page's factual placeholder content.
- A bottom navigation link returns home and, where useful, advances to the next section.

### Evidence and media
- Skills and devices use open ruled facts; the device page gives the iPhone 16 Plus and Redmi Book Pro 14S separate image slots, proportioned for phone and laptop photography. Education and project information use definition lists.
- Supplied skills, education details, devices, and project title receive modest emphasis through brighter text within the existing ruled layout, not cards or added decoration.
- The project page is a small case-study template for owner-written details, with the working title “Chatbot AI của Trường Đại học Đại Nam”.
- Its longer project heading uses a smaller responsive size than the other page titles so it stays expressive without dominating the detail page.
- Device and project image examples keep `src=""` inside commented markup beside prominent Vietnamese instructions. Other non-project sections do not require images or evidence links.
- Facebook, Zalo, Gmail, demo, and source examples keep `href=""` inside commented markup beside prominent Vietnamese instructions. No external URL is invented.

## Accessibility and responsive behavior

- Pages use Vietnamese document language, semantic headings, descriptive navigation labels, and a skip link.
- The active detail-page link uses `aria-current="page"`.
- Keyboard focus remains visibly outlined; muted text maintains readable contrast against the dark background.
- Hover/focus motion and smooth scrolling respect `prefers-reduced-motion`.
- The layout wraps long user-provided text rather than forcing horizontal scrolling.

## Constraints

- Static HTML and CSS only; no JavaScript, framework, or third-party library.
- Use verified personal information only. Replace bracketed placeholders when the owner supplies facts.
- Keep media sources and external destinations empty until the owner provides real assets and URLs.
