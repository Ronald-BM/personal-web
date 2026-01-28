# Skill: Design System — Ronald Scheffers

## Design Philosophy

**"Precision meets Innovation"**

A minimal, commanding digital presence that speaks through restraint. Every element serves a purpose. The design should feel like walking into a well-architected system — clean, intentional, and subtly powerful.

## Core Principles

1. **Negative space is essential** — let elements breathe, never crowd
2. **Subtle over flashy** — guide attention, never distract
3. **Tech-forward aesthetic** — evoke AI/neural networks without being literal
4. **Confidence through restraint** — say more with less
5. **Precision in every detail** — pixel-perfect, intentional choices

---

## Color Palette

### Dark Theme (Primary)

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| Void | `#0D0D0D` | 13, 13, 13 | Primary background |
| Graphite | `#1A1A1A` | 26, 26, 26 | Cards, secondary surfaces |
| Smoke | `#2D2D2D` | 45, 45, 45 | Borders, dividers |
| Steel | `#4A4A4A` | 74, 74, 74 | Muted text, icons |

### Accent Colors

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| Signal Orange | `#FF6B35` | 255, 107, 53 | Primary accent, CTAs, highlights |
| Ember | `#FF8C5A` | 255, 140, 90 | Hover states, gradients |
| Glow | `#FFAA80` | 255, 170, 128 | Subtle highlights, glows |

### Neutral Colors

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| Pure | `#FFFFFF` | 255, 255, 255 | Headlines, primary text |
| Mist | `#B3B3B3` | 179, 179, 179 | Body text |
| Fog | `#666666` | 102, 102, 102 | Secondary text, captions |

### Color Usage Rules

- Orange is **surgical** — use sparingly for maximum impact
- Never use orange for large areas; it's for accents only
- Dark backgrounds should dominate (80%+ of surface area)
- Text contrast must meet WCAG AA minimum (4.5:1 for body)

---

## Typography

### Font Stack

| Purpose | Font | Fallbacks |
|---------|------|-----------|
| Display/Headlines | Space Grotesk | -apple-system, sans-serif |
| Body | Inter | -apple-system, BlinkMacSystemFont, sans-serif |
| Code (optional) | JetBrains Mono | Fira Code, monospace |

### Type Scale

| Element | Size | Weight | Letter Spacing |
|---------|------|--------|----------------|
| Hero Title | 72-96px (clamp) | 600 | -0.02em |
| Section Title | 48-56px (clamp) | 500 | -0.01em |
| Subsection | 24-32px | 500 | 0 |
| Body Large | 18-20px | 400 | 0.01em |
| Body | 16px | 400 | 0.01em |
| Caption | 14px | 400 | 0.02em |
| Label | 12px | 500 | 0.08em (uppercase) |

### Typography Rules

- Headlines: Negative letter-spacing (tighter)
- Body: Slight positive letter-spacing (more open)
- Max line width: ~65 characters for optimal readability
- Line height: 1.6-1.8 for body text

---

## Spacing System

Based on an 8px grid.

| Token | Value | Usage |
|-------|-------|-------|
| xs | 8px | Tight gaps, icon padding |
| sm | 16px | Standard element spacing |
| md | 32px | Section internal padding |
| lg | 64px | Between major elements |
| xl | 128px | Section vertical padding |
| 2xl | 256px | Hero/dramatic spacing |

### Spacing Rules

- Sections: Minimum 128px vertical padding
- Content max-width: 1200px (800px for text-heavy)
- Let elements float in space — asymmetry creates interest
- When in doubt, add more space

---

## Component Patterns

### Buttons
- Ghost style (transparent with orange border)
- Fill on hover (orange background, dark text)
- Subtle glow on hover
- Uppercase, letter-spaced labels

### Cards
- Dark graphite background
- Subtle smoke border
- Orange top-line reveal on hover
- Lift effect (translateY -4px)

### Links
- Mist color default, pure white on hover
- Underline animation (grows from left)
- Orange underline color

### Section Headers
- Small uppercase label (orange)
- Large title below
- Orange accent line (60px wide, 2px tall)

---

## Visual Inspiration

### Reference Sites
- **Linear.app** — Clean dark UI, purposeful motion
- **Vercel.com** — Tech-forward, commanding
- **Stripe.com** — Subtle animations, gradients
- **Apple.com** — Negative space mastery

### Mood Keywords
- Architectural
- Nocturnal
- Precise
- Forward
- Restrained
