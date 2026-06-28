# Rate Card Template — OSS Sponsorship Slots

A rate card you hand a sponsor (or embed in a [media kit](media-kit.md)) to set
a starting anchor for slot pricing. Use it as an **internal reference and a
conversation opener**, never as a published price list or a quote.

> **ALL FIGURES ARE ESTIMATES / REFERENCE ONLY.** There is no standardized
> public market tying $/month to star count. Real prices depend on vertical,
> traffic, user quality, conversion rate, audience geography, and sponsor
> budget. Star count is a popularity **proxy**, not a pricing metric — the real
> drivers are unique monthly visitors (GitHub Traffic) + package downloads
> (npm/PyPI/Docker) + audience-to-sponsor fit.

Numbers below are consistent with
[../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml). Slot
taxonomy from [../data/sponsor-types.yml](../data/sponsor-types.yml). Platform
fees (GitHub Sponsors 0%/6%, Open Collective, etc.) in
[../data/platforms.yml](../data/platforms.yml).

---

## (a) USD monthly estimate grid — star tier × slot type

All cells: **estimate / reference only**, monthly USD.

| Stars | README top banner | README bottom logo | README bottom text | Docs site ad | Release note | Newsletter / issue |
|------:|------------------:|-------------------:|-------------------:|-------------:|-------------:|-------------------:|
| 100 | $100–300 | $50–150 | $20–75 | $10–40 | $50–150 | $30–100 |
| 500 | $200–500 | $100–300 | $50–150 | $25–80 | $100–300 | $100–250 |
| 1,000 | $400–1,000 | $200–600 | $100–300 | $50–200 | $200–600 | $200–500 |
| 5,000 | $1,000–3,000 | $500–1,500 | $250–750 | $150–600 | $500–1,500 | $500–1,500 |
| 10,000 | $2,000–6,000 | $1,000–3,000 | $500–1,500 | $300–1,500 | $1,000–3,000 | $1,000–2,500 |
| 50,000 | $5,000–15,000 | $3,000–10,000 | $1,500–5,000 | $1,000–5,000 | $2,500–8,000 | $2,500–7,000 |

> Outliers (e.g. Tailwind CSS, ~$200,000/mo from ~70 companies — third-party
> derived, not official; source: tailwindcss.com/sponsor) sit **far above the
> 50,000★ row**. The grid is a floor anchor, not a ceiling. Verified disclosed
> case studies (Astro, Vue, Vite, Homebrew, Sentry, Caleb Porzio, komorebi)
> live in [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml)
> `anchors:` — cite those URLs rather than re-stating them as your own.

---

## (b) RMB domestic version — 人民币国内参考价

Conversion rule (estimate): **RMB ≈ USD × 6–7** (low end ×6, high end ×7).
Domestic sponsors, however, often land in a tighter real band than the raw
multiplier suggests — see the note under the table.

All cells: **估算 / 仅供参考（estimate / reference only）**，月度人民币。

| Stars | README 顶部横幅 | README 底部 Logo | README 底部文字 | 文档站广告 | Release Note | Newsletter / 期 |
|------:|---------------:|-----------------:|----------------:|-----------:|-------------:|----------------:|
| 100 | ¥600–2,100 | ¥300–1,050 | ¥120–525 | ¥60–280 | ¥300–1,050 | ¥180–700 |
| 500 | ¥1,200–3,500 | ¥600–2,100 | ¥300–1,050 | ¥150–560 | ¥600–2,100 | ¥600–1,750 |
| 1,000 | ¥2,400–7,000 | ¥1,200–4,200 | ¥600–2,100 | ¥300–1,400 | ¥1,200–4,200 | ¥1,200–3,500 |
| 5,000 | ¥6,000–21,000 | ¥3,000–10,500 | ¥1,500–5,250 | ¥900–4,200 | ¥3,000–10,500 | ¥3,000–10,500 |
| 10,000 | ¥12,000–42,000 | ¥6,000–21,000 | ¥3,000–10,500 | ¥1,800–10,500 | ¥6,000–21,000 | ¥6,000–17,500 |
| 50,000 | ¥30,000–105,000 | ¥18,000–70,000 | ¥9,000–35,000 | ¥6,000–35,000 | ¥15,000–56,000 | ¥15,000–49,000 |

> **国内实际成交带（estimate / reference only）：** 国内 1,000★ 量级仓库的
> 常见月度成交区间约 **¥500–¥5,000**，集中在底部文字、底部 Logo、文档站广告、
> Release Note 等中低位档；顶部横幅与 Newsletter 在国内同样量级成交较少，多走
> 打包或年付折扣。实际取决于流量与受众契合度，star 数只是参考，不要直接按
> 表格高线报价。国内收款常走对公转账或个人收款码；GitHub Sponsors 不支持
> 中国大陆（香港/澳门特区可），见 [../data/platforms.yml](../data/platforms.yml)。

---

## (c) Per-slot one-line descriptions

| Slot | One-line description |
|------|----------------------|
| README top banner | Top of README, above the fold. Highest-visibility real estate. One or two logos max. Premium price. |
| README bottom logo | Bottom Sponsors section, logo grid. Dominant pattern (Vue/Vite/Astro). Dynamic SVG grid — README never needs editing. Tiered (Gold/Silver/Bronze). |
| README bottom text | Bottom Sponsors section, text list. Cheapest slot. Name + link. Good for individuals/small backers (BACKERS.md style). |
| Docs site ad | Sidebar/banner on docs site. Traffic-driven (EthicalAds ~$2.50 CPM). Decouples revenue from star count. Best for high-traffic docs. |
| Release note | GitHub Release / CHANGELOG entry. Per-release. Sponsors like version-aligned moments (launches, blog posts). |
| Newsletter / issue | Dedicated email / classified / primary spot. Highest $ per impression if you have a list. Anchored to JS Weekly $3,590/issue (180k subs, estimate / reference only). |

Full taxonomy (value/intrusiveness notes, plus demo-site / community-channel /
issue-template / CLI-startup / sponsor-page slots not priced in this grid):
[../data/sponsor-types.yml](../data/sponsor-types.yml).

---

## (d) Deal models — pick the structure, then price the slot

| Model | Structure | When it fits |
|-------|-----------|--------------|
| One-time | Single payment, defined period (1 release / 1 month) | Test slot, launch tie-in, low commitment |
| Monthly recurring | Predictable MRR | Default for GitHub Sponsors / Open Collective tiers |
| Annual (paid yearly) | ~10–12× monthly, discounted 15–20% | Sponsors who budget annually; improves retention |
| One-time 12-month display | ~8–10× monthly, discounted 15–20% vs paying monthly | Logo placement locked for a year; see (e) below |
| Affiliate (pure) | $0 fixed; 10–30% recurring or $5–$50 flat per converted user (volume-dependent) | Performance-only; founder/growth leads who pay for conversions |
| **Fixed + affiliate (hybrid)** | Lower fixed retainer (50–70% of slot base) + commission on conversions | Best balance of predictability + upside — see below |
| In-kind / barter | Face-value of credits/services (CI, hosting, DNS, secrets) | Infrastructure sponsors (e.g. MacStadium, 1Password for Homebrew) |
| Bounty | Funder pays fixed bounty for a specific issue/PR | IssueHunt (oss.issuehunt.io, stale), Algora (now recruiting-first) |

### Fixed + affiliate hybrid — explained

The hybrid exists because pure-affiliate deals put **all the risk on you** (you
might earn $0 if the audience doesn't convert), while pure-fixed deals put all
the risk on the **sponsor** (they pay full price before seeing any conversion).

**How it works (estimate / reference only):**
- Take the slot's monthly base from the USD grid above.
- Set the **fixed retainer at 50–70% of that base** — this is your floor and
  covers the placement cost regardless of conversion.
- Add a **commission on conversions** attributable to the placement:
  - 10–30% **recurring** on subscription revenue from attributed signups, OR
  - $5–$50 **flat** per converted user (volume-dependent — higher volume →
    lower per-unit, lower volume → higher per-unit).
- Cap the commission or define an attribution window up front (e.g. 30-day
  click-attribution via a dedicated landing URL) so both sides know when the
  deal stops paying out.

**Example (5,000★ repo, docs sidebar slot, estimate only):**
- Slot base: $150–600/mo → fixed retainer at 60% = ~$90–360/mo.
- Plus 15% recurring on attributed signups, 30-day attribution window.
- Floor: ~$90–360/mo guaranteed; upside uncapped if the audience converts.

> Match the model to the sponsor kind: **company_direct / devrel** → fixed or
> annual; **founder_growth** → fixed+affiliate or pure affiliate; **infrastructure**
> → in-kind. Sponsor-kind taxonomy: [../data/sponsor-types.yml](../data/sponsor-types.yml).

---

## (e) One-time 12-month display — the annual logo deal

For a sponsor who wants a **logo locked in place for a year** without monthly
invoicing, offer a single upfront payment for 12 months of display.

- **Multiplier:** ~**8–10× the monthly rate** for that slot/star tier.
- **Discount:** 15–20% off vs paying the monthly rate 12 times (the
  undiscounted 12× monthly comes down into the ~8–10× band once the discount
  is applied; sponsors typically negotiate toward the lower end).
- **When to use it:** top-banner / bottom-logo placements where the creative
  doesn't change monthly; pairs well with a release-note mention on a major
  version drop.
- **Annual paid-yearly (vs 12-month display):** a related but distinct model —
  ~10–12× monthly, discounted 15–20%. Use paid-yearly for recurring-tier
  sponsors (GitHub Sponsors / Open Collective); use 12-month display for a
  one-off contracted placement with an invoice.

**Example (5,000★ repo, top banner, estimate only):**
- Monthly base: $1,000–3,000.
- 12-month display: ~8–10× → ~$8,000–30,000, with the 15–20% discount already
  baked in. Quote a single number in that band, e.g. ~$12,000 for the year
  (estimate / reference only — confirm against your traffic before sending).

---

## How to re-derive your own number (always more credible than the star-tier table)

The grid is a starting anchor. A number you derive from your own traffic and
conversion data is far more defensible to a sponsor. Use the method that
matches the slot:

| Slot type | Derivation (estimate) |
|-----------|------------------------|
| Docs site ad | `monthly_pageviews / 1000 × ~$2.50` (EthicalAds publisher CPM, 70% revshare; source: ethicalads.io). E.g. 80k pageviews → ~$200/mo. |
| Newsletter | `subs × open_rate × CTR × target_CPC`; or anchor to JS Weekly: $3,590/issue at 180k subs / 41% open (source: cooperpress media kit, estimate / reference only). Scale to your list. |
| README slot | Star count is a **proxy only**. Real drivers = unique monthly visitors (GitHub Traffic, admin-only, 14-day, self-reported) + npm/PyPI/Docker pulls + audience-to-sponsor fit. |
| Release note | Anchor to the README slot for the same tier, then discount ~30–50% (per-release, not persistent). |
| Affiliate slots | $0 fixed; set commission at 10–30% recurring or $5–$50 flat per converted user, tuned to your conversion rate and volume. |

**Rule of thumb:** If you can't show traffic or conversion data, price at the
**LOW end** of the range and raise after the first 3 closed deals. Conversely,
if you have a verifiable high-traffic docs site or a large engaged newsletter,
price toward the **HIGH end** and lead the pitch with those metrics (see
[media-kit.md](media-kit.md)).

**Region:** USD figures are the global default (multiplier 1.0). For RMB
domestic, multiply USD × 6–7, but expect domestic 1k-star repos to land in the
¥500–¥5,000/mo band — see the RMB table note above. Full derivation method and
region multipliers: [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml)
(`derivation_method:` and `region_multipliers:`).

---

## Checklist before you send this to a sponsor

- [ ] Every figure carries "estimate / reference only" (or a cited public URL for disclosed anchors).
- [ ] You picked the star-tier row matching your actual star count, then adjusted toward the low or high end per your traffic data.
- [ ] You stated the deal model (one-time / monthly / annual / 12-month display / fixed+affiliate / in-kind) — not just a number.
- [ ] Affiliate numbers include an attribution window and a per-unit or % structure.
- [ ] 12-month display quote is in the 8–10× band with the 15–20% discount noted.
- [ ] For RMB quotes, the ¥500–¥5,000 domestic band caveat is present for 1k-star repos.
- [ ] You did **not** present an estimate as a firm quote — the sponsor kit/rate card is an opener for negotiation.
