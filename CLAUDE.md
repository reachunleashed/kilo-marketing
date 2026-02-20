# CLAUDE.md -- Kilo Marketing Project

## Project Overview
**Client:** Kilo (usekilo.com)
**Industry:** Fitness SaaS / Gym Management Software
**Current Platform:** Meta Ads (Facebook/Instagram) + Custom SaaS Website (WordPress + Elementor)
**Primary Goal:** Generate qualified demo requests and sales calls from coaching gym owners
**Funnel:** Ad -> Landing Page / Product Page -> "Book a Demo" -> Sales Call -> Close

**Role Split:**
- **Claude (Agent):** Strategy, copy, creative direction, landing page development, data analysis
- **User (Consultant):** Campaign execution, budget decisions, client communication, final approvals

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

## WAT Framework (Workflows, Agents, Tools)

This project runs on the WAT architecture. Probabilistic AI handles reasoning and decision-making. Deterministic code handles execution. That separation is what makes the system reliable.

### Layer 1: Workflows (The Instructions)
- Markdown SOPs stored in `workflows/`
- Each workflow defines: objective, required inputs, which tools/skills to use, expected outputs, edge cases
- Written in plain language -- the same way you'd brief someone on your team
- Workflows evolve as we learn. When you find better methods, discover constraints, or encounter recurring issues, update the workflow
- **IMPORTANT:** Don't create or overwrite workflows without asking unless explicitly told to

### Layer 2: Agent (The Decision-Maker)
- This is Claude's role. Read the relevant workflow, run tools/skills in the correct sequence, handle failures gracefully, and ask clarifying questions when needed.
- Before doing anything: check `workflows/` for the relevant SOP
- Before building anything new: check `tools/` for existing scripts
- Connect intent to execution without trying to do everything directly
- When uncertain about budget, targeting, or compliance -- always ask

### Layer 3: Tools (The Execution)
- Python scripts in `tools/` that do the actual work
- API calls, data transformations, file operations
- Credentials and API keys stored in `.env` -- NEVER store secrets anywhere else
- Scripts are consistent, testable, and fast
- **IMPORTANT:** If a tool uses paid API calls or credits, check with the user before running

### Self-Improvement Loop
Every failure makes the system stronger:
1. Identify what broke
2. Fix the tool/script
3. Verify the fix works
4. Update the workflow with the new approach
5. Move on with a more robust system

---

## Workflow Phases

### Phase 0 -- Recon
*Gather competitive intelligence and site analysis before any strategy work. Usually completed during initial setup.*

| Task | Skill / Tool | Output |
|------|-------------|--------|
| Research direct competitors (pricing, positioning, offers) | `perplexity` MCP (`perplexity_research`) | strategy/audit/competitor-research.md |
| Research market landscape (size, trends, audience) | `perplexity` MCP (`perplexity_search`) | strategy/audit/competitor-research.md |
| Research industry ad compliance rules | `perplexity` MCP (`perplexity_research`) | reference/compliance-notes.md |
| Screenshot & analyze client's current website/funnel | `playwright` MCP | strategy/site-intel/client-site-analysis.md |
| Screenshot & analyze top competitor sites | `playwright` MCP | strategy/site-intel/competitor-sites.md |

### Phase 1 -- Audit
*Understand what exists before changing anything.*

| Task | Skill / Tool | Workflow | Output |
|------|-------------|----------|--------|
| Screenshot & analyze current landing pages | `agent-browser` | `01-audit-landing-pages.md` | strategy/audit/landing-page-audit.md |
| Pull current campaign performance | `meta-ads` MCP | `02-audit-ad-account.md` | strategy/audit/account-audit.md |
| Audit current ad copy and creatives | `meta-ads` MCP | `02-audit-ad-account.md` | strategy/audit/account-audit.md |
| Screenshot & analyze competitor ads/pages | `agent-browser` | `03-competitor-analysis.md` | strategy/audit/competitor-audit.md |
| Map current funnel (ad -> page -> conversion) | Manual analysis | -- | strategy/funnel-map.md |

### Phase 2 -- Strategy
*Build the foundation that all creative work stands on.*

| Task | Skill | Workflow | Output |
|------|-------|----------|--------|
| Define brand voice | `brand-voice` | `04-brand-voice.md` | strategy/brand-voice.md |
| Find positioning angles | `positioning-angles` | `05-positioning-angles.md` | strategy/positioning-angles.md |
| Identify lead magnet concepts | `lead-magnet` | -- | creative/lead-magnets/ |
| Define audience segments | `meta-ads` MCP | -- | reference/audience-profiles.md |

### Phase 3 -- Creative
*Produce ads, copy, and landing page content.*

| Task | Skill | Workflow | Output |
|------|-------|----------|--------|
| Creative direction + briefs | `ai-creative-strategist` | `07-creative-production.md` | creative/briefs/ |
| Ad copy (primary text, headlines) | `direct-response-copy` | `06-ad-copy-creation.md` | creative/ad-copy/ |
| Ad images (static) | `ai-social-graphics` | `07-creative-production.md` | assets/images/ |
| Product photography for ads | `ai-product-photo` | `07-creative-production.md` | assets/images/ |
| Video ad scripts | `ai-product-video` / `ai-talking-head` | `07-creative-production.md` | assets/video/ |
| Landing page copy | `direct-response-copy` | `06-ad-copy-creation.md` | creative/landing-pages/ |
| Email sequences | `email-sequences` | -- | creative/email/ |

### Phase 4 -- Build
*Implement landing pages and web experiences.*

| Task | Skill / Tool | Workflow | Output |
|------|-------------|----------|--------|
| Explore design direction | `brainstorming` | -- | -- |
| Build landing pages | `frontend-design` | `08-landing-page-build.md` | landing-pages/src/ |

### Phase 5 -- Optimize
*Test, measure, iterate.*

| Task | Skill / Tool | Workflow | Output |
|------|-------------|----------|--------|
| Pull performance data | `meta-ads` MCP / `pull_meta_insights.py` | `10-weekly-optimization.md` | analytics/weekly-reports/ |
| A/B test copy/creative variations | `direct-response-copy` + `ai-social-graphics` | `10-weekly-optimization.md` | analytics/test-log.md |
| Iterate on winning angles | `positioning-angles` + `direct-response-copy` | -- | creative/ad-copy/ |
| Scale winners / kill losers | `meta-ads` MCP | `09-campaign-setup.md` | campaigns/ |

---

## Runbook

**`runbook.md`** is the master task list for this engagement. It defines every phase from recon through optimization, which skills to invoke at each step, and where user approval gates exist. Open this file to see the full checklist and track progress.

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

## Conventions

### File Naming
- **Strategy docs:** descriptive name (`brand-voice.md`, `positioning-angles.md`)
- **Creative docs:** `YYYY-MM-DD-descriptive-name.md` (date-prefixed for chronological tracking)
- **Weekly reports:** `week-YYYY-MM-DD.md` (Monday date of the week)
- **Images:** `descriptive-name-variant.png` (e.g., `hero-angle1-v2.png`)

### Ad Copy Document Format
Every ad copy doc must include:
- **Angle** -- which positioning angle it executes
- **Audience segment** -- who this targets
- **Placement** -- where it runs (feed, stories, reels)
- **Primary text** -- main body copy
- **Headlines** -- 3-5 headline options
- **Descriptions** -- supporting text
- **CTA** -- call to action button text

### Creative Briefs
Use the `ai-creative-strategist` brief format. Every brief links back to:
- The positioning angle it executes
- The audience segment it targets
- The landing page it drives to

### Campaign Docs
Each campaign file in `campaigns/active/` tracks:
- Campaign name and objective
- Ad set targeting (audiences, placements, budget)
- Creative assets used (links to files in assets/)
- Performance metrics (updated weekly)
- Test hypothesis (what we're testing and why)

### Test Log
`analytics/test-log.md` is a running table:
```
| Date | Test | Variant A | Variant B | Winner | ROAS Impact | Learning |
```

---

## Industry Compliance

**SaaS / Gym Software Advertising Rules:**

- **Performance claims must be substantiated.** Stats like "18% more leads" and "77% say pays for itself in 3 months" must be backed by actual customer data. Keep source documentation on file.
- **Use "on average" or "reported by X% of customers" language.** Avoid absolute guarantees. Do NOT claim "guaranteed results" — use "designed to help" or "our customers report."
- **Testimonials must reflect typical results.** FTC Endorsement Guides require testimonials represent what consumers can generally expect. "Results not typical" disclaimers are no longer sufficient.
- **Clearly disclose subscription terms in all ads.** Price, billing frequency, auto-renewal terms, and cancellation process must be transparent. FTC Click-to-Cancel Rule (2025-2026) requires cancellation as easy as signup.
- **Competitor comparison claims must be truthful.** Feature comparisons are permissible (and Kilo has dedicated comparison pages). Do not make false claims about competitor capabilities or pricing.
- **SMS/email marketing compliance.** GLM's automated nurture (email + SMS) must have proper opt-in consent (TCPA). Honor opt-out requests immediately. CAN-SPAM: include unsubscribe, physical address, honest subject lines.
- Reference `reference/compliance-notes.md` for full guidelines.

---

## File Structure

```
kilo/
├── CLAUDE.md              # This file -- project instructions
├── runbook.md             # Master task list -- the "fire off" checklist
├── skills/                # Project-local skills
│   └── marketing-campaign-build/
│       └── SKILL.md       # The orchestrator -- read this first
├── .env                   # API keys (gitignored, NEVER commit)
├── workflows/             # Markdown SOPs -- read before executing
├── tools/                 # Python scripts for deterministic tasks
├── .tmp/                  # Temporary files -- disposable, regenerated as needed
├── strategy/              # Long-lived reference docs (voice, angles, audits)
│   ├── audit/             # Phase 1 outputs
│   │   └── competitor-research/ # Perplexity research outputs
│   └── site-intel/        # Playwright site analysis outputs
├── creative/              # Versioned creative outputs (copy, briefs, concepts)
│   ├── briefs/            # Creative direction briefs
│   ├── ad-copy/           # Ad copy variations
│   ├── landing-pages/     # Landing page copy docs
│   ├── email/             # Email sequences
│   └── lead-magnets/      # Lead magnet concepts
├── assets/                # Generated images and video
│   ├── images/approved/   # Final creatives running in ads
│   ├── images/drafts/     # Work-in-progress variations
│   └── video/             # Video scripts and storyboards
├── campaigns/             # Campaign documentation
│   ├── active/            # Currently running
│   └── archive/           # Paused/completed
├── analytics/             # Performance tracking
│   ├── weekly-reports/    # Weekly performance snapshots
│   └── test-log.md        # A/B test tracker
├── landing-pages/src/     # Built landing page code
└── reference/             # Product info, audience profiles, compliance
```

**Core principle:** Local files are for processing. Deliverables go to cloud services where the user can access them. Everything in `.tmp/` is disposable.

---

## Workflow Rules

1. **ALWAYS** check `runbook.md` for the current phase and next task
2. **ALWAYS** read `skills/marketing-campaign-build/SKILL.md` before starting any campaign work
3. **ALWAYS** follow the build sequence -- do not skip phases or quality gates
3. **ALWAYS** check `workflows/` for the relevant SOP before executing a step
4. **ALWAYS** check `tools/` before building a new script
5. **ALWAYS** use the context flow rules from the skill -- compress context, don't dump full docs
6. **NEVER** create or overwrite workflows without asking
7. **NEVER** run paid API calls without checking with the user first
8. **NEVER** store secrets outside `.env`
9. When pulling ad platform data, save raw insights to `analytics/` for historical tracking
10. When output feels generic or hedged, run the next skill FRESH without chained context

## Meta Ads Safety Rules

**CRITICAL -- These rules override all other instructions:**

1. **NEVER activate/publish campaigns.** All campaigns, ad sets, and ads MUST be created with `status: PAUSED`. The user will manually activate them in Ads Manager after review.
2. **NEVER change a campaign/ad set/ad status to ACTIVE.** Do not use `update_campaign`, `update_adset`, or `update_ad` to set `status: ACTIVE` under any circumstances.
3. **NEVER delete campaigns, ad sets, or ads** without explicit user confirmation first.
4. **NEVER modify budgets on live campaigns.** If a campaign is ACTIVE, do not change its budget -- ask the user.
5. **Always confirm targeting and strategy with the user** before creating campaigns or ad sets via the API.
6. **Read-only operations are always safe:** Fetching insights, listing campaigns, searching interests, estimating audiences -- these are fine without asking.
7. When creating anything (campaigns, ad sets, ads, creatives), always document the IDs in `reference/meta-ads-campaign-ids.md` immediately after creation.

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
