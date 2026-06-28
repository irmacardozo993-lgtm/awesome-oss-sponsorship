# Worked example: a 10000-star repo

> **At 10k stars you finally have a real audience — and a real obligation to run sponsorship like a small business.**
> Two anchors hold the tension: [Astro raised $836k all-time on Open Collective](https://opencollective.com/astrodotbuild) and [Vite raised $162k](https://opencollective.com/vite) — both with clean tier ladders and standalone sponsor pages. But [komorebi (~10k stars) made only ~$155/mo in 2024](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) because it did no active sales. **10k stars still requires active sales.** Stars are an audience proxy, not a vending machine.

All prices below are **estimate / reference only** — the 10000-star row of [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml). Real drivers are unique monthly visitors (GitHub Traffic) + package downloads + audience-to-sponsor fit.

---

## 1. The tiered sponsorship program

Anchor your ladder to the two cleanest public structures: [Vite (Bronze $50 / Silver $150 / Gold $500)](https://opencollective.com/vite) and [Astro (Gold $250 / Platinum $1,000 / Exclusive $10,000)](https://opencollective.com/astrodotbuild). A realistic 10k-star program (slots from [../data/sponsor-types.yml](../data/sponsor-types.yml); prices **estimate / reference only**):

| Tier | USD/mo (est.) | Inventory included | Mirrors |
|------|---------------|--------------------|---------|
| **Bronze** | $50 | README bottom text line | [Vite Bronze $50](https://opencollective.com/vite) |
| **Silver** | $150 | README bottom logo (grid) | [Vite Silver $150](https://opencollective.com/vite) |
| **Gold** | $500 | README top banner + release note | [Vite Gold $500](https://opencollective.com/vite) |
| **Platinum** | $1,000 | Gold + docs site ad + featured on sponsor page | [Astro Platinum $1,000](https://opencollective.com/astrodotbuild) |

> [Astro's $10,000/mo "Exclusive" tier](https://opencollective.com/astrodotbuild) and [Tailwind's $5,000/mo Partner tier](https://tailwindcss.com/sponsor) are out of reach for most 10k-star repos — they require a flagship-brand pull most projects never get. Don't publish an Exclusive tier you can't fill; an empty top tier makes the ladder look broken.

Annual modifier (est.): annual paid yearly = ~10–12× monthly, discounted 15–20%. Sponsors prefer annual for budgeting; offer it from day one. See [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml) `deal_model_modifiers`.

### Why tiers (and where they live)

Tier labels (Bronze/Silver/Gold/Platinum) **do not belong inside the README.** That is the dominant convention: [Vue, Vite, Astro, and Homebrew](https://opencollective.com) all render a remotely-hosted dynamic logo grid in the README and keep the actual tier ladder on an external sponsor page. The README never needs editing — logos flow in from a sponsors endpoint/JSON. See [../data/sponsor-types.yml](../data/sponsor-types.yml) `sponsor_page` and `readme_bottom_logo`.

## 2. The standalone sponsor page (Vue / Astro pattern)

Build `your-repo.tld/sponsors` as the single source of truth. README links to it; the page renders tiers, goals, the public budget ledger, and the dynamic logo grid.

```markdown
# Sponsors

Thank you to the companies and individuals keeping [your-repo] sustainable.

## Goals (this quarter)
- [ ] Fund [N] days/month of maintenance ($[X])
- [ ] Sponsor [contributor name]'s work on [area]
- [ ] Cover infra: CI runners, docs hosting (~$[X]/mo)

## Tiers
| Tier | USD/mo | Inventory |
|------|--------|-----------|
| Bronze | $50 | README text line |
| Silver | $150 | README logo grid |
| Gold | $500 | Top banner + release note |
| Platinum | $1,000 | Gold + docs ad + featured here |

## Public budget
Hosted on Open Collective (transparent ledger):
https://opencollective.com/[your-collective]

## Logo grid
<!-- Logos render dynamically from /api/sponsors.json — never edit this by hand. -->
<img src="/api/sponsors.svg" alt="Sponsors" />
```

- **Public ledger:** use [Open Collective](https://opencollective.com) (free Discover plan, transparent income+expenses) or [Open Source Collective](https://www.oscollective.org) (US 501(c)(6), tax-deductible for US sponsors in many cases, automated 990s). 10k+ stars is exactly where a fiscal host pays for itself.
- **Dynamic SVG grid:** generate from a sponsors JSON endpoint so the README/page updates without commits. This is the Vue/Astro/Homebrew norm; a static grid you hand-edit rots.

### README snippet (just links out)

```markdown
## Sponsors

[your-repo] is sustained by our sponsors. 💛

[![Sponsors](https://your-repo.tld/api/sponsors.svg)](https://your-repo.tld/sponsors)

[Become a sponsor](https://your-repo.tld/sponsor) · [Public budget](https://opencollective.com/your-collective)
```

Two of six sampled repos (Tailwind, esbuild) keep the README minimal and route sponsorship entirely externally — also a legitimate "no-README-sponsor-block" pattern. Either works; pick one and be consistent.

## 3. Ad-network integration (EthicalAds on the docs site)

At 10k stars your docs site likely clears the [~50,000 monthly pageview floor](https://www.ethicalads.io/publishers/calculator/). Add [EthicalAds](https://www.ethicalads.io/publishers/calculator/) — it is the privacy-first, dev-only default (cookie-free, one ad per page, above the fold, no newsletter/README/podcast placement).

**Revenue math (estimate / reference only):**

```
monthly_revenue ≈ monthly_pageviews / 1000 × ~$2.50
```

- [EthicalAds publisher revshare = 70%, effective ~$2.25–$2.75 CPM (mid ~$2.50) for EU+NA traffic](https://www.ethicalads.io/publishers/calculator/). Min payout $50 (PayPal / OpenCollective / GitHub Sponsors / Stripe bank).
- Worked numbers:

| Docs pageviews/mo | Est. revenue/mo (~$2.50 CPM) |
|-------------------|------------------------------|
| 100,000 | ~$250 |
| 200,000 | ~$500 |
| 500,000 | ~$1,250 |

> The docs-site-ad estimate grid for 10k stars is $300–1,500/mo — consistent with the CPM math at 120k–600k pageviews. **This is the most honest dollar at any tier**: it's tied to actual traffic, not a star proxy. See `docs_site_ad` in [../data/sponsor-types.yml](../data/sponsor-types.yml).

**Carbon Ads** ([carbonads.NET](https://carbonads.net)) is the curated, sales-assisted alternative — advertiser entry $5,000–$10,000/mo over 60–90 days, 350+ hand-picked dev sites, $120M+ paid to publishers cumulatively. Realistically you graduate *to* Carbon (it approaches you / you apply and are vetted) once your docs traffic is substantial; you do not self-serve onto it. Publisher payout terms are not public.

**BuySellAds** ([buysellads.com](https://buysellads.com)) is the parent umbrella (Carbon + Coin.Network are sub-networks) for multi-format deals (email/native/sponsored/display/podcast/custom) — relevant only if you also run a newsletter or podcast; no pricing transparency, contact required.

## 4. Anchor cases (read these before you set expectations)

| Project | Stars (approx) | Sponsorship outcome | Lesson |
|---------|----------------|---------------------|--------|
| [komorebi](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) | ~10k | $1,861.88/yr (~$155/mo; range $92→$229) | **10k stars ≈ $155/mo with no active sales.** The single most important anchor in this file. |
| [Astro](https://opencollective.com/astrodotbuild) | 10k+ | $836,294.61 all-time; ~$438k/yr est.; tiers up to $10,000/mo | Clean tier ladder + standalone page + fiscal host = the ceiling for a well-run program. |
| [Vite](https://opencollective.com/vite) | 10k+ | $162,400.34 all-time; ~$102k/yr est.; Bronze $50 → Gold $500 | A simpler ladder also works; you don't need an Exclusive tier. |
| [Sentry](https://blog.sentry.io) | n/a (giver) | $155k→$750k/yr OSS outflow; $2,000/engineer/yr via [Open Source Pledge](https://opensourcepledge.com) | What a *sponsor* budgets — useful when you pitch enterprise prospects. |
| [PostHog](https://posthog.com/handbook/marketing/open-source-sponsorship) | n/a (giver) | ~$6,609/mo across tailwindcss/Django/rrweb/Tiptap | Real enterprise per-project spend sits in the $500–$2,500/mo band — i.e., your Gold/Platinum tiers. |

Takeaway: the *same* 10k-star footprint can yield ~$155/mo or ~$10,000/mo depending entirely on whether you run active outbound. Build the program, then sell it.

## 5. Platform setup at this scale

- **GitHub Sponsors** (org account): up to 6% = 3% card + 3% service; the 3% card fee is removed with **invoiced billing** — push org sponsors to invoiced billing to drop to 3%. Max 10 one-time + 10 monthly tiers, max $12,000/mo, prices immutable after publish (retire + recreate to change). Mainland China not supported (HK/Macau SAR are). See [../data/platforms.yml](../data/platforms.yml).
- **Open Collective / Open Source Collective:** the public ledger + 501(c)(6) fiscal host. At 10k stars this is table stakes for enterprise credibility. Multi-country/currency payouts, automated 990s.
- **EthicalAds** on the docs site (above).
- **.github/FUNDING.yml:** `github` (single or array up to 4) + `open_collective` + `custom` (array up to 4, quoted if it contains a colon) pointing to `/sponsor` and `/media-kit`. See the project's [.github/FUNDING.yml](../.github/FUNDING.yml).
- **thanks.dev / StackAid:** inbound channels for sponsors who want to fund your whole dependency tree automatically. [thanks.dev takes 5% commission](https://thanks.dev); [StackAid subscriptions from $15/mo, self-cap 7.5%](https://www.stackaid.us). Real corporate adoption: [Canonical committed $120k/12mo across 358 users/orgs via thanks.dev](https://thanks.dev). List them as supplementary inbound, not your primary rail.

## 6. Sales motion (you still have to sell)

Even at 10k stars, inbound alone = komorebi's $155/mo. Run the [first-50-DMs plan](./1000-stars-repo.md#5-the-first-50-dms-plan) continuously, scaled up:

- Maintain a **rolling 50-prospect pipeline**, scored with [../tools/sponsor-fit-score.md](../tools/sponsor-fit-score.md) (pursue 61–100).
- **3-touch-then-close** cadence (initial → +4d → +9d → close), tracked in [../tools/outreach-checklist.md](../tools/outreach-checklist.md).
- Tier your outreach: pitch Gold/Platinum to `ecosystem`/`devrel`/`company_direct` prospects; pitch Bronze/Silver to individuals and small users.
- Publish a [sponsor case study](../templates/media-kit.md) (4–6 paragraphs) after each Platinum deal — it compounds.

## 7. What 10k stars does *not* unlock

- **No Carbon Ads self-serve.** You apply and are vetted; it's sales-assisted with a $5k–$10k/mo advertiser floor.
- **No newsletter revenue without a list.** The newsletter slot is $1,000–2,500/issue (est.) at 10k stars — but only if you actually publish to tens of thousands of subscribers. [JavaScript Weekly's $3,590/issue](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf) sits at 179,802 subs / 41% open. No list, no slot.
- **No Exclusive-tier money without flagship pull.** Astro's $10k/mo and Tailwind's $5k/mo require brand gravity most 10k repos lack.

---

**Bottom line:** at 10k stars, ship the tier ladder + standalone sponsor page + EthicalAds on docs, then keep selling. The program is the easy part; the outbound is what separates komorebi's $155/mo from Astro's $400k/yr.
