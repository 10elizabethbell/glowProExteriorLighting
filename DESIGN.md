---
name: Glow Pro Booking Widget
description: A Jersey Shore roofline at night, strung with C9 bulbs that light up as the booking form fills.
colors:
  signal-red: "#e0262b"
  signal-red-hot: "#f23a3f"
  bulb-warm: "#ffd27a"
  bulb-red: "#ff2d2d"
  bulb-white: "#fff1cc"
  bulb-blue: "#2aa6ff"
  night: "#0d1a35"
  night-sky: "#16295a"
  house: "#14254a"
  card: "#122248"
  well: "#0a1530"
  well-selected: "#1c2f5e"
  edge: "#2e4273"
  edge-hover: "#4a609a"
  cream: "#f6f0e3"
  mist: "#b7c3de"
  placeholder: "#8f9fc4"
  err-text: "#ffb0a6"
  err-edge: "#ff7a70"
typography:
  display:
    fontFamily: "Anton, 'Arial Narrow', sans-serif"
    fontSize: "clamp(46px, 6.6vw, 92px)"
    fontWeight: 400
    lineHeight: 0.98
    letterSpacing: "0.005em"
  headline:
    fontFamily: "Anton, 'Arial Narrow', sans-serif"
    fontSize: "clamp(34px, 4.4vw, 58px)"
    fontWeight: 400
    lineHeight: 1
  title:
    fontFamily: "Anton, 'Arial Narrow', sans-serif"
    fontSize: "32px"
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: "0.01em"
  title-sm:
    fontFamily: "Anton, 'Arial Narrow', sans-serif"
    fontSize: "24px"
    fontWeight: 400
    lineHeight: 1.1
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "14.5px"
    fontWeight: 650
    lineHeight: 1.3
  meta:
    fontFamily: "-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 400
    lineHeight: 1.45
rounded:
  field: "12px"
  tile: "14px"
  panel: "16px"
  card: "22px"
  pill: "999px"
spacing:
  gap-chip: "8px"
  gap-tile: "10px"
  gap-field: "14px"
  gutter-phone: "16px"
  gutter-desktop: "32px"
  card-pad-x: "28px"
  section-gap: "64px"
components:
  button-primary:
    backgroundColor: "{colors.signal-red}"
    textColor: "#ffffff"
    typography: "{typography.label}"
    rounded: "{rounded.tile}"
    padding: "0 18px"
    height: "54px"
    width: "100%"
  button-primary-hover:
    backgroundColor: "{colors.signal-red-hot}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.cream}"
    rounded: "{rounded.tile}"
    padding: "0 18px"
    height: "54px"
    width: "100%"
  button-call:
    backgroundColor: "transparent"
    textColor: "{colors.cream}"
    rounded: "{rounded.pill}"
    padding: "0 16px"
    height: "42px"
  booking-card:
    backgroundColor: "{colors.card}"
    textColor: "{colors.cream}"
    rounded: "{rounded.card}"
    padding: "74px 28px 26px"
  service-tile:
    backgroundColor: "{colors.well}"
    textColor: "{colors.cream}"
    rounded: "{rounded.tile}"
    padding: "12px"
  service-tile-selected:
    backgroundColor: "{colors.well-selected}"
    textColor: "{colors.cream}"
  chip:
    backgroundColor: "{colors.well}"
    textColor: "{colors.mist}"
    rounded: "{rounded.pill}"
    padding: "0 14px"
    height: "40px"
  chip-selected:
    backgroundColor: "{colors.well-selected}"
    textColor: "{colors.cream}"
  input:
    backgroundColor: "{colors.well}"
    textColor: "{colors.cream}"
    typography: "{typography.body}"
    rounded: "{rounded.field}"
    padding: "0 14px"
    height: "50px"
---

# Design System: Glow Pro Booking Widget

Source of truth: `index.html` (single file; CSS custom properties in `:root`, canvas motion in the `LIGHT STRINGS` script). Motion, shadows, breakpoints and component snippets live in `.impeccable/design.json`.

## Overview

**Creative North Star: "Flipping On the Lights"**

The page is a winter night on the Jersey Shore. A navy sky (never black) with light snow sits over a house whose roofline is strung with real-feeling C9 bulbs in the logo's red, warm white and blue. The booking card is part of that scene. It has its own short string of bulbs, and each valid answer lights one more. Anton caps carry the voice, borrowed from glowpronj.com. A plain system sans does the work everywhere else.

The world is built from three materials. Night ground is tonal navy layers. Glass light is the canvas bulbs and their additive halos. Warm-white glow is the single UI accent for focus, selection and emphasis. Everything else stays quiet. Inputs are dark wells with a hairline edge, and type is cream or mist. The only saturated fill on the page is one red button.

The same file runs in two modes. The full demo page includes a hero roofline, a "how it works" house section and a footer string. Embed mode (`?embed=1`) shows only the card on a transparent ground for an iframe on the client's WordPress site. `&urgency=off` hides the holiday line.

**Key Characteristics:**
- Navy tonal layering, no black, no white surfaces.
- One accent role (warm bulb gold) for every focus, selection and highlight state.
- Red only for the commit action, because it is the logo's red.
- Bulbs are the decoration. The motion is physics (verlet wire, swinging sockets) and nothing is keyframed except the urgency blink and the done-state rise.
- The house color is the section divider. Where the roof (or the footer's wire) meets the sky, the color changes.

## Colors

A cold, saturated night palette (hue ~265 in OKLCH) lit by three bulb colors. Warm gold is the only warm UI color.

### Primary
- **Signal Red** (`signal-red`): fill for the one commit button per view ("Text my request", "Open messages again"). Hover goes to **Signal Red Hot**. It is never used for text or borders. Errors have their own colors.

### Secondary
- **Bulb Warm Gold** (`bulb-warm`, CSS `--warm`): the interaction light. It covers the focus ring (2px outline, 3px offset), selected tile and chip borders, selected service icons, `::selection`, the caret, the second line of the hero headline, the urgency line and the done-state heading.

### Tertiary (bulb glass, canvas and dots only)
- **Bulb Red / Bulb White / Bulb Blue** (`bulb-red`, `bulb-white`, `bulb-blue`): base glass colors for the C9 sprites and the small CSS `.dot` bulbs (fact list, step markers, urgency dot). Each has a light highlight, a dark rim and two "off" tones defined in `COLORS` in the script. Strings cycle red, white, blue. These are never used for UI fills or text.

### Neutral
- **Night** (`night`): page ground, footer ground, `theme-color`.
- **Night Sky** (`night-sky`): the horizon glow, a radial gradient behind the roof at the bottom of the hero.
- **House** (`house`): the roof polygon, the "how it works" section and the footer's fill above its wire. One color, so the roofline reads as the divider.
- **Card** (`card`): booking card surface and the code-panel button.
- **Well** (`well`): inputs, service tiles, chips, the message preview and the code panel. These are wells sunk into the card.
- **Well Selected** (`well-selected`): a checked tile or chip lifts one step toward the card.
- **Edge / Edge Hover** (`edge`, `edge-hover`): 1.5px control borders, scrollbar thumb and section hairlines. Hover moves to `edge-hover`.
- **Cream** (`cream`): primary text. Translucent cream (`rgba(246,240,227,.5–.55)`) is the outline for ghost and call buttons.
- **Mist** (`mist`): secondary text, subs, hints, captions, footer copy and unselected chip text.
- **Placeholder** (`placeholder`): input placeholders only.
- **Error** (`err-text`, `err-edge`): inline error text and the invalid border. They are deliberately pink-salmon so they never read as Signal Red.

### Named Rules
**The One Warm Light Rule.** Every "this is active" state uses Bulb Warm Gold: focus, checked, selected, highlighted. Don't introduce a second accent for state.

**The Red Is the Button Rule.** Signal Red fills the one primary action per view and nothing else.

**The Never-Black Rule.** The darkest value is `well`. Shadows use a navy-black `rgba(2,7,20,…)`, never `#000`.

## Typography

**Display Font:** Anton (fallback 'Arial Narrow', sans-serif), latin subset inlined as base64 `@font-face`.
**Body Font:** system UI stack (-apple-system, Segoe UI, Roboto, …).
**Mono:** ui-monospace / SF Mono / Menlo, used only in the embed-snippet code panel (13.5px/1.6).

**Character:** Anton is condensed, loud, all caps and sign-like, and it matches the client's own site. The system sans keeps the form fast and native-feeling on phones.

### Hierarchy
- **Display** (`display`): hero H1 only, uppercase, `text-wrap: balance`. The second clause sits on its own line in Warm Gold.
- **Headline** (`headline`): section H2 ("From your website straight to your phone"), uppercase, max 16em.
- **Title** (`title`): booking card H2, uppercase. 29px at ≤520px. The 30px "Paste this where you want it" heading is the same role.
- **Title Small** (`title-sm`): done-state heading (Warm Gold) and footer business name. Uppercase.
- **Body** (`body`): 16px base. Hero pitch scales `clamp(16px, 1.45vw, 20px)` with max 34em. Step copy is max 34ch and embed copy max 44ch. Step titles are system sans at 19px/1.3.
- **Label** (`label`): legends, field labels, the urgency line (600) and the "Prefer to talk?" line. The 650 weight is used throughout for emphasis: buttons (17px), tile titles (15px) and the call pill (15px).
- **Meta** (`meta`): hints, notes and errors (13–13.5px). Tile subtitles are 12.5px.

### Named Rules
**The Anton Is Always Caps Rule.** Anton appears only at weight 400, uppercase, line-height ≤1.1. It's for headings only and never for body text, labels or buttons.

## Layout

- **Container:** 1240px max, 32px gutters (16px at ≤960px).
- **Hero (desktop):** a two-column grid `minmax(0,1fr) 460px` with a 64px column gap. Copy sits top left, the photo bottom left and the booking card spans both rows on the right. The sky runs under the top bar (`margin-top: -90px`).
- **Hero (≤960px):** one column at max 560px. Hero facts are hidden. The order is copy, card, photo, and the photo bleeds to the edges. The copy gets 96px of bottom margin so the roof peaks have room above the card.
- **≤520px:** the card padding tightens to 70/18/22, name and phone stack, and service tiles drop to an icon-over-text layout (min-height 96px).
- **How it works:** three equal columns of steps (gap 40px), then a 5fr/7fr split for the embed copy and code panel. Both stack at ≤960px.
- **Footer:** 120px top padding (104px on phone) leaves room for the footer light string. The grid is name/contact on the left and towns on the right.
- **Embed mode:** everything except the card is `display:none`. The body is transparent, the grid becomes a block at max 480px with 18/8/16 padding, and only the card's own string runs.
- **Rhythm:** spacing is hand-tuned rather than on a strict scale. Recurring steps are 8 (chips), 10 (tiles, button stacks), 14 (field-to-field), 18 (fieldsets) and 22 (header-to-form, done block).

## Elevation & Depth

Depth comes from tonal layering first. The order from back to front is night, house, card and well, and wells sit *below* the card. Shadows are few, soft, long and navy-tinted, and they only lift objects that sit in front of the scene. Light is the other depth cue: bulbs draw with additive `lighter` halos that bloom over whatever is behind them.

### Shadow Vocabulary
- **Card lift** (`0 34px 70px -24px rgba(2,7,20,.8), 0 8px 22px -10px rgba(2,7,20,.5)`): the booking card only.
- **Panel lift** (`0 18px 40px -22px rgba(2,7,20,.9)`): the embed code panel.
- **Primary press** (`0 10px 22px -12px rgba(2,7,20,.8)`): the red button.
- **Selected tile** (`0 8px 18px -10px rgba(2,7,20,.7)`): a checked service tile.
- **Bulb glow** (`0 2px 8px rgba(<bulb>, .55)`): CSS `.dot` bulbs. Colored glow is reserved for bulbs.

### Named Rules
**The Only Glow Is a Bulb Rule.** Colored glow and bloom belong to bulbs (canvas halos, `.dot` shadows). UI controls never glow. Their active state is a gold border.

## Shapes

Soft, friendly rounding that gets larger as the container grows: fields 12px, tiles and buttons 14px, panels 16px, the card 22px (20px on phone), and pills for chips and the call button. Control borders are always 1.5px and hairline dividers 1px `edge`. The two organic silhouettes are the C9 teardrop (canvas bezier, and the CSS `.dot` with `border-radius: 50% / 40% 40% 60% 60%`) and the roof polyline with gable peaks (`ROOF` points, plus a 7px `#1d3363` fascia stroke). The hero photo has no frame. A two-axis gradient mask dissolves its edges into the sky.

## Components

### Buttons
- **Shape:** gently rounded (`rounded.tile`), 54px tall, full width, 1.5px border, 650 weight at 17px, with an optional 20px stroke icon (1.9 stroke, round caps).
- **Primary:** Signal Red fill, white text, translucent cream border, primary-press shadow. Hover goes to Red Hot with a full cream border.
- **Ghost:** transparent with a translucent cream border. Hover adds a 7% cream wash and a full cream border.
- **Press:** `translateY(1px)` on `:active`. Transitions run .18s on colors and .12s on transform.
- **Call pill:** 42px (40px on phone) with a pill radius, used in the top bar.
- **Text link button:** mist, underlined, cream on hover ("Edit my details").

### Chips
- **Style:** 40px pill on `well`, `edge` border, mist text at 14px.
- **State:** hover changes the border to `edge-hover`. Checked gets a gold border, cream text and the `well-selected` fill. The checkbox is visually hidden and the focus ring moves to the span.

### Service tiles (radio cards)
- **Style:** `well` with an `edge` border, 14px radius and min-height 78px. A 28px line icon (stroke mist, 1.7) sits left of the title (650, 15px) and mist subtitle (12.5px). Two columns.
- **Icon detail:** each icon has `.lit` dots (its "bulbs") that fill mist at rest and gold when selected.
- **State:** hover changes the border to `edge-hover`. Checked gets a gold border, the `well-selected` fill and the selected-tile shadow, and the icon turns gold. Invalid gives every tile an `err-edge` border.

### Inputs / Fields
- **Style:** 50px tall, `well` fill, 1.5px `edge` border, 12px radius, 16px text (prevents iOS zoom). Labels sit above in `label` style.
- **Focus:** the border turns gold, plus a 2px gold outline at 2px offset on `:focus-visible`.
- **Error:** `aria-invalid` gives an `err-edge` border and the error text sits below in `err-text`. Errors appear only after a field is touched and clear live while it is being fixed.
- **Date:** a custom iOS-only placeholder overlay ("blank box" fix), and the picker indicator is tinted to suit the dark scheme.

### Booking card (signature)
Card surface with 22px radius and the card-lift shadow. The top padding is 74px to make room for its light string (a canvas overhanging the card by 6px each side and 14px above). Inside, in order: Anton title, mist sub, an optional urgency line (gold 600 text after a blinking red `.dot`, 2.4s), the form, the red submit button, a mist note, then a hairline and the "Prefer to talk?" ghost call button. On submit the form is replaced by the done state (rises in over .5s `cubic-bezier(.16,1,.3,1)`): a gold title, the message preview in a well using `pre-wrap`, the red and ghost buttons, and an email fallback. Everything is prefixed `gpw-`, so it survives being pasted into a WordPress page.

### Light strings (signature motion)
All three strings run on one engine in the `LIGHT STRINGS` script:
- **Rope:** pinned clips with 4–6 verlet nodes per span, an initial sine sag of 18% of the span, and slack of 1.12–1.16. Eight constraint passes per frame. The wire can go slack but never stretch. Bulbs hang on every other node and cycle red, white, blue. Each bulb swings on its socket, lagging the wire (it follows 45% of the wire angle, with spring .07 and damping .09).
- **Forces:** gravity, plus a two-sine wind whose gust swells and fades slowly. Pointer or finger within `pushRadius` shoves nodes outward and passes on some of the pointer's velocity. Bulbs near the pointer brighten by up to 35%.
- **Render:** a 2px dark-green wire (`#27493a`), clip dots, then the cached unlit sprite with the lit sprite cross-faded over it by brightness, then additive halo sprites. Brightness includes a per-bulb twinkle.
- **Hero roofline:** a gabled roof polyline (`ROOF`) with clips every 84px (60px on phone) and 19px bulbs (15px on phone), plus snow (46 flakes on desktop, 18 on phone) that parts around the pointer. Desktop sets the eave at the first-screen bottom, above the photo, with peaks clear of the copy. When stacked, the eave sits 32px below the card top, so the card stands on the house. A static SVG roof is shown until JS is ready.
- **Card progress string:** 5 spans and 16px bulbs, all starting off. `GlowStrings.progress(validFields / 5)` lights the first N bulbs, and each newly lit bulb pops. Lit state survives resizes.
- **Footer divider:** a full-width string with 17px bulbs (14px on phone) and color offset 1. The `house` color fills everything *above* the wire, so the wire itself is the house/footer edge.
- **Shared loop:** one `requestAnimationFrame` steps every visible scene. IntersectionObserver pauses offscreen canvases, and the loop sleeps when none are visible and wakes on pointer movement. DPR is capped at 2. Resize rebuilds are debounced 120ms and skip height-only changes (phone URL bar). On submit, `GlowStrings.cheer()` runs a pop chase along every string.
- **Reduced motion:** the loop never starts, strings are drawn once, bulbs light instantly, and all CSS animation and transitions are off.
- **Tunables (`TUNE`):** gravity .32, damping .975, windBase .05, windGust .045, windSpeed 1.9, pushRadius 95, push 2.4, carry .16, twinkle .16, snowDesktop 46, snowPhone 18. Change these before changing code.

### Embed mode
`?embed=1` adds `.is-embed` to `<html>` before first paint, so the demo shell never flashes. In embed mode the color-scheme stays normal (otherwise the iframe gets an opaque canvas), card links open in `_top`, and the card posts `gpw-height` on resize and `gpw-done` on submit to the host page. `&urgency=off` adds `.no-urgency`. The `URGENCY` / `URGENCY_TEXT` constants are the in-file switch.

## Do's and Don'ts

### Do:
- **Do** take every color from `:root` custom properties. Add a variable before adding a literal.
- **Do** use Warm Gold for every focus, selected and highlight state, with focus rings at 2px and an offset.
- **Do** keep Anton uppercase at 400 for headings, and the system sans for everything you read or tap.
- **Do** make new decoration out of the bulb vocabulary (C9 sprites, `.dot` bulbs, `.lit` dots in icons), cycling red, white, blue.
- **Do** tune motion through `TUNE` and keep every canvas on the one shared loop with IntersectionObserver pausing.
- **Do** keep any new widget CSS prefixed `gpw-` and check it in `?embed=1` on a transparent ground.

### Don't:
- **Don't** use pure black or white surfaces. The ground is navy and text is cream.
- **Don't** use Signal Red for anything but the primary button. Errors use the salmon `err` pair.
- **Don't** add glows, gradients or colored shadows to UI controls. Glow belongs to bulbs.
- **Don't** start a second animation loop or keyframe the strings. Motion is physics, and it must stop under `prefers-reduced-motion`.
- **Don't** add a divider line between hero and house or between house and footer. The roof and the footer wire are the dividers.
