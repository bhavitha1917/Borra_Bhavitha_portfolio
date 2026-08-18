# Design & Implementation Insights

* **Colors:** Navy `#0b1f3a` (primary/headings), soft pale lavender `#f4f0fa` (page background), white `#ffffff` (card surfaces, kept white so cards still read distinctly against the tinted background), gray `#5c6270` (secondary text), lavender `#8b7fd6` with a light tint `#ece9fb` (restrained accent for underlines, borders, links).
* **Typography:** Manrope (headings/nav/tagline) + Inter (body), loaded via Google Fonts with system sans-serif fallback stack in case of offline/blocked font load.
* **Layout:** Mobile-first CSS; single-column base layout, grid breakpoints introduced at 600px (2-column cards/skills) and 900px (3-column skills, larger hero text). `box-sizing: border-box` and `overflow-x: hidden` on body used to guard against horizontal overflow.
* **Experience vs. Projects:** Kept as two distinct `<section>`s per spec — the internship lives only under Experience; the Breast Tissue Density Classification project (also done during the internship) is listed separately under Projects with its own description, since the spec explicitly requires both entries.
* **JS scope:** `script.js` was kept to the minimum needed — a mobile nav toggle (hamburger button + collapsible menu) — since CSS alone can't manage the open/close interaction state. No other JS was added (no frameworks, no unnecessary interactivity), per spec constraints.
* **Accessibility:** Added a skip-to-content link, `aria-expanded`/`aria-controls` on the nav toggle, and `alt` text on the profile image.
* **CV link:** Uses `target="_blank" rel="noopener"` as required so it opens in a new tab without exposing a `window.opener` reference.

## Update (spec revision: lavender bg, inline skills, coursework/JEE ranks, extra-curricular section)
* **Skills format:** Replaced the pill-tag grid with a single `.label-list` component (bold category label + comma-separated inline text) to match the spec's strict "Category: skill_1, skill_2, ..." format. This component is reused as-is for the new Extra-curricular Activities section, since both are "label: comma/semicolon-separated content" lists — avoids introducing a second, near-duplicate list style.
* **Coursework:** Rendered as a single flowing sentence under the B.Tech entry (`.timeline-courses`) rather than a bulleted sub-list, to keep the academic timeline visually compact and avoid a long nested list interrupting its rhythm.
* **JEE ranks:** Added as two additional `.timeline-detail` lines under Class XII, consistent with how the existing 98.3% score line was already styled.
* **New section placement:** Extra-curricular Activities was placed after Skills and before Contact, following the same order it appears in the spec, and added to the nav.

## Update (hero side-by-side layout)
* **Structure:** Wrapped the photo and text in `.hero-media`/`.hero-text` sub-containers inside `.hero` so flexbox can control the two-column split independently of the existing internal spacing (e.g. `.hero-subtitle`'s own margin-top).
* **Breakpoint:** Introduced a new `700px` breakpoint (between the existing 600px and 900px ones) purely for the hero row layout — chosen because the hero's two-column content needs less width than the grid-based sections to look balanced, so reusing 900px would leave it stacked longer than necessary.
* **Mobile default:** `.hero` stays `flex-direction: column` with centered, center-aligned text below 700px (no change from prior stacked behavior), then switches to `flex-direction: row` with left-aligned, vertically centered text at 700px+.

## Update (subtitle split into two lines, tagline removed)
* Subtitle now marked up as two `<span class="hero-subtitle-line">` elements inside `.hero-subtitle`, each forced to `display: block` — a minimal, scoped CSS addition (not a new section/design change) needed so the spec's explicit "two separate lines" requirement actually renders instead of running the spans together inline.

## Update (uniform card styling)
* About, Academic Background, Skills, and Extra-curricular Activities content is now each wrapped in a `<div class="card">` inside its `<section>`, matching Experience's existing markup pattern (`section-title` outside the card, content inside). No new CSS was written — the existing `.card` rule (white background, 12px radius, subtle shadow) is reused verbatim so all six sections (About, Academic Background, Experience, Projects, Skills, Extra-curricular) now render with identical card styling.
* Projects was left untouched since each project was already individually wrapped in its own `.card` inside `.card-grid` — it already satisfied the uniform-card requirement.
* Contact and Hero were left as-is since the task scoped the change to About/Academic Background/Skills/Extra-curricular specifically.
