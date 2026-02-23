# CLAUDE.md — Kilo Marketing Project

> Global rules (WAT framework, conventions, Meta Ads safety, context flow) are in `~/.claude/CLAUDE.md`. This file covers Kilo-specific context only.

## Client Overview
- **Client:** Kilo (usekilo.com)
- **Industry:** Fitness SaaS / Gym Management Software
- **Platform:** Meta Ads (Facebook/Instagram) + Custom SaaS Website (WordPress + Elementor)
- **Goal:** Generate qualified demo requests and sales calls from coaching gym owners
- **Funnel:** Ad -> Landing Page / Product Page -> "Book a Demo" -> Sales Call -> Close

---

## Client Details

**Founder:** [TBD — confirm with user]
**Methodology:** All-in-one SaaS platform for coaching gyms — combining management software, CRM/marketing automation (Gym Lead Machine), and done-for-you website creation
**Core Offer:** SaaS subscriptions: GMS ($150/mo), GLM ($375/mo), Bundle ($450/mo), Websites ($175/mo)
**Target Audience:** Independent gym owners running coaching-style gyms — CrossFit affiliates, martial arts studios, bootcamp gyms, HYROX facilities, personal training studios, small group training gyms, 24/7 access gyms, multi-location operators
**Location:** Global (English-speaking markets, primarily U.S.)
**Contact:** hello@usekilo.com | 14255 U.S. Hwy 1 Suite 281, Juno Beach, FL 33408

**Key Claims & Stats:**
- "1,000+ gyms worldwide"
- "18% more leads monthly" (Kilo websites)
- "61% lead volume increase in 3 months" (Kilo websites)
- "210% membership growth" (GLM users)
- "384 hours saved per year" (GLM automation)
- "35.3 more qualified leads per month" (GLM)
- "77% of customers say GLM pays for itself in the first 3 months"
- "80% of customers report Kilo is easier to use than previous software"
- "92% would highly recommend Kilo"
- "Websites live in 9 days or less"

**Brand Identity:**
- Colors: Dark Navy (#0A1C38) + Bright Cyan (#1EB1F9) + Mint/Teal gradient (hero sections)
- Fonts: Custom serif "KILO" logo, modern sans-serif body text (premium web fonts)
- Tone: Professional, confident, results-focused, approachable, anti-complexity
- Trust elements: Capterra Best Value 2025, Software Advice Front Runners 2025, GetApp Category Leaders 2025, Capterra Best Ease of Use 2025, Capterra Shortlist 2025; named testimonials with photos; industry partnership logos (Two Brain Business, Business for Unicorns, Andrew Hiller, The Sevan Podcast); Inc. magazine profile

**Current Funnel:**
1. Content marketing (blog, Gym World, resources) + Paid ads -> usekilo.com
2. Product pages (Gym Websites, GLM, GMS) with "Learn More" / "Watch a Demo"
3. "Book a Demo" / "Book a Free Call" -> /book-your-sales-call/ (calendar booking)
4. Sales call -> Close on subscription

---

## Primary Skills

### 1. `orchestrator` (Vibe Marketing)
Run this first (Phase 1 of the runbook). It asks qualifying questions, diagnoses the client's situation, and recommends the right skill sequence. Think of it as the fractional CMO layer.

### 2. `marketing-campaign-build` (project-local)
Read `skills/marketing-campaign-build/SKILL.md` before starting any campaign work (Phases 2-6 of the runbook). This skill defines the complete build sequence across audit, strategy, creative, build, and optimize phases — which underlying skills to invoke at each step, what context to pass between them, and where user approval is required.

**IMPORTANT:** Always read the skill file first. It orchestrates all Vibe Marketing skills (brand-voice, positioning-angles, direct-response-copy, lead-magnet, email-sequences, content-atomizer), all Vibe Creative skills (ai-creative-strategist, ai-social-graphics, ai-product-photo, ai-product-video, ai-talking-head), and core skills (brainstorming, agent-browser, frontend-design) in the correct order with proper context flow.

### Supporting Tools
| Tool | Use For |
|------|---------|
| `perplexity` MCP | Competitor research, market intelligence, compliance research (Phase 0) |
| `playwright` MCP | Site screenshots, page analysis, competitor site capture (Phase 0, 5) |
| `agent-browser` | Browse/screenshot websites, audit pages, test built pages |
| `brainstorming` | Explore direction before committing to creative or design choices |
| `frontend-design` | Build landing pages and web components |
| `meta-ads` MCP | Facebook/Meta ad operations, targeting research, performance data |
| `ghl-mcp` MCP | CRM operations if client uses GoHighLevel |

---

## Key Reference Documents

| Document | Location | Purpose |
|----------|----------|---------|
| Master task list | `runbook.md` | Full phase checklist and progress tracking |
| Campaign build skill | `skills/marketing-campaign-build/SKILL.md` | Orchestrator for Phases 2-6 |
| Product info | `reference/product-info.md` | Kilo product details and pricing |
| Audience profiles | `reference/audience-profiles.md` | Target segment definitions |
| Compliance notes | `reference/compliance-notes.md` | SaaS/gym advertising rules |
| Campaign IDs | `reference/meta-ads-campaign-ids.md` | All created Meta Ads object IDs |

---

## SaaS / Gym Software Compliance

- **Performance claims must be substantiated.** Stats like "18% more leads" and "77% say pays for itself in 3 months" must be backed by actual customer data. Keep source documentation on file.
- **Use "on average" or "reported by X% of customers" language.** Avoid absolute guarantees. Do NOT claim "guaranteed results" — use "designed to help" or "our customers report."
- **Testimonials must reflect typical results.** FTC Endorsement Guides require testimonials represent what consumers can generally expect. "Results not typical" disclaimers are no longer sufficient.
- **Clearly disclose subscription terms in all ads.** Price, billing frequency, auto-renewal terms, and cancellation process must be transparent. FTC Click-to-Cancel Rule (2025-2026) requires cancellation as easy as signup.
- **Competitor comparison claims must be truthful.** Feature comparisons are permissible (and Kilo has dedicated comparison pages). Do not make false claims about competitor capabilities or pricing.
- **SMS/email marketing compliance.** GLM's automated nurture (email + SMS) must have proper opt-in consent (TCPA). Honor opt-out requests immediately. CAN-SPAM: include unsubscribe, physical address, honest subject lines.
- Reference `reference/compliance-notes.md` for full guidelines.

---

## Project-Specific Rules

1. **Kilo is a SaaS product, not a service.** All copy must sell software subscriptions, not consulting or done-for-you services (except the website build offering).
2. **Always qualify claims with source language.** Every stat from the "Key Claims & Stats" section must include hedging language ("on average," "reported by X% of customers") per compliance rules above.
3. **Demo is the conversion event.** All ads and landing pages drive to "Book a Demo" — never direct purchase. The sales team closes on the call.
4. **Multiple products require clear segmentation.** GMS, GLM, Websites, and Bundle each have distinct value props and audiences. Don't conflate them in a single ad unless promoting the Bundle.
5. **Competitor comparison pages exist on usekilo.com.** Leverage these in ad strategy (e.g., "Kilo vs PushPress") but ensure all comparative claims are truthful and verifiable.

---

## Setup Checklist
- [x] Copy this file into client folder
- [x] Copy `skills/marketing-campaign-build/` directory
- [x] Create `runbook.md` master task list
- [x] Create directory structure (including recon directories)
- [x] Perplexity competitor research (Phase 0)
- [x] Playwright site analysis (Phase 0)
- [ ] Replace all placeholders with client-specific values
- [ ] Fill in `reference/product-info.md` with product details
- [ ] Create `.env` with required API keys (if needed)
- [x] Create `.gitignore`
- [x] Initialize git repo
- [ ] Run `orchestrator` skill (Phase 1 of runbook)
- [ ] Follow `marketing-campaign-build` skill (Phases 2-6 of runbook)
