# Product: Glow Pro Exterior Lighting — consultation booking widget

## Platform
web · stack: static single-file HTML/CSS/JS (no backend, no frameworks, no tracking)

## What it is
An embeddable "Book your free consultation" widget for glowpronj.com (WordPress/Elementor), shipped as one self-contained HTML file that also works opened directly. It is an unsolicited free-fix pitch: the owner should see a working booking tool for their own business, ready to paste in.

## Users
- **Owner (first viewer):** Glow Pro Exterior Lighting LLC. Today their site only offers "fill out our contact form or call". They need to see the widget in their own brand, working, within one screen.
- **Homeowners and businesses in Ocean and Monmouth County, NJ** (Toms River, Brick, Point Pleasant, Manchester, Lacey, Berkeley, Jackson, Barnegat, Beachwood, Seaside Heights, Freehold, Middletown, Manalapan, Marlboro, Holmdel, Wall, Manasquan, Long Branch, Red Bank, Colts Neck — per glowpronj.com) who want holiday or year-round exterior lighting and are mostly on phones.

## Purpose
Turn a visit into a consultation request in under a minute: pick a service, give name, phone, address, preferred week, and hand off a pre-filled text message to (609) 222-8146. Tap-to-call as fallback.

## Positioning
Their own site's words: "From holiday displays to permanent architectural lighting, Glow Pro handles the design, installation, maintenance, and removal so you can simply enjoy the glow." First step in their process: "Free Consultation and Custom Design … a photo based estimate and a custom layout."

## Capabilities and constraints
- Services (their wording, shortened for the picker): residential holiday/Christmas light installation; year-round exterior and landscape lighting; permanent LED / smart color-changing systems; commercial exterior and holiday lighting. Add-ons: tree wrapping, pathway, security/motion, smart timers.
- Whether (609) 222-8146 accepts texts is unknown (brief, 2026-10-08), so every SMS path has a call and email (Info@glowpronj.com) fallback.
- Output is an `sms:` link (plus a pre-filled mailto fallback). No server, no storage, no analytics.
- Must embed in WordPress (iframe or Custom HTML block) without leaking styles into their theme.
- Urgency line ("Holiday slots fill fast — book early") is a toggle, never a fake deadline.

## Brand commitments
- Logo: white roofline-of-bulbs mark with red, white and blue bulbs, "Glow Pro / Exterior Lighting LLC" (from glowpronj.com).
- Site colors observed: red #CC0000, white, near-black grounds; display font Anton. (Page ground here: deep night navy, not black — house rule.)
- Licensed and insured (per their site; not repeated as a new claim beyond that).

## Evidence on hand
- Phone (609) 222-8146, email Info@glowpronj.com, service area towns, services list, 3-step process copy: from brief and glowpronj.com.
- Photos: work-01 from glowpronj.com (night roofline install, clean) is used; work-02 (vehicle in frame) and work-03 (two people in frame) are not.
- Three testimonials exist on their own site (Sarah M., Mike D., Lauren P.); not used on the page yet.
- No prices used. Their site's early-booking discount ended September 30 (inferred stale as of 2026-10-08); not used.

## Principles
1. Their business, done better, inside one screen.
2. Every fact traceable to the brief or their site.
3. Short form, big targets, works with one thumb.
4. Light is the material: the motion is their bulbs.
