# Developer Ad Networks

Comparison of ad networks that monetize **developer audience inventory** — docs
sites, newsletters, podcasts. Ads decouple revenue from star count: a
high-traffic docs site can earn more from CPM ads than a high-star repo with no
traffic.

All figures are **estimate / reference only** unless a source URL is cited
inline (then it is a publicly disclosed figure). Re-verify at each network's
official page before signing up.

## Table of contents

- [At a glance](#at-a-glance)
- [EthicalAds](#ethicalads)
- [Carbon Ads](#carbon-ads)
- [BuySellAds](#buysellads)
- [Passionfroot](#passionfroot)
- [Paved](#paved)
- [Comparison table](#comparison-table)
- [Revenue math](#revenue-math)
- [Choosing by inventory type](#choosing-by-inventory-type)

## At a glance

| Network | Model | Inventory | Key gate | Status |
|---------|------|-----------|----------|--------|
| [EthicalAds](https://www.ethicalads.io) | CPM, self-serve | docs/site display | ~50k monthly pageviews, dev-only | alive |
| [Carbon Ads](https://www.carbonads.net) | CPC, sales-assisted | curated site display | advertiser min $5k–$10k/mo | alive (BuySellAds sub-network) |
| [BuySellAds](https://www.buysellads.com) | managed + directory | email/native/sponsored/display/podcast/custom | contact required | alive (parent umbrella) |
| [Passionfroot](https://www.passionfroot.me) | creator marketplace | newsletter/YouTube/LinkedIn/X/TikTok | pivoted to "Zest" B2B GTM | alive_pivoted |
| [Paved](https://www.paved.com) | flat-fee + PPC | newsletter only | 25k subs (flat) / 1M impressions (PPC) | alive |

> **Two pivots/sub-networks to remember:** Carbon Ads is a **BuySellAds
> sub-network** (its official domain is **carbonads.NET**, not .com, and
> dashboards live on sell.buysellads.com). Passionfroot **pivoted to "Zest"**,
> a B2B GTM platform — it is now a brand-deal marketplace for newsletter
> creators, not a generic ad network.

## EthicalAds

The privacy-first default for OSS docs sites.

- **Model:** CPM. Publisher **70% revshare**; effective **~$2.25–$2.75 CPM
  (midpoint ~$2.50)** for EU + North America traffic
  ([source](https://www.ethicalads.io/publishers/calculator/)).
- **Requirements:** developer-only audience; **one ad per page**; must be
  **above the fold**; **~50,000 monthly pageviews** to join.
- **No** newsletter, podcast, or README placement — display/banner only.
- **Privacy:** cookie-free, no tracking, GDPR-compliant (no cookie banner),
  never loads third-party scripts/pixels. Acceptable Ads approved. Fully open
  source.
- **Payout:** min $50; PayPal, OpenCollective, GitHub Sponsors, or bank via
  Stripe. Cited publishers: ESLint, Flask, daily.dev. 35M dev impressions/mo.
- **Best for:** OSS project **documentation sites** with real traffic. Not a
  fit for low-traffic repos.

## Carbon Ads

The curated, sales-led developer/design ad network.

- **Model:** CPC, native; **sales-assisted, no self-serve**. Official domain is
  **carbonads.NET** (not .com).
- **Requirements (advertiser side):** **$5,000–$10,000/month** investment over
  a 60–90 day period
  ([source](https://carbonads.net)). Curated **350+ hand-picked tech sites**
  across 4 categories (Frontend & Frameworks 148, Dev Tools & Infra 119,
  Design & Creative 49, AI & Emerging 36).
- **Publisher payout:** **no public per-publisher benchmark**; $120M+ paid to
  publishers cumulatively. Threshold, schedule, and methods absent from the
  homepage and /join (unverified).
- **Formats:** native non-intrusive (Cover + Classic); pixel-based (not cookie)
  tracking. Brand clients: MongoDB, GitLab, Atlassian, Adobe, AWS.
- **Best for:** established developer/design **websites** with a curated
  audience. No newsletter/email/podcast. Direct site targeting is "generally
  discouraged."

## BuySellAds

The parent umbrella; Carbon Ads (developers) and Coin.Network (crypto) are
sub-networks.

- **Model:** managed contextual advertising + self-serve directory; **no
  primary CPM/CPC/flat disclosed** — no pricing transparency.
- **Formats:** email, native, sponsored content, display, podcast
  (short-form audio), custom placements (OOH, site sponsorships, browser ads).
- **Region:** global; verticals: Business, AI, Crypto, Design, Developer.
- **Payout:** "reliable payment schedule" + "complimentary accounting support"
  mentioned; net terms, threshold, and methods not disclosed.
- **Publishers:** Axios, Reuters, Morning Brew, Dribbble, MDN, CodePen.
- **Best for:** **multi-format monetization** across site + newsletter +
  podcast with a human account team. For a dev-focused list, Carbon Ads is the
  more targeted entry point; BSA itself is the broader multi-vertical option.

## Passionfroot

Pivoted to **"Zest"** — a B2B GTM platform. Canonical domain is
**passionfroot.ME** (not .com, which has a TLS cert error).

- **Model:** creator marketplace for inbound brand deals.
  - **Self-managed deals:** **2% fee** (brand covers).
  - **Platform-matched deals:** **15% fee** (includes payment fees).
  - Brand-side pricing **not public** (unverified).
  - Creator tiers: Free ($0/mo, no paid creator tiers).
- **Inventory:** X, Beehiiv, Substack, LinkedIn, YouTube, Instagram, TikTok.
- **Payout:** via "FrootWallet"; no out-of-pocket/upfront costs; min threshold
  and schedule unverified.
- **Testimonials:** HubSpot, Figma, Intercom, ElevenLabs, Replit, Framer.
- **Best for:** OSS authors who **also run a newsletter** (Beehiiv/Substack)
  and want inbound brand deals. B2B/tech lean; no obvious public marketplace
  (brand discovery is AI-curated). Evolved from a creator sponsor-storefront
  into an AI-powered B2B GTM platform.

## Paved

Newsletter-only monetization. No podcast/blog/docs/README.

- **Model:** two options.
  - **Direct/scheduled:** flat-fee (publisher sets rates for direct
    partnerships). Min **25,000 subscribers**.
  - **Dynamic/native:** PPC (paid per real human click). Min **1,000,000
    monthly impressions**.
- **Scale:** **3,000+ premium newsletters, 253M subscribers.**
- **Payout:** "automated payouts"; "immediate payouts from advertisers when
  they book placements"; Paved handles invoicing/contracts/payouts with payment
  protection. Revenue-share %, threshold, and methods unverified.
- **Manual ad review**; publisher can refuse advertisers; tracks
  open/click/conversion.
- **Best for:** maintainers who run a **real developer newsletter**. The 25k-sub
  / 1M-impression floors are the key gates. Not relevant for repo/README/docs
  monetization.

## Comparison table

| Criterion | EthicalAds | Carbon Ads | BuySellAds | Passionfroot | Paved |
|-----------|-----------|------------|------------|--------------|-------|
| Status | alive | alive | alive | alive_pivoted (→Zest) | alive |
| Model | CPM | CPC (sales-assisted) | managed + directory | marketplace (brand deals) | flat-fee + PPC |
| Inventory | docs/site display | curated site display | email/native/sponsored/display/podcast/custom | newsletter/YouTube/LinkedIn/X/TikTok | newsletter only |
| Self-serve? | yes | no | no (contact) | platform-matched or self-managed | yes (direct) |
| Audience gate | ~50k pageviews, dev-only | curated 350+ sites | contact required | pivoted to B2B GTM | 25k subs / 1M impressions |
| Publisher payout terms | public ($50 min; PayPal/OC/Sponsors/Stripe) | **not public** | not disclosed | via FrootWallet (unverified) | automated (rev-share % unverified) |
| Transparency | high (open source, CPM public) | advertiser min public; publisher not | low (no pricing) | low (brand pricing not public) | medium (floors public; rev-share not) |
| Newsletter? | no | no | yes | yes | yes (only) |
| Podcast? | no | no | yes | no | no |
| README? | no | no | no | no | no |
| Best for | docs site | curated dev/design site | multi-format site+news+podcast | newsletter brand deals | newsletter ads |

## Revenue math

**EthicalAds (docs site):**

```
monthly_revenue ≈ monthly_pageviews / 1000 × ~$2.50
```

Example (estimate / reference only): 100,000 monthly pageviews ≈ 100 × $2.50 ≈
**$250/mo**. The ~$2.50 is the effective publisher CPM after the 70% revshare,
for EU+NA traffic ([source](https://www.ethicalads.io/publishers/calculator/)).
Lower-geo traffic pays less.

**Carbon Ads:** publisher payout terms are **not public** — there is no
per-publisher CPM benchmark to compute from. Revenue is sales-assisted and
negotiated; you only know the advertiser side ($5k–$10k/mo over 60–90 days,
[source](https://carbonads.net)).

**Newsletter anchors (publicly disclosed — cite, don't present as a quote to
your own list):**

| Newsletter | Subs | Open rate | Primary/issue | Other slots | Source |
|------------|------|-----------|---------------|-------------|--------|
| JavaScript Weekly (Cooperpress, Q2 2024) | 179,802 | 41% | $3,590 | Sponsored Links $1,190; Job $180 | [media kit](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf) |
| Refactoring (2023, third-party-reported) | 170,000+ | — | $2,000 | Secondary $800; sponsored guest post $5,000 | [refactoring.fm](https://refactoring.fm) |

To derive your own newsletter number (estimate / reference only):
`subs × open_rate × CTR × target_cpc`, anchored to the JS Weekly figure.

## Choosing by inventory type

| You have | Pick | Why |
|----------|------|-----|
| A **docs site** with ≥50k monthly pageviews | EthicalAds | Privacy-first, self-serve, ~$2.50 CPM, dev-only |
| A **curated dev/design site** with brand demand | Carbon Ads | Sales-led, premium brand clients, but publisher terms not public |
| A **site + newsletter + podcast** bundle | BuySellAds | Multi-format, human account team, but no pricing transparency |
| A **newsletter** (Beehiiv/Substack) seeking inbound brand deals | Passionfroot | 2% self-managed / 15% matched; pivoted to Zest B2B GTM |
| A **newsletter** with ≥25k subs or ≥1M impressions | Paved | Newsletter-only scale (3,000+ newsletters, 253M subs) |
| A **README** or repo only | none of these | All five are site/newsletter/podcast — not README. Sell README slots directly via a [rate card](../templates/rate-card.md) instead. |

## See also

- [getting-started.md](getting-started.md) — the 5-minute path and link map
- [../data/platforms.yml](../data/platforms.yml) — source of truth (ad network entries)
- [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml) — estimate grid + ad/newsletter anchors
- [../templates/rate-card.md](../templates/rate-card.md) — sponsor rate card
- [case-studies.md](case-studies.md) — verified disclosed ad/newsletter pricing
