# Design System Inspired by Mijn Thuisbatterij

> Category: Energy & Sustainability
> Dutch home-battery advisory tool. Emerald and dark-green palette, Tilt Warp display type, Outfit body text, "Dongel" plug mascot.

## 1. Visual Theme & Atmosphere

Mijn Thuisbatterij ("My Home Battery") is a Dutch consumer advisory tool that helps homeowners size a home battery correctly, using a "batterijsimulator" (battery simulator) built on the visitor's own energy consumption and generation. This design system is sourced from the brand's official "Huisstijl" (house-style) guide by Studio Nieuwe Weide, so its colors, typefaces, and mascot are confirmed brand assets, not inferred.

The identity is built on a house-shaped logomark: an emerald-green gabled roofline topped by a yellow lightning-bolt chevron, with the stacked wordmark "mijn / thuis / batterij" set inside. The house-style guide states the rationale directly — "the green base forms a sustainable building which, combined with the yellow lightning bolt, stands for charging energy and results in a rising, positive balance." That sentence is the entire brand thesis: sustainability (green) plus energy (yellow) equals a positive financial outcome, and every visual choice should reinforce it.

A bright emerald hero band opens the page like a poster, carrying the white logo card, a floating yellow sun/lightning decoration, and a large two-line headline in the brand's display face, phrased as a direct, confident question ("Een batterij die jou éxact past?" — "A battery that fits you exactly?"). Below the hero, the page drops to a clean white canvas where a short feature list makes the pitch in plain language. Each point is anchored by **Dongel** — the brand's mascot — a smiling, light-blue, rounded plug-shaped character with a dark-green plug top, used as the system's default "feature bullet" icon in place of a generic checkmark.

Typography pairs two Google Fonts with distinct jobs: **Tilt Warp** (a bold, rounded, wavy-stroke display face) for headers and subheadings, and **Outfit Light** (a clean, geometric, low-weight sans) for body copy. The pairing gives headlines a playful, energetic character while keeping body text calm and legible — display type carries the brand's personality, body type gets out of the way.

Supporting the logo and mascot is a confirmed flat, two-tone illustration/icon set: bar chart, lightbulb/target, lightning bolt, tree, plug-with-leaf, house, globe, sun, solar-panel grid, and floor lamp. Every icon uses the same construction — one primary shape in Dark Green or Emerald Green, one accent shape in Yellow, Orange, or Light Blue — never more than two colors per icon, and no outlines or gradients.

**Key Characteristics:**
- House-shaped logomark: emerald gable + yellow lightning-bolt roofline, stacked wordmark
- Official 5-color palette: Dark Green, Emerald Green, Light Blue, Orange, Yellow — used consistently, not loosely mixed
- "Dongel" mascot — a smiling light-blue plug character — as the system's default feature-bullet icon
- Tilt Warp (bold, rounded, wavy display face) for all headers/subheadings; Outfit Light for body text — a confirmed two-family pairing
- Flat, two-tone illustration system: one primary hue + one accent hue per icon, no outlines, no gradients
- Fully-pill CTA buttons in a clear primary (solid dark green)/secondary (white, dark-green outline) pairing
- Plain-language, reassuring, calculator-driven Dutch copywriting ("zonder gok" — "without guessing")
- A reversed/"diapositief" logo lockup exists for use on green backgrounds (light card, colored wordmark) — don't render the primary dark-on-white lockup directly on a green surface

## 2. Color Palette & Roles

All five colors below are taken directly from the official house-style guide (not estimated).

### Primary
- **Dark Green** (`#0E3D23`): The brand's core dark ink — wordmark text ("thuis"/"batterij"), primary CTA fill, body copy. CSS variable `--accent` / `--fg`.
- **Emerald Green** (`#00A36F`): The "sustainable building" green — hero-band surface wash, the "mijn" portion of the wordmark, logo gable shape. CSS variable `--hero-bg` (C-extension) and `--success`.

### Secondary
- **Yellow** (`#FFCD00`): The "energy / charging" color — the logomark's lightning-bolt roofline, decorative sun/lightning motifs. CSS variable `--warn`.
- **Orange** (`#E94E1B`): An illustration-system accent — appears within the flat icon set (e.g. the bar-chart accent bar), not used as a general UI color. CSS variable `--illustration-orange` (C-extension).
- **Light Blue** (`#9CD6E8`): The Dongel mascot's body color and the feature-list icon-chip background. CSS variable `--surface-warm`.

### Neutral / Surface
- **White** (`#ffffff`): Page canvas outside the hero band, logo card background, secondary CTA fill. CSS variables `--bg` / `--surface`.
- **Muted Green-Gray** (`#4c6a5b`): Derived secondary/caption text tint — the house-style guide defines the 5-color brand palette above but not a full UI neutral ramp, so this is a derived, not confirmed, value. CSS variable `--muted`.
- **Pale Emerald Tint** (`#d7ece3`): Derived hairline border color, same caveat as above. CSS variable `--border`.

### Semantic
- **Success** (`#00A36F`): Bound to Emerald Green per the house-style guide's own "rising, positive balance" rationale — a direct fit for a savings/simulator result.
- **Warn** (`#FFCD00`): Bound to Yellow per the guide's "energy charging" lightning-bolt motif.
- **Danger** (`#dc2626`): No brand-defined red; inherits the shared schema default.

## 3. Typography Rules

### Font Family
- **Display / Headers & Subheadings ("Koptekst" / "Subkoppen")**: `"Tilt Warp", "Baloo 2", -apple-system, system-ui, sans-serif` — Tilt Warp is a Google Font, used at Regular weight only (it has no separate bold/light cut in the house-style guide). Its wavy, rounded stroke terminals give headlines a distinctly playful, energetic character.
- **Body ("Bodytekst")**: `"Outfit", -apple-system, system-ui, sans-serif` — Outfit is a Google Font, specified at Light (300) weight. Its clean geometric letterforms keep long-form copy calm and legible in contrast to the display face.
- **Mono**: schema default (`ui-monospace, "SF Mono", "JetBrains Mono", Menlo, Monaco, Consolas, monospace`) — no code/technical UI specified by the brand.

### Hierarchy

| Role | Font | Size | Weight | Line Height | Notes |
|------|------|------|--------|-------------|-------|
| Hero Headline | Tilt Warp | 56px / `--text-4xl` | Regular | 1.15 | Two-line hero statement, e.g. "Een batterij die jou éxact past?" |
| Section Heading | Tilt Warp | 32px / `--text-2xl` | Regular | 1.15 | Content-section titles ("Koptekst") |
| Subheading | Tilt Warp | 24px / `--text-xl` | Regular | 1.2 | "Subkoppen" — content dividers |
| Feature Row Text | Outfit | 20px / `--text-lg` | 600 (Semibold) | 1.5 | Bold dark-green feature-list copy — Outfit's Light cut is reserved for long-form body, so feature callouts step up in weight |
| Body | Outfit | 16px / `--text-base` | 300 (Light) | 1.5 | General body copy — the brand's specified "Bodytekst" weight |
| Button Label | Tilt Warp | 16px / `--text-base` | Regular | 1.15 | CTA pill labels, frequently two lines |
| Caption / Tagline | Outfit | 14px / `--text-sm` | 300 (italic for tagline) | 1.5 | "besparing inzicht" tagline treatment |

### Principles
- Reserve Tilt Warp for headers, subheadings, and CTA labels only — never set long-form body copy in the display face.
- Outfit Light (300) is the default body weight; step up to Semibold only for short emphasis (feature-list lead-ins, labels), never for paragraphs.
- Reserve italics for the tagline treatment only ("besparing inzicht"); don't apply italics elsewhere.
- Zero letter-spacing throughout — both typefaces read best without added tracking.
- Favor short, confident, question-form or benefit-form headline copy over long descriptive sentences.

## 4. Component Stylings

### Buttons

**Primary CTA Pill** ("Meer info over een thuisbatterij")
- Background: Dark Green `#0E3D23`
- Text: White `#ffffff`, Tilt Warp, frequently wraps to two centered lines
- Radius: full pill (`--radius-pill`)
- Padding: generous — roughly 20px vertical, 32px horizontal
- Hover: `--accent-hover` (`#13512e`)
- Active: `--accent-active` (`#0a2c19`)
- Use case: the primary "learn more" path

**Secondary CTA Pill** ("Batterijsimulatie")
- Background: White `#ffffff`
- Text: Dark Green `#0E3D23`, Tilt Warp
- Border: ~2px solid Dark Green `#0E3D23`
- Radius: full pill
- Use case: the "run the simulator" path — kept visually equal in weight to the primary pill so neither reads as an afterthought

### Logo Lockup
- Primary (light background): house-shaped mark — Emerald Green gable roof topped with a Yellow lightning-bolt chevron; stacked wordmark below — "mijn" in Emerald Green, "thuis" and "batterij" in Dark Green — all set in Tilt Warp; thin underline; italic Outfit tagline "besparing inzicht" ("savings insight"), with the "in" of "inzicht" set in italics for emphasis
- Reversed / "diapositief" (on Emerald Green background): white card containing the same house-icon glyph and wordmark, tagline set on a Dark Green underline bar — use this variant whenever the lockup sits on a green surface (e.g. the hero band); never place the primary dark-on-white lockup directly on green

### Dongel Mascot
- A smiling, rounded plug-shaped character: dark-green "plug prongs" forming an L-shape at the top, connected to a rounded Light Blue (`#9CD6E8`) body with two dot eyes and a simple curved smile
- Default component: the system's "feature bullet" — used inside a rounded-square Light-Blue chip (`--surface-warm`, `--radius-md`) beside each feature-list line, in place of a generic checkmark or emoji
- Use sparingly outside the feature-list context — Dongel is a mascot moment, not a repeating decorative pattern

### Illustration / Icon System
- Confirmed set: bar chart, lightbulb/target, lightning bolt, tree, plug-with-leaf, house, globe, sun, solar-panel grid, floor lamp — all energy/sustainability themed
- Construction rule: flat fill, no outlines, no gradients; each icon uses exactly one primary hue (Dark Green or Emerald Green) plus one accent hue (Yellow, Orange, or Light Blue) — never more than two colors per icon
- Orange (`--illustration-orange`, `#E94E1B`) appears only within this icon system (e.g. a bar-chart accent bar) — do not promote it to a general UI/button color

### Decorative Motifs
- A radial sun-burst / lightning-bolt shape in Yellow, unbordered, floating freely within the hero band — echoes the logomark's roofline chevron
- Used sparingly — one instance per hero, not a repeating pattern

## 5. Layout Principles

### Spacing & Grid
- Base rhythm: 4px grid (`--space-1` … `--space-12`)
- Section padding: 80px desktop / 56px tablet / 40px phone (`--section-y-*`)
- Container max width: 1200px, gutters 32px desktop / 24px tablet / 16px phone

### Composition
- The hero band is a full-bleed Emerald Green color field — the only place `--hero-bg` appears — containing the reversed logo lockup (top-left), a hamburger menu affordance (top-right), the floating yellow decoration, and the headline
- Below the hero, content sections sit on plain white with no tonal surface shift
- The feature list is a simple vertical stack of Dongel-chip + text rows, not a grid — reinforces a step-by-step, guided reading order
- The CTA pair sits side by side beneath the feature list, primary first (left), secondary second (right)

## 6. Depth & Elevation

No shadow or elevation evidence is documented in the house-style guide or the reference screenshot — the hero band, logo card, and buttons all read as flat, relying on color contrast and generous padding rather than shadows for separation. Inherit the schema's flat/whisper defaults (`--elev-flat`, `--elev-ring`, `--elev-raised`) rather than inventing a signature elevation treatment.

## 7. Do's and Don'ts

### Do
- Keep the palette to the five official colors — Dark Green, Emerald Green, Light Blue, Yellow, Orange — don't introduce additional hues.
- Use the reversed/"diapositief" logo lockup on any green background; never place the primary dark-on-white lockup on a colored surface.
- Reserve Tilt Warp for headers/subheadings/buttons and Outfit for body copy — don't swap their roles or mix in a third family.
- Use Dongel as the feature-list bullet consistently — don't substitute a generic checkmark or unrelated icon.
- Keep illustration-system icons to exactly two colors each (one primary + one accent), flat fill, no outlines.
- Write plain, reassuring, calculator-driven Dutch copy — lead with the outcome, not technical specifications.

### Don't
- Don't use Orange (`--illustration-orange`) as a button or general UI accent — it's illustration-system only.
- Don't set body copy in Tilt Warp, or headlines in Outfit — the two-family pairing is a deliberate role split.
- Don't add drop shadows or heavy elevation — the system reads as flat and confident, not "lifted."
- Don't make the secondary CTA visually subordinate (e.g. text-link-only) — both CTAs are first-class actions.
- Don't add outlines or gradients to illustration-system icons — flat fill only.

## 8. Responsive Behavior

*The house-style guide documents brand assets (logo, palette, type, icons) but not responsive layout rules; the following is inferred from the reference screenshot and generic friendly-consumer-site conventions — flagged accordingly.*

- **Hero**: headline and logo lockup stack to a single column on narrow viewports; the yellow decoration shrinks or repositions to avoid overlapping the headline text
- **CTA pair**: the primary/secondary buttons likely stack vertically (primary on top) below a certain width, rather than staying side-by-side
- **Feature list**: already a single-column stack, so no structural change expected across breakpoints — only spacing tightens
- **Touch targets**: CTA pills should meet or exceed 44×44px at all sizes given their prominence as the page's primary conversion actions

## 9. Agent Prompt Guide

### Quick Color Reference
- Dark ink / primary CTA: "Dark Green (#0E3D23)"
- Hero surface / success: "Emerald Green (#00A36F)"
- Energy accent / warn: "Yellow (#FFCD00)"
- Illustration-only accent: "Orange (#E94E1B)"
- Dongel mascot / feature-chip background: "Light Blue (#9CD6E8)"
- Page background: "White (#ffffff)"

### Example Component Prompts
- "Create a full-bleed hero band in Emerald Green (#00A36F) containing the reversed white logo card (house-icon glyph with Yellow lightning-bolt roofline, stacked 'mijn'/'thuis'/'batterij' wordmark in Tilt Warp, italic Outfit tagline), a floating Yellow (#FFCD00) sun/lightning decoration, and a bold two-line Tilt Warp headline at 56px."
- "Build a primary CTA pill: Dark Green (#0E3D23) background, white Tilt Warp label, full pill radius, generous padding, hover state lightens slightly to #13512E."
- "Build a secondary CTA pill: white background, Dark Green (#0E3D23) 2px border and Tilt Warp text — visually equal weight to the primary pill."
- "Draw the Dongel mascot: a smiling rounded plug character — dark-green L-shaped plug prongs at top, connected to a Light Blue (#9CD6E8) rounded body with two dot eyes and a simple curved smile — inside a rounded-square Light Blue chip."
- "Design a three-row feature list on white background, each row pairing a Dongel-chip icon with Outfit Semibold Dark Green (#0E3D23) text, making a plain-language claim about a home-battery simulator that sizes the right battery based on the user's own energy usage."
- "Create a flat two-tone illustration icon (e.g. a house, a solar panel grid, or a tree) using Dark Green or Emerald Green as the primary shape and Yellow, Orange, or Light Blue as a single accent — no outlines, no gradients."

### Iteration Guide
1. Keep the palette to the five official brand colors — if a sixth hue appears, remove it.
2. Reference exact hex values from this document rather than approximate color names.
3. Keep the Tilt Warp / Outfit role split intact — display face for headers/buttons, body face for paragraphs.
4. Keep copy plain-language and outcome-first — avoid technical battery/energy jargon in UI copy.
5. Default to Dongel as the feature-bullet icon rather than a generic checkmark.

### Known Gaps
- **Colors, typefaces, and the Dongel mascot are confirmed** from the official Studio Nieuwe Weide house-style guide — not estimated.
- **`--muted` and `--border` are derived, not brand-specified.** The house-style guide defines a 5-color brand palette but no full UI neutral ramp; these two values are conservative tints of the official Dark Green / Emerald Green rather than confirmed brand assets.
- **Responsive behavior (§8) is inferred**, not documented in the house-style guide.
- **Component-level pixel specs** (exact button padding, chip sizing, breakpoint widths) are estimated from a single reference screenshot, not measured from production CSS.
- **Font weights**: the house-style guide specifies Tilt Warp "Regular" and Outfit "Light" explicitly; any other weights used in this document (e.g. Outfit Semibold for feature-row emphasis) are reasonable extensions within each family's available cuts, not directly confirmed by the guide.
