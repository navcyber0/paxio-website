---
name: Paxio
description: Marketing and legal site for Paxio, an Android parental-controls app
colors:
  calm-teal: "#12B886"
  calm-teal-dark: "#0E9370"
  calm-teal-light: "#DFF4EC"
  calm-teal-mid: "#CDEFE2"
  warm-paper: "#F6F3EC"
  surface: "#FFFFFF"
  ink: "#14201A"
  ink-soft: "#5B6963"
  border: "#E7E2D6"
  coral: "#E24C36"
  coral-light: "#FDE2DE"
  blue: "#4C7CF0"
  blue-light: "#E7ECFC"
  purple: "#8B5CF6"
  purple-light: "#EFE6FB"
  orange: "#F5A623"
  orange-light: "#FFE9D9"
  dashboard-bg: "#10231D"
  dashboard-surface: "#16332A"
  dashboard-border: "#274238"
  dashboard-ink: "#EAF3EE"
  dashboard-ink-soft: "#9DB6AD"
typography:
  headline:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif"
    fontSize: "clamp(2.3rem, 4.2vw, 3.4rem)"
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1.8rem, 3vw, 2.4rem)"
    fontWeight: 800
    lineHeight: 1.25
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 600
  mono:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontWeight: 700
rounded:
  sm: "10px"
  md: "14px"
  lg: "20px"
  pill: "999px"
spacing:
  sm: "14px"
  md: "22px"
  lg: "28px"
  xl: "88px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.warm-paper}"
    rounded: "{rounded.pill}"
    padding: "15px 28px"
  button-primary-hover:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.warm-paper}"
  button-ghost:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "15px 28px"
  button-ghost-hover:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
  card-feature:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: "28px"
  nav-cta:
    backgroundColor: "{colors.calm-teal}"
    textColor: "#FFFFFF"
    rounded: "{rounded.pill}"
    padding: "9px 18px"
  nav-cta-hover:
    backgroundColor: "{colors.calm-teal-dark}"
    textColor: "#FFFFFF"
---

# Design System: Paxio

## Overview

**Creative North Star: "The Kitchen Table Talk"**

Paxio's site reads like a calm conversation at the kitchen table about a real parenting worry, not a pitch delivered from a stage. The warm paper background (`#F6F3EC`), soft fully-rounded pill buttons, and restrained single-accent color discipline all work together to keep the tone grounded and unhurried. Where the product needs to show real capability — the dashboard section with its usage charts, ring gauges, and monospaced numerals — the palette shifts to a quiet dark surface that feels like a control panel a parent checks in on, not a wall of alerts.

The system deliberately rejects the typical SaaS/startup marketing look: no urgency banners, no countdown timers, no glossy 3D gradients or stock-photo hero people, no aggressive contrast or oversized claims. Color is used sparingly and semantically (teal for trust/positive state, coral for blocked/restricted, blue for informational, orange for bedtime/time-based, purple for uninstall-protection) rather than decoratively. This matches the product's explicit brand commitment: authentic, safety-first, and never sales-y.

**Key Characteristics:**
- Warm, paper-toned neutral background instead of stark white or corporate blue
- One dominant accent (Calm Teal) used with restraint; secondary hues are functional, not decorative
- Fully rounded pill shapes for buttons, chips, and tags; softly rounded corners (14–20px) for cards
- A quiet dark "control room" surface reserved for the dashboard/usage-data section
- Monospace numerals (JetBrains Mono) wherever a real stat or value is shown, signaling honesty and precision
- Flat-at-rest surfaces; shadow appears only as a hover/interaction response, never as ambient decoration

## Colors

The palette is warm-neutral dominant with a single confident accent and functional secondary hues reserved for status meaning, not decoration.

### Primary
- **Calm Teal** (`#12B886`): the one brand accent — CTAs, links, active nav states, progress rings, positive/allowed status. Used with restraint; it should read as a deliberate signal, not a background wash.
- **Calm Teal Dark** (`#0E9370`): hover state for teal elements and dark-mode CTA text.
- **Calm Teal Light** (`#DFF4EC`) / **Calm Teal Mid** (`#CDEFE2`): tinted backgrounds for eyebrow pills, tags, "allowed" chips, and icon tiles.

### Secondary (status hues)
- **Coral** (`#E24C36`) + **Coral Light** (`#FDE2DE`): blocked/restricted state (app blocking, filtering denials).
- **Blue** (`#4C7CF0`) + **Blue Light** (`#E7ECFC`): informational/neutral status (content filtering, sync).
- **Orange** (`#F5A623`) + **Orange Light** (`#FFE9D9`): time-based features (bedtime scheduling, usage charts' mid-range values).
- **Purple** (`#8B5CF6`) + **Purple Light** (`#EFE6FB`): protective/administrative actions (uninstall protection, privacy).

### Neutral
- **Warm Paper** (`#F6F3EC`): page background — the grounding "kitchen table" tone, never pure white.
- **Surface** (`#FFFFFF`): cards, nav dropdown panels, FAQ items — anything that needs to lift slightly off the paper background.
- **Ink** (`#14201A`): primary text, headings, primary-button background.
- **Ink Soft** (`#5B6963`): secondary/body text, captions, muted nav links.
- **Border** (`#E7E2D6`): all hairline dividers, card borders, input borders.

### Dark "Control Room" surface (Dashboard section + dark color-scheme)
- **Dashboard BG** (`#10231D`) / **Dashboard Surface** (`#16332A`) / **Dashboard Border** (`#274238`): the dark, dashboard-only palette used for the usage-data section and for the site's `prefers-color-scheme: dark` mode. Text on this surface uses **Dashboard Ink** (`#EAF3EE`) and **Dashboard Ink Soft** (`#9DB6AD`).

### Named Rules
**The One Accent Rule.** Calm Teal is the only color allowed to represent a positive/primary action. Every other hue (coral, blue, orange, purple) is reserved for a specific status meaning and must not be reused as a generic decorative accent.

**The Paper, Not White Rule.** Page backgrounds use Warm Paper (`#F6F3EC`), never pure white. Pure white (`--surface`) is reserved for elements that need to visually lift off the page (cards, dropdowns, the nav's mobile menu).

## Typography

**Display/Body Font:** Inter (with system-ui fallback stack)
**Numeral/Mono Font:** JetBrains Mono

**Character:** Inter carries nearly all text at a confident 700–800 weight for headings, keeping the voice direct without shouting (no italics, no script faces). JetBrains Mono is reserved exclusively for real numeric values — ring-gauge readouts, stat cards, chip percentages — so a reader can tell "this number is live data" on sight.

### Hierarchy
- **Headline** (800, `clamp(2.3rem, 4.2vw, 3.4rem)`, 1.1 line-height, -0.02em tracking): hero `h1` only.
- **Title** (800, `clamp(1.8rem, 3vw, 2.4rem)`, tight tracking): section headings (`.section-head h2`).
- **Body** (400, 1rem–1.15rem, 1.55 line-height): paragraph copy; hero lead paragraph capped at 46ch for readability.
- **Label** (600, 0.72–0.95rem): tags, chips, nav links, button text — often uppercase with 0.04em tracking for tag/badge components specifically.
- **Mono numeral** (700, 1.15–1.5rem): ring-gauge values, dashboard stat values — always monospace, never Inter, wherever a figure represents real usage data.

### Named Rules
**The Mono-Means-Real Rule.** Any number representing live or real product data (screen time, stat cards, gauge readouts) renders in JetBrains Mono. Inter numerals are reserved for marketing copy (e.g. "4 controls") where the number is prose, not data.

## Layout

Content is constrained to a `1180px` max-width container with `28px` horizontal padding, centered throughout. Sections use a consistent `88px` vertical rhythm (`section { padding: 88px 0; }`), broken only by the dark dashboard section and the compact legal-page layout (`760px` max-width, tighter padding for long-form reading).

Grids are primarily `auto-fit`/`minmax` based (feature cards, contact cards, blog cards) so column count adapts without explicit breakpoints; a few key layouts (hero, benefits, flex-mode rows) collapse from a two-column grid to a single stacked column at `760–860px`. The mobile nav collapses into a `max-height`-animated dropdown below `760px`.

Scroll-triggered reveal is systemic: elements start `opacity: 0` / `translateY(28px)` and transition to visible on scroll (`.reveal` / `.reveal.is-visible`), giving every section a gentle arrival rather than an abrupt appearance.

## Elevation & Depth

Surfaces are flat at rest — cards and rows are distinguished by a `1px` warm-neutral border (`--border`) and a subtle background shift, not a shadow. Shadow (`--shadow: 0 12px 28px rgba(15, 40, 34, 0.1)`, doubled opacity in dark mode) appears only as a response to interaction: card hover-lift, the phone-mockup frames, the CTA banner, and dropdown panels. Depth is otherwise conveyed through tonal layering (Warm Paper → Surface → dark dashboard surface), not stacked shadows.

### Shadow Vocabulary
- **Ambient card shadow** (`box-shadow: 0 12px 28px rgba(15, 40, 34, 0.1)`): applied on `.feature-card:hover`, `.blog-card:hover`, and static on phone-frame mockups / the nav dropdown panel / the CTA banner, where it substitutes for a hover state that can't apply.
- **Primary button shadow** (`box-shadow: 0 10px 24px rgba(20, 32, 26, 0.22)`): a heavier, ink-tinted shadow reserved for `.btn-primary` only, giving the main CTA a slight lift off the page at rest.

### Named Rules
**The Flat-By-Default Rule.** Cards, rows, and containers are flat (border + background only) at rest. Shadow is earned by hover or by genuinely floating elements (phone mockups, dropdowns, the CTA banner) — it is never applied to a static content block just for depth.

## Shapes

Radius scales from tight to generous by surface size: `10px` (`--radius-sm`, inputs/small chips), `14px` (`--radius-md`, FAQ items, icon tiles), `20px` (`--radius-lg`, feature/contact cards), up to `26–36px` for phone-frame mockups and the CTA banner. Interactive controls that represent an action (buttons, nav CTA, tags, chips, screen-tour tabs) are always fully rounded pills (`999px`) — this is the single most consistent shape signal in the system. No sharp corners appear anywhere; the softest radius rule extends even to the mega-menu dropdown and legal-page icon tiles.

### Named Rules
**The Pill-For-Action Rule.** Anything the user can click that triggers navigation or a state change (buttons, tags, nav CTA, screen-tour tabs) is a `999px` pill. Anything that is a passive container (card, panel, mockup frame) uses the graduated `10–36px` radius scale instead, never a pill.

## Components

### Buttons
- **Shape:** fully rounded pill (`border-radius: 999px`).
- **Primary:** Ink background (`#14201A`), Warm Paper text, `15px 28px` padding, ink-tinted lift shadow (`0 10px 24px rgba(20, 32, 26, 0.22)`); hover lifts `-1px` via `transform`.
- **Ghost:** white/Surface background, Ink text, `1px` Border-colored outline; hover shifts border to Calm Teal (never a fill change).
- **Nav CTA:** smaller pill variant, Calm Teal background, white text, `9px 18px` padding; hover darkens to Calm Teal Dark.

### Chips / Tags
- **Tag** (eyebrow/section label): Calm Teal Light background, Calm Teal Dark text, uppercase, 0.04em tracking, pill radius.
- **Status chip** (hero "in action" row): three semantic variants — `.ok` (teal-light/teal-dark), `.blocked` (coral-light/coral), `.info` (blue-light/blue) — always paired with a mono value beneath the label.
- **Toggle switch:** `36×20px` pill track; `.on` = Calm Teal fill, `.off` = Coral fill — reuses the status-color vocabulary rather than a generic gray/green pattern.

### Cards / Containers
- **Corner Style:** `20px` (feature/contact/teaser cards), `18px` (blog cards), `22px` (dashboard cards).
- **Background:** Surface (white) on light sections; Dashboard Surface on the dark section.
- **Shadow Strategy:** flat at rest, lift shadow + `-3px` translateY on hover (see Elevation & Depth).
- **Border:** `1px solid var(--border)` (or `--dark-border` on dark cards) always present, even when a shadow is also shown.
- **Internal Padding:** `28px` standard (feature/teaser/contact cards), `20–26px` for denser dashboard/stat cards.

### Icon Tiles
- **Style:** `48×48px` (or `44px` for benefit rows, `32px` for legal-page inline icons) rounded-square tile in a tinted color, containing a small CSS-drawn glyph (no emoji, no icon font). Each feature keeps a fixed color-to-concept mapping (teal = limits, orange = bedtime, coral = app blocking, blue = filtering, purple = uninstall protection).
- **Motion:** feature-grid icon tiles (not feature-row or contact-card variants) float gently via `iconFloat` (±5px, 5s ease-in-out loop) to signal "live," never on icons inside dense list rows.

### Inputs / Fields
- No custom text-input styling is currently implemented in the shared stylesheet (the site has no live form fields yet; contact page routes to email/external channels). Any new input should inherit the system's `10px` radius, `1px` Border stroke, and Calm Teal focus treatment consistent with the button-ghost hover pattern.

### Navigation
- **Style:** sticky, translucent Warm-Paper blur (`backdrop-filter: blur(10px)`) over a `1px` Border bottom edge; scrolls with the page beneath it.
- **Typography:** 0.95rem/500 links in Ink Soft; active/hover state darkens to Ink or Calm Teal respectively.
- **Mega-menu:** hover/focus-revealed dropdown panel, `16px` radius, ambient shadow, teal-light hover row background.
- **Mobile:** collapses under a `max-height` checkbox-driven toggle below `760px`; links gain full-width row borders and the nav CTA becomes a centered full-width pill.

### Phone Mockup Frame (signature component)
A recurring gradient-bordered frame (`linear-gradient(160deg, teal, teal-dark)`, `10px` padding, `28–36px` radius) wraps every product screenshot across hero, screen-tour, and benefits sections. It's the system's one consistently reused "signature" device — always teal-gradient, never a plain border, reinforcing brand color even where the screenshot itself carries none.

## Do's and Don'ts

### Do:
- **Do** keep the page background Warm Paper (`#F6F3EC`) and reserve pure white for elements that need to visually lift (cards, dropdowns).
- **Do** use JetBrains Mono for any number that represents real product data; keep Inter for numbers used in prose.
- **Do** make every clickable action element (buttons, tags, chips, nav CTA) a fully rounded pill; reserve the graduated radius scale for passive containers.
- **Do** keep shadows flat-at-rest and earn them only through hover or genuinely floating elements (mockup frames, dropdowns, CTA banner).
- **Do** keep the dark "control room" palette scoped to data/dashboard contexts (usage charts, stat cards) rather than spreading it across marketing sections.

### Don't:
- **Don't** introduce glossy gradients, 3D bevels, countdown timers, or urgency banners — they contradict the confirmed "not sales-y" brand voice and the deliberate rejection of typical SaaS marketing visuals.
- **Don't** use stock-photo hero imagery of people; the system relies on real product screenshots inside the teal gradient phone frame instead.
- **Don't** apply a secondary status hue (coral/blue/orange/purple) decoratively outside its established meaning (blocked/informational/time/protective) — Calm Teal is the only general-purpose accent.
- **Don't** add drop shadows to static content blocks that aren't hovering or floating; depth comes from tonal layering and borders first.
