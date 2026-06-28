# Case Studies — Verified Numbers from Real OSS Projects

> Every figure below is either (a) a **publicly disclosed** number with the source URL cited inline, or (b) a **derived estimate** explicitly marked as such. Disclosed figures do not carry an "estimate" tag; derived estimates do. No figure here is a promise of what you will earn. See [pricing benchmarks](../data/pricing-benchmarks.yml) for the estimate grid and [platform statuses](../data/platforms.yml) for fee structures.
>
> Two buckets to keep straight while reading:
> - **Sponsorship / donations** — money given *to fund the open-source project itself* (GitHub Sponsors, Open Collective tiers, ad revenue on docs).
> - **Commercial revenue** — money earned from a *separate paid product* built by the same people (Tailwind UI, Sentry's SaaS). Mixing these inflates the "OSS sponsorship" picture. We separate them below.

A consolidated table is at the bottom: [Quick comparison](#quick-comparison).

---

## 1. Astro — Open Collective

**Source:** https://opencollective.com/astrodotbuild (live page, fetched 2026-06-29)

| Metric | Figure | Type |
|---|---|---|
| Total raised (all-time) | **$836,294.61** | Disclosed (public ledger) |
| Annual budget | **$438,118.47** | OpenCollective-displayed estimate |
| Backer tier | $10/mo | Disclosed |
| Sponsor tier | $100/mo | Disclosed |
| Gold tier | $250/mo | Disclosed |
| Theme tier | $200/mo | Disclosed |
| Platinum tier | $1,000/mo | Disclosed |
| Exclusive tier | $10,000/mo | Disclosed |

Astro's ladder spans four orders of magnitude ($10 → $10,000). The $10,000/mo "Exclusive" slot exists because Astro ships a real product (the Astro web framework + integrations ecosystem) that sponsors want to be associated with at the top of the funnel.

**Takeaway:** A wide tier ladder ($10 → $10k) lets a project capture both goodwill tips and serious enterprise sponsorships on the same transparent ledger.

---

## 2. Vue.js — Open Collective

**Source:** https://opencollective.com/vuejs (live page, fetched 2026-06-29)

| Metric | Figure | Type |
|---|---|---|
| Total raised (all-time) | **$852,880.86** | Disclosed (public ledger) |
| Annual budget | **$219,061.00** | OpenCollective-displayed estimate |
| Evan You personal sponsorship, 2016 | ~$8,000/mo | Disclosed (maintainer-reported) |
| Evan You personal sponsorship, 2017 | ~$9,800/mo | Disclosed (maintainer-reported) |

Vue is one of the earliest and most-cited OSS-sponsorship success stories. Evan You's ~$8k–$9.8k/mo in 2016–2017 came from *direct personal sponsorship* of the project's creator — not from Vue's commercial offerings. Vue also self-hosts `vuejs.org/sponsor/` and keeps an in-repo `BACKERS.md`.

**Takeaway:** A flagship framework with a recognized creator can fund a full-time maintainer on sponsorship alone — but that is the exception, not the default outcome.

---

## 3. Vite — Open Collective

**Source:** https://opencollective.com/vite (live page, fetched 2026-06-29)

| Metric | Figure | Type |
|---|---|---|
| Total raised (all-time) | **$162,400.34** | Disclosed (public ledger) |
| Annual budget | **$102,536.16** | OpenCollective-displayed estimate |
| Backer tier | $5/mo | Disclosed |
| Supporter tier | $15/mo | Disclosed |
| Bronze tier | $50/mo | Disclosed |
| Silver tier | $150/mo | Disclosed |
| Gold tier | $500/mo | Disclosed |

Vite's ladder tops out at $500/mo (Gold) — far below Astro's $10k Exclusive — yet it raises a healthy six-figure annual budget. The lower ceiling reflects a younger project still building its sponsor roster; the tight $5 → $500 ladder is easy for a sponsor to climb.

**Takeaway:** You do not need a $10k tier to raise six figures. A clean $5 → $500 ladder with strong adoption works.

---

## 4. Homebrew — Open Collective

**Source:** https://opencollective.com/homebrew (live page, fetched 2026-06-29)

| Metric | Figure | Type |
|---|---|---|
| All-time contributions | **$486,870.56** | Disclosed (public ledger) |
| Backer tier | $5/mo | Disclosed |
| Sponsor tier | $100/mo | Disclosed |

Homebrew runs the simplest ladder here: just two tiers ($5 / $100). It is also the canonical example of **in-kind sponsorship** — MacStadium (macOS CI hardware) and 1Password (secrets) provide services worth real money in exchange for logo placement, logged at fair-market value rather than cash.

**Takeaway:** A two-tier ladder plus in-kind infrastructure sponsors can fund a package nearly every macOS developer touches. Don't overlook credits/services as sponsorship.

---

## 5. Tailwind CSS — sponsorship tiers vs commercial revenue

**Sources:**
- Sponsorship tiers: https://tailwindcss.com/sponsor
- Commercial history (Adam Wathan): https://adamwathan.me/tailwindcss-from-side-project-byproduct-to-multi-mullion-dollar-business/

### Sponsorship tiers (launched ~Jul 2025) — disclosed

| Tier | Price |
|---|---|
| Partner | $5,000/mo |
| Ambassador | $2,500/mo |
| Supporter | $500/mo |
| Individual | $120/yr |

### Derived estimate (NOT official)

- **~$200,000/mo from ~70 companies** — this is a third-party derived figure, not disclosed by Tailwind. Treat as **estimate / reference only**.

### Commercial revenue (Tailwind UI) — disclosed, but NOT sponsorship

This is the critical distinction. Adam Wathan disclosed **~$4m revenue in under 2 years** for Tailwind UI (the paid component product). That is commercial SaaS revenue, *separate* from the sponsorship tiers above. Do not fold it into "OSS sponsorship income."

### 2026 decline (commercial side, not sponsorship)

- Revenue down **~80%** (commercial, Tailwind UI).
- Docs traffic down **~40% from early 2023**.
- **75% of the engineering team was laid off in Jan 2026** (commercial, not sponsorship).

These declines hit the *commercial* product, not necessarily the sponsorship tiers. They are included here because anyone citing Tailwind as a "sponsorship success" must not confuse the two buckets.

**Takeaway:** Tailwind is a top-of-market sponsorship program ($5k Partner) *and* a separate commercial business that hit turbulence in 2026. Cite the tiers; do not cite Tailwind UI revenue as sponsorship income.

---

## 6. Sentry — annual OSS funding outflow (Sentry *gives*, not receives)

**Sources:**
- Annual recap posts: https://blog.sentry.io
- Open Source Pledge: https://opensourcepledge.com

Sentry is a *sponsor* (the direction of money is outbound), not a project being sponsored. They publish their OSS funding each year.

| Year | OSS funding paid out | Type |
|---|---|---|
| 2021 | **$154,999.89** | Disclosed (Sentry blog) |
| 2022 | **$260,028** | Disclosed (Sentry blog) |
| 2023 | **$500,000** | Disclosed (Sentry blog) |
| 2024 | **$750,000** | Disclosed (Sentry blog) |
| 2025 | **$750,000** | Disclosed (Sentry blog) |

Trajectory: roughly **5× growth from 2021 ($155k) to 2024 ($750k)**, then flat at $750k in 2025.

Sentry co-founded the **Open Source Pledge**, whose standard is **$2,000/engineer/yr** paid out to OSS projects. This pledge is the most concrete public benchmark for "how much a company should sponsor per engineer."

**Takeaway:** If you are pitching a company sponsor, the Open Source Pledge's $2,000/engineer/yr is a concrete, citable ask floor — Sentry's own spend grew 5× over four years along this model.

---

## 7. PostHog — per-engineer sponsorship budget

**Source:** https://posthog.com/handbook/marketing/open-source-sponsorship

PostHog gives every team member a **$100/mo budget** to sponsor OSS projects they use. Their published sponsorship table (snapshot):

| Recipient | Monthly |
|---|---|
| Tailwind CSS | $2,500 |
| Django | $2,500 |
| rrweb | $1,000 |
| Tiptap | $149 |
| (others) | … |
| **Total published** | **~$6,609/mo** |

These are disclosed figures from PostHog's public handbook. The $100/mo-per-engineer rule is the internal mechanism; the table is the observable output.

**Takeaway:** PostHog is a template for *inbound* sponsorship — they publish who they fund and at what level. Projects in their dependency graph (Tailwind, Django, rrweb, Tiptap) receive predictable monthly income. Being in a published sponsor's table is worth more than a cold logo placement.

---

## 8. Anthony Fu (antfu) — GitHub Sponsors tier prices vs pass-through fund

**Sources:**
- GitHub Sponsors profile: https://github.com/sponsors/antfu
- Open Collective pass-through fund: https://opencollective.com/antfu

| Metric | Figure | Type |
|---|---|---|
| Current sponsors | 168 | Disclosed (GitHub Sponsors profile) |
| Past sponsors | 872 | Disclosed (GitHub Sponsors profile) |
| Tier *options* | $4 / $8 / … / $2,048/mo | Disclosed (tier price list) |
| "Anthony Fu Fund" all-time raised | **$21,492.46** | Disclosed (Open Collective ledger) |
| Personal income | **Not disclosed** | n/a |

**Two traps to avoid with antfu's numbers:**
1. The $4–$2,048/mo figures are *tier price options*, not his income. Do not multiply a tier by a sponsor count.
2. The "Anthony Fu Fund" ($21,492.46 all-time) is a **pass-through** that redistributes to *other* maintainers — it is **not** his personal income. He has disclosed no personal income number.

**Takeaway:** A prolific maintainer can run both a personal GitHub Sponsors profile and a pass-through fund; the public tier prices tell you nothing about actual take-home. Never infer income from tier options.

---

## 9. Caleb Porzio — $112,680/yr on GitHub Sponsors

**Source:** https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it

| Metric | Figure | Type |
|---|---|---|
| Annual GitHub Sponsors income | **$112,680/yr** | Disclosed (maintainer blog) |
| Monthly equivalent | ~$9,390/mo | Derived from disclosed annual |

Caleb (creator of Livewire and Alpine.js) crossed $100k/yr on GitHub Sponsors. This is one of the few *publicly disclosed personal-income* numbers for an individual maintainer on GitHub Sponsors (0% platform fee on personal accounts).

**Takeaway:** Six-figure personal sponsorship income on GitHub Sponsors is achievable for a maintainer with multiple widely-adopted projects *and* an active sales/content effort — it is not passive.

---

## 10. komorebi (~10k stars) — the "stars ≠ sponsorship" lesson

**Source:** https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/

| Metric | Figure | Type |
|---|---|---|
| Stars | ~10,000 | Disclosed |
| GitHub Sponsors income, 2024 | **$1,861.88** | Disclosed (maintainer blog) |
| Monthly average | ~$155/mo | Derived |
| Monthly range | $92.35 (Jan) → $229.00 (Nov) | Disclosed |

komorebi is a tiling window manager for Windows with ~10k stars — a "popular" repo by the star-count proxy. Yet total sponsorship for 2024 was **$1,861.88**, averaging ~$155/mo. This is the single most important counterexample in this file.

**Takeaway:** Star count is a popularity proxy, not a pricing metric. 10k stars without active sales converted to under $1,900 for the year. The real drivers are unique monthly visitors (GitHub Traffic), package downloads, and audience-to-sponsor fit — plus the maintainer actually *selling*. See [the 1000-stars playbook](1000-stars-playbook.md) for the active-sales approach.

---

## 11. DigitalOcean OSS credits — free cloud credits, not cash

**Source:** https://github.com/Aniket-508/awesome-oss-perks

| Star tier | Annual credits | Type |
|---|---|---|
| 100+ | $60/yr | Disclosed |
| … (tiered) | … | Disclosed |
| 10,000+ | up to $20,000/yr | Disclosed |

**Critical label:** these are **free cloud credits tiered by stars — NOT cash sponsorship.** They are in-kind value (hosting/compute) you can log at fair-market value, but they do not pay a maintainer's rent. Useful as an in-kind anchor alongside cash sponsors.

**Takeaway:** Star-tiered credits are the easiest "sponsorship" to claim (no sales call required), but they are in-kind, not income. Pair them with cash sponsors from [platforms](../data/platforms.yml).

---

## 12. Ad & newsletter pricing anchors

These are disclosed rate-card / pricing-page figures, useful as anchors when you price your own docs-site ad or newsletter slot. See the [pricing benchmarks](../data/pricing-benchmarks.yml) `derivation_method` for how to re-derive from your own traffic.

### EthicalAds (publisher side) — disclosed

**Source:** https://www.ethicalads.io/publishers/calculator/

| Metric | Figure |
|---|---|
| Publisher revenue share | 70% |
| Effective CPM (EU + NA traffic) | $2.25–$2.75 (midpoint ~$2.50) |
| Minimum payout | $50 |

Formula: `monthly_pageviews / 1000 × ~$2.50`. Requires ~50,000 monthly pageviews to join; one ad per page, above the fold; developer-only audience; no newsletter/README/podcast slots.

### Carbon Ads (advertiser entry) — disclosed

**Source:** https://carbonads.net

| Metric | Figure |
|---|---|
| Advertiser minimum | $5,000–$10,000/mo over 60–90 days |
| Cumulative paid to publishers | $120M+ |
| Publisher per-README benchmark | not public (sales-assisted) |

Official domain is **carbonads.net** (not .com). Curated 350+ tech sites; sales-assisted, no self-serve; no newsletter/README placement.

### JavaScript Weekly (Cooperpress) — disclosed rate card, Q2 2024

**Source:** https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf

| Metric | Figure |
|---|---|
| Subscribers | 179,802 |
| Open rate | 41% |
| Primary sponsorship (per issue) | $3,590 |
| Sponsored links (per issue) | $1,190 |
| Job listing | $180 |

### Refactoring — third-party-reported 2023 rates

**Source:** https://refactoring.fm

| Metric | Figure |
|---|---|
| Subscribers | 170,000+ |
| Primary sponsorship | $2,000 |
| Secondary sponsorship | $800 |
| Sponsored guest post | $5,000 |

**Takeaway:** A developer newsletter with ~170k–180k subs commands **$2,000–$3,590 per issue** for the primary slot. If you run a real dev newsletter, that is your anchor; re-derive via `subs × open_rate × CTR × target_cpc` (see [pricing benchmarks](../data/pricing-benchmarks.yml)).

---

## Quick comparison

| Project / person | Bucket | Headline number | Source |
|---|---|---|---|
| Astro | Sponsorship (OC) | $836,294.61 total raised | opencollective.com/astrodotbuild |
| Vue.js | Sponsorship (OC) | $852,880.86 total raised | opencollective.com/vuejs |
| Vite | Sponsorship (OC) | $162,400.34 total raised | opencollective.com/vite |
| Homebrew | Sponsorship (OC) | $486,870.56 all-time | opencollective.com/homebrew |
| Tailwind CSS | Sponsorship tiers | $120/yr → $5,000/mo tiers | tailwindcss.com/sponsor |
| Tailwind CSS | Commercial (NOT sponsorship) | ~$4m revenue, then ~80% decline 2026 | adamwathan.me |
| Tailwind CSS | Derived estimate | ~$200,000/mo from ~70 cos (estimate / reference only) | third-party derived |
| Sentry | Sponsor (outflow) | $154,999.89 (2021) → $750,000 (2025) | blog.sentry.io |
| PostHog | Sponsor (outflow) | ~$6,609/mo published table; $100/mo per engineer | posthog.com/handbook |
| Anthony Fu | Sponsorship (personal) | Tier options $4–$2,048/mo; fund $21,492.46 (pass-through, not income) | github.com/sponsors/antfu |
| Caleb Porzio | Sponsorship (personal) | $112,680/yr (~$9,390/mo) | calebporzio.com |
| komorebi | Sponsorship (personal) | $1,861.88 in 2024 (~$155/mo) | lgug2z.com |
| DigitalOcean | In-kind credits (not cash) | $60/yr (100+) → up to $20,000/yr (10k+) | github.com/Aniket-508/awesome-oss-perks |
| EthicalAds | Docs-site ad | 70% revshare, ~$2.50 CPM | ethicalads.io |
| Carbon Ads | Docs-site ad | $5k–$10k/mo advertiser min | carbonads.net |
| JavaScript Weekly | Newsletter | $3,590/issue primary (179,802 subs) | cooperpress.com |
| Refactoring | Newsletter | $2,000 primary (170k+ subs) | refactoring.fm |

## How to use these

- **Pitching a company:** cite the Open Source Pledge ($2,000/engineer/yr) and Sentry/PostHog as companies that publish their spend. Concrete, citable, not a guess.
- **Pricing a docs ad:** anchor to EthicalAds ~$2.50 CPM (`pageviews / 1000 × $2.50`) — estimate / reference only.
- **Pricing a newsletter:** anchor to JS Weekly $3,590/issue at ~180k subs; scale down by your subscriber count.
- **Setting a tier ladder:** copy Vite ($5 → $500) or Astro ($10 → $10,000) depending on ambition; see [the 1000-stars playbook](1000-stars-playbook.md).
- **Reality check:** keep komorebi ($1,861.88 at 10k stars) on hand whenever star count tempts you to skip the sales work.

Related: [1000-stars playbook](1000-stars-playbook.md), [launch plan](launch-plan.md), [platforms](../data/platforms.yml), [pricing benchmarks](../data/pricing-benchmarks.yml), [sponsor taxonomy](../data/sponsor-types.yml).
