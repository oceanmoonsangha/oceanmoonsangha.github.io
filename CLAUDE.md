# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML website for Ocean Moon Sangha, a Zen Buddhist meditation group in Santa Monica, California. Hosted on GitHub Pages at oceanmoon.org.

**Tech Stack:** HTML5, CSS3, Vanilla JavaScript (ES6+) - no build tools, frameworks, or dependencies.

## Development

**No build process required.** Edit files directly and push to main branch for automatic GitHub Pages deployment.

To preview locally, open any HTML file in a browser or use a local server:
```bash
python3 -m http.server 8000
```

## Architecture

### CSS Design System (styles.css)

Color palette uses CSS custom properties:
- `--ink` / `--deep-ocean` / `--twilight` - dark tones
- `--moon-glow` / `--sand` / `--warm-white` - light tones
- `--muted-gold` / `--soft-sage` / `--stone` - accents

Typography uses self-hosted Gentium Plus (WOFF2 files in root) for consistent rendering of macrons in Japanese names (e.g., "Ryūtaku").

Responsive breakpoints: 900px (tablet), 768px (mobile with hamburger menu).

### Page Structure

All pages share: fixed navigation bar → page header → main content in `.container` → footer.

Key CSS components: `.container` (1200px max-width wrapper), `.practice-card`, `.teacher-card`, `.schedule-table`, `.contact-form`.

### JavaScript (script.js)

- Navigation scroll effect (background change)
- Mobile hamburger menu toggle
- Intersection Observer fade-in animations
- Smooth anchor scrolling
- Dynamic copyright year

## File Structure

- `index.html` - Homepage (hero, intro, practice info, location)
- `about.html` - Mission, history, teacher bios, lineage
- `schedule.html` - Weekly schedule table
- `contact.html` - Contact form
- `resources.html` - External links
- `CNAME` - Domain configuration (oceanmoon.org)
