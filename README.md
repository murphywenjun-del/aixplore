# AiXplore

AI-powered community participation app for newcomers and seniors 50+.

**Live prototypes:**
- [Senior App (phone view)](https://murphywenjun-del.github.io/aixplore/prototype/AiXplore_Senior_App_v3.html)
- [Workstation (staff dashboard)](https://murphywenjun-del.github.io/aixplore/prototype/AiXplore_Workstation_v2.html)

## What is AiXplore?

One loop: **Setup → Discover → Understand → Attend → Return** (repeats weekly)

- A pre-filled senior profile (set by their adult child)
- 15-25 verified community activities in the feed
- Simple rules for filtering & ranking; AI for explanation in the senior's language
- "Pulong" is a **computer helper**, honestly disclosed — not a real person
- Facts come only from the verified feed. If unknown → "I'll check with the organizer"

## Structure

```
index.html                    ← Landing page
prototype/
  AiXplore_Senior_App_v3.html ← Senior's phone (the main product)
  AiXplore_Workstation_v2.html← Staff/admin dashboard
docs/
  AiXplore_App_Logic.pdf     ← Product logic spec
  AiXplore_Sprint2_Script.md ← Pitch script
AiXplore.md                  ← Project bible (full strategy, 8 journeys, trust model)
```

## Design principles

- **Honest disclosure**: Pulong is a program, not a person. Never hides AI status.
- **No fabricated social bonds**: "Maria attended" not "Maria is your friend".
- **Dual trust anchor**: Child's name + Institution logo on every screen.
- **Zero-input onboarding**: No login, no password, no email. Child sets up in person.
- **Stop service**: One tap → daughter notified → data deleted in 24h.
- **App-first, multi-channel**: App is primary; WeChat/WhatsApp/SMS/Phone are optional Pulong channels.

## Languages

UI: English (base). Pulong speaks in the senior's language: English / Mandarin / Tagalog.
