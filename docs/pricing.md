# Pricing Sponsorship

How to set a defensible monthly rate for each sponsor slot. The short version: **stars are a proxy, traffic + downloads + audience fit are the real drivers, and you price at the low end until you have three closed deals to anchor against.**

Every figure on this page is **estimate / reference only** unless it carries an inline source URL — those are publicly disclosed numbers you can cite directly.

> Canonical numbers live in [`../data/pricing-benchmarks.yml`](../data/pricing-benchmarks.yml) (estimate grid + anchors) and [`../data/sponsor-types.yml`](../data/sponsor-types.yml) (slot/kind/deal taxonomy). This doc explains how to use them. Do not contradict the data files.

---

## 1. Why star count is a proxy, not a metric

Stars measure **popularity at one moment**, not value to a sponsor. A repo can have 10k stars and almost no active install traffic; another can have 1k stars and 500k monthly package downloads. Sponsors pay for **reach to developers at the moment of consideration** — that is traffic and downloads, not a star button.

The hard proof, from a maintainer's own 2024 breakdown (source URL below):

| Repo | Stars | GitHub Sponsors income 2024 | Lesson |
|---|---|---|---|
| komorebi | ~10,000 | **$1,861.88** total (~$155/mo avg; range $92 Jan → $229 Nov) | 10k stars did **not** auto-convert to meaningful sponsorship without active sales. |

Source: https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/

Contrast with a solo maintainer who actively sold:

| Maintainer | Annual GitHub Sponsors | Notes |
|---|---|---|
| Caleb Porzio | **$112,680/yr** (~$9,390/mo) | Active sales + tiered story. |

Source: https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it

Stars get you *into the conversation*. They do not close deals. Use the star tier only as a **first-pass bucket**; then re-derive from real drivers (section 2).

---

## 2. The derivation method (always more credible than a star table)

For each slot, compute a number from measurable signals. Three signals, in priority order:

1. **Unique monthly visitors** — from GitHub Traffic (admin-only, 14-day rolling window; see [sponsor-kit.md](sponsor-kit.md) for how to pull it). Self-reported, short window, so present it honestly.
2. **Package downloads** — npm weekly downloads, PyPI downloads (via `pypistats` / BigQuery), Docker Hub pulls. These are public and sponsor-verifiable, so they carry more weight than Traffic.
3. **Audience-to-sponsor fit** — does your user base overlap the sponsor's buyer? A 5k-star testing tool used by QA engineers is worth more to a CI vendor than a 50k-star general utility is to a niche database company.

Per-slot formulas (all outputs are **estimates / reference only**):

| Slot | Derivation |
|---|---|
| Docs site ad | `monthly_pageviews / 1000 × ~$2.50` (EthicalAds publisher CPM, 70% revshare, EU+NA traffic). Source: https://www.ethicalads.io/publishers/calculator/ |
| Newsletter | `subs × open_rate × CTR × target_cpc`, **or** anchor to JavaScript Weekly: **$3,590/issue** primary spot at 179,802 subs / 41% open (Q2 2024). Source: https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf |
| README slot | Stars are a proxy; real drivers = unique monthly visitors + npm/PyPI/Docker pulls + audience-to-sponsor fit. Use the grid in section 3 as the starting anchor. |

If you cannot show traffic or conversion data, fall back to the grid — but price at the **low end** (section 4).

---

## 3. The estimate grid (starting anchor, not a price list)

All cells are **estimates / reference only**. Ranges reflect typical observed deals; outliers (Tailwind-scale) sit far above the 50k row. Full machine-readable grid: [`../data/pricing-benchmarks.yml`](../data/pricing-benchmarks.yml).

Monthly USD by star tier × slot:

| Stars | README top banner | README bottom logo | README bottom text | Docs site ad | Release note | Newsletter / issue |
|---:|---:|---:|---:|---:|---:|---:|
| 100 | 100–300 | 50–150 | 20–75 | 10–40 | 50–150 | 30–100 |
| 500 | 200–500 | 100–300 | 50–150 | 25–80 | 100–300 | 100–250 |
| 1,000 | 400–1,000 | 200–600 | 100–300 | 50–200 | 200–600 | 200–500 |
| 5,000 | 1,000–3,000 | 500–1,500 | 250–750 | 150–600 | 500–1,500 | 500–1,500 |
| 10,000 | 2,000–6,000 | 1,000–3,000 | 500–1,500 | 300–1,500 | 1,000–3,000 | 1,000–2,500 |
| 50,000 | 5,000–15,000 | 3,000–10,000 | 1,500–5,000 | 1,000–5,000 | 2,500–8,000 | 2,500–7,000 |

Slot value/intrusiveness taxonomy (from [`../data/sponsor-types.yml`](../data/sponsor-types.yml)): top banner = high value / medium intrusiveness; bottom logo = medium-high / low; bottom text = low / low; docs ad = medium / low; release note = medium / low; newsletter = high / medium. Price roughly tracks value.

---

## 4. Anchor to real case studies (publicly disclosed)

Use these as **citable comparables** when a sponsor asks "what do others pay." All figures are from live public ledgers or maintainer blogs (URLs inline).

| Project | Total raised | Annual (est, on ledger) | Tier ladder (monthly) | Source |
|---|---:|---:|---|---|
| Astro | $836,294.61 | $438,118.47 | Backer $10 / Sponsor $100 / Gold $250 / Theme $200 / Platinum $1,000 / Exclusive $10,000 | https://opencollective.com/astrodotbuild |
| Vue.js | $852,880.86 | $219,061.00 | (Evan You historical ~$8,000/mo 2016 → ~$9,800/mo 2017) | https://opencollective.com/vuejs |
| Vite | $162,400.34 | $102,536.16 | Backer $5 / Supporter $15 / Bronze $50 / Silver $150 / Gold $500 | https://opencollective.com/vite |
| Homebrew | $486,870.56 (all-time contributions) | — | Backer $5 / Sponsor $100 | https://opencollective.com/homebrew |
| Tailwind CSS | — | derived ~$200,000/mo from ~70 companies (**third-party derived, not official**) | Partner $5,000 / Ambassador $2,500 / Supporter $500 / Individual $120/yr | https://tailwindcss.com/sponsor |

Notes:
- Astro/Vue/Vite/Homebrew totals are **public OpenCollective ledger figures** (disclosed). The "annual" number is an estimate computed on the ledger page, not a maintained-promise.
- Tailwind's ~$200k/mo is **derived by third parties, not official** — present it only as "reportedly" and link the sponsor page, not the derived number, as the source of truth. (Tailwind's commercial revenue from Tailwind UI is a separate stream and not sponsorship.)
- The komorebi and Caleb Porzio rows in section 1 are the two cautionary/encouraging anchors: **stars without sales ≈ $155/mo; sales without scale can still clear $100k/yr.**

---

## 5. The rule: price at the LOW end, raise after 3 closed deals

When you have no traffic or conversion data, you have no leverage. The credible move:

1. **Price at the low end of your star-tier cell** in the grid above.
2. Pitch 50 prospects (see [outreach.md](outreach.md)).
3. After **3 closed deals at or above that price**, you have a market signal. Raise the published rate 15–25%.
4. Repeat. Re-derive from real drivers (section 2) as soon as you have traffic/downloads, and switch to the derivation number once it exceeds the grid low end.

Why low-end-first: a published high price with zero deal history looks aspirational and scares off the sponsors you can actually close. A low price with three logos in the README looks like momentum.

---

## 6. Region multipliers and the RMB domestic band

Estimates / reference only.

| Region | Multiplier | Notes |
|---|---|---|
| Global (USD) | 1.0 | Default. Quote in USD for international sponsors. |
| RMB domestic (China) | USD × 6–7 for the "face" RMB number | Mainland-China sponsors cannot use GitHub Sponsors (PRC not supported; HK/Macau SAR are). Domestic sponsors often pay in a **¥500–¥5,000/mo band for ~1k-star repos** via WeChat/Alipay direct transfer or a domestic fiscal path. |

Domestic-band guidance (estimate / reference only, for ~1k-star repos):

| Slot | RMB/month (domestic) |
|---|---|
| README top banner | ¥2,000–¥5,000 |
| README bottom logo | ¥1,000–¥3,000 |
| README bottom text | ¥500–¥1,500 |
| Docs site ad | ¥500–¥1,500 |

If you serve a domestic audience, do not quote USD-only — RMB face numbers land better with Chinese sponsors, and you need a non-GitHub-Sponsors collection path (Open Collective via a fiscal host, or direct transfer). See [faq.md](faq.md) for the China-country question.

---

## 7. Deal models: one-time vs monthly vs annual vs fixed+affiliate

The slot base price is a **monthly** number. The deal model modifies it. Full taxonomy in [`../data/sponsor-types.yml`](../data/sponsor-types.yml); modifiers from [`../data/pricing-benchmarks.yml`](../data/pricing-benchmarks.yml).

| Deal model | Price behavior | When to use |
|---|---|---|
| **One-time** (display, 12mo) | ~8–10× the monthly rate, discounted 15–20% vs paying monthly | A sponsor wants a fixed budget and no recurring commitment. Good for release-aligned moments. |
| **Monthly recurring** | Base rate, no discount | Default for GitHub Sponsors / Open Collective tiers. Predictable MRR, lowest sponsor friction. |
| **Annual (paid yearly)** | ~10–12× monthly, discounted 15–20% | Sponsors prefer annual for budgeting; you get cash up front. Offer as the "best value" option. |
| **Affiliate (pure)** | $0 fixed; 10–30% recurring or $5–$50 flat per converted user (volume-dependent) | Performance-only. Use when the sponsor wants signups/installs, not brand. Track in `affiliate-tracker.csv` (see [outreach.md](outreach.md)). |
| **Fixed + affiliate (hybrid)** | Lower fixed retainer (50–70% of slot base) + commission on conversions | Best balance of predictability + upside. The default for ecosystem/adjacent vendors and founder/growth leads. |
| **In-kind / barter** | Face-value of credits/services; log at fair-market value | Hosting, CI, DNS, secrets (e.g., MacStadium, 1Password for Homebrew). Real value — record it as sponsorship. DigitalOcean gives free cloud credits tiered by stars ($60/yr at 100+ → up to $20,000/yr at 10,000+); these are **credits, not cash**. Source: https://github.com/Aniket-508/awesome-oss-perks |

Sponsor-kind typical deals (estimate / reference only, from [`../data/sponsor-types.yml`](../data/sponsor-types.yml)):

| Sponsor kind | Typical deal |
|---|---|
| Individual backer | $2–$50/mo |
| Company using your project | $100–$5,000+/mo |
| DevRel / dev marketing | $250–$10,000/mo or campaign |
| Infrastructure / in-kind | Credits equal to $ value |
| Ecosystem / adjacent vendor | $500–$5,000/mo + affiliate |
| Founder / growth lead | Affiliate or fixed+affiliate hybrid |

---

## 8. Pricing checklist

- [ ] Pull your star tier from the grid (section 3) as a first-pass anchor.
- [ ] Re-derive from traffic + downloads + fit (section 2); use the higher of {grid low end, derivation} as your floor.
- [ ] Cite one comparable case study (section 4) when a sponsor asks for context.
- [ ] Quote monthly as the base; offer annual (~10–12×, −15–20%) and one-time (~8–10×, −15–20%) as options.
- [ ] For performance sponsors, lead with fixed+affiliate, not pure affiliate.
- [ ] Apply region multiplier (section 6) and pick a collection path the sponsor can actually use.
- [ ] Price at the low end until you have 3 closed deals, then raise 15–25%.
- [ ] Label every number "estimate / reference only" except cited disclosed figures.

See also: [sponsor-kit.md](sponsor-kit.md) (how to package these numbers for a sponsor), [readme-monetization.md](readme-monetization.md) (where each slot physically lives), [faq.md](faq.md).
