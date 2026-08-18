# Implementation Plan: Academic Portfolio Website

## 1. File Setup
1. Create `index.html`, `style.css`, and `script.js` in the `Website/` directory.
2. Link Manrope + Inter via Google Fonts `<link>` tags in `<head>`, with fallback stack `-apple-system, Segoe UI, Roboto, sans-serif`.
3. Link `style.css` and defer-load `script.js` from `index.html`.

## 2. HTML Structure (`index.html`)
Build a single page with semantic sections, in order:
1. **Header/Nav** — sticky top bar with name/logo + anchor links to each section (About, Background, Experience, Projects, Skills, Contact).
2. **Hero** — circular `profile.jpg` headshot, name (Borra Bhavitha), subtitle (B.Tech Mathematics and Computing | IISc Bengaluru), tagline ("Mathematics, Computing & AI"), CV button linking to `Borra_Bhavitha_CV.pdf` with `target="_blank" rel="noopener"`.
3. **About** — short first-person paragraph covering B.Tech status at IISc and interests (ML, DL, CV, AI research, problem-solving).
4. **Academic Background** — list/timeline of the 3 entries (B.Tech, Class XII, Class X) with institution, dates, and score.
5. **Experience** — single entry: Engineering Intern @ TANUH AI Center for Excellence in Healthcare, May–July 2026, with full description. Kept visually distinct from Projects.
6. **Projects** — exactly 2 cards: Self-Supervised Learning (Mar–Apr 2026) and Breast Tissue Density Classification (May–Jul 2026), each with title, dates, and description bullets/paragraph.
7. **Skills** — grouped into 5 categories (Programming, ML/DL, Computer Vision, Core CS, Systems/Tools) as tag/chip lists.
8. **Interests** — brief line or chip group (ML, DL, Problem Solving) integrated near About or Skills.
9. **Contact** — both emails (as `mailto:` links), LinkedIn, GitHub links (all opening in new tabs where external).
10. **Footer** — simple copyright/name line.

## 3. CSS Structure (`style.css`)
1. **Reset & base** — box-sizing reset, base font sizes, `overflow-x: hidden` safety, smooth scroll for anchor nav.
2. **Design tokens** — CSS custom properties for colors (deep navy primary, white/off-white background, gray secondary text, lavender accent), spacing scale, font families.
3. **Typography** — Manrope for headings, Inter for body; consistent heading scale.
4. **Layout** — CSS Grid/Flexbox for section containers, max-width wrapper (e.g. 1100px) centered with side padding.
5. **Components** — nav bar, hero, circular image styling, timeline/list items for Background, cards for Experience & Projects, skill chips, contact link buttons/icons.
6. **Responsive breakpoints** — mobile-first with breakpoints (~600px, ~900px) for nav collapse, grid-to-stack transitions, and font-size adjustments; verify no horizontal overflow.
7. **Polish** — subtle hover/transition states, spacing rhythm, restrained use of accent color.

## 4. JS (`script.js`, only if needed)
1. Mobile nav toggle (hamburger menu) if header nav doesn't fit on small screens.
2. Smooth-scroll fallback / active-link highlighting on scroll (optional, only if CSS `scroll-behavior` isn't sufficient).
3. Skip entirely if pure CSS/HTML covers all interactivity needs.

## 5. Verification Pass
1. Check all internal anchor links scroll to correct sections.
2. Check CV link and external links (LinkedIn, GitHub, mailto) open correctly in new tabs where applicable.
3. Test responsiveness at mobile/tablet/desktop widths; confirm no horizontal scroll.
4. Confirm `profile.jpg` and `Borra_Bhavitha_CV.pdf` are currently 0-byte placeholder files — flag this in `issues.md` since the image/PDF won't render/open until real files are supplied.

## 6. Documentation Artifacts
1. `issues.md` — log placeholder/empty asset files (profile.jpg, CV PDF) and any other implementation caveats (e.g., unverifiable external links).
2. `insights.md` — log key design decisions (color/font tokens chosen, layout approach, responsive strategy, why/if JS was used or avoided).
