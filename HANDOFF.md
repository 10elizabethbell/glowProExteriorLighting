# Glow Pro Exterior Lighting — handoff at ~60%

**Live:** https://10elizabethbell.github.io/glowProExteriorLighting/ (widget only: `?embed=1`) · **Repo:** https://github.com/10elizabethbell/glowProExteriorLighting (public) · **Built:** 2026-10-08 from Muse brief (brief.md, Muse run 2026-10-08; the brief was revised mid-build and the build follows the revision)

## What's built
- **Widget, not a site.** Per the brief, this is an embeddable "Book your free consultation" card for glowpronj.com, shown on a short demo page. `index.html?embed=1` renders only the card (transparent background), and `&urgency=off` hides the holiday line.
- **Proof:** work-01 from glowpronj.com (a two-story roofline install at night) sits under the hero copy. Its black sky is masked so it dissolves into the page sky. On phones it comes after the card.
- **World:** a Jersey Shore roofline at night strung with C9 bulbs in the logo's red, warm white and blue; navy winter sky with light snow; Anton headings (their site's display face, inlined as a 5.6KB subset).
- **Signature motion:** verlet-rope light strings with layered gust wind. Bulbs swing on their sockets, and the pointer or a finger shoves the wire and brightens nearby bulbs. Three strings, all in one shared loop:
  - the hero roofline. On desktop it sits at the bottom of the first screen, with peaks sized to clear the copy. On phones it sits just above the card, so the card stands on the house.
  - the top of the card.
  - the how→footer seam, where the house color follows the swaying wire.
- **The authored moment:** the card's 10 bulbs light two at a time as each of the 5 required answers becomes valid. On submit, a chase runs along both strings.
- **Booking:** service picker (4), optional add-ons (4), name, phone, address, preferred week (date input, reported as "week of Mon, Nov 9"). Inline plain-language errors. Submit opens `sms:+16092228146?&body=…`; a done state shows the message with "Open messages again", "Copy message" and "Edit my details". A "Prefer to talk?" button calls `tel:+16092228146`, with a plain email link (Info@glowpronj.com) under it. The done state also offers a pre-filled email of the same message. In embed mode the links target `_top` so they leave the iframe.
- **Embed:** instructions are commented at the top of the file, and the snippet is shown on the demo page with a Copy button. The iframe reports its height to the parent with postMessage, so it fits without an inner scrollbar.
- One shared rAF loop. Rendering pauses when the strings are off screen; reduced motion gets one still frame. No tracking, no external requests.

## Assumptions I made
- **Navy ground, not their black.** glowpronj.com uses black/near-black with #CC0000 red. House rule: no black grounds, so I used deep night navy. Their red sits on the primary button as #e0262b, brightened slightly so white text passes 4.5:1 on navy.
- **Logo** taken from their site (the white transparent-background PNG), converted to a 400px WebP.
- **Service names** are shortened for the picker ("Holiday lights / Residential install"). The full wording from their site goes into the text message.
- **"Licensed & insured"** and "commercial-grade LEDs" plus "design, install, maintenance & takedown" are copied from their homepage claims. Nothing new was invented.
- **Card sub-copy** promises a follow-up for a "photo-based estimate and custom design". That's their own step 1 wording, but the follow-up promise is mine.
- **Hosting route:** WordPress's Media Library blocks .html uploads, so the instructions say to upload with the host's File Manager or SFTP to `/booking-widget/index.html`. This needs confirming against their host.
- The SMS body uses the `?&body=` form, which iOS and Android both accept.

## Placeholders and gaps
- Only work-01 is used. work-02 (pathway light) has an SUV in the background, and work-03 (brick home) has two people silhouetted. Both are unused until cropped or cleared.
- Three real testimonials on their site (Sarah M. of Toms River, Mike D. of Manasquan, Lauren P. of Freehold) are **not** on the page. One could go under the card's submit button if Ellie wants social proof inside the widget.
- The Muse brief says "logo: none found". I took it from glowpronj.com's schema markup (the transparent white PNG).
- No hours, no owner name, no reviews, no prices (none in the brief, so none on the page).
- The urgency line is a plain toggle with no date. Its wording comes from the brief.

## Questions for the owner
- **Does (609) 222-8146 take texts?** The brief says unknown. If it's a landline, every SMS request is lost: change `SMS_TO` in the widget script. Call and email fallbacks are on the card either way.
- Would they rather get requests by email (Info@glowpronj.com) as well, or instead? A mailto fallback is easy to add.
- Which services matter most this season (picker order)? Should add-ons stay, or is a shorter form better?
- Is there a service-area cutoff? An address outside Ocean or Monmouth County currently goes through without a check.
- Who manages their WordPress and hosting (to place the file)?

## Outreach flags (from the brief + my scan of glowpronj.com, 2026-10-08)
- Their site still shows the placeholder **"Call 555 123 4567"**: the brief says the footer, and my scan also found it in a second copy of the header menu (likely the mobile one). The other header copy shows the real 609 number.
- The homepage still advertises **"Reserve your spot before September 30 for 10% off … plus an extra $200 off"**, which is now expired. The banner "Get 10% Off Your Christmas Light Installation!" is still up.
- One "Why choose" list repeats "Complete all inclusive package…" four times.

## Phone-first pass (2026-10-08, Ellie's rule relayed from the blessedMobileDetailing session)
- CSS rewritten phone-first: base styles target 360–430px, then `min-width: 521px` and `min-width: 961px` layers.
- First phone screen: logo, a call pill, the headline, the pitch (what and where) and the lit roofline. On short phones a sticky dock adds **Book free consultation** (jumps to the card) and a 56px call button. The dock hides while the picker or the card's buttons are on screen, while someone is typing, and in embed mode.
- Sizes: buttons 56px tall, chips and links 44px+, inputs 52px. Text is 16px for body and inputs, never under 14px. No sideways scroll at 360px (checked programmatically).
- The photo's data loads after the scripts, so the card and contact buttons work first. Copy buttons report when the clipboard is blocked (Facebook's in-app browser) and point to press-and-hold instead.
- Repo visibility: **public** since 2026-10-08 (Ellie's call), with GitHub Pages serving main / root. `brief.md` and Muse's `TRIGGER.md` were committed in the first two commits. Both are now untracked and gitignored but still in history. Raw `src-assets/` was never committed.

## Festive pass (2026-10-08, Ellie: "more festivity around the rest of the page")
- **Wreath** hangs from the left gable of the hero roof on a red ribbon. It has mini bulbs, a bow and berries, and it swings in the wind and when the pointer or a finger shoves it.
- **Santa's sleigh** with four reindeer (Rudolph's nose glows) crosses the hero sky every ~25s and leaves gold sparkle dust. Go near him and he hops and bursts sparkles. On desktop he climbs out over the top right; on phones he crosses the gap above the roof. He is off under reduced motion.
- **Snowy yard** at the bottom of the footer: lit trees (7 on desktop, 4 on phones) with spiral strands and stars, and wrapped presents in the logo colors. Trees sway away from the pointer and their bulbs brighten; tapping a tree runs a light chase up to its star. Presents hop when nudged or tapped. Snow falls. Submitting the form chases every tree as part of the cheer.
- **Holly** sprig on the card's top-right corner (it rustles, and jiggles each time a new pair of bulbs lights) and after the "how" heading. On the card it is a holiday touch: `&urgency=off` hides it along with the urgency line.
- All of it runs in the same animation loop and pauses off screen. No images were added (everything is drawn in code), so the file grew by about 25KB.

## Review round (finish reviewer, 2026-10-08)
- Applied:
  - roofline in the first viewport
  - done state scrolls into view (and tells the parent page in embed mode)
  - no opaque iframe canvas in embed
  - texts-unknown copy and setup note
  - iOS empty-date placeholder
  - matching button outlines
  - footer light-string divider
- Rejected: rewording the urgency line. The brief specifies "Holiday slots fill fast — book early" verbatim, and it stays a toggle with no deadline.

## Ideas not built (yours to pick)
- **Runner-up world:** a permanent-LED eave track whose pixels chase color under the pointer, with a color swatch picker in the card (sells their smart-LED line).
- A quick-pick row of time windows (morning/afternoon/evening) next to the week.
- A "Send a photo of your house" nudge in the done state, since their estimate is photo-based (MMS can't be pre-attached, but the copy can ask for it).
- A sticky "Book" pill on phones for the demo page.
- Bulbs that snap off the string and fall into the snow if flicked hard (Ellie's "break free" pattern).
- A light-mode card variant if their page section behind the iframe is white. The navy card currently reads as a deliberate night panel.

## Not verified
- Real-device touch on iOS/Android, and the SMS handoff opening Messages with the body intact (iOS Safari inside an iframe especially).
- Iframe height postMessage on a real WordPress/Elementor page.
- Frame rate on older phones. The hero rope is about 100 nodes with 8 constraint passes.
- Date-input styling on iOS Safari (it uses the native picker).
- `pitch-site/scripts/shoot.sh` didn't produce phone.png on this run. I captured the phone screenshot manually with the same iframe method.
