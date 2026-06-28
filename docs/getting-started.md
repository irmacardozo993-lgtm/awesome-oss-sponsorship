# Getting Started

Orientation guide for turning an open-source project into sponsored work.
Start here, then follow the link map at the bottom to go deep on any platform.

> **If you only read one thing:** Sponsorship is a sales channel, not a star-count
> reward. Stars are a popularity proxy — the real pricing drivers are **unique
> monthly visitors** (GitHub Traffic, self-reported, 14-day rolling window),
> **package downloads** (npm / PyPI / Docker Hub), and **audience-to-sponsor fit**.
> The fastest credible path is: pick a platform → add `.github/FUNDING.yml` →
> publish tiers → list your inventory slots → start outbound outreach with a
> rate card anchored to your own traffic. Skip the platforms that pivoted away
> from sponsorship (Polar → AI billing, Algora → recruiting). 10k stars does
> **not** auto-convert: komorebi (~10k stars) made ~$155/mo on GitHub Sponsors
> in 2024 ([source](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/)).

## Table of contents

- [Who this is for](#who-this-is-for)
- [The 5-minute path](#the-5-minute-path)
- [Which platform first?](#which-platform-first)
- [Pricing in one paragraph](#pricing-in-one-paragraph)
- [Link map](#link-map)

## Who this is for

| You are | Start with | Why |
|---------|-----------|-----|
| **100-star maintainer** (early CLI/SDK, first users) | GitHub Sponsors + `.github/FUNDING.yml` | 0% personal fees, native GitHub button, no traffic minimum. Realistic for inbound tips; outbound deals are still small. |
| **1k-star maintainer** (growing devtool, real download base) | GitHub Sponsors + Open Collective + a rate card | Enough traffic to price docs/README slots. OC gives you a public ledger if you pay contributors. |
| **10k-star maintainer** (established project, docs traffic) | Open Collective (fiscal host) + EthicalAds + tiered README grid | Multiple sponsors/vendors need a legal umbrella; docs traffic earns CPM ad revenue; README logo grid is the dominant pattern. |
| **Indie dev / solo maintainer** | GitHub Sponsors (0%) + Buy Me a Coffee (one-off tips) | Solo = skip the fiscal host. Pair recurring (Sponsors) with a tip jar (BMC). |
| **Devtool / CLI / SDK maintainer** | GitHub Sponsors + thanks.dev (dependency-tree inbound) | Companies that depend on you can auto-fund via thanks.dev; Sponsors captures direct relationships. |
| **Maintainer who also runs a newsletter** | GitHub Sponsors + Paved (newsletter ads) | Newsletter inventory is the highest $/impression; Paved is newsletter-only. |
| **Maintainer shipping a paid SaaS/AI product** | Polar (Merchant-of-Record) — **not** for sponsorship | Polar handles global tax/billing for usage-based products. It is no longer an OSS sponsorship tool. |

## The 5-minute path

1. **Pick a platform.** Solo? GitHub Sponsors (0% personal fee). Multiple
   contributors/vendors? Open Collective (fiscal host + public ledger). See
   [Which platform first?](#which-platform-first).
2. **Add `.github/FUNDING.yml`.** This wires the "Sponsor" button on your repo
   and is the universal CTA. See the copy-paste template:
   [funding-yml-example](../templates/funding-yml-example.md). Current supported
   keys (12): `community_bridge`, `github` (single user OR array up to 4),
   `issuehunt`, `ko_fi`, `liberapay`, `open_collective`, `patreon`, `tidelift`
   (`PLATFORM/PACKAGE`; platforms: npm, pypi, rubygems, maven, packagist,
   nuget), `polar`, `buy_me_a_coffee`, `thanks_dev` (`u/gh/USERNAME`),
   `custom` (single URL OR array up to 4; any URL containing a colon MUST be
   wrapped in quotes). **Not** supported: `otechie`, `givebutter`,
   `lfx_crowdfunding`.
3. **Set your tiers.** GitHub Sponsors: up to 10 one-time + 10 monthly, max
   $12,000/mo; **price is immutable once published** — to change a price you
   retire the tier and recreate it. Anchor tiers to real disclosed ladders
   (Vite: $5/$15/$50/$150/$500; Astro: $10/$100/$200/$250/$1,000/$10,000) in
   [case-studies.md](case-studies.md) — but label your own numbers
   **estimate / reference only**.
4. **List your inventory slots.** You are selling *exposure*, not stars. Use the
   slot taxonomy in [../data/sponsor-types.yml](../data/sponsor-types.yml):
   README top banner, README bottom logo grid (the dominant pattern — dynamic
   SVG, never edit the README), docs-site ad, release-note sponsor, newsletter.
   Each slot has a different value/intrusiveness/conversion profile.
5. **Start outreach.** Build a one-page [rate card](../templates/rate-card.md)
   anchored to **your** traffic (pageviews / 1000 × ~$2.50 for docs ads; subs ×
   open rate × CTR for newsletters), then send the
   [cold-email](../templates/cold-email.md) template to companies that appear in
   your Popular Referrers (GitHub Traffic) or that file issues. Price at the
   **low** end of the estimate range until you close 3 deals.

## Which platform first?

| Need | Platform | Fee (reference only) | Notes |
|------|----------|---------------------|-------|
| Solo, 0% fees, native GitHub button | [GitHub Sponsors](github-sponsors.md) | 0% personal / up to 6% org | Mainland China NOT supported; HK/Macau SAR are. |
| Public ledger, pay multiple contributors | [Open Collective](open-collective.md) | $0 / $60 / $320 per fiscal host; or 5% crowdfunding | 501(c)(6) via OSC; integrates with Sponsors + thanks.dev. |
| Your OSS project ships a paid SaaS/AI product | [Polar](polar.md) | 5%+50¢ → 3.40%+30¢ by plan | Merchant-of-Record (global tax). **Not sponsorship.** |
| Docs-site ad revenue (decouples from stars) | [Ad networks](ad-networks.md) | EthicalAds ~$2.50 CPM publisher | Needs ~50k monthly pageviews; dev-only audience. |

## Pricing in one paragraph

There is no standardized public market tying $/month to star count. Use the
[estimate grid](../data/pricing-benchmarks.yml) (monthly USD by star tier ×
slot) **only** as an internal anchor — every cell is **estimate / reference
only**. Re-derive your own number from traffic: docs-site ad ≈
`monthly_pageviews / 1000 × ~$2.50` (EthicalAds publisher CPM, 70% revshare);
newsletter ≈ `subs × open_rate × CTR × target_cpc`, anchored to JavaScript
Weekly's $3,590/issue at 180k subs
([source](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf)).
If you can't show traffic or conversion data, price at the low end and raise
after the first 3 closed deals. Real disclosed anchors (Astro $836k total
raised, Vue $852k, Vite $162k, Sentry's $750k/yr outflow, Caleb Porzio's
$112,680/yr) are in [case-studies.md](case-studies.md) — cite, don't copy.

## Link map

**Docs (this directory):**

- [github-sponsors.md](github-sponsors.md) — deep guide: eligibility, regions, setup, tiers, fees, README display
- [open-collective.md](open-collective.md) — fiscal hosts, OSC 501(c)(6), public ledger, plans/fees
- [polar.md](polar.md) — the pivot to AI billing / Merchant-of-Record; when it fits vs not
- [ad-networks.md](ad-networks.md) — EthicalAds, Carbon Ads, BuySellAds, Passionfroot, Paved
- [pricing.md](pricing.md) — pricing sponsorship: estimate grid + how to derive your own number
- [readme-monetization.md](readme-monetization.md) — README & surface monetization (logo grids, BACKERS.md)
- [outreach.md](outreach.md) — finding sponsors proactively
- [sponsor-kit.md](sponsor-kit.md) — building a sponsor kit (guide)
- [1000-stars-playbook.md](1000-stars-playbook.md) — the 1k-star sponsorship playbook
- [launch-plan.md](launch-plan.md) — cold-start distribution plan
- [case-studies.md](case-studies.md) — verified disclosed numbers (Astro, Vue, Vite, Sentry, Tailwind, …)
- [faq.md](faq.md) — frequently asked questions

**Templates (`../templates/`):**

- [funding-yml-example.md](../templates/funding-yml-example.md) — copy-paste `.github/FUNDING.yml`
- [rate-card.md](../templates/rate-card.md) — one-page sponsor rate card
- [cold-email.md](../templates/cold-email.md) — outbound outreach email
- [sponsor-kit.md](../templates/sponsor-kit.md) — full media kit (TLDR-style)

**Tools (`../tools/`):**

- [sponsor-fit-score.md](../tools/sponsor-fit-score.md) — score a sponsor's fit before outreach

**Data (`../data/`):** the source of truth — read these first:

- [platforms.yml](../data/platforms.yml) — 17 platforms, status/fees/payout
- [pricing-benchmarks.yml](../data/pricing-benchmarks.yml) — real anchors + estimate grid
- [sponsor-types.yml](../data/sponsor-types.yml) — slot taxonomy, sponsor kinds, deal models

**Repo root:**

- [../README.md](../README.md) — the Awesome List itself (platform comparison table)
- [../README.zh-CN.md](../README.zh-CN.md) — Chinese edition
- [../CONTRIBUTING.md](../CONTRIBUTING.md) — how to add/correct a platform (cite official sources)
