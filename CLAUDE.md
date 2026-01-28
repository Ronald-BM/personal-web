# CLAUDE.md — Ronald Scheffers Projects

## How to Use This File

This project uses **skill files** to maintain consistent brand identity, design, and tone across all work. Before starting any task, load the relevant skills.

### Loading Skills

**Always read the skill files before doing design, copy, or visual work:**

```
.claude/skills/brand-identity.md     → WHO Ronald is, what NOT to mention
.claude/skills/design-system.md      → Colors, typography, spacing, components
.claude/skills/tone-of-voice.md      → Copy guidelines, word choices, patterns
.claude/skills/animation-principles.md → Motion design, timing, performance
```

### When to Load Which Skills

| Task | Skills to Load |
|------|----------------|
| Writing copy | brand-identity, tone-of-voice |
| UI/visual design | brand-identity, design-system, animation-principles |
| Full page/feature | All four skills |
| Code review (style) | design-system, animation-principles |
| Content editing | tone-of-voice |

---

## Quick Context

**Ronald Scheffers** — CTO of an AI Automation Agency.

**Critical rule:** Never explicitly mention the agency or CTO role. The expertise should be implied through sophisticated design and AI-focused messaging.

**Brand essence:** "Precision meets Innovation" — minimal, commanding, tech-forward.

---

## Skill Summaries

### Brand Identity
- Ronald helps businesses automate and implement AI
- Never mention "agency" or "CTO" explicitly
- Convey technical depth, strategic thinking, quiet confidence

### Design System
- Dark theme: Void `#0D0D0D`, Graphite `#1A1A1A`
- Accent: Signal Orange `#FF6B35`
- Fonts: Space Grotesk (headlines), Inter (body)
- Generous negative space, 8px grid

### Tone of Voice
- Confident, concise, active voice
- Outcome-focused, slightly provocative
- Avoid: buzzwords, jargon, explicit agency mentions
- Example: "I make machines do the work. So humans can do the thinking."

### Animation Principles
- Purposeful, subtle, physics-based
- Particle networks, scroll reveals, cursor glow
- Always respect `prefers-reduced-motion`

---

## Using Skills in Other Projects

To use these skills in another project:

1. Copy the `.claude/skills/` directory to the new project
2. Copy this `CLAUDE.md` file
3. Add any project-specific context below the skills section
4. Remove or modify skills that don't apply

The skills are designed to be **modular** — use what you need, ignore what you don't.

---

## Project-Specific Notes

*Add any notes specific to this project below:*

### Current Website Sections
1. Hero — Name, tagline, particle animation
2. About — "Intelligence by design"
3. Work — Automate, AI Strategy, Intelligent Integration
4. Contact — "What could you automate?"
5. Footer — Copyright, LinkedIn

### Files
- `index.html` — Main single-page website
- `STYLE_GUIDE.md` — Detailed design documentation (legacy, see skills instead)
