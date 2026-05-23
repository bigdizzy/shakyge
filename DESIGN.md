---
name: Shaky Gaming & Entertainment
description: Dark game-studio atmosphere for a creator support brand — technical craft, quiet confidence.
colors:
  void-navy: "#050913"
  depth-navy: "#060b1c"
  frost-text: "#eaf3ff"
  electric-royal: "#1d4cff"
  signal-sky: "#2aa9ff"
  cyan-edge: "#33d6ff"
  glass-surface: "rgba(10, 18, 42, 0.34)"
  hairline-mist: "rgba(180, 210, 255, 0.14)"
typography:
  display:
    fontFamily: "ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial"
    fontSize: "clamp(46px, 5.2vw, 86px)"
    fontWeight: 900
    lineHeight: 0.96
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial"
    fontSize: "20px"
    fontWeight: 900
    lineHeight: 1.2
    letterSpacing: "-0.01em"
  body:
    fontFamily: "ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "normal"
  label:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, Liberation Mono, Courier New, monospace"
    fontSize: "12px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0.02em"
rounded:
  card: "22px"
  button: "14px"
  chip: "999px"
  logo: "14px"
spacing:
  nav-y: "14px"
  nav-x: "18px"
  card-pad: "22px"
  hero-pad: "26px"
  grid-gap: "14px"
components:
  button-primary:
    backgroundColor: "rgba(51, 214, 255, 0.10)"
    textColor: "{colors.frost-text}"
    rounded: "{rounded.button}"
    padding: "12px 15px"
  button-primary-hover:
    backgroundColor: "rgba(51, 214, 255, 0.14)"
    textColor: "{colors.frost-text}"
    rounded: "{rounded.button}"
    padding: "12px 15px"
  button-ghost:
    backgroundColor: "rgba(5, 9, 19, 0.22)"
    textColor: "{colors.frost-text}"
    rounded: "{rounded.button}"
    padding: "12px 15px"
  glass-card:
    backgroundColor: "{colors.glass-surface}"
    textColor: "{colors.frost-text}"
    rounded: "{rounded.card}"
    padding: "{spacing.card-pad}"
---

# Design System: Shaky Gaming & Entertainment

## 1. Overview

**Creative North Star: "The Night Operator"**

Shaky's site should feel like a credible game-studio or broadcast operator at night: deep navy atmosphere, Shaky blue as instrument lighting, and one signature motion treatment (wireframe geometry) instead of a pile of retro HUD effects. The impression is technical craft and quiet confidence, not an agency deck or a SaaS template wearing gaming cosplay.

The current implementation (`index.html`) encodes the dark mood and brand blues. Several layers (scanlines, grain, corner brackets, fake status mono, stacked glass, side-stripe quotes) read as cyber HUD clichés and generic AI output. Future redesign work should **keep** night mode, gradient depth, glass surfaces used sparingly, and the canvas geometry. It should **remove or replace** the cliché stack per PRODUCT.md anti-references.

**Key Characteristics:**

- Deep void navy base with cool frost text (`#050913` → `#eaf3ff`)
- Three-step blue accent ramp: royal → sky → cyan edge (`#1d4cff` → `#2aa9ff` → `#33d6ff`)
- Large display headlines (clamp up to ~86px), heavy weight, tight tracking
- Glass panels with 22px radius, hairline borders, deep drop shadow
- Signature background: animated 3D wireframe shapes on canvas (cyan edges, low fill)
- Scroll progress bar and section reveal fades

## 2. Colors

A committed cool-blue palette on near-black navy. Accents glow; neutrals are blue-tinted frost, never pure white or pure black.

### Primary

- **Void Navy** (`#050913` / oklch(0.14 0.03 265)): Page background top, theme-color, header scrim base.
- **Depth Navy** (`#060b1c` / oklch(0.15 0.035 265)): Background gradient bottom, depth behind content.
- **Electric Royal** (`#1d4cff` / oklch(0.48 0.22 264)): Progress bar start, shape fill accents, radial glow secondary.
- **Signal Sky** (`#2aa9ff` / oklch(0.68 0.14 240)): Selection highlight, shape fills, button glow.
- **Cyan Edge** (`#33d6ff` / oklch(0.78 0.12 220)): Primary CTA borders, kicker dot, wireframe edges, hero glow.

### Neutral

- **Frost Text** (`#eaf3ff` / oklch(0.95 0.02 250)): Primary text and headings.
- **Muted Frost** (`rgba(234, 243, 255, 0.72)`): Body paragraphs, nav links default.
- **Whisper Frost** (`rgba(234, 243, 255, 0.60–0.62)`): Hints, footer, tiny copy.
- **Hairline Mist** (`rgba(180, 210, 255, 0.10–0.18)`): Borders, accent lines, grid lines.
- **Glass Surface** (`rgba(10, 18, 42, 0.34)`): Card backgrounds with backdrop blur.

### Named Rules

**The Logo Blue Rule.** Accent hues must stay within the existing Shaky ramp (royal → sky → cyan). Do not introduce purple gradients, gold fintech accents, or neon magenta.

**The Tinted Void Rule.** Backgrounds stay blue-black voids. Never use `#000000` or `#ffffff` as surface colors.

## 3. Typography

**Display / Body / Label Font:** System UI stack (`ui-sans-serif, system-ui, -apple-system, …`) for all marketing type today.

**Label / Status Font:** System monospace (`ui-monospace, SFMono-Regular, Menlo, …`) for `.monoTag` only.

**Character:** Heavy, tight display type on dark fields reads as gaming-adjacent product marketing. Future evolution should replace the system stack with a deliberate display + body pairing (game-studio or broadcast reference) without sliding into editorial serif essay layout.

### Hierarchy

- **Display** (900, `clamp(46px, 5.2vw, 86px)`, line-height 0.96): Hero `h1` only. Subtle cyan text-shadow glow.
- **Headline** (900, 20px, -0.01em tracking): Section `h2`, brand name in header.
- **Body** (400, 17px lead / default paragraph, ~1.5 line-height): `.lead` max ~74ch; section copy uses muted frost.
- **Label** (mono, 12–13px, uppercase kickers with 0.08em tracking): `.kicker` rows; use sparingly in redesign.

### Named Rules

**The One Glow Rule.** Display headlines may carry a single soft glow. Do not add gradient text (`background-clip: text`) or multiple competing text effects.

**The Mono Sparingly Rule.** Monospace is for short metadata, not voice. Remove fake terminal status lines in redesign ("Status online. Queue open.").

## 4. Elevation

Hybrid depth: **tonal layering** (skewed band backgrounds, glass translucency) plus **deep ambient shadows** on hero and cards. Decorative layers (vignette, grid, canvas, scanlines, grain) sit behind content at negative z-index.

### Shadow Vocabulary

- **Card lift** (`0 18px 60px rgba(0, 0, 0, 0.45)`): Default `.glass` panels.
- **Hero mass** (`0 26px 90px rgba(0, 0, 0, 0.55)`): `.heroWrap` container.
- **Cyan halo** (multi-layer `box-shadow` on `.heroGlow`): Outer brand glow, not a drop shadow on type.

### Named Rules

**The Flat Stack Ban (redesign).** Do not combine vignette + grid + scanlines + grain + HUD corners + glass stacks. Pick **one** signature atmospheric layer (recommended: canvas geometry) plus base gradient.

**The Glass Sparingly Rule.** Glass is a surface treatment for content panels, not the default answer for every block. Nested glass-on-glass is forbidden.

## 5. Components

Atmosphere-forward marketing primitives. Shapes are generously rounded (22px cards, 14px buttons).

### Buttons

- **Shape:** Soft rectangle (14px radius), inline-flex, 12×15px padding.
- **Primary:** Cyan-tinted border `rgba(51, 214, 255, 0.34)`, fill `rgba(51, 214, 255, 0.10)`, subtle blue outer glow on shadow.
- **Ghost:** Dark fill `rgba(5, 9, 19, 0.22)`, hairline border.
- **Hover:** `translateY(-1px)` only; no bounce easing.

### Chips / Pills

- **Pill row:** Full-radius capsules for hero facts (Since 2020, 300+ creators).
- **Chips:** Smaller tags (12px type) for topic labels in About.
- **Nav pill:** Contact link with cyan border wash in header.

### Cards / Containers

- **Glass card:** `.glass` — blur 16px, saturate 1.25, inset top highlight pseudo-element, diagonal radial wash pseudo-element.
- **Hero frame:** `.heroWrap` + optional `.hud` corner brackets (deprecated for redesign).
- **List items:** `.item` nested rows inside glass, 16px radius, darker inset fill.
- **Quote:** Left border accent 2px cyan (replace in redesign: no side-stripe borders >1px as colored accent).

### Navigation

- **Header:** Sticky below 3px progress bar, frosted `rgba(5, 9, 19, 0.62)` + blur 14px.
- **Links:** 14px muted; hover lifts background mist. Mobile hides link row below 920px (no menu replacement yet).

### Signature: Wireframe Canvas

- Full-viewport `#geom` canvas, cyan wire edges with shimmer animation along edges, icosa/cube/tetra meshes.
- **Reduced motion:** Static single frame when `prefers-reduced-motion: reduce`.
- This is the **one signature motion** to preserve; other motion layers should defer to it.

## 6. Do's and Don'ts

### Do:

- **Do** keep dark void navy backgrounds and the Shaky blue → cyan accent ramp anchored to `images/shakyblue.png`.
- **Do** treat wireframe canvas geometry as the primary atmospheric motion; respect `prefers-reduced-motion`.
- **Do** use glass panels with hairline borders and 22px radius for major content blocks, not for every nested element.
- **Do** write display type large and tight (hero clamp 46–86px, weight 900) for game-studio energy.
- **Do** keep copy direct and operator-toned (loadouts, systems, runway) per PRODUCT.md.

### Don't:

- **Don't** ship generic SaaS landing patterns: hero metric blocks, three identical icon cards, purple gradients.
- **Don't** sound like a creator agency pitch deck: promise language, roster flex, hype.
- **Don't** use cyber HUD clichés: corner brackets, scanlines, fake status pings, stacked glass cards.
- **Don't** pivot to AI editorial layout (cream paper, magazine serif essay) as a substitute for Shaky's dark identity.
- **Don't** use neon crypto / Web3 aesthetics (magenta, gold, laser grids).
- **Don't** use `border-left` greater than 1px as a colored stripe on quotes or callouts (current `.quote` violates this; fix on redesign).
- **Don't** use gradient text or the hero-metric template (big number, small label, supporting stats grid).
- **Don't** stack vignette + grid + scanlines + grain + HUD + glass; one signature layer wins.
