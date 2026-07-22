# Crave Kangen — Virginia's First Enagic® Showroom (Occoquan, VA)

A self-contained, single-page marketing site for **Crave Kangen**, a Kangen
Water® storefront in historic Occoquan — plus a *Private Water Class*
rabbit-hole page. Product-led and education-first: bring traffic via the free
weekly class, sell Enagic machines by educating, and pitch the marketing
software to distributor prospects.

## Files

- `index.html` — the single-page scroll site
- `private-class.html` — the Private Water Class sub-page (the "rabbit hole")

Open either in any browser — no build step, no dependencies (only external
request is Google Fonts).

## Section structure (as briefed)

Hero → Story → **Featured Menu** (6 sample waters, not the full list) → The
Water (science) → Filtration → **Free Water Class** + Private Class link → 
**Systems** (CTA-only, links out to the Enagic store — nothing embedded) → 
Build a Business + marketing software → Reviews → **Visit & Contact** (location,
hours, phone, email, map, and the reservation form all folded together) → footer.

Single-page, no multi-page nav — the one deliberate exception is
`private-class.html`, the deeper private-class page linked from the Free Class
section and footer.

## Real business details baked in

- **Address:** 206 Union Street, Unit 101, Occoquan, VA 22125
- **Phone:** (703) 565-4854 · **Hours:** Tue 10–6 · Wed–Sat 10–7 · Sun 10–5 (Mon closed)
- Rating shown as **4.7★** with a link straight to the Google listing.
- Systems CTA → `cravekangen.enagicweb.info`; opportunity → `cravekangen.enagicweb.net`.
- Socials linked: Instagram / Facebook / TikTok `@cravekangen`.

## PLACEHOLDERS — please confirm / replace before launch

- **Reviews:** Google/Yelp blocked automated scraping, so the three quotes use
  the *genuine sentiment* found in your listings but are attributed generically
  ("Verified guest review"). Replace with verbatim quotes + names, or leave the
  "Read every review on Google" button to do the work. Confirm the 4.7★ figure.
- **Free class time:** the site says "held weekly — see current time" rather than
  inventing a day/hour. Add the real recurring day & time.
- **Email:** `hello@cravekangen.com` is a guess — set your real address.
- **Marketing software:** described generically (capture/follow-up, funnels,
  analytics). Drop in its real name + link/pricing.
- **Machine line-up & links:** K8 / SD501 / JR IV / Anespa are described; verify
  the store URLs point where you want buyers to land.
- **Photography:** currently type/color-driven (no stock photos) to stay
  self-contained — add real showroom + water photos when ready.
- **Trademarks/compliance:** footer notes independent-distributor status + an
  FDA disclaimer. Adjust to your preferred wording.

## Accessibility & performance

`prefers-reduced-motion` respected; semantic HTML, skip link, focus rings,
labelled form fields with `aria-live` feedback; today's hours auto-highlight.
Responsive at 375 / 768 / 1024 / 1440; 48px+ touch targets; no JS libraries.
