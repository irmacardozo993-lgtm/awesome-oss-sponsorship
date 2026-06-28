# Contributing to awesome-oss-sponsorship

First: thank you. The single biggest reason this list stays useful is people
sending PRs with verified platform facts and fresh case studies. This doc tells
you exactly how to do that without getting rejected.

## The one rule that overrides everything

> **Do not publish unverified facts.** If you can't cite an official source,
> mark it `unverified` and say so in the text. A missing fact is fine. A wrong
> fact is not.

All pricing, fees, and revenue numbers must be labeled **estimate / reference
only**. We never promise returns, and we never publish a price as if it were a
quote.

## Ways to contribute

| Area | What you'd do | File(s) |
|------|---------------|---------|
| **Platforms** | Add or correct a monetization platform (status, fees, payout) | `data/platforms.yml`, `docs/*.md` |
| **Affiliate programs** | Add a verified affiliate/referral program | `data/affiliate-programs.yml`, `docs/affiliate-programs.md` |
| **Pricing benchmarks** | Add a real anchored data point or correct an estimate | `data/pricing-benchmarks.yml` |
| **Case studies** | Add a maintainer/company with disclosed sponsorship numbers | `docs/case-studies.md` |
| **Templates** | Improve a copy-paste template (cold email, rate card, sponsor kit) | `templates/*.md` |
| **Translations** | Improve the Chinese edition or add a new language | `README.zh-CN.md`, `docs/*.zh-CN.md` |
| **Fixes** | Typos, dead links, stale statuses | any |

## Adding / updating a platform — checklist

1. **Fetch the official site yourself** (don't trust blog roundups — they rot).
   Open the platform's canonical homepage + pricing/docs page.
2. In `data/platforms.yml`, add or update the entry with these fields:
   `name`, `category`, `url`, `docs`, `status`, `best_for`, `monetization_model`,
   `region`, `payout_support`, `pros` (≤4), `cons` (≤4), `notes`.
3. Set `status` truthfully:
   - `alive` — operating as an OSS monetization platform
   - `alive_pivoted` — still up but changed focus (note the pivot)
   - `alive_unverified` — couldn't fetch (e.g. bot-blocked) — say so
   - `acquired` — bought/redirected (link to the acquirer)
   - `dead` — sunset/404
4. If the platform has a dedicated doc page, mirror the key facts there too
   (`docs/github-sponsors.md`, `docs/open-collective.md`, etc.).
5. Add a one-line entry to the README platform comparison table **and** the
   Chinese README if it's significant.
6. Cite the URL you fetched in the `notes` or via the `url`/`docs` fields.

## Adding an affiliate program — checklist

1. Confirm the program's official page exists and loads.
2. Capture: company, official program URL, commission structure (one-time /
   recurring / % / flat), cookie/attribution duration, payout method & minimum.
3. If a company has **no** public affiliate program, do **not** invent one. You
   may add it to `data/affiliate-programs.yml` with `program: none` and a note,
   so the next person doesn't re-research it.
4. Add it to the comparison table in `docs/affiliate-programs.md`.

## Adding a case study — checklist

1. Only use **publicly disclosed** numbers (official blogs, OpenCollective
   pages, maintainer posts). No leaks, no "a friend told me".
2. Cite the source URL inline.
3. If numbers aren't public, say "no public data" — that's a valid entry.
4. Distinguish **sponsorship** revenue from **commercial** revenue (e.g.
   Tailwind UI license sales ≠ sponsorship).

## Style

- English content: natural, developer-friendly, no marketing tone, no
  Chinglish. Tables and checklists over prose.
- Chinese content (`*.zh-CN.md`): grounded and practical, not lowbrow.
- Every template must be **directly copy-pasteable** — fill-in fields in
  `[brackets]`, no placeholder lorem.
- Keep README sections scannable. This is an Awesome List: people skim.

## Pull request format

- Branch from `main`.
- Title: `add: <platform>` / `fix: <thing>` / `docs: <area>`.
- In the PR description, paste the URL(s) you fetched as evidence.
- If you changed pricing, confirm you labeled it `estimate / reference only`.

## Out of scope

- Get-rich-quick framing, yield promises, or "guaranteed star" schemes.
- Promoting your own sponsor-deal-matching SaaS as if it were neutral data
  (disclose affiliation in the PR).
- Scraping private GitHub Traffic data from repos you don't own.

By contributing, you agree your contributions are licensed under CC-BY-4.0
(code snippets MIT). See `LICENSE`.
