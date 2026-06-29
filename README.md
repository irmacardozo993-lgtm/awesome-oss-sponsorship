<div align="center">

# awesome-oss-sponsorship

**A field guide to getting open-source projects paid — sponsors, ad networks, affiliate deals, and the outreach that actually closes.**

Curated platforms · verified pricing anchors · copy-paste templates · real case studies · a 7-day cold-start plan.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Made for maintainers](https://img.shields.io/badge/for-100%2B%20%E2%86%92%2010k%2B%20star%20repos-blueviolet)](#who-this-is-for)

</div>

🌐 **Languages:** [English](README.md) · [中文](README.zh-CN.md) · [Español](README.es.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

> **Sponsorship is a sales channel, not a star-count reward.** Stars are a popularity
> proxy — the real pricing drivers are **unique monthly visitors** (GitHub Traffic),
> **package downloads** (npm / PyPI / Docker Hub), and **audience-to-sponsor fit**. This
> repo is the playbook for running that sales channel professionally: which platforms,
> which slots, what price, who to message, and what to send.

Everything here is **copy-pasteable** and grounded in **verified public sources** (official
docs, OpenCollective pages, maintainer blogs, ad-network pricing pages). All prices are
**estimates / reference only** — never a quote, never a promise. See
[the disclaimer](#disclaimer).

---

## Table of contents

- [Who this is for](#who-this-is-for)
- [Quick start (5 minutes)](#quick-start-5-minutes)
- [If you only have 1,000 stars](#if-you-only-have-1000-stars)
- [Platform comparison](#platform-comparison)
- [Pricing reference (estimate)](#pricing-reference-estimate)
- [Affiliate programs that actually pay](#affiliate-programs-that-actually-pay)
- [How to find sponsors](#how-to-find-sponsors)
- [The 7-day cold-start plan](#the-7-day-cold-start-plan)
- [Templates & tools](#templates--tools)
- [Documentation](#documentation)
- [Real case-study anchors](#real-case-study-anchors)
- [Contributing](#contributing)
- [Star History](#star-history)
- [Disclaimer](#disclaimer)

---

## Who this is for

| You are | Start here |
|---------|-----------|
| **100-star maintainer** (early CLI/SDK) | GitHub Sponsors (0% fee) + `.github/FUNDING.yml`. Focus on momentum, not money. → [100-star example](examples/100-stars-repo.md) |
| **1,000-star maintainer** (the sweet spot) | GitHub Sponsors + Open Collective + a rate card. Run the first-50-DMs plan. → [1000-star playbook](docs/1000-stars-playbook.md) · [example](examples/1000-stars-repo.md) |
| **10,000-star maintainer** | Tiered program + standalone sponsor page + EthicalAds on docs. → [10000-star example](examples/10000-stars-repo.md) |
| **Indie / solo dev** | GitHub Sponsors (recurring) + Buy Me a Coffee (one-off tips). Skip the fiscal host. |
| **Devtool / CLI / SDK maintainer** | GitHub Sponsors + thanks.dev (dependency-tree inbound) + affiliate hybrid. |
| **Newsletter-running mainter** | GitHub Sponsors + Paved (newsletter ads — highest $/impression). |
| **Maintainer shipping a paid SaaS/AI product** | Polar (Merchant-of-Record) — **not** for sponsorship. |

---

## Quick start (5 minutes)

1. **Pick a platform.** Solo → [GitHub Sponsors](docs/github-sponsors.md) (0% personal fee). Multiple contributors/vendors → [Open Collective](docs/open-collective.md) (fiscal host + public ledger).
2. **Add `.github/FUNDING.yml`.** Wires the "Sponsor" button. Copy the [annotated template](templates/funding-yml-example.md) (12 current keys; `otechie`/`givebutter`/`lfx_crowdfunding` are **not** supported).
3. **Set tiers.** GitHub Sponsors: up to 10 one-time + 10 monthly, max $12,000/mo; **price is immutable once published** (retire + recreate to change). Anchor to real ladders — Vite `$5/$15/$50/$150/$500`, Astro `$10/$100/$200/$250/$1,000/$10,000` — but label yours **estimate / reference only**.
4. **List your inventory.** You sell *exposure*, not stars. Slot taxonomy in [`data/sponsor-types.yml`](data/sponsor-types.yml): README top banner, README bottom logo grid (the dominant pattern — dynamic SVG, never edit the README), docs-site ad, release-note, newsletter.
5. **Start outreach.** Build a one-page [rate card](templates/rate-card.md) anchored to **your** traffic, then send the [cold-email](templates/cold-email.md) template to companies in your dependency tree or your Popular Referrers. Price at the **low** end until you close 3 deals.

> The 5-minute path is detailed in [docs/getting-started.md](docs/getting-started.md).

---

## If you only have 1,000 stars

1,000 stars is the sweet spot: real users, real downloads, real procurement conversations — but still close enough to the metal that you can sell it yourself. The full strategy is the [1000-star playbook](docs/1000-stars-playbook.md); the essentials:

- **It is commercially valuable** — but only if you sell. [komorebi (~10k stars) made only ~$155/mo](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) with no sales; [Caleb Porzio hit ~$112,680/yr](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) by actively selling on a bigger footprint.
- **Price at the low end** of the [estimate grid](#pricing-reference-estimate); raise after 3 closed deals.
- **Run a 50-prospect pipeline**, scored with the [Sponsor Fit Score](tools/sponsor-fit-score.md), on a 3-touch-then-close cadence — see the [first-50-DMs plan](examples/1000-stars-repo.md#5-the-first-50-dms-plan).
- **Offer a first-month test** at 50% off (or free) to remove risk for a founding sponsor.
- **Don't hurt the repo.** A vetting policy + clean affiliate disclosure + no spam-blasting protects the reputation that makes the repo sponsorable in the first place.

---

## Platform comparison

Statuses verified 2026-06-29 against official sites. Fees are **reference only**.

| Platform | Type | Status | Fee (ref. only) | Best for |
|---|---|---|---|---|
| [GitHub Sponsors](docs/github-sponsors.md) | sponsorship | ✅ alive | 0% personal / ≤6% org | solo maintainers; native GitHub button. ⚠ mainland China **not** supported |
| [Open Collective](docs/open-collective.md) | fiscal host | ✅ alive | $0/$60/$320 plan; or 5% | public ledger; multiple contributors |
| Open Source Collective | fiscal host | ✅ alive | via OC | US 501(c)(6) umbrella, tax-deductible |
| [Polar](docs/polar.md) | billing MoR | 🔄 pivoted | 5%+50¢ → 3.40%+30¢ | paid SaaS/AI billing+tax. **Not sponsorship** |
| Buy Me a Coffee | donation | ✅ alive | 5% + Stripe processing | one-off tips |
| Ko-fi | donation | ⚠ unverified | 0% donations; Gold ~$12/mo (verify) | direct PayPal/Stripe tips |
| Patreon | subscription | ✅ alive | 10% | recurring memberships |
| thanks.dev | donation | ✅ alive | 5% | auto-fund your dependency tree |
| StackAid | donation | ✅ alive | subs from $15/mo | fund direct + transitive deps |
| Tidelift | subscription | ❌ acquired | — | historical; acquired by Sonar (Dec 2024) |
| IssueHunt | bounty | ⚠ stale | n/d | bounty-on-issue — use **oss.issuehunt.io**, verify liveness |
| Algora | recruiting | 🔄 pivoted | n/d | OSS hiring + bounty sidebar |
| [EthicalAds](docs/ad-networks.md) | ads (CPM) | ✅ alive | 70% revshare, ~$2.50 CPM | dev docs sites (50k+ pageviews) |
| Carbon Ads | ads (CPC) | ✅ alive | sales-assisted | curated dev sites ($5–10k adv. min) |
| BuySellAds | ads (multi) | ✅ alive | managed | email/native/sponsored/podcast |
| Passionfroot | ads/marketplace | 🔄 pivoted→Zest | 2% / 15% | newsletter brand deals |
| Paved | ads (newsletter) | ✅ alive | flat + PPC | newsletters (25k subs / 1M pv) |

Full structured DB: [`data/platforms.yml`](data/platforms.yml).

---

## Pricing reference (estimate)

> **Estimate / reference only.** There is **no** standardized public market tying $/month
> to star count. Star count is a popularity proxy, not a pricing metric. Re-derive from
> **your** traffic: docs ad ≈ `monthly_pageviews / 1000 × ~$2.50` (EthicalAds publisher
> CPM); newsletter ≈ `subs × open_rate × CTR × target_cpc`, anchored to [JavaScript
> Weekly's $3,590/issue at 180k subs](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf).
> Price at the **low** end without traffic/conversion data; raise after 3 closed deals.

Monthly USD by star tier × slot (estimate):

| Stars | README top banner | README bottom logo | README bottom text | Docs-site ad | Release note | Newsletter / issue |
|------:|---:|---:|---:|---:|---:|---:|
| 100 | $100–300 | $50–150 | $20–75 | $10–40 | $50–150 | $30–100 |
| 500 | $200–500 | $100–300 | $50–150 | $25–80 | $100–300 | $100–250 |
| 1,000 | $400–1,000 | $200–600 | $100–300 | $50–200 | $200–600 | $200–500 |
| 5,000 | $1,000–3,000 | $500–1,500 | $250–750 | $150–600 | $500–1,500 | $500–1,500 |
| 10,000 | $2,000–6,000 | $1,000–3,000 | $500–1,500 | $300–1,500 | $1,000–3,000 | $1,000–2,500 |
| 50,000 | $5,000–15,000 | $3,000–10,000 | $1,500–5,000 | $1,000–5,000 | $2,500–8,000 | $2,500–7,000 |

Deal-model modifiers (est.): one-time 12-month display ≈ 8–10× monthly (15–20% off); annual ≈ 10–12× monthly (15–20% off); pure affiliate = $0 fixed + 10–30% recurring; **fixed + affiliate hybrid** = lower retainer + commission (the best model). Full grid + RMB domestic band in [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml); copy-paste rate card in [`templates/rate-card.md`](templates/rate-card.md).

---

## Affiliate programs that actually pay

Most devtool companies have **no** public affiliate program (OpenAI, Anthropic, GitHub,
Supabase, Cloudflare, AWS — all confirmed absent). The ones that do, verified 2026-06-29:

| Program | Commission (ref.) | Cookie | Payout | Fit |
|---|---|---|---|---|
| [Railway](https://railway.com/affiliate-program) | 15% recurring, 12 mo | n/d | GitHub Sponsors / BMC | ★★★ cash via Sponsors |
| [Neon](https://neon.com/programs/open-source) | $20 cash / referral | n/d | GitHub Sponsors | ★★★ OSS-program |
| [ElevenLabs](https://elevenlabs.io/affiliates) | 22% recurring, 12 mo | n/d | PartnerStack, $5 | ★★★ AI voice |
| [Apify](https://apify.com/partners/affiliate) | 20%→30%, cap $2,500/customer | 45 d | PayPal/bank, $100 | ★★★ scraping |
| [Bright Data](https://brightdata.com/affiliate) | 50% up to $2,500 + 15% 2nd-tier | 90 d | PartnerStack | ★★★ proxies |
| [ScrapingBee](https://www.scrapingbee.com/affiliates/) | 25% recurring lifetime | n/d | PayPal, $50 | ★★★ scraping |
| [Browserless](https://www.browserless.io/affiliate) | 20–30% tiered, 12 mo | 90 d | PayPal/bank, $50 | ★★★ headless browser |
| [n8n](https://n8n.io/affiliates/) | 30% recurring, 12 mo (Cloud) | n/d | PayPal, €100 | ★★★ automation |
| [Make](https://www.make.com/en/affiliate) | 35% recurring, 12 mo | 30 d | Wise, $100 | ★★ automation |
| [Raycast](https://www.raycast.com/blog/affiliate-program) | 30% recurring (Pro) | n/d | Wise, £50 | ★★ macOS |
| [Pluralsight](https://www.pluralsight.com/affiliate) | $1/trial + 30%/10%/5% one-time | 7 d | CJ | ★★ dev learning |
| [DigitalOcean](https://www.digitalocean.com/affiliates) | 10% recurring, 12 mo | n/d | Awin/CJ | ★★ hosting |
| [Netlify](https://www.netlify.com/partners/) | 20% recurring, 12–24 mo | n/d | PartnerStack | ★★ Jamstack |
| [Vercel / v0](https://partners.dub.co/v0) | 30% recurring, 6 mo + $5/lead | n/d | Dub | ★★ frontend |

Closed/dead: Hetzner (sunset 2026-06-15), Notion (closed to new), ShareASale (defunct→Awin), Heroku (dead).
Networks to join as a publisher: **PartnerStack** (best devtool density, $5 min) and **Impact** (broad, $10 min). Full DB + the "no program found" de-bunk list in [`data/affiliate-programs.yml`](data/affiliate-programs.yml) and [docs/affiliate-programs.md](docs/affiliate-programs.md).

---

## How to find sponsors

Don't spray-and-pray. Build a scored 50-prospect list. Priority sources (full method in [docs/outreach.md](docs/outreach.md)):

1. **Companies in your dependency tree** — who ships software that *uses* your project? Their DevRel/growth teams are the best fit.
2. **Stargazers/forkers that are companies** — GitHub orgs starring/forking you; find the DevRel/founder/growth contact via LinkedIn/X.
3. **Adjacent vendors** — products that deploy *with* yours (hosting, ORM, observability, CI).
4. **In-kind sponsors** — hosting/CI/secrets/monitoring vendors trading credits for a logo (Homebrew pattern: MacStadium, 1Password).
5. **Power-user issue reporters** — ask them to intro their employer.

Score every prospect with the [Sponsor Fit Score](tools/sponsor-fit-score.md) (0–100). Pursue **61–100**; skip **0–30**. Send the [cold-email](templates/cold-email.md) / [DM](templates/dm-template.md) templates on a 3-touch-then-close cadence. Track everything in the [outreach checklist](tools/outreach-checklist.md).

---

## The 7-day cold-start plan

A week to go from "no sponsor program" to "first pitches out + repo launched." Each day is a checklist in [docs/launch-plan.md](docs/launch-plan.md) and [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md).

| Day | Do this | Output |
|---|---|---|
| **1** | Pick platform; add `.github/FUNDING.yml`; set 3–5 tiers (low end) | Live Sponsor button + tier ladder |
| **2** | List inventory slots; build a one-page [rate card](templates/rate-card.md) | Rate card (internal anchor) |
| **3** | Pull GitHub Traffic + npm/PyPI/Docker downloads; build a one-page [sponsor kit](templates/sponsor-kit.md) | Kit with self-reported-traffic caveat |
| **4** | Build a 50-prospect list (dep tree, stargazer-orgs, adjacent vendors); score with [Sponsor Fit Score](tools/sponsor-fit-score.md) | Scored prospect list |
| **5** | Send wave 1 (10 prospects) via [cold-email](templates/cold-email.md) / [DM](templates/dm-template.md) | 10 outbound, tracked |
| **6** | Send wave 2 (10); draft launch posts (HN / Reddit / V2EX / X) | Launch assets ready |
| **7** | Launch + publish a standalone sponsor page; log all in [outreach checklist](tools/outreach-checklist.md) | Repo live, pipeline running |

After day 7: keep the rolling 50-prospect pipeline, run 3-touch cadences, and sustain updates for organic star growth (see [docs/launch-plan.md](docs/launch-plan.md) §12).

---

## Templates & tools

Copy-paste, fill in the `[brackets]`, ship.

| File | What it is |
|---|---|
| [templates/funding-yml-example.md](templates/funding-yml-example.md) | Annotated `.github/FUNDING.yml` — all 12 keys, 3 full examples |
| [templates/rate-card.md](templates/rate-card.md) | One-page rate card (USD + RMB, star-tier × slot grid) |
| [templates/cold-email.md](templates/cold-email.md) | Cold email + follow-ups + yes/no replies (EN + 中文) |
| [templates/dm-template.md](templates/dm-template.md) | LinkedIn / X / Discord / 微信 / V2EX-掘金 DMs |
| [templates/sponsor-kit.md](templates/sponsor-kit.md) | Full sponsor kit (fill-in + worked example) |
| [templates/media-kit.md](templates/media-kit.md) | TLDR-style media kit (all components + example) |
| [templates/readme-sponsor-block.md](templates/readme-sponsor-block.md) | README top/bottom/logo/text/affiliate snippets |
| [templates/affiliate-tracker.csv](templates/affiliate-tracker.csv) | CSV to track affiliate deals |
| [tools/sponsor-fit-score.md](tools/sponsor-fit-score.md) | 0–100 prospect scoring model + worked example |
| [tools/outreach-checklist.md](tools/outreach-checklist.md) | 50-prospect pipeline tracker (markdown + CSV) |

---

## Documentation

| Doc | Covers |
|---|---|
| [docs/getting-started.md](docs/getting-started.md) | Orientation + the 5-minute path + link map |
| [docs/github-sponsors.md](docs/github-sponsors.md) | Eligibility, regions (China caveat), setup, tiers, fees, README display |
| [docs/open-collective.md](docs/open-collective.md) | Fiscal hosts, OSC 501(c)(6), public ledger, plans/fees |
| [docs/polar.md](docs/polar.md) | The pivot to AI billing / MoR — when it fits vs not |
| [docs/ad-networks.md](docs/ad-networks.md) | EthicalAds, Carbon, BuySellAds, Passionfroot, Paved |
| [docs/affiliate-programs.md](docs/affiliate-programs.md) | Verified affiliate programs + the de-bunk list + networks |
| [docs/pricing.md](docs/pricing.md) | How to price (traffic, not stars) + estimate grid |
| [docs/sponsor-kit.md](docs/sponsor-kit.md) | Building a sponsor kit (guide) + GitHub Traffic facts |
| [docs/readme-monetization.md](docs/readme-monetization.md) | README + surface monetization (every slot) |
| [docs/outreach.md](docs/outreach.md) | Finding sponsors proactively |
| [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md) | The 10-section 1k-star playbook |
| [docs/launch-plan.md](docs/launch-plan.md) | Cold-start distribution (HN/Reddit/PH/V2EX/掘金/X) |
| [docs/case-studies.md](docs/case-studies.md) | Verified disclosed numbers (Astro/Vue/Vite/Tailwind/Sentry/…) |
| [docs/faq.md](docs/faq.md) | 15+ Q&A |

Data (source of truth): [`data/platforms.yml`](data/platforms.yml) · [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml) · [`data/sponsor-types.yml`](data/sponsor-types.yml) · [`data/affiliate-programs.yml`](data/affiliate-programs.yml).

🌐 **Languages:** [English](README.md) · [中文](README.zh-CN.md) · [Español](README.es.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

---

## Real case-study anchors

Publicly disclosed numbers (cited in [docs/case-studies.md](docs/case-studies.md)). Estimates marked.

| Project | What's disclosed (source) | Takeaway |
|---|---|---|
| [Astro](https://opencollective.com/astrodotbuild) | $836k all-time on OC; tiers up to $10,000/mo | Clean ladder + sponsor page + fiscal host = the ceiling |
| [Vue.js](https://opencollective.com/vuejs) | $852k all-time on OC | Self-hosted sponsor page + BACKERS.md works |
| [Vite](https://opencollective.com/vite) | $162k all-time on OC; Bronze $50 → Gold $500 | A simpler ladder also works |
| [Homebrew](https://opencollective.com/homebrew) | $486k all-time on OC | In-kind (MacStadium/1Password) + cash mix |
| [Tailwind CSS](https://tailwindcss.com/sponsor) | Partner $5,000/mo (est. ~$200k/mo from ~70 cos) | Sponsorship tiers work at flagship scale; commercial ≠ sponsorship |
| [Sentry](https://blog.sentry.io) | $155k→$750k/yr OSS outflow; $2,000/engineer/yr pledge | What a *sponsor* budgets |
| [Caleb Porzio](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) | $112,680/yr on GitHub Sponsors | Active selling on a real footprint |
| [komorebi (~10k★)](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) | $1,861/yr (~$155/mo) | **10k stars ≠ sponsorship without sales** |

---

## Contributing

Corrections and new platforms/programs are welcome — **with a cited official source**. See [CONTRIBUTING.md](CONTRIBUTING.md). The one rule: **do not publish unverified facts**; mark anything uncertain `unverified` rather than guessing.

---

## Star History

<a href="https://star-history.com/#irmacardozo993-lgtm/awesome-oss-sponsorship&Date">
  <img src="https://api.star-history.com/svg?repos=irmacardozo993-lgtm/awesome-oss-sponsorship&type=Date" alt="Star History">
</a>

---

## Acknowledgments

- **[Linux.do](https://linux.do)** — Chinese-language developer & tech community (Discourse) whose members and feedback shaped the China-distribution guidance in this guide.
- **[Telegram OpenClaw 中文社区](https://t.me/OpenClaw_Group)** — the Chinese-language OpenClaw community on Telegram, for support and discussion.

---

## Disclaimer

All pricing, fees, commission rates, and revenue figures in this repository are
**estimates / reference only**. They are not quotes, not guarantees, and not financial,
legal, or tax advice. Real prices depend on vertical, traffic, user quality, conversion
rate, audience geography, and sponsor budget. **Verify current terms with each platform
before relying on them.** Platform statuses were checked 2026-06-29 and change
frequently. This project does not promise any earnings and is not a "get rich" scheme —
it is a field guide for maintainers who want to run sponsorship professionally.

License: [CC-BY-4.0](LICENSE) for content; MIT for embedded code snippets. See [LICENSE](LICENSE).
