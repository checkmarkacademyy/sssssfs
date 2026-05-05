---
name: Obsidian Flux
colors:
  surface: '#121317'
  surface-dim: '#121317'
  surface-bright: '#38393e'
  surface-container-lowest: '#0d0e12'
  surface-container-low: '#1a1b20'
  surface-container: '#1f1f24'
  surface-container-high: '#292a2e'
  surface-container-highest: '#343439'
  on-surface: '#e3e2e8'
  on-surface-variant: '#c7c4d7'
  inverse-surface: '#e3e2e8'
  inverse-on-surface: '#2f3035'
  outline: '#908fa0'
  outline-variant: '#464554'
  surface-tint: '#c0c1ff'
  primary: '#c0c1ff'
  on-primary: '#1000a9'
  primary-container: '#8083ff'
  on-primary-container: '#0d0096'
  inverse-primary: '#494bd6'
  secondary: '#4cd7f6'
  on-secondary: '#003640'
  secondary-container: '#03b5d3'
  on-secondary-container: '#00424e'
  tertiary: '#bdc7d9'
  on-tertiary: '#27313f'
  tertiary-container: '#8791a3'
  on-tertiary-container: '#202a38'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e1e0ff'
  primary-fixed-dim: '#c0c1ff'
  on-primary-fixed: '#07006c'
  on-primary-fixed-variant: '#2f2ebe'
  secondary-fixed: '#acedff'
  secondary-fixed-dim: '#4cd7f6'
  on-secondary-fixed: '#001f26'
  on-secondary-fixed-variant: '#004e5c'
  tertiary-fixed: '#d9e3f6'
  tertiary-fixed-dim: '#bdc7d9'
  on-tertiary-fixed: '#121c2a'
  on-tertiary-fixed-variant: '#3d4756'
  background: '#121317'
  on-background: '#e3e2e8'
  surface-variant: '#343439'
typography:
  h1:
    fontFamily: Inter
    fontSize: 40px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  h2:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.3'
    letterSpacing: -0.01em
  h3:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.4'
    letterSpacing: 0em
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
    letterSpacing: 0em
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
    letterSpacing: 0em
  label-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '500'
    lineHeight: '1'
    letterSpacing: 0.02em
  label-xs:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1'
    letterSpacing: 0.05em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 4px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  container-margin: 40px
  gutter: 20px
---

## Brand & Style

This design system is built for a premium, high-performance productivity environment. The brand personality is sophisticated, nocturnal, and technologically advanced, targeting power users who value focus and high-end aesthetics. 

The visual direction utilizes **Glassmorphism** as its primary driver, emphasizing depth through translucency rather than heavy solid colors. The interface should feel like a series of suspended light-emitting panels over a deep, infinite void. The emotional response is one of "calm precision"—reducing cognitive load through blurred backgrounds while highlighting critical actions with high-energy neon accents.

## Colors

The palette is anchored by **Deep Obsidian (#0B0C10)**, providing a pure, high-contrast foundation that makes accent colors vibrate. 

- **Electric Indigo (#6366F1)** serves as the primary action color, used for main CTAs, active states, and primary branding.
- **Neon Cyan (#06B6D4)** is the secondary accent, utilized for progress indicators, success states, and interactive secondary elements.
- **Surface & Borders**: Rather than solid grays, surfaces use a translucent white at 5% opacity to create the glass effect, paired with a 10% opacity white border to define edges against the dark background.

## Typography

This design system exclusively employs **Inter** for its systematic clarity and neutral character. 

Hierarchy is established through weight and tracking rather than just size. Headlines (H1-H2) use tighter letter spacing and heavy weights to command attention. Labels and metadata utilize medium and semi-bold weights with slight letter spacing to maintain legibility against blurred glass backgrounds. Body text is kept at a comfortable 16px to ensure readability in a dark environment.

## Layout & Spacing

The layout follows a **Fixed-Fluid hybrid** model. Main navigation and sidebars occupy fixed widths, while the primary task view spans the remaining space. 

A strict 4px spacing system ensures visual rhythm. Large container margins (40px) provide the "premium" breathable feel, preventing the UI from feeling cluttered. Task lists should have generous vertical padding (16px) between items to emphasize each task as an individual "object" floating in the space.

## Elevation & Depth

Depth is achieved through **multi-layered glassmorphism** and background physics:

1.  **The Void (Base):** Pure #0B0C10.
2.  **Atmospheric Layer:** Abstract, low-opacity blurred circles of Indigo and Cyan floating behind the UI to create a sense of three-dimensional space.
3.  **Glass Panels:** Containers use `backdrop-filter: blur(20px)` and `background: rgba(255, 255, 255, 0.05)`.
4.  **The Stroke:** Every elevated element must have a 1px border (`rgba(255, 255, 255, 0.1)`). On hover, this border should transition to `rgba(255, 255, 255, 0.2)`.
5.  **Shadows:** Use large, highly diffused shadows (`0 20px 40px rgba(0, 0, 0, 0.4)`) to separate active panels from the background.

## Shapes

The design system utilizes **Rounded (Level 2)** geometry to balance modern tech with organic approachability. 

- Standard components (Buttons, Inputs): **12px (0.75rem)** radius.
- Large containers and Cards: **16px (1rem)** radius.
- Progress bars and pill-style tags: Fully rounded/circular ends.

Consistency in corner radii is critical to maintaining the "engineered" feel of the interface.

## Components

### Buttons
- **Primary:** Solid gradient from Electric Indigo to a slightly darker shade, 12px radius, white text, subtle indigo outer glow on hover.
- **Secondary (Glass):** Backdrop-filter blur, 1px white (0.1) border, transparent background.

### Task Items (List)
Tasks should appear as glass cards. The checkbox is a 20px circle with a 1px border. When checked, it fills with a Cyan-to-Indigo gradient and triggers a subtle strikethrough on the text with 50% opacity.

### Input Fields
Inputs are minimalist: a bottom border only in the default state, expanding to a full glass container with a Cyan border-glow when focused.

### Chips & Tags
Small, pill-shaped elements with a 10% opacity fill of the accent color (Cyan or Indigo) and matching high-contrast text.

### Progress Visuals
Use a Neon Cyan gradient for progress bars. Add a subtle `box-shadow` of the same color to create a "neon light" effect that reflects onto the glass panels below.