# Strategy & Decisions

## Strategic Context

This project emerged from Fahad's strategic pivot on Aug 11, 2026:
- **Killed:** Sigma Vanity (e-commerce) and all side projects
- **New focus:** Single service, single channel — Instagram personal brand → web dev/web design clients
- **Parallel:** Building physique/looks as social capital multiplier

The brand photoshoot audit was the first concrete build under the new strategy — a lead generation funnel for a personal brand photography service.

## Why This Service?

1. **High-margin service business** — low overhead, high value
2. **Fahad's existing skills** — web dev, design sensibility, personal brand building
3. **Instagram-first distribution** — aligns with the single-channel strategy
4. **Personal brand credibility** — the shoot itself becomes content and proof
5. **Scalable** — audit is the funnel, shoots are the product, system is the IP

## Key Decisions Log

### 1. Free Audit as Entry Point (not paid)
- **Decision:** The audit is 100% free, no credit card
- **Why:** Lowest possible friction. Goal is qualified lead volume, not upfront revenue
- **Trade-off:** Time investment per audit — mitigated by 10/month cap

### 2. No Prices on Landing Page
- **Decision:** Zero price mentions anywhere on the page
- **Why:** Price destroys value-building. The call is where value gets established and price gets contextualized
- **Implementation:** All pricing stripped in commit `98cca58`

### 3. Emotion→Logic→Fear Structure
- **Decision:** Restructure from flat sections to 3-block narrative arc
- **Why:** Pure logic doesn't convert. Pure emotion doesn't build trust. The arc does both
- **Implementation:** Commit `b6b9784`

### 4. Homework Page Added
- **Decision:** 3-step pre-call questionnaire on separate page
- **Why:** Pre-frames the prospect, reduces call time spent on basics, increases perceived value
- **Implementation:** Commit `b6b9784`, `homework.html`

### 5. "Looks, Not Photos" as Core Concept
- **Decision:** Make this the defining mental model shift
- **Why:** It's contrarian, memorable, and true. Everyone thinks they need more photos. They need a plan
- **Implementation:** Woven throughout copy, FAQ, and homework

### 6. 10 Audits/Month Scarcity Cap
- **Decision:** Hard cap at 10/month, stated on page
- **Why:** Creates urgency, protects quality, justifies the "application" framing
- **Implementation:** Urgency section with live slot counter

## Domain Strategy

46 domains checked across 5 tiers (see `domains.csv`):
- **T1 - Brand:** maincharacterphotos.com, thesharplook.com, signaturelooks.com
- **T2 - Mechanic:** looksnotpics.com, thelooksformula.com, thelookaudit.com
- **T3 - Coach/Audit:** brandphotoaudit.com, freebrandphotoaudit.com
- **T4 - Level Up/Post-Worthy:** upgradeyourphotos.com, postworthyphotos.com
- **T5 - Local/Wildcard:** shootsmontreal.com, montrealbrandshoots.com

7 taken, 39 available. Domain not yet purchased.

## What's Still Pending

- [ ] Booking widget (Calendly/Cal.com embed) on homework page
- [ ] Serverless email endpoints (`/api/audit`, `/api/homework`)
- [ ] Custom domain purchase + DNS
- [ ] Vercel deployment config (currently on default subdomain)
- [ ] Instagram content to drive traffic to the funnel
- [ ] Actual shoot pricing model (discussed on call only)