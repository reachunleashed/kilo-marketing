# Recon Summary — Kilo (usekilo.com)

**Date:** 2026-02-20
**Phase:** 0 — Reconnaissance Complete
**Tools Used:** Firecrawl (site scraping + search), Playwright (screenshots + snapshots)

---

## Company Overview

**Kilo** is a gym management SaaS company based in Juno Beach, FL. They build software specifically for coaching-style gyms (CrossFit, martial arts, bootcamp, HYROX, personal training studios). Founded in 2019, they serve 1,000+ gyms worldwide.

**Products:**
- **Gym Management Software (GMS)** — $150/mo — Member management, billing, scheduling, reporting
- **Gym Lead Machine (GLM)** — $375/mo — Marketing automation, CRM, done-for-you website, lead nurture
- **Bundle** — $450/mo — GMS + GLM combined
- **Gym Websites** — $175/mo — Standalone website-only product

**Unique value proposition:** The ONLY gym software platform that combines management software + marketing automation + done-for-you websites in a single system. No competitor offers this combination.

---

## Competitive Landscape

### Tier 1 — Direct Competitors (same target market)

| Competitor | Focus | Key Difference from Kilo |
|-----------|-------|------------------------|
| **PushPress** | Coaching gym management | No done-for-you websites, smaller marketing automation |
| **Wodify** | CrossFit-focused management | Complex UI, no CRM/marketing, no website service |

### Tier 2 — Adjacent Competitors (broader market)

| Competitor | Focus | Key Difference from Kilo |
|-----------|-------|------------------------|
| **Zen Planner** | Boutique fitness (Daxko family) | Legacy platform, no integrated website/CRM |
| **Mindbody** | General wellness/fitness | Expensive, generalist, not coaching-gym-specific |
| **Glofox** (ABC Fitness) | Boutique studios | Enterprise pricing, acquired by ABC Fitness |

### Tier 3 — Newer/Smaller Players
Gymdesk, WellnessLiving, 1Club.ai, Smart Health Clubs, Woven

### Competitive Moat
Kilo's done-for-you website service ($175/mo, live in 9 days, annual redesign, white-glove support) has NO direct competitor equivalent. This is their strongest differentiator and should be central to any ad strategy.

---

## Site Architecture

99 pages discovered across 8 content categories:
- 3 product pages, 7 industry pages, 4 competitor comparison pages
- 5+ customer case studies, 4 resource sections (blog, Gym World, Using Kilo, Sales)
- Strong SEO structure with industry-specific landing pages

**Tech:** WordPress + Elementor, Meta Pixel (PixelYourSite), GymLeadMachine scripts

---

## Messaging & Voice

### Brand Voice Characteristics
- **Confident but not arrogant** — uses data and social proof rather than superlatives
- **Results-focused** — every claim backed by a specific stat
- **Empathetic to pain points** — "Running a gym is hard. Kilo makes it easier."
- **Anti-complexity positioning** — positions against "overwhelm" and "bloated interfaces"
- **Community-oriented** — emphasizes gym owner partnerships, annual town halls, mentorship brand partnerships

### Key Messaging Themes
1. **Time savings** — "Reclaim your time," "384 hours saved/year"
2. **Revenue growth** — "210% more memberships," ROI calculator
3. **Ease of use** — "80% say easier than previous software," Capterra Best Ease of Use
4. **All-in-one simplicity** — vs juggling multiple tools/platforms
5. **Done-for-you** — "We do the work for you," white-glove service

### Social Proof Strategy
- Named testimonials with photos + gym names (not anonymous)
- Specific results: "7 NSI's and 5 new members in 5 days" (Jay Storey)
- Third-party review badges (Capterra, GetApp, Software Advice — 5 awards)
- Industry partner endorsements (Chris Cooper, Andrew Hiller, Mark Fisher)
- "Gyms that switched from [competitor]" carousels with real gym logos

---

## Pricing Intelligence

| Tier | Monthly | Annual Equivalent | ROI Story |
|------|---------|-------------------|-----------|
| GMS | $150 | $1,800 | Core management tools |
| GLM | $375 | $4,500 | "Close 2 extra members/year and GLM is fully paid for" |
| Bundle | $450 | $5,400 | Best value — $75 savings vs separate |
| Websites only | $175 | $2,100 | Standalone option for website-only customers |

**Competitor pricing context:** From firecrawl search results, the comparison sites indicate Kilo is competitively priced in the mid-range. PushPress and Wodify have similar or higher pricing for fewer integrated features.

---

## Strategic Opportunities

### 1. "Switch from [Competitor]" Campaigns
Kilo already has dedicated comparison pages with customer logos for Wodify, Zen Planner, PushPress, and Mindbody. These are ready-made ad angles — target dissatisfied users of each competitor.

### 2. ROI Calculator as Lead Magnet
The GLM page's ROI table ("2 members/year = 60% ROI, 860% ROI at 1/month") is a compelling conversion tool. Could be turned into an interactive calculator or lead magnet.

### 3. "Done-For-You Website" Differentiator
No competitor offers this. Position as: "The only gym software that builds your website FOR you — live in 9 days."

### 4. Industry-Specific Targeting
7 dedicated industry pages (CrossFit, martial arts, bootcamp, HYROX, PT studios, 24/7 gyms, multi-location) enable hyper-targeted ad campaigns with matching landing pages.

### 5. Partnership-Driven Authority
Two Brain Business and Business for Unicorns are two of the largest gym mentorship brands. Their endorsement is a powerful trust signal — feature in ads targeting their communities.

### 6. Results-Based Ad Copy
Rich stat library for ad hooks:
- "18% more leads monthly"
- "61% lead increase in 3 months"
- "77% say it pays for itself in 3 months"
- "Websites live in 9 days"
- "Net gain of 33 members" (Charlie Goode testimonial)

---

## Compliance Considerations

Key rules for Kilo ad campaigns (full details in `reference/compliance-notes.md`):
1. Substantiate all performance claims with source data
2. Use "on average" or "reported by X% of customers" language
3. Clearly disclose subscription terms in all ads
4. Competitor comparison claims must be factual
5. SMS/email marketing requires opt-in consent (TCPA)
6. FTC Click-to-Cancel Rule applies to subscription cancellation

---

## Output Files Reference

| File | Contents |
|------|----------|
| `strategy/audit/competitor-research.md` | Full competitor analysis with pricing, features, and positioning |
| `strategy/audit/recon-summary.md` | This file — unified summary |
| `strategy/site-intel/client-site-analysis.md` | Detailed page-by-page site breakdown |
| `strategy/site-intel/sitemap-crawled.md` | 99 discovered URLs |
| `reference/compliance-notes.md` | SaaS advertising compliance rules |
| `assets/images/screenshots/` | 4 full-page screenshots (homepage, websites, GLM, pricing) |
| `.firecrawl/` | Raw scrape data (homepage, GLM, pricing, vs-wodify, vs-zen-planner, search results) |

---

## Next Steps

1. **Phase 1 — Diagnose:** Run the `orchestrator` skill to determine skill sequence
2. **Phase 2 — Audit:** Analyze current ad account (if active), audit competitor Facebook ads
3. **Phase 3 — Strategy:** Extract brand voice, develop positioning angles, audience research
4. **Phase 4 — Creative:** Ad copy, landing pages, email sequences
5. **Phase 5 — Build:** Landing page implementation
6. **Phase 6 — Optimize:** Weekly performance loop
