---
name: Aetheric Developer Edition
colors:
  surface: '#111318'
  surface-dim: '#111318'
  surface-bright: '#37393e'
  surface-container-lowest: '#0c0e12'
  surface-container-low: '#1a1c20'
  surface-container: '#1e2024'
  surface-container-high: '#282a2e'
  surface-container-highest: '#333539'
  on-surface: '#e2e2e8'
  on-surface-variant: '#bac9cd'
  inverse-surface: '#e2e2e8'
  inverse-on-surface: '#2f3035'
  outline: '#859397'
  outline-variant: '#3b494c'
  surface-tint: '#00daf8'
  primary: '#baf2ff'
  on-primary: '#00363f'
  primary-container: '#00e0ff'
  on-primary-container: '#005f6d'
  inverse-primary: '#006877'
  secondary: '#d8b9ff'
  on-secondary: '#450086'
  secondary-container: '#6e06d0'
  on-secondary-container: '#d5b5ff'
  tertiary: '#e3e7ff'
  on-tertiary: '#002b75'
  tertiary-container: '#bbcbff'
  on-tertiary-container: '#004dc5'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#a5eeff'
  primary-fixed-dim: '#00daf8'
  on-primary-fixed: '#001f25'
  on-primary-fixed-variant: '#004e5a'
  secondary-fixed: '#eddcff'
  secondary-fixed-dim: '#d8b9ff'
  on-secondary-fixed: '#290055'
  on-secondary-fixed-variant: '#6200bc'
  tertiary-fixed: '#dae1ff'
  tertiary-fixed-dim: '#b3c5ff'
  on-tertiary-fixed: '#001849'
  on-tertiary-fixed-variant: '#003fa4'
  background: '#111318'
  on-background: '#e2e2e8'
  surface-variant: '#333539'
typography:
  display-xl:
    fontFamily: Space Grotesk
    fontSize: 72px
    fontWeight: '700'
    lineHeight: 80px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Space Grotesk
    fontSize: 48px
    fontWeight: '600'
    lineHeight: 56px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Space Grotesk
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  code-sm:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.1em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 8px
  container-max: 1280px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 64px
  stack-sm: 12px
  stack-md: 24px
  stack-lg: 48px
---

## Brand & Style

This design system is built for the high-end developer persona, blending technical precision with a futuristic, "cyber-noir" aesthetic. The interface evokes the feeling of a premium command center or a high-fidelity IDE. It targets recruiters and tech leads who value both engineering rigor and modern design sensibilities.

The visual language is rooted in **Glassmorphism** and **Vaporwave-inspired Minimalism**. It utilizes deep, ink-like backgrounds to provide maximum contrast for neon accents, creating a sense of infinite depth. Motion is a core brand pillar; transitions should feel fluid and weightless, utilizing "glow-tracking" effects where light follows user interaction.

## Colors

The palette is centered on a **Deep Space Navy** base that nears absolute black to ensure the glass effects pop. 

- **Primary (Cyan Glow):** Used for critical actions, active states, and terminal cursors.
- **Secondary (Purple Neon):** Used for decorative elements, code syntax highlighting, and secondary brand marks.
- **Tertiary (Electric Blue):** Used for links and interactive hover states.
- **Surface Colors:** Utilize semi-transparent variants of the neutral palette to create the glass effect. Layers are built using `rgba(13, 17, 23, 0.6)`.

Gradients should be used sparingly but impactfully on card borders and progress bars to simulate light refracting through glass.

## Typography

This design system utilizes a trio of typefaces to balance futurism with readability. 

1. **Space Grotesk** is used for large displays and headlines, providing a technical, geometric edge that feels engineered.
2. **Inter** serves as the primary workhorse for body copy, ensuring long-form content (like project descriptions or blogs) remains highly legible for recruiters.
3. **JetBrains Mono** is reserved for labels, metadata, and code snippets, reinforcing the developer-centric nature of the portfolio.

Apply a subtle text-shadow of `0 0 8px rgba(0, 224, 255, 0.2)` to primary headlines to give them a faint "screen glow" effect.

## Layout & Spacing

The layout follows a **Fixed Grid** model for desktop to maintain the "dashboard" feel, switching to a fluid single-column for mobile. 

- **Desktop (1440px+):** 12-column grid with a 1280px max-width container.
- **Tablet (768px - 1024px):** 8-column grid with 24px margins.
- **Mobile (<767px):** 4-column grid with 16px margins.

Spacing is governed by an 8px base unit. Use generous "Stack" spacing (`stack-lg`) between major sections to allow the background glows and glass elements room to breathe.

## Elevation & Depth

Depth is achieved through **Backdrop Blurs** and **Tonal Stacking** rather than traditional drop shadows.

1. **Level 0 (Background):** Solid `#020408` with occasional radial gradients of Primary/Secondary colors at 5% opacity to simulate ambient light.
2. **Level 1 (Glass Cards):** Background `rgba(13, 17, 23, 0.6)` with a `blur(12px)`. These cards feature a 1px border of `rgba(255, 255, 255, 0.1)`.
3. **Level 2 (Active/Hover):** The border transitions to the `border_gradient` and the backdrop blur increases to `20px`.
4. **Floating Elements:** Use a "Neon Underglow" — a box-shadow using the primary color at 20% opacity with a high blur radius (30px+) and 0px spread.

## Shapes

The shape language is **Refined & Geometric**. A `0.5rem` (8px) base radius is used for all cards and input fields to maintain a professional, structured look. 

Buttons and "Skill Chips" use a slightly more aggressive `rounded-xl` or pill-shape to distinguish them as interactive, tactile elements. Decorative elements, such as background shards or code brackets, should remain sharp (0px) to contrast with the soft glass containers.

## Components

### Buttons
- **Primary:** Gradient background (Cyan to Blue), white text, 0.5s transition on hover to increase "Outer Glow."
- **Secondary:** Transparent background, 1px Cyan border, text-color Cyan.
- **Ghost:** No border, JetBrains Mono font, subtle color shift on hover.

### Glass Cards
The signature component. Must include `backdrop-filter: blur(12px)` and a `linear-gradient` border. For project cards, the background image should sit behind the glass layer with a 0.4 opacity multiply blend.

### Input Fields
Dark backgrounds (`#0A0C10`) with a bottom-only border that illuminates to a full gradient on focus. Use JetBrains Mono for placeholder text.

### Skill Chips
Small, pill-shaped badges with a low-opacity primary background (`rgba(0, 224, 255, 0.1)`) and a solid 1px border.

### Scroll Progress Mask
A thin, 2px fixed bar at the top of the viewport using the `primary_color_hex` with a `box-shadow` glow that tracks reading progress.