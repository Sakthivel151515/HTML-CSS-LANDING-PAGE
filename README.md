# Trabook — Travel Agency Landing Page

This repository contains a static HTML + CSS mock landing page for a travel brand named "Trabook." The project focuses on layout and visual design; it does not include a backend or JavaScript-driven interactions by default.

Summary
- Static files: `index.html`, `script.css`, and an `assets/` folder containing images and SVGs.
- Responsive layout with a mobile breakpoint at 600px (see `script.css`).

How to preview locally

1. Open `index.html` directly in a browser (quick preview).
2. Recommended: serve the folder via a local HTTP server so fonts and some browser behaviors load consistently:

```powershell
# from the project root
python -m http.server 8000
# then open http://localhost:8000
```

Or use the VS Code Live Server extension.

Code-focused notes

- Main files
  - `index.html` — semantic sections for header/hero, features, deals, testimonials, blog, subscribe/footer.
  - `script.css` — full styling, organized by page sections with comments ("page 1", "page 2", ...).

- Typography
  - Google Fonts used: Poppins (body), Roboto (paragraphs), Volkhov (headings). These load in `index.html` via Google Fonts link tags.

- CSS variables (in `:root` of `script.css`)
  - `--orange-color: #fa7436` (primary/brand)
  - `--dimwhite-color: #fefcfb`
  - `--desaturatedblue-color: #4086f4`
  - `--yellow-color: #ffb60a`
  - `--desaturated-purbleblue-color: #4e4e73`

- Layout map (how sections in `index.html` map to styles in `script.css`)
  - Header/Hero: `.section1`, `.navigation`, `.hero-section` (large left copy + right image card stack)
  - Search/CTA row: `.bottom` (location, date, guest, explore)
  - Features: `.section2`, `.bottom3` (cards with icons)
  - Deals: `.section3`, `.thirdimg` (tour cards)
  - Vacation plans: `.section4`, `.fourthimg` (featured trips)
  - Testimonials: `.fifth`, `.aboutcard`, `#about` (client quotes)
  - Blog: `.sixth`, `.latestblogs`
  - Subscribe & Footer: `.seventh`, `.base`, `.social`

Accessibility & code quality checklist
- [ ] Add descriptive `alt` attributes to any decorative or informative images that currently have empty or generic alt text.
- [ ] Ensure interactive elements (links, buttons) have focus styles and keyboard behaviour (e.g., menu toggle for mobile).
- [ ] Check color contrast for text over backgrounds; consider using the CSS variables to maintain consistent accessible color combinations.
- [ ] Replace `content: url(...)` pseudo-element images (used for small decorative icons) with inline `<img>` or background images if they are informative; pseudo-elements are not announced by screen readers.

Small improvements I can do for you (pick one or more)
- Add a lightweight npm dev script (package.json) and an `npm start` script that runs a tiny static server.
- Add an explicit MIT license file.
- Replace Google Fonts links with locally hosted fonts.
- Add simple JavaScript to wire a mobile navigation toggle and smooth scroll.
- Run a quick accessibility pass (alt text additions, aria labels, semantic improvements).

Notes & known issues
- Several decorative images are inserted using CSS `content: url(...)` which can be problematic for accessibility and caching; consider moving these into HTML where appropriate.
- Links in `index.html` are placeholders (`href="#"`) and forms do not submit to a backend.
- The stylesheet contains a single mobile breakpoint at 600px — depending on audience you may want additional breakpoints for tablets and large desktops.

License & credits
- This is a learning/demo project. If you'd like an explicit license added (for reuse or publishing), tell me which license (MIT, Apache 2.0, etc.) and I'll add a `LICENSE` file.

---
Generated and updated based on `script.css` and `index.html` found in the project root.
