# Instagram Content Analysis Framework

Deep analysis framework tailored for Instagram's unique engagement patterns and carousel format.

## Purpose

Before creating carousel infographics, thoroughly analyze the source material to:
- Maximize hook power and swipe motivation
- Identify save-worthy and share-worthy elements
- Plan the visual narrative arc
- Match content to optimal style/layout

## Platform Characteristics

Instagram carousel engagement is driven by:
- **Hook Power**: Cover image decides 90% of engagement — must stop the scroll
- **Slide 2 Rule**: IG may re-serve carousels starting from slide 2, so it must independently hook
- **Save Value**: Saves are the #1 algorithm signal — content worth bookmarking
- **Share/DM Value**: DM shares are the #2 signal — "send this to someone who needs it"
- **Dwell Time**: Time spent on each slide signals quality to the algorithm
- **Swipe-Through Rate**: Each slide must compel users to continue swiping

## Analysis Dimensions

### 1. Content Type Classification

| Type | Characteristics | Best Style | Best Layout |
|------|----------------|------------|-------------|
| Educational carousel | Tips, how-to, tutorials, frameworks | clean-minimal, line-art | balanced/list |
| Listicle | Rankings, recommendations, collections | clean-minimal, bold-graphic | list/dense |
| Comparison | This vs that, do/don't, myth/fact | bold-graphic, editorial | comparison |
| Story/transformation | Before/after, journey, personal growth | soft-muted, editorial | balanced |
| Quote/inspiration | Motivation, thought leadership, wisdom | dark-cinematic, editorial | sparse |
| Behind-the-scenes | Process reveals, day-in-life, making-of | earthy-organic, retro-nostalgia | balanced/flow |
| Data/stats | Research findings, industry insights, numbers | neon-gradient, clean-minimal | dense/list |

### 2. Hook Analysis

Evaluate title/hook potential using Instagram-specific patterns:

**Hook Types**:
- **Curiosity gap**: "The #1 mistake...", "Nobody talks about this...", "What they don't tell you..."
- **Number hooks**: "7 tips that will...", "5 things you need...", "3 rules for..."
- **Challenge/controversy**: "Stop doing this!", "Unpopular opinion:", "This is why you're failing"
- **Promise hooks**: "How I saved $10K...", "This changed everything", "The only guide you need"
- **Identity hooks**: "Entrepreneurs need this", "If you're a designer...", "For my overthinkers..."

**Rating Scale**:
- 5/5: Multiple strong hooks combined — viral potential
- 4/5: Clear hook with room for enhancement
- 3/5: Basic hook, needs strengthening
- 2/5: Weak hook, requires significant improvement
- 1/5: No clear hook

### 3. Target Audience

| Audience | Interests | Preferred Style | Content Focus |
|----------|-----------|-----------------|---------------|
| Entrepreneurs/founders | Growth, systems, strategy | clean-minimal, bold-graphic | Frameworks, tactics, mindset |
| Creators/designers | Tools, aesthetics, workflow | neon-gradient, playful-pop | Tips, resources, inspiration |
| Wellness/lifestyle | Self-care, routines, balance | soft-muted, earthy-organic | Guides, rituals, recommendations |
| Fashion/beauty | Trends, styling, products | editorial, retro-nostalgia | Curations, reviews, looks |
| Tech/developers | Tools, concepts, tutorials | line-art, clean-minimal | How-tos, explanations, comparisons |
| Students/learners | Study tips, concepts, career | playful-pop, line-art | Cheat sheets, guides, motivation |
| Premium brands | Luxury, exclusivity, quality | dark-cinematic, editorial | Showcase, storytelling, authority |

### 4. Engagement Potential

**Save Triggers (bookmark value)**:
- Is it reference material? (checklists, templates, frameworks) → High save
- Is it a step-by-step guide? → High save
- Is it a curated list? → High save
- Would someone come back to this later? → High save
- Is it time-sensitive news? → Low save

**Share/DM Triggers**:
- "My friend needs to see this" → relatable, useful
- "Tag someone who does this" → identity-based
- "Send this to your coworker" → professional utility
- Controversial take → "what do you think about this?"

**Comment Triggers**:
- Open-ended questions: "Which one are you?"
- Debate starters: "Agree or disagree?"
- Experience sharing: "Drop your favorite in comments"
- Polls: "Option A or Option B?"

**Dwell Time Optimizers**:
- Information density that rewards slow reading
- Multi-step content requiring slide-by-slide consumption
- Visual complexity that invites exploration

### 5. Visual Opportunity Map

| Content Element | Visual Treatment | Example |
|-----------------|------------------|---------|
| Data/statistics | Oversized numbers, simple charts | "80% of people..." with giant "80%" |
| Comparison | Before/after, side-by-side split | Left vs right with clear divider |
| Steps/process | Numbered flow, connected nodes | 1→2→3 with icons per step |
| Checklist | Clean check/cross icons | ✓/✗ list with brief labels |
| Quote | Large text on minimal background | Pull-quote with attribution |
| Product/tool | Clean showcase with labels | Product with feature callouts |
| Transformation | Before→after with arrow | Two states with clear contrast |

### 6. Swipe Flow Design

Plan the narrative arc across slides:

| Position | Purpose | Hook Strategy |
|----------|---------|---------------|
| **Cover (Slide 1)** | Stop the scroll | Strongest visual + compelling title |
| **Slide 2 (Second Chance)** | Re-hook (IG re-serve) | Must work independently — don't assume slide 1 context |
| **Setup (Slide 2-3)** | Build context | Relatable problem or curiosity |
| **Core (Middle)** | Deliver value | One key idea per slide, scannable |
| **Payoff (Near end)** | Practical takeaway | Actionable summary or framework |
| **Ending (Last)** | Drive action | CTA: save, share, follow, comment |

**Swipe Motivation Between Slides**:
- End each slide with a visual or textual hook for the next
- Use open loops: start an idea, resolve it on the next slide
- Progressive revelation: "and the most important one..."
- Numbering creates expectation: "Tip 3 of 7" → must see the rest
- Mid-sentence breaks across slides (use sparingly)

## Output Format

Analysis results should be saved to `analysis.md` with:

```yaml
---
title: "7 AI Tools That Will 10x Your Productivity"
topic: AI productivity tools
content_type: educational-listicle
source_language: en
user_language: en
recommended_image_count: 9
---

## Target Audience

- **Primary**: Entrepreneurs and knowledge workers — seeking productivity gains
- **Secondary**: Creators and freelancers — need AI tools for workflow
- **Tertiary**: Students — looking for study/work efficiency

## Hook Analysis

**Hook Rating**: 4/5
- ✓ Number hook: "7"
- ✓ Promise hook: "10x Your Productivity"
- △ Could strengthen: Add identity hook "Every entrepreneur needs..."

**Suggested optimization**:
- Original: "7 AI Tools That Will 10x Your Productivity"
- Enhanced: "7 AI Tools Every Entrepreneur Needs (I use #4 daily)"

## Value Proposition

**Why would someone save this?**
1. **Reference value**: Tool list they can come back to
2. **Utility**: Directly actionable recommendations
3. **FOMO**: Others are using these tools

**Save likelihood**: High
**Share likelihood**: Medium-high (tag a friend who needs this)

## Engagement Design

- **Save trigger**: Curated tool list = bookmark material
- **Share trigger**: "Send this to your coworker who's still doing everything manually"
- **Comment prompt**: "Which one is your favorite? Drop it below"
- **Dwell time**: Detailed enough per slide to reward reading

## Content Signals

- "AI tools" → clean-minimal + list
- "Productivity" → clean-minimal + balanced
- "Listicle format" → bold-graphic + list

## Swipe Flow

| Slide | Position | Purpose | Hook |
|-------|----------|---------|------|
| 1 | Cover | Stop scroll | Bold title + visual impact |
| 2 | Setup | Context (re-hook) | Why you need AI tools now |
| 3-8 | Core | Value delivery | One tool per slide with key benefit |
| 9 | Ending | Action | Summary + save/share CTA |

## Recommended Approaches

1. **Clean-Minimal + List** — Professional, scannable (recommended)
2. **Bold-Graphic + List** — High-impact dark mode aesthetic
3. **Line-Art + Balanced** — Illustrated, educational feel
```

## Analysis Checklist

Before proceeding to outline generation:

- [ ] Can I identify the content type?
- [ ] Is the hook strong enough? (3+ rating)
- [ ] Do I know the primary audience?
- [ ] Have I identified save/share triggers?
- [ ] Are there clear visual opportunities?
- [ ] Is the swipe flow planned?
- [ ] Have I selected 3 style+layout combinations?
- [ ] Does slide 2 work independently? (IG re-serve check)
