# VELARE EXOTICS — MASTER PLAN

> A peer-to-peer marketplace for exotic and luxury vehicles. Built to make Turo look like Craigslist.

**Document version:** 1.0
**Last updated:** May 2026
**Status:** Pre-build planning

---

## Table of Contents

1. [Executive Summary](#1-executive-summary)
2. [Why Turo Loses the Exotic Segment](#2-why-turo-loses-the-exotic-segment)
3. [Brand Positioning & Voice](#3-brand-positioning--voice)
4. [Killer Differentiators (How We Win)](#4-killer-differentiators-how-we-win)
5. [Membership & Vetting Model](#5-membership--vetting-model)
6. [Revenue Model & Fee Structure](#6-revenue-model--fee-structure)
7. [The Profit Calculator (AI-Powered)](#7-the-profit-calculator-ai-powered)
8. [Site Architecture](#8-site-architecture)
9. [Design Language](#9-design-language)
10. [Technical Architecture](#10-technical-architecture)
11. [Backend & Admin System](#11-backend--admin-system)
12. [AI Feature Stack](#12-ai-feature-stack)
13. [Trust, Safety & Insurance](#13-trust-safety--insurance)
14. [Database Schema (High-Level)](#14-database-schema-high-level)
15. [API Surface](#15-api-surface)
16. [Build Roadmap](#16-build-roadmap)
17. [Open Questions](#17-open-questions)

---

## 1. Executive Summary

**Velare Exotics** is an invitation-and-application-based marketplace for renting exotic, luxury, and collector-grade vehicles. We are not trying to be Turo for everyone — we are trying to be the **only** platform a McLaren owner would trust to rent their car, and the only place a buyer of a $5,000/day experience would think to look.

**The thesis is simple:**
- Turo is a volume game. They take 25–40% off owners and put a Camry next to a 720S.
- Exotic owners hate Turo. The economics are brutal, the renters are unscreened, and the "Ultimate" insurance tier still leaves them exposed on cars worth $300K+.
- Renters paying $1,500/day don't want to be on the same platform as the guy renting a 2014 Civic.

**Velare wins on five axes:**
1. **Owner economics** — 12% commission vs Turo's 15–40% on host plans.
2. **Curation** — every car professionally vetted, every renter background-checked.
3. **Real insurance** — agreed-value policies that actually pay out on a Lambo.
4. **Brand** — a site that feels like it belongs next to the cars on it.
5. **Concierge layer** — delivery, detailing, track partnerships, photo/film rentals.

---

## 2. Why Turo Loses the Exotic Segment

A clear-eyed look at where the incumbent fails. Each of these is a wedge.

| Pain Point | Turo's Behavior | Velare's Wedge |
|---|---|---|
| **Commission** | 15–40% off owner depending on protection plan | Flat 12% Standard / 8% Velare Black |
| **Insurance ceiling** | Up to $750K liability, but vehicle valuation often disputed | Agreed-value policies underwritten for exotics specifically |
| **Renter quality** | Anyone with a license and a credit card | Application + ID verify + driving history + financial check |
| **Listing quality** | Owner takes iPhone photos in their driveway | Free professional photoshoot for every approved listing |
| **Damage disputes** | Notoriously slow, owner-unfriendly | 48-hour resolution SLA, dedicated case manager per claim |
| **Wear & tear** | Capped reimbursement, miles often disputed | Per-mile premium pricing; track miles billed separately |
| **Mileage limits** | Often 200/day, overage fees frustrate renters | Tiered: Touring (200mi), Open Road (unlimited highway), Track (separate) |
| **Customer support** | Chat-only, often offshore | US-based concierge line, 24/7 for active rentals |
| **Brand fit** | Generic startup aesthetic | A brand that an owner is proud to associate with |
| **Track use** | Forbidden by terms | Sanctioned track-day rentals at partner circuits |
| **Static rentals** | Allowed but undifferentiated | Photo/film/wedding rentals as a separate product line |

---

## 3. Brand Positioning & Voice

### Name
**Velare** — Italian, "to veil." The cars are unveiled to you. Connotes Italian motoring heritage without being a cliché.

### Tagline options
- *Drive what you've earned.*
- *The exotic, on demand.*
- *For the cars you only see at concours.*

(Recommend: **"Drive what you've earned."** — works for both renters and owners, slightly aspirational without being tacky.)

### Voice
- **Confident, never loud.** Apple/Hermès, not Liquid Death.
- **Spare copy.** Three words where Turo uses fifteen.
- **Specifics over adjectives.** "611 hp, 0–60 in 2.7" beats "blazing fast."
- **No exclamation marks. Anywhere.**

### Visual direction
- Dark mode default. Pure black (#0A0A0A) backgrounds, never true `#000`.
- Photography is the design. Cars are the heroes; UI gets out of the way.
- Type: **Söhne** or **Inter Tight** for body, **PP Editorial New** or **Saol Display** for headlines. (Both are licensed — get a one-time license per font, not a free swap.)
- One accent color — a deep champagne/gold (`#C9A961`) — used sparingly for CTAs and active states.
- Generous whitespace. Apple-style scroll-jacked sections that reveal photography.

---

## 4. Killer Differentiators (How We Win)

These are the things that, if executed, make Turo irrelevant for this segment.

### 4.1 Velare Concierge
A real human service layer, not a chatbot.
- Vehicle delivery to hotel, airport, residence, or yacht
- Pre-rental detail + post-rental detail included on rentals over $X/day
- Routes, restaurant recs, and scenic drive itineraries
- Optional security driver or chase car for ultra-high-value units

### 4.2 Track Day Program
Turo bans track use. We embrace it as a paid premium product.
- Partner with circuits: Willow Springs, COTA, Road America, Thermal Club, Monticello, etc.
- "Track-Approved" listings at premium rates with pre-arranged insurance riders
- Owner opt-in only; many will say yes for the right rate

### 4.3 Static / Production Rentals
A separate, lower-rate product for non-driving use.
- Photo shoots, music videos, weddings, commercials, social content
- Half the day rate, no mileage, on-set contract
- Owners love this — passive income with zero wear

### 4.4 The Velare Drives Calendar
Members-only events that drive owner retention and renter loyalty.
- Quarterly group drives in Malibu, Big Sur, Tail of the Dragon, etc.
- Owners-only gala once a year
- Rolling Concours: members display at curated cars-and-coffee

### 4.5 Verified by Velare Photography
Every approved listing gets a free 90-minute professional shoot.
- Same lens, same edit grade, same composition rules across the platform
- This single decision is what makes the marketplace look unified — Turo will never do this because it doesn't scale to 200,000 cars; it scales fine to 5,000.

### 4.6 Owner Cooperative Profit Share
Top 10% of owners by revenue at year-end share in a 1% pool.
- Costs us almost nothing, locks in the supply side, becomes a status symbol.

### 4.7 White-Label Concierge for Hotels
Five-star hotels white-label our fleet for guest delivery.
- Four Seasons concierge calls Velare; we deliver to the porte-cochère.
- Hotel earns a referral fee, we earn a luxury distribution channel.

### 4.8 AR "See It in Your Driveway"
WebXR-based: scan your driveway, place the car, walk around it.
- Closes the gap between browsing and booking.
- Turo will not build this. Most owners will love it.

### 4.9 Telematics & Geofencing
Standard on every vehicle (we pay for the unit, owner installs).
- Real-time location, speed, RPM
- Owner-set geofences (e.g., no Mexico, no track unless track-rental booked)
- Drives down insurance costs, increases owner trust

### 4.10 Pre/Post Inspection Video
Required, structured, timestamped — not a vague photo set.
- 360° walkaround video at handoff and return, both parties on camera
- Eliminates 80% of damage disputes before they start

---

## 5. Membership & Vetting Model

This is the wall that keeps Turo's worst customers out.

### Renters
**Application required.** Not a hard wall — most applications approved within 24 hours — but a wall.
- ID + driver's license verification (Persona or Stripe Identity)
- MVR (Motor Vehicle Record) check via Checkr or Samba Safety
- Soft credit pull for financial responsibility
- Minimum age: 25 for sports/luxury, 30 for hyper-class
- For cars over $500K market value: financial verification (proof of liquidity or premium membership)

**Membership tiers:**
| Tier | Eligibility | Benefits |
|---|---|---|
| **Standard** | Approved application | Access to most listings |
| **Velare Gold** | $1,000/yr or $15K+ in rentals | Priority booking, free delivery, no security deposit |
| **Velare Black** | Invitation only | Access to off-market hyper cars, concierge, private events |

### Owners
- KYC + title verification (we pull DMV records)
- Vehicle inspection (in-person for first listing, photo-based for additional)
- Insurance policy review
- Bank account + tax info (1099 reporting)

---

## 6. Revenue Model & Fee Structure

The pricing has to be both *better than Turo* and *legible* — owners need to see the math instantly.

### Owner Commission
| Plan | Velare Take | Turo Equivalent | Velare Provides |
|---|---|---|---|
| **Standard** | **12%** | 25% (Turo "85") | $1M liability, basic protection, standard support |
| **Plus** | **15%** | 30% (Turo "80") | $2M liability, full physical damage, photo shoot, priority placement |
| **Black** | **8%** | N/A | Invite-only owners; full white-glove, custom insurance, lowest commission |

### Renter Fees
- **Service fee:** 10% of rental subtotal (Turo: 10–15% obscured)
- **Concierge delivery fee:** flat by zone, transparent
- **Damage protection:** $19/$39/$79 per day tiers (Basic / Premium / Black)
- **Young driver fee:** $25/day for 25–29
- **Cleaning fee:** Owner-set, capped at $200

### Other revenue
- Membership dues (Gold tier)
- Track-day program (15% on top of rental, paid by renter)
- Production/photo rental coordinator fee (10%)
- White-label hotel partnership revenue share
- Premium listing placements (transparent, labeled, capped at 3 per page)

### The "Beat Turo" Math

For an owner renting a $1,500/day Lambo at 80% occupancy (24 days/month):

| | Turo (15% plan) | Turo (40% plan) | **Velare Standard (12%)** |
|---|---|---|---|
| Gross | $36,000 | $36,000 | $36,000 |
| Commission | -$5,400 | -$14,400 | **-$4,320** |
| **Net to owner** | $30,600 | $21,600 | **$31,680** |

That's **$120,960 more per year** than Turo's most popular plan. This is the headline number for owner acquisition.

---

## 7. The Profit Calculator (AI-Powered)

A core acquisition tool. Lives at `/list-your-car` and as a marketing landing page at `/calculator`.

### Inputs
- Year, Make, Model, Trim
- ZIP code (location)
- Estimated retail value (auto-pulled, owner can override)
- Owner's expected availability (days/month)
- Optional: photos for condition assessment

### Outputs
- **Estimated daily rate** (low / median / high)
- **Estimated monthly revenue** at conservative / realistic / optimistic occupancy
- **Estimated annual revenue**
- **Velare fee transparency** — line-item breakdown
- **Comparison to Turo** — same car, same usage, on Turo's most-used plans
- **Booking frequency forecast** — "Your car would likely be booked X days/month in your area"
- **Demand heat map** — visual of demand in surrounding zip codes
- **Top 3 comparable listings** in the area with their pricing

### How the AI gets the answer

The calculator is **not a single LLM call**. The LLM is the orchestrator over real data.

**Data inputs (we maintain):**
- `comparable_listings` table — scraped/licensed data on similar vehicles, their rates, and approximate booking density
- `market_demand` table — by ZIP code, by vehicle class, by month (seasonality)
- `vehicle_msrp` lookup — book values via partner API (Black Book or KBB B2B)

**The orchestration:**
```
User submits form
  → Server pulls market data for that car class + ZIP
  → Claude (Sonnet) is given:
      - The car details
      - 5–10 most-comparable real listings with their rates and booking days
      - Local demand index
      - Seasonality data
  → Claude returns structured JSON: {
       daily_rate: { low, median, high, reasoning },
       occupancy: { conservative, realistic, optimistic },
       narrative: "..."  // explanation shown to user
    }
  → Server computes the dollar math and renders the result
```

**Why use the LLM at all?**
- It synthesizes the comparable listings into a defensible rate range with a *reasoning narrative* the user trusts.
- It handles edge cases (rare cars, no comparables) gracefully — falls back to class averages with explanation.
- It writes the personalized "your car in your market" copy that makes the result feel bespoke.

### API key handling — read this carefully
- The Anthropic API key lives **only** in `process.env.ANTHROPIC_API_KEY` on the server.
- The calculator UI calls `/api/estimate` (a Next.js route handler).
- That route handler is the *only* place that imports the Anthropic SDK.
- The browser never sees the key. Ever.
- Add rate limiting (Upstash Redis, 5 calls / IP / hour) to prevent abuse.
- Add a CAPTCHA (Cloudflare Turnstile) on the form to prevent automated draining.

### Sample server route (illustrative pseudocode)
```ts
// app/api/estimate/route.ts
import Anthropic from "@anthropic-ai/sdk";
import { rateLimit } from "@/lib/rate-limit";

export async function POST(req: Request) {
  await rateLimit(req);
  const { year, make, model, zip, daysPerMonth } = await req.json();

  const comparables = await db.findComparables({ make, model, year, zip });
  const demand = await db.getDemandIndex(zip, vehicleClass(make, model));

  const client = new Anthropic({ apiKey: process.env.ANTHROPIC_API_KEY });
  const msg = await client.messages.create({
    model: "claude-sonnet-4-6",
    max_tokens: 1024,
    system: ESTIMATOR_SYSTEM_PROMPT,
    messages: [{
      role: "user",
      content: JSON.stringify({ vehicle: { year, make, model }, zip,
                                comparables, demand, daysPerMonth })
    }],
  });

  return Response.json(parseStructured(msg));
}
```

---

## 8. Site Architecture

### Public pages
- `/` — Hero, featured fleet, "How it works," social proof, CTA
- `/fleet` — Browse listings (filterable: make, class, location, price, dates)
- `/fleet/[slug]` — Vehicle detail page (gallery, specs, owner, calendar, book)
- `/destinations/[city]` — Curated landing per market (LA, Miami, NYC, Vegas, Dubai…)
- `/list-your-car` — Owner acquisition flow with embedded calculator
- `/calculator` — Standalone profit calculator (marketing entry point)
- `/membership` — Tier comparison (Standard / Gold / Black)
- `/concierge` — Concierge service detail
- `/track-program` — Track day rentals
- `/production-rentals` — Photo/film rentals
- `/about` / `/journal` (editorial) / `/contact`
- `/legal/*` — Terms, Privacy, Insurance disclosures

### Authenticated — Renter
- `/account` — Profile, ID verification status, payment methods
- `/account/trips` — Active, upcoming, past
- `/account/messages` — Owner conversations
- `/account/membership` — Tier, benefits, billing

### Authenticated — Owner (Host)
- `/host` — Dashboard (revenue, occupancy, upcoming bookings)
- `/host/listings` — Manage listings
- `/host/listings/new` — Add a vehicle (multi-step wizard)
- `/host/calendar` — Availability and pricing
- `/host/earnings` — Payouts, tax docs
- `/host/messages`

### Admin (separate subdomain or `/admin/*` behind auth)
See [Section 11](#11-backend--admin-system).

---

## 9. Design Language

### Layout grid
- 12-col on desktop, 8-col tablet, 4-col mobile
- Max content width 1440px, but hero/photo sections go edge-to-edge
- Generous vertical rhythm — minimum 96px between major sections on desktop

### Color system
```
--bg-primary:    #0A0A0A   (near-black, never #000)
--bg-elevated:   #141414
--bg-card:       #1A1A1A
--border-subtle: #262626
--text-primary:  #FAFAFA
--text-muted:    #A1A1A1
--text-faint:    #525252
--accent:        #C9A961   (champagne)
--accent-hover:  #D4B574
--success:       #4ADE80
--danger:        #EF4444
```

### Gradients (the "no sharp page breaks" requirement)
- Section transitions use a 200px overlap with a vertical gradient mask
- Hero → next section: `bg-primary` fading into a 5% radial of `accent` then back into `bg-elevated`
- Cards lift on hover with a subtle gold inner-glow (`box-shadow: inset 0 0 0 1px rgba(201,169,97,0.2)`)
- Use CSS `mask-image: linear-gradient(...)` on section seams instead of background-color hops

### Motion principles (the "Apple feel")
- Default ease: `cubic-bezier(0.22, 1, 0.36, 1)` — strong start, soft end
- Default duration: 600ms for big moves, 200ms for micro-interactions
- Scroll-driven reveals using IntersectionObserver, not on-mount
- Hero: a single hero car that parallaxes and rotates slightly on scroll (Three.js GLB or a layered image stack)
- Page transitions: shared-element via Next.js View Transitions API
- Loading: never spinners. Use skeletons that match the final layout exactly.

### Typography scale
```
Display:  72/80/96  PP Editorial New, weight 400
H1:       48/56     PP Editorial New, weight 400
H2:       36/44     PP Editorial New, weight 400
H3:       24/32     Inter Tight, weight 500
Body L:   18/28     Inter Tight, weight 400
Body:     16/26     Inter Tight, weight 400
Caption:  13/18     Inter Tight, weight 500, tracking 0.04em
```

Tracking: -0.02em on display headlines, +0.04em on uppercase captions.

### Logomark usage
The `logomarknobg.png` (transparent PNG you have locally) goes in:
- Top-left nav (32px height)
- Footer (48px height)
- Loading screen (centered, 96px, with subtle pulse)
- Email headers
- PDF rental contracts
- Owner dashboard
- Watermark on owner-uploaded photos (small, bottom-right corner, 8% opacity)

Drop the file at `/public/brand/logomark.png` (and ideally an SVG version) when we build.

---

## 10. Technical Architecture

### Stack
| Layer | Choice | Why |
|---|---|---|
| Framework | **Next.js 15 (App Router)** | SSR, RSC, image optimization, fastest path to a polished marketing + app |
| Styling | **Tailwind CSS v4** + custom design tokens | Fast iteration, design system enforced |
| Animation | **Framer Motion** + native View Transitions | The "Apple feel" |
| 3D | **Three.js / React Three Fiber** | Hero car rotation, AR preview |
| Database | **PostgreSQL** (Supabase or Neon) | Relational data, real auth, RLS |
| ORM | **Prisma** | Type safety, migrations |
| Auth | **Clerk** or **NextAuth + Postgres** | Clerk is faster; NextAuth is cheaper |
| Payments | **Stripe Connect** | Escrow, owner payouts, identity, PCI offload |
| Storage | **Cloudflare R2** or **AWS S3** + Cloudflare Images | Photo/video hosting, transformations |
| Search | **Typesense** or **Algolia** | Instant filtering on `/fleet` |
| Maps | **Mapbox GL JS** | Pickup/delivery zones, demand heatmap |
| Email | **Resend** + **React Email** | Transactional emails that don't look transactional |
| SMS | **Twilio** | Booking confirmations, two-factor |
| Background jobs | **Inngest** or **Trigger.dev** | Reminders, payout schedules, AI tasks |
| Analytics | **PostHog** (self-hostable) | Funnels, session replay, feature flags |
| Error tracking | **Sentry** | |
| AI | **Anthropic Claude** | Per project preference |
| KYC | **Persona** or **Stripe Identity** | |
| MVR check | **Checkr** or **Samba Safety** | |
| Telematics | **Bouncie** or **Smartcar** | OBD-II + connected-car data |
| Hosting | **Vercel** for frontend + API, **Railway/Fly** for workers | |

### Repository layout
```
velare/
├── apps/
│   ├── web/              # Next.js marketing + customer app
│   └── admin/            # Internal admin (can be Next.js too, behind auth)
├── packages/
│   ├── db/               # Prisma schema + client
│   ├── ui/               # Shared design system components
│   ├── auth/             # Auth helpers
│   ├── ai/               # Anthropic clients, prompts, parsers
│   └── jobs/             # Inngest functions
├── public/
│   └── brand/            # logomark.png, logomark.svg, fonts
└── turbo.json
```

### Performance targets
- Lighthouse Performance: 95+ on `/`, `/fleet`, vehicle detail pages
- LCP under 1.8s on 4G
- CLS effectively 0
- Hero photography served as AVIF with WebP fallback, max 200KB per image
- All images via `next/image` with explicit dimensions

---

## 11. Backend & Admin System

The admin system is a first-class product, not an afterthought. It's how the business runs.

### Account model
```
Master account (you)
  └── Employees (with roles)
       └── Customers (renters)
       └── Hosts (owners)
       └── Vehicles
       └── Bookings
       └── ...
```

### Roles & permissions (RBAC)
Default roles, all customizable per-employee:

| Role | Permissions |
|---|---|
| **Master** (Owner) | Everything. Cannot be deleted. Can grant/revoke any permission. |
| **Admin** | All except billing/employee management |
| **Operations Manager** | Bookings, listings, disputes, customer support |
| **Concierge Agent** | Active bookings, customer messaging, delivery scheduling |
| **Listings Reviewer** | Approve/reject new listings, request changes |
| **Trust & Safety** | KYC reviews, fraud flags, account suspensions |
| **Finance** | Payouts, refunds, tax reports, revenue dashboards |
| **Marketing** | Promo codes, content publishing, featured listings |
| **Read-only Auditor** | View everything, change nothing |

**Permission granularity** — each role is a bag of fine-grained permissions:
```
LISTINGS_VIEW, LISTINGS_APPROVE, LISTINGS_REJECT, LISTINGS_DELETE,
BOOKINGS_VIEW, BOOKINGS_REFUND, BOOKINGS_CANCEL, BOOKINGS_OVERRIDE_PRICING,
USERS_VIEW, USERS_SUSPEND, USERS_DELETE, USERS_PROMOTE,
EMPLOYEES_INVITE, EMPLOYEES_REMOVE, EMPLOYEES_ROLE_EDIT,
PAYOUTS_VIEW, PAYOUTS_RUN, PAYOUTS_HOLD,
DISPUTES_VIEW, DISPUTES_RESOLVE,
ANALYTICS_VIEW, ANALYTICS_EXPORT,
SETTINGS_EDIT, AUDIT_LOG_VIEW
```

You as Master can build a custom role by checking which permissions it has. Like Notion's permission system or Linear's.

### Admin dashboard surfaces

**Home** — KPIs at a glance
- GMV (this month vs last)
- Active bookings right now
- New listings pending review (count)
- Disputes open (count, with SLA timers)
- Recent signups

**Vehicles**
- All listings, filterable by status (pending / live / paused / rejected)
- Click into a listing → full edit, photo replacement, owner contact, booking history
- Approval queue with side-by-side: photos, specs, owner profile, KYC status

**Users**
- Renters tab + Hosts tab
- Per-user: profile, verification status, booking history, payment history, notes (internal), flag/suspend
- Note: PII access is itself a permission and audit-logged

**Bookings**
- All bookings with status filter
- Click into → trip timeline, messages, contracts, inspection videos, payment status
- Override actions (refund, extend, cancel) all require reason + double confirm

**Payouts**
- Owners' upcoming payouts
- Hold/release controls (with reason)
- 1099 reporting + downloadable tax docs

**Disputes**
- Damage claims, refund requests, no-shows, accidents
- Per-case: timeline, evidence (videos, photos, messages), AI-suggested resolution, manual override
- SLA timers visible and color-coded

**Employees**
- Invite by email
- Assign role(s) — can be combined
- View their audit log
- Suspend/remove

**Audit log**
- Every sensitive action: who, what, when, IP, user-agent
- Filterable, exportable
- Immutable (append-only table, no deletes)

**Settings**
- Commission tiers
- Insurance policy text
- Service area zones
- Featured listings
- Promo codes
- Brand assets

### Auth & security
- 2FA required for all employees (TOTP, not SMS)
- Master account requires hardware key (WebAuthn)
- Session timeout: 8 hours for employees
- Geographic alerts: any login from new country pings master
- Read-after-write audit logs (every admin action logged before response sent)

---

## 12. AI Feature Stack

Where Claude (or other models) actually earn their keep.

### 12.1 Profit Calculator (covered in §7)

### 12.2 Listing Quality Coach
When an owner is creating a listing, the AI reviews photos and copy in real time:
- "Your hero shot is underexposed — try this angle"
- "Your description is missing: drivetrain, mileage, modifications"
- "Listings with X get 40% more bookings"

### 12.3 Demand-Aware Dynamic Pricing (opt-in)
- Suggests rate adjustments per day based on local demand, events, competitor rates
- "Rate Aware" badge on listings using it
- Owner approves/rejects suggestions or auto-accepts within a band

### 12.4 Damage Triage Assistant
On post-rental inspection videos:
- AI compares pre/post inspection clips
- Flags candidate damage points with timestamps
- Routes to appropriate Trust & Safety agent
- *Decisions are still human* — AI just speeds up triage

### 12.5 Concierge Copilot (internal)
Tool for concierge agents — drafts responses to customer questions using:
- Customer's booking context
- Vehicle specs
- Local recommendations
Agent reviews and sends. Reduces response time from minutes to seconds.

### 12.6 Trip Itinerary Generator (renter-facing)
"You booked a 458 in LA for 3 days. Here's a curated drive: PCH to Malibu, lunch at Geoffrey's, Mulholland sunset, dinner at..."

### 12.7 Application Reviewer (assistive)
For renter applications, AI flags:
- Inconsistencies in submitted info
- Higher-risk indicators (fresh license, mismatched names)
- Suggests approve/manual-review/reject — final decision is human.

### Anthropic API integration pattern
```
packages/ai/
├── client.ts              # Singleton Anthropic client (server only)
├── prompts/
│   ├── estimator.ts
│   ├── listing-coach.ts
│   ├── damage-triage.ts
│   └── concierge-copilot.ts
├── parsers/               # Structured JSON parsers per feature
├── rate-limit.ts          # Per-user, per-feature limits
└── audit.ts               # Log every AI call (input/output) for review
```

**Every AI call is audit-logged.** Cost-tracked per feature. Rate-limited per user.

---

## 13. Trust, Safety & Insurance

### Insurance strategy
This is the single biggest blocker for an exotic platform. Get this wrong and owners won't list.

**Three-policy stack:**
1. **Commercial liability umbrella** — $1M baseline, $2M for Plus tier
2. **Physical damage coverage** — agreed-value, not actual cash value (critical for appreciating cars)
3. **Owner gap policy** — fills any gap between Velare's coverage and the owner's personal collector policy

**Carriers to approach:**
- Intact Insurance (commercial fleet)
- Hagerty (collector specialist; possible partnership)
- Markel, Chubb (high-net-worth segment)

**The pitch to owners:**
> Your $400K car is insured at agreed value, not Kelly Blue Book. If it's totaled, you're made whole at the value we wrote in the policy when it was listed.

### Renter screening
- ID verification (Persona)
- License verification + MVR
- Soft credit (TransUnion B2B)
- Watchlist screening (sanctions, sex offender registries)
- Address verification
- Phone verification

### Vehicle requirements
- Title in owner's name (or LLC owned by host)
- Personal insurance must allow commercial use OR be willing to ride excess of Velare
- Telematics required on units over $100K
- No salvage titles
- Annual safety inspection on rental fleet vehicles

### Damage process (the 48-hour SLA)
1. **At return**: structured inspection video required by both parties
2. **If damage flagged**: AI triage runs immediately, case opens
3. **Within 24h**: dedicated case manager assigned, contacts both parties
4. **Within 48h**: estimate produced (in-network bodyshop or independent appraiser)
5. **Within 5 days**: payout to owner (we eat the float, recover from renter or insurance)

---

## 14. Database Schema (High-Level)

Not exhaustive — just the spine.

```
users
  id, email, phone, name, role (renter|host|both), tier, created_at,
  kyc_status, mvr_status, stripe_customer_id, stripe_connect_id

employees
  id, user_id, role_id, status, invited_at, last_active_at

roles
  id, name, permissions (jsonb array), is_system_role

permissions_audit
  id, employee_id, action, target_type, target_id, metadata, ip, ua, at

vehicles
  id, owner_user_id, year, make, model, trim, vin, color, mileage,
  msrp, market_value, photos (jsonb), description, status,
  vehicle_class, location_zip, lat, lng, telematics_id

listings
  id, vehicle_id, daily_rate, weekly_rate, monthly_rate,
  min_age, mileage_limit, delivery_radius, instant_book,
  velare_plan (standard|plus|black), status

bookings
  id, listing_id, renter_user_id, owner_user_id,
  start_at, end_at, daily_rate, total, fees (jsonb),
  status, contract_id, inspection_pre_id, inspection_post_id

inspections
  id, booking_id, type (pre|post), video_url, photos (jsonb),
  notes, performed_by, performed_at, ai_flags (jsonb)

payments
  id, booking_id, amount, type (charge|refund|payout|fee),
  stripe_id, status, occurred_at

disputes
  id, booking_id, opened_by, opened_at, status, sla_deadline,
  evidence (jsonb), resolution, resolved_by, resolved_at

messages
  id, thread_id, sender_user_id, body, attachments, sent_at, read_at

market_data
  zip, vehicle_class, demand_index, avg_daily_rate,
  avg_occupancy, sample_size, last_updated_at

ai_events
  id, feature, input_hash, prompt_tokens, completion_tokens,
  cost_cents, latency_ms, user_id, created_at

audit_log
  id, actor_user_id, actor_employee_id, action, target_type,
  target_id, before (jsonb), after (jsonb), ip, ua, at
```

Use Postgres row-level security so a host can only see their own bookings, a renter only their trips, etc. Never enforce in app layer alone.

---

## 15. API Surface

REST + a few RPC-style endpoints. Auth via session cookies (HttpOnly, SameSite=Strict).

```
Public
  POST  /api/estimate                  — profit calculator
  GET   /api/listings                  — search/filter
  GET   /api/listings/:slug
  GET   /api/destinations/:city

Auth
  POST  /api/auth/signup
  POST  /api/auth/signin
  POST  /api/auth/signout
  POST  /api/auth/2fa/verify

Renter
  POST  /api/bookings                  — create
  GET   /api/bookings
  GET   /api/bookings/:id
  POST  /api/bookings/:id/cancel
  POST  /api/bookings/:id/extend
  POST  /api/messages

Host
  POST  /api/host/listings
  PATCH /api/host/listings/:id
  GET   /api/host/earnings
  GET   /api/host/calendar

Webhooks
  POST  /api/webhooks/stripe
  POST  /api/webhooks/persona
  POST  /api/webhooks/checkr
  POST  /api/webhooks/telematics

Admin (separate auth, employee-only)
  GET   /api/admin/dashboard
  GET   /api/admin/listings/pending
  POST  /api/admin/listings/:id/approve
  POST  /api/admin/listings/:id/reject
  GET   /api/admin/users
  POST  /api/admin/users/:id/suspend
  POST  /api/admin/employees/invite
  PATCH /api/admin/employees/:id
  ...etc
```

---

## 16. Build Roadmap

This is a 6–12 month buildout. Don't try to ship it all at once.

### Phase 0 — Foundation (Weeks 1–3)
- Brand identity finalized (logo, type license, photo direction)
- Domain, hosting, repo, design tokens
- Marketing landing page only (capture interest, build mailing list)
- The profit calculator as a standalone page (this alone will drive owner sign-ups)

### Phase 1 — MVP (Weeks 4–14)
- Full marketing site (`/`, `/fleet` browse, `/list-your-car`, destinations)
- Listing creation flow (host onboarding)
- Booking flow (renter side)
- Stripe Connect payouts
- Auth + KYC integration
- Basic admin (approve listings, view bookings, manage users)
- Soft launch in **one market** (LA or Miami) with 10–20 hand-picked vehicles

### Phase 2 — Operations (Weeks 14–22)
- Insurance integration finalized
- Inspection video flow
- Dispute & damage handling
- Concierge dashboard
- Permissions system + employee accounts
- Audit log
- Telematics integration
- Mobile-optimized everything

### Phase 3 — Differentiators (Weeks 22–36)
- Track day program (one partner circuit)
- Production rentals product
- Velare Black tier
- Profit-share program
- AR preview
- Editorial/journal section
- Second + third markets

### Phase 4 — Scale (Month 9+)
- White-label hotel partnerships
- Owner mobile app (notifications, instant approve, calendar)
- Renter mobile app
- Dynamic pricing
- International (Dubai, Monaco, London)

---

## 17. Open Questions

Things to decide before building:

1. **Legal entity & jurisdiction** — Which state are you incorporating in? California, Delaware, or Nevada have different implications for a peer-to-peer rental marketplace.
2. **Insurance partner** — This is the gating decision. Without an insurance carrier signed, you cannot launch. Start conversations *now*.
3. **First market** — LA, Miami, NYC, Vegas, or Dubai? Each has different supply, demand, and regulatory profiles. LA has the most cars but most competition; Miami has the wealthiest tourist density; Dubai has the most spectacular fleet but is harder to operate from the US.
4. **DMV & rental car regulations per state** — Some states require specific licensure to operate as a rental marketplace. Need a transactional attorney before launching.
5. **Build vs. buy on the booking engine** — Are we writing the calendar/booking core ourselves, or licensing something like Hyrecar's white-label? (Recommend: build it. Core IP.)
6. **Founding team** — At minimum need: a senior full-stack engineer (probably you), a designer who has done luxury work, and an operations lead who understands car logistics and insurance.
7. **Funding** — Insurance float alone is a working-capital monster. Even with a partner, you'll need to cover gaps. Plan for $500K–$2M to get to revenue.
8. **Fee transparency vs. competitiveness** — Our 12% commission is the headline. Are we willing to go to 10% for the first 100 owners as a moat-builder?
9. **Trademarks** — "Velare" needs a USPTO search and filing before there's a website. Do this week one.

---

## Appendix A: Page-by-Page Wireframe Notes

### Homepage
- **Hero (100vh)**: Single hero car (rotating Three.js or photo loop), tagline ("Drive what you've earned"), two CTAs ("Browse the Fleet" / "List Your Car")
- **Why Velare**: 3-up — Curation, Owner Economics, Concierge — each with a single sharp image
- **Featured Fleet**: Horizontal scroll of 6–8 hero listings, dark cards with edge-to-edge photos
- **By the Numbers**: Owner-facing stats — avg payout, occupancy, member count
- **Destinations**: 4 city tiles (LA, Miami, NYC, Vegas), tap to enter
- **Member Stories**: Editorial-style, real owner quotes (with photos)
- **Calculator preview**: A teaser of the calculator with a CTA to the full page
- **Footer**: Logo, links, newsletter signup, legal

### Vehicle Detail Page
- Above the fold: gallery (left, 60%) + booking widget (right, 40%, sticky)
- Below: specs table, owner card, location map (with delivery radius), reviews, similar listings
- The booking widget is the conversion engine — keep it tight, instant feedback on price changes

### Calculator Page
- Big input form, single column, one question at a time
- Results render in-place with smooth height transitions
- Comparable listings shown as small cards with photo + rate
- "Beat Turo" comparison module
- CTA at the bottom: "List your car in 5 minutes"

---

## Appendix B: Copy Bank (Starter)

> *Drive what you've earned.*

> Velare Exotics is a peer-to-peer marketplace for the world's most desirable cars. Every vehicle is curated. Every renter is verified. Every detail considered.

> **For Owners.** Earn more from your car than you thought possible. 12% commission. Agreed-value insurance. Free professional photography. Guests vetted before they ever see your listing.

> **For Renters.** Apply once. Drive forever. Access cars you've only seen at concours, delivered to your door.

---

## Appendix C: What Goes in `.env`

```
# Server-only secrets — NEVER expose to client
ANTHROPIC_API_KEY=sk-ant-... # ROTATE the one you shared and put the new one here
DATABASE_URL=postgres://...
STRIPE_SECRET_KEY=sk_live_...
STRIPE_WEBHOOK_SECRET=whsec_...
PERSONA_API_KEY=...
CHECKR_API_KEY=...
RESEND_API_KEY=...
TWILIO_AUTH_TOKEN=...
SESSION_SECRET=...           # 32 random bytes, generate with openssl rand -hex 32
UPSTASH_REDIS_REST_URL=...
UPSTASH_REDIS_REST_TOKEN=...

# Public — safe in NEXT_PUBLIC_ prefix
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_live_...
NEXT_PUBLIC_MAPBOX_TOKEN=...
NEXT_PUBLIC_POSTHOG_KEY=...
NEXT_PUBLIC_SITE_URL=https://velareexotics.com
```

`.env.local` is gitignored. Production secrets live in Vercel env vars + a vault (1Password or Doppler).

---

*End of master plan v1.0. Next document: `DESIGN_SYSTEM.md` once brand direction is locked.*
