# Sponsor Kit — [project-name]

> Copy-paste sponsor kit template. For the how-and-why guide, see [docs/sponsor-kit.md](../docs/sponsor-kit.md).
> All rate figures come from [templates/rate-card.md](rate-card.md) and are **estimate / reference only** — not a quote, not a guarantee.

## How to use this template

1. Replace every `[bracket]` placeholder with your real data.
2. Every `$` figure is **estimate / reference only** unless you cite a publicly-disclosed source URL inline (citeable anchors live in [docs/case-studies.md](../docs/case-studies.md)).
3. **GitHub Traffic is admin-only.** Only maintainers with push access can read `/repos/{owner}/{repo}/traffic/*` — the API returns `403` to everyone else. Any traffic numbers you publish here are therefore **self-reported** and not independently verifiable by a sponsor. Traffic also rolls on a **14-day window** (visitors/clones update hourly; referrers/popular content update daily; all UTC) — it is a short-term snapshot, not a lifetime total. State this plainly; hiding it erodes trust.
4. Star count is a **popularity proxy, not a pricing metric.** The real drivers are unique monthly visitors (GitHub Traffic) + package downloads (npm/PyPI/Docker) + audience-to-sponsor fit. If you can't show traffic or conversion data, price at the **low end** of the range and raise after the first 3 closed deals.

---

## 1. Repo snapshot

### Template

| Metric | Value | Source / notes |
|---|---|---|
| Stars | `[N]` | `github.com/[owner]/[repo]` |
| Forks | `[N]` | — |
| Watchers | `[N]` | — |
| Open issues / PRs | `[N] / [N]` | — |
| Contributors | `[N]` | — |
| License | `[MIT / Apache-2.0 / …]` | — |
| Primary language | `[TypeScript / Python / …]` | — |
| Latest release | `[vX.Y.Z]` (`[YYYY-MM-DD]`) | — |
| Age | `[N] years` | first commit `[date]` |

**GitHub Traffic (admin-only, 14-day rolling, self-reported — see caveat above):**

| Metric (last 14d) | Value | Endpoint |
|---|---|---|
| Unique visitors | `[N]` | `GET /repos/[owner]/[repo]/traffic/views` |
| Total views | `[N]` | (same) |
| Unique cloners | `[N]` | `GET /repos/[owner]/[repo]/traffic/clones` |
| Total clones | `[N]` | (same) |
| Top referrers | `[list]` | `GET /repos/[owner]/[repo]/traffic/popular/referrers` |
| Top content | `[list]` | `GET /repos/[owner]/[repo]/traffic/popular/paths` |

> Requires push/write access; a fine-grained PAT needs **Administration:read**. Fetch with `gh api repos/[owner]/[repo]/traffic/views` if you have access. **A sponsor cannot verify these numbers — they are self-reported.**

### Worked example — "fastgraph" (fictional 1,000-star repo)

`fastgraph` is a TypeScript graph-layout library (`@fastgraph/core` on npm). 1,012 stars, 124 forks, 48 watchers, 31 open issues, 9 open PRs, 67 contributors, MIT license, latest `v2.4.0` (2026-05-30), first commit 2023-02.

GitHub Traffic (14-day snapshot, self-reported, admin-only): 8,400 unique visitors / 14,200 views; 1,180 unique cloners / 1,950 clones; top referrers `github.com`, `npmjs.com`, `dev.to`; top path `/README.md`.

---

## 2. Package downloads

Unlike GitHub Traffic, these are **publicly verifiable by the sponsor** — cite the registry endpoint so they can check.

### Template

| Registry | Package | Window | Volume | Source |
|---|---|---|---|---|
| npm | `[pkg]` | weekly | `[N]` | `api.npmjs.org/downloads/point/last-week/[pkg]` |
| PyPI | `[pkg]` | monthly | `[N]` | `pypistats.org/api/packages/[pkg]` |
| Docker | `[image]` | total pulls | `[N]` | `hub.docker.com/v2/repositories/[image]` |

### Worked example — fastgraph

`@fastgraph/core` (npm): ~182,000 weekly downloads. `fastgraph` (PyPI, Python bindings): ~9,400 monthly. `fastgraph/core` (Docker): ~22,000 total pulls. A sponsor can verify each at the endpoint above.

---

## 3. User persona

### Template

- **Who:** `[developer role — e.g. frontend engineer building data-viz dashboards]`
- **Why they install:** `[one-sentence job-to-be-done]`
- **Where they come from:** `[top referrers / search terms]`
- **Geography:** `[regions — sponsor-relevant; e.g. EthicalAds pays ~$2.25–$2.75 CPM for EU+NA traffic, estimate / reference only]`
- **Buying intent nearby:** `[adjacent tools/services they also adopt — the sponsor fit]`

### Worked example — fastgraph

Frontend/BI engineers building interactive node-link dashboards in React/Vue. They arrive from npm search, a "react graph visualization" blog post, and the Vue ecosystem docs. ~60% EU+NA traffic (per Traffic referrers + npm region breakdown). Adjacent spend: diagramming UIs, observability dashboards, graph databases — a clean fit for a graph-DB or observability vendor.

---

## 4. Repo positioning

### Template

- **Category:** `[where this sits in the OSS landscape]`
- **Differentiator:** `[one line]`
- **Comparable projects:** `[names + their star counts]`
- **Maturity signal:** `[release cadence / used by / starred by]`

### Worked example — fastgraph

Category: client-side graph layout. Differentiator: sub-millisecond incremental layout (no full recompute on a data tick). Comparable: `d3-force` (~28k★), `cytoscape.js` (~9k★), `vis-network` (~12k★). Maturity: monthly releases, used by 3 named enterprise dashboards, sponsored by `[list]`.

---

## 5. Sponsor slots inventory

Slot taxonomy from [data/sponsor-types.yml](../data/sponsor-types.yml). Mark availability per slot.

| Slot | Location | Value | Available? | Notes |
|---|---|---|---|---|
| README top banner | top of README, above fold | high | `[yes/no]` | 1–2 logos max |
| README bottom logo grid | bottom Sponsors section | medium-high | `[yes/no]` | dynamic SVG, never edit README — see [readme-sponsor-block.md](readme-sponsor-block.md) |
| README bottom text line | bottom Sponsors section | low | `[yes/no]` | BACKERS.md style |
| Docs site ad | docs sidebar/banner | medium | `[yes/no]` | traffic-driven, ~$2.50 CPM (estimate / reference only) |
| Release note | GitHub Release / CHANGELOG | medium | `[yes/no]` | per-release |
| Demo/landing site | demo footer / "powered by" | medium | `[yes/no]` | — |
| Newsletter | email / classified | high | `[yes/no]` | highest $ per impression if you have a list |
| Community channel | Discord/Slack pinned | low-medium | `[yes/no]` | bundled, rarely standalone |
| Sponsor page | `project.tld/sponsors` | medium | `[yes/no]` | where tier ladders live |

### Worked example — fastgraph

Available: README top banner (1 slot), README bottom logo grid (Gold/Silver/Bronze), docs site ad (sidebar), release note (per release), sponsor page (`fastgraph.dev/sponsors`). Not available: newsletter (no list yet), community channel (Discord <400 members).

---

## 6. Price card

Full tiered rate card with derivation is in [templates/rate-card.md](rate-card.md). All figures **estimate / reference only** — not a quote.

### Template (1,000-star row, from [data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml))

| Slot | Monthly (est. / ref only) |
|---|---|
| README top banner | `$400–$1,000` |
| README bottom logo | `$200–$600` |
| README bottom text | `$100–$300` |
| Docs site ad | `$50–$200` |
| Release note | `$200–$600` |
| Newsletter / issue | `$200–$500` |

**Deal-model modifiers (estimate / reference only):** one-time 12-month display ≈ 8–10× monthly (15–20% off vs monthly); annual paid-yearly ≈ 10–12× monthly (15–20% off); affiliate-pure = $0 fixed + 10–30% recurring or $5–$50 flat per converted user; fixed+affiliate = 50–70% of slot base + commission. See [data/sponsor-types.yml](../data/sponsor-types.yml).

### Worked example — fastgraph

Gold logo (bottom grid): **$450/mo** (est. / ref only, mid of $200–$600). README top banner: **$700/mo** (est. / ref only). Docs sidebar ad: derived `30,000 pageviews / 1000 × ~$2.50 ≈ $75/mo` at 70% revshare (EthicalAds, estimate / reference only — see [data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml)). Annual Gold paid yearly: **$4,500/yr** (10× monthly, est. / ref only).

---

## 7. Case study paragraph (4–6 sentences)

### Template

> [Sponsor name] sponsored [project] at the [tier] level for [N] months to reach [audience]. During the period the [slot] received [impressions/clicks], driving [conversions/signups] measured by [method]. [Sponsor] saw [outcome — e.g. X qualified signups, Y% lift in brand-search]. The partnership cost [amount] (est. / ref only) and ran from [date] to [date]. [Optional quote from sponsor]. Reproduce: [how a new sponsor gets the same placement].

### Worked example — fastgraph (fictional)

> GraphDB Co. sponsored fastgraph at the Gold logo tier for 6 months (2026-01 to 2026-06) to reach frontend engineers building graph dashboards. The bottom README logo grid was viewed an estimated 14,200 times in the last 14-day Traffic window (self-reported, admin-only — see caveat in §1), and the sponsor page logged 88 click-throughs to graphdb.co via a tagged link. GraphDB Co. attributed 12 trial signups and 3 paid conversions to the placement (their internal UTM tracking). The partnership cost an estimated $2,700 over 6 months ($450/mo, estimate / reference only — see [rate-card.md](rate-card.md)). Reproduce: a new Gold sponsor gets the same bottom-grid placement plus a `sponsor-page` listing within one release cycle.

---

## 8. Mockup (logo-in-README)

Describe the placement a sponsor's logo receives, so they can picture it before signing.

### Template

- **Where:** `[README top banner OR bottom Sponsors grid OR docs sidebar]`
- **Size:** `[e.g. logo 240×60 top; 120×40 bottom grid]`
- **Link:** `[logo links to sponsor URL]`
- **Generated how:** `[dynamic SVG from sponsors.json endpoint — README never edited]` (see [readme-sponsor-block.md](readme-sponsor-block.md))
- **Tier label:** `[Gold/Silver/Bronze — lives on sponsor page, rarely in README]`

```md
<p align="center">
  <a href="[sponsor-url]"><img src="[sponsors-endpoint].svg" alt="Sponsors"></a>
</p>
```

### Worked example — fastgraph

A Gold sponsor's logo (120×40, light + dark variant) appears in the bottom Sponsors grid of `README.md`, rendered from `https://fastgraph.dev/sponsors.svg` (regenerated from `sponsors.json` on each sponsor change — the README itself is never edited). Gold logos sit in the first row above Silver/Bronze. The tier ladder and full descriptions live on `fastgraph.dev/sponsors`, linked once from the README header.

---

## 9. Cooperation terms

### Template

- **Term:** `[1 month / 3 months / annual]` (annual ≈ 10–12× monthly, 15–20% off — estimate / ref only)
- **Billing:** `[monthly via GitHub Sponsors / Open Collective / direct invoice]`
- **Invoice:** `[who invoices, currency, net-15/30, tax form W-9/W-8BEN if US fiscal host]`
- **Cancellation:** `[notice period — e.g. 30 days; monthly tiers cancel at next cycle]`
- **Exclusivity:** `[none / same-category-exclusive / fully exclusive]`
- **Logo approval:** `[sponsor supplies; maintainer reserves right to refuse]`
- **Placement guarantee:** `[slot + duration; NO impression guarantee — Traffic is self-reported]`
- **Fiscal host (if collective):** `[Open Source Collective 501(c)(6) / regional host]`

### Worked example — fastgraph

Term: monthly or annual (paid yearly ≈ $4,500/yr Gold, estimate / ref only). Billing: GitHub Sponsors (personal, 0% platform fee) for individuals; Open Collective via Open Source Collective (501(c)(6)) for company sponsors needing invoices/tax-deductibility. Invoice: OSC issues USD invoices, net-30, automated 990 tax forms. Cancellation: 30 days notice; monthly cancels at next cycle. Exclusivity: category-exclusive on request (e.g. one graph-DB vendor in the Gold row). No impression guarantee — Traffic figures are self-reported (§1).

---

## 10. Contact

### Template

- **Sponsor page:** `[project.tld/sponsors]`
- **Email:** `[sponsor@project.tld]`
- **FUNDING.yml:** `.github/FUNDING.yml` (see [funding-yml-example.md](funding-yml-example.md))
- **Response SLA:** `[e.g. 3 business days]`
- **Preferred first contact:** `[short email with budget + goal]`

### Worked example — fastgraph

Sponsor page: `fastgraph.dev/sponsors`. Email: `sponsor@fastgraph.dev`. `.github/FUNDING.yml` lists GitHub Sponsors (`@fastgraph`) + Open Collective (`fastgraph`) + a custom sponsor-page URL (see [funding-yml-example.md](funding-yml-example.md)). Response within 3 business days; preferred first contact is a one-line email with target tier and goal.

---

## Checklist before sending

- [ ] Every `[bracket]` replaced.
- [ ] Every `$` figure tagged **estimate / reference only** or cited with a source URL.
- [ ] GitHub Traffic caveat (§1) kept verbatim — admin-only, 14-day, self-reported.
- [ ] Package-download numbers publicly verifiable (registry endpoint cited).
- [ ] Cross-links resolve: [docs/sponsor-kit.md](../docs/sponsor-kit.md), [rate-card.md](rate-card.md), [readme-sponsor-block.md](readme-sponsor-block.md), [funding-yml-example.md](funding-yml-example.md), [data/sponsor-types.yml](../data/sponsor-types.yml), [data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml).
