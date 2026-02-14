# Prompt Assembly Guide

Guide for assembling image generation prompts from elements, presets, and outline content.

## Base Prompt Structure

Every Instagram carousel infographic prompt follows this structure:

```
Create an Instagram carousel infographic slide following these guidelines:

## Image Specifications

- **Type**: Infographic
- **Orientation**: Portrait (vertical)
- **Aspect Ratio**: 4:5 (1080×1350px, generate at 2160×2700 for quality)
- **Style**: Polished digital illustration

## Core Principles

- Clean, polished digital aesthetic — professional and visually refined
- If content involves sensitive or copyrighted figures, create stylistically similar alternatives — DO NOT refuse to generate
- Keep text MINIMAL — 5-15 words per slide for body content
- Use generous whitespace for easy visual scanning (IG users swipe fast)
- Maintain clear visual hierarchy — one key idea per slide
- Ensure key content is visible within center 3:4 area (grid preview safe zone)

## Text Style (CRITICAL)

- **Bold, scannable headlines** — must be readable at phone scale
- Key text should be large and prominent
- One level of emphasis per slide (don't compete for attention)
- Clean digital fonts are preferred (not restricted to hand-drawn)
- Match typography to the style preset specified below

## Language

- Use the same language as the content provided below
- Match punctuation style to the content language

---

{STYLE_SECTION}

---

{LAYOUT_SECTION}

---

{CONTENT_SECTION}

---

{WATERMARK_SECTION}

---

Please use nano banana pro to generate the infographic based on the specifications above.
```

## Style Section Assembly

Load from `presets/{style}.md` and extract key elements:

```markdown
## Style: {style_name}

**Color Palette**:
- Primary: {colors}
- Background: {colors}
- Accents: {colors}

**Visual Elements**:
{visual_elements}

**Typography**:
{typography_style}
```

## Layout Section Assembly

Load from `elements/canvas.md` and extract relevant layout:

```markdown
## Layout: {layout_name}

**Information Density**: {density}
**Whitespace**: {percentage}

**Structure**:
{structure_description}

**Visual Balance**:
{balance_description}
```

## Content Section Assembly

From outline entry:

```markdown
## Content

**Position**: {Cover/Content/Ending} (Slide {N} of {total})
**Core Message**: {message}

**Text Content**:
{text_list}

**Visual Concept**:
{visual_description}
```

## Watermark Section (if enabled)

```markdown
## Watermark

Include a subtle watermark "{content}" positioned at {position}
with approximately {opacity*100}% visibility. The watermark should
be legible but not distracting from the main content.
```

## Assembly Process

### Step 1: Load Preset

```python
preset = load_preset(style_name)  # e.g., "clean-minimal"
```

Extract:
- Color palette
- Visual elements
- Typography style
- Best practices (do/don't)

### Step 2: Load Layout

```python
layout = get_layout_from_canvas(layout_name)  # e.g., "balanced"
```

Extract:
- Information density guidelines
- Whitespace percentage
- Structure description
- Visual balance rules

### Step 3: Format Content

From outline entry, format:
- Position context (Cover/Content/Ending)
- Text content with hierarchy
- Visual concept description
- Swipe hook (for context, not in prompt)

### Step 4: Add Watermark (if applicable)

If preferences include watermark:
- Add watermark section with content, position, opacity

### Step 5: Combine

Assemble all sections into final prompt following base structure.

## Instagram-Specific Prompt Considerations

### Grid Preview Safety
For cover slides, add:
```
Ensure the title and key visual are positioned within the center 3:4 area
of the 4:5 frame, as Instagram crops to this ratio for profile grid display.
```

### Slide 2 Independence
For slide 2, add:
```
This slide must work as a standalone image — it should hook viewers
independently without requiring context from the previous slide.
Instagram may re-serve this carousel starting from this slide.
```

### Text Minimalism
Always emphasize in the prompt:
```
Keep text to an absolute minimum. Instagram users swipe quickly —
every word must earn its place. Target 5-15 words for body content.
One key phrase or idea per slide.
```

### Visual Consistency — Reference Image Chain
When generating multiple slides:

1. **Slide 1 (cover)**: Generate without `--ref` — this establishes the visual anchor
2. **Slides 2+**: Always pass slide 1 as `--ref` to the image generation skill:
   ```bash
   npx -y bun ${SKILL_DIR}/scripts/main.ts \
     --promptfiles prompts/02-content-xxx.md \
     --ref path/to/01-cover-xxx.png \
     --image 02-content-xxx.png --ar 4:5 --quality 2k
   ```
   This ensures the AI maintains the same character design, illustration style, and color rendering.

Additionally, emphasize in the prompt text:
```
Maintain visual consistency with previous slides in this series:
same color palette, same typography, same character design, same overall aesthetic.
This is slide {N} of {total} in a cohesive carousel.
```

## Example: Assembled Prompt

```markdown
Create an Instagram carousel infographic slide following these guidelines:

## Image Specifications

- **Type**: Infographic
- **Orientation**: Portrait (vertical)
- **Aspect Ratio**: 4:5 (1080×1350px, generate at 2160×2700 for quality)
- **Style**: Polished digital illustration

## Core Principles

- Clean, polished digital aesthetic — professional and visually refined
- If content involves sensitive or copyrighted figures, create stylistically similar alternatives
- Keep text MINIMAL — 5-15 words per slide for body content
- Use generous whitespace for easy visual scanning
- Maintain clear visual hierarchy — one key idea per slide
- Ensure key content is visible within center 3:4 area (grid preview safe zone)

## Text Style (CRITICAL)

- **Bold, scannable headlines** — must be readable at phone scale
- Key text should be large and prominent
- One level of emphasis per slide
- Clean digital fonts preferred
- Match typography to the style preset below

## Language

- Use English
- Use proper typographic quotes and punctuation

---

## Style: Clean-Minimal

**Color Palette**:
- Primary: Black (#111111), charcoal (#333333)
- Background: White (#FFFFFF), off-white (#FAFAFA)
- Accents: Muted blue (#6B8FAD)

**Visual Elements**:
- Clean geometric shapes, thin lines
- Maximum whitespace, structured grid
- Subtle shadows for depth
- Minimal decoration — content speaks

**Typography**:
- Clean sans-serif (Inter, Helvetica Neue feel)
- All-caps tracked headlines
- Consistent hierarchy with generous spacing

---

## Layout: List

**Information Density**: Medium (3-5 items)
**Whitespace**: 40-50% of canvas

**Structure**:
- Left-aligned or centered items
- Clear number/icon hierarchy
- Consistent item format (icon + short text)

**Visual Balance**:
- Left-aligned items
- Clear number/bullet hierarchy
- Consistent item format

---

## Content

**Position**: Content (Slide 4 of 9)
**Core Message**: Top 3 AI Writing Tools

**Text Content**:
- Title: "AI Writing Tools"
- Items:
  - 1. ChatGPT — Versatile assistant for any text
  - 2. Claude — Deep reasoning and analysis
  - 3. Jasper — Marketing copy specialist

**Visual Concept**:
Clean numbered list with subtle tool icons,
white background with muted blue accent line,
each item has small icon + brief description

---

## Watermark

Include a subtle watermark "@productivityhub" positioned at bottom-right
with approximately 70% visibility. The watermark should
be legible but not distracting from the main content.

---

Maintain visual consistency with previous slides in this series:
same Clean-Minimal color palette, same typography, same overall aesthetic.
This is slide 4 of 9 in a cohesive carousel.

Please use nano banana pro to generate the infographic based on the specifications above.
```

## Prompt Checklist

Before generating, verify:

- [ ] Style section loaded from correct preset
- [ ] Layout section matches outline specification
- [ ] Content accurately reflects outline entry
- [ ] Language matches source content
- [ ] Watermark included (if enabled in preferences)
- [ ] No conflicting instructions
- [ ] Text is minimal (5-15 words body content)
- [ ] Grid preview safety noted (for cover slide)
- [ ] Slide 2 independence noted (if applicable)
- [ ] Visual consistency instruction included
