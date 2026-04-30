---
name: Krisvin Joseph Portfolio
description: Personal engineering portfolio — confident, precise, earned dark.
colors:
  void-ground: "#0a0a0a"
  carbon: "#111111"
  carbon-lifted: "#161616"
  shadow-seam: "#1e1e1e"
  iron-seam: "#2c2c2c"
  graphite-trace: "#444444"
  technical-gray: "#888888"
  chalk: "#f0f0f0"
  signal-white: "#ffffff"
  muted-signal: "#dddddd"
typography:
  display:
    fontFamily: "'Space Grotesk', system-ui, sans-serif"
    fontSize: "clamp(3.25rem, 9vw, 6.75rem)"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "'Space Grotesk', system-ui, sans-serif"
    fontSize: "clamp(1.875rem, 5vw, 3.125rem)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "-0.03em"
  title:
    fontFamily: "'Space Grotesk', system-ui, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 700
    lineHeight: 1.3
    letterSpacing: "-0.02em"
  body:
    fontFamily: "'DM Sans', system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.9
  label:
    fontFamily: "'DM Sans', system-ui, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 500
    lineHeight: 1.75
  micro:
    fontFamily: "'DM Sans', system-ui, sans-serif"
    fontSize: "0.6875rem"
    fontWeight: 500
    letterSpacing: "0.01em"
rounded:
  pill: "50px"
  card: "18px"
  skill: "8px"
  tag: "6px"
spacing:
  section: "96px"
  card: "28px"
  gap: "14px"
  gutter: "24px"
components:
  button-primary:
    backgroundColor: "{colors.signal-white}"
    textColor: "{colors.void-ground}"
    rounded: "{rounded.pill}"
    padding: "11px 26px"
  button-primary-hover:
    backgroundColor: "{colors.muted-signal}"
    textColor: "{colors.void-ground}"
    rounded: "{rounded.pill}"
    padding: "11px 26px"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.chalk}"
    rounded: "{rounded.pill}"
    padding: "11px 26px"
  project-card:
    backgroundColor: "{colors.carbon}"
    textColor: "{colors.chalk}"
    rounded: "{rounded.card}"
    padding: "{spacing.card}"
  project-card-hover:
    backgroundColor: "{colors.carbon-lifted}"
    textColor: "{colors.chalk}"
    rounded: "{rounded.card}"
    padding: "{spacing.card}"
  tag:
    backgroundColor: "transparent"
    textColor: "{colors.technical-gray}"
    rounded: "{rounded.tag}"
    padding: "4px 10px"
  skill-pill:
    backgroundColor: "{colors.carbon}"
    textColor: "{colors.technical-gray}"
    rounded: "{rounded.skill}"
    padding: "6px 12px"
---

# Design System: Krisvin Joseph Portfolio

## 1. Overview

**Creative North Star: "The Operator's Log"**

This is a portfolio that reads like the work log of someone who ships real things. Dark ground. Tight type. Numbers over adjectives. The craft lives in restraint — in what is not there. A recruiter scanning this page should feel the same quiet confidence they feel opening a well-built CLI or a Stripe dashboard: nothing is wasted, everything is correct.

The palette is pure grayscale with no color accent. This is not a limitation — it is the statement. In a sea of teal-gradient, glassmorphic, neon-saturated engineering portfolios, a system that earns attention through hierarchy and precision reads as more sophisticated, not less. Signal White (#fff) at full opacity on Void Ground (#0a0a0a) IS the loudest signal in this system. Its rarity is its power.

Density is low. Breathing room is generous. Each section has one job. The typography compresses aggressively at display scale (line-height 1.0, -0.04em tracking) and opens at body scale (line-height 1.9). This contrast — tight display, airy body — creates the rhythm of a confident speaker: precise headline, then room to read.

**Key Characteristics:**
- Monochromatic grayscale, no color accent — Signal White is the emphasis color
- Tonal layering for depth, never shadows
- Space Grotesk for hierarchy and identity; DM Sans for readability at work
- Metrics and outcomes in the primary copy position; descriptors subordinate
- Floating pill navigation, anchored to top-center — the only chrome element above content
- 760px maximum container — tight enough to force clear hierarchy

## 2. Colors

A system of six gray steps from near-void to near-white. There is no accent hue. Emphasis comes from contrast alone.

### Primary
- **Signal White** (#ffffff): Hero `<h1>` text, primary button background. The single brightest element in the system — used only where maximum contrast is required. Do not use for body text, which uses Chalk instead.
- **Chalk** (#f0f0f0): All primary text on dark surfaces. Section headings, card titles, strong-weight bullets. Slightly softened from pure white to avoid the harshness of a pure #fff text color against deep backgrounds.

### Neutral
- **Void Ground** (#0a0a0a): Page background. The base of the entire stack. Also used as button-primary text (white button, dark label — the one inversion).
- **Carbon** (#111111): Card and surface background at rest. Lifted one step above Void Ground — enough to read as a distinct layer, not enough to feel light.
- **Carbon Lifted** (#161616): Card hover state. The background brightens; the border strengthens; the card translates -3px. Three signals at once.
- **Shadow Seam** (#1e1e1e): Border at rest. Subtle enough to read as structure, not decoration.
- **Iron Seam** (#2c2c2c): Border on hover and strong-boundary contexts (tag chips, expanded cards). Doubles as the visual anchor when Carbon Lifted is active.
- **Graphite Trace** (#444444): Decorative and subordinate elements: bullet dashes (em dash markers in lists), arrow icons at rest, footer text. Not for any text the user should actually read.
- **Technical Gray** (#888888): Secondary and supporting text. About paragraphs, card descriptions, bullet copy, skill labels, contact links at rest. The working color of the system.

### Named Rules

**The No-Accent Rule.** There is no color in this system. Signal White on Void Ground is the maximum contrast pair — it functions as the accent. Adding any hue (blue, teal, purple, orange) breaks the intentional restraint and reduces the system to a cliché.

**The Inversion Rule.** The only surface-text inversion is the primary button: Signal White background with Void Ground text. No other element should invert the relationship. Dark text on a light surface anywhere else reads as a design accident.

## 3. Typography

**Display Font:** Space Grotesk (wght 700, from Google Fonts — preloaded with `rel="preload" as="style"`)
**Body Font:** DM Sans (wght 400/500/600, optical size 9–40, from Google Fonts)

**Character:** Space Grotesk is geometric with faint quirks (the curved "G", the wide "M") that give it a technical-but-human feel without the sterility of pure geometric sans. DM Sans has a humanist warmth at body sizes that makes long bullets scannable. Together: Space Grotesk announces, DM Sans explains.

### Hierarchy

- **Display** (700, clamp(3.25rem → 6.75rem), line-height 1.0, tracking -0.04em): Hero `<h1>` only. Compressed to near-solid at large sizes. The most aggressive tracking in the system.
- **Headline** (700, clamp(1.875rem → 3.125rem), line-height 1.1, tracking -0.03em): Section headings (`<h2>`). Anchors each scroll section with a clear landmark. Max-width container keeps it left-aligned for scan.
- **Title** (700, 1.125rem / 18px, line-height 1.3, tracking -0.02em): Card titles (project name, company name). Space Grotesk here signals a named entity — a thing that shipped.
- **Body** (400, 1rem / 16px, line-height 1.9): About paragraphs. Wide line-height invites reading — the only section where prose runs at this scale. Max 620px width enforces the 65–75ch rule.
- **Label** (500, 0.875rem / 14px, line-height 1.75): Card descriptions, bullet copy, exp-bullets. The workhorse size — most content lives here.
- **Micro** (500, 0.6875rem / 11px, tracking 0.01em): Tag chips, skill pills, nav tabs, footer, date labels. Slight positive tracking compensates for small size.

### Named Rules

**The Compression Rule.** Display and Headline weights carry negative tracking (-0.04em to -0.03em). Body and Label weights carry no tracking. Never apply negative tracking below 18px — it collapses letterforms and reduces legibility.

**The Scale Leap Rule.** No two adjacent hierarchy levels are within 1.25x of each other. Display to Headline is a 2x+ step. Title to Label is a 1.28x step. If a new text style is needed, it must land outside the existing steps or inherit an existing one.

## 4. Elevation

This system uses **tonal layering exclusively**. There are no box-shadows anywhere in the codebase — depth is a property of surface lightness.

Three-step stack:
- **Void Ground** (#0a0a0a) — base; page background; not a surface
- **Carbon** (#111111) — resting surface; cards, experience blocks
- **Carbon Lifted** (#161616) — elevated surface; hover state for interactive cards

A card hover triggers three simultaneous signals: background brightens (#111 to #161), border strengthens (#1e1e1e to #2c2c2c), and the card translates -3px on Y. The motion is the elevation — no shadow needed.

### Named Rules

**The Carbon Stack Rule.** Surfaces get depth from tonal shift, not shadow blur. If you need a new layer of depth, add a surface step between existing gray values. Do not introduce `box-shadow`.

**The Flat-at-Rest Rule.** No element has a shadow in its default state. Shadows, if ever introduced, must be earned by state change (hover, focus, active). Static decorative shadows are prohibited.

## 5. Components

### Buttons

Two variants: primary and outline. Both use pill shape (50px radius) and the same padding (11px 26px). They always appear as a pair — primary action left, secondary right.

- **Shape:** Fully rounded pill (50px radius). Never a rectangle or a square button.
- **Primary:** Signal White background (#fff), Void Ground text (#0a0a0a), DM Sans 500 13px. Hover: Muted Signal (#ddd) background + translateY(-1px). The only white surface in the system.
- **Outline:** Transparent background, Chalk/0.75 text (rgba(255,255,255,0.75)), border rgba(255,255,255,0.22). Hover: full Chalk text, border rgba(255,255,255,0.5) + translateY(-1px).
- **Focus:** 2px solid Chalk outline, 3px offset, 4px border-radius on the outline — consistent with all focusable elements.
- **Transition:** `all 0.2s ease` on both variants. Keep motion simple; no spring or bounce.

### Navigation

Floating pill nav, fixed to top-center. The only element that floats above content.

- **Container:** rgba(16,16,16,0.92) background, 1px border rgba(255,255,255,0.08), 50px radius, `backdrop-filter: blur(24px)`. Always top-center, never full-width.
- **Tab (inactive):** DM Sans 500 13.5px, rgba(255,255,255,0.6). Hover: rgba(255,255,255,0.85).
- **Tab (active):** #fff, rgba(255,255,255,0.1) background behind the tab, 40px radius. The active tab is a chip-within-the-pill — contained, not underlined.
- **Mobile (≤680px):** Tabs compress to 11.5px / 6px 10px padding. At 480px: 11px / 5px 8px.
- **Behavior:** IntersectionObserver at 0.35 threshold drives active state — no click-only nav. The page scroll position always reflects in the nav.

### Project Card

Full-bleed link cards. Each card IS the link — not a button inside the card.

- **Shape:** 18px radius (card rounded). Full border at rest: 1px Shadow Seam (#1e1e1e).
- **Background:** Carbon (#111) at rest. Carbon Lifted (#161) on hover.
- **Border on hover:** Iron Seam (#2c2c2c).
- **Transform on hover:** `translateY(-3px)` — lifts visually without a shadow.
- **Internal padding:** 28px (20px at mobile).
- **Structure:** Header row (project title + arrow icon) → description paragraph → bullet list → tag strip. The arrow icon translates `(2px, -2px)` on hover to signal directionality.
- **Arrow:** Graphite Trace (#444) at rest; Chalk (#f0f0f0) on hover. The color shift + translate is the only motion on the icon.

### Experience Card

Non-interactive surface. Same shape as project card but no hover state and no link.

- **Shape and background:** Identical to Project Card at rest. No hover treatment.
- **Structure:** Header row (company name + date, baseline-aligned) → role subtitle → bullet list.
- **Date treatment:** Graphite Trace (#444), 12px, right-aligned in the header row.

### Tags (Technology Chips)

Appear in the tag strip at the bottom of each project card.

- **Shape:** 6px radius (tag rounded). Transparent background, 1px Iron Seam border.
- **Text:** DM Sans 500 11px, Technical Gray (#888), 0.01em tracking.
- **On card hover:** Text shifts to Chalk (#f0f0f0); border to #3a3a3a. The whole strip responds to card hover — no individual chip hover state.
- **Do not add individual chip hover states.** The chip strip is informational, not interactive.

### Skill Pills

Appear in the Skills section. Non-interactive.

- **Shape:** 8px radius (skill rounded). Carbon background (#111), 1px Shadow Seam border (#1e1e1e).
- **Text:** DM Sans 500 13px, Technical Gray (#888).
- **No hover state.** These are a list, not controls.

### Signature Component: Floating Particle Canvas

Full-viewport canvas behind the hero. 72 particles at random position and velocity. Connects particles within 155px distance with a stroke opacity proportional to `(1 - d/LINK) * 0.1` — very faint at the threshold, slightly brighter near-zero distance.

- **Particle fill:** rgba(255,255,255,0.2)
- **Line stroke:** maximum rgba(255,255,255,0.1), fades to transparent at 155px
- **Canvas is `position: absolute; inset: 0`** behind `.hero-content` which is `z-index: 1`
- **Never**: add color to the particles. They are white-on-black. Adding any hue (blue glow, purple tint) breaks the monochromatic discipline.

## 6. Do's and Don'ts

### Do:

- **Do** use Signal White (#fff) only at maximum emphasis — hero h1 text and primary button background. Its rarity is its power.
- **Do** lead with numbers in card copy: "100+ sales", "18% accuracy improvement", "200+ active users". Outcomes earn the reader's time; adjectives do not.
- **Do** use Space Grotesk with negative tracking at display and headline scale (-0.04em, -0.03em). The compression is intentional and produces the "precision tool" feeling.
- **Do** use translateY(-3px) + border + background shift as the three-signal hover pattern for interactive cards. Never use box-shadow as a hover state.
- **Do** keep the container max-width at 760px. The tight container forces hierarchy — everything must earn its width.
- **Do** follow `prefers-reduced-motion` by disabling the particle animation and card translate transitions when the user has reduced motion enabled.
- **Do** use DM Sans at 500 weight for labels, tags, nav tabs, and micro copy. The medium weight reads at small sizes where 400 would thin out.

### Don't:

- **Don't** add any color accent — no teal, blue, purple, orange, green, or any hue. This is the No-Accent Rule. If it has chroma, it does not belong here.
- **Don't** use glassmorphism decoratively. The floating nav uses backdrop-filter purposefully (it floats above scrolling content). No other element in the system uses blur or glass effects.
- **Don't** use neon-on-black — no bright, saturated color against Void Ground. This is the aesthetic of a gaming portfolio, not an engineering portfolio seeking serious hires.
- **Don't** use the Framer/Webflow template aesthetic: no gradient blobs, no large decorative abstract shapes, no hover-to-reveal image cards with color overlays.
- **Don't** use `box-shadow` anywhere. The Carbon Stack Rule prohibits it. If depth is needed, use a surface color step.
- **Don't** use `border-left` or `border-right` greater than 1px as a colored stripe on cards, list items, or callouts. Rewrite with a full border or background tint.
- **Don't** use gradient text (`background-clip: text`). Body copy and headings are solid single colors. Emphasis comes from weight and scale, not gradients.
- **Don't** animate layout properties (width, height, top, left, padding). Only animate `transform`, `opacity`, `color`, `background-color`, `border-color`.
- **Don't** add color to the particle canvas. Particles and connection lines are white at low opacity. Any hue in the hero creates a "gaming RGB" aesthetic that conflicts with the system's register.
- **Don't** stack nested cards. Project cards and experience cards are the outer container. Nothing inside them should have a card-like background/border/radius treatment.
- **Don't** use the hero-metric template (big number + label + supporting stats). Krisvin's metrics belong inline in bullet copy, not in a statistics dashboard layout.
