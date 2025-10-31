# CLAUDE.md
 # CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-page website for **ODES** (Orbital Dynamics and Engineering Solutions), a space technology company focused on mission validation and simulation platforms for the New Space era. The website showcases the company's comprehensive validation platform, team, value proposition, and contact information.

## Technology Stack

- **Frontend Framework**: React 18 (loaded via CDN)
- **Styling**: Tailwind CSS (loaded via CDN)
- **Build Tool**: Babel Standalone (for JSX transpilation in browser)
- **Architecture**: Single HTML file with embedded JSX/React components

## Project Structure

```
/home/ggalanos/website/
├── odes-website-updated.html    # Main website file (self-contained)
└── odes-RGB-reverse.png         # Company logo (1000x1000 PNG)
```

## Key Architecture Details

### Single-File Application
The entire website is contained in a single HTML file (`odes-website-updated.html`) that includes:
- All CSS styling (custom + Tailwind utility classes)
- All React components written in JSX
- All SVG icon components
- Animation definitions and space-themed visual effects

### Component Structure
The application follows a modular React component architecture:

1. **SVG Icon Components**: Custom-built icons for features (SatelliteIcon, RadioIcon, ShieldIcon, BoltIcon, RefreshIcon, TargetIcon, ChartIcon, LocationIcon, BuildingIcon, HandshakeIcon, RocketIcon, PersonIcon)

2. **Main Components**:
   - `Navigation`: Fixed header with scroll-based opacity changes
   - `Hero`: Full-screen landing section with animated stars and satellite icon
   - `About`: Two-column layout explaining the challenge and solution
   - `Solution`: Grid of 6 feature cards with icons
   - `Value`: Business value proposition with statistics
   - `Team`: Grid of 4 team member cards
   - `Contact`: Contact information and CTA section
   - `Footer`: Simple footer with logo and copyright

3. **App Component**: Root component that composes all sections in order

### Styling Patterns
- **Color Scheme**: Purple gradient (`#667eea` to `#764ba2`) as primary brand color
- **Background**: Dark space theme (`#0a0e27`, `#1a1a2e`, `#16213e`)
- **Typography**: Inter font family from Google Fonts
- **Animations**:
  - `animate-float`: 6s infinite floating animation for hero satellite
  - `twinkle`: 3s infinite star twinkling
  - `card-hover`: Lift and shadow effect on feature cards

### State Management
Minimal state usage:
- Navigation scroll state (`isScrolled`) - triggers background blur/opacity when scrolling past 50px

## Development Workflow

### Viewing the Website
Simply open `odes-website-updated.html` in a web browser. No build process required.

```bash
# Using a local server (recommended for development)
python3 -m http.server 8000
# Then navigate to http://localhost:8000/odes-website-updated.html

# Or directly open the file
xdg-open odes-website-updated.html
```

### Making Changes
Since this is a single-file application with CDN-loaded dependencies:
1. Edit the HTML file directly
2. Refresh the browser to see changes
3. No compilation or build step needed

### Testing
- Test on multiple screen sizes (responsive design with Tailwind breakpoints: `md:`, `lg:`, `sm:`)
- Verify smooth scrolling behavior between sections
- Check navigation highlights and scroll effects
- Ensure all icons render correctly
- Verify animations perform smoothly

## Content Structure

The website presents the following narrative flow:
1. **Hero**: Brand positioning - "Validation Beyond Boundaries"
2. **About**: Problem (65% CubeSat failure rate) → Solution (comprehensive validation platform)
3. **Solution**: 6 core platform features (simulation, validation, hardware-in-loop, testing, tracing, analytics)
4. **Value**: Business benefits and market statistics (€413M opportunity, 94% gross margin)
5. **Team**: 4 team members (3 co-founders + 1 advisor)
6. **Contact**: Location (Athens), backing (EMTECH SPACE), partners (ESA, Open Cosmos), missions (HSD, HELEO, ERMIS)

## Key Design Decisions

### Why Single-File Architecture?
- Simple deployment (just upload one HTML file + logo)
- No build complexity or dependencies
- Fast iteration during development
- Easy to share and preview

### CDN Dependencies
All libraries loaded from CDN:
- React 18 (production build)
- ReactDOM 18
- Babel Standalone (for JSX transpilation)
- Tailwind CSS

This eliminates the need for npm/package management but means the site requires internet connectivity for these resources.

### Custom SVG Icons
All icons are hand-crafted SVG components rather than using an icon library. This:
- Reduces dependencies
- Allows precise brand-aligned styling
- Enables gradient fills matching brand colors
- Keeps file size minimal

## Important Notes

- The logo file (`odes-RGB-reverse.png`) must be in the same directory as the HTML file
- All anchor links use hash navigation (`#about`, `#solution`, etc.)
- Email contact: `info@odes-space.com`
- No backend or API integrations
- No analytics or tracking code included
