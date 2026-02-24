# WordPress Design Specs — Kilo Landing Pages

**Date:** 2026-02-24
**Prepared for:** Kilo (usekilo.com) — WordPress + Elementor implementation
**Reference prototypes:** `landing-pages/src/*.html`

These specs document the design system, layout structure, and section-by-section details for recreating 5 standalone HTML prototypes in WordPress/Elementor. Open each HTML file in a browser alongside this document for visual reference.

---

## Global Design System

### Brand Colors

| Token | Hex | Usage |
|-------|-----|-------|
| Navy (Primary) | `#0A1C38` | Backgrounds, text, primary buttons |
| Cyan (Accent) | `#1EB1F9` | CTAs, links, highlights, badges |
| Mint/Teal | `#20F2CA` / `#14B8A6` | Tertiary accents, check icons, secondary highlights |
| White | `#FFFFFF` | Light backgrounds, card surfaces |
| Off-White | `#F8FAFC` | Alternate section backgrounds |
| Gray-200 | `#E2E8F0` | Borders, dividers |
| Gray-400 | `#94A3B8` | Muted text, labels |
| Gray-500 | `#64748B` | Secondary body text |

### Typography

Each page uses a slightly different heading/body pairing for distinctiveness. All are available on Google Fonts.

| Page | Headings | Body | Monospace (stats) |
|------|----------|------|-------------------|
| Book Demo | Outfit (600-800) | DM Sans (400-600) | — |
| Pricing | Instrument Serif (italic accent) | DM Sans (400-600) | — |
| Gym Websites | Outfit (600-800) | DM Sans (400-600) | — |
| GLM/ROI | Inter (600-900) | Inter (400-500) | JetBrains Mono (stats) |
| Switch to Kilo | Sora (600-800) | Nunito Sans (400-600) | — |

**Type Scale (approximate):**
- H1: 48-56px desktop / 32-36px mobile
- H2: 36-42px desktop / 28-32px mobile
- H3: 24-28px desktop / 20-24px mobile
- Body: 16-18px
- Small/caption: 13-14px
- Eyebrow/label: 13px, uppercase, 0.1-0.15em letter-spacing, font-weight 600

### Spacing & Layout

- **Max container width:** 1200px (1280px on Switch page)
- **Section padding:** `clamp(64px, 8vw, 120px)` vertical, 24px horizontal
- **Card border-radius:** 12-16px
- **Button border-radius:** 8-12px (some pages use pill/50px for CTAs)
- **Standard gap between elements:** 16-24px
- **Section background alternation:** White → Off-white → White → Navy (dark)

### Shared UI Patterns

- **Fixed header:** Sticky nav with `backdrop-filter: blur(12px)`, gains subtle shadow on scroll
- **Scroll reveal animations:** Elements fade up 32px with 0.7s cubic-bezier transition on viewport entry
- **FAQ accordion:** Click to expand/collapse, one open at a time, chevron/plus icon rotates
- **Trust badges:** Row of 5 award badges (Capterra Best Value 2025, Software Advice Front Runners 2025, GetApp Category Leaders 2025, Capterra Ease of Use 2025, Capterra Shortlist 2025)
- **Buttons:** Two styles — filled (navy bg, white text) and outline (transparent bg, navy border). Cyan filled for primary CTAs.
- **Card shadows:** `0 4px 16px rgba(10, 28, 56, 0.08)` base, deepens on hover

### Responsive Breakpoints

| Breakpoint | Behavior |
|------------|----------|
| > 1024px | Full desktop layout |
| 768-1024px | Tablet — grids collapse to 2 columns |
| < 768px | Mobile — single column, stacked layout |
| < 480px | Small mobile — reduced padding/font sizes |

---

## Page 1: Book a Demo (`book-demo.html`)

### Layout
**Split-screen design** — two equal columns side by side.
- Left panel: Dark navy background with content
- Right panel: White background with calendar widget
- Mobile: Stacks vertically (left panel on top, calendar below)

### Left Panel (Dark Navy)

**Section order:**
1. **Kilo logo** — SVG, white text on navy
2. **Hero headline:** "Book a Free Demo" with "Free Demo" in cyan gradient text
3. **Subtitle:** "See how 1,000+ coaching gyms simplify management, marketing, and growth with one platform."
4. **Note:** "We look forward to connecting! Here's what to expect:"
5. **What to Expect checklist** (4 items with cyan checkmark icons):
   - "Personalized walkthrough of Kilo's platform"
   - "Discussion of your gym's specific needs and goals"
   - "Live Q&A — ask us anything, no pressure"
   - "Custom recommendations for your gym type"
6. **3 testimonial cards** (dark card with subtle border):
   - Charlie Goode, CrossFit Watford: "After switching... net gain of 33 members"
   - Lindsey Barber, PB&J Functional Fitness: "We've had 210% membership growth since using GLM"
   - Eric Cruz, Croga CrossFit: "Saves me roughly 6 hours per week on admin tasks"
7. **Trust badge row** — 5 award pills (rounded, semi-transparent bg on navy)
8. **Bottom line:** "1,000+ coaching gyms trust Kilo" with cyan "Learn more →" link

### Right Panel (White)

**Calendar widget** (mock — will be replaced by actual Calendly/booking embed):
1. **Badge:** Kilo logo + "Kilo"
2. **Header:** "Free Demo" with "FREE" badge, "30 min" duration, "Zoom" platform
3. **Month selector:** ← February 2026 →
4. **Calendar grid:** 7-column day grid
   - Past dates: grayed out
   - Today: cyan ring
   - Selected date: navy filled
   - Available dates: small mint dot indicator
5. **Time slots:** 3-column grid of available times (e.g., "9:00 AM", "10:00 AM", etc.)
   - Selected: navy fill with white text
   - Available: white with navy border
6. **"Confirm Booking" button** — Full-width navy
7. **Note:** "No credit card required. Cancel or reschedule anytime."
8. **Timezone selector** at bottom

**Elementor implementation note:** Replace the mock calendar with an embedded Calendly or CRM booking widget. Keep the surrounding content (testimonials, what to expect) intact. The right panel should use a sticky position so the calendar stays in view while scrolling left panel content on desktop.

---

## Page 2: Pricing (`pricing.html`)

### Section Order

1. **Fixed Header**
   - Logo + nav links (Products, Pricing, Customers, Resources, Blog, Contact)
   - "Book a Demo" cyan CTA button
   - Mobile: hamburger menu

2. **Compact Hero** (minimal height — prices must be visible above fold)
   - H1: "Simple Pricing. *Serious Results.*" — "Serious Results" in Instrument Serif italic with cyan color
   - Subtitle: "All the tools you need to manage your gym, attract new clients, and grow your business. No hidden fees."
   - No large decorative elements — keep hero SHORT

3. **4 Pricing Cards** (horizontal row, equal height)
   - **Gym Websites** — $175/mo
     - 6 features with teal check icons
     - "Book a Demo" outline button
   - **GMS** — $150/mo
     - 6 features with teal check icons
     - "Book a Demo" outline button
   - **GLM** — $375/mo
     - Label: "Everything in Websites plus"
     - 6 features with teal check icons
     - Social proof: "77% say it pays for itself in 3 months"
     - "Book a Demo" outline button
   - **Bundle (GLM + GMS)** — $450/mo — **HIGHLIGHTED**
     - "Best Value" cyan badge at top
     - Cyan left border accent
     - Savings callout: "$75/month savings" / "$900/year" in amber/yellow badge
     - 6 features with teal check icons
     - "Book a Demo" — FILLED navy button (primary CTA)

   **Grid:** 4 columns desktop → 2 columns tablet → 1 column mobile

4. **Feature Comparison Matrix** (full-width table)
   - 4 columns: Websites | GMS | GLM | Bundle
   - 4 categories: Website Features, Marketing Features, Management Features, Support
   - 25+ feature rows with checkmarks (✓) and dashes (—)
   - Bundle column: subtle cyan tint background
   - Mobile: horizontally scrollable with scroll hint

   **Elementor note:** Use a responsive table widget or custom HTML table. The horizontal scroll on mobile is essential — don't try to stack this vertically.

5. **ROI Section** (dark navy background)
   - H2: "The ROI That Pays for Itself"
   - 3 explanation cards (one per tier): how each product pays for itself
   - ROI table: rows for 2, 6, 12, 24 members/year showing return percentages
   - Highlighted row: 12 members/year = 860% ROI
   - "TYPICAL" badge on highlighted row

6. **Testimonials** (3 cards, light background)
   - 5-star rating
   - Quote text
   - Author name, gym name, avatar initials
   - Cards: Lindsey Barber, Chris Lomen, Andrew Hiller

7. **FAQ Accordion** (10 questions)
   - Questions include: contract length, switching ease, GLM capabilities, custom domain, support, bundle value, free trial, payment methods, ROI guarantee, annual billing
   - Plus icon rotates to X when expanded

8. **Final CTA** (gradient background)
   - "Ready to grow your gym?"
   - Navy CTA button with arrow

9. **Footer** (4-column grid)
   - Brand column: logo, tagline
   - Company: About, Careers, Contact, Partners
   - Resources: Blog, Help Center, API Docs, System Status
   - Legal: Privacy, Terms, Cookie Policy
   - Address: 14255 U.S. Hwy 1, Suite 281, Juno Beach, FL 33408
   - Social: Facebook, Instagram, LinkedIn, YouTube
   - Award badges row

---

## Page 3: Done-For-You Gym Websites (`gym-websites.html`)

### Primary Angle: Done-For-You (#1)

### Section Order

1. **Fixed Header** — Same pattern as Pricing page

2. **Hero**
   - Eyebrow: "GYM WEBSITES" (cyan, uppercase, letter-spaced)
   - H1: "Your Gym Website." (line break) "Built For You. *Live in 9 Days.*" — "Live in 9 Days" in cyan gradient
   - Subtitle: "Stop DIY-ing your gym's online presence. Kilo builds you a custom, lead-generating website — and handles everything from design to maintenance."
   - Dual CTAs: "See How It Works" (navy filled) + "Book a Free Demo" (outline)
   - Right visual: Browser mockup frame containing a gym website preview + floating phone mockup
   - Phone mockup has subtle bobbing CSS animation

3. **Stats Bar** (floating card overlapping hero/content boundary)
   - 4 stats in a row: 1,000+ Gyms | 18% More Leads | 61% Lead Increase | 9 Days Live
   - Numbers animate/count up on scroll into view
   - Background: white card with subtle shadow, slightly offset upward from section below

4. **How It Works** (3 steps)
   - Step 1: "Tell Us About Your Gym" — numbered circle with connecting gradient line
   - Step 2: "We Build Your Website"
   - Step 3: "Launch & Grow"
   - Each step has an icon area and description text
   - Layout: horizontal with connecting line (vertical on mobile)

5. **Features Grid** (6 cards in 2x3 grid)
   - Custom Design, Lead Capture Forms, Mobile Responsive, SEO Optimized, Blog Integration, Ongoing Updates
   - Each card: colored icon, title, description
   - Hover: gradient top-border reveals, slight lift
   - Cards use alternating accent colors (cyan, mint, navy)

6. **Comparison Table** (3 columns)
   - DIY (Wix/Squarespace) vs Local Provider vs Kilo
   - "RECOMMENDED" badge on Kilo column
   - Rows: Time to Launch, Monthly Cost, Custom Design, Lead Capture, SEO, Mobile-Optimized, Ongoing Support, Updates Included
   - ✓/✗/Partial icons per cell
   - Detail annotations under some cells

7. **Testimonials** (3 cards)
   - Bethany Ream, Lindsey Barber, Russell Francis
   - 5-star ratings, quote text, avatar initials

8. **Pricing Card** (dark navy centered card)
   - $175/mo prominently displayed
   - 7 feature checkmarks in 2-column grid
   - "Book a Free Demo" cyan CTA

9. **FAQ Accordion** (6 items)
   - Questions about: customization, timeline, own domain, SEO, content updates, contract

10. **Final CTA** (dark navy section)
    - "Get Started Today"
    - Cyan CTA button

11. **Trust Badges** — 5 award badges

12. **Footer** — 4-column layout matching other pages

---

## Page 4: Gym Lead Machine / ROI Calculator (`gym-lead-machine.html`)

### Primary Angle: ROI Math (#3) + Done-For-You (#1)

### Section Order

1. **Fixed Header** — Same pattern

2. **Hero**
   - Eyebrow badge: pulsing cyan dot + "GYM LEAD MACHINE"
   - H1: "Close *2 Extra Members.* GLM Has Already Paid for Itself." — "2 Extra Members" in cyan
   - Subtitle: "Kilo's Gym Lead Machine generates leads, books appointments, and grows your gym on autopilot. 77% of gym owners say it pays for itself in 3 months."
   - Dual CTAs: "See the ROI" (navy, scrolls to ROI section) + "Book a Free Demo" (outline)
   - Right visual: Dashboard mockup with bar charts + floating metric cards ("+35.3 Leads/mo" and "$43,200 Revenue") with gentle bob animation

3. **ROI Calculator Section** (elevated, near hero — THIS IS THE KEY DIFFERENTIATOR)
   - **Left column:** 3-step math breakdown
     - Step 1: "Your average member pays $___/month" (show $150 default)
     - Step 2: "Average member stays ___ months" (show 12 default)
     - Step 3: "Lifetime value = $1,800"
     - Bottom: "GLM costs $375/month. Close 2 extra members per year and it's already paid for itself."
   - **Right column:** ROI table card
     - Dark navy header: "Your GLM Return on Investment"
     - 3 rows: 2 members/yr = ~60% ROI, 12/yr = 860% ROI, 24/yr = 1,820% ROI
     - Highlighted row: 860% with cyan left border + "TYPICAL" badge
     - CTA: "Book a Demo to See Your Numbers"

   **Elementor note:** Consider making this an interactive calculator where gym owners can input their own membership price and retention — the ROI updates live. The HTML prototype shows static numbers but the concept supports interactivity.

4. **Stats Bar** (dark navy background)
   - 4 stats: 210% More Memberships | 35.3 More Leads/mo | 384 Hours Saved/yr | 77% Pays for Itself
   - JetBrains Mono font for numbers
   - Animated counter on scroll

5. **How GLM Works** (6 features, alternating left-right layout)
   - 01: Lead-Generating Website
   - 02: Automated Lead Nurture
   - 03: Smart Appointment Booking
   - 04: Performance Dashboard
   - 05: Social Media & Review Tools
   - 06: Dedicated Support Team
   - Each: numbered label, title, description, placeholder visual area
   - Alternating: image left/text right, then text left/image right

6. **Problem/Solution Table** (4 rows)
   - Without GLM (✗) vs With GLM (✓)
   - Rows: Lead follow-up, Booking, Marketing tracking, Time management
   - Split header: navy left, white right

7. **Testimonials** (4 cards in 2x2 grid, dark navy background)
   - Star ratings, quotes, author names with gym names

8. **Pricing Card** (centered, gradient top border)
   - $375/month in large mono type
   - Feature list
   - Dual CTAs

9. **FAQ Accordion** (8 items)

10. **Final CTA** (dark navy with radial glow)
    - "Stop Losing Leads. Start Growing."
    - Cyan CTA

11. **Trust Badges** (5 inline badges with SVG icons)

12. **Footer**

---

## Page 5: Switch to Kilo (`switch-to-kilo.html`)

### Primary Angle: The Switch (#2) + Time Recapture (#4)

### Section Order

1. **Fixed Header** — Same pattern

2. **Hero** (dark navy background with subtle grid overlay + animated glow orbs)
   - Eyebrow pill: "SWITCHING TO KILO"
   - H1: "1,000+ Gyms Switched to Kilo." (line break) "Here's Why." — "1,000+ Gyms Switched" in cyan-to-mint gradient text
   - Subtitle: "Still on Wodify, Zen Planner, PushPress, or Mindbody? See what you're missing."
   - Dual CTAs: "Compare Now" (navy on white) + "Book a Free Demo" (outline on dark)
   - Browser-frame dashboard mockup

3. **Why Gyms Switch** (3-card grid)
   - "Easier to Use" — 80% report easier than previous software
   - "Better Support" — 3 specialized teams (website, marketing, management)
   - "Done-For-You Websites" — No competitor offers this
   - Card hover: lift + gradient top border reveal

4. **Feature Comparison Table** (6-column full table)
   - Columns: Feature | Kilo (highlighted) | Wodify | Zen Planner | PushPress | Mindbody
   - Kilo column: cyan tint background + "RECOMMENDED" badge
   - Category separator rows in navy
   - Rows include: Website Builder, Lead Nurture, CRM, Billing, Class Scheduling, Mobile App, Reporting, Done-For-You Setup, Ongoing Support, Starting Price
   - Icons: ✓ (green), ✗ (red), ◐ (partial/yellow), ★ (star for excellent)
   - Mobile: horizontally scrollable with hint text

   **Elementor note:** This is the most complex table. Use a custom HTML widget or a table plugin that supports horizontal scroll. The Kilo column highlight is critical — use a subtle background color to differentiate.

5. **How Switching Works** (3-step timeline)
   - Step 1: "Schedule Your Demo" — See the platform, ask questions
   - Step 2: "We Migrate Your Data" — Kilo handles the data transfer
   - Step 3: "Go Live" — Launch your new system
   - Horizontal numbered circles connected by gradient line
   - Circles: hover animates to gradient fill
   - Mobile: collapses to vertical timeline

6. **Switching Testimonials** (4 cards, dark navy background with ambient glow)
   - 2x2 grid
   - All 4 quotes from real switching customers
   - Avatar initials, author name, gym name

7. **Stats Bar**
   - 4 stats: 80% Say Easier | 3x Support Teams | 2 Days to Migrate | 92% Recommend
   - Gradient number treatment
   - Counter animation on scroll

8. **FAQ Accordion** (6 items)
   - Questions about: migration process, data transfer, cost, timeline, training, contracts
   - One answer links to comparison table section

9. **Final CTA** (dark navy with radial glow)
   - "They Switched. *You Can Too.*" — "You Can Too" in gradient highlight
   - Dual CTAs: "Book a Free Demo" (cyan) + "See Pricing" (outline)

10. **Trust Badges** — 5 Capterra/Software Advice/GetApp awards

11. **Footer** — Standard layout

---

## Implementation Notes for Elementor

### General
- Each HTML prototype is a complete visual reference. Open in browser and match the layout.
- All fonts are Google Fonts — add them in Elementor's Typography settings.
- Use Elementor's CSS custom properties or custom CSS per-section for brand colors.
- Scroll reveal animations: use Elementor's built-in "Motion Effects" (entrance animations) or a lightweight plugin like AOS.

### Specific Elementor Patterns
- **Sticky header:** Use Elementor's "Sticky" motion effect on the header section. Set `backdrop-filter: blur(12px)` via custom CSS.
- **FAQ accordion:** Use Elementor's native "Accordion" widget. Style with custom CSS for the chevron rotation and spacing.
- **Stats counters:** Use Elementor's "Counter" widget with starting value 0.
- **Comparison tables:** Use a custom HTML widget or Table plugin. Native Elementor tables lack the styling control needed.
- **Cards:** Use Elementor's "Inner Section" or "Container" widget with border-radius, shadow, and hover effects via custom CSS.
- **Gradient text:** Use `background: linear-gradient(...)` + `-webkit-background-clip: text` + `-webkit-text-fill-color: transparent` on heading widgets via custom CSS.

### CTA Links
All "Book a Demo" buttons should link to `/book-your-sales-call/` (or whatever the new booking page URL is after the redesign). All "See Pricing" buttons link to `/pricing/`.

### Images
The HTML prototypes use placeholder mockups (CSS-drawn browser frames, abstract UI elements). Replace these with:
- Actual Kilo dashboard screenshots
- Real gym website examples from the template gallery
- Headshots for testimonials (if available)
- Award badge images from Capterra, GetApp, Software Advice

### Mobile Testing Checklist
- [ ] Pricing cards stack properly on mobile (1 column)
- [ ] Comparison tables scroll horizontally with visible scroll indicator
- [ ] Hero sections stack (text above, visual below)
- [ ] Nav collapses to hamburger menu
- [ ] FAQ accordion works on touch
- [ ] CTAs are thumb-friendly (min 48px touch target)
- [ ] No horizontal overflow on any page
- [ ] Font sizes are readable (min 16px body)
