# KISSA NOIR — Art-Direction Reset Log

Crew brief: `~/workspace/ai-webdesign-study/AI_CREW_CRITIQUE_R1.md` (ChatGPT High Intelligence + Grok, 2026-10-05).
Mission: stop looking like a sophisticated website *about* a kissa; feel like entering one.
LOCAL ONLY. No commit, no push, no deploy.

## Design thesis
"The shop's accumulated ephemera." Dark wood, lamplight, paper (obi strips, request slips, stamped menus), amplifier faceplates. Type that whispers: Cormorant Garamond (real italics) + JetBrains Mono (kept per crew). Inter leaves. Anton leaves. No shouting, no outlines, sentence case.

## Pass plan (10 minimum)
1. Foundation: type system, palette, @property --accent, base CSS.
2. Hero + loader + HUD reskin (whisper hero, lamp glow, room-tone toggle).
3. Record instrument: crate jackets with spines, platter + tonearm, SIDE A scroll progress, accent switching.
4. Dividers: obi strips (paper) + groove divider (scroll-driven stylus). Kill marquee + scrubband.
5. Room: amp-faceplate spec grid + VU meter; video consolidation (2 pieces), unified grain/lamp grade, reduced-motion stills.
6. Code (paper menu card), visit, finale, footer.
7. Sound: opt-in generated room tone (Web Audio, no files). JS wiring.
8. Reduced-motion + keyboard + aria audit.
9. Copy audit (no em dashes, no invented facts), node --check, screenshots 1440/390.
10. Final polish.

## Crew directives checklist
- [x] Anton replaced, display sizes roughly halved, type whispers
- [x] Inter removed from body copy (mono or real-italic text face)
- [x] Visual system from physical objects (obi, spines, slips, faceplates, speaker cloth, dark wood, stamped menus)
- [x] NOLA x Japanese listening culture collision, no random Japanese characters
- [x] Record selector = instrument (crate-digging, vinyl leaves shelf, tonearm cues, SIDE A scroll progress, accent shift)
- [x] Marquees killed or replaced with jazz-native metaphors
- [x] Video consolidated 4 -> 2, matched grain/lamp grade, poster frames, pause offscreen, stills for reduced motion
- [x] Opt-in sound (generated room tone; no copyrighted autoplay)
- [x] Motion structural (deleting it makes page worse, not cleaner)
- [x] House rules, gear list, door note, mono HUD kept
- [x] CONCEPT MOCK disclosure kept (finale + footer, quiet)
- [x] No em dashes, no invented proof, keyboard navigable, RM honored

## Completed passes (2026-10-05, all verified in Playwright)
P1 Foundation rewrite (whisper type, physical-object system). P2 Record instrument (crate jackets, peek disc, platter spin, tonearm cue, SIDE A progress, per-sleeve accent shift, aria-live). P3 Marquee kill (obi strips + groove divider with scroll-driven needle dot). P4 Video 4→2 consolidation, unified grade, pause offscreen. P5 Opt-in room tone (Web Audio, no autoplay). P6 Overflow hunt: fixed 39px grid blowout at 1440 (min-width:0) and 3px plinth overflow at 1024 (fluid width); clean at 1440/1280/1024/768/390. P7 Label clipping fixes (platter label, 33⅓ RPM). P8 Reduced-motion + keyboard + tone QA, zero errors. P9 Fonts self-hosted (8 woff2 in media/fonts/, 9 faces verified loading). P10 Merged polish refinements found in file (lamp amber #E8A33D, @property --accent, second obi, 600 weights); restored section ids. P11 Faceplate screw fix (transparent tiles). P12 Final audit: 0 em dashes, 0 Anton, 0 marquee, node --check clean, zero page errors everywhere.

Kept: house rules, gear list (SP-10/McIntosh/JBL 4343/three sweet seats), Decatur door note, mono HUD, CONCEPT MOCK disclosure, fictional framing.
Screenshots: qa-shots/reset/ (1440 + 390, incl. reduced-motion).
Status: DONE local. index.html modified, uncommitted. Nothing pushed or deployed. Awaiting Kiminou's review.
Sandbox-only notes: Pexels video + Google Fonts blocked in headless browser (ERR_EMPTY_RESPONSE; curl fine); fonts now self-hosted. Real-device iPhone check still needs Kiminou.

## P13 — Gemini adjudication: video killed entirely (2026-10-05 ~05:15 CDT)
Gemini (third crew voice) pushed past the 4→2 consolidation: kill video ENTIRELY, replace with static ambient texture photography. Verdict after review: **Gemini is right — cut to stills.**
Reasoning: (1) The "one continuous room-feel" test fails — a vinyl extreme macro and a live band performance never read as one place; the grade unified color, not place. The montage problem was reduced, not solved. (2) Conceptual mismatch: a kissa plays *recorded* music — there is no live band at a listening bar, yet band footage sat behind "Built for the needle," a section about the amplifier chain. (3) The page's motion identity is already carried by structural/mechanical systems (tonearm cue, platter spin, VU needle, SIDE A progress, groove stylus) — the background videos were decorative atmosphere, and the crew's own rule says the coolest behavior must come from the business itself. (4) Reliability: video backgrounds are the flakiest asset on the page.
Sourced 2 high-res Pexels stills, downloaded to media/ (self-hosted): hero-needle.jpg (1920px, Philips 422 cartridge on vinyl, warm gold — Pexels 3916058, Matthias Groeneveld) and room-tubes.jpg (1600px, illuminated vintage receiver dial + knobs + wood — Pexels 26100254, Jakub Zerdzicki). Both graded under the existing lamp glow + grain + grade overlays; hero grade top deepened slightly for kicker legibility. Removed both <video> elements, the play/pause IO, heroVid refs; parallax retargeted to the stills (overscan preserved via inset:-10%). Deleted the now-unused 2.9MB media/club-1080p.mp4. Footer credit updated: "CONCEPT MOCK · PHOTOS VIA PEXELS". Preload added for hero still. Verified: zero page errors, no failed requests, no overflow, instrument + accent shift + tone toggle all still working. Screenshots: qa-shots/reset/s-hero2.png, s-room.png, s-m-hero.png.

## P14 — ChatGPT round-2: the room itself (2026-10-05 ~07:00 CDT)
ChatGPT R2: "I know the taste of the room now, but I still don't know the room." Macro hi-fi imagery could be a cartridge company. Prescription: ONE irreplaceable spatial image as the visual anchor.
Executed: generated room-wide.jpg (AI-generated concept image, disclosed as concept mock) — wide, low-light, seated-eye-level: JBL horns in corners, turntable + record station on the wood bar, vinyl shelved behind, warm table lamps, fourteen seats in dark wood. Swapped into the hero (.hero-still + preload); the room is now the visual anchor. Verified: 1440 + 390 screenshots, no overflow, zero page errors. Next: map copy geography to the room (three sweet seats = actual chairs, Decatur door note at the door) in a future pass.

## P15 — Grok round-2 items (2026-10-05 ~07:30 CDT)
Grok R2 (on pre-P14 shots): italic orange accent wearing out; LISTEN as far-edge scrollbar; mobile kicker breaking; cluster LISTEN with NOW SPINNING.
Executed: orange italic now ONLY on "Noir" in the hero title (removed from loader + "Built for the needle" headline; body-copy cream italics kept as emphasis). Deleted the far-right scroll-hint; LISTEN is now a cue inside the tone-row cluster next to ROOM TONE + NOW SPINNING. Mobile kicker tightened (9px/.22em) — "JAZZ LISTENING BAR · NEW ORLEANS, LA" holds one line at 390px. Verified: desktop + mobile screenshots, zero page errors.

## P16 — Gemini round-2: contrast (2026-10-05 ~08:00 CDT)
Gemini R2: body copy over dark vinyl grooves failed legibility ("whispering UI crossed into illegible").
Executed: hero body text lifted from muted grey to cream (#F2EAD8); mobile gets a non-layout scrim (::before gradient behind hero-copy, bleeds to edges via negative inset, no layout shift). First attempt with margin/padding scrim broke mobile layout (kicker clipped) — reverted to pseudo-element. Verified: 390 + 1440 screenshots, text legible, zero page errors.
