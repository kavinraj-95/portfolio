# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **personal portfolio website** - a single-page application showcasing education, experience, projects, and technical skills. The portfolio is fully self-contained in one HTML file with embedded CSS and JavaScript.

**Tech Stack:** HTML5, CSS3 (with animations and gradients), Vanilla JavaScript

## File Structure

- **`index.html`** - The main portfolio webpage (contains all HTML, CSS, and JavaScript)
- **`README.md`** - Basic repository description
- **`Kavinraj's Resume.pdf`** - PDF resume file

## Development & Deployment

### Viewing the Portfolio
Open `index.html` directly in a web browser:
```bash
# Linux/Mac
open index.html

# Or use a local server (Python 3)
python3 -m http.server 8000
# Then visit http://localhost:8000
```

### No Build Process
This project has no build step, dependencies, or compilation. All changes are made directly to `index.html`.

## Architecture & Content Sections

The portfolio is organized into the following sections (all in a single file):

1. **Header** - Name, subtitle, contact links (email, LinkedIn, GitHub, phone)
2. **Education** - University details, GPA, relevant coursework with skill tags
3. **Experience** - Two positions with dates and bullet-point descriptions
4. **Projects** - Six project cards in a responsive grid layout with tech stacks
5. **Technical Skills** - Three skill categories (Languages, ML & AI, Tools & Platforms)
6. **Footer** - Copyright and tagline

## Styling Details

- **Color Scheme:** Purple-to-violet gradient header (`#667eea` to `#764ba2`), white content sections with colorful gradient accents
- **Animations:**
  - `fadeInDown` - Header entrance animation
  - `fadeInUp` - Section entrance animations
  - Intersection Observer - Sections animate in as they come into view
  - Hover effects - Cards scale, lift, and get shadows on interaction
- **Responsive Design:** Media query at `768px` breakpoint for mobile optimization
- **Grid Layouts:**
  - Projects use `grid-template-columns: repeat(auto-fit, minmax(300px, 1fr))` for flexible wrapping
  - Skills use flexbox for responsive multi-column layout

## Editing Guidelines

When modifying the portfolio:

- **Content Updates** - Edit the HTML in the main body section (lines 253-400)
- **Styling Changes** - Modify the `<style>` block (lines 7-249)
- **Interactive Behavior** - Update the `<script>` section (lines 402-431)
- **Color Consistency** - Primary color is `#667eea`, secondary is `#764ba2` - update both places if changing
- **Project Cards** - Each `.project-card` follows the pattern: title, tech stack, description
- **Skill Tags** - Use `.skill-tag` elements for all skill badges across sections

## No Special Commands Required

This is a static HTML site with no CLI tools, testing frameworks, linters, or build processes. All work is done through:
- Direct HTML/CSS/JS editing
- Git version control
- Browser testing via `index.html` or a local server
