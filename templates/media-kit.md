# Media Kit Template — OSS Repo Sponsor Pitch

A fill-in media kit you send to a sponsor *after* a cold email or DM earns
interest. It exists to answer, in one document, the four questions a sponsor
will ask: **who** sees the placement, **what** inventory you sell, **how much**
(estimate, not a quote), and **who else** has sponsored you.

> The gold-standard structure follows the TLDR media-kit template (audience,
> demographics, engagement, slot inventory, rate card, past sponsors,
> testimonials, case studies/ROI, contact) plus OSS-specific additions:
> public budget ledger, sponsorship tiers + goals, `.github/FUNDING.yml`,
> fiscal host, vetting policy, and a 4–6 paragraph sponsor case study.

## How to use

1. Fill the **[blank template](#blank-template)** below for your repo. Replace
   every `[bracket]`. Numbers you cannot verify → write "no public data"; never
   invent.
2. Cross-link, don't duplicate: point to the live [rate card](rate-card.md)
   (estimate / reference only) and [../data/platforms.yml](../data/platforms.yml)
   rather than re-pasting platform fee tables.
3. **Every price/fee/revenue figure must say "estimate / reference only"**
   unless it is a directly-cited publicly-disclosed figure (then cite the URL
   inline). Never present an estimate as a quote.
4. Send as a **single PDF or a single linked page**, not a folder of files.
   Keep it under ~6 pages.
5. The cold-email/DM that earned this conversation is in
   [cold-email.md](cold-email.md) and [dm-template.md](dm-template.md).

---

## Blank template

Copy from here down. Replace `[brackets]`.

```markdown
# [your-repo] — Sponsor Media Kit

**[one-line project description].** [your-repo-url]
Maintained by [your-name/org]. [license] licensed. [star-count]★ GitHub stars.

## 1. Audience size

- GitHub stars: [star-count] (as of [date])
- GitHub Traffic (self-reported — SEE CAVEAT BELOW):
  - Unique visitors (14-day rolling): [unique-visitors-14d]
  - Views (14-day rolling): [views-14d]
  - Unique cloners (14-day rolling): [unique-cloners-14d]
- Package downloads (independent, publicly verifiable):
  - [npm/PyPI/Docker]: [monthly-downloads] / month ([source-url, e.g. npmjs.com/package/x])
- Documentation site: [monthly-pageviews] pageviews / month ([analytics-tool])
- Newsletter: [subscriber-count] subscribers
- Community: [discord/slack] — [member-count] members

> ⚠️ **GitHub Traffic caveat (read this before quoting it to a sponsor):**
> GitHub Traffic (views, unique visitors, clones, popular referrers/paths) is
> **NOT publicly visible** — only maintainers/admins with **push access** can
> read it via the REST API (`/repos/{owner}/{repo}/traffic/views|clones|...`);
> it returns **403 for everyone else**. Figures are therefore **self-reported
> and not independently verifiable** by the sponsor. They are also a
> **14-day rolling window** (clones/visitors update hourly, referrers/paths
> daily, all UTC) — a short-term snapshot, **not a lifetime total**. Lead with
> independently verifiable metrics (package downloads, docs analytics) and
> treat Traffic as supporting context only.

## 2. Audience demographics

- Primary language/stack: [e.g. TypeScript, Python, Go]
- Developer roles: [e.g. 60% backend, 25% fullstack, 15% DevOps — source: survey/analytics]
- Geography: [e.g. US 35%, EU 30%, India 15%, other 20% — source: analytics]
- Company size: [e.g. 40% enterprise, 35% SMB, 25% indie — source]
- How they arrive: top referrers — [referrer 1], [referrer 2], [referrer 3] (from GitHub Traffic popular/referrers, 14-day, self-reported)

## 3. Engagement

- Docs site: [bounce-rate] bounce, [avg-session] avg session, [pages-per-session] pages/session
- Newsletter: [open-rate]% open, [ctr]% CTR ([source])
- GitHub: [pr-count] PRs / month, [issue-close-med] median issue close time, [contributor-count] contributors
- Star growth: [star-growth-rate] stars / month over last [N] months

## 4. Sponsorship slot inventory

| Slot | Where it appears | Visibility | Intrusiveness |
|------|------------------|------------|---------------|
| README top banner | Top of README, above fold | High | Medium |
| README bottom logo | Bottom Sponsors grid (dynamic SVG) | Medium-high | Low |
| README bottom text | Bottom Sponsors text line | Low | Low |
| Docs site ad | Sidebar/banner on docs | Medium | Low |
| Release note | GitHub Release / CHANGELOG | Medium | Low |
| Newsletter | Dedicated/classified spot in email | High | Medium |

Full per-slot descriptions and value notes: [sponsor-types](../data/sponsor-types.yml).
Pricing (estimate / reference only): [rate card](rate-card.md).

## 5. Rate card (estimate / reference only)

> All figures are **estimates / reference only**, not quotes. Star count is a
> popularity proxy, not a pricing metric — real drivers are unique monthly
> visitors, package downloads, and audience-to-sponsor fit.

See the full [rate card](rate-card.md) for the star-tier × slot grid (USD) and
the RMB domestic version. Representative slots for a [your-star-tier]-star repo:

| Slot | Monthly (est., reference only) | Annual 12-mo (est., 8–10×, −15–20%) |
|------|--------------------------------|--------------------------------------|
| README top banner | $[range] | $[range] |
| Docs site ad | $[range] | $[range] |
| Release note | $[range] | $[range] |
| Newsletter / issue | $[range] | $[range] |

Deal models: monthly recurring, annual (paid yearly), one-time 12-month display,
fixed + affiliate hybrid. Details: [rate card](rate-card.md).

## 6. Sponsorship tiers & goals

| Tier | Monthly | What it includes |
|------|---------|------------------|
| [Backer] | $[x] | Name in BACKERS.md |
| [Sponsor] | $[x] | Logo in bottom grid |
| [Gold] | $[x] | Top banner + release note |
| [Partner] | $[x] | Exclusive placement + newsletter |

**Public budget ledger:** [link to Open Collective / GitHub Sponsors page]
**Current goal:** [e.g. fund 1 part-time maintainer at $[x]/mo — [N]% funded]

## 7. Past & current sponsors

| Sponsor | Tier | Since | Public note |
|--------|------|-------|-------------|
| [name] | [tier] | [date] | [optional quote/ROI] |

## 8. Testimonials

> "[quote from sponsor or user]" — [name], [role] @ [company] ([source-link])

## 9. Case study (4–6 paragraphs)

**[Sponsor X] × [your-repo]** — [one-line outcome].
1. The fit: why [Sponsor X]'s audience overlaps with [your-repo] users.
2. The placement: which slot, what dates, what creative.
3. The exposure: impressions / clicks / conversions (distinguish self-reported
   GitHub Traffic from independently verifiable package/docs metrics).
4. The result: [outcome — signups, pipeline, brand lift]. Be honest about what
   is measured vs estimated.
5. The sponsor's words: a short quote.
6. Why it worked / what we'd change.

## 10. How sponsorship works (logistics)

- Fiscal host: [Open Collective / Open Source Collective / GitHub Sponsors / direct] — [link]
- FUNDING.yml: [.github/FUNDING.yml configured with: your platforms]
- Invoicing: [GitHub Sponsors invoiced billing / Open Collective expense / direct invoice]
- Logo placement: README renders a **dynamically-generated SVG/PNG logo grid**
  from a sponsors endpoint/JSON — no manual README edits needed (Vue/Vite/Astro
  pattern). Sponsors added via JSON entry.
- Vetting policy: [e.g. no gambling/casino/adware/surveillance sponsors; right
  to refuse; logo must be [your-repo]'s existing audience-appropriate]
- Tax: [W-8BEN non-US / W-9 US] handled at the fiscal host.

## 11. Contact

- Primary: [your-email]
- Scheduling: [scheduling-link]
- GitHub: [your-github]
- Sponsor page: [your-repo].tld/sponsors
```

---

## Example — filled in for "AcmeCLI" (fictional 5,000★ repo)

> Fictional repo for illustration only. All numbers below are **estimates /
> reference only** and invented for the template — do not cite them as real.
> Star-tier slot anchors are consistent with
> [pricing-benchmarks.yml](../data/pricing-benchmarks.yml) (5,000★ row).

```markdown
# AcmeCLI — Sponsor Media Kit

**A terminal-first task runner for polyglot dev teams.** https://github.com/acme/acmecli
Maintained by the AcmeCLI core team. MIT licensed. 5,000★ GitHub stars.

## 1. Audience size

- GitHub stars: 5,000 (as of 2026-06-29)
- GitHub Traffic (self-reported — SEE CAVEAT BELOW):
  - Unique visitors (14-day rolling): ~12,000
  - Views (14-day rolling): ~31,000
  - Unique cloners (14-day rolling): ~2,400
- Package downloads (independent, publicly verifiable):
  - npm: ~180,000 downloads / month (https://npmjs.com/package/acmecli)
  - Docker: ~22,000 pulls / month
- Documentation site: ~80,000 pageviews / month (Plausible Analytics)
- Newsletter: 4,200 subscribers
- Community: Discord — 3,100 members

> ⚠️ **GitHub Traffic caveat:** GitHub Traffic (views, unique visitors, clones,
> popular referrers/paths) is **NOT publicly visible** — only maintainers/admins
> with **push access** can read it via the REST API
> (`/repos/acme/acmecli/traffic/views|clones|...`); it returns **403 for everyone
> else**. These figures are therefore **self-reported and not independently
> verifiable** by a sponsor. They are a **14-day rolling window** (clones/visitors
> update hourly, referrers/paths daily, all UTC) — a short-term snapshot, **not a
> lifetime total**. We lead with independently verifiable metrics (npm/Docker
> pulls, Plausible docs analytics) and provide Traffic as supporting context only.

## 2. Audience demographics

- Primary stack: TypeScript (55%), Go (25%), Python (20%) — source: opt-in user survey, n=640
- Roles: 60% backend, 25% fullstack, 15% DevOps — source: survey
- Geography: US 34%, EU 31%, India 16%, other 19% — source: Plausible + npm
- Company size: 40% enterprise, 35% SMB, 25% indie — source: survey
- Top referrers (14-day, self-reported): github.com, google.com, dev.to, news.ycombinator.com

## 3. Engagement

- Docs site: 42% bounce, 2m40s avg session, 3.1 pages/session (Plausible)
- Newsletter: 41% open, 6.2% CTR (Buttondown)
- GitHub: ~28 PRs/month, ~4-day median issue close, 47 contributors
- Star growth: ~210 stars/month over last 6 months

## 4. Sponsorship slot inventory

| Slot | Where it appears | Visibility | Intrusiveness |
|------|------------------|------------|---------------|
| README top banner | Top of README, above fold | High | Medium |
| README bottom logo | Bottom Sponsors grid (dynamic SVG) | Medium-high | Low |
| README bottom text | Bottom Sponsors text line | Low | Low |
| Docs site ad | Sidebar on docs.acmecli.dev | Medium | Low |
| Release note | GitHub Release / CHANGELOG | Medium | Low |
| Newsletter | Classified spot in monthly email | High | Medium |

Per-slot taxonomy: [sponsor-types](../data/sponsor-types.yml). Pricing (estimate
only): [rate card](rate-card.md).

## 5. Rate card (estimate / reference only)

> All figures are **estimates / reference only**, not quotes. Star count is a
> popularity proxy, not a pricing metric — real drivers are unique monthly
> visitors, package downloads, and audience-to-sponsor fit.

Full grid: [rate card](rate-card.md). Representative slots at the 5,000★ tier:

| Slot | Monthly (est., reference only) | Annual 12-mo (est., 8–10×, −15–20%) |
|------|--------------------------------|--------------------------------------|
| README top banner | $1,000–3,000 | ~$8,000–24,000 |
| README bottom logo | $500–1,500 | ~$4,000–12,000 |
| README bottom text | $250–750 | ~$2,000–6,000 |
| Docs site ad | $150–600 | ~$1,200–4,800 |
| Release note | $500–1,500 | ~$4,000–12,000 |
| Newsletter / issue | $500–1,500 | ~$4,000–12,000 |

Docs-site derivation (estimate): 80,000 pageviews / 1000 × ~$2.50 publisher CPM
(EthicalAds anchor) ≈ **$200/mo** — sits in the $150–600 band; we list the band
and derive down. Newsletter anchor: JS Weekly charges $3,590/issue at 180k subs
(estimate / reference only, source: cooperpress.com media kit); at 4,200 subs we
scale well below, hence the $500–1,500 band. Full anchors & derivation method:
[pricing-benchmarks.yml](../data/pricing-benchmarks.yml).

Deal models: monthly recurring, annual (paid yearly, ~10–12×, −15–20%), one-time
12-month display (~8–10× monthly, −15–20%), fixed + affiliate hybrid (retainer
50–70% of slot base + commission on conversions). Details: [rate card](rate-card.md).

## 6. Sponsorship tiers & goals

| Tier | Monthly | What it includes |
|------|---------|------------------|
| Backer | $10 | Name in BACKERS.md |
| Supporter | $50 | Logo in bottom grid |
| Sponsor | $150 | Logo + docs sidebar |
| Gold | $500 | Top banner + release note |
| Partner | $1,000 | Exclusive banner + newsletter spot |

**Public budget ledger:** https://opencollective.com/acmecli (transparent income + expenses)
**Current goal:** fund 1 part-time maintainer at $3,000/mo — 62% funded ($1,860/mo recurring)

## 7. Past & current sponsors

| Sponsor | Tier | Since | Public note |
|--------|------|-------|-------------|
| Northwind Cloud | Gold | 2026-02 | "Best-performing dev channel we ran in Q1" — growth lead |
| Pipeware CI | Supporter | 2026-04 | — |
| Indie backers (×14) | Backer | ongoing | listed in BACKERS.md |

## 8. Testimonials

> "AcmeCLI's docs page gave us a higher-quality sign-up pool than two paid search
> campaigns combined. The audience is exactly who we sell to." — [name], Growth @
> Northwind Cloud (case study link)

## 9. Case study — Northwind Cloud × AcmeCLI

**Northwind Cloud × AcmeCLI — top-banner + docs sidebar over 90 days.**

1. **The fit.** AcmeCLI users run polyglot microservices; Northwind Cloud's
   managed runtime targets exactly that workflow, so the docs sidebar reaches
   devs at the deploy decision.
2. **The placement.** README top banner (SVG, ~728px) + docs sidebar ad
   (EthicalAds-style slot, Northwind creative), 2026-02-01 to 2026-04-30.
3. **The exposure.** Docs sidebar: ~80,000 pageviews/mo (Plausible, verifiable).
   README banner impressions: GitHub Traffic views ~31,000/14-day window
   (self-reported, admin-only, not independently verifiable — see caveat).
4. **The result.** Northwind attributed ~340 signups via the dedicated landing
   URL over 90 days (estimate; not all attributable). Cost per signup well
   below their paid-search CPA (estimate / reference only — confirm with
   Northwind before publishing a hard number).
5. **The sponsor's words.** "Best-performing dev channel we ran in Q1."
6. **Why it worked / what we'd change.** The fit was tight (same stack); next
   time we'd add a release-note mention to time with Northwind's launch.

## 10. How sponsorship works (logistics)

- Fiscal host: Open Source Collective (501(c)(6), US) on the Open Collective
  platform — https://opencollective.com/acmecli . Transparent public ledger.
- FUNDING.yml: `.github/FUNDING.yml` configured with `github: acme` + `open_collective: acmecli`.
- Invoicing: via Open Collective expense workflow; GitHub Sponsors invoiced
  billing available for org sponsors (drops the 3% card fee).
- Logo placement: README renders a **dynamically-generated SVG logo grid** from
  `/sponsors.json` — no manual README edits (Vue/Vite/Astro pattern). Sponsors
  added by appending a JSON entry.
- Vetting policy: no gambling/casino/adware/surveillance sponsors; right to
  refuse; creative must fit a developer audience.
- Tax: W-8BEN (non-US maintainer) handled at the fiscal host.

## 11. Contact

- Primary: sponsors@acmecli.dev
- Scheduling: https://cal.com/acmecli/sponsor
- GitHub: https://github.com/acme/acmecli
- Sponsor page: https://acmecli.dev/sponsors
```

---

## Checklist before you send

- [ ] Every price/fee/revenue figure says "estimate / reference only" OR cites a public URL.
- [ ] GitHub Traffic figures carry the self-reported / 14-day / admin-only caveat.
- [ ] Independently verifiable metrics (npm/Docker/docs analytics) lead the audience section.
- [ ] Slot inventory and pricing match [rate-card.md](rate-card.md) and [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml).
- [ ] Fiscal host + FUNDING.yml + invoicing path are stated.
- [ ] At least one past sponsor or testimonial (if none, say "first sponsor slot open" — don't fabricate).
- [ ] Case study distinguishes measured vs estimated outcomes.
- [ ] Contact + scheduling link work.
