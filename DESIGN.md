---
name: Glow Pro Exterior Lighting
description: A calm, banded booking page that lets the customer's own lit-up home do the selling and turns a visit into a pre-written text.
colors:
  bulb-gold: "#ffc24a"
  bulb-gold-bright: "#ffd27a"
  gold-ink: "#8a5a00"
  logo-blue: "#0b7fd1"
  night-navy: "#15295a"
  deep-navy: "#0b1834"
  paper: "#f4f6fb"
  card-white: "#ffffff"
  ink: "#0d1b3d"
  body-slate: "#2a3650"
  soft-slate: "#4a5670"
  on-dark: "#f4f7fb"
  on-dark-soft: "#c6d1e8"
  hairline: "rgba(13,27,61,.12)"
  error-red: "#b3261e"
typography:
  display:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(42px, 12vw, 80px)"
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: "-0.005em"
  headline:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(30px, 7.6vw, 48px)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-0.005em"
  title:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(20px, 5.4vw, 23px)"
    fontWeight: 400
    lineHeight: 1.2
  label:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.2
  button:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1
  lede:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(17px, 4.6vw, 19px)"
    fontWeight: 400
    lineHeight: 1.5
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.7
  small:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.4
rounded:
  field: "10px"
  tile: "16px"
  card: "24px"
  pill: "999px"
spacing:
  gutter-phone: "20px"
  gutter-desktop: "40px"
  tile-gap: "10px"
  card-gap: "20px"
  form-gap: "22px"
  card-padding: "clamp(20px, 5vw, 32px)"
  band-phone: "64px"
  band-desktop: "96px"
components:
  button-primary:
    backgroundColor: "{colors.bulb-gold}"
    textColor: "{colors.ink}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-primary-hover:
    backgroundColor: "{colors.bulb-gold-bright}"
    textColor: "{colors.ink}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.on-dark}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  booking-card:
    backgroundColor: "{colors.card-white}"
    rounded: "{rounded.card}"
    padding: "{spacing.card-padding}"
  input-field:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.field}"
    padding: "13px 14px"
    height: "52px"
  service-tile:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.tile}"
    padding: "12px 14px"
    height: "76px"
  service-tile-selected:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.card-white}"
  chip:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 18px"
    height: "48px"
  chip-selected:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.card-white}"
  step-marker:
    backgroundColor: "{colors.bulb-gold}"
    textColor: "{colors.ink}"
    size: "48px"
  text-float:
    backgroundColor: "{colors.bulb-gold}"
    textColor: "{colors.ink}"
    size: "60px"
---

# Design System: Glow Pro Exterior Lighting

## Overview

**Creative North Star: "The Lit Porch at Dusk"**

The page is a quiet, orderly street at night: off-white paper bands for reading and filling in, night-sky navy bands for arrival and sign-off, and one warm bulb gold that behaves like the lights themselves, a fill that glows rather than a colour that talks. The customer's own photo of a lit roofline is the only spectacle; everything around it stays calm so the work does the selling.

Density is generous and phone-first. Bands stack full-bleed, content sits in one 1160px column, and the booking card is the destination of every primary action. Rounded, soft-cornered forms (24px containers, pill actions) keep the tone friendly and domestic rather than corporate. Depth is mostly tonal; only the booking card and the floating text circle lift.

The world was revamped on 2026-10-19 from a festive light-string look. That earlier world (condensed caps display, canvas light strings, red buttons, seasonal mascots) is retired and lives only in git history; nothing from it carries forward.

**Key Characteristics:**
- Full-bleed bands in three grounds: paper, night navy, deep navy with a faint diagonal line texture.
- One accent, bulb gold, used as a fill; gold-ink when gold must be text on a light ground.
- The logo's blue reserved for form hover and focus outlines on light grounds.
- Cal Sans at a single weight (400) for every heading, label, button and phone number; system sans for running text.
- Pill buttons and chips, 24px cards, 16px inner tiles, 10px fields.
- Motion is a greeting, not a performance: one H1 letter bounce-in and one 12px fade-up, both absent under reduced motion and without JS.

## Colors

A cool night-sky palette (paper, two navies, slate text) warmed by a single bulb gold.

### Primary
- **Bulb Gold** (`bulb-gold`): the one accent. Fills the primary button, the floating text circle, numbered step markers, the dot in label pills, and text selection. Also the colour of accent words inside headings and of icons on dark bands, where it passes contrast.
- **Bright Bulb** (`bulb-gold-bright`): hover state of gold fills only.
- **Gold Ink** (`gold-ink`): gold as text or icon on a light ground (5.3:1 on paper): accent words in headings on paper, the header phone icon and hover, the claim icons.

### Secondary
- **Logo Blue** (`logo-blue`): the logo's blue, used only as the hover and focus outline of form controls and links on light grounds (fields, service tiles, chips, the card's submit button, text links). It keeps "you are here" distinct from the gold "do this" fill.

### Neutral
- **Night Navy** (`night-navy`): hero and closing bands; also the input caret.
- **Deep Navy** (`deep-navy`): the "how it works" band and the footer, always with the diagonal texture; also the code block ground inside the deep band.
- **Paper** (`paper`): page ground, header, and the resting fill of fields, tiles, chips and the message preview inside the white card.
- **Card White** (`card-white`): the booking card surface only.
- **Ink** (`ink`): headings and labels on light, text on gold, and the selected fill of service tiles and chips.
- **Body Slate** (`body-slate`): running text on light.
- **Soft Slate** (`soft-slate`): ledes, hints, sub-copy, placeholders, the "(optional)" note.
- **On Dark** (`on-dark`): headings and primary text on navy.
- **On Dark Soft** (`on-dark-soft`): running text on navy.
- **Hairline** (`hairline`): the 1px divider between claim rows.
- **Error Red** (`error-red`): inline error text and the bad-field border.

### Named Rules
**The Bulb Gold Rule.** Gold is a light, not ink: it fills, and anything sitting on it is Ink. On paper or white, gold never appears as text; use Gold Ink instead. On navy, gold text is allowed for accent words and icons.

**The Two Outlines Rule.** On light grounds every hover and focus outline is Logo Blue; on navy and deep bands (hero, how it works, close, footer) the focus outline switches to Bulb Gold. Never use gold as a focus ring on paper.

**The Ink Selection Rule.** A chosen option turns solid Ink with white text. Selection is never shown in gold, so the only gold in the card is the submit button.

## Typography

**Display Font:** Cal Sans (with Avenir Next, Segoe UI, system-ui)
**Body Font:** the platform system sans (-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial)
**Label/Mono Font:** ui-monospace stack, only for the embed snippet code block (13px / 1.55)

**Character:** a rounded, slightly tight geometric display face that reads warm and confident at any size, paired with the phone's own sans for everything you read at length.

### Hierarchy
- **Display** (400, clamp 42px to 80px, 1.02): the hero H1 only, white on navy, max 12ch, balanced.
- **Headline** (400, clamp 30px to 48px, 1.08): band headings. The booking card heading is a slightly smaller step (clamp 30px to 40px); the snippet panel heading drops to clamp 24px to 30px.
- **Title** (400, clamp 20px to 23px, 1.2): claim rows, step titles (21px, 22px on desktop), service tile names (17px).
- **Label** (400, 17px, 1.2): form legends and field labels, in Ink.
- **Button** (400, 18px, 1): every button and the header phone number (17px, 20px desktop). The closing phone number scales up to clamp 30px to 52px.
- **Lede** (400, clamp 17px to 19px, 1.5): the hero promise (to 20px) and section ledes, Soft Slate, max 34 to 38ch.
- **Body** (400, 16px, 1.7): running text, field input text, chips.
- **Small** (400, 14px to 15px): hints, errors, the "opens your messages" note, tile sub-lines.

### Named Rules
**The One Weight Rule.** Cal Sans is only ever set at 400. Hierarchy comes from size, never from bolding the display face.

**The Display Speaks Rule.** Anything the customer reads as a heading, a choice, a label or a call to act (buttons, phone numbers, tile names, step numbers) is Cal Sans; anything they read as an explanation is system sans.

## Layout

One centred column (max 1160px) with a 20px gutter on phones and 40px from 760px. Sections are full-bleed bands with 64px vertical padding on phones and 96px from 760px.

Band order on the full page: paper header (logo left, tap-to-call number right, 72px tall, 84px desktop), textured night-navy hero, paper booking band, textured deep "how it works" band, plain night-navy close, textured deep footer. The footer leaves 96px plus the safe-area inset at the bottom so the floating circle never covers its content.

- **Phones (default):** everything stacks. Hero copy, then two full-width stacked buttons, then the photo card. The booking card comes before the claims list.
- **760px and up:** hero buttons sit side by side (min 240px each).
- **1024px and up:** hero splits copy and photo 1 : 1.25; the booking band splits claims (sticky, 40px from top) and card 1 : 1.15 with claims on the left; name and phone pair up; steps go three across; the snippet panel splits 5 : 7; the close puts the big phone number bottom-right.
- **Phones held sideways (landscape, height 500px or less):** the header shrinks to 52px with an 88px logo, the hero goes two-column with a smaller H1 (clamp 28px to 40px on viewport height) and 48px buttons side by side, so the offer and both buttons fit the first screen.
- **Narrow phones (380px or less):** tile and chip padding tighten.

**The Card Is The Destination Rule.** Every primary action on the page leads to the booking card or a phone link; nothing else competes for the primary button.

## Elevation & Depth

Depth is tonal first: paper against white, navy against deep, and the diagonal line texture (a 1px white line at 3.5% every 23px, at 135 degrees) on the hero, deep band and footer. Only two things lift, both with soft, navy-tinted ambient shadows. There are no hard offset shadows and no shadows on buttons, tiles or fields.

### Shadow Vocabulary
- **Card lift** (`box-shadow: 0 18px 50px rgba(13,27,61,.08)`): the booking card on paper.
- **Embedded card lift** (`box-shadow: 0 8px 30px rgba(13,27,61,.12)`): the same card inside an iframe, tighter so it reads on an unknown host page.
- **Float lift** (`box-shadow: 0 10px 28px rgba(8,18,46,.3)`): the floating text circle.

### Named Rules
**The Quiet Texture Rule.** The diagonal texture is faint enough to be felt rather than seen. It belongs to navy grounds only; never on paper or inside the card.

## Shapes

A family of soft rounds, scaled by size: 24px for containers (booking card, hero photo, snippet panel), 16px for elements inside a container (service tiles, the message preview, the code block), 10px for text fields, full pills for buttons, chips and label pills, and circles for the numbered step markers and the floating text circle. Focus outlines take a 6px round. Borders are rare: inputs, tiles and chips carry a 2px transparent border that only colours on hover, focus, error or selection, so states never shift layout.

**The Nested Round Rule.** An element inside a 24px container uses 16px or less; nothing inside the card is rounder than the card except pills.

## Components

### Buttons
- **Shape:** full pill (999px), 56px tall, 26px side padding, Cal Sans 18px, optional 20px stroke icon leading.
- **Primary:** Bulb Gold fill and border, Ink text. One per view: "Book a free consultation" in the hero, "Text my request" in the card.
- **Hover / Focus:** primary brightens to Bright Bulb; inside the card buttons also take a 2px Logo Blue outline at 2px offset. Hover styles exist only on devices with a real pointer. Press scales to 0.98.
- **Ghost (on navy):** transparent, On Dark text, 2px border of On Dark at 70%; hover goes to a full white border and a 10% white wash. On the deep band it hovers with a gold outline.
- **Line (on light):** transparent, Ink text, 2px Ink border at 35%, hover to full Ink. Used for "Copy message".
- **Link button:** underlined Ink text with a 35% Ink underline, 44px tall target; hover turns Logo Blue with an outline.

### Booking Card (signature)
The one self-contained component: white, 24px radius, clamp 20px to 32px padding, 20px internal gap, max 600px wide, soft card lift. Heading, a Soft Slate sub-line, then the form at a 22px rhythm.
- **Service tiles:** a two-column grid of four tinted tiles (Paper, 16px round, min 76px tall), each a Cal Sans name over a Soft Slate sub-line. Selected turns solid Ink with white name and On Dark Soft sub-line. Hover and keyboard focus draw the 2px Logo Blue border. Behaves as a radio group.
- **Add-on chips:** wrapping row of Paper pills, 48px tall, system 16px text; selected turns Ink with white text. Multi-select.
- **Fields:** Paper fill, 2px transparent border, 10px round, 52px tall, 16px text (no zoom on iOS), Soft Slate placeholder. Hover and focus colour the border Logo Blue; no outline glow. The date field shows a "Tap to pick a day" placeholder only where iOS renders a blank box. Name and phone pair up from 1024px.
- **Inline errors:** validated on submit only. A bad field's border turns Error Red, a 15px Error Red sentence appears beneath it saying exactly what to fix, the control gets `aria-invalid`, and focus moves to the first bad field. Each error clears the moment its field becomes valid.
- **Footnotes:** a centred Soft Slate 15px line under the submit button, then a "Prefer to talk?" line with an underlined call link.
- **Done state:** the sub-line and form disappear; in their place a "Your text is ready" heading (28px), a short we-voice line, the message preview (Paper box, 16px round, pre-wrapped 16px Ink text), a primary "Open messages again" button, a line "Copy message" button whose label briefly confirms, a Soft Slate note for computer users, and an "Edit my details" link button. The card scrolls into view and the done block takes focus.

### Embed Mode
With `?embed=1` the page shows only the booking card: header, hero, claims, how it works, close, footer and floating circle are hidden; the page ground goes transparent; the card sits in a max 536px column with 8px side padding and the tighter embedded lift. The class is set before first paint so the full page never flashes inside the iframe. The card posts its height to the parent on every resize so the iframe never scrolls internally, posts a "done" message on submit, and its call and SMS links open in the top window. No motion runs in embed mode.

### Claims List
Three rows on paper, each a 40px Gold Ink line icon beside a Cal Sans title, separated by Hairline rules. On desktop the list sits sticky beside the card.

### Steps
Numbered list on the deep band: a 48px Bulb Gold circle with an Ink Cal Sans numeral, a Cal Sans title in On Dark, and a system-sans explanation in On Dark Soft. Stacks on phones, three across from 1024px.

### Floating Text Circle
A single 60px Bulb Gold circle with an Ink chat icon, fixed 16px from the bottom-right safe-area corner. It slides up (0.35s) once the hero has scrolled away and slides down while the booking card is on screen; it is never a bottom bar. Removed in embed mode and when IntersectionObserver is unavailable.

### Motion
- **Hero H1 bounce-in:** on load, each letter slides in from 50px right with a slight overshoot (1s, `cubic-bezier(.34,1.56,.64,1)`), 20ms apart; words never break mid-word. When the last letter lands, the plain heading is restored so kerning and selection return. The split is done by script, so without JS, in embed mode, or under reduced motion the heading is plain text from the start.
- **Fade-up:** elements that start below the first screen rise 12px and fade in (0.4s ease-out) as they enter. Everything is visible at rest; nothing already on the first screen ever hides.
- **Reduced motion:** smooth scrolling, the fade-up, the H1 split, the float slide and button transitions are all off.

**The Visible At Rest Rule.** No content depends on motion or script to appear. Animation may only add an entrance to something that is already readable without it.

## Do's and Don'ts

### Do:
- **Do** keep Bulb Gold as a fill with Ink on it, and switch to Gold Ink for any gold text or icon on paper or white.
- **Do** use Logo Blue for hover and focus outlines on light grounds and Bulb Gold for focus on navy bands.
- **Do** show selection as solid Ink with white text, in tiles and chips alike.
- **Do** set every heading, label, button and phone number in Cal Sans at weight 400.
- **Do** give every tap target at least 44px, buttons 56px, fields 52px, chips 48px.
- **Do** keep the diagonal texture on navy grounds only, at its faint 3.5% white.
- **Do** gate hover styles behind a real pointer so taps never leave them stuck on.
- **Do** keep the booking card self-contained so it renders identically on the page and in embed mode.

### Don't:
- **Don't** use gold as text on paper or white, or as a focus ring on light grounds.
- **Don't** bold Cal Sans or fall back to a condensed caps display face.
- **Don't** put shadows on buttons, tiles or fields, and don't use hard offset shadows anywhere.
- **Don't** add a sticky bottom bar; the single floating circle is the only fixed element.
- **Don't** hide content behind motion or script; reduced motion and no-JS must show the finished page.
- **Don't** add eyebrow labels above headings on new surfaces; the three label pills in the current build are carried, not a pattern to extend.
- **Don't** bring back the retired festive world: light-string canvases, red buttons, seasonal mascots.
