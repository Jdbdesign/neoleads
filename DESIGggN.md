# NeoLeads Marketing Website — Design Spec

## Overview

Pixel-faithful recreation of the NeoLeads dark-mode marketing website.  
**No deviations from the design.** Structure, layout, color, spacing, and content must match the uploaded reference exactly.

---

## Tech Stack

- Single HTML file (`index.html`) with embedded CSS and vanilla JS
- Google Fonts: `Inter` (all weights 400–700)
- No external component libraries
- Fully responsive (desktop-first, mobile-friendly)

---

## Design Tokens

### Colors
```
--bg-primary:       #02071A     /* Page background */
--bg-card:          #080D1F     /* Card/section background */
--bg-card-border:   #1A2040     /* Card border color */
--brand:            #6C2BDF     /* Purple accent / CTA */
--brand-light:      #8B4DFF     /* Hover / lighter purple */
--brand-glow:       rgba(108, 43, 223, 0.3)
--text-primary:     #FFFFFF
--text-secondary:   #8B9CC8     /* Muted gray-blue */
--text-muted:       #4A5578
--highlight-yellow: #F5C542     /* "We Grow." word in hero */
--highlight-orange: #FF6B35     /* Warm accent in some cards */
--green-accent:     #22C55E
--nav-bg:           rgba(2, 7, 26, 0.95)
--card-purple-bg:   rgba(108, 43, 223, 0.08)
```

### Typography
```
Font: Inter (Google Fonts)
--font-nav:         13px / 500
--font-hero-h1:     52px / 700 / line-height: 1.1
--font-h2:          36px / 700
--font-h3:          20px / 600
--font-body:        15px / 400 / line-height: 1.6
--font-small:       13px / 400
--font-label:       11px / 600 / letter-spacing: 0.1em / uppercase
```

### Spacing
- Section padding: `100px 0`
- Container max-width: `1160px`, centered, `0 auto`, padding `0 24px`
- Card gap: `20px`
- Border radius cards: `12px`
- Border radius buttons: `8px`

---

## Layout Sections (Top to Bottom)

---

### 1. NAVBAR

**Sticky top navigation bar.**

- Background: `rgba(2, 7, 26, 0.95)` with `backdrop-filter: blur(12px)`
- Border-bottom: `1px solid #1A2040`
- Height: `60px`

**Left:** `NeoLeads` logo in white bold text with a small purple square icon to its left.

**Center nav links** (inline, spaced):
`Solutions` | `Products` | `Pricing` | `Integrations` | `Resources` | `Tools` | `Teams`  
All links: `#8B9CC8`, hover: `#FFFFFF`, font-size `13px`

**Right:**
- `Log in` — ghost text link, white
- `Start for Free →` — filled button, background `#6C2BDF`, white text, border-radius `8px`, padding `8px 18px`

---

### 2. HERO SECTION

**Two-column layout:**

**Left column (55% width):**

- Small label above headline: `#6C2BDF` pill badge reading `AI-POWERED OUTBOUND` — uppercase, font-size `11px`, letter-spacing `0.1em`, background `rgba(108,43,223,0.15)`, border `1px solid rgba(108,43,223,0.4)`, border-radius `20px`, padding `4px 12px`

- Headline (H1, 52px bold, line-height 1.1):
  ```
  We Find. We Engage.
  They Reply. We Grow.
  ```
  — `We Find. We Engage.` = white  
  — `They Reply.` = white  
  — `We Grow.` = `#F5C542` (yellow)

- Subtext paragraph (16px, `#8B9CC8`, max-width 480px):  
  `The world's first AI-powered outbound platform that runs itself. We handle everything from finding leads to sending and receiving replies — so you only pay when other prospects engage.`

- Two CTA buttons side by side:
  - `Start for Free →` — filled `#6C2BDF`, white text, border-radius `8px`
  - `Book a Demo` — ghost, border `1px solid #1A2040`, white text, border-radius `8px`

- Small trust indicators below buttons (horizontal row, gap `24px`):
  - ✓ `No credit card required`
  - ✓ `10 free contacts`
  - ✓ `Cancel anytime`
  — checkmarks in `#22C55E`, text in `#8B9CC8`, font-size `13px`

**Right column (45% width):**

- Dark dashboard UI mockup card, background `#080D1F`, border `1px solid #1A2040`, border-radius `16px`, padding `20px`
- Inside: simulate a mini analytics dashboard with:
  - Top row: small bar chart (bars in purple gradient, varying heights)
  - Middle: a small line chart or stats row showing metrics like `Sent: 1,240`, `Replied: 87`, `Booked: 12`
  - Bottom row: small activity feed items (3 rows with avatar circles, text lines in gray, and a green "Replied" badge on one)
- Use CSS/HTML shapes (no actual image needed) — blocks and styled divs simulating a real dashboard

**Hero background:**  
Subtle radial gradient behind the left text: `radial-gradient(ellipse at 20% 50%, rgba(108,43,223,0.15) 0%, transparent 60%)`

---

### 3. LOGO BAR (Social Proof)

Full-width strip, `#02071A`, `padding: 48px 0`.

- Small label centered: `TRUSTED BY BUSINESSES WORLDWIDE` in `#4A5578`, uppercase, `11px`
- Below: horizontal row of **6 company logos** in muted white (`#3A4468`):
  - `Allstate` | `Abbvie` | `BlackRock` | *(Lotus-like symbol)* | `COTERRA` | `Candice`
- Logos spaced evenly, slight hover brightness increase

---

### 4. PRODUCT FEATURES — "The Complete Outbound Ecosystem"

**Section label** (centered, `#6C2BDF` pill): `FEATURES`

**H2** (centered, white, 36px bold): `The Complete Outbound Ecosystem`

**Subtext** (centered, `#8B9CC8`, 15px):  
`NeoLeads combines industry-leading technology with AI to find, start conversations, and send emails.`

**3-column grid of feature cards** (2 rows = 6 cards total):

Each card:
- Background: `#080D1F`
- Border: `1px solid #1A2040`
- Border-radius: `12px`
- Padding: `24px`
- Icon top-left: colored square icon (32×32px, border-radius `8px`)

**Row 1:**

1. **Zeus (Lead Discovery)**
   - Icon: Purple square with a lightning bolt `⚡`
   - Title: `Zeus (Lead Discovery)`
   - Body: `Find your ideal companies with AI-powered data with enrichment and intent signals.`

2. **Verifyrit (Email Validation)**
   - Icon: Teal/cyan square with a check `✓`
   - Title: `Verifyrit (Email Validation)`
   - Body: `Ensure 99%+ email deliverability with advanced verification and list data cleaning.`

3. **Warmrit (Email Warmer)**
   - Icon: Orange square with flame `🔥`
   - Title: `Warmrit (Email Warmer)`
   - Body: `Land in the inbox, not the spam folders.`

**Row 2:**

4. **Sendrit (Outreach Engine)**
   - Icon: Blue square with send arrow `→`
   - Title: `Sendrit (Outreach Engine)`
   - Body: `Create personalized email sequences, automate follow ups, and track every email.`

5. **Snaarp Mail (Inbox & Inbox)**
   - Icon: Purple square with envelope `✉`
   - Title: `Snaarp Mail (Inbox & Inbox)`
   - Body: `Unlimited mailboxes with a unified inbox to manage all replies in one place.`

6. **NeoBrain AI (Intelligence)**
   - Icon: Green square with brain/star `★`
   - Title: `NeoBrain AI (Intelligence)`
   - Body: `AI that replies, scores leads, creates email and helps you focus on the best opportunities.`

**Below the grid:** centered CTA button  
`Explore All Products →` — filled `#6C2BDF`, white text, padding `12px 28px`, border-radius `8px`

---

### 5. HOW IT WORKS — "From Leads to Conversations in 6 Simple Steps"

**Section label** (centered, `#6C2BDF` pill): `HOW IT WORKS`

**H2** (centered, white): `From Leads to Conversations in 6 Simple Steps`

**6-step icon grid** (3 columns × 2 rows):

Each step:
- Numbered circle top: `#6C2BDF` background, white number, `32px` diameter
- Icon below (circle, `48px`, `rgba(108,43,223,0.12)` bg, purple icon)
- Step title: white, `16px`, bold
- Step body: `#8B9CC8`, `14px`
- Connector arrow `→` between steps (horizontal within a row)

**Steps:**
1. `Find Leads` — Zeus finds your companies based on your ideal customer profile.
2. `Verify Emails` — Verifyrit confirms 99%+ email deliverability and data cleaning.
3. `Warm Up` — Warmrit builds strong sending reputation with inbox-safe warmup.
4. `Pay Per Conversation` — Only pay $10 for each reply.
5. `Get Replies` — AI replies, sends your art into their pipeline.
6. `Send Campaigns` — Sendrit launches personalized email campaigns.

---

### 6. ALL-IN-ONE PLATFORM — "Everything You Need. All In One Platform"

**Section label** (centered): `ALL-IN-ONE`

**H2** (centered, 2 lines):  
```
Everything You Need.
All In One Platform
```

**Subtext** (centered, `#8B9CC8`):  
`NeoLeads combines leading Saas technology with Al to initiate, start conversations and send emails.`

**4 feature showcase cards** in a 2×2 grid (large cards):

Each card has:
- Dark card bg (`#080D1F`), border `1px solid #1A2040`, border-radius `16px`
- Product name pill label top-left (small, `#6C2BDF` bg)
- Headline (H3, white)
- Body copy (`#8B9CC8`)
- Mini UI screenshot mock (CSS-drawn dark panel with purple accents)

**Cards:**

1. **Zeus Prospecting** — `Find qualified prospects with decisions makers' data and intent signals.` — Mock: dark panel with 3 lead rows, each with a company icon, name, and a small "Add" button in purple.

2. **Verifyrit & Warmrit** — `Unlimited contacts with a well-filtered and clean list sent to the inbox, not the spam.` — Mock: verification score `96/100` in large green text, below a row of email check statuses.

3. **Sendrit Automation** — `Run personalized email workflows to send your message at scale. Follow up smartly, personalize at every step.` — Mock: mini email sequence flowchart (Step 1 → Wait 2d → Step 2 → Wait 3d → Step 3).

4. **Snaarp Mail** — `Manage your entire inbox from a single unified inbox without switching accounts.` — Mock: mini inbox UI with 3 rows, sender name, subject preview, reply count badge.

**Full-width card (below the 2×2):**

5. **NeoBrain AI** — `Automate only qualifying incoming replies and score/email them to you so Zeus slots Verifyrit to do timing the rest.` — Card has a score badge showing `87` in a large circle, purple/teal gradient. Right side: mini metric display.

---

### 7. PRICING — "Pay Only for Conversations"

**Section label** pill (centered): `PAY PER RESULTS, NOT SOFTWARE`

**H2** (centered, 32px):  
```
Pay Only for
Conversations
```

**Subtext** (centered, `#8B9CC8`):  
`No monthly fee. No hidden fees. Just a simple $10 per qualified conversation we start for you.`

**Feature list (left column, 40%):**
- ✓ Unlimited qualified email sends
- ✓ Unlimited lead verification  
- ✓ Unlimited inboxes
- ✓ Custom analytics, complete daily costs

**Starting price (below feature list):**  
`Starting at` in `#8B9CC8`, then large `~$99` in white bold

**Right: Two pricing cards side by side**

**Card 1 — Platform Access:**
- Background `#080D1F`, border `1px solid #1A2040`
- Label: `Platform Access`
- Bullet list:
  - ✓ Zeus Lead Finder
  - ✓ Verifyrit Validation
  - ✓ Warmrit Warmup
  - ✓ Sendrit Campaigns
  - ✓ Snaarp Mail Inbox
  - ✓ NeoBrain AI

**Card 2 — Pay Per Conversation:**
- Background: subtle purple gradient border or glow
- Label: `Pay Per Conversation`
- Big number: `$10`  
  Subtext: `Per conversation started`
- Bullet list:
  - ✓ Only pay when Al books a reply
  - ✓ No monthly fees
  - ✓ No hidden costs
  - ✓ No limits on sends

**CTA below cards:**  
`Start for Free →` button, `#6C2BDF`, centered

---

### 8. INTEGRATIONS — "Plugs into your entire tech stack."

**Section label** pill (centered): `INTEGRATIONS`

**H2** (centered, 28px):  
`Plugs into your entire tech stack.`

**Subtext** (centered, `#8B9CC8`):  
`Connects Mailbox tools to your tech stack with CRMs, Slack, CRMs and more — 1000+ integrations.`

**Integration icons grid:**  
A 5×2 grid of rounded square integration icons (48×48px each), each with a white border on dark bg, spaced evenly. Icons represent (use colored placeholder squares with letters/symbols for each):

Row 1: Gmail (red), Outlook (blue), Slack (purple), HubSpot (orange), Salesforce (blue)  
Row 2: Pipedrive (green), Zapier (orange), Airtable (teal), Notion (white/black), LinkedIn (blue)

---

### 9. TESTIMONIALS — "Don't just take our word for it."

**Section label** pill (centered): `CUSTOMER STORIES`

**H2** (centered): `Don't just take our word for it.`

**3-column testimonial grid:**

Each testimonial card:
- Background `#080D1F`, border `1px solid #1A2040`, border-radius `12px`, padding `24px`
- ⭐⭐⭐⭐⭐ stars in gold (`#F5C542`) at top
- Quote text in white, `15px`
- Bottom: small avatar circle (gray placeholder), name in white `13px` bold, title in `#8B9CC8` `12px`

**6 testimonials (2 rows × 3 columns):**

1. ⭐⭐⭐⭐⭐ — *"NeoLeads completely changed our outbound workflow. We went from 5% reply rate to over 23% in 3 weeks."* — **James T.**, VP Sales, TechCorp

2. ⭐⭐⭐⭐⭐ — *"The pay-per-conversation model is genius. We only pay for actual results, not wasted software subscriptions."* — **Maria K.**, Founder, GrowthLab

3. ⭐⭐⭐⭐⭐ — *"NeoBrain AI is scary good. It replies to leads like a human, qualifies them and books meetings on autopilot."* — **Derek W.**, Head of Growth, ScaleUp

4. ⭐⭐⭐⭐⭐ — *"Setup was fast and the results came quickly. This is the future of outbound sales."* — **Priya S.**, Marketing Director, FintechHub

5. ⭐⭐⭐⭐⭐ — *"Best investment we made this year. Our pipeline has never been healthier."* — **Carlos M.**, CEO, LaunchPad

6. ⭐⭐⭐⭐⭐ — *"The unified inbox alone is worth it. Managing 10 mailboxes from one place is a game changer."* — **Sophie L.**, Sales Lead, Nexvio

---

### 10. SECURITY — "Keep your organization secure and compliant."

**Section label** pill (centered, green): `SECURITY & COMPLIANCE` — pill bg `rgba(34, 197, 94, 0.1)`, text `#22C55E`, border `1px solid rgba(34,197,94,0.3)`

**H2** (centered, 32px):  
```
Keep your organization secure
and compliant.
```

**Compliance badge row** (centered, horizontal, `gap: 32px`):

6 badges, each: dark card `#080D1F`, border `1px solid #1A2040`, border-radius `10px`, padding `16px 24px`, icon + label below:

1. `SOC 2` — shield icon, white text
2. `GDPR` — EU stars icon, white
3. `ISO 27001` — certificate icon, white
4. `CCPA` — lock icon, white
5. `HIPAA` — cross/medical icon, white  
6. `PCI DSS` — card icon, white

---

### 11. FINAL CTA — "Ready to generate real conversations?"

**Full-width section**, centered, `padding: 100px 0`

Subtle background: `radial-gradient(ellipse at 50% 50%, rgba(108,43,223,0.1) 0%, transparent 70%)`

**Section label** pill (centered): `GET STARTED`

**H2** (centered, 40px bold):  
`Ready to generate real conversations?`

**Subtext** (centered, `#8B9CC8`):  
`Join hundreds of businesses that only pay for results.`

**Two buttons centered:**
- `Start for Free →` — filled `#6C2BDF`, white, padding `14px 32px`, border-radius `8px`
- `Book a Demo` — ghost, border `1px solid #1A2040`, white

**Small trust row** (centered, below buttons):
- 🔒 `SOC 2 Certified` | ✓ `No credit card` | ✓ `Cancel anytime`
- All in `#4A5578`, font-size `13px`, `gap: 32px`

---

### 12. FOOTER

Background `#02071A`, border-top `1px solid #0F1535`  
Padding: `60px 0 40px`

**Top row (4 columns):**

**Col 1 — Brand:**
- `NeoLeads` logo (same as navbar)
- Tagline: `The world's first pay-per-result outbound platform for B2B sales teams.`
  — `#8B9CC8`, `14px`
- Social icons row: LinkedIn, Twitter/X, YouTube — circle icons, `#3A4468` bg, white icon, `36px`

**Col 2 — Solutions:**
- Heading: `Solutions` — white, `13px`, uppercase, bold
- Links (each `#8B9CC8`, `13px`, hover white):
  - Lead Generation
  - Email Outreach
  - Inbox Management
  - AI Automation
  - Analytics

**Col 3 — Products:**
- Heading: `Products`
- Links:
  - Zeus
  - Verifyrit
  - Warmrit
  - Sendrit
  - Snaarp Mail
  - NeoBrain AI

**Col 4 — Company:**
- Heading: `Company`
- Links:
  - About
  - Careers
  - Blog
  - Press
  - Contact

**Col 5 — Contact Information:**
- Heading: `Contact Information`
- Email: `hello@neoleads.io`
- Support: `support@neoleads.io`

**Bottom bar** (border-top `1px solid #0F1535`, `padding-top: 24px`):
- Left: `© 2025 NeoLeads. All rights reserved.`
- Right: `Privacy Policy` | `Terms of Service` | `Cookie Policy`
- All: `#4A5578`, `13px`

---

## Global CSS Rules

```css
* { box-sizing: border-box; margin: 0; padding: 0; }
body {
  background: #02071A;
  color: #FFFFFF;
  font-family: 'Inter', sans-serif;
  font-size: 15px;
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}
a { text-decoration: none; color: inherit; }
img { max-width: 100%; }

/* Section label pill (reused) */
.section-label {
  display: inline-block;
  background: rgba(108, 43, 223, 0.12);
  border: 1px solid rgba(108, 43, 223, 0.35);
  color: #6C2BDF;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  border-radius: 20px;
  padding: 5px 14px;
  margin-bottom: 20px;
}

/* Container */
.container {
  max-width: 1160px;
  margin: 0 auto;
  padding: 0 24px;
}

/* Primary button */
.btn-primary {
  background: #6C2BDF;
  color: #FFFFFF;
  border: none;
  border-radius: 8px;
  padding: 11px 22px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.2s;
}
.btn-primary:hover { background: #8B4DFF; }

/* Ghost button */
.btn-ghost {
  background: transparent;
  color: #FFFFFF;
  border: 1px solid #1A2040;
  border-radius: 8px;
  padding: 11px 22px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  transition: border-color 0.2s;
}
.btn-ghost:hover { border-color: #6C2BDF; }

/* Card base */
.card {
  background: #080D1F;
  border: 1px solid #1A2040;
  border-radius: 12px;
  padding: 24px;
}
```

---

## Implementation Notes for Claude Code

1. **Single file** — All CSS in `<style>` tags in the `<head>`. All JS inline at bottom of `<body>`.
2. **No external images** — Use CSS-drawn UI mocks, SVG icons inline, or Unicode symbols/emoji where appropriate.
3. **Dashboard mock in hero** — Build using pure HTML/CSS: divs styled as bars, lines, rows. No `<canvas>`.
4. **Google Fonts** — Import at top: `@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');`
5. **Sticky navbar** — `position: sticky; top: 0; z-index: 100;`
6. **Section backgrounds** — Alternate slightly between `#02071A` and `#04081F` to create visual rhythm.
7. **Hover states** — All interactive elements must have visible hover feedback.
8. **Responsive** — At `≤768px`: single column for all grids, hamburger menu for nav (optional: collapse to hidden).
9. **Smooth scroll** — `html { scroll-behavior: smooth; }`
10. **Scroll reveal** — Optional: use `IntersectionObserver` to fade-in sections as user scrolls.
11. **Hero radial glow** — CSS `radial-gradient` on a pseudo-element behind the hero text.
12. **Keep exact section order** as listed in this document, top to bottom.
13. **Brand color consistency** — Every purple usage must be exactly `#6C2BDF` (buttons, badges, icons, highlights). No approximations.
14. **Yellow highlight** — `We Grow.` in the hero H1 must use `#F5C542`.
