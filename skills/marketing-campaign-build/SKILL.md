# Marketing Campaign Build

Build a complete marketing campaign from audit to optimization. This skill orchestrates all Vibe Marketing, Vibe Creative, and Core skills in the correct sequence with the right context flowing between them.

**When to use:** Any marketing campaign work in this project. Read this skill before starting.

---

## The Build Sequence

24 steps across 6 phases. Steps marked `(if needed)` are conditional -- skip them if the funnel doesn't require it. Steps marked `(skip if recon done)` can be skipped if Phase 0 was completed during initial setup. Steps are sequential within a phase. Do not skip phases.

---

### PHASE 0: RECON
*Gather competitive intelligence and site analysis. Usually completed during `new-client-setup` — skip if already done.*

| Step | Invoke | What to Do | Output |
|------|--------|------------|--------|
| 0a *(skip if recon done)* | `perplexity` MCP | Use `perplexity_research` to research direct competitors (pricing, positioning, offer structure, strengths/weaknesses). Use `perplexity_search` for market landscape (size, trends, demographics). Use `perplexity_research` for industry ad compliance rules (FTC, Meta policies, industry-specific restrictions). | `strategy/audit/competitor-research.md`, `reference/compliance-notes.md` |
| 0b *(skip if recon done)* | `playwright` MCP | Use `browser_navigate` → `browser_take_screenshot` → `browser_snapshot` to capture client's website and funnel pages. Document: headline, CTA, forms, social proof, above-fold content, page structure. Repeat for top 3-5 competitor sites identified in Step 0a. | `strategy/site-intel/client-site-analysis.md`, `strategy/site-intel/competitor-sites.md` |

**CHECK:** If `strategy/audit/competitor-research.md` and `strategy/site-intel/` files already exist from setup, skip to Phase 1.

---

### PHASE 1: AUDIT
*Understand what exists before changing anything.*

| Step | Invoke | What to Do | Output |
|------|--------|------------|--------|
| 1 | `agent-browser` | Open each current landing page URL. Take full-page screenshots (`screenshot --full`). Snapshot interactive elements (`snapshot -i`). Document: headline, CTA, forms, social proof, above-the-fold content, mobile responsiveness. Identify CRO gaps. Use Perplexity recon and Playwright site-intel from Phase 0 as additional context. | `strategy/audit/landing-page-audit.md` |
| 2 | `meta-ads` MCP | Pull campaigns (`get_campaigns`), ad sets (`get_adsets`), ads + insights (`get_ads`, `get_insights`), creatives (`get_ad_creatives`, `get_ad_image`). Analyze: structure, budget allocation, targeting, ROAS by level, creative performance, frequency/fatigue. | `strategy/audit/account-audit.md` |
| 3 | `agent-browser` | Browse Facebook Ad Library for competitors. Screenshot active ads. Visit competitor landing pages. Cross-reference with Perplexity competitor research from Phase 0. Document copy patterns, visual styles, offer structures, funnel types. Identify differentiation gaps. | `strategy/audit/competitor-audit.md` |
| 4 | Manual analysis | Map the current funnel: Ad -> Landing Page -> Conversion Event. Identify drop-off points and friction. | `strategy/funnel-map.md` |

**GATE: Present audit findings to user. Do not proceed to Phase 2 until user reviews and approves.**

---

### PHASE 2: STRATEGY
*Build the foundation all creative work stands on.*

| Step | Invoke | What to Do | Output |
|------|--------|------------|--------|
| 5 | `brainstorming` | Explore strategic direction before locking anything. Present 2-3 approaches with trade-offs. Get user input on direction. | -- |
| 6 | `brand-voice` | Run in Extract mode (if existing content is strong) or Build mode (if pivoting). Produce voice profile: tone spectrum, vocabulary guide, personality traits, example snippets. | `strategy/brand-voice.md` |
| 7 | `positioning-angles` | Feed product info + competitor audit + audience context. Generate 3-5 distinct angles (contrarian, unique mechanism, transformation, enemy, speed/ease, specificity, social proof, risk reversal). Assess market sophistication level. | `strategy/positioning-angles.md` |
| 8 | `lead-magnet` *(if needed)* | If funnel includes a lead capture step before purchase. Feed selected angle + audience pain points. Generate 3-5 lead magnet concepts with hooks, formats, and bridges to paid offer. | `creative/lead-magnets/` |
| 9 | `meta-ads` MCP | Audience research: `search_interests`, `search_behaviors`, `search_demographics`, `estimate_audience_size`. Define 2-3 target segments. | `reference/audience-profiles.md` |

**GATE: Present voice profile + positioning angles to user. User selects primary and secondary angles. Do not write any copy until voice + angles are approved.**

---

### PHASE 3: CREATIVE
*Produce ads, copy, and content.*

| Step | Invoke | Context to Pass | What to Do | Output |
|------|--------|----------------|------------|--------|
| 10 | `ai-creative-strategist` | Winning angle (1-2 sentences) + audience summary | Run 5-phase process: Discover -> Research -> Preview -> Feedback -> Brief. Generate 2-3 visual direction previews. Get user approval on direction. Output creative brief with approved direction, proven prompt template, and asset requirements. | `creative/briefs/` |
| 11 | `direct-response-copy` | Voice summary (3 sentences) + winning angle (1-2 sentences) + audience segment | Ad copy: 3 primary text variations (short/medium/long) per angle, 5 headline options, 3 descriptions, CTA recommendation. Follow Ad Copy Document Format (see CLAUDE.md conventions). | `creative/ad-copy/` |
| 12 | `direct-response-copy` | Voice summary (3 sentences) + winning angle (1-2 sentences) + landing page structure | Landing page copy: hero headline + subheadline, above-fold body, feature/benefit sections, social proof, FAQ, CTA copy, objection handling. Must message-match the ad angle. | `creative/landing-pages/` |
| 13 | `ai-social-graphics` | Creative brief (approved direction + prompt template) | Facebook ad images. Generate 3-5 variations per angle. Specs: 1:1 (feed), 1.91:1 (feed), 9:16 (stories/reels). Save to drafts -> user approves -> move to approved. | `assets/images/` |
| 14 | `ai-product-photo` *(if needed)* | Creative brief + product details | Product shots for ads. Style aligned with approved visual direction. | `assets/images/` |
| 15 | `ai-product-video` *(if needed)* | Creative brief + winning angle | Video ad scripts and storyboards. Account for sound-off viewing (captions, visual storytelling). | `assets/video/` |
| 16 | `ai-talking-head` *(if needed)* | Creative brief + voice profile summary | Founder/testimonial talking head video content. Script with hook, body, CTA structure. | `assets/video/` |
| 17 | `email-sequences` *(if needed)* | Voice summary + lead magnet hook + winning angle | Welcome -> nurture -> conversion sequence. Subject lines, preview text, full copy, timing. | `creative/email/` |

**GATE: Present all creative (copy + visuals + video scripts) to user. User approves or requests revisions before build phase.**

---

### PHASE 4: BUILD
*Implement landing pages and web experiences.*

| Step | Invoke | What to Do | Output |
|------|--------|------------|--------|
| 18 | `brainstorming` | Explore 2-3 landing page design directions. Consider CRO best practices, mobile-first (Facebook traffic is mostly mobile), and message match with ads. Get user approval on direction. | -- |
| 19 | `frontend-design` + `ghl-forms` | **Default: Standalone HTML** — single-file HTML page with GHL form embedded via iframe. Use `ghl-forms` skill for seamless form integration (loading spinner, height auto-resize, background matching, responsive min-heights). Distinctive design (no generic AI aesthetic). Mobile-first, fast loading. Clear visual hierarchy -> CTA. Must include: hero matching ad copy, social proof above fold, benefits, objection handling, multiple CTAs, trust signals, compliance disclaimers in footer. **GHL-native version (on request only):** If user explicitly asks for a "GHL version" or "GHL landing page," also build a full-page version designed for GHL's funnel builder that takes up the entire viewport and is hosted on GHL's subdomain. Do NOT build GHL-native version unless specifically requested. | `landing-pages/src/` |
| 20 | `agent-browser` | Test built pages. Verify rendering, check mobile view, confirm all CTAs work, check page load speed. | -- |

**GATE: User reviews built pages. Approves or requests changes before campaign setup.**

---

### PHASE 5: OPTIMIZE
*Weekly cycle: measure, learn, iterate.*

| Step | Invoke | What to Do | Output |
|------|--------|------------|--------|
| 21 | `meta-ads` MCP | Pull this week's performance: campaign/adset/ad level spend, ROAS, conversions, CPA. Compare to previous week + baseline. Identify winners (scale candidates) and losers (pause candidates). | `analytics/weekly-reports/week-YYYY-MM-DD.md` |
| 22 | `direct-response-copy` + `ai-social-graphics` | Iterate: write new copy variations on winning angles, create new image variations. Update test log with hypothesis, result, learning. | `analytics/test-log.md`, `creative/ad-copy/`, `assets/images/` |

*Repeat Steps 21-22 weekly. If all tests are losing, go back to Step 7 (positioning-angles) and find new angles.*

---

## Context Flow Rules

How much context to pass between skills. More is NOT always better -- over-contexted skills produce generic, hedged output.

### Three Context Tiers

| Tier | What to Pass | When |
|------|-------------|------|
| **Tier 1: Essential** (always) | Brand voice summary (3 sentences), winning angle (1-2 sentences), primary keyword/topic | Every copy and creative skill |
| **Tier 2: Helpful** (if relevant) | Audience pain points (bullets only), competitor gaps (summary), specific constraints | When it adds focus |
| **Tier 3: Skip** | Full research docs, complete audience profiles, exhaustive competitor analysis | Almost never pass full docs |

### Specific Handoff Rules

| From | To | Pass This | NOT This |
|------|-----|-----------|----------|
| `brand-voice` | All copy skills | 3-sentence voice summary | Full profile document |
| `positioning-angles` | `direct-response-copy` | Winning angle (1-2 sentences) | All 5 angle options |
| `positioning-angles` | `lead-magnet` | Angle + pain points only | Full angles doc |
| `ai-creative-strategist` | `ai-social-graphics` | Approved direction + proven prompt template | Full brief |
| `ai-creative-strategist` | `ai-product-photo` | Approved direction + style characteristics | Full brief |
| `keyword-research` | `direct-response-copy` | Main keyword only | Full cluster spreadsheet |
| `lead-magnet` | `email-sequences` | Hook + format | Full concept doc |

### When to Run Fresh (No Chained Context)
- Output from previous skill feels generic, hedged, or committee-sounding
- You want bold, opinionated copy
- Previous output was mediocre
- Testing a completely different angle
- Copy needs to feel human, not over-researched

**The test:** If adding more context would make the output try to please all inputs instead of being sharp and specific -- run fresh.

---

## Handoff Protocol

Use this format every time you transition between skills:

```markdown
## Handoff -> [Skill Name]

**Goal:** [User's stated goal for this phase]
**Current state:** [What has been completed so far]
**This skill's job:** [Specific outcome needed from this skill]

**Inputs available:**
- Brand voice: [yes/no -- if yes, include 3-sentence summary]
- Positioning: [yes/no -- if yes, include winning angle in 1-2 sentences]
- Creative direction: [yes/no -- if yes, include approved direction name]
- Audience: [yes/no -- if yes, include primary segment in 1 sentence]

**After this skill:** [What comes next in the sequence]
```

---

## Quality Gates

Four mandatory checkpoints. Never skip these.

| Gate | After | What User Reviews | Must Have Before Proceeding |
|------|-------|-------------------|---------------------------|
| **Gate 1** | Phase 1 (Audit) | Audit findings, funnel map, CRO opportunities | User confirms understanding of current state |
| **Gate 2** | Phase 2 (Strategy) | Voice profile, positioning angles | User selects primary + secondary angles |
| **Gate 3** | Phase 3 (Creative) | Ad copy, landing page copy, ad images, video scripts | User approves creative for production |
| **Gate 4** | Phase 4 (Build) | Built landing pages | User approves pages for deployment |

Phase 5 (Optimize) runs in a weekly loop and doesn't have a gate -- but major strategic pivots (new angles, new funnel structure) should be discussed with the user before executing.

---

## Quick Reference

```
RECON:    perplexity (competitors + compliance) -> playwright (client site + competitor sites) [skip if done during setup]
AUDIT:    agent-browser -> meta-ads -> agent-browser -> funnel map -> GATE 1
STRATEGY: brainstorming -> brand-voice -> positioning-angles -> [lead-magnet] -> meta-ads -> GATE 2
CREATIVE: ai-creative-strategist -> direct-response-copy (ads) -> direct-response-copy (pages) -> ai-social-graphics -> [ai-product-photo] -> [ai-product-video] -> [ai-talking-head] -> [email-sequences] -> GATE 3
BUILD:    brainstorming -> frontend-design -> agent-browser/playwright -> GATE 4
OPTIMIZE: meta-ads -> iterate (weekly loop)
```

**Context shortcut:** Voice (3 sentences) + Angle (1-2 sentences) = the minimum context every creative/copy skill needs.

**If stuck:** Go back one phase. If creative isn't working, revisit angles. If angles aren't working, revisit the audit.
