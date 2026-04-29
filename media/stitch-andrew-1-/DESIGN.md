---
name: Manuscript Noir
colors:
  surface: '#131313'
  surface-dim: '#131313'
  surface-bright: '#393939'
  surface-container-lowest: '#0e0e0e'
  surface-container-low: '#1b1b1b'
  surface-container: '#1f1f1f'
  surface-container-high: '#2a2a2a'
  surface-container-highest: '#353535'
  on-surface: '#e2e2e2'
  on-surface-variant: '#c4c7c8'
  inverse-surface: '#e2e2e2'
  inverse-on-surface: '#303030'
  outline: '#8e9192'
  outline-variant: '#444748'
  surface-tint: '#c6c6c7'
  primary: '#ffffff'
  on-primary: '#2f3131'
  primary-container: '#e2e2e2'
  on-primary-container: '#636565'
  inverse-primary: '#5d5f5f'
  secondary: '#c6c6c7'
  on-secondary: '#2f3131'
  secondary-container: '#454747'
  on-secondary-container: '#b4b5b5'
  tertiary: '#ffffff'
  on-tertiary: '#2f3131'
  tertiary-container: '#e2e2e2'
  on-tertiary-container: '#636565'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e2e2e2'
  primary-fixed-dim: '#c6c6c7'
  on-primary-fixed: '#1a1c1c'
  on-primary-fixed-variant: '#454747'
  secondary-fixed: '#e2e2e2'
  secondary-fixed-dim: '#c6c6c7'
  on-secondary-fixed: '#1a1c1c'
  on-secondary-fixed-variant: '#454747'
  tertiary-fixed: '#e2e2e2'
  tertiary-fixed-dim: '#c6c6c7'
  on-tertiary-fixed: '#1a1c1c'
  on-tertiary-fixed-variant: '#454747'
  background: '#131313'
  on-background: '#e2e2e2'
  surface-variant: '#353535'
typography:
  headline-lg:
    fontFamily: JetBrains Mono
    fontSize: 48px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  headline-md:
    fontFamily: JetBrains Mono
    fontSize: 32px
    fontWeight: '400'
    lineHeight: '1.3'
    letterSpacing: -0.01em
  body-lg:
    fontFamily: JetBrains Mono
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
    letterSpacing: '0'
  body-md:
    fontFamily: JetBrains Mono
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
    letterSpacing: '0'
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '700'
    lineHeight: '1.4'
    letterSpacing: 0.1em
spacing:
  unit: 8px
  container-max: 720px
  gutter: 32px
  margin-page: 64px
  paragraph-spacing: 32px
---

## Brand & Style

This design system is built upon the concept of "Literary Minimalism"—a digital experience that prioritizes the written word as the sole vessel of meaning. It evokes the quiet, focused intensity of a dark room illuminated only by the glow of a terminal or a mechanical typewriter. 

The aesthetic draws heavily from Brutalist and Minimalist movements, stripping away all decorative ornamentation to expose the raw structure of information. The target audience is the intellectual, the writer, and the developer who find beauty in precision and clarity. By removing conventional UI metaphors, the design system creates an immersive, archival atmosphere where negative space acts as the primary navigational guide.

## Colors

The palette is an absolute binary of light and shadow. There are no shades of gray or accent colors to distract the eye. 

The background is a pure, ink-black (#000000), providing a void-like depth that eliminates screen glare and maximizes visual focus. Typography is rendered in a crisp, stark white (#FFFFFF) to ensure the highest possible contrast ratio. Interaction is signaled not through color shifts, but through rhythmic changes in text weight, underlines, or bracketed symbols.

## Typography

Typography is the sole structural element of this design system. We utilize JetBrains Mono for its technical precision and "typewriter" soul. The monospaced nature of the font ensures a predictable, grid-like rhythm across all content.

Headlines should be used sparingly, relying on scale and negative space rather than bold colors to denote hierarchy. Body text is set with generous line heights to facilitate long-form reading without fatigue. For metadata or small labels, use all-caps with increased letter spacing to create a distinct visual texture compared to prose.

## Layout & Spacing

The layout philosophy follows a "Fixed Manuscript" model. Content is centered within a constrained width to mimic the proportions of a printed page or a terminal window. This prevents line lengths from becoming uncomfortably long on wide displays.

The rhythm is vertical. We use a strict 8px baseline grid to ensure alignment. Information density is kept intentionally low; large blocks of negative space are used to separate concepts and sections. Margins are oversized to frame the content as a singular object of focus amidst the black void.

## Elevation & Depth

This design system is strictly two-dimensional. There are no shadows, blurs, or gradients. Hierarchy is conveyed through:
1. **Vertical Position:** The most critical information is placed at the top of the stack.
2. **Scale:** Larger type denotes higher-level headings.
3. **Indentation:** Borrowing from code and literature, nesting information or indenting paragraphs creates a logical "depth" without physical layers.

The screen is treated as a flat surface of light and ink.

## Shapes

The design system utilizes a sharp (0px) geometry. Since there are no containers, borders, or buttons, "shape" is defined by the character blocks of the typography and the outer bounds of text selection markers. Every visual element is rectangular and uncompromising, mirroring the strict grid of the monospaced font.

## Components

In the absence of traditional UI elements, components are constructed purely through text:

*   **Links/Interactions:** Interactive text is identified via a persistent underline or by being wrapped in brackets (e.g., `[ Explore ]`). On hover, the link should invert colors—white background with black text—mimicking a text selection highlight.
*   **Lists:** Unordered lists use the asterisk `*` or hyphen `-`. Ordered lists use simple numerals followed by a period `1.`
*   **Dividers:** When a section break is required, use a single line of repeating characters such as `_ _ _` or `...` rather than a solid graphical border.
*   **Input Fields:** Represented as an underscore `_` or a blinking block cursor `█` following a text label. There are no input boxes.
*   **Navigation:** A simple vertical or horizontal list of plain text words, separated by generous whitespace.