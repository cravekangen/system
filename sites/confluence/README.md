# Confluence — Water Wellness (Occoquan, VA)

A premium, single-file marketing site for a fictional riverside water-wellness
house in historic Occoquan, Virginia. Built with the `ui-ux-pro-max` design
skill for grounding, then art-directed away from its templated defaults.

## Preview

Open `index.html` in any browser — no build step, no dependencies.

```bash
open sites/confluence/index.html      # macOS
xdg-open sites/confluence/index.html  # Linux
```

## What's inside

- **Self-contained:** one HTML file. Only external request is Google Fonts
  (Fraunces + Inter), loaded with `display=swap` and preconnect.
- **No JS libraries:** animations are hand-built with CSS + a small
  `IntersectionObserver` (scroll reveals, count-up stats) and rAF — featherweight
  and smooth on any device.
- **Sections:** hero, ethos/name story, the waters (bento grid), the ritual
  (numbered sequence), membership pricing, the space (gallery), testimonials,
  journal, booking form, footer.

## Design decisions

- **Palette** — deep petrol/teal + misty aqua + warm brass on limestone mist,
  derived from *water* rather than the generic spa pink the database suggests.
- **Type** — Fraunces (optical soft-serif display) + Inter (body); two families
  only, for fast loads.
- **Name** — "Confluence" is a placeholder; Occoquan means roughly "at the end
  of the water," which the copy leans into.

## Accessibility & performance

- `prefers-reduced-motion` fully respected (animations disabled, content shown).
- Semantic HTML, skip link, visible focus rings, labelled form fields,
  `aria-live` form feedback, alt/aria on icons.
- Responsive at 375 / 768 / 1024 / 1440; no horizontal scroll; 48px+ touch
  targets; `min-h-dvh`-safe layout.

## Swap in real content

Placeholders to replace before launch: business name/logo, photography (the CSS
"water" panels in *The Space* and *Journal* are stand-ins for real images),
address, phone, hours, pricing, and testimonials. Wire the booking form's submit
handler to your real booking backend (currently a client-side demo).
