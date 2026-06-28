# The 1000-Stars Sponsorship Playbook

A practical, step-by-step playbook for monetizing a repo with ~1,000 GitHub stars. Every dollar figure in this file is **estimate / reference only** unless it cites a disclosed source inline. Star count is a popularity proxy, not a pricing metric — the real drivers are unique monthly visitors (GitHub Traffic), package downloads (npm/PyPI/Docker), and audience-to-sponsor fit.

See [case studies](case-studies.md) for real numbers, [pricing benchmarks](../data/pricing-benchmarks.yml) for the full estimate grid, [sponsor taxonomy](../data/sponsor-types.yml) for slot/kind/deal definitions, and [platforms](../data/platforms.yml) for fee structures.

The 1,000-star row of the estimate grid (monthly USD, **estimate / reference only**):

| Slot | 1k-star range |
|---|---|
| README top banner | $400–1,000 |
| README bottom logo | $200–600 |
| README bottom text | $100–300 |
| Docs site ad | $50–200 |
| Release note | $200–600 |
| Newsletter / issue | $200–500 |

---

## 1. Is a 1k-star repo commercially valuable?

**Yes — but only conditionally, and not because of the star count.**

1,000 stars means a real, growing audience. It is the threshold where a sponsor's logo gets *meaningful* impressions. But star count alone converts to almost nothing (komorebi had ~10k stars and earned **$1,861.88 in all of 2024**, ~$155/mo — see [case studies](case-studies.md)). The commercial value comes from what the stars are a proxy for.

**A 1k-star repo is commercially valuable when ALL of these hold:**

- [ ] It has a real, identifiable user base you can count (npm weekly downloads, Docker pulls, PyPI downloads) — not just stargazers who starred and never installed.
- [ ] Its users are concentrated in a sponsor-worthy audience (professional developers, DevOps, data engineers) rather than students/hobbyists with no budget.
- [ ] You can read your own GitHub Traffic (you are admin/owner) and the unique-visitor number is non-trivial.
- [ ] You are willing to do sales work — DMs, emails, follow-ups. Sponsorship at this scale is sold, not waited for.

**It is NOT commercially valuable when:**

- Stars are mostly drive-by stars from a viral tweet (low install correlation).
- The audience is hobbyist/academic with no commercial sponsor overlap.
- You expect sponsors to find you.

> Rule of thumb (from [pricing benchmarks](../data/pricing-benchmarks.yml)): if you cannot show traffic or conversion data, price at the LOW end of the range and raise after the first 3 closed deals.

---

## 2. Which 1k-star repo types monetize best

Not all 1k-star repos monetize equally. Ranked by sponsor-friendliness:

| Repo type | Monetizes well? | Why | Anchor |
|---|---|---|---|
| **Developer tool / CLI** | Yes — best | Installed by professionals at work; sponsor can reach devs at the consideration moment | Homebrew (package manager) |
| **Framework / meta-framework** | Yes | Captures a whole ecosystem; sponsors want top-of-funnel | Astro, Vite, Vue |
| **SDK / client library** | Yes | Tied to a vendor's product (cloud, DB, API); that vendor is a natural sponsor | PostHog sponsors its dep graph |
| **App / end-user product** | Medium | Users may not be developers; sponsor fit depends on the niche | n/a |
| **Pure library (utility)** | Lower | Used inside other code; users may not even know they use it | komorebi-style ceiling risk |
| **Awesome list / resource** | Lowest | Stars inflate vs. actual usage; no install signal; hard to prove audience | n/a |

**Devtool/CLI/SDK/framework > library > app > awesome-list.** The pattern: the closer your users are to *making a buying decision at work*, the more a sponsor will pay to reach them.

**Library vs. app — the deciding question:** can a sponsor reach a *decision-making developer* through your project? A CLI run by ops engineers (decision moment: "which tool do we standardize on?") is worth more than an app used by end consumers who never buy enterprise software.

**Practical check:** look at your `package.json`/`pyproject.toml` dependents on GitHub. If companies with dev-marketing budgets depend on you, you are in the monetizable tier.

---

## 3. Which sponsors to prioritize

Use the [sponsor kinds taxonomy](../data/sponsor-types.yml). At 1k stars, prioritize in this order:

1. **Companies using your project** (`company_direct`, typical $100–$5,000+/mo) — highest fit. They already derive value; the pitch is "your team relies on this, fund its maintenance." Find them via your GitHub Traffic `popular/referrers` and dependency graph.
2. **Ecosystem / adjacent vendors** (`ecosystem`, $500–$5,000/mo + affiliate) — vendors whose product *deploys with or integrates* your project. Their incentive is structural.
3. **DevRel / developer-marketing teams** (`devrel`, $250–$10,000/mo or campaign) — they have budgets earmarked to reach devs; your repo is a channel.
4. **Infrastructure / in-kind sponsors** (`infrastructure`) — CI, hosting, DNS, secrets vendors (MacStadium, 1Password model). Easiest to close; log at fair-market value.
5. **Individual backers** (`individual`, $2–$50/mo) — goodwill tips. Fill the bottom of your ladder; do not spend sales time here.

**De-prioritize:** founder/growth leads seeking pure performance (affiliate) until you have conversion data to prove ROI — at 1k stars you usually cannot.

**Where to find them:** GitHub Sponsors profiles of *adjacent* projects (who sponsors Vite, Astro, your dependencies?), the Open Source Pledge member list (companies that publicly commit $2,000/engineer/yr — see [Sentry case study](case-studies.md)), and your own referrer traffic.

---

## 4. How to price (low end of the grid)

**Default: price at the LOW end of the 1k-star range, then raise after the first 3 closed deals.**

| Slot | Low-end price (estimate / reference only) | When to use |
|---|---|---|
| README top banner | ~$400/mo | Premium slot; only after you have traffic proof |
| README bottom logo | ~$200/mo | Default first sponsor slot |
| README bottom text | ~$100/mo | Individuals / small backers |
| Docs site ad | ~$50/mo | If docs get real traffic (`pageviews/1000 × ~$2.50`) |
| Release note | ~$200/mo | Per-release; sponsors like version moments |
| Newsletter / issue | ~$200/mo | Only if you actually have a list |

**Three pricing rules:**

1. **Never publish a star-tier price list as a "quote."** All figures are estimate / reference only. Present a *rate card* with ranges, then negotiate per deal. See [templates/rate-card.md](../templates/rate-card.md).
2. **Re-derive from your own data where possible** (more credible than a star table):
   - Docs ad: `monthly_pageviews / 1000 × ~$2.50` (EthicalAds CPM).
   - Newsletter: `subs × open_rate × CTR × target_cpc`, anchored to JS Weekly $3,590/issue at ~180k subs (scale down).
   - README slot: driven by unique monthly visitors (GitHub Traffic) + package pulls + audience fit.
3. **Raise after proof.** After 3 closed deals at the low end, move to mid-range. A signed sponsor is the strongest signal your price was too low, not too high.

**Annual modifier** (from [pricing benchmarks](../data/pricing-benchmarks.yml)): annual paid yearly ≈ 10–12× monthly, discounted 15–20%. Sponsors prefer annual for budgeting — offer it.

---

## 5. How to package the repo

Before the first DM, the repo must *look sponsorable*. A sponsor who clicks through and sees no sponsor infrastructure will not reply.

### 5.1 `.github/FUNDING.yml`

The sponsor button. Current supported keys (12): `community_bridge`, `github` (single user OR array up to 4), `issuehunt`, `ko_fi`, `liberapay`, `open_collective`, `patreon`, `tidelift` (`PLATFORM/PACKAGE`; platforms: npm, pypi, rubygems, maven, packagist, nuget), `polar`, `buy_me_a_coffee`, `thanks_dev` (value `u/gh/USERNAME`), `custom` (single URL OR array up to 4; any URL with a colon MUST be quoted).

> Do NOT list as supported: `otechie`, `givebutter`, `lfx_crowdfunding`. `tidelift` is acquired (→ Sonar); `polar` has pivoted to billing — link only if you ship a paid SaaS.

Minimal 1k-star `FUNDING.yml` (personal maintainer, 0% fee):

```yaml
github: [your-github-username]
custom: ["https://your-sponsor-page.tld"]
```

For a project entity (transparent ledger), use Open Collective:

```yaml
open_collective: [your-collective-slug]
github: [your-github-username]
```

### 5.2 README sponsors section

Follow the dominant pattern (Vue, Vite, Astro, Homebrew): a bottom `## Sponsors` section rendering a **remotely-hosted SVG/PNG logo grid** generated from a sponsors endpoint/JSON, so the README never needs editing. Tier labels (Diamond/Platinum/Gold) live on an external sponsor page, not in the README — the README just renders the grid and links out.

A minimal "no-README-sponsor" pattern (Tailwind, esbuild) — routing sponsorship entirely to an external page — is also legitimate and lower-maintenance. Pick one and be consistent.

### 5.3 Standalone sponsor page

Host `project.tld/sponsors` (or `github.com/sponsors/[you]`). This is where the tier ladder lives. Copy a proven ladder:

- **Conservative (Vite model):** $5 / $15 / $50 / $150 / $500 per month.
- **Ambitious (Astro-inspired):** $10 / $100 / $200 / $250 / $1,000 / $10,000 per month.

At 1k stars, start with the Vite-shaped ladder; you can always add a top tier later.

### 5.4 Rate card

Build a one-page rate card ([templates/rate-card.md](../templates/rate-card.md)) listing each [slot](../data/sponsor-types.yml), its price range (estimate / reference only), audience size, and past sponsors (once you have them). Attach it to every outbound pitch.

### 5.5 Fiscal host (optional, recommended for projects paying multiple contributors)

Route funds through Open Collective (free Discover tier; transparent public ledger; regional fiscal hosts US/EU/NZ/UK; 501(c)(6) via Open Source Collective for US tax-deductibility). Use GitHub Sponsors (0% personal) if it is just you. See [platforms](../data/platforms.yml).

**Packaging checklist:**

- [ ] `.github/FUNDING.yml` present and valid (quote any URL with a colon)
- [ ] README `## Sponsors` section with dynamic logo grid (or a clean external redirect)
- [ ] Sponsor page live with a tier ladder
- [ ] Rate card PDF/page ready to attach
- [ ] Fiscal host or GitHub Sponsors set up (Stripe Connect, tax form done)
- [ ] GitHub profile lists the repo in your Sponsors profile (up to 6 repos)

---

## 6. How to prepare GitHub Traffic data

GitHub Traffic is your strongest internal proof — and it has sharp limits you must understand before putting it in a pitch.

**What the UI shows:** Views, Unique visitors, Clones, Unique cloners, Popular referrers, Popular content.

**Critical constraints (get these exactly right):**

- **Admin-only.** Traffic is NOT publicly visible. Only maintainers/admins with push access can read it. The REST endpoints (`GET /repos/{owner}/{repo}/traffic/{views,clones,popular/referrers,popular/paths}`) return **403 for everyone else**. A fine-grained PAT needs `Administration:read`.
- **14-day rolling window.** Retention is ~14 days. Clones + visitors update hourly; referrers + popular content update daily. All UTC.
- **Therefore self-reported.** Any traffic figure you publish in a sponsor kit is SELF-REPORTED and not independently verifiable by the sponsor. Combined with the 14-day window, Traffic is a *short-term self-reported snapshot*, not a lifetime total.

**How to prepare it for a pitch:**

1. Pull the four endpoints weekly for ~4 weeks before pitching, so you can show a *trend*, not a single 14-day spike.
2. Combine Traffic with **verifiable** public signals — npm weekly downloads, Docker pulls, PyPI stats — so the sponsor has something they can cross-check, not just your self-report.
3. In the rate card, label Traffic figures as "self-reported, 14-day rolling" and put the verifiable download numbers alongside.

**REST endpoints:**

```
GET /repos/{owner}/{repo}/traffic/views
GET /repos/{owner}/{repo}/traffic/clones
GET /repos/{owner}/{repo}/traffic/popular/referrers
GET /repos/{owner}/{repo}/traffic/popular/paths
```

**Traffic prep checklist:**

- [ ] You have push access (you are the owner — confirmed)
- [ ] 4 weeks of weekly snapshots saved (views + unique visitors + referrers)
- [ ] Public download/pull stats captured alongside (npm/Docker/PyPI) for cross-verification
- [ ] Rate card labels Traffic as "self-reported, 14-day rolling"

---

## 7. How to send the first 50 DMs

Sponsorship at 1k stars is sold, not waited for. The first 50 outbound contacts are where most maintainers quit. Here is the system.

### 7.1 Build the list (50 targets)

- 20 from your GitHub Traffic `popular/referrers` (companies whose docs/blogs refer users to you).
- 15 from your dependency graph (companies that depend on you, or that you depend on and are adjacent vendors).
- 10 from the Open Source Pledge member list + published sponsor tables (Sentry, PostHog — see [case studies](case-studies.md)).
- 5 ecosystem/adjacent vendors whose product integrates with yours.

For each target, find a named human: DevRel lead, engineering manager, or founder (LinkedIn, GitHub org members, company "about" page). Generic `info@` inboxes convert near zero.

### 7.2 Cadence

- **Volume:** 50 over ~3 weeks (~15–20/week). Do not blast all 50 in a day — it reads as spam and you cannot personalize at that rate.
- **Channel:** email first (LinkedIn second). GitHub issues/DMs are a last resort and feel intrusive.
- **Follow-up:** one nudge at day 5, one final at day 12, then drop. Three touches max.
- **Personalization:** each first email must reference something specific to that company (their dependency on you, a blog post of theirs, a referrer in your Traffic). Zero personalization = zero replies.

### 7.3 Template (bracketed variables to fill per target)

> Subject: Sponsoring [your-repo] — [sponsor-name] shows up in our traffic
>
> Hi [first-name],
>
> I maintain [your-repo], a [one-line description] with ~1,000 GitHub stars and [N] monthly [npm installs / Docker pulls]. [Sponsor-name] appears in our top referrers / is listed as a dependent — your team already uses it.
>
> I'm opening a small sponsorship program to fund maintenance. Slots start at ~$[low-end-price]/mo (estimate / reference only) for a README logo placement, with an annual discount. Full rate card: [rate-card-url]. Transparent ledger: [opencollective-or-github-sponsors-url].
>
> Worth a 15-minute call to see if it fits your dev-marketing budget? I'm free [two specific time windows].
>
> [your-name]

### 7.4 Tracking

Track in a spreadsheet (or CRM): target, contact, channel, date sent, follow-up dates, status (no-reply / replied / call booked / closed / rejected), outcome. At 50 contacts you need this to follow up — at 500 it is mandatory.

**First-50 checklist:**

- [ ] 50 named-human targets built (with source for each)
- [ ] Cadence scheduled (~15–20/week, 3 touches max)
- [ ] Template personalized per target (specific reference required)
- [ ] Tracking sheet live before the first send

---

## 8. How to design a low-price first-month test

Your first sponsor is not about revenue — it is about proof. Design the deal to be easy to say yes to.

**Test structure:**

- **Price:** the low end of the 1k-star range for your chosen slot (e.g., ~$200/mo for a README bottom logo — estimate / reference only). For the very first sponsor, consider a one-month trial at 50% off to remove risk.
- **Slot:** README bottom logo (the dominant pattern; low intrusiveness; easy to render dynamically). Avoid the top banner for the first deal — save premium inventory.
- **Term:** one month, then month-to-month. Do not lock in a year at the test price — you will raise it.
- **Deliverable:** logo in the dynamic Sponsors grid + a one-line entry on your sponsor page. No custom content, no newsletter yet.
- **Payment:** GitHub Sponsors (0% fee, personal) or Open Collective (transparent ledger). Avoid high-fee platforms (Patreon 10%, Buy Me a Coffee 5% + processing) for the first deal.

**What the test proves:**

- [ ] Your pitch converts.
- [ ] Your traffic/install claims are credible to a real buyer.
- [ ] The slot renders correctly and the sponsor is visible.
- [ ] You can fulfil without it dominating your maintenance time.

A closed first deal — even at a below-market test price — is worth more than ten "interested" replies. It becomes the social proof for sponsor #2.

---

## 9. How to go from 1st to 2nd sponsor (social proof)

The hardest gap is 0 → 1. The second-hardest is 1 → 2. Social proof is the lever.

**Sequence:**

1. **Ship the first sponsor's logo immediately** in the dynamic README grid and on the sponsor page. Make it visible before you pitch #2.
2. **Ask the first sponsor for a one-line testimonial** and permission to name them. ("X sponsors [your-repo] to fund maintenance — [quote].") Put it on the rate card.
3. **Mention the first sponsor by name in pitch #2.** "We recently closed our first sponsorship with [company-A] at ~$[price]/mo." This converts far better than an unverified claim of value.
4. **Offer sponsor #2 a small premium** for being early — e.g., the same price but the top banner slot instead of bottom logo, or an annual discount — to reward committing before the roster fills.
5. **Publish a public budget/ledger** (Open Collective makes this automatic). A transparent ledger where sponsor #1's contribution is visible is itself social proof that the program is real and the money is accounted for.

**Why this works:** sponsors are risk-averse. The existence of a paid peer de-risks the decision. This is exactly why published sponsor tables (PostHog, Sentry — see [case studies](case-studies.md)) are so effective: they are public proof that other companies paid.

**2nd-sponsor checklist:**

- [ ] Sponsor #1 logo shipped and visible
- [ ] Testimonial secured + on rate card
- [ ] Pitch #2 names sponsor #1 explicitly
- [ ] Public ledger live (Open Collective or GitHub Sponsors profile)

---

## 10. How to avoid hurting OSS reputation

Monetization done badly alienates users, contributors, and future sponsors. Guardrails:

- [ ] **Never paywall the OSS itself.** The project stays free (OSI license). You sell *exposure* and *maintenance funding*, not features. Sponsor logos are placement, not gated functionality.
- [ ] **Keep ads non-intrusive.** One logo grid at the bottom of the README; one ad per page on docs (EthicalAds rule); no popups, no interstitials, no README top banner above the project description unless it is a premium paid slot the community expects.
- [ ] **CLI/`--help` sponsor lines must be opt-in or silent by default.** Never block or slow startup (per [sponsor taxonomy](../data/sponsor-types.yml) `cli_startup` notes). Cache-bust carefully.
- [ ] **Issue/PR template sponsors stay subtle.** Do not make support issues feel like ad pages.
- [ ] **Disclose in-kind sponsors at fair-market value.** Log MacStadium/1Password-style credits as sponsorship value, not hide them.
- [ ] **Be transparent about money.** Use a public ledger (Open Collective). Hiding where sponsorship goes is the fastest way to lose contributor trust.
- [ ] **Keep delivering the project.** Sponsorship must not slow releases or pull-request triage. A stalled repo cannot retain sponsors.
- [ ] **No "get rich" framing.** Every public figure labeled estimate / reference only unless it is a cited disclosed number. Never promise returns.
- [ ] **Respect sponsor-fit.** Reject advertisers mismatched to a developer audience (e.g., gambling, low-quality SEO) — one bad ad tanks credibility with the users who matter.
- [ ] **Attribution honesty.** Distinguish sponsorship income from commercial product revenue in any public post (the Tailwind lesson in [case studies](case-studies.md)).

The reputation test: would a power user who has never sponsored still recommend your project after seeing your sponsor page? If yes, you have held the line.

---

Related: [case studies](case-studies.md), [launch plan](launch-plan.md), [platforms](../data/platforms.yml), [pricing benchmarks](../data/pricing-benchmarks.yml), [sponsor taxonomy](../data/sponsor-types.yml), [rate card template](../templates/rate-card.md), [sponsor-fit-score tool](../tools/sponsor-fit-score.md).
