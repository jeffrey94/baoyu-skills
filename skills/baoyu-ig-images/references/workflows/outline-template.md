# Instagram Carousel Outline Template

Template for generating carousel infographic series outlines with layout specifications.

## File Naming

Outline files use strategy identifier in the name:
- `outline-strategy-a.md` - Story-driven variant
- `outline-strategy-b.md` - Information-dense variant
- `outline-strategy-c.md` - Visual-first variant
- `outline.md` - Final selected (copied from chosen variant)

## Image File Naming

Images use meaningful slugs for readability:
```
NN-{type}-[slug].png
NN-{type}-[slug].md (in prompts/)
```

| Type | Usage |
|------|-------|
| `cover` | First image (cover slide) |
| `content` | Middle content slides |
| `ending` | Last image |

**Examples**:
- `01-cover-morning-routine.png`
- `02-content-why-it-matters.png`
- `03-content-tip-one.png`
- `04-content-tip-two.png`
- `05-content-tip-three.png`
- `06-content-framework.png`
- `07-ending-take-action.png`

**Slug rules**:
- Derived from slide content (kebab-case)
- Must be unique within the series
- Keep short but descriptive (2-4 words)

## Layout Selection Guide

### Density-Based Layouts

| Layout | When to Use | Info Points | Whitespace |
|--------|-------------|-------------|------------|
| sparse | Covers, quotes, impact statements | 1-2 | 60-70% |
| balanced | Standard content, key ideas | 2-3 | 50-60% |
| dense | Knowledge cards, cheat sheets | 3-5 | 30-40% |

### Structure-Based Layouts

| Layout | When to Use | Structure |
|--------|-------------|-----------|
| list | Rankings, checklists, steps | Numbered/bulleted vertical (3-5 items) |
| comparison | Before/after, pros/cons, do/don't | Left vs right split |
| flow | Processes, timelines | Connected nodes with arrows (3-5 steps) |

### Position-Based Recommendations

| Position | Recommended | Reasoning |
|----------|-------------|-----------|
| Cover (Slide 1) | sparse | Maximum impact, grid-safe title |
| Slide 2 | sparse/balanced | Must independently hook (IG re-serve) |
| Core (Middle) | balanced/list/comparison | Match content — one idea per slide |
| Payoff | balanced/list | Clear takeaways |
| Ending | sparse | Clean CTA, memorable |

## Instagram Text Density Guidelines

IG carousel slides should have significantly LESS text than other platforms:

| Element | Word Target | Example |
|---------|-------------|---------|
| Headline | 3-8 words | "Stop Making This Mistake" |
| Subheadline | 5-12 words | "Here's what successful people do instead" |
| Body point | 5-15 words | "Use the 2-minute rule for small tasks" |
| CTA | 3-8 words | "Save this for later" |

**Rule of thumb**: If you can't read a slide in 3-5 seconds, there's too much text.

## Outline Format

```markdown
# Instagram Carousel Infographic Series Outline

---
strategy: a  # a, b, or c
name: Story-Driven
style: editorial
default_layout: balanced
image_count: 7
generated: YYYY-MM-DD HH:mm
---

## Slide 1 of 7

**Position**: Cover
**Layout**: sparse
**Hook**: "The #1 mistake killing your morning routine"
**Slug**: morning-mistake
**Filename**: 01-cover-morning-mistake.png

**Text Content**:
- Title: The #1 Mistake Killing Your Morning Routine
- Subtitle: And what to do instead

**Visual Concept**:
Split composition — chaotic left vs serene right,
warm golden tones, editorial typography

**Swipe Hook**: Here's what most people get wrong →

---

## Slide 2 of 7

**Position**: Content (Second Chance)
**Layout**: sparse
**Core Message**: The problem everyone faces
**Slug**: the-problem
**Filename**: 02-content-the-problem.png

**Text Content**:
- Title: "You're starting your day in reaction mode"
- Supporting: Checking phone → emails → social media → already stressed

**Visual Concept**:
Phone screen glow in dark room,
single impactful visual with bold text overlay

**Swipe Hook**: Here's what changed everything for me →

**Note**: This slide MUST work independently — IG may re-serve carousel from here.

---

## Slide 3 of 7

**Position**: Content
**Layout**: balanced
**Core Message**: The turning point
**Slug**: turning-point
**Filename**: 03-content-turning-point.png

**Text Content**:
- Title: "I tried the 5-5-5 method"
- Points:
  - 5 min meditation
  - 5 min journaling
  - 5 min movement

**Visual Concept**:
Clean three-part visual with icons,
warm tones, editorial layout

**Swipe Hook**: Here are the results after 30 days →

---

## Slide 7 of 7

**Position**: Ending
**Layout**: sparse
**Core Message**: Take action
**Slug**: take-action
**Filename**: 07-ending-take-action.png

**Text Content**:
- Title: "Your morning sets the tone for everything"
- CTA: Save this → Try it tomorrow → Share with someone who needs it

**Visual Concept**:
Clean, bright composition, bold CTA text,
save/share visual cues

---
```

## Swipe Hook Strategies

Each slide should end with a hook for the next:

| Strategy | Example |
|----------|---------|
| Arrow/continuation | "Here's how →" |
| Teaser | "And the most important one..." |
| Numbering | "Tip 3 of 7" |
| Superlative | "The next one changed everything" |
| Question | "But what about...?" |
| Promise | "The last one is the most powerful" |
| Open loop | Start an idea, resolve next slide |

## Strategy Differentiation

Three strategies should differ meaningfully:

| Strategy | Focus | Structure | Slide Count | Recommended Styles |
|----------|-------|-----------|-------------|-------------------|
| A: Story-Driven | Emotional, personal | Hook → Problem → Turning Point → Transformation → Lessons → CTA | 6-8 | soft-muted, earthy-organic, editorial |
| B: Information-Dense | Factual, scannable | Bold Claim → Key Points → Details → Framework → CTA | 5-7 | clean-minimal, line-art, bold-graphic |
| C: Visual-First | Atmospheric, minimal text | Hero → Mood → Impact → Statement → CTA | 4-6 | dark-cinematic, neon-gradient, retro-nostalgia |

**Example for "7 AI Productivity Tools"**:
- `outline-strategy-a.md`: Editorial + Balanced — Personal journey discovering these tools
- `outline-strategy-b.md`: Clean-Minimal + List — One tool per slide, scannable format
- `outline-strategy-c.md`: Neon-Gradient + Sparse — Futuristic visual showcase, minimal text

## Slide 2 Rule

Instagram may re-serve carousels starting from slide 2 (not always the cover). Therefore:

**Slide 2 MUST**:
- Work as a standalone hook without slide 1 context
- Have its own compelling visual and headline
- Not start with "As I mentioned..." or reference slide 1
- Be independently save/share-worthy

**Good slide 2 examples**:
- "The biggest myth about productivity" (curiosity gap)
- A striking statistic or data point
- A bold, controversial statement
- A relatable scenario ("You wake up, grab your phone...")

## Grid Preview Consideration

The cover slide (slide 1) appears on the user's IG profile grid, center-cropped to approximately 3:4 from 4:5.

**Design implication**: Keep the essential content (title, key visual) within the center 3:4 area. Avoid placing critical text at the very top or bottom edges of the 4:5 frame.

```
┌─────────────────────────┐
│   ↑ may be cropped ↑    │
│  ┌───────────────────┐  │
│  │                   │  │
│  │  KEY CONTENT HERE │  │  ← Center 3:4 = grid-safe
│  │                   │  │
│  └───────────────────┘  │
│   ↓ may be cropped ↓    │
└─────────────────────────┘
```
