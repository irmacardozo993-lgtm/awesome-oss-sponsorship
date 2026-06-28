# Sponsor Fit Score (0–100)

A lightweight model for ranking sponsorship prospects before you spend a DM on them. Score every prospect, pursue the top of the list, and skip the rest. This protects your reputation (no spray-and-pray) and your time (no dead-end conversations).

> **Star count is a popularity proxy, not a pricing metric.** A high star count on *your* repo does not make a *prospect* a good fit. Fit is about whether *their* users overlap with *your* users and whether they can actually pay and convert. Use this score alongside [../data/sponsor-types.yml](../data/sponsor-types.yml) (sponsor kinds + deal models) and [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml) (slot pricing).

---

## How it works

7 dimensions, each scored **0–10** (use 0 / 2 / 5 / 10 as named guideposts — intermediate values like 7 or 8 are allowed when a prospect sits between anchors), weighted, then normalized to 0–100.

| # | Dimension | Weight | What it asks |
|---|-----------|--------|--------------|
| 1 | User overlap | 20% | Do their users match your repo's users? |
| 2 | Product AOV | 15% | Can they afford it (is the price meaningful to them)? |
| 3 | Developer relevance | 15% | Is their product dev-facing? |
| 4 | Sponsorship history | 15% | Have they sponsored OSS before? |
| 5 | Brand match | 10% | Do values / positioning fit? |
| 6 | Conversion path | 15% | Can users actually click-through and convert? |
| 7 | Budget likelihood | 10% | Does company stage/size imply a marketing budget? |
| | **Total** | **100%** | |

### Formula

```
Total = ( Σ dimension_score × weight ) / 10
```

Each dimension score is **0–10** (the 0 / 2 / 5 / 10 marks are guideposts, not the only allowed values — use intermediates when a prospect falls between anchors); weights sum to 100. Maximum = (10 × 100) / 10 = **100**.

### Score bands

| Score | Band | Action |
|-------|------|--------|
| 0–30 | **Skip** | Don't message. Wrong audience / can't pay / no path. |
| 31–60 | **Maybe** | Park in a "later" list. Contact only if pipeline is thin or they come inbound. |
| 61–85 | **Pursue** | Active outbound; standard 3-touch cadence (see [../tools/outreach-checklist.md](../tools/outreach-checklist.md)). |
| 86–100 | **Priority** | Top of the wave. Personalize heavily; seek a warm intro if possible. |

---

## Scoring rubric (0–10 per dimension; 0 / 2 / 5 / 10 are named guideposts)

### 1. User overlap (20%) — do their users match your repo's users?
- **0** — No overlap; totally different audience.
- **2** — Tangential; a few users might overlap by coincidence.
- **5** — Partial; adjacent verticals, a meaningful minority overlap.
- **10** — Strong; their users *are* your users (e.g., they sell managed hosting, you're a deploy-time library).

### 2. Product AOV (15%) — can they afford it?
- **0** — Free product / no revenue model; a $500/mo ask is a stretch.
- **2** — Low-AOV consumer product (<$10/user); sponsorship is real money to them.
- **5** — Mid-AOV SaaS ($10–100/user/mo or annual contracts in the hundreds–thousands); sponsorship fits a marketing line.
- **10** — High-AOV enterprise/B2B (ACV $10k+); your top tier is rounding error.

### 3. Developer relevance (15%) — is their product dev-facing?
- **0** — End-user consumer product; devs never see them.
- **2** — Dev-adjacent; a few dev touchpoints.
- **5** — Mixed; serves devs + non-devs.
- **10** — Pure dev-facing (DevTools, infra, hosting, CI, observability); reaching devs is their core need.

### 4. Sponsorship history (15%) — have they sponsored OSS before?
- **0** — Never; no public history, skeptical of OSS spend.
- **2** — One-off in the distant past; no program.
- **5** — Sporadic; sponsors occasionally, no dedicated budget line.
- **10** — Active OSS sponsor (GitHub Sponsors profile, [Open Source Pledge](https://opensourcepledge.com) member, visible on other repos' sponsor pages).

### 5. Brand match (10%) — values / positioning fit?
- **0** — Brand clash (e.g., gambling, ad-tech tracker sponsoring a privacy-first repo).
- **2** — Neutral; no obvious fit or clash.
- **5** — Reasonable; compatible positioning.
- **10** — Strong; their brand reinforces your repo's identity (e.g., a privacy vendor sponsoring a security tool).

### 6. Conversion path (15%) — can users click-through and convert?
- **0** — No path; no website, no signup, or conversion happens offline months later.
- **2** — Weak path; link exists but conversion is fuzzy / high-friction.
- **5** — Plausible path; README link → landing page → signup is a real (if unmeasured) funnel.
- **10** — Clean path; self-serve signup, conversions attributable, affiliate tracking possible.

### 7. Budget likelihood (10%) — does company stage/size imply a marketing budget?
- **0** — Solo founder / pre-revenue / unfunded.
- **2** — Tiny bootstrapped; marketing budget is personal money.
- **5** — Growth-stage (Series A–B); a marketing line exists but spend is scrutinized.
- **10** — Well-funded / scale (Series C+, public, profitable at scale); dedicated DevRel/growth budget.

---

## Blank scorecard (copy-paste)

```
Prospect: [name] @ [company] — [role]
Repo: [your-repo] ([stars] stars, [downloads]/mo)

| # | Dimension            | Score (0–10)     | Weight | Weighted |
|---|----------------------|------------------|--------|----------|
| 1 | User overlap         |                  |   20%  |          |
| 2 | Product AOV          |                  |   15%  |          |
| 3 | Developer relevance  |                  |   15%  |          |
| 4 | Sponsorship history  |                  |   15%  |          |
| 5 | Brand match          |                  |   10%  |          |
| 6 | Conversion path      |                  |   15%  |          |
| 7 | Budget likelihood    |                  |   10%  |          |
|   | TOTAL                |                  |  100%  |     /10  |

Weighted sum = [sum]; Total score = [sum]/10 = [0–100]  →  Band: [Skip/Maybe/Pursue/Priority]
```

---

## Fully worked example

**Prospect:** Sam Lee, Head of Growth @ **DevHost** (fictional managed-app-hosting company, Series B).
**Repo:** `fastdb` (fictional, ~1,500 stars, a database client library). We're pricing a Gold-tier pitch (~$500/mo, **estimate / reference only** per [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml)).

| # | Dimension | Score | Weighted (score × weight) | Reasoning |
|---|-----------|-------|---------------------------|-----------|
| 1 | User overlap | 8 | 160 | DevHost users deploy apps that talk to databases; fastdb users are a near-exact subset. Strong but not perfect (some DevHost users don't use this DB). |
| 2 | Product AOV | 5 | 75 | Hosting plans ~$20–500/mo; a $500/mo Gold tier is a real but defensible marketing line, not rounding error. |
| 3 | Developer relevance | 10 | 150 | Pure dev-facing infra; reaching devs at the deploy moment is their core need. |
| 4 | Sponsorship history | 5 | 75 | Sponsored two small OSS repos before (visible on their GitHub Sponsors profile) but no dedicated program/budget line. |
| 5 | Brand match | 8 | 80 | Dev-friendly, no clash; brand reinforces fastdb's "fast/deploy-time" identity. |
| 6 | Conversion path | 7 | 105 | README link → DevHost signup is a real funnel; self-serve signup exists, but attribution to a specific sponsor link is partial. |
| 7 | Budget likelihood | 5 | 50 | Series B growth-stage; a marketing line exists but is scrutinized. |
| | **TOTAL** | | **695** | |

```
Weighted sum = 695
Total score  = 695 / 10 = 69.5  →  ~70  →  Band: Pursue (61–85)
```

**Action:** Pursue. Put Sam at the top of the next outbound wave, use the standard 3-touch cadence, pitch the Gold tier with a first-month discount. Track in [../tools/outreach-checklist.md](../tools/outreach-checklist.md).

### Contrast (one line each, to show the bands)

- **Skip (~15):** A consumer mobile-game company. User overlap 0, dev relevance 0, brand match 2 → no reason to message. Don't.
- **Priority (~88):** A Series-C observability vendor whose SDK integrates with fastdb, already an [Open Source Pledge](https://opensourcepledge.com) member, with self-serve signup. User overlap 10, sponsorship history 10, budget 10 → seek a warm intro, pitch Platinum.

---

## Notes & caveats

- The model is a **triage tool, not a forecast.** It tells you who to talk to, not what they'll pay. Prices come from [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml) and are always **estimate / reference only**.
- Weights are tunable. If you sell an **ad/newsletter slot**, raise *Conversion path* and *User overlap* and lower *Developer relevance* (a non-dev brand with clean attribution can still buy ads). If you sell **in-kind credits**, raise *Budget likelihood* and *Sponsorship history* and lower *Product AOV* (credits cost them wholesale, not retail).
- Sponsorship history is the single best leading indicator — a company already paying other maintainers will pay you. Verify it: check their [GitHub Sponsors profile](https://github.com/sponsors), look for their logo on other repos' sponsor pages, and scan the [Open Source Pledge](https://opensourcepledge.com) member list.
- Re-score quarterly. Companies get funded, pivot, and cut budgets; a Priority prospect can become a Skip in one quarter.
