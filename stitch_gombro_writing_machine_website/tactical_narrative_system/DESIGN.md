---
name: Tactical Narrative System
colors:
  surface: '#131313'
  surface-dim: '#131313'
  surface-bright: '#3a3939'
  surface-container-lowest: '#0e0e0e'
  surface-container-low: '#1c1b1b'
  surface-container: '#201f1f'
  surface-container-high: '#2a2a2a'
  surface-container-highest: '#353534'
  on-surface: '#e5e2e1'
  on-surface-variant: '#e0bfbc'
  inverse-surface: '#e5e2e1'
  inverse-on-surface: '#313030'
  outline: '#a78a87'
  outline-variant: '#58413f'
  surface-tint: '#ffb3ac'
  primary: '#ffb3ac'
  on-primary: '#680007'
  primary-container: '#8b1a1a'
  on-primary-container: '#ff9a91'
  inverse-primary: '#ac322e'
  secondary: '#cac6be'
  on-secondary: '#31302b'
  secondary-container: '#484741'
  on-secondary-container: '#b8b5ad'
  tertiary: '#96ccf8'
  on-tertiary: '#00344f'
  tertiary-container: '#004c71'
  on-tertiary-container: '#86bce7'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#ffdad6'
  primary-fixed-dim: '#ffb3ac'
  on-primary-fixed: '#410003'
  on-primary-fixed-variant: '#8a1a1a'
  secondary-fixed: '#e6e2da'
  secondary-fixed-dim: '#cac6be'
  on-secondary-fixed: '#1c1c17'
  on-secondary-fixed-variant: '#484741'
  tertiary-fixed: '#cae6ff'
  tertiary-fixed-dim: '#96ccf8'
  on-tertiary-fixed: '#001e30'
  on-tertiary-fixed-variant: '#004b70'
  background: '#131313'
  on-background: '#e5e2e1'
  surface-variant: '#353534'
typography:
  display-lg:
    fontFamily: Bebas Neue
    fontSize: 72px
    fontWeight: '700'
    lineHeight: 64px
    letterSpacing: -0.02em
  headline-h1:
    fontFamily: Bebas Neue
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 44px
    letterSpacing: 0.02em
  headline-h2:
    fontFamily: Bebas Neue
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 32px
    letterSpacing: 0.05em
  body-lg:
    fontFamily: IBM Plex Mono
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: IBM Plex Mono
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 22px
  pull-quote:
    fontFamily: Playfair Display
    fontSize: 24px
    fontWeight: '400'
    lineHeight: 36px
  label-caps:
    fontFamily: IBM Plex Mono
    fontSize: 11px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.1em
  headline-h1-mobile:
    fontFamily: Bebas Neue
    fontSize: 36px
    fontWeight: '700'
    lineHeight: 32px
spacing:
  unit: 4px
  gutter: 16px
  margin-sm: 24px
  margin-lg: 40px
  column-gap: 1px
---

## Brand & Style

This design system is a high-precision interface modeled after military-grade instrumentation and specialized tactical hardware. The brand personality is disciplined, cold, and hyper-functional, catering to writers who view their craft as a rigorous engineering process. 

The aesthetic is **Industrial Minimalism**. It rejects all organic softness in favor of mechanical rigidity. The UI should evoke the feeling of a glass-cockpit display or a machined magnesium alloy chassis. 

**Core Principles:**
- **Zero Softness:** No rounded corners, no gradients, and no soft shadows.
- **Instrument Precision:** Every element must look like it was measured and calibrated.
- **High Information Density:** Clear hierarchy through scale and weight rather than color or depth.
- **Tactile feedback:** Use of 1px rules and hairline strokes to define structure, mimicking etched metal.

## Colors

The palette is strictly limited to four tones to maintain a high-contrast, low-light tactical environment. 

- **Canvas (#0a0a0a):** The deep black primary background.
- **Inertia (#0f0f0f):** Used for secondary containers to create subtle architectural shifts without depth.
- **Lumen (#e8e4dc):** A cold, bone-white for all critical data and body text.
- **Warning (#8B1A1A):** A deep, dried-blood red used exclusively for critical actions, active states, or "combat" modes (editing/deleting).
- **Structure (#1a1a1a):** The specific shade for 1px rules and grid lines.

## Typography

Typography is the primary tool for differentiation. 

- **Headings:** Bebas Neue must always be uppercase. Tracking should be tight for display sizes and slightly tracked out for sub-headers to improve legibility on dark backgrounds.
- **Body:** IBM Plex Mono provides the "typewriter" or "monitored data" feel. It is used for all functional text and primary manuscript input.
- **Pull Quotes:** Playfair Display Italic is the only serif and the only "humanist" element in the system. Use it sparingly for stylistic emphasis within the manuscript.
- **Metadata:** Use IBM Plex Mono at small sizes (11px) with wide letter spacing for labels, timestamps, and word counts.

## Layout & Spacing

The layout is governed by a **Hard Grid** system. All components must align to a 4px baseline and 1px borders should be placed exactly on the pixel grid to ensure maximum sharpness.

- **Grid:** Use a 12-column fixed grid for desktop, reducing to a 4-column fluid grid for mobile.
- **Separation:** Do not use whitespace alone to separate major sections; use 1px rules (#1a1a1a).
- **Margins:** High-density layouts are preferred. Keep margins tight (24px) to emphasize the utilitarian nature of the "instrument."
- **Reflow:** On mobile, the manuscript view takes 100% width, while sidebars (navigation/outline) are hidden behind a toggle that slides in as a hard-edged panel.

## Elevation & Depth

This system uses **Tonal Layering** with zero shadows. Depth is an illusion created by 1px rules and contrasting background shades.

- **Base Level:** #0a0a0a.
- **Elevated Level:** Panels or modals use #0f0f0f and are outlined with a 1px #1a1a1a border.
- **Active State:** Instead of a shadow, an active "elevation" is signaled by a 1px solid border of #8B1A1A (Deep Red) or a color inversion (Lumen background with Black text).
- **Overlay:** Modals should not have a backdrop blur. Use a solid 80% #000000 overlay to kill background context and focus on the technical task.

## Shapes

The shape language is strictly **Rectilinear**. 

- All buttons, inputs, cards, and containers must have **0px corner radius**. 
- Any diagonal lines must be 45-degree chamfers (used sparingly for "technical detail" in icons or UI corners).
- Icons should be stroke-based, 1px or 2px thickness, with sharp joins and no caps.

## Components

**Buttons:** 
- Rectangular with 1px border. Default: #e8e4dc border/text. Hover: #8B1A1A border/text. 
- Primary Action: Solid #8B1A1A background with #0a0a0a text.

**Input Fields:**
- Bottom-border only (1px #1a1a1a) for a minimal look, or a full rectangle for tactical focus. 
- Placeholder text in IBM Plex Mono at 40% opacity.

**Chips/Tags:**
- Small rectangles with 1px border. No fill. 
- Text in `label-caps`.

**Cards:**
- No shadows. 1px #1a1a1a border. 
- Header section separated by a 1px horizontal rule.

**The "Manuscript" Area:**
- A stark, distraction-free container. 
- Word count and status indicators pinned to the bottom-right rule in `label-caps`.

**The "Tactical" Sidebar:**
- Vertical navigation icons with text labels. 
- Active tab indicated by a vertical 2px line of #8B1A1A on the far left edge.