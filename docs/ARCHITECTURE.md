# Architecture & Deployment

## Current Stack

- **Frontend:** Static HTML/CSS/JS (no framework, no build step)
- **Hosting:** Vercel (default subdomain)
- **Repo:** github.com/realfahadrahman/brand-photoshoot-audit
- **Fonts:** Google Fonts (Inter)

## File Structure

```
brand-photoshoot-audit/
├── index.html          # Landing page — free audit funnel
├── homework.html       # Pre-call questionnaire (3 steps)
├── domains.csv         # 46 domain candidates researched
├── .gitignore          # Ignores .vercel
└── docs/               # Strategy & offer documentation
    ├── OFFER.md
    ├── COPY_FRAMEWORKS.md
    ├── STRATEGY.md
    └── ARCHITECTURE.md
```

## Pages

### index.html (Landing Page)
- Hero with "Free Personal Brand Photo Audit" badge
- Emotion→Logic→Fear narrative structure
- Audit form (name, email, Instagram, platform, struggle)
- Form submits to `/api/audit` (not yet implemented) + stores in sessionStorage
- On submit, shows booking CTA linking to homework.html
- FAQ section (7 questions)
- Final CTA

### homework.html (Pre-Call Questionnaire)
- 3-step progressive form:
  1. Goals & platforms (goal select, platform checkboxes, profile links)
  2. Style & archetype (archetype select, style description, inspiration links, best feature, insecurities)
  3. Pre-call checklist (concept confirmation, extra notes)
- Progress bar with step indicators
- Submits to `/api/homework` (not yet implemented)
- Success screen on submit

## Deployment

Currently deployed to Vercel default subdomain:
- `landing-page-nine-rust-83.vercel.app`
- `landing-page-nine-rust-83.vercel.app/homework.html`

## Pending Infrastructure

### API Endpoints (Serverless)
- `POST /api/audit` — receive audit form submissions, send notification email
- `POST /api/homework` — receive homework submissions, send notification email

### Booking Widget
- Cal.com or Calendly embed on homework page success state
- Replaces current placeholder link

### Custom Domain
- Not yet purchased
- Top candidates: `freebrandphotoaudit.com` (SEO gold), `thesharplook.com` (brand), `looksnotpics.com` (contrarian hook)
- See `domains.csv` for full list

### Analytics
- Not yet set up
- Should track: page views, form completion rate, homework completion rate, conversion to call booking