# Kilo — Current Funnel Map

**Date:** 2026-02-24
**Status:** Phase 2 audit

---

## Current Funnel Architecture

### Stage 1: Awareness (Entry Points)
| Source | Landing Page | Traffic Type |
|--------|-------------|--------------|
| Organic search | Homepage, product pages, blog | SEO |
| Content marketing | Blog, Gym World, Resources, Using Kilo, Sales | Inbound |
| Industry-specific search | /crossfit/, /martial-arts/, /bootcamp/, /hyrox/, /personal-training-studio/, /24-7-access-gyms/, /multi-location-gym/ | SEO / Long-tail |
| Competitor search | /kilo-vs-wodify/, /kilo-vs-zen-planner/, /kilo-vs-pushpress/, /kilo-vs-mindbody/ | SEO / Comparison |
| Partner referrals | Homepage (Two Brain Business, Business for Unicorns, etc.) | Referral |
| Direct | Homepage | Brand |

### Stage 2: Consideration (Product Pages)
| Page | Product | Price | Primary CTA | Secondary CTA |
|------|---------|-------|-------------|---------------|
| /gym-websites/ | Done-for-you websites | $175/mo | "See How It Works" (popup) | "Book a Free Call" (bottom) |
| /gym-lead-machine/ | Marketing automation + CRM | $375/mo | "Watch The Demo" (popup) | "Book a Free Call" (bottom) |
| /gym-management-software/ | Member management + billing | $150/mo | "See How Kilo Works" (popup) | "Book a Free Call" (bottom) |
| /pricing/ | All products | $150-$450/mo | "Get Started Today" (anchor) | "Book a Demo" (on each card) |
| /customers/ | Case studies | N/A | Links to product pages | N/A |

### Stage 3: Decision (Booking)
| Page | Action | Duration | Friction Level |
|------|--------|----------|----------------|
| /book-your-sales-call/ | Schedule a "Sales Call" | 45 minutes | HIGH — long commitment, "sales" language |

### Stage 4: Close
| Event | Owner | Outcome |
|-------|-------|---------|
| 45-min sales call | Kilo sales team | Close on GMS, GLM, Bundle, or Website subscription |

---

## Conversion Paths

### Path A: High-Intent (Direct → Book)
```
Nav "Book a Demo" → /book-your-sales-call/ → Schedule → Sales Call → Close
```
- **Shortest path:** 2 clicks to booking
- **Friction:** "Sales Call" language, 45-min commitment

### Path B: Product Research → Book
```
Homepage → Product Page → "Book a Free Call" (bottom CTA) → /book-your-sales-call/ → Schedule → Sales Call → Close
```
- **Path length:** 3-4 pages
- **Friction:** Popup CTAs at top of product pages; direct booking CTA only at bottom

### Path C: Video Demo → ??? (Broken)
```
Any Page → "Watch a Demo" (popup) → Video plays → ??? No next step captured
```
- **Issue:** Video demo popup doesn't capture email or redirect to booking. Dead end.

### Path D: Competitor Comparison → Book
```
Search "Kilo vs Wodify" → /kilo-vs-wodify/ → "Book a Demo" → /book-your-sales-call/ → Schedule → Sales Call → Close
```
- **Strong path:** Pre-qualified prospects already evaluating alternatives

---

## Funnel Gaps

### 1. No Lead Capture for Low-Intent Visitors
The site has no mechanism to capture email addresses from visitors who aren't ready to book a call:
- No newsletter signup
- No gated content (guides, whitepapers, templates)
- No free tool (ROI calculator, gym health check)
- No "Get a Quote" form
- No "Email me the pricing" option

**Impact:** All medium/low-intent traffic is lost forever.

### 2. Video Demo is a Dead End
"Watch a Demo" is one of the most-clicked CTAs, but the popup video doesn't:
- Capture contact info before or after viewing
- Show a booking CTA after the video ends
- Track who watched and for how long (for retargeting)

### 3. Single Conversion Event
The only conversion event is booking a 45-minute sales call. There's no:
- Quick 15-minute intro call option
- Self-serve trial or sandbox
- Live chat for instant questions
- Contact form for email inquiries (only mailto: link)

### 4. No Post-Visit Nurture
Without email capture, there's no way to:
- Send follow-up content to visitors who browsed but didn't book
- Re-engage with educational content
- Build a nurture sequence that warms cold leads

---

## Recommendations for Landing Page Work

Based on this funnel analysis, here are the landing page opportunities:

1. **Redesign /book-your-sales-call/** — Fix "Sales Call" language, add social proof, consider shorter call option
2. **Create a lead capture mechanism** — Interactive ROI calculator, pricing comparison tool, or downloadable guide
3. **Add a post-video-demo CTA flow** — After watching the demo, redirect to booking or email capture
4. **Pricing page improvements** — Feature comparison matrix, savings callout, visible prices above fold
5. **Industry-specific landing pages** — Use existing /crossfit/, /martial-arts/ pages as templates for paid traffic landing pages (if/when Meta Ads are added)
