# CLAUDE.md — Project Context for AI Assistants

## Project Overview

Personal website for **Ronald Scheffers**, CTO of an AI Automation Agency.

**Important:** The agency role should NOT be explicitly mentioned on the site. Instead, the design and copy should *reflect* this expertise through sophistication, technical credibility, and AI/automation-focused messaging.

---

## Design Philosophy

**"Precision meets Innovation"**

A minimal, commanding digital presence that speaks through restraint. Every element serves a purpose. The design should feel like walking into a well-architected system — clean, intentional, and subtly powerful.

### Core Principles
- **Negative space is essential** — let elements breathe, never crowd
- **Subtle over flashy** — animations guide attention, never distract
- **Tech-forward aesthetic** — evoke AI/neural networks without being literal
- **Confidence through restraint** — say more with less

---

## Color Palette

### Dark Theme (Primary)
| Name | Hex | Usage |
|------|-----|-------|
| Void | `#0D0D0D` | Primary background |
| Graphite | `#1A1A1A` | Cards, secondary surfaces |
| Smoke | `#2D2D2D` | Borders, dividers |
| Steel | `#4A4A4A` | Muted text, icons |

### Accent
| Name | Hex | Usage |
|------|-----|-------|
| Signal Orange | `#FF6B35` | Primary accent, CTAs, highlights |
| Ember | `#FF8C5A` | Hover states, gradients |
| Glow | `#FFAA80` | Subtle highlights |

### Neutrals
| Name | Hex | Usage |
|------|-----|-------|
| Pure | `#FFFFFF` | Headlines, primary text |
| Mist | `#B3B3B3` | Body text |
| Fog | `#666666` | Secondary text |

---

## Typography

```css
--font-display: 'Space Grotesk', -apple-system, sans-serif;  /* Headlines */
--font-body: 'Inter', -apple-system, sans-serif;              /* Body text */
```

- Headlines: Bold, geometric, negative letter-spacing
- Body: Clean, highly readable, subtle positive letter-spacing
- Max line width: ~65 characters for readability

---

## Animation Guidelines

1. **Purposeful** — every animation serves a function
2. **Subtle** — micro-interactions over dramatic movements
3. **Physics-based** — natural easing with slight overshoot
4. **Performant** — CSS transforms only, 60fps minimum
5. **Respectful** — honor `prefers-reduced-motion`

### Implemented Animations
- Particle network in hero (neural network aesthetic)
- Cursor glow trail (orange, low opacity)
- Scroll-triggered reveals (fade up with stagger)
- Scroll progress bar (top of page)
- Card hover effects (lift + border glow)

---

## Tone of Voice

### Characteristics
- **Confident, not arrogant** — state capabilities plainly
- **Concise** — no filler words, every word earns its place
- **Active voice** — "I build" not "systems are built"
- **Outcome-focused** — emphasize results over process
- **Slightly provocative** — challenge the reader to think

### Copy Examples
- Hero: *"I make machines do the work. So humans can do the thinking."*
- About header: *"Intelligence by design"*
- Contact CTA: *"What could you automate?"*

### Words to Use
- Automate, intelligent, systems, transform, eliminate, streamline
- Build, architect, design, implement, integrate

### Words to Avoid
- Revolutionary, cutting-edge, synergy, leverage (overused)
- Best-in-class, world-class (generic)
- AI Agency, automation agency (don't explicitly mention)

---

## Technical Stack

- **HTML5** — semantic, accessible markup
- **CSS3** — custom properties, grid, flexbox, no frameworks
- **Vanilla JS** — no dependencies, modern ES6+
- **Fonts** — Google Fonts (Space Grotesk, Inter)

### Preferences
- Single-file demos are fine for simplicity
- Separate CSS files for production
- Mobile-first responsive design
- Respect accessibility (WCAG AA minimum)

---

## File Structure

```
/personal-web
├── CLAUDE.md           (this file)
├── STYLE_GUIDE.md      (detailed design documentation)
├── index.html          (main website)
├── css/                (optional: separated styles)
├── js/                 (optional: separated scripts)
└── assets/
    └── fonts/
```

---

## Current Site Sections

1. **Hero** — Name, tagline, CTA, particle animation
2. **About** — "Intelligence by design" + brief intro
3. **Work/Expertise** — Three cards: Automate, AI Strategy, Intelligent Integration
4. **Contact** — "What could you automate?" + email
5. **Footer** — Copyright + social links

---

## Future Considerations

- Case studies / portfolio section
- Blog integration
- Dark/light mode toggle (currently dark only)
- More sophisticated particle interactions (mouse reactivity)
- Page transitions if multi-page

---

## Quick Reference

**When writing copy:** Be direct, outcome-focused, slightly provocative. Don't explicitly mention "AI Agency" — let the expertise speak through the work.

**When designing:** Dark grey + orange, generous whitespace, subtle animations. Think Linear, Vercel, Stripe — sophisticated tech aesthetic.

**When coding:** Vanilla stack, no frameworks, semantic HTML, CSS custom properties, modern JS.
