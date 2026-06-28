# Building a Sponsor Kit

This is the **guide** to building a sponsor kit — what to put in it and why. For the fill-in-the-blanks file you hand to a sponsor, use the template at [`../templates/sponsor-kit.md`](../templates/sponsor-kit.md). For how to price the slots inside it, see [pricing.md](pricing.md).

A sponsor kit is the single document (or page) that answers "why should I pay you?" before the sponsor has to ask. Without one, every pitch is a cold email with no evidence. With one, a DevRel manager can forward it internally and get budget approved.

---

## 1. Why you need one

Sponsors are buying **verified reach to a developer audience at the moment of consideration**. They cannot verify that reach themselves — so you have to package the evidence. The kit does three things a README cannot:

1. **Quantifies** your audience (traffic, downloads, subs) in one place.
2. **Prices** the slots you sell, with comparables that justify the number.
3. **De-risks** the sponsor: shows prior sponsors, a vetting policy, and a clear fiscal path.

A repo with 5k stars and no kit gets ignored. The same repo with a one-page kit citing its npm downloads and three current sponsors closes deals.

---

## 2. What to include (the component checklist)

The gold-standard media-kit structure is TLDR's: audience size, demographics, engagement, ad-slot inventory, rate card, past sponsors, testimonials, case studies/ROI, contact. OSS adds **five** repo-specific pieces (public budget ledger, sponsorship tiers + goals, `.github/FUNDING.yml`, fiscal host, vetting policy). Full checklist:

| # | Component | What it proves | Required? |
|---:|---|---|---|
| 1 | **Audience size** | Reach: stars, unique monthly visitors, weekly downloads, newsletter subs | Yes |
| 2 | **Audience demographics** | Who they are: languages, regions, seniority (from surveys / GitHub Traffic referrers) | Yes |
| 3 | **Engagement** | Quality: open rate, CTR, issue/PR activity, release adoption speed | Yes |
| 4 | **Ad-slot inventory** | What you sell: each slot from [`../data/sponsor-types.yml`](../data/sponsor-types.yml), with availability | Yes |
| 5 | **Rate card / pricing** | What each slot costs (monthly + annual + one-time) | Yes |
| 6 | **Past & current sponsors** | Social proof: logo grid + names | Yes (even 1–2 helps) |
| 7 | **Testimonials** | A named sponsor vouching for ROI | Strongly recommended |
| 8 | **Case study (4–6 paragraphs)** | A concrete before/after for one sponsor | Strongly recommended |
| 9 | **Public budget ledger** | Where the money goes (Open Collective page) | Yes if you have one |
| 10 | **Sponsorship tiers + goals** | Tier ladder + what each tier unlocks + a goal bar | Yes |
| 11 | **`.github/FUNDING.yml`** | The machine-readable CTA target | Yes |
| 12 | **Fiscal host** | Legal/tax umbrella (OSC, OC Europe) so sponsors can pay and deduct | Yes for company sponsors |
| 13 | **Vetting policy** | Which sponsors you accept/reject (no gambling, no spyware, etc.) | Yes |
| 14 | **Contact** | Email, calendar link, response-time SLA | Yes |

Items 1–8 and 14 (Contact) are the TLDR gold standard; items 9–13 are the five OSS-specific additions. The template at [`../templates/sponsor-kit.md`](../templates/sponsor-kit.md) lays these out as fillable sections.

---

## 3. How to get GitHub Traffic data (the trickiest piece)

GitHub Traffic is the maintainer-only signal for "how many devs actually looked at my repo." Get it exactly right, because it is the most-misunderstood number in a sponsor kit.

### What the metrics are

The repo Traffic view shows: **Views, Unique visitors, Clones, Unique cloners, Popular referrers, Popular content.**

- **Retention:** ~14 days rolling window. It is a short-term snapshot, **not a lifetime total.**
- **Update cadence:** Clones + visitors update **hourly**; referrers + popular content update **daily**. All times UTC.
- **Visibility:** GitHub Traffic is **NOT publicly visible.** Only maintainers/admins with **push access** can read it. The API returns **403** for everyone else.

### The critical caveat for sponsor kits

Because Traffic is admin-only, **any traffic figure you publish in a sponsor kit is self-reported and not independently verifiable by the sponsor.** Combined with the 14-day rolling window, this means:

- Do not present Traffic as a lifetime or annual total — it is a recent snapshot.
- Pair every Traffic number with a **sponsor-verifiable** signal (npm/PyPI/Docker downloads, which are public). Downloads carry more weight because the sponsor can check them.
- Label Traffic figures as "self-reported, 14-day rolling window."

### REST endpoints

`GET` (require push/write access; a fine-grained PAT needs the **Administration: read** permission):

| Endpoint | Returns |
|---|---|
| `/repos/{owner}/{repo}/traffic/views` | Views + unique visitors (hourly/daily, 14d) |
| `/repos/{owner}/{repo}/traffic/clones` | Clones + unique cloners (14d) |
| `/repos/{owner}/{repo}/traffic/popular/referrers` | Top referring sites (daily) |
| `/repos/{owner}/{repo}/traffic/popular/paths` | Most-viewed paths (daily) |

Example (needs a PAT with Administration: read on the repo):

```bash
curl -H "Authorization: Bearer $GITHUB_TOKEN" \
  -H "Accept: application/vnd.github+json" \
  https://api.github.com/repos/[owner]/[repo]/traffic/views
```

Put the JSON into the kit as: "Past 14 days: **[X] unique visitors, [Y] clones.** Top referrers: [list]. Self-reported, rolling 14-day window; see npm downloads below for a sponsor-verifiable signal."

### How to present it honestly

| Signal | Source | Sponsor-verifiable? | How to present |
|---|---|---|---|
| Unique visitors / clones | GitHub Traffic API | No (admin-only, 14d) | "Self-reported, 14-day rolling window" |
| Popular referrers | GitHub Traffic API | No | Shows where devs come from (docs, search, HN) |
| npm weekly downloads | npmjs.com | **Yes** | Lead with this. Public, historical. |
| PyPI downloads | pypistats / BigQuery | **Yes** | Lead with this for Python projects. |
| Docker Hub pulls | hub.docker.com | **Yes** | Lead with this for containerized projects. |
| Stars | GitHub repo page | Yes | Popularity proxy only — do not price on it (see [pricing.md](pricing.md)). |

---

## 4. How to present npm / PyPI / Docker downloads

Downloads are your strongest sponsor-verifiable reach signal. Present them as a small table with a trend:

```
| Package | Weekly downloads | 30-day trend |
|---|---:|---|
| [your-pkg] (npm) | 142,300 | +8% |
```

- **npm:** weekly downloads are on the package page; 30-day history via `https://api.npmjs.org/downloads/range/last-month/[pkg]`.
- **PyPI:** use `pypistats` (`pypistats recent [pkg]`) or the BigQuery public dataset for long history.
- **Docker:** cumulative pulls on the Hub page; note pulls over-count multi-arch and CI rebuilds, so state the methodology.

Anchor a docs-ad or newsletter price to these (see [pricing.md](pricing.md) §2): docs ad = `monthly_pageviews / 1000 × ~$2.50`; newsletter = `subs × open_rate × CTR × target_cpc`, or anchor to JavaScript Weekly's **$3,590/issue** at 179,802 subs / 41% open (source: https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf — disclosed rate card).

---

## 5. How to write the 4–6 paragraph case study

This is item #8 in the checklist and the part sponsors actually read. Structure it as **Situation → Action → Result → Quote**, across 4–6 short paragraphs:

1. **Situation (1 sentence):** who the sponsor is and what they wanted (e.g., "[Sponsor] wanted to reach backend devs evaluating job-queue libraries").
2. **Action (1 sentence):** what slot they took and for how long (e.g., "They took the README top banner for 6 months at $[X]/mo").
3. **Result (1–2 sentences):** the measurable outcome — clicks, signups, installs, pipeline. Use a real number. If you have no conversion tracking, use impressions/CTR.
4. **Quote (1 sentence):** a named attribution from the sponsor ("'We saw [Y] signups in the first month' — [Name], [Title], [Sponsor]").

Rules:
- No quote, no real number = no case study. Better to omit than to fabricate.
- Get written permission to name the sponsor and use the quote.
- One strong case study beats three vague ones.

The template at [`../templates/sponsor-kit.md`](../templates/sponsor-kit.md) has a fillable case-study block with the [bracketed] variables.

---

## 6. Page vs PDF: how to package

| Format | When | Why |
|---|---|---|
| **Standalone web page** (`[project].tld/sponsors` or `/sponsor`) | Default | Always-current; sponsors can bookmark; logs the dynamic logo grid; is the canonical tier-ladder home (Vue pattern). Matches the "tier labels live on an external page, README just renders the grid" convention. |
| **PDF** | When a sponsor's procurement/legal needs a fixed, dated artifact to attach to a PO | Snapshot the web page to PDF on the day you send it; date-stamp the footer. A PDF freezes numbers, so regenerate per deal. |
| **Notion / Google Doc** | Early stage, no site yet | Fastest to produce; acceptable while you have <5 sponsors. Graduate to a real page before scaling outreach. |

Recommendation: build the web page as source of truth, export a dated PDF only when a sponsor asks for one. Do not maintain a PDF as the primary — it will go stale and you will send wrong numbers.

---

## 7. Build order (do it in this sequence)

1. Collect the three reach signals (Traffic API + npm/PyPI/Docker). Label Traffic as self-reported.
2. Set tier ladder and slot prices from [pricing.md](pricing.md); cite one comparable (Astro/Vite/Tailwind).
3. Stand up a fiscal host (Open Source Collective for US-leaning; Open Collective Europe for EU) so company sponsors can pay and deduct. See [`../data/platforms.yml`](../data/platforms.yml).
4. Add `.github/FUNDING.yml` (the CTA target — current 12 keys documented in the platform data).
5. Write the case-study paragraph (only if you have a real sponsor + number; otherwise skip).
6. Publish as a web page; export a dated PDF on request.
7. Add the vetting policy and contact + response SLA.

You do not need all 14 components on day one. The minimum viable kit is: **audience size (downloads-led) + rate card + fiscal host + FUNDING.yml + contact.** Add testimonials, case studies, and the public ledger as you close deals.

---

## 8. Kit checklist (copy-paste)

- [ ] Audience size: stars + unique visitors (self-reported, 14d) + weekly downloads (verifiable)
- [ ] Audience demographics + top referrers
- [ ] Engagement: open rate / CTR / issue-PR activity
- [ ] Slot inventory (each slot, availability)
- [ ] Rate card: monthly + annual + one-time, every number "estimate / reference only" unless cited
- [ ] Past/current sponsors (logo grid + names)
- [ ] One testimonial (named)
- [ ] One 4–6 paragraph case study (real number + quote) — or omit
- [ ] Public budget ledger link (Open Collective)
- [ ] Tier ladder + goal bar
- [ ] `.github/FUNDING.yml` committed
- [ ] Fiscal host named
- [ ] Vetting policy (accept/reject categories)
- [ ] Contact + response SLA
- [ ] Published as a web page; PDF export on request

See also: [pricing.md](pricing.md), [outreach.md](outreach.md), [readme-monetization.md](readme-monetization.md), [faq.md](faq.md).
