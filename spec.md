# Ekan Solutions Inc. — Services Landing Page

## Current State
- App.tsx has a simple page state: `"home" | "about"`
- AboutPage.tsx is a standalone full landing page component with setPage prop
- Header nav links are anchor links (#services etc.) on home, but "About" triggers page change
- No dedicated Services page exists yet

## Requested Changes (Diff)

### Add
- `src/frontend/src/components/ServicesPage.tsx`: Full dedicated Services landing page with:
  1. Hero section — bold headline, subheadline, CTA button ("Get a Free Consultation")
  2. Services overview grid — 5 service cards (Cybersecurity, Project Management, Full Stack Dev, AWS Cloud, Java Development) with icons, descriptions, hover lift
  3. Deep-dive sections — one detailed section per service with bullet capabilities, use cases, and a side icon/visual
  4. Technology stack badges section — logos/tags for key tech used
  5. Process / How We Work section — 5-step flow (Analyze → Plan → Build → Secure → Deploy)
  6. Testimonials / Client Success strip (placeholder stats: 500+ projects, 15+ years, 100+ clients, 24/7 support)
  7. CTA banner — "Ready to Get Started? Contact Us Today"

### Modify
- `App.tsx`: Extend page state to `"home" | "about" | "services"`, add ServicesPage render branch, pass setPage
- `App.tsx` Header / NAV_LINKS: "Services" nav item triggers `setPage("services")` instead of anchor scroll

### Remove
- Nothing removed

## Implementation Plan
1. Create ServicesPage.tsx with all sections above, matching existing brand colors (#0A3D62 navy, #1ABC9C teal), Inter font, fade-in-up animations
2. Update App.tsx page state type to include "services"
3. Add ServicesPage import and render branch in App
4. Update Header so clicking "Services" nav item calls setPage("services") and clicking "Home" / logo returns to home
5. Validate and deploy
