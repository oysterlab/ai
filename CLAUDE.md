# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AX Lab is a static HTML experiment archive site documenting AI prototyping experiments. It showcases case studies exploring how accurately AI can implement designs from images and descriptions.

**Language**: Korean (content), English (code)

## Architecture

```
study01/
├── index.html                                    # Main blog page listing all experiments
├── experiments/
│   └── [NNN]-[name]/                            # Each experiment in its own folder
│       ├── experiment-[YYYYMMDD]-[NNN].html     # Experiment detail page
│       └── images/                              # Experiment-specific images
├── 01-create-archive-site.md                    # Design spec for experiment pages
└── 02-quick-prompts.md                          # Quick prompts for common modifications
```

## Tech Stack

- Vanilla HTML/CSS/JavaScript (no build step required)
- Google Fonts: Instrument Serif + DM Sans
- CSS scroll-snap for horizontal carousels
- IntersectionObserver for scroll reveal animations

## Design System

### Color Palette
```css
--bg: #FAFAF8;
--bg-warm: #F5F4F0;
--text: #1A1A1A;
--text-muted: #6B6B6B;
--accent: #3D4F5F;
--border: #E5E4E0;
```

### Typography
- Headings: `font-family: 'Instrument Serif'`
- Body: `font-family: 'DM Sans'`
- Generous whitespace, designer portfolio aesthetic

## Key Interactive Features

1. **Horizontal Carousel**: Each Phase section has attempt cards in a CSS scroll-snap carousel with focus/blur effects (active card: full opacity, inactive: 0.4 opacity + 2px blur)

2. **Floating TOC**: Auto-hides after 2 seconds of inactivity, shows on scroll/keyboard input

3. **Keyboard Navigation**: Arrow up/down for sections, left/right for carousel slides

4. **Comparison Modal**: Click attempt cards to show target vs result comparison

## File Naming Convention

- Experiment folders: `[NNN]-[experiment-name]` (e.g., `001-ax-prototyping`)
- Experiment files: `experiment-[YYYYMMDD]-[NNN].html`
- Images go in each experiment's `images/` subfolder
