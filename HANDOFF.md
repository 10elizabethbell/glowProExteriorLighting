# Glow Pro Exterior Lighting — handoff at ~60% (calm-style revamp)

**Live:** https://10elizabethbell.github.io/glowProExteriorLighting/ (card only: `?embed=1`) · **Repo:** https://github.com/10elizabethbell/glowProExteriorLighting (public) · **Built:** 2026-10-08 from Muse brief (Muse run 2026-10-08) · **Revamped:** 2026-10-19 to the calm band style

## Revamp, 2026-10-19: what changed
Ellie made the calm band style (from lpmr.co.uk, `calm-photo-style.md`) the house default. The business hasn't been contacted yet, so the page was rebuilt from scratch on DPG's `index.html`. The old light-string world is still in git history (`10c3dfc`).
- **Removed:** every canvas and animation from the old build:
  - the swinging C9 light strings on the roof, the card and the footer
  - the bulbs that lit up as the form filled, and the chase on submit
  - the wreath, Santa's sleigh, the holly and the snowy yard of trees and presents
  - the Anton font, the red buttons and the dark card
  - the urgency line ("Holiday slots fill fast — book early") and its `&urgency=off` switch: that line isn't in the current brief, so it read as an invented claim
- **Look:** paper header and paper booking band; a night-navy hero; a deep navy "how it works" band with the faint line texture; a navy close; a deep footer.
  - **Accent:** one warm-white bulb gold (#ffc24a), used only as a fill with navy text on it. Where gold has to be text on light, it uses the darker #8a5a00.
  - **Form outlines:** the logo's blue (#0b7fd1) on hover and focus, so they stand out from the gold buttons.
  - **Type and shapes:** Cal Sans headings, 24px cards and pill buttons.
- **Header:** their real logo (the black-line transparent PNG from glowpronj.com) on the left, the tap-to-call number top right.
- **Hero:** eyebrow pill "Holiday & year-round lighting".
  - **H1:** "Your home, lit up in Ocean & Monmouth." It bounces in letter by letter.
  - **Promise:** their own line, "We handle the ladders, the lights, and the details…".
  - **Buttons:** Book a free consultation (gold, scrolls to the card) and Text us (outlined, `sms:`).
  - **Photo:** their work-01 night photo, cropped to 1024x520, in a 24px card. It sits under the copy on phones and beside it on desktop.
- **Booking card** (still the deliverable; still the only thing `?embed=1` shows):
  - **Fields:** an eyebrow "Free, no obligation estimate", 4 service tiles, 4 optional add-on chips, name, phone, the address of the property, and a preferred week.
  - **Errors and submit:** inline errors in plain sentences, then "Text my request".
  - **Done state:** the message written out, "Open messages again", "Copy message" and "Edit my details". There's also a quiet "Prefer to talk? Call (609) 222-8146" link, because whether that number takes texts is unknown.
  - **Embed:** the iframe height now shrinks again after submit.
- **Beside the card** (desktop) or **under it** (phone): "You enjoy the glow. We do the rest." with three claims from their own site: design, installation, maintenance and removal; commercial-grade weather-resistant LEDs; fully licensed and insured.
- **How it works** (for the owner): three steps plus the embed snippet with a Copy button. The snippet's default height is now 1240px, and the postMessage resizes it.
- **Close:** name, "Fully licensed and insured.", the 20 towns as plain text, and a big tap-to-call number. **Footer:** name, area, phone and the email (the only email on the page).
- **Floating text circle** (`CONFIG.FLOAT`): hidden on the hero, shown below it, hidden while the booking card is on screen, and off in embed mode.
- **Motion:** the H1 bounce-in and one 12px fade-up (`.rise`), nothing else. Under reduced motion or with JS off, everything shows at once (checked in Chromium and WebKit).
- **Phones held sideways** (≤500px tall) get a compact header and a two-column hero, so both buttons fit on the first screen.
- **New `og.png`:** 1200x630, taken from the new hero. The favicon and apple-touch-icon are unchanged: both are the logo's roofline-and-bulbs mark.
- **Docs:** `PRODUCT.md` updated; `DESIGN.md` rewritten from the built page.

## Assumptions I made
- **Gold accent, not their red.** The calm style wants one warm accent used as a fill with navy text on it. Navy on their red #CC0000 is about 3.6:1, which fails, so I used the warm-white glow of their C9 bulbs. Their red, white and blue stay in the logo and favicon.
- **Navy, not their black,** because of the house rule against black grounds.
- **Hero photo:** the calm style asks for "the best wide photo under a navy overlay". work-01 is only 1024px wide, so a full-bleed hero would blur on desktop. It sits in a card next to the copy instead, so no white text sits on the photo and no pixel sampling is needed.
- **Audience not treated as 40+.** The brief doesn't flag it. Ocean County does have many retirement communities (Manchester, Berkeley). If Ellie sees them as 40+, the fix is two lines: remove the bounce-in and fade-up blocks, and raise body text to 18px.
- **Copy I wrote:**
  - "Your home, lit up in Ocean & Monmouth."
  - "You enjoy the glow. We do the rest.", adapted from their "so you can simply enjoy the glow"
  - "We'll design it around your home and look after it like it's our own."
  - "we'll be in touch to set up your free consultation", from their own "we will schedule a free consultation"
  - None of these add facts.
- **Service tiles** use short names, but the full wording from their site goes into the text message. "We" voice, as their site uses.

## Placeholders and gaps
- Only work-01 is on the page. work-02 has an SUV in frame and work-03 has two people in frame, so both are still unused.
- **No Facebook link.** The brief found no business page, only a group post, so there's nothing to link under the photo or in the footer.
- **Three real testimonials** from glowpronj.com aren't on the page: Sarah M. (Toms River), Mike D. (Manasquan) and Lauren P. (Freehold). The widget scope kept them off.
- No hours, owner name, prices or Google rating (none in the brief).
- **Public repo history:** the first two commits contain `brief.md` (Muse's prospecting notes) and `TRIGGER.md`. Both have been untracked since 2026-10-08 but are still in history. The repo was made public on Ellie's call on 2026-10-08. If those notes shouldn't be public, the history needs rewriting.

## Questions for the owner
- **Does (609) 222-8146 take texts?** If it doesn't, every text request is lost: change `CONFIG.SMS_TO`. The call link stays on the card either way.
- Do you have a Facebook page? It would go under the work photo and in the footer.
- Can we use photos without people or cars in them, and before/afters?
- Which service matters most this season (it sets the tile order)? Should add-ons stay, or should the form be shorter?
- Is there a service-area cutoff? Any address goes through today.
- Who manages your WordPress and hosting, so we can upload the file?

## Outreach flags (brief + scan of glowpronj.com, 2026-10-08)
- Their site still shows the placeholder **"Call 555 123 4567"** in the footer, and in a second header menu copy (probably the mobile one).
- The homepage still advertises the expired "Reserve your spot before September 30…" discount.
- One "Why choose" list repeats "Complete all inclusive package…" four times.

## Ideas not built (yours to pick)
- **Impeccable findings kept on purpose (Ellie's calm-style choices):** the craft floor bans eyebrow pills, and the detector flags the diagonal band texture ("repeating-stripes-gradient"). Both stay. The bounce-in, the floating circle and Cal Sans also stay.
- **Finish reviewer's "phone number twice on the last phone screen"** (the close's big number plus the footer line): not applied. The calm-style footer carries the phone, and the finishing rules allow the close and footer to repeat it.
- **The three testimonials:** they could go under the claims on desktop, which would also fill the empty left column there, or one could sit under the card's submit button.
- **Opt-in signature motion (runner-up worlds from their trade):**
  1. A permanent-LED eave track whose pixels chase colour under your finger. This one fits best, since it sells their smart-LED line.
  2. The old swinging C9 roofline, which is in git history.
  3. A path of landscape lights that switch on as you scroll.
  4. Tree-wrap spirals.
- Atkinson Hyperlegible for body text, if the audience turns out older.
- A "Send a photo of your house" nudge in the done state, since their estimate is photo-based.
- Time-window chips (morning, afternoon, evening) next to the week.
- A white card already suits their dark site, but a version tinted to their section colour could be offered.

## Not verified
- Real-device touch, and the SMS handoff opening Messages with the body intact, especially iOS Safari inside an iframe.
- The iframe height postMessage on a real WordPress/Elementor page.
- Date input styling on iOS (it uses the native picker; the "Tap to pick a day" placeholder only shows on iOS).
- Cal Sans loading inside Facebook's in-app browser. If it's blocked, the page falls back to Avenir Next / Segoe UI.
