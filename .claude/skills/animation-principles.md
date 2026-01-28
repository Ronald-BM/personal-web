# Skill: Animation Principles — Ronald Scheffers

## Core Philosophy

Animation should feel like **intelligence in motion** — purposeful, precise, and never gratuitous.

## Guiding Principles

| Principle | Description |
|-----------|-------------|
| **Purposeful** | Every animation guides attention or provides feedback. Never decorative. |
| **Subtle** | Micro-interactions over dramatic movements. Users should feel it, not see it. |
| **Physics-based** | Natural easing with momentum. Slight overshoot on stops. |
| **Performant** | CSS transforms only. 60fps minimum. No jank. |
| **Respectful** | Always honor `prefers-reduced-motion`. |

---

## Timing Functions

### CSS Custom Properties

```css
/* Smooth entrance — elements appearing */
--ease-out: cubic-bezier(0.16, 1, 0.3, 1);

/* Interactive feedback — buttons, toggles */
--ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);

/* Snappy micro-interactions — small UI elements */
--ease-snap: cubic-bezier(0.34, 1.56, 0.64, 1);
```

### When to Use Each

| Easing | Use Case |
|--------|----------|
| ease-out | Page transitions, reveals, modal opens |
| ease-in-out | Hovers, toggles, state changes |
| ease-snap | Button clicks, micro-feedback, small movements |

---

## Animation Catalog

### 1. Scroll Reveal

Elements fade up as they enter viewport.

```
Duration: 600-800ms
Transform: translateY(30px) → translateY(0)
Opacity: 0 → 1
Trigger: IntersectionObserver at 10% visibility
Stagger: 50-100ms between siblings
```

### 2. Particle Network

Ambient floating nodes that connect when nearby. Evokes neural networks / AI.

```
Particle count: 40-60
Movement: 0.3-0.5px per frame drift
Connection distance: 150px
Connection opacity: 15% max, fades with distance
Particle opacity: 60%
Color: Signal Orange (#FF6B35)
```

### 3. Cursor Glow

Subtle orange radial gradient follows cursor with delay.

```
Size: 300px diameter
Opacity: 8%
Delay: Lerp at 0.1 factor (smooth follow)
Color: Signal Orange
Hide on: touch devices, reduced motion
```

### 4. Scroll Progress Bar

Thin line at top of viewport showing page progress.

```
Height: 2px
Color: Signal Orange
Position: Fixed, top: 0
Animation: Width 0% → 100% based on scroll
```

### 5. Card Hover

Cards lift and glow on hover.

```
Transform: translateY(-4px)
Border: Smoke → Signal Orange
Shadow: 0 20px 40px rgba(0,0,0,0.4)
Top line: scaleX(0) → scaleX(1)
Duration: 400ms
```

### 6. Button Fill

Ghost buttons fill with color on hover.

```
Background: translateX(-100%) → translateX(0)
Text color: Orange → Void (dark)
Glow: 0 0 30px rgba(255,107,53,0.3)
Duration: 300ms
Active: scale(0.98)
```

### 7. Link Underline

Underlines grow from left on hover.

```
Width: 0% → 100%
Height: 1px
Color: Signal Orange
Origin: Left
Duration: 300ms
```

### 8. Staggered Children

Child elements animate in sequence.

```
Base delay: 100ms
Increment: 50-100ms per child
Max children: 4-6 (avoid long waits)
```

---

## Reduced Motion

Always provide a reduced motion fallback:

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }

  .cursor-glow,
  .particles {
    display: none;
  }
}
```

---

## Performance Rules

1. **Only animate transforms and opacity** — these don't trigger layout
2. **Use `will-change` sparingly** — only on elements that will animate
3. **Avoid animating during scroll** — except progress indicators
4. **Test on low-end devices** — if it jitters, simplify
5. **Use `requestAnimationFrame`** — for JS animations

---

## What NOT to Animate

- Text size or line-height
- Layout properties (width, height, padding, margin)
- Colors on large surfaces (expensive)
- Multiple properties simultaneously on mobile
- Anything that distracts from content

---

## Quick Reference

| Animation | Duration | Easing |
|-----------|----------|--------|
| Reveal on scroll | 600-800ms | ease-out |
| Hover states | 300-400ms | ease-out |
| Button click | 150ms | ease-snap |
| Page transition | 400-600ms | ease-in-out |
| Particle drift | Continuous | Linear |
| Cursor follow | Continuous | Lerp 0.1 |
