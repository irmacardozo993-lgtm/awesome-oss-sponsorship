# GitHub Sponsors

Deep guide to receiving sponsorship through GitHub Sponsors — the default
starting platform for most maintainers because personal sponsorships carry a
**0% platform fee** and the "Sponsor" button is wired natively into every repo
via `.github/FUNDING.yml`.

All fees below are GitHub's published schedule, cited from
[docs.github.com](https://docs.github.com/en/sponsors) — treat as **reference
only** and re-verify the current schedule before publishing a rate card.

## Table of contents

- [At a glance](#at-a-glance)
- [Eligibility & supported regions](#eligibility--supported-regions)
- [Setup: the exact steps](#setup-the-exact-steps)
- [Tier design](#tier-design)
- [Fees](#fees)
- [Displaying sponsors in your README](#displaying-sponsors-in-your-readme)
- [FUNDING.yml](#fundingyml)
- [Limitations & gotchas](#limitations--gotchas)

## At a glance

| Field | Value |
|-------|-------|
| Status | alive |
| Category | sponsorship (direct recurring/one-time) |
| Best for | Individual OSS maintainers who want 0% fees and native GitHub integration |
| Personal fee | 0% platform fee (only payment-processing applies) |
| Org fee | up to 6% = 3% card processing + 3% GitHub service fee; invoiced billing removes the 3% card fee |
| Payment methods | debit/credit cards. **PayPal was dropped Feb 23, 2023.** |
| Regions | 103 supported. Mainland China NOT supported; HK/Macau SAR are. Russia + sanctioned countries excluded. |
| Payout | Bank via Stripe Connect; bank region must match region of residence |
| Tax | W-9 (US) / W-8BEN (non-US) |
| Tiers | up to 10 one-time + 10 monthly; max $12,000/mo; price immutable after publish |
| Lifetime paid | $40M+ to maintainers; 4,200+ orgs sponsoring |
| Docs | https://docs.github.com/en/sponsors |

Source: [GitHub Sponsors docs](https://docs.github.com/en/sponsors).

## Eligibility & supported regions

- **103 supported regions.** Mainland China (PRC) is **NOT** supported; Hong
  Kong SAR and Macao SAR **are**. Russia and several sanctioned countries are
  excluded.
- **Waitlist exists** for unsupported regions — you can join it, but there is
  no guaranteed timeline.
- **2FA is mandatory** before you can be sponsored.
- A **fiscal host can only be chosen at initial sign-up** — pick correctly the
  first time; you cannot switch later without starting over.
- **Bank region must match your region of residence** (Stripe Connect
  requirement). A bank account in a different country than where you live will
  fail verification.

## Setup: the exact steps

Follow this order — skipping a step blocks the next:

1. **Sponsors → Get sponsored.** Start the application from
   [github.com/sponsors](https://github.com/sponsors).
2. **Enable 2FA** on your GitHub account (required).
3. **Profile.** Link up to **6 repos** you want associated with your sponsor
   profile.
4. **Tiers.** Create one-time and/or monthly tiers (see
   [Tier design](#tier-design)).
5. **Stripe Connect.** Connect a bank account whose region matches your
   residence.
6. **Tax.** Submit W-9 (US persons) or W-8BEN (non-US persons).
7. **Request approval.** GitHub reviews — typically a few days. You are not
   live until approved.

## Tier design

- You can publish **up to 10 one-time tiers + 10 monthly tiers**.
- Maximum monthly tier price: **$12,000/mo**.
- **A tier price is immutable once published.** To change a price you must
  **retire the tier and recreate it** — existing sponsors on the retired tier
  are notified. Plan your ladder before publishing.
- Anchor your ladder to real disclosed tiers (label your own numbers
  **estimate / reference only**):
  - Vite: Backer $5 / Supporter $15 / Bronze $50 / Silver $150 / Gold $500
    ([source](https://opencollective.com/vite))
  - Astro: Backer $10 / Sponsor $100 / Gold $250 / Theme $200 / Platinum
    $1,000 / Exclusive $10,000 ([source](https://opencollective.com/astrodotbuild))
  - Homebrew: Backer $5 / Sponsor $100 ([source](https://opencollective.com/homebrew))
- Common ladder shape: a $2–$10 individual entry, a $50–$250 mid "Sponsor",
  and a $500–$5,000+ "Partner/Platinum" for companies. Caleb Porzio reached
  ~$9,390/mo ($112,680/yr) on GitHub Sponsors
  ([source](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it));
  komorebi (~10k stars) made only ~$155/mo in 2024
  ([source](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/)) —
  the difference is active sales, not stars.

## Fees

| Sponsor type | Platform fee | Card fee | Notes |
|--------------|--------------|----------|-------|
| Personal account | **0%** | processing only | 100% to developer; the default for solo maintainers |
| Organization account | 3% service | + 3% card | up to 6% total |
| Org with **invoiced billing** | 3% service | **0%** (card fee removed) | best for org sponsors who can pay by invoice |

- **No PayPal** — dropped Feb 23, 2023. Cards only.
- Personal sponsorships: 0% platform fee; only payment-processing applies.
- Org sponsorships: up to 6% = 3% card processing + 3% GitHub service fee; the
  3% card fee can be removed with invoiced billing.

Reference only — verify at [docs.github.com/en/sponsors](https://docs.github.com/en/sponsors).

## Displaying sponsors in your README

The dominant pattern across Vue, Vite, Astro, and Homebrew is a bottom
`## Sponsors` section that renders a **remotely-hosted, dynamically-generated
SVG/PNG logo grid**. The grid is built from a sponsors endpoint/JSON, so **the
README never needs editing** when a sponsor joins or leaves — the image
regenerates on the next fetch.

- Tier labels (Diamond/Platinum/Gold) are **rare inside READMEs**; they live on
  an external sponsor page (Vue self-hosts `vuejs.org/sponsor/`). The README
  just renders the grid and links out.
- 2 of 6 sampled repos (Tailwind, esbuild) keep READMEs minimal and route
  sponsorship externally — a legitimate "no-README-sponsor" pattern.
- GitHub Sponsors + Open Collective are the most-cited platforms. Astro uses
  `.github/FUNDING.yml` as the CTA target; Vue self-hosts a sponsor page **and**
  keeps an in-repo `BACKERS.md`.

A minimal README block:

```markdown
## Sponsors

Support this project by becoming a sponsor. Your logo will show up here.

<!-- Replace src with your dynamic sponsors image endpoint -->
<a href="https://github.com/sponsors/[your-handle]">
  <img src="https://[your-sponsors-endpoint]/sponsors.svg" alt="Sponsors" />
</a>
```

## FUNDING.yml

`.github/FUNDING.yml` wires the **Sponsor** button on your repo. Current
supported keys (12): `community_bridge`, `github` (single user OR array up to
4), `issuehunt`, `ko_fi`, `liberapay`, `open_collective`, `patreon`, `tidelift`
(`PLATFORM/PACKAGE`; platforms: npm, pypi, rubygems, maven, packagist, nuget),
`polar`, `buy_me_a_coffee`, `thanks_dev` (`u/gh/USERNAME`), `custom` (single
URL OR array up to 4; any URL containing a colon MUST be wrapped in quotes).

**Not** supported (do not list): `otechie`, `givebutter`, `lfx_crowdfunding`.

For a ready-to-edit file, see the copy-paste template:
[funding-yml-example.md](../templates/funding-yml-example.md).

## Limitations & gotchas

- **Mainland China, Russia, and other sanctioned regions cannot receive
  funds.** HK/Macau SAR are supported. Use the waitlist otherwise, or route
  through an Open Collective fiscal host instead ([open-collective.md](open-collective.md)).
- **No PayPal.** Cards only since Feb 2023.
- **Tier price is immutable after publish** — must retire + recreate to change.
- **Org sponsorships cost up to 6%** unless the sponsor uses invoiced billing
  (drops the 3% card fee).
- **GitHub Traffic is not publicly visible** — only maintainers with push
  access can read Views/Unique visitors/Clones (REST: `/repos/{owner}/{repo}/traffic/views`,
  `/clones`, `/popular/referrers`, `/popular/paths`; fine-grained PAT needs
  `Administration:read`). Traffic is a **14-day rolling self-reported snapshot,
  not a lifetime total**. Any traffic figure you put in a sponsor kit is
  self-reported and not independently verifiable by the sponsor.
- **Stars are a popularity proxy, not a pricing metric.** Price from traffic +
  downloads + audience fit, not star count. See
  [getting-started.md](getting-started.md) and
  [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml).

## See also

- [getting-started.md](getting-started.md) — the 5-minute path and link map
- [open-collective.md](open-collective.md) — when a fiscal host beats a solo account
- [case-studies.md](case-studies.md) — verified disclosed GitHub Sponsors income
- [../templates/funding-yml-example.md](../templates/funding-yml-example.md) — copy-paste FUNDING.yml
- [../templates/rate-card.md](../templates/rate-card.md) — sponsor rate card
