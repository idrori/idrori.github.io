# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the static website for the **Superintelligence Lab** (superintelligencelab.org), a research lab led by Iddo Drori focused on AGI, mathematical reasoning, and AI for education. The site is hosted via GitHub Pages at `idrori.github.io`.

## Development

**No build step required.** This is a pure static site with HTML, CSS, and vanilla JavaScript.

To preview locally:
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .
```

**Deployment:** Push to `main` branch - GitHub Pages deploys automatically.

## Architecture

```
├── index.html          # Main homepage (research, publications, teaching, talks, contact)
├── team.html           # Team members page
├── service.html        # Academic service page
├── bio.html            # Biography page
├── styles.css          # Global stylesheet (CSS variables, responsive design)
├── script.js           # Global JS (smooth scroll, parallax, mobile menu, nav highlighting)
├── agi-spring-2025/    # AGI course materials (Spring 2025)
├── agi-spring-2026/    # AGI course materials (Spring 2026)
├── rl-spring-2026/     # Reinforcement Learning course materials (Spring 2026)
└── *viz.html           # Mathematical visualization pages (IMO problems, Erdős-Szekeres)
```

## Key Patterns

- **Typography:** Cormorant Garamond for headings, Inter for body text
- **CSS Variables:** Defined in `:root` in `styles.css` for consistent theming
- **Responsive Design:** Mobile-first with hamburger menu for navigation
- **Accessibility:** Skip links, ARIA labels, semantic HTML throughout
- **Analytics:** Google Analytics (G-C4D2T7XF9V) included in all HTML pages

## Adding New Pages

1. Copy the `<head>` section from `index.html` (includes meta tags, fonts, analytics, stylesheet)
2. Include the navigation header and footer from existing pages
3. Link `script.js` at the end of `<body>` for standard interactivity

## Course Pages

Course directories (e.g., `agi-spring-2026/`) contain:
- `index.html` - Course homepage with syllabus, schedule, resources
- `homework*.txt` - Assignment files
- Additional HTML resources as needed
