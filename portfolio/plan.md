# Implementation Plan: Academic Portfolio Website

## 1. Setup
- Confirm assets present: `profile.jpg`, `Borra_Bhavitha_CV.pdf` (both already in `portfolio/`).
- Create empty `index.html`, `style.css`, `issues.md`, `insights.md`. Add `script.js` only if a real interactive need arises (e.g. mobile nav toggle, smooth scroll, active-section highlight).

## 2. HTML Structure (`index.html`)
- Semantic skeleton: `<header>` (hero), `<nav>` (section links), then `<main>` with `<section>`s in order: About, Academic Background, Experience, Projects, Skills, Contact; `<footer>` for CV/social links + copyright.
- Hero: profile.jpg as circular headshot, name, subtitle, tagline.
- About: single first-person paragraph.
- Academic Background: 3 entries (IISc B.Tech, Class XII, Class X) as a structured list/table (institution, dates, score).
- Experience: single internship entry (title, org, dates, description) in its own section, separate from Projects.
- Projects: exactly the 2 specified projects, each with title, dates, tech, and description.
- Skills: grouped by category (Programming, ML/DL, Computer Vision, Core CS, Systems/Tools) as labeled lists.
- Contact: both emails, LinkedIn, GitHub as links; CV link with `target="_blank" rel="noopener"`.
- Link all sections from the nav via anchor IDs.

## 3. CSS (`style.css`)
- Define CSS custom properties: navy primary, white/off-white background, gray secondary text, lavender accent.
- Import Manrope (headings) + Inter (body) via Google Fonts `<link>`, with system sans-serif fallback stack.
- Mobile-first layout using flexbox/grid; base styles first, then `min-width` media queries for tablet/desktop breakpoints.
- Style hero (centered, circular image via `border-radius: 50%` + `object-fit: cover`), nav (sticky or simple top bar, collapsible on mobile if needed), section spacing/rhythm, cards for Projects/Experience, skill tag/pill styling, footer/contact links.
- Explicitly guard against horizontal overflow: `max-width`, `box-sizing: border-box`, `overflow-x: hidden` on containers as needed.

## 4. JS (`script.js`, only if needed)
- Add only if a feature can't be done in pure CSS: e.g. mobile nav toggle button, smooth-scroll fallback, or active nav-link highlighting on scroll.
- Keep minimal, vanilla, no dependencies.

## 5. Verification Pass
- Open in browser (or use `run` skill) and check: no horizontal scroll at mobile/tablet/desktop widths, all nav links jump to correct sections, CV link opens in new tab, external links (LinkedIn/GitHub/emails) are correct and `mailto:`/`https:` formatted properly, image loads and is cropped cleanly.
- Validate content against spec exactly: correct dates, CGPA, percentages, project scope limited to the 2 listed projects, experience kept separate from projects.

## 6. Documentation Deliverables
- `issues.md`: log any real implementation issues found (e.g., placeholder/unverifiable links, missing assets, ambiguous spec points).
- `insights.md`: log key design/implementation decisions (color/type choices, breakpoint values, why JS was or wasn't used, layout choices for Experience vs Projects separation, etc.) for future maintainers.
