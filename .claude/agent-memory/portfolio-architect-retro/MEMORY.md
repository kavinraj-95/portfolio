# Portfolio Architect - Retro Theme Memory

## Project: KAVINRAJ.SYS Portfolio

### User Information (from Resume)
- **Name**: Kavinraj S
- **Email**: kavinraj191105@gmail.com
- **Phone**: +91 7305199372
- **LinkedIn**: linkedin.com/in/kavinraj95
- **GitHub**: github.com/kavinraj-95
- **University**: Amrita Vishwa Vidyapeetham (NOT SJCE)
- **Degree**: B.Tech in Computer Science, CGPA: 9.0, Minor: IoT
- **Duration**: June 2023 - May 2027

### Design System
- **Color Palette**: Dark terminal theme with teal (#00d4aa) primary, amber (#f5a623) for highlights, purple (#7c3aed) accent
- **Typography**: JetBrains Mono primary, Fira Code fallback - loaded from Google Fonts
- **Background**: #0a0f14 (deep dark), #121a22 (secondary), #0d1419 (tertiary)

### Implementation Stages
1. **Stage 1 (Complete)**: Foundation + Boot Sequence
2. **Stage 2 (Complete)**: Hero + Navigation
3. **Stage 3 (Complete)**: Education + Experience Sections
4. **Stage 4 (Pending)**: Projects Section
5. **Stage 5 (Pending)**: Skills + Contact + Terminal Easter Egg
6. **Stage 6 (Pending)**: Polish + Deployment

### Stage 3 Implementation Details

#### Education Section ("INSTALLED_MODULES")
- ASCII box-drawing header with `+--` borders
- University displayed as npm package: `amrita-vishwa-vidyapeetham@9.0.0`
- Module card with left gradient border (teal to purple)
- Status indicator with amber pulsing dot for "ACTIVE"
- Coursework as package tags in 3-column grid (2 tablet, 1 mobile)
- Package tags with bracket notation: `[COURSE_NAME]`
- Hover effect: translateX(4px) + teal glow

#### Experience Section ("ACTIVE_PROCESSES")
- Timeline connector with ASCII pipe characters (desktop only)
- Process cards with status indicators on timeline
- IEEE: status-active (amber), 4 months, Remote
- XCMG: status-complete (teal), 3 months, Tamil Nadu
- Expandable details via click/keyboard (Enter/Space)
- ARIA attributes for accessibility (aria-expanded, aria-controls)
- Metrics visualization with gradient progress bars
- Hover effect on cards: translateX(4px) + glow intensification

#### CSS Patterns Used
- `.section-header` with `[data-animate]` for Intersection Observer
- Staggered animation delays via nth-child selectors
- Status indicators: 8px dots with box-shadow glow
- Process card border-left: 3px solid (amber for active, teal for complete)
- `max-height` transition for expandable sections (0 to 500px)

#### JavaScript Additions
- `initSectionAnimations()`: Intersection Observer for fade-in-up
- `initProcessCards()`: Click/keyboard handlers for expand/collapse
- `prefersReducedMotion()`: Accessibility check
- Animation threshold: 0.15, rootMargin: '0px 0px -50px 0px'

### Technical Patterns
- Single HTML file with embedded CSS/JS (no build process)
- IIFE pattern for JavaScript to avoid global pollution
- CSS variables enable easy theming
- `prefers-reduced-motion` media query for accessibility
- Desktop-first responsive approach (breakpoints: 1024px, 768px, 480px)
- Passive scroll event listeners for performance

### Key Responsive Breakpoints
- 1024px: Tablet - 2-column course grid, hide ASCII art
- 768px: Mobile - Single column, hide timeline, stack layouts
- 480px: Small mobile - Reduced font sizes

### Accessibility Features
- Proper heading hierarchy (h2 for sections, h3 for items)
- ARIA labels on interactive elements
- role="button" with tabindex="0" for keyboard navigation
- aria-expanded for expandable sections
- aria-controls linking headers to detail panels
- prefers-reduced-motion support
