# AI Web Design Lab

Design experiments from Kiminou's AI website design research: can AI build websites with actual taste? Each site is a single self-contained HTML file. Open any `index.html` in a browser, no build step.

All shops, people, addresses, and phone numbers are fictional concept mocks. Photography was sourced via Google image search; local mirrors live in `assets/` in case hotlinks die.

## The sites

| Folder | Concept | Video inspiration |
|---|---|---|
| `crown-cuts-v1/` | Crown Cuts, restrained editorial barbershop | Baseline build |
| `crown-cuts-v2/` | Crown Cuts with a real cut-builder, price board, sign-painter type | Grok + Gemini critique of v1 |
| `crown-cuts-after-dark/` | Cinematic scroll-scrubbed night shop. Scrolling "turns the lights on": pinned hero, film grain, floating dust, neon glow, marquee, live open/closed clock | Cinematic AI websites video (scroll-scrubbed heroes, palette-sampled accents) |
| `first-chair/` | Scrolling IS the appointment: 01 Walk In, 02 Consult, 03 The Cut, 04 Detail, 05 Finish. Fixed progress rail, sticky chapters, parallax | Scrollcraft video (scroll-correlated journeys, emotional direction) |
| `velvet-blade/` | Flagship $95 service as a product launch: massive type, gold accents, sticky ritual sections, spec grid, interactive add-on builder | Apple-style page rebuild video (visualize first, reference-quality polish) |

## Taste rules applied

- High tech, fun, animated, floaty. Minimalism is not the goal; creative confidence is.
- Real barbershop lingo researched from real shop sites: skin fade, taper, line-up/shape-up, guard numbers, hot towel shave, straight razor, foil shaver, blocked/rounded/tapered necklines, "walk-ins welcome", "book the chair".
- No em dashes anywhere in site copy.
- No AI slop markers: no purple/blue gradients, no "delve", no lorem ipsum, no generic testimonials.

## Process

Build it, screenshot it, critique it with Grok + Gemini (+ ChatGPT), revise, ship. The critique notes live in the project workspace, not in this repo.

## Assets

`assets/` holds local copies of every photo used across the three new sites (17 images, each unique to its site). The HTML files reference these local files via `../assets/`, so each page works offline the moment you open it. `assets/IMAGE_SOURCES.md` records the original source URL of every image; licenses are unverified, these are concept mocks only.
