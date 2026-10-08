# Glow Pro Exterior Lighting — handoff at ~60%

**Live file:** index.html · **Repo:** https://github.com/10elizabethbell/glowProExteriorLighting (private) · **Built:** 2026-10-08 from Muse brief (brief.md, dropped 2026-10-08)

## What's built
- **Widget, not a site.** Per the brief, this is an embeddable "Book your free consultation" card for glowpronj.com, shown on a short demo page. `index.html?embed=1` renders only the card (transparent background), and `&urgency=off` hides the holiday line.
- **World:** a Jersey Shore roofline at night strung with C9 bulbs in the logo's red, warm white and blue; navy winter sky with light snow; Anton headings (their site's display face, inlined as a 5.6KB subset).
- **Signature motion:** verlet-rope light strings with layered gust wind. Bulbs swing on their sockets, and the pointer or a finger shoves the wire and brightens nearby bulbs. One string runs along the hero's roofline (the roof fill becomes the next section's background, so the roofline is the divider); a second string hangs across the top of the card.
- **The authored moment:** the card's 10 bulbs light two at a time as each of the 5 required answers becomes valid. On submit, a chase runs along both strings.
- **Booking:** service picker (4), optional add-ons (4), name, phone, address, preferred week (date input, reported as "week of Mon, Nov 9"). Inline plain-language errors. Submit opens `sms:+16092228146?&body=…`; a done state shows the message with "Open messages again", "Copy message" and "Edit my details". A "Prefer to talk?" button calls `tel:+16092228146`. In embed mode the links target `_top` so they leave the iframe.
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
- No photos of their work are used. Their gallery exists on glowpronj.com, but the widget didn't need them and I didn't pull them.
- No hours, no owner name, no reviews, no prices (none in the brief, so none on the page).
- The urgency line is a plain toggle with no date. Its wording comes from the brief.

## Questions for the owner
- Does (609) 222-8146 take texts? The whole flow depends on it.
- Would they rather get requests by email (Info@glowpronj.com) as well, or instead? A mailto fallback is easy to add.
- Which services matter most this season (picker order)? Should add-ons stay, or is a shorter form better?
- Is there a service-area cutoff? An address outside Ocean or Monmouth County currently goes through without a check.
- Who manages their WordPress and hosting (to place the file)?

## Outreach flags (from the brief + my scan of glowpronj.com, 2026-10-08)
- Their site still shows the placeholder **"Call 555 123 4567"**: the brief says the footer, and my scan also found it in a second copy of the header menu (likely the mobile one). The other header copy shows the real 609 number.
- The homepage still advertises **"Reserve your spot before September 30 for 10% off … plus an extra $200 off"**, which is now expired. The banner "Get 10% Off Your Christmas Light Installation!" is still up.
- One "Why choose" list repeats "Complete all inclusive package…" four times.

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
