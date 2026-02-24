# Kilo — Landing Page & CRO Audit

**Date:** 2026-02-24
**Auditor:** Claude (Agent)
**Pages Audited:** Homepage, Gym Websites, Gym Lead Machine, Gym Management Software, Pricing, Book a Call
**Screenshots:** `assets/images/screenshots/audit/`

---

## Executive Summary

Kilo's website is **professionally built and well-structured** — far above average for the gym SaaS space. The site has strong social proof, clear product segmentation, and consistent CTAs. However, there are several CRO opportunities that could improve conversion rates, particularly around the booking page, pricing page structure, and hero section CTAs.

**Overall Grade: B+**
- Design & Branding: A
- Social Proof: A+
- CTA Clarity: B+
- Conversion Path: B
- Booking Page: C+
- Mobile Readiness: B+ (responsive templates, but not verified on mobile)

---

## Page-by-Page Analysis

### 1. Homepage (usekilo.com)

**Hero Section:**
- H1: "Gym Management Software & Services" (eyebrow)
- H2: "Software Built to Grow Coaching Gyms"
- Subhead: "Run your gym, grow your membership, and reclaim your time with software built for coaching gyms."
- CTAs: "Watch a Demo" + "Speak with an Expert"

**Strengths:**
- Clean, modern design with strong visual hierarchy
- Product mockups (laptop + mobile) show the actual software
- Immediate differentiation: "coaching gyms" is specific, not generic
- Dual CTAs offer low-commitment (Watch Demo) and high-commitment (Speak with Expert) paths

**Issues:**
- [ ] **P1 — No headline stat.** The hero doesn't lead with a compelling number. "1,000+ gyms worldwide" or "18% more leads" would add instant credibility above the fold.
- [ ] **P2 — "Watch a Demo" opens a popup** (Elementor action URL). If the popup fails to load or is slow, the primary CTA is dead. Should have a fallback URL.
- [ ] **P2 — Large whitespace gap** between hero and "Running a gym is hard" section. This dead space pushes compelling content below the fold unnecessarily.
- [ ] **P3 — "Gym Management Software & Services" eyebrow** is redundant with the H2. Could be replaced with a trust signal (e.g., "Trusted by 1,000+ coaching gyms").

**Below the Fold:**
- 3 product sections (Websites, GLM, GMS) — well laid out with clear "Learn More" CTAs
- Partner carousel (Two Brain Business, Business for Unicorns, Andrew Hiller, The Sevan Podcast)
- 5 software award badges (Capterra, GetApp, Software Advice)
- Industry slider (6 gym types)
- 3 named testimonials with photos (Mark Fisher, Andrew Hiller, Chris Cooper)

**Issues:**
- [ ] **P2 — No mid-page CTA.** The page scrolls through ~5 sections before hitting another conversion opportunity. Should add "Book a Demo" CTA after the 3 product sections.
- [ ] **P3 — Partner logos load lazily** and some appear blank in screenshots. Ensure all logos have proper alt text and fallback images.

---

### 2. Gym Websites (/gym-websites/)

**Hero Section:**
- Eyebrow: "GYM WEBSITES"
- H2: "Gym Website Creation Services"
- Subhead: "A professionally built, high-performing website designed to attract new members and grow your gym."
- CTA: "See How It Works" (opens demo popup)
- Visual: Torque Health & Fitness website mockup with "Lead Capture" and "Mobile Responsive" callouts

**Strengths:**
- Strong stat section: 1,000+ gyms, 61% lead increase, 92% recommend
- Excellent comparison table (Build Yourself vs Local Provider vs Kilo)
- Template carousel shows actual website designs
- Clear pricing in bottom CTA: "$175/month"
- FAQ section addresses common objections
- Named testimonials from specific gym owners

**Issues:**
- [ ] **P1 — Only 1 CTA in hero** ("See How It Works" popup). Missing a direct "Book a Call" button alongside it. Every product page hero should have both a low-commitment and high-commitment CTA.
- [ ] **P2 — "See How It Works" label is vague.** Users don't know what happens when they click. "Watch a 2-Min Demo" or "See Website Examples" would be clearer.
- [ ] **P2 — Stat counters start at 0** and animate up on scroll. If JavaScript fails or user scrolls quickly, they see "0" instead of the actual numbers. Consider showing final numbers by default.
- [ ] **P3 — Template carousel images** are small in viewport. Clicking them should open a full-size preview or link to live example sites.

---

### 3. Gym Lead Machine (/gym-lead-machine/)

**Hero Section:**
- Eyebrow: "MARKETING AUTOMATION SOFTWARE"
- H2: "Gym Lead Machine"
- Subhead: "Kilo's powerful, all-in-one marketing and sales system built to help you generate more leads, book more appointments, and grow your gym with less effort."
- CTA: "Watch The Demo" (popup)
- Visual: Chat/messaging UI mockup showing lead conversation flow

**Strengths:**
- Strongest stat section of all pages: 210% more memberships, 384 hours saved, 35.3 more leads/month
- Excellent "How GLM Works" section with 6 step-by-step features
- ROI calculator table (2 members/year = 60% ROI, 12/year = 860% ROI) — extremely compelling
- Problem/Solution comparison table is very persuasive
- Video testimonial section
- Multiple named testimonials with specific results ("net gain of 33 members")

**Issues:**
- [ ] **P1 — Same single-CTA problem as Websites page.** Hero only has "Watch The Demo" popup — no direct booking CTA.
- [ ] **P1 — ROI table is buried** deep in the page. This is the most compelling content on the entire site. Consider elevating it closer to the hero or making it an interactive calculator.
- [ ] **P2 — "Watch The Demo" popup CTA is the only hero action.** If the Elementor popup breaks, 100% of hero clicks fail. Always have a fallback link.
- [ ] **P2 — Chat UI mockup in hero** is visually nice but doesn't show the product dashboard. Users want to see the actual software they'll be using, not a stylized conversation.

---

### 4. Gym Management Software (/gym-management-software/)

**Hero Section:**
- Eyebrow: "DISCOVER THE BEST SOFTWARE FOR GYM MANAGEMENT"
- H2: "Gym Management Software"
- Subhead: "A powerful, all-in-one system built to simplify operations, increase revenue, and help you run a stronger, more profitable gym."
- CTA: "See How Kilo Works" (popup)
- Trust: 8 award/review badges inline
- Visual: Dashboard screenshots showing member management, payments, reporting
- Availability note: "Available now in the USA, Canada, and the UK."

**Strengths:**
- Best hero of all pages — shows actual product screenshots (dashboard, payments, member list)
- 8 trust badges immediately visible
- "8 Reasons" section is persuasive (built for coaching gyms, weekly features, simple, fast support, transparent pricing, smooth transition, integrated with GLM, data ownership)
- Video testimonial
- "Switching to Kilo" section directly addresses migration fear (top objection for SaaS switches)
- Clear pricing: "$150/month" in bottom CTA

**Issues:**
- [ ] **P1 — Same single-CTA popup issue.** "See How Kilo Works" opens a popup with no fallback.
- [ ] **P2 — Feature carousel** only shows 1 slide at a time. Users can't scan features quickly. Consider a grid layout instead.
- [ ] **P3 — Testimonials are text-heavy.** Some quotes are 100+ words. Consider pull-quote formatting with the key stat bolded.

---

### 5. Pricing (/pricing/)

**Hero Section:**
- H1: "Simple Software for Gym Owners"
- H2: "All the tools you need to manage your gym, attract new clients, and grow your business."
- CTA: "Get Started Today" (anchor link to pricing cards below)
- "No hidden fees."

**Pricing Cards:**
- GMS: $150/month — 4 bullet features + expandable "See All Features" + "Book a Demo"
- GLM: $375/month — 4 bullet features + expandable "See All Features" + "Book a Demo"
- Bundle (GLM + GMS): $450/month — "BEST VALUE" badge — 2 bullet features + expandable + "Book a Demo"

**Strengths:**
- Clean, clear pricing — no confusion
- "BEST VALUE" badge on Bundle draws the eye
- Every card has a "Book a Demo" CTA
- FAQ section addresses common pricing questions (10 questions)
- Testimonials section reinforces value

**Issues:**
- [ ] **P1 — Pricing cards are below the fold.** Hero area has a large decorative gradient and vertical line animation that pushes the actual prices way down. Users who land on /pricing/ want to see prices IMMEDIATELY.
- [ ] **P1 — No feature comparison matrix.** Users can't easily see what GMS includes vs GLM vs Bundle. The "See All Features" expandable is hidden by default. A side-by-side comparison grid would dramatically improve decision-making.
- [ ] **P2 — Bundle card only has 2 bullets** ("Combines all features from GLM and GMS" and "Fully integrated for a seamless experience"). This is the most important card but has the least information.
- [ ] **P2 — No savings callout on Bundle.** $150 + $375 = $525, but Bundle is $450 — that's $75/month savings ($900/year). This should be prominently displayed.
- [ ] **P3 — "Get Started Today" CTA text** implies you can sign up directly. It actually scrolls to pricing cards. Misleading micro-copy.
- [ ] **P3 — Gym Websites ($175/month) is not shown** on pricing page. Users who want a standalone website won't find pricing here.

---

### 6. Book a Call (/book-your-sales-call/)

**Layout:**
- Left panel: Dark overlay image with "Book a Demo with a Kilo Expert" heading + brief description
- Right panel: Embedded calendar (external booking tool) showing "Sales Call" — 45 minutes

**Strengths:**
- Clean, simple layout focused on the single action
- Calendar is embedded and functional
- Shows duration (45 min) and timezone
- Multiple time slots available

**Issues:**
- [ ] **P0 — CRITICAL: Page title says "Sales Call" not "Demo."** The nav says "Book a Demo" but the calendar widget says "Sales Call — 45 Mins." This creates a disconnect. Prospects expecting a product demo may be put off by "Sales Call" language. This is likely hurting conversion.
- [ ] **P0 — No social proof on booking page.** This is the highest-intent page on the entire site and it has ZERO testimonials, trust badges, or stats. Every booking page should reinforce value at the moment of decision.
- [ ] **P1 — 45-minute call is long.** For a SaaS demo, 45 minutes is a significant time commitment. Consider offering a shorter option (15-min "Quick Chat" or "Express Demo") alongside the full 45-min call.
- [ ] **P1 — No "what to expect" section.** Users don't know what happens on the call. Adding 3-4 bullets (e.g., "We'll show you the dashboard, discuss your gym's needs, answer questions — no pressure") would reduce booking anxiety.
- [ ] **P2 — Calendar shows times in PST** by default. For a global product serving US/Canada/UK, auto-detecting timezone or prominently showing timezone selector would reduce friction.
- [ ] **P2 — Below the calendar is empty space** followed by the full footer. There should be a "Still have questions?" section with contact info (hello@usekilo.com) and/or FAQ links.

---

## Cross-Site Issues

### Recurring Patterns

1. **Every product page hero relies on an Elementor popup for the primary CTA.** If the popup script fails, breaks, or is blocked by an ad blocker, the most important action on every page is broken. Every popup CTA should have a direct URL fallback.

2. **Console error on every page:** `ReferenceError: wp is not defined` (wp-i18n-js-after). Minor but indicates a WordPress script loading issue that should be fixed.

3. **Duplicate Meta Pixel warning** was flagged in Phase 0 recon. PixelYourSite may be firing the pixel twice, which would inflate retargeting audiences and skew conversion tracking.

4. **No exit-intent or scroll-triggered CTAs.** The site doesn't attempt to capture visitors who are about to leave or who have scrolled 50%+ without converting.

5. **No live chat or chatbot.** For a SaaS product at this price point ($150-$450/mo), having a live chat widget (even if AI-powered) could capture prospects who aren't ready to book a 45-minute call.

---

## Priority Summary

### P0 — Fix Immediately
| # | Issue | Page | Impact |
|---|-------|------|--------|
| 1 | "Sales Call" vs "Demo" language mismatch on booking page | /book-your-sales-call/ | High — creates trust friction at highest-intent moment |
| 2 | Zero social proof on booking page | /book-your-sales-call/ | High — no value reinforcement at decision point |

### P1 — High Impact
| # | Issue | Page | Impact |
|---|-------|------|--------|
| 3 | All hero CTAs depend on Elementor popup with no fallback | All product pages | Medium-High — single point of failure |
| 4 | Pricing cards below fold with decorative gap | /pricing/ | Medium — pricing page visitors want to see prices immediately |
| 5 | No feature comparison matrix on pricing page | /pricing/ | Medium — makes it hard to compare products |
| 6 | Product page heroes have only 1 CTA (popup) — need a direct "Book a Call" | All product pages | Medium — missing high-commitment CTA path |
| 7 | ROI table buried deep on GLM page | /gym-lead-machine/ | Medium — strongest conversion content is hard to find |
| 8 | No stat/credibility number in homepage hero | Homepage | Medium — missed opportunity for instant trust |

### P2 — Medium Impact
| # | Issue | Page | Impact |
|---|-------|------|--------|
| 9 | No mid-page CTA between sections on homepage | Homepage | Low-Medium |
| 10 | Bundle pricing card lacks savings callout ($75/month saved) | /pricing/ | Low-Medium |
| 11 | 45-minute call commitment with no shorter option | /book-your-sales-call/ | Low-Medium |
| 12 | Stat counters animate from 0 (JS-dependent) | /gym-websites/, /gym-lead-machine/ | Low-Medium |
| 13 | Standalone Website pricing ($175/mo) absent from pricing page | /pricing/ | Low-Medium |

### P3 — Low Impact / Polish
| # | Issue | Page | Impact |
|---|-------|------|--------|
| 14 | Console error: wp is not defined | All pages | Low |
| 15 | Duplicate Meta Pixel concern | All pages | Low |
| 16 | Feature carousel shows 1 item at a time | /gym-management-software/ | Low |

---

## Funnel Map

```
                    AWARENESS
                       │
                       ▼
    ┌──────────────────────────────────────┐
    │          ENTRY POINTS                │
    │  • Organic search → Homepage         │
    │  • Blog/Resources → Content pages    │
    │  • Industry pages → /crossfit/, etc. │
    │  • Competitor pages → /kilo-vs-X/    │
    │  • Direct → Homepage                 │
    └──────────────────┬───────────────────┘
                       │
                       ▼
    ┌──────────────────────────────────────┐
    │         PRODUCT PAGES                │
    │  • /gym-websites/      ($175/mo)     │
    │  • /gym-lead-machine/  ($375/mo)     │
    │  • /gym-management-software/ ($150)  │
    │  • /pricing/           (all 3)       │
    └──────────────────┬───────────────────┘
                       │
           ┌───────────┼───────────┐
           ▼           ▼           ▼
    ┌──────────┐ ┌──────────┐ ┌──────────┐
    │ Watch a  │ │ Speak    │ │ Book a   │
    │ Demo     │ │ with an  │ │ Demo     │
    │ (popup)  │ │ Expert   │ │ (nav)    │
    └────┬─────┘ └────┬─────┘ └────┬─────┘
         │            │            │
         │            └──────┬─────┘
         │                   ▼
         │     ┌───────────────────────┐
         │     │ /book-your-sales-call │
         │     │  "Sales Call" — 45min │
         │     │  Calendar booking     │
         │     └───────────┬───────────┘
         │                 │
         │                 ▼
         │     ┌───────────────────────┐
         │     │    SALES CALL         │
         │     │  45-min guided demo   │
         │     │  → Close on plan      │
         │     └───────────┬───────────┘
         │                 │
         ▼                 ▼
    ┌──────────┐  ┌───────────────┐
    │ Video    │  │   CUSTOMER    │
    │ Demo     │  │  GMS $150/mo  │
    │ (nurture)│  │  GLM $375/mo  │
    │          │  │  Bundle $450  │
    └──────────┘  │  Web $175/mo  │
                  └───────────────┘
```

**Key Funnel Observations:**
1. **Single conversion point.** All paths lead to /book-your-sales-call/. There's no alternative conversion mechanism (no free trial, no self-serve signup, no lead magnet).
2. **Video demo is a dead end.** "Watch a Demo" opens a popup video but doesn't capture contact info or redirect to booking. It's a nurture step with no next action.
3. **No email capture.** There's no newsletter signup, free resource download, or gated content to capture leads who aren't ready to book a call.
4. **Funnel is effectively: Page → Book 45-min Call → Sales Close.** This works for high-intent traffic but loses all medium/low-intent visitors.
