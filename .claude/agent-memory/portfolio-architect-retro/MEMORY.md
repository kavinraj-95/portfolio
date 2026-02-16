# Portfolio Architect - Retro Theme Memory

## Project: KAVINRAJ.SYS Portfolio

### Design System
- **Color Palette**: Dark terminal theme with teal (#00d4aa) primary, amber (#f5a623) for highlights, purple (#7c3aed) accent
- **Typography**: JetBrains Mono primary, Fira Code fallback - loaded from Google Fonts
- **Background**: #0a0f14 (deep dark), #121a22 (secondary), #0d1419 (tertiary)

### Implementation Stages
1. **Stage 1 (Complete)**: Foundation + Boot Sequence
   - CSS custom properties for entire color system
   - CRT scanline overlay effect
   - Boot sequence with realistic system messages
   - Skip button (ESC key) for accessibility
   - Auto-advance after boot completes

2. **Stage 2 (Complete)**: Hero + Navigation
   - Full-screen hero section (100vh) with terminal aesthetics
   - Animated typing effect for "KAVINRAJ S" (80ms/char)
   - Terminal prompt prefix with color-coded segments
   - ASCII art neural network decoration (desktop only)
   - Rotating subtitle system (4 roles, 3s display, 500ms fade)
   - Contact links styled as executable commands (./email --send, etc.)
   - Scroll indicator with pulsing chevron animation
   - Sticky navigation bar (appears after scrolling past hero)
   - Nav links with bracket hover effect [LINK]
   - Mobile hamburger menu with slide-down animation

3. **Stage 3 (Pending)**: Content Sections
4. **Stage 4 (Pending)**: Terminal Easter Egg
5. **Stage 5 (Pending)**: Polish + Deployment

### Technical Patterns
- Single HTML file with embedded CSS/JS (no build process)
- IIFE pattern for JavaScript to avoid global pollution
- CSS variables enable easy theming
- `prefers-reduced-motion` media query for accessibility
- Desktop-first responsive approach (breakpoints: 1024px, 768px, 480px)
- Passive scroll event listeners for performance

### Boot Sequence Details
- Duration: ~3.5 seconds
- 12 sequential messages with status indicators
- Blinking cursor effect with CSS animation
- Smooth fade transition to portfolio content
- Skip via ESC key or button click

### Hero Section Details
- Typing effect: Character-by-character with 80ms delay
- Cursor blink: 530ms timing (classic terminal feel)
- Subtitle rotation: 3000ms display, 500ms fade transition
- Commands hover: Sweep animation + amber color change
- Scroll indicator: Appears after 2.5s delay with pulse animation

### Navigation Details
- Height: 60px (--nav-height CSS variable)
- Background: rgba(10, 15, 20, 0.95) with backdrop-filter blur
- Appears when scrolling past hero height - 100px threshold
- Active link tracking based on scroll position
- Mobile: Hamburger toggle with slide-down menu

### Key CSS Techniques
- Scanlines: `repeating-linear-gradient` with 2px transparent / 1px semi-transparent
- Text glow: Multiple layered `text-shadow` with rgba teal values
- CRT vignette: `radial-gradient` overlay from transparent center to dark edges
- Command hover sweep: `linear-gradient` animated via `left` property
- Nav bracket effect: `::before`/`::after` with opacity + transform transitions
