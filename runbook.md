# Kilo — Client Runbook

**Created:** 2026-02-20
**Status:** Phase 0 COMPLETE — Ready for Phase 1

This is the master task list for the Kilo marketing engagement. Work through each phase in order. Do not skip phases or quality gates.

---

## Phase 0: RECON
*Gather competitive intelligence and site analysis before any strategy work.*

**Tools:** Firecrawl CLI (search + scrape), Playwright MCP (screenshots + snapshots)
*Note: Perplexity API key expired during setup — firecrawl search used as replacement for all research queries.*

| # | Task | Tool | Status | Output |
|---|------|------|--------|--------|
| 0.1 | Research direct competitors — pricing, positioning, offer structure | Firecrawl search + Firecrawl scrape (comparison pages) | ☑ | `strategy/audit/competitor-research.md` |
| 0.2 | Research market landscape — market size, trends, audience demographics | Firecrawl search | ☑ | `strategy/audit/competitor-research.md` |
| 0.3 | Research industry compliance — FTC, Meta policies, auto-renewal rules | Firecrawl search | ☑ | `reference/compliance-notes.md` |
| 0.4 | Screenshot & analyze client's website — homepage, product pages, pricing | Playwright + Firecrawl scrape | ☑ | `strategy/site-intel/client-site-analysis.md` + screenshots in `assets/images/screenshots/` |
| 0.5 | Map all site URLs + deep content extraction | Firecrawl map + batch scrape | ☑ | `strategy/site-intel/sitemap-crawled.md` + `.firecrawl/` |
| 0.6 | Compile recon findings — competitive advantages, gaps, opportunities | Synthesis | ☑ | `strategy/audit/recon-summary.md` |

**Perplexity Query Templates:**
```
0.1: "[Client industry] online courses/services competitors pricing comparison 2026"
0.1: "Who are the top [number] [client industry] [product type] providers online?"
0.2: "[Client industry] market size trends target audience demographics"
0.3: "[Client industry] Facebook Meta advertising rules compliance restrictions"
0.3: "FTC advertising guidelines for [client industry] testimonials claims"
```

**Playwright Capture Checklist (per site):**
- Full-page screenshot
- Above-the-fold screenshot
- Interactive element snapshot (forms, quizzes, CTAs)
- Note: headline, subheadline, CTA text, social proof, trust signals, offer structure

---

## Phase 1: DIAGNOSE
*Use the orchestrator to determine the right skill sequence for this client.*

**Skill:** `orchestrator` (Vibe Marketing)

| # | Task | Status |
|---|------|--------|
| 1.1 | Run the `orchestrator` skill — answer qualifying questions (goal, existing assets, timeline) | ☐ |
| 1.2 | Review orchestrator output — recommended skill sequence and state tracker | ☐ |
| 1.3 | **GATE: User approves direction and skill sequence before proceeding** | ☐ |

**Orchestrator Inputs to Prepare:**
- Client's goal (leads, sales, awareness, launch)
- What marketing assets already exist (voice, positioning, content, landing pages, email list)
- Timeline (immediate, this week, long-term build)
- Recon findings from Phase 0 (competitor gaps, opportunities)

---

## Phase 2: AUDIT
*Understand what the client currently has before changing anything.*

**Skill:** `marketing-campaign-build` — Steps 1-4

| # | Task | Skill Step | Status | Output |
|---|------|-----------|--------|--------|
| 2.1 | Audit current landing pages (screenshots + CRO analysis) | Step 1 — `agent-browser` | ☐ | `strategy/audit/landing-page-audit.md` |
| 2.2 | Pull current ad account performance (if Meta Ads exist) | Step 2 — `meta-ads` MCP | ☐ | `strategy/audit/account-audit.md` |
| 2.3 | Audit competitor ads (Facebook Ad Library) | Step 3 — `agent-browser` | ☐ | `strategy/audit/competitor-audit.md` |
| 2.4 | Map current funnel (ad → page → conversion) | Step 4 — Manual | ☐ | `strategy/funnel-map.md` |
| 2.5 | **GATE 1: Present audit findings to user. User confirms understanding.** | | ☐ | |

---

## Phase 3: STRATEGY
*Build the foundation all creative work stands on.*

**Skill:** `marketing-campaign-build` — Steps 5-9

| # | Task | Skill Step | Status | Output |
|---|------|-----------|--------|--------|
| 3.1 | Strategic brainstorm — explore 2-3 approaches with trade-offs | Step 5 — `brainstorming` | ☐ | — |
| 3.2 | Define brand voice (extract or build mode) | Step 6 — `brand-voice` | ☐ | `strategy/brand-voice.md` |
| 3.3 | Find positioning angles (3-5 distinct angles) | Step 7 — `positioning-angles` | ☐ | `strategy/positioning-angles.md` |
| 3.4 | Create lead magnet concepts (if funnel requires it) | Step 8 — `lead-magnet` | ☐ | `creative/lead-magnets/` |
| 3.5 | Audience research — interests, behaviors, demographics, segment sizing | Step 9 — `meta-ads` MCP | ☐ | `reference/audience-profiles.md` |
| 3.6 | **GATE 2: Present voice + angles to user. User selects primary/secondary angles.** | | ☐ | |

---

## Phase 4: CREATIVE
*Produce ads, copy, and content.*

**Skill:** `marketing-campaign-build` — Steps 10-17

| # | Task | Skill Step | Status | Output |
|---|------|-----------|--------|--------|
| 4.1 | Creative direction + briefs (visual direction previews) | Step 10 — `ai-creative-strategist` | ☐ | `creative/briefs/` |
| 4.2 | Ad copy — primary text, headlines, descriptions per angle | Step 11 — `direct-response-copy` | ☐ | `creative/ad-copy/` |
| 4.3 | Landing page copy — hero, benefits, social proof, FAQ, CTAs | Step 12 — `direct-response-copy` | ☐ | `creative/landing-pages/` |
| 4.4 | Ad images — 3-5 variations per angle (feed, stories, reels) | Step 13 — `ai-social-graphics` | ☐ | `assets/images/` |
| 4.5 | Product photography (if needed) | Step 14 — `ai-product-photo` | ☐ | `assets/images/` |
| 4.6 | Video ad scripts (if needed) | Step 15 — `ai-product-video` | ☐ | `assets/video/` |
| 4.7 | Talking head scripts (if needed) | Step 16 — `ai-talking-head` | ☐ | `assets/video/` |
| 4.8 | Email sequences (if needed) | Step 17 — `email-sequences` | ☐ | `creative/email/` |
| 4.9 | **GATE 3: Present all creative to user. User approves for production.** | | ☐ | |

---

## Phase 5: BUILD
*Implement landing pages and web experiences.*

**Skill:** `marketing-campaign-build` — Steps 18-20

| # | Task | Skill Step | Status | Output |
|---|------|-----------|--------|--------|
| 5.1 | Explore landing page design direction | Step 18 — `brainstorming` | ☐ | — |
| 5.2 | Build landing pages (mobile-first, distinctive design) | Step 19 — `frontend-design` | ☐ | `landing-pages/src/` |
| 5.3 | Test built pages (rendering, mobile, CTAs, load speed) | Step 20 — `agent-browser` / `playwright` | ☐ | — |
| 5.4 | **GATE 4: User reviews built pages. Approves for deployment.** | | ☐ | |

---

## Phase 6: OPTIMIZE
*Weekly cycle: measure, learn, iterate.*

**Skill:** `marketing-campaign-build` — Steps 21-22

| # | Task | Skill Step | Frequency | Output |
|---|------|-----------|-----------|--------|
| 6.1 | Pull weekly performance data | Step 21 — `meta-ads` MCP | Weekly | `analytics/weekly-reports/` |
| 6.2 | Iterate — new copy/creative on winning angles | Step 22 — `direct-response-copy` + `ai-social-graphics` | Weekly | `analytics/test-log.md` |

*Repeat weekly. If all tests lose, go back to Phase 3 (positioning-angles).*

---

## Skill Quick Reference

| Skill | Source | Used In |
|-------|--------|---------|
| `orchestrator` | Vibe Marketing | Phase 1 |
| `marketing-campaign-build` | Project-local (`skills/`) | Phases 2-6 |
| `agent-browser` | Core | Phases 2, 5 |
| `brainstorming` | Core | Phases 3, 5 |
| `brand-voice` | Vibe Marketing | Phase 3 |
| `positioning-angles` | Vibe Marketing | Phase 3 |
| `lead-magnet` | Vibe Marketing | Phase 3 |
| `direct-response-copy` | Vibe Marketing | Phases 4, 6 |
| `ai-creative-strategist` | Vibe Creative | Phase 4 |
| `ai-social-graphics` | Vibe Creative | Phases 4, 6 |
| `ai-product-photo` | Vibe Creative | Phase 4 |
| `ai-product-video` | Vibe Creative | Phase 4 |
| `ai-talking-head` | Vibe Creative | Phase 4 |
| `email-sequences` | Vibe Marketing | Phase 4 |
| `frontend-design` | Core | Phase 5 |
| `perplexity` MCP | MCP Server | Phase 0 |
| `playwright` MCP | MCP Server | Phases 0, 5 |
| `meta-ads` MCP | MCP Server | Phases 2, 3, 6 |
| `ghl-mcp` MCP | MCP Server | As needed (CRM clients) |
