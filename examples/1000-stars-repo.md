# Worked example: a 1000-star repo (the sweet spot)

> **1000 stars is the sweet spot: real users, real downloads, real procurement conversations — but still close enough to the metal that you can sell it yourself.**
> This is where a deliberate sponsorship program starts to pay. The full strategy lives in [../docs/1000-stars-playbook.md](../docs/1000-stars-playbook.md); this file is a concrete, copy-pasteable worked example.

All prices below are **estimate / reference only** — not a quote. They are the 1000-star row of [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml). Real drivers are unique monthly visitors (GitHub Traffic) + package downloads (npm/PyPI/Docker) + audience-to-sponsor fit, not the star count itself.

---

## 1. Where you actually stand

A 1000-star repo typically has:

- **Real package downloads** — enough that a sponsor can imagine click-through.
- **A small but genuine audience** — a docs site, maybe a Discord, maybe a nascent newsletter.
- **No procurement leverage** — you are not "Vue." Companies sponsor out of goodwill + dev-marketing, not brand fear.

Set the ceiling expectation honestly: [Caleb Porzio hit ~$112,680/yr (~$9,390/mo) on GitHub Sponsors](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) — but that took years of active selling on a much larger footprint (Livewire/Phoenix). At 1000 stars, a realistic *first-year* target is a handful of sponsors totaling a few hundred to low-thousands per month. The [komorebi lesson](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) (~10k stars → only ~$155/mo with no sales) is your warning: stars do not sell themselves.

## 2. Filled `.github/FUNDING.yml`

Two cash rails (GitHub Sponsors for recurring, Buy Me a Coffee for one-off tips) + Open Collective for the public ledger + a custom link to your sponsor page. This is a realistic, fully-filled file for a fictional 1000-star repo `fastdb` (a database client library):

```yaml
# .github/FUNDING.yml for fastdb
# Docs: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/displaying-a-sponsor-button-in-your-repository

# GitHub Sponsors — single username OR array of up to 4.
github: your-username

# Open Collective (public ledger; free Discover plan).
open_collective: fastdb

# Buy Me a Coffee (one-off tips; 5% platform fee + Stripe processing).
buy_me_a_coffee: your-username

# Custom — up to 4 URLs. Any URL with a colon MUST be quoted.
custom: ["https://fastdb.example.com/sponsor", "https://fastdb.example.com/media-kit"]
```

Notes from [../data/platforms.yml](../data/platforms.yml):
- **GitHub Sponsors** personal account = 0% platform fee. 103 regions; **mainland China not supported** (HK/Macau SAR are). Tier price is immutable once published — to change a price you retire the tier and recreate it. Max 10 one-time + 10 monthly tiers, max $12,000/mo.
- **Buy Me a Coffee** = 5% platform fee + Stripe 2.9% + $0.30 + 0.5% payout + 1% international + 0.5% subscription. No PayPal. Good for one-off appreciation; pair with GitHub Sponsors for recurring.
- **Open Collective** Discover = $0/mo, free with optional Platform Tips (or a 5% Crowdfunding Fee in place of tips). Transparent public ledger — worth it at 1000 stars because companies like the auditability.
- Not supported as FUNDING.yml keys (do not list): `otechie`, `givebutter`, `lfx_crowdfunding`.

## 3. Mini rate card (USD + RMB)

All figures **estimate / reference only.** Low-end anchors for a first-year 1000-star repo. Raise after your first three closed deals.

| Slot | USD/mo (est., low end) | RMB/mo (est. face) | Notes |
|------|------------------------|--------------------|-------|
| README top banner | $400 | ~¥2,600 | Premium; 1–2 logos. Sell only if you have a top sponsor. |
| README bottom logo | $200 | ~¥1,300 | The dominant pattern (Vue/Vite/Astro). Dynamic SVG grid. |
| README bottom text | $100 | ~¥650 | Cheapest; individuals / small backers. |
| Docs site ad | $50 | ~¥325 | Traffic-driven; see [ad math](#6-optional-docs-site-ad). |
| Release note | $200 | ~¥1,300 | Per-release; version-aligned moment. |
| Newsletter per issue | $200 | ~¥1,300 | Only if you have a real list. |

**RMB note (from [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml) region multipliers):** multiply USD × ~6–7 for an RMB "face" number, **but** domestic China sponsors often pay in the **¥500–¥5,000/mo band** for 1000-star repos — i.e., a domestic backer may pay less than the USD×6.5 face value. Treat the RMB column as a ceiling anchor, and quote domestic prospects in the ¥500–¥5,000 band first.

### Deal-model modifiers (apply on top of the slot base)

| Deal model | Modifier (est.) |
|------------|------------------|
| One-time 12-month display | ~8–10× monthly, discounted 15–20% vs monthly |
| Annual paid yearly | ~10–12× monthly, discounted 15–20% |
| In-kind credits | Face-value of credits/services; log at fair-market |
| Affiliate (pure) | $0 fixed; 10–30% recurring or $5–$50 flat per converted user |

### The low-price-first-month test

Before you commit to a published rate, run this:

1. Pick your **3 most-likely prospects** (score them with [../tools/sponsor-fit-score.md](../tools/sponsor-fit-score.md)).
2. Pitch the **low end** of each slot, with **month one at 50% off** (or free) to remove risk.
3. Track outcome in [../tools/outreach-checklist.md](../tools/outreach-checklist.md).
4. After 3 closed deals, you have a market signal — raise to the mid of the range. If 0 of 3 close at the low end, your traffic/conversion story (not your price) is the problem; go fix that first.

> A rate card is a draft until three sponsors have paid something close to it. Until then it is an internal anchor, not a published price list. See [../templates/rate-card.md](../templates/rate-card.md) for the full template.

## 4. Sponsor-kit excerpt

The sponsor kit is the one-pager you attach to a DM. At 1000 stars keep it to one page. Fields in brackets are yours to fill.

```markdown
# [your-repo] — Sponsor Kit

## Audience (self-reported, 14-day rolling window)
- GitHub stars: ~[1,000]
- Package downloads: ~[XX,000]/mo ([npm/PyPI/Docker])
- GitHub Traffic unique visitors: ~[X,000]/mo (self-reported; maintainers-only API, 14-day window)
- Docs site pageviews: ~[XX,000]/mo (if measured)

> Traffic figures are self-reported and not independently verifiable by sponsors.
> Use them as a directional indicator, not an impression guarantee.

## What you get
| Tier | USD/mo (est.) | Inventory |
|------|---------------|-----------|
| Backer | $100 | README bottom text line |
| Supporter | $200 | README bottom logo + release note |
| Partner | $400 | README top banner + release note + docs ad |

## Sponsors (so far)
- [founding sponsor] — [tier] (or "Seeking founding sponsor" if none yet)

## Logistics
- Cash: GitHub Sponsors (0% fee, personal) — https://github.com/sponsors/[your-username]
- Ledger: Open Collective — https://opencollective.com/[your-collective]
- Fiscal host: [Open Source Collective (US 501(c)(6)) / regional host]
- .github/FUNDING.yml: configured
- Vetting: we do not accept [gambling/adult/etc.] sponsors.

## Contact
[email / Discord / GitHub Discussions] — [your-name]
```

Full media-kit template (TLDR-style): audience size, demographics, engagement, inventory, rate card, past sponsors, testimonials, case study, contact. See [../templates/media-kit.md](../templates/media-kit.md).

## 5. The first-50-DMs plan

You will not get sponsorships without outbound. Plan a **first 50** prospect batch.

### Build the list (target 50 prospects)

Source, in priority order (see sponsor kinds in [../data/sponsor-types.yml](../data/sponsor-types.yml)):

1. **Companies in your dependency tree** — who ships software that *uses* `fastdb`? Their DevRel/growth teams are your best fit (`devrel`, `ecosystem`).
2. **Adjacent vendors** — products that deploy *with* yours (hosting, ORM, observability) (`ecosystem`).
3. **Companies using your project in prod** — ask power-user issue reporters to intro their employer (`company_direct`).
4. **In-kind sponsors** — hosting/CI/secrets/monitoring vendors trading credits for a logo (`infrastructure`).
5. **Founders/growth leads** running performance campaigns (`founder_growth`) — offer a fixed+affiliate hybrid.

### Score and rank

Score all 50 with the [Sponsor Fit Score](../tools/sponsor-fit-score.md). Pursue score **61–100** (61–85 pursue, 86–100 priority); **0–30 skip**, **31–60 maybe**.

### Send in waves + 3-touch

- Send in **waves of ~10** so you can adapt the pitch after each wave.
- Cadence rule: **3 touches, then close.** Initial DM → follow-up #1 (day +4) → follow-up #2 (day +9). After three touches with no positive signal, mark `closed-lost` and move on. Do not burn reputation with a 4th touch.
- Track every prospect in the [outreach checklist](../tools/outreach-checklist.md) (markdown table + CSV variant provided there).

### What the first DM looks like

Lead with the audience overlap, not the star count. One concrete reason their users match yours. Low-end price. First-month discount. Same shape as the [100-star outreach DM](./100-stars-repo.md#4-sample-outreach-dm), but with real traffic/download numbers in the bracketed fields.

## 6. Optional: docs site ad

If your docs site sustains **~50,000+ monthly pageviews**, add [EthicalAds](https://www.ethicalads.io/publishers/calculator/) (the 50k floor is a hard gate; below it you won't be accepted). Revenue math (**estimate / reference only**):

```
monthly_revenue ≈ monthly_pageviews / 1000 × ~$2.50
```

- [EthicalAds publisher revshare = 70%, effective ~$2.25–$2.75 CPM (mid ~$2.50) for EU+NA traffic](https://www.ethicalads.io/publishers/calculator/). Min payout $50 (PayPal / OpenCollective / GitHub Sponsors / Stripe bank). One ad per page, above the fold, dev-only audience, no newsletter/README placement.
- Example: 60,000 docs pageviews/mo → ~60 × $2.50 = **~$150/mo (est.)**. Decouples revenue from star count — the most honest dollar at this tier because it's tied to actual traffic, not a popularity proxy.

Do **not** bother with [Carbon Ads](https://carbonads.net) at 1000 stars — its advertiser minimum is $5,000–$10,000/mo over 60–90 days, sales-assisted, and it curates 350+ hand-picked sites; you are not yet on that list.

## 7. Graduation criteria

Move to the [10000-star example](./10000-stars-repo.md) (tiered program, standalone sponsor page, ad-network at scale) when you have:

- [ ] 3+ paying sponsors and a published rate card validated by closed deals.
- [ ] Docs traffic sustaining ~50k+ pageviews/mo (EthicalAds live).
- [ ] A real newsletter list (if you want to sell the newsletter slot at the $200–500/issue band).
- [ ] Star count trending through ~5k+.

Until then, keep selling the [1000-star playbook](../docs/1000-stars-playbook.md) low-end slots, one founding sponsor at a time.
