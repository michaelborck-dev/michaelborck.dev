# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is Michael Borck's personal portfolio website (michaelborck.dev) - a static website built with vanilla HTML, CSS, and JavaScript. The site showcases his work as a developer, educator, and researcher across multiple domains including indie game development (RetroVerse Studios), educational technology (Borck.Education), consultancy services, and research projects.

## Architecture

### File Structure
- **HTML Pages**: Five main pages (`index.html`, `resume.html`, `consultancy.html`, `research.html`) 
- **Shared Styles**: `styles/common.css` contains global styles, CSS variables, and dark mode theming
- **Page-Specific Styles**: Each page has its own CSS file (`styles/index.css`, `styles/resume.css`, etc.)
- **JavaScript**: `js/common.js` handles shared functionality across all pages
- **Deployment**: GitHub Pages via CNAME file pointing to `michaelborck.dev`

### Design System

**CSS Architecture:**
- CSS custom properties for consistent theming (light/dark mode support)
- Modular CSS with shared base styles and page-specific overrides
- Consistent card-based layouts with different visual treatments per page

**Component Patterns:**
- **Home page**: Simple `work-card` components with emojis, titles, descriptions, and text links
- **Resume page**: Rich `format-card` components with large emoji icons and styled buttons (`format-link`)
- **Consultancy page**: `service-card` components with emojis, feature lists, and call-to-action buttons (`service-cta`)
- **Research page**: Clean `card` components with `accent-border` and status badges (deliberately emoji-free for professional appearance)

**Navigation Pattern:**
- Consistent header with brand name, social icons (GitHub, Twitter, LinkedIn), and back links on sub-pages
- Social icons use inline SVG for optimal performance

### JavaScript Functionality

All interactive features are handled by `js/common.js`:
- **Theme Management**: Dark/light mode toggle with localStorage persistence
- **Scroll Animations**: Intersection Observer API for fade-in effects on scroll
- **Smooth Scrolling**: Enhanced anchor link behavior
- **Card Interactions**: Hover effects with CSS transforms
- **Parallax Effects**: Subtle parallax scrolling for hero sections

### Styling Conventions

**Card Design Philosophy:**
- Home page: Simple and clean with emoji accents
- Resume/Consultancy: Rich and interactive with styled buttons
- Research: Professional and minimal (no emojis)
- Each page maintains its own color theme while sharing base styles

**Animation Classes:**
- `.animate-on-scroll` and `.animate-fade` for scroll-triggered animations
- Staggered delays (`.delay-1`, `.delay-2`, etc.) for sequential reveals

## Development Workflow

**No Build Process**: This is a static site with no bundling, compilation, or package management. Files can be edited directly and served by any web server.

**Local Development**: Serve files with any static server (e.g., Python's `python -m http.server`, Node's `npx serve`, or VS Code's Live Server extension).

**Deployment**: Automatic deployment via GitHub Pages when changes are pushed to the main branch.

## Content Updates

**Adding New Work/Projects**: Add new `work-card` components to `index.html` following the established pattern with appropriate emojis.

**Theme Consistency**: When adding new pages, include both `common.css` and a page-specific stylesheet. Include `js/common.js` for shared functionality.

**Social Links**: Update social media links in the header navigation across all HTML files when needed. Links currently point to GitHub (michael-borck), Twitter (@Michael_Borck), and LinkedIn (michaelborck).

## Domain and External Links

**Primary Domains:**
- `michaelborck.dev` (main site)
- `michaelborck.education` (educational tools)
- `retroverse.studio` (indie games)

**Key External Links:**
- Developer role links to GitHub profile: `https://github.com/michael-borck`
- Social media profiles are consistently linked across all pages