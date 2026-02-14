---
name: baoyu-ig-images
description: Generates Instagram carousel infographic series with 10 visual styles and 8 layouts. Breaks content into 4-10 polished slides optimized for IG engagement (saves, shares, dwell time). Use when user mentions "Instagram images", "IG carousel", "Instagram infographics", "IG slides", or wants social media infographics for Instagram.
---

# Instagram Carousel Infographic Series Generator

Break down complex content into polished, swipe-worthy Instagram carousel infographic series with multiple style options.

## Usage

```bash
# Auto-select style and layout based on content
/baoyu-ig-images posts/ai-future/article.md

# Specify style
/baoyu-ig-images posts/ai-future/article.md --style clean-minimal

# Specify layout
/baoyu-ig-images posts/ai-future/article.md --layout balanced

# Combine style and layout
/baoyu-ig-images posts/ai-future/article.md --style editorial --layout list

# Direct content input
/baoyu-ig-images
[paste content]

# Direct input with options
/baoyu-ig-images --style bold-graphic --layout comparison
[paste content]
```

## Options

| Option | Description |
|--------|-------------|
| `--style <name>` | Visual style (see Style Gallery) |
| `--layout <name>` | Information layout (see Layout Gallery) |

## Two Dimensions

| Dimension | Controls | Options |
|-----------|----------|---------|
| **Style** | Visual aesthetics: colors, mood, decorations | clean-minimal, bold-graphic, soft-muted, editorial, retro-nostalgia, neon-gradient, earthy-organic, dark-cinematic, playful-pop, line-art |
| **Layout** | Information structure: density, arrangement | sparse, balanced, dense, list, comparison, flow, mindmap, quadrant |

Style × Layout can be freely combined. Example: `--style editorial --layout balanced` creates a magazine-quality layout with refined typography and neutral tones.

## Style Gallery

| Style | Description |
|-------|-------------|
| `clean-minimal` (Default) | White space, structured, professional — polished Instagram aesthetic |
| `bold-graphic` | Deep black bg, neon accents, high contrast — attention-grabbing |
| `soft-muted` | Muted pastels, desaturated, gentle — lifestyle and wellness |
| `editorial` | Neutral palette, mixed serif+sans, magazine hierarchy — premium feel |
| `retro-nostalgia` | Warm 70s tones, film grain, Y2K pastels — trendy and cultural |
| `neon-gradient` | Electric blues, neon pinks, digital gradients — tech and futuristic |
| `earthy-organic` | Terracotta, olive, warm tan, natural textures — grounded and authentic |
| `dark-cinematic` | Dark charcoal/navy bg, jewel tone accents — dramatic and premium |
| `playful-pop` | Vibrant primaries, rounded bubbly shapes — energetic and fun |
| `line-art` | White bg, single ink color + pastels, illustrated — educational and clear |

Detailed style definitions: `references/presets/<style>.md`

## Layout Gallery

| Layout | Description |
|--------|-------------|
| `sparse` (Default) | Minimal information, maximum impact (1-2 points, 60-70% whitespace) |
| `balanced` | Standard content layout (2-3 points, 50-60% whitespace) |
| `dense` | Higher information density (3-5 points, 30-40% whitespace) |
| `list` | Enumeration and ranking format (3-5 items) |
| `comparison` | Side-by-side contrast layout |
| `flow` | Process and timeline layout (3-5 steps) |
| `mindmap` | Center radial mind map layout (4-6 branches) |
| `quadrant` | Four-quadrant / circular section layout |

Detailed layout definitions: `references/elements/canvas.md`

## Auto Selection

| Content Signals | Style | Layout |
|-----------------|-------|--------|
| Business, coaching, SaaS, productivity | `clean-minimal` | balanced/list |
| Announcements, bold claims, agencies | `bold-graphic` | sparse/list |
| Lifestyle, beauty, food, wellness | `soft-muted` | balanced/flow |
| Fashion, travel, luxury, photography | `editorial` | sparse/balanced |
| Music, culture, youth, throwback | `retro-nostalgia` | balanced/list |
| Tech, AI, gaming, digital, futuristic | `neon-gradient` | balanced/dense |
| Sustainability, nature, craft, organic | `earthy-organic` | balanced/flow |
| Premium brands, night themes, luxury | `dark-cinematic` | sparse/balanced |
| Youth brands, entertainment, fun | `playful-pop` | sparse/list |
| Education, how-to, concepts, tutorials | `line-art` | balanced/dense |

## Outline Strategies

Three differentiated outline strategies for different content goals:

### Strategy A: Story-Driven

| Aspect | Description |
|--------|-------------|
| **Concept** | Personal narrative thread, emotional resonance first |
| **Features** | Start from relatable hook, show transformation, strong authenticity |
| **Best for** | Personal stories, before/after, journey posts, brand stories |
| **Structure** | Hook → Relatable problem → Turning point → Transformation → CTA |
| **Slides** | 6-8 slides |
| **Recommended styles** | soft-muted, earthy-organic, editorial |

### Strategy B: Information-Dense

| Aspect | Description |
|--------|-------------|
| **Concept** | Value-first, efficient information delivery with visual clarity |
| **Features** | Clear structure, scannable points, expert credibility |
| **Best for** | Tips, tutorials, comparisons, checklists, tool recommendations |
| **Structure** | Bold claim → Key points → Details → Summary → CTA |
| **Slides** | 5-7 slides |
| **Recommended styles** | clean-minimal, line-art, bold-graphic |

### Strategy C: Visual-First

| Aspect | Description |
|--------|-------------|
| **Concept** | Visual impact as core, minimal text, atmosphere-driven |
| **Features** | Large visuals, mood-forward, instant aesthetic appeal |
| **Best for** | Mood boards, aesthetic content, brand showcase, high-design topics |
| **Structure** | Hero visual → Detail shots → Mood scenes → CTA |
| **Slides** | 4-6 slides |
| **Recommended styles** | dark-cinematic, neon-gradient, retro-nostalgia |

## File Structure

Each session creates an independent directory named by content slug:

```
ig-images/{topic-slug}/
├── source-{slug}.{ext}             # Source files (text, images, etc.)
├── analysis.md                     # Deep analysis + questions asked
├── outline-strategy-a.md           # Strategy A: Story-driven
├── outline-strategy-b.md           # Strategy B: Information-dense
├── outline-strategy-c.md           # Strategy C: Visual-first
├── outline.md                      # Final selected/merged outline
├── prompts/
│   ├── 01-cover-[slug].md
│   ├── 02-content-[slug].md
│   └── ...
├── 01-cover-[slug].png
├── 02-content-[slug].png
└── NN-ending-[slug].png
```

**Slug Generation**:
1. Extract main topic from content (2-4 words, kebab-case)
2. Example: "AI Tools for Creators" → `ai-tools-creators`

**Conflict Resolution**:
If `ig-images/{topic-slug}/` already exists:
- Append timestamp: `{topic-slug}-YYYYMMDD-HHMMSS`
- Example: `ai-tools` exists → `ai-tools-20260118-143052`

**Source Files**:
Copy all sources with naming `source-{slug}.{ext}`:
- `source-article.md`, `source-photo.jpg`, etc.
- Multiple sources supported: text, images, files from conversation

## Workflow

### Progress Checklist

Copy and track progress:

```
IG Carousel Infographic Progress:
- [ ] Step 0: Check preferences (EXTEND.md) ⛔ BLOCKING
  - [ ] Found → load preferences → continue
  - [ ] Not found → run first-time setup → MUST complete before Step 1
- [ ] Step 1: Analyze content → analysis.md
- [ ] Step 2: Confirmation 1 - Content understanding ⚠️ REQUIRED
- [ ] Step 3: Generate 3 outline + style variants
- [ ] Step 4: Confirmation 2 - Outline & style & elements selection ⚠️ REQUIRED
- [ ] Step 5: Generate images (sequential)
- [ ] Step 6: Completion report
```

### Flow

```
Input → [Step 0: Preferences] ─┬─ Found → Continue
                               │
                               └─ Not found → First-Time Setup ⛔ BLOCKING
                                              │
                                              └─ Complete setup → Save EXTEND.md → Continue
                                                                                      │
        ┌───────────────────────────────────────────────────────────────────────────┘
        ↓
Analyze → [Confirm 1] → 3 Outlines → [Confirm 2: Outline + Style + Elements] → Generate → Complete
```

### Step 0: Load Preferences (EXTEND.md) ⛔ BLOCKING

**Purpose**: Load user preferences or run first-time setup.

**CRITICAL**: If EXTEND.md not found, MUST complete first-time setup before ANY other questions or steps. Do NOT proceed to content analysis, do NOT ask about style, do NOT ask about layout — ONLY complete the preferences setup first.

Use Bash to check EXTEND.md existence (priority order):

```bash
# Check project-level first
test -f .baoyu-skills/baoyu-ig-images/EXTEND.md && echo "project"

# Then user-level (cross-platform: $HOME works on macOS/Linux/WSL)
test -f "$HOME/.baoyu-skills/baoyu-ig-images/EXTEND.md" && echo "user"
```

┌────────────────────────────────────────────────────┬───────────────────┐
│                        Path                        │     Location      │
├────────────────────────────────────────────────────┼───────────────────┤
│ .baoyu-skills/baoyu-ig-images/EXTEND.md             │ Project directory │
├────────────────────────────────────────────────────┼───────────────────┤
│ $HOME/.baoyu-skills/baoyu-ig-images/EXTEND.md       │ User home         │
└────────────────────────────────────────────────────┴───────────────────┘

┌───────────┬─────────────────────────────────────────────────────────────────────────────────────────────────────┐
│  Result   │                                              Action                                              │
├───────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Found     │ Read, parse, display summary → Continue to Step 1                                                 │
├───────────┼─────────────────────────────────────────────────────────────────────────────────────────────────────┤
│ Not found │ ⛔ BLOCKING: Run first-time setup ONLY (see below) → Complete and save EXTEND.md → Then Step 1    │
└───────────┴─────────────────────────────────────────────────────────────────────────────────────────────────────┘

**First-Time Setup** (when EXTEND.md not found):

**Language**: Use user's input language or saved language preference.

Use AskUserQuestion with ALL questions in ONE call. See `references/config/first-time-setup.md` for question details.

**EXTEND.md Supports**: Watermark | Preferred style/layout | Custom style definitions | Language preference

Schema: `references/config/preferences-schema.md`

### Step 1: Analyze Content → `analysis.md`

Read source content, save it if needed, and perform deep analysis.

**Actions**:
1. **Save source content** (if not already a file):
   - If user provides a file path: use as-is
   - If user pastes content: save to `source.md` in target directory
   - **Backup rule**: If `source.md` exists, rename to `source-backup-YYYYMMDD-HHMMSS.md`
2. Read source content
3. **Deep analysis** following `references/workflows/analysis-framework.md`:
   - Content type classification (educational, listicle, comparison, story, quote, BTS, data)
   - Hook analysis (curiosity gap, number hook, challenge, promise, identity)
   - Target audience identification
   - Engagement potential (saves, shares, comments, dwell time)
   - Visual opportunity mapping
   - Swipe flow design
4. Detect source language
5. Determine recommended image count (4-10, sweet spot 8-10)
6. **Generate clarifying questions** (see Step 2)
7. **Save to `analysis.md`**

### Step 2: Confirmation 1 - Content Understanding ⚠️

**Purpose**: Validate understanding + collect missing info. **Do NOT skip.**

**Display summary**:
- Content type + topic identified
- Key points extracted
- Tone detected
- Source images count

**Use AskUserQuestion** for:
1. Core value proposition (multiSelect: true)
2. Target audience
3. Tone preference: Authentic / Expert authority / Aspirational / Auto
4. Additional context (optional)

**After response**: Update `analysis.md` → Step 3

### Step 3: Generate 3 Outline + Style Variants

Based on analysis + user context, create three distinct strategy variants. Each variant includes both **outline structure** and **visual style recommendation**.

**For each strategy**:

| Strategy | Filename | Outline | Recommended Style |
|----------|----------|---------|-------------------|
| A | `outline-strategy-a.md` | Story-driven: emotional, transformation | soft-muted, earthy-organic, editorial |
| B | `outline-strategy-b.md` | Information-dense: structured, scannable | clean-minimal, line-art, bold-graphic |
| C | `outline-strategy-c.md` | Visual-first: atmospheric, minimal text | dark-cinematic, neon-gradient, retro-nostalgia |

**Outline format** (YAML front matter + content):
```yaml
---
strategy: a  # a, b, or c
name: Story-Driven
style: editorial  # recommended style for this strategy
style_reason: "Magazine-quality layout enhances personal narrative with sophistication"
elements:  # from style preset, can be customized in Step 4
  background: neutral-warm
  decorations: [editorial-frames, minimal-lines]
  emphasis: underline
  typography: mixed-serif-sans
layout: balanced  # primary layout
image_count: 7
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
Split composition — chaotic left side vs serene right side,
warm golden tones, editorial typography

**Swipe Hook**: Here's what most people get wrong →

---
```

**Differentiation requirements**:
- Each strategy MUST have different outline structure AND different recommended style
- Adapt slide count: A typically 6-8, B typically 5-7, C typically 4-6
- Include `style_reason` explaining why this style fits the strategy
- Consider user's style preference from Step 2

**Instagram-specific requirements**:
- **Slide 2 Rule**: Slide 2 must be independently compelling (IG may re-serve carousels starting from slide 2)
- **Minimal text**: Target 5-15 words per slide for body content, single key phrase focus
- **Grid preview**: Cover design must work when center-cropped to 3:4 for IG profile grid

Reference: `references/workflows/outline-template.md`

### Step 4: Confirmation 2 - Outline & Style & Elements Selection ⚠️

**Purpose**: User chooses outline strategy, confirms visual style, and customizes elements. **Do NOT skip.**

**Display each strategy**:
- Strategy name + slide count + recommended style
- Slide-by-slide summary (S1 → S2 → S3...)

**Use AskUserQuestion** with three questions:

**Question 1: Outline Strategy**
- Strategy A (Recommended if "authentic/story")
- Strategy B (Recommended if "expert/informational")
- Strategy C (Recommended if "aspirational/visual")
- Combine: specify slides from each

**Question 2: Visual Style**
- Use strategy's recommended style (show which style)
- Or select from: clean-minimal / bold-graphic / soft-muted / editorial / retro-nostalgia / neon-gradient / earthy-organic / dark-cinematic / playful-pop / line-art
- Or type custom style description

**Question 3: Visual Elements** (show after style selection)
Display the selected style's default elements from preset, then ask:
- Use style defaults (Recommended) - show preview: background, decorations, emphasis
- Adjust background - options: solid-white / neutral-warm / gradient-linear / gradient-radial / dark-solid / textured
- Adjust decorations - options: minimal-lines / geometric-shapes / editorial-frames / gradient-overlays / organic-shapes / glass-morphism
- Type custom element preferences

**After response**:
- Single strategy → copy to `outline.md` with confirmed style
- Combination → merge specified slides with confirmed style
- Custom request → regenerate based on feedback
- Style defaults → use preset's Element Combination as-is
- Background adjustment → update elements.background with user choice
- Decorations adjustment → update elements.decorations with user choice
- Custom elements → parse user's preferences into elements fields
- Update `outline.md` frontmatter with final style and elements

### Step 5: Generate Images

With confirmed outline + style + layout:

**Visual Consistency — Reference Image Chain**:
To ensure character/style consistency across all slides in a carousel:
1. **Generate slide 1 (cover) FIRST** — without `--ref`
2. **Use slide 1 as `--ref` for ALL remaining slides** (2, 3, ..., N)
   - This anchors the character design, color rendering, and illustration style
   - Command pattern: `--ref <path-to-slide-01.png>` added to every subsequent generation

This is critical for styles that use recurring characters, mascots, or illustration elements. Slide 1 becomes the visual anchor for the entire carousel.

**For each image (cover + content + ending)**:
1. Save prompt to `prompts/NN-{type}-[slug].md` (in user's preferred language)
   - **Backup rule**: If prompt file exists, rename to `prompts/NN-{type}-[slug]-backup-YYYYMMDD-HHMMSS.md`
2. Generate image:
   - **Slide 1**: Generate without `--ref` (this establishes the visual anchor)
   - **Slides 2+**: Generate with `--ref <slide-01-path>` for consistency
   - **Backup rule**: If image file exists, rename to `NN-{type}-[slug]-backup-YYYYMMDD-HHMMSS.png`
3. Report progress after each generation

**Watermark Application** (if enabled in preferences):
Add to each image generation prompt:
```
Include a subtle watermark "[content]" positioned at [position].
The watermark should be legible but not distracting from the main content.
```
Reference: `references/config/watermark-guide.md`

**Image Generation Skill Selection**:
- Check available image generation skills
- If multiple skills available, ask user preference

**Session Management**:
If image generation skill supports `--sessionId`:
1. Generate unique session ID: `ig-{topic-slug}-{timestamp}`
2. Use same session ID for all images
3. Combined with reference image chain, ensures maximum visual consistency

### Step 6: Completion Report

```
Instagram Carousel Infographic Series Complete!

Topic: [topic]
Strategy: [A/B/C/Combined]
Style: [style name]
Layout: [layout name or "varies"]
Location: [directory path]
Slides: N total

✓ analysis.md
✓ outline-strategy-a.md
✓ outline-strategy-b.md
✓ outline-strategy-c.md
✓ outline.md (selected: [strategy])

Files:
- 01-cover-[slug].png ✓ Cover (sparse)
- 02-content-[slug].png ✓ Content (balanced)
- 03-content-[slug].png ✓ Content (balanced)
- ...
- NN-ending-[slug].png ✓ Ending (sparse)

IG Tips:
- Grid preview: Cover image works in center 3:4 crop ✓
- Slide 2 is independently compelling ✓
- CTA on final slide ✓
```

## Image Modification

| Action | Steps |
|--------|-------|
| **Edit** | **Update prompt file FIRST** → Regenerate with same session ID |
| **Add** | Specify position → Create prompt → Generate → Renumber subsequent files (NN+1) → Update outline |
| **Delete** | Remove files → Renumber subsequent (NN-1) → Update outline |

**IMPORTANT**: When updating images, ALWAYS update the prompt file (`prompts/NN-{type}-[slug].md`) FIRST before regenerating. This ensures changes are documented and reproducible.

## Content Breakdown Principles

1. **Cover (Slide 1)**: Hook + visual impact → `sparse` layout
2. **Slide 2 (Second Chance)**: Must independently hook — IG may re-serve carousel starting here
3. **Content (Middle)**: One key idea per slide → `balanced`/`dense`/`list`/`comparison`/`flow`
4. **Ending (Last 1-2)**: CTA / summary / engagement prompt → `sparse` or `balanced`

**Instagram-Specific Design Rules**:
- **Minimal text**: 5-15 words per slide (body content), one key phrase focus
- **Grid preview**: Key content visible in center 3:4 crop of 4:5 image (profile grid)
- **Swipe signals**: Visual cues that content continues (arrows, partial reveals, numbering)
- **Save triggers**: Reference material, checklists, templates → users bookmark for later
- **Share triggers**: Relatable content, "tag someone who needs this" → DM sharing

**Style × Layout Matrix** (✓✓ = highly recommended, ✓ = works well):

| | sparse | balanced | dense | list | comparison | flow | mindmap | quadrant |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| clean-minimal | ✓✓ | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓ | ✓ | ✓ |
| bold-graphic | ✓✓ | ✓ | ✓ | ✓✓ | ✓✓ | ✓ | ✓ | ✓✓ |
| soft-muted | ✓✓ | ✓✓ | ✓ | ✓ | ✓ | ✓✓ | ✓ | ✓ |
| editorial | ✓✓ | ✓✓ | ✓ | ✓ | ✓✓ | ✓ | ✓ | ✓ |
| retro-nostalgia | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓ | ✓ | ✓ |
| neon-gradient | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓ | ✓✓ | ✓ | ✓ |
| earthy-organic | ✓✓ | ✓✓ | ✓ | ✓ | ✓ | ✓✓ | ✓✓ | ✓ |
| dark-cinematic | ✓✓ | ✓✓ | ✓ | ✓ | ✓✓ | ✓ | ✓ | ✓ |
| playful-pop | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓ | ✓ | ✓ |
| line-art | ✓✓ | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓ |

## References

Detailed templates in `references/` directory:

**Elements** (Visual building blocks):
- `elements/canvas.md` - Aspect ratios, safe zones, grid layouts
- `elements/image-effects.md` - Cutout, stroke, filters
- `elements/typography.md` - Typography trends, text hierarchy
- `elements/decorations.md` - Backgrounds, overlays, frames, decorative elements

**Presets** (Style presets):
- `presets/<name>.md` - Element combination definitions (clean-minimal, editorial, bold-graphic...)

**Workflows** (Process guides):
- `workflows/analysis-framework.md` - Content analysis framework
- `workflows/outline-template.md` - Outline template with layout guide
- `workflows/prompt-assembly.md` - Prompt assembly guide

**Config** (Settings):
- `config/preferences-schema.md` - EXTEND.md schema
- `config/first-time-setup.md` - First-time setup flow
- `config/watermark-guide.md` - Watermark configuration

## Notes

- Auto-retry once on failure | Create stylistic alternatives for sensitive/copyrighted figures
- Use confirmed language preference | Maintain style consistency across all slides
- **Two confirmation points required** (Steps 2 & 4) - do not skip
- IG carousel sweet spot: 8-10 slides for maximum engagement
- Slide 2 must work as an independent hook (IG re-serve feature)

## Extension Support

Custom configurations via EXTEND.md. See **Step 0** for paths and supported options.
