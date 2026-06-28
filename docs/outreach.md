# Outreach: Finding Sponsors Proactively

Sponsorship does not arrive on its own — the komorebi case (10k stars, ~$155/mo) is the proof. You find sponsors by **identifying companies that already pay for reach to your audience** and pitching them personally. This doc covers where to look, who to contact, how to judge fit, and the cadence that actually closes deals.

All slot prices referenced below are **estimates / reference only**; see [pricing.md](pricing.md).

> The single rule that governs everything else: **do not mass-blast. Personalize.** A generic "Dear Sponsor" email to 200 addresses gets zero replies and burns the list. Fifty researched, personalized pitches beat 500 copy-pasted ones every time.

---

## 1. Where to look for sponsors

### 1a. Similar repos' existing sponsors (highest-signal source)

Companies that already sponsor a comparable repo are pre-qualified: they have a sponsor budget, they understand OSS sponsorship, and they care about your adjacent audience. Mine their public sponsor surfaces:

| Source | What it tells you | How to read it |
|---|---|---|
| `.github/FUNDING.yml` in peer repos | Which platforms a project uses + custom sponsor URLs | `curl` the raw file from the repo's default branch. Current 12 keys: `community_bridge, github, issuehunt, ko_fi, liberapay, open_collective, patreon, tidelift, polar, buy_me_a_coffee, thanks_dev, custom`. See [`../data/platforms.yml`](../data/platforms.yml). |
| `BACKERS.md` in peer repos | Named individual + company backers | A text list in-repo (Vue pattern). Companies here have already paid someone like you. |
| OpenCollective pages of peer projects | Live ledger of who pays what | e.g., Astro/Vite/Homebrew ledgers show real company names and tier amounts. Source: https://opencollective.com/astrodotbuild |
| GitHub Sponsors profiles of peer maintainers | "Past sponsors" + "Current sponsors" sections | Public on each `github.com/sponsors/[user]` profile. |
| A peer repo's README bottom logo grid | The dynamic SVG of current sponsors | Rendered from a sponsors endpoint; names are usually linkable to the sponsor's site. |

Build a target list of **companies appearing across 2+ peer repos** — they have an active OSS-sponsorship program, not a one-off.

### 1b. Stargazers and forkers that are companies

Your own stargazers/forkers are the warmest possible pool: they use your project. Filter them:

- Sort stargazers by the `company` field on their GitHub profile (many devs list an employer).
- Flag org-owned stargazer accounts (the `@company` GitHub org) vs individuals — orgs have budgets.
- Cross-reference forkers: a company fork usually means internal adoption, which is the strongest "they depend on you" signal.

A company that stars + forks + depends on your project is a **company_direct** sponsor (typical deal $100–$5,000+/mo, per [`../data/sponsor-types.yml`](../data/sponsor-types.yml)).

### 1c. DevRel / founder / growth / marketing contacts

These are the people with discretionary reach budget:

| Sponsor kind | Intent | Typical deal | Where they sit |
|---|---|---|---|
| DevRel / developer marketing | Reach devs at the consideration moment | $250–$10,000/mo or campaign | "Developer Advocate", "DevRel", "Developer Marketing" titles |
| Founder / growth lead | Performance: signups, installs, pipeline | Affiliate or fixed+affiliate hybrid | Early-stage startup founders, "Head of Growth" |
| Ecosystem / adjacent vendor | Their product deploys with/integrates yours | $500–$5,000/mo + affiliate | Companies whose tooling sits next to yours in the stack |
| Infrastructure / in-kind | Provide credits/services for a logo | Credits equal to $ value | CI, hosting, DNS, secrets vendors |

Source for typical deals: [`../data/sponsor-types.yml`](../data/sponsor-types.yml) (estimates / reference only).

---

## 2. How to find the right person

Once you have a target company, find the **individual** with budget or influence. Do not pitch a `info@` inbox.

| Channel | Best for | Tactic |
|---|---|---|
| **LinkedIn** | DevRel, Head of Growth, developer marketing at mid/large companies | Search `[company] developer relations` / `developer marketing` / `head of growth`. Filter to current employees. |
| **X (Twitter)** | Founders, indie DevRel, OSS-adjacent devs | Many maintainers and DevRel folk are active here; DM after a public reply. |
| **Product Hunt** | Early-stage founders launching dev tools | Launchers of dev-tool products are actively buying dev reach. |
| **V2EX** | Chinese dev-tool companies, indie founders | `jobs` and `create` nodes; company accounts often list contact. |
| **掘金 (juejin.cn)** | Chinese frontend/backend dev audience + sponsoring companies | Companies running campaigns here have dev-marketing budget. |
| **知乎** | Chinese technical founders / maintainers with a following | Search your stack keywords; answerers with company affiliation are leads. |
| **微信群 (WeChat groups)** | Domestic sponsors, China-based DevRel | Your own project's user group first; then peer-tool groups. Highest-trust domestic channel. |

For international sponsors, LinkedIn + X cover most. For domestic (China) sponsors — who cannot use GitHub Sponsors (PRC unsupported; HK/Macau SAR are) — V2EX / 掘金 / 知乎 / 微信群 are the path, and you need a non-GitHub-Sponsors collection route (Open Collective fiscal host or direct transfer; see [faq.md](faq.md)).

---

## 3. How to judge sponsor-fit

Before you pitch, score the prospect so you spend effort on the ones likely to convert. Use the scorecard at [`../tools/sponsor-fit-score.md`](../tools/sponsor-fit-score.md). The dimensions that matter:

| Dimension | Strong-fit signal | Weak-fit signal |
|---|---|---|
| **Audience overlap** | Their buyer is your user (e.g., CI vendor → testing tool) | Their buyer is unrelated to your audience |
| **Budget signal** | Already sponsors a peer repo / runs dev-marketing campaigns | No public OSS-sponsorship or dev-marketing footprint |
| **Adoption** | They star/fork/depend on your project | No connection to your repo |
| **Timing** | Launching a product, hiring devs, rebranding | Static, no current initiative |
| **Deal model fit** | Wants brand → monthly/annual; wants performance → fixed+affiliate | Wants something you don't sell (e.g., newsletter when you have none) |

Only pitch prospects scoring above your threshold. The scorecard keeps you from burning a personalized pitch on a poor fit.

---

## 4. Outreach cadence: 50 prospects, 3-touch

The cadence that works for solo maintainers (no SDR team):

| Touch | When | Channel | Content |
|---:|---|---|---|
| 1 | Day 0 | Email or DM | 1 personal line (why *them*), 1 sentence on your project's reach (a real number), 1 ask (a 15-min call or "here's the kit"). Link the kit from [sponsor-kit.md](sponsor-kit.md). |
| 2 | Day 4 | Same channel, reply to touch 1 | A single new fact: a comparable sponsor, a tier price, a download number. No guilt, no "just following up" filler. |
| 3 | Day 10 | Different channel if possible (e.g., LinkedIn if touch 1 was email) | A concrete offer: a specific slot at a specific price for a specific period. Make saying yes easy. |

- **Batch size: 50 prospects** at a time. Fewer and you lack signal; more and personalization collapses.
- **Stop after 3 touches** with no reply. Move on; revisit the list next quarter.
- **Track every prospect** in a spreadsheet/CRM (next section). Memory is not a CRM.

The "personalize" rule in practice: touch 1 must contain something that proves you read *their* situation — a reference to their product, their launch, a peer repo they already sponsor. If you can swap the company name and send the same email to 50 people, it is not personalized; rewrite it.

---

## 5. Tools: spreadsheet/CRM + the affiliate tracker

### Prospect tracker (spreadsheet or CRM)

Minimum columns:

| Column | Example |
|---|---|
| Company | [sponsor-name] |
| Contact name + title | Jane Doe, DevRel |
| Channel + handle | LinkedIn / @janedoe |
| Source | Peer repo FUNDING.yml / stargazer / PH launch |
| Fit score | 7/10 (from [`../tools/sponsor-fit-score.md`](../tools/sponsor-fit-score.md)) |
| Slot pitched | README top banner |
| Price pitched | $[X]/mo (estimate / reference only) |
| Touch 1 / 2 / 3 date | 2026-06-29 / — / — |
| Status | Pitched / Replied / Closed / Rejected |
| Notes | "Mentioned their Jun launch; follow up after GA" |

Any tool works: a Google Sheet, Notion, Linear, or a real CRM. The discipline is the columns, not the app.

### Affiliate tracker (`affiliate-tracker.csv`)

When you run **affiliate or fixed+affiliate** deals (per [`../data/sponsor-types.yml`](../data/sponsor-types.yml) and [pricing.md](pricing.md) §7), you must track conversions to invoice correctly. Use `affiliate-tracker.csv` with columns:

```
date,sponsor,deal_model,slot,fixed_monthly_usd,commission_rate,conversions,campaign_link,invoice_status,notes
```

- **deal_model:** `affiliate_pure` or `fixed_plus_affiliate`
- **commission_rate:** 10–30% recurring or $5–$50 flat per converted user (estimate / reference only, per [`../data/pricing-benchmarks.yml`](../data/pricing-benchmarks.yml))
- **conversions:** signups/installs attributed to the sponsor's campaign link
- **invoice_status:** `pending` / `invoiced` / `paid`

Append a row per sponsor per month. Affiliate revenue is only real when the conversions are tracked — an untracked affiliate deal pays nothing.

---

## 6. Outreach checklist

- [ ] Built a target list from peer repos' FUNDING.yml / BACKERS.md / OpenCollective ledgers (section 1a).
- [ ] Added org-owned stargazers/forkers from your own repo (section 1b).
- [ ] Identified the individual (not the inbox) via LinkedIn / X / PH / V2EX / 掘金 / 知乎 / 微信群 (section 2).
- [ ] Scored each prospect with [`../tools/sponsor-fit-score.md`](../tools/sponsor-fit-score.md); only pitch above threshold (section 3).
- [ ] Kit from [sponsor-kit.md](sponsor-kit.md) is live and linkable before touch 1.
- [ ] Batch of 50, 3-touch cadence, personalize every touch 1 (section 4).
- [ ] Every prospect + touch logged in the spreadsheet; affiliate deals in `affiliate-tracker.csv` (section 5).
- [ ] For China-based sponsors, use a domestic channel + non-GitHub-Sponsors collection path.

See also: [sponsor-kit.md](sponsor-kit.md) (what you send), [pricing.md](pricing.md) (what you charge), [readme-monetization.md](readme-monetization.md) (where the logos go once they say yes), [faq.md](faq.md).
