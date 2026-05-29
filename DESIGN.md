---
name: Linguist Pro Tablet
colors:
  surface: '#f7f9ff'
  surface-dim: '#d7dadf'
  surface-bright: '#f7f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f1f4f9'
  surface-container: '#ebeef3'
  surface-container-high: '#e5e8ee'
  surface-container-highest: '#e0e3e8'
  on-surface: '#181c20'
  on-surface-variant: '#424753'
  inverse-surface: '#2d3135'
  inverse-on-surface: '#eef1f6'
  outline: '#727785'
  outline-variant: '#c2c6d5'
  surface-tint: '#005ac4'
  primary: '#00459a'
  on-primary: '#ffffff'
  primary-container: '#005cc8'
  on-primary-container: '#cfdcff'
  inverse-primary: '#aec6ff'
  secondary: '#006d38'
  on-secondary: '#ffffff'
  secondary-container: '#93f4ad'
  on-secondary-container: '#00723b'
  tertiary: '#47494a'
  on-tertiary: '#ffffff'
  tertiary-container: '#5f6162'
  on-tertiary-container: '#dbdcdd'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#d8e2ff'
  primary-fixed-dim: '#aec6ff'
  on-primary-fixed: '#001a42'
  on-primary-fixed-variant: '#004396'
  secondary-fixed: '#96f7b0'
  secondary-fixed-dim: '#7ada96'
  on-secondary-fixed: '#00210d'
  on-secondary-fixed-variant: '#005229'
  tertiary-fixed: '#e1e3e4'
  tertiary-fixed-dim: '#c5c7c8'
  on-tertiary-fixed: '#191c1d'
  on-tertiary-fixed-variant: '#454748'
  background: '#f7f9ff'
  on-background: '#181c20'
  surface-variant: '#e0e3e8'
typography:
  display-lg:
    fontFamily: Public Sans
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Public Sans
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
  body-xl:
    fontFamily: Public Sans
    fontSize: 24px
    fontWeight: '400'
    lineHeight: 32px
  body-lg:
    fontFamily: Public Sans
    fontSize: 20px
    fontWeight: '400'
    lineHeight: 28px
  label-caps:
    fontFamily: Public Sans
    fontSize: 14px
    fontWeight: '700'
    lineHeight: 20px
    letterSpacing: 0.05em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  stack-margin: 32px
  gutter: 24px
  safe-area: 40px
  bubble-padding: 20px 24px
  touch-target-min: 64px
---

## Brand & Style

The design system is centered on **Corporate Modernism** with a heavy focus on **Accessibility and Utility**. The primary goal is to facilitate seamless, face-to-face communication through a shared hardware interface (iPad 10th Gen). 

The brand personality is **reliable, professional, and empathetic**. It avoids unnecessary decorative elements in favor of high-contrast functional zones. The UI must feel robust enough for government or medical use while remaining approachable for everyday travel. The visual style uses "Tonal Layering"—using distinct background washes to define user territory—and oversized touch targets to ensure the interface is usable at arm's length.

## Colors

The palette is designed for **territorial distinction**. 

- **Primary (Blue):** Assigned to Speaker A. A deep, professional blue that ensures high contrast against its soft background.
- **Secondary (Green):** Assigned to Speaker B. A nature-inspired green that signals "active" and "friendly," providing a clear visual pivot from Speaker A.
- **Surface Colors:** Each speaker has a dedicated tint (`speaker_one_surface` and `speaker_two_surface`) to wash their half of the split-screen layout.
- **High Contrast:** All text must maintain a minimum 7:1 contrast ratio against background tints to satisfy AAA accessibility standards for tablet-based legibility.

## Typography

This design system utilizes **Public Sans** for its institutional clarity and exceptional legibility at varied distances. 

To accommodate the iPad being placed on a table between two users, the scale is intentionally oversized. 
- **Display-LG** is used for the translated text output, ensuring it is readable at a 2-3 foot distance.
- **Body-XL** is the standard for conversational input.
- **Labels** use high-weight caps to clearly identify language toggles and interface modes.

The typography for Speaker B (the person facing the "top" of the iPad) should be rotated 180 degrees via the layout engine, not a specific font style.

## Layout & Spacing

The layout utilizes a **Fixed Split-Screen Grid** specifically optimized for the 10.9-inch display. 

1.  **Vertical Split:** The screen is divided into two equal halves (horizontally when in landscape). 
2.  **Symmetry:** The interface for Speaker B is a 180-degree mirrored reflection of Speaker A.
3.  **The Interaction Zone:** A central "neutral" gutter of 24px separates the two halves.
4.  **Touch Targets:** All interactive elements (microphones, language switchers) adhere to a strict 64px minimum touch target to prevent accidental triggers during proximity-based conversation.

## Elevation & Depth

This design system avoids heavy shadows to maintain a clean, professional aesthetic. 

- **Surface Tiers:** Hierarchy is established through color value rather than physical depth. The active microphone button uses a subtle ambient shadow (8% opacity, 12px blur) to indicate it is "pressed" or "live."
- **Ghost Outlines:** Input fields and secondary buttons use 1px solid borders in a slightly darker shade of the background tint.
- **Glass Effects:** When a settings overlay or language picker is activated, a backdrop blur of 20px is applied to the entire screen to focus the user on the modal.

## Shapes

The shape language is **Rounded (Level 2)**. 

- **Speech Bubbles:** Feature a 16px (1rem) corner radius. To improve accessibility, bubbles do not use "tails" which can clutter the UI; instead, they rely on proximity to the user's avatar and color coding.
- **Control Buttons:** Circular shapes are reserved exclusively for the Microphone (Primary Action). All other buttons (Language, History) use the standard `rounded-lg` (16px) tokens.

## Components

### Speech Bubbles
Bubbles occupy the majority of the territorial half. Speaker A's bubbles are `primary_color_hex` with white text. Speaker B's bubbles are `secondary_color_hex` with white text. They should have a maximum width of 80% of the half-screen to allow for clear transcript margins.

### Microphone Toggle
The central interaction point. 
- **Idle:** A circular button with a 2px outline.
- **Active:** Pulsing animation with a filled background. The icon should be a simplified, bold microphone glyph.

### Language Indicators
Placed at the top corner of each speaker's zone. Includes the ISO code (e.g., "EN") and the full language name in a `label-caps` format. These serve as the trigger for the language selection modal.

### Waveform Visualizer
A horizontal bar component that appears next to the microphone when active. It uses `primary_color_hex` or `secondary_color_hex` to provide real-time visual feedback that the system is capturing audio.

### List Items
For conversation history, use high-density list items with 16px internal padding, using `body-lg` for the text.