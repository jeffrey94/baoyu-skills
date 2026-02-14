# Canvas & Layout

Core canvas specifications and layout grids for Instagram carousel infographics.

## Aspect Ratios

| Name | Ratio | Pixels | Export Size | Note |
|------|-------|--------|-------------|------|
| portrait-4-5 | 4:5 | 1080×1350 | 2160×2700 | Highest engagement on IG (recommended) |
| square | 1:1 | 1080×1080 | 2160×2160 | Works for grid consistency |
| portrait-9-16 | 9:16 | 1080×1920 | 2160×3840 | Story-style, full screen |

**Default**: portrait-4-5 for maximum feed visibility and engagement.

**Export note**: Generate at 2x resolution (2160×2700) for crisp display on high-DPI screens.

## Safe Zones

Avoid placing critical content in these areas:

| Zone | Position | Reason |
|------|----------|--------|
| bottom-bar | Bottom 5% | IG UI overlay (like/comment/share buttons) |
| grid-crop | Outer edges of 4:5 | Grid preview crops to center 3:4 area |
| top-corners | Top-left/right corners | Story ring, username overlay |

```
┌─────────────────────────────┐
│ [username]                  │  ← top-left: may overlap
│  ┌───────────────────────┐  │
│  │                       │  │
│  │    ✓ SAFE CONTENT     │  │  ← center 3:4 = grid preview safe
│  │       AREA            │  │
│  │                       │  │
│  └───────────────────────┘  │
│  [♡ 💬 ↗ ···]              │  ← bottom 5%: IG UI overlay
└─────────────────────────────┘
```

**Grid Preview Rule**: When this 4:5 image appears on your IG profile grid, it's center-cropped to roughly 3:4. Ensure the cover slide's key content (title, hero visual) is visible within the center 3:4 area.

## Grid Layouts

### Density-Based Layouts

| Layout | Info Density | Whitespace | Points/Slide | Best For |
|--------|--------------|------------|--------------|----------|
| sparse | Low | 60-70% | 1-2 | Covers, quotes, impactful statements |
| balanced | Medium | 50-60% | 2-3 | Standard content, key ideas |
| dense | High | 30-40% | 3-5 | Knowledge cards, cheat sheets |

**Note**: IG layouts use MORE whitespace than text-heavy platforms — slides should feel open and breathable. Dense on IG is equivalent to balanced on other platforms.

### Structure-Based Layouts

| Layout | Structure | Items | Best For |
|--------|-----------|-------|----------|
| list | Vertical enumeration | 3-5 | Rankings, checklists, step guides |
| comparison | Left vs Right | 2 sections | Before/after, pros/cons, do/don't |
| flow | Connected nodes | 3-5 steps | Processes, timelines, workflows |
| mindmap | Center radial | 4-6 branches | Concept maps, topic overview |
| quadrant | 4-section grid | 4 sections | Priority matrix, classification |

## Layout by Position

| Position | Recommended Layout | Why |
|----------|-------------------|-----|
| Cover (Slide 1) | sparse | Maximum visual impact, clear title, grid-safe |
| Slide 2 | sparse/balanced | Must independently hook (IG re-serve) |
| Core (Middle) | balanced/list/comparison/flow | Based on content — one idea per slide |
| Payoff | balanced/list | Clear takeaways |
| Ending | sparse | Clean CTA, memorable close |

## Grid Cells

For multi-element compositions:

| Name | Cells | Use Case |
|------|-------|----------|
| single | 1 | Hero image, maximum impact |
| dual | 2 | Before/after, comparison |
| triptych | 3 | Steps, process flow |
| quad | 4 | Product showcase |

## Visual Balance

### Sparse Layout
- Single focal point centered
- Generous breathing room on all sides
- Bold headline with minimal supporting text
- Maximum visual impact

### Balanced Layout
- Top-weighted title or centered headline
- 2-3 supporting points evenly spaced
- Clear visual hierarchy with ample spacing
- Comfortable reading experience

### Dense Layout
- Organized sections with clear boundaries
- 3-5 key points with concise text
- Still maintains IG-appropriate whitespace (30-40%)
- Compact but scannable

### List Layout
- Left-aligned or centered items
- Clear number/icon hierarchy
- Consistent item format (icon + short text)
- 3-5 items maximum per slide

### Comparison Layout
- Symmetrical left/right or top/bottom
- Clear visual contrast between sections
- Divider or color differentiation
- Minimal text per side

### Flow Layout
- Directional flow (top→bottom or left→right)
- Connected nodes with arrows or lines
- Clear progression indicators
- 3-5 steps maximum per slide

### Mindmap Layout
- Central topic node
- Radial branches outward
- Clean connections (lines, not cluttered)
- 4-6 branches maximum

### Quadrant Layout
- 4-section grid (2×2)
- Clear axis labels or section headers
- Each quadrant with single key point
- Optional circular variant for cycles
