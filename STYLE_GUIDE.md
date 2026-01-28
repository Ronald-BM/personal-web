# Personal Webpage Style Guide
## Ronald Scheffers

---

## Design Philosophy

**"Precision meets Innovation"**

A minimal, commanding digital presence that speaks through restraint. Every element serves a purpose. The design should feel like walking into a well-architected system — clean, intentional, and subtly powerful.

---

## Color Palette

### Primary Colors

| Name | Hex | Usage |
|------|-----|-------|
| **Void** | `#0D0D0D` | Primary background |
| **Graphite** | `#1A1A1A` | Secondary background, cards |
| **Smoke** | `#2D2D2D` | Borders, subtle divisions |
| **Steel** | `#4A4A4A` | Muted text, icons |

### Accent Colors

| Name | Hex | Usage |
|------|-----|-------|
| **Signal Orange** | `#FF6B35` | Primary accent, CTAs, highlights |
| **Ember** | `#FF8C5A` | Hover states, gradients |
| **Glow** | `#FFAA80` | Subtle highlights, animations |

### Neutral Colors

| Name | Hex | Usage |
|------|-----|-------|
| **Pure** | `#FFFFFF` | Headlines, primary text |
| **Mist** | `#B3B3B3` | Body text |
| **Fog** | `#666666` | Secondary text, captions |

---

## Typography

### Font Stack

```css
/* Headlines - Sharp, geometric, authoritative */
--font-display: 'Space Grotesk', 'Inter', -apple-system, sans-serif;

/* Body - Clean, highly readable */
--font-body: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;

/* Code/Tech accents - Optional monospace moments */
--font-mono: 'JetBrains Mono', 'Fira Code', monospace;
```

### Type Scale

| Element | Size | Weight | Letter Spacing |
|---------|------|--------|----------------|
| Hero Title | 72-96px | 600 | -0.02em |
| Section Title | 48-56px | 500 | -0.01em |
| Subsection | 24-32px | 500 | 0 |
| Body Large | 18-20px | 400 | 0.01em |
| Body | 16px | 400 | 0.01em |
| Caption | 14px | 400 | 0.02em |
| Label | 12px | 500 | 0.08em (uppercase) |

---

## Spacing System

Based on an 8px grid with generous negative space.

```css
--space-xs: 8px;
--space-sm: 16px;
--space-md: 32px;
--space-lg: 64px;
--space-xl: 128px;
--space-2xl: 256px;
```

### Negative Space Philosophy

- **Sections**: Minimum 128px vertical padding
- **Content width**: Max 1200px, often narrower (800px for text)
- **Element breathing room**: Let elements float in space
- **Asymmetry**: Off-center placements create visual interest

---

## Animation Principles

### Core Values
1. **Purposeful** — Animation guides attention, never decorates
2. **Subtle** — Micro-interactions over macro-movements
3. **Physics-based** — Natural easing, slight overshoot
4. **Performance** — CSS transforms only, 60fps minimum

### Timing Functions

```css
/* Smooth entrance */
--ease-out: cubic-bezier(0.16, 1, 0.3, 1);

/* Interactive feedback */
--ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);

/* Snappy micro-interactions */
--ease-snap: cubic-bezier(0.34, 1.56, 0.64, 1);
```

### Animation Ideas

#### 1. **Ambient Particle Field**
Sparse, slowly drifting particles/nodes that subtly connect when near each other. Think: neural network visualization, but minimal.
- Color: `#FF6B35` at 10-20% opacity
- Movement: 0.5-2px per second drift
- Connection lines: appear within 100px proximity

#### 2. **Cursor Glow Trail**
Subtle orange glow that follows cursor with delay, fading quickly.
- Radius: 150-200px
- Opacity: 5-10%
- Delay: 100ms

#### 3. **Text Reveal**
Characters or words fade up with stagger on scroll.
- Duration: 600ms per element
- Stagger: 50ms between items
- Transform: translateY(20px) → translateY(0)

#### 4. **Magnetic Buttons**
Interactive elements subtly pull toward cursor when nearby.
- Range: 50px
- Movement: 5-10px maximum
- Return: smooth spring animation

#### 5. **Grid Lines Pulse**
Background grid that subtly pulses from interaction points.
- Very low opacity (2-5%)
- Ripple speed: 200px/second
- Fade distance: 300px

#### 6. **Scroll Progress Indicator**
Thin orange line at top showing page progress.
- Height: 2px
- Animated fill from left

---

## Layout Concepts

### Hero Section
```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│                                                         │
│                                                         │
│     RONALD                                              │
│     SCHEFFERS                      [subtle particle     │
│                                     animation here]     │
│     Building the future,                                │
│     one system at a time.                               │
│                                                         │
│                                        ↓ scroll         │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

### Section Pattern
```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│                                                         │
│              SECTION TITLE                              │
│              ────────────── (orange accent line)        │
│                                                         │
│                                                         │
│         Content aligned left or centered,               │
│         never filling full width.                       │
│         Maximum 65 characters per line                  │
│         for optimal readability.                        │
│                                                         │
│                                                         │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## Component Styles

### Buttons

```css
/* Primary Button */
.btn-primary {
  background: transparent;
  border: 1px solid #FF6B35;
  color: #FF6B35;
  padding: 16px 32px;
  font-size: 14px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  transition: all 0.3s var(--ease-out);
}

.btn-primary:hover {
  background: #FF6B35;
  color: #0D0D0D;
  box-shadow: 0 0 30px rgba(255, 107, 53, 0.3);
}
```

### Cards

```css
.card {
  background: #1A1A1A;
  border: 1px solid #2D2D2D;
  padding: 48px;
  transition: all 0.4s var(--ease-out);
}

.card:hover {
  border-color: #FF6B35;
  transform: translateY(-4px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
}
```

### Links

```css
.link {
  color: #B3B3B3;
  text-decoration: none;
  position: relative;
}

.link::after {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 1px;
  background: #FF6B35;
  transition: width 0.3s var(--ease-out);
}

.link:hover {
  color: #FFFFFF;
}

.link:hover::after {
  width: 100%;
}
```

---

## Visual Inspiration

### Mood Keywords
- **Architectural** — Grid-based, structural
- **Nocturnal** — Dark, with strategic light
- **Precise** — Pixel-perfect, intentional
- **Forward** — Cutting-edge without being trendy
- **Restrained** — Power through simplicity

### Reference Sites for Inspiration
1. **Stripe.com** — Masterful use of subtle animation and gradients
2. **Linear.app** — Clean dark UI with purposeful motion
3. **Vercel.com** — Tech-forward, minimal, commanding
4. **Apple.com** — Negative space mastery
5. **Pentagram.com** — Bold typography, editorial layout

### Imagery Style (if used)
- Abstract: Data visualization aesthetics
- Geometric: Clean lines, node networks
- Gradient meshes: Subtle orange-to-dark transitions
- Avoid: Stock photos, busy patterns, generic tech imagery

---

## Interaction States

| State | Visual Change |
|-------|---------------|
| Default | Base styling |
| Hover | Subtle lift, glow, color shift |
| Active/Click | Brief scale down (0.98), darker |
| Focus | Orange outline, 2px offset |
| Disabled | 40% opacity, no pointer |

---

## Accessibility Notes

- Maintain 4.5:1 contrast ratio minimum for body text
- Orange on dark grey meets WCAG AA for large text
- Include focus states for keyboard navigation
- Respect `prefers-reduced-motion` for animations
- Semantic HTML structure

---

## File Structure Suggestion

```
/personal-web
├── index.html
├── css/
│   ├── variables.css    (tokens, custom properties)
│   ├── reset.css        (normalize styles)
│   ├── typography.css   (font definitions)
│   ├── layout.css       (grid, spacing)
│   ├── components.css   (buttons, cards, etc.)
│   └── animations.css   (keyframes, transitions)
├── js/
│   ├── main.js          (initialization)
│   ├── particles.js     (ambient animation)
│   └── scroll.js        (scroll-based effects)
└── assets/
    └── fonts/
```

---

## Summary

This design language positions you as someone who builds sophisticated systems — without saying it explicitly. The dark palette with surgical orange accents suggests precision and innovation. Generous negative space communicates confidence and clarity of thought. Subtle, physics-based animations hint at the complexity beneath the surface.

**Less is more. Let the space speak.**
