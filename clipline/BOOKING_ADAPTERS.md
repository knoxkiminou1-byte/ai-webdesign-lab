# ClipLine Template 001 — Booking Provider Adapter Options
Prepared 2026-10-05. For Kiminou's choice before wiring a real provider into the template.
Rule: NO-PAID law. Only free tiers / free software considered.

## How the adapter works (all options)
Template 001 currently runs a demo 4-step flow (Service > Barber > Time > Details) with no backend.
Each adapter below replaces the demo's dead ends with a real booking path while keeping the
ClipLine look (gold/ink/smoke, Cormorant + JetBrains Mono, receipt confirmation) around it.

## Option A — Square Appointments (free plan)
- Cost: $0/mo (solo/small team, one location). Card processing 2.9% + 30c online only when paid online.
- Integration: embeddable "Book Now" widget on the site, or link to Square's free booking page.
- Adapter work: swap the 4-step demo panels for the Square embed inside a ClipLine-styled frame;
  keep the branded receipt screen, mapping Square's confirmation data into it.
- Pros: genuinely free, trusted brand, POS built in if the shop takes cards in chair.
- Cons: free plan is one location; combo-service booking and barber-preference tracking are thin.

## Option B — Fresha (free software)
- Cost: $0 software. Catch: ~20% commission on NEW clients who find the shop through Fresha's
  marketplace app, plus card fees per transaction. Direct website bookings avoid the commission.
- Integration: embeddable booking widget.
- Adapter work: same pattern as Square — embed in a ClipLine frame, map confirmation to receipt.
- Pros: free, polished client experience, big existing user base.
- Cons: the marketplace commission is the real price; worth it only if the shop wants discovery.

## Option C — Setmore (free plan)
- Cost: free tier available; simple.
- Integration: web embed / integrations.
- Adapter work: embed or deep link; lightest lift of the three.
- Pros: simplest, cheapest to wire.
- Cons: least barbershop-specific; fewer grooming-industry features.

## Option D — OpenSalon (self-hosted, open source)
- Cost: $0 forever. No per-user fees, no commissions, no vendor lock-in. Runs on own infra (SQLite).
- Integration: full control — the template's 4-step flow becomes the REAL flow, backed by OpenSalon.
- Adapter work: biggest lift. Deploy OpenSalon (or a slimmed fork) as the booking backend;
  wire the existing Service/Barber/Time/Details UI to its API. This is the "own it outright" play.
- Pros: zero ongoing cost, no vendor, the demo UI becomes production UI, we keep every review/client.
- Cons: needs hosting somewhere (free tiers exist); we own uptime and maintenance.

## Paid options (NOT recommended under standing law, listed for completeness)
- Booksy (~$30/mo), Vagaro (~$24-30/mo): barbershop-specific, no free plan. Skip.

## Recommendation
Default the template to **Option A (Square)** for the fastest credible "real booking" story at $0,
with the adapter interface designed so **Option D (OpenSalon)** can replace it later without
redesigning the front end. If Rashida's shop wants marketplace discovery, offer Option B as the
alternate and let her pick.

## Awaiting Kiminou
1. Which provider (A/B/C/D)?
2. Rashida's real shop facts still needed: shop name, address, hours, phone, price list.
   Nothing ships with real facts until she confirms them.
