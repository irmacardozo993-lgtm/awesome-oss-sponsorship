# Polar

> **Read this first: Polar is no longer an OSS sponsorship platform.** It
> pivoted to **AI-era billing / Merchant-of-Record**. If your goal is
> sponsoring maintainers or accepting donations, **use GitHub Sponsors or Open
> Collective instead** — see [github-sponsors.md](github-sponsors.md) and
> [open-collective.md](open-collective.md). Polar is relevant **only** when
> your OSS project ships a paid SaaS/AI product and needs global tax handling.

All fees below are Polar's published schedule, cited from
[polar.sh/docs](https://polar.sh/docs) — treat as **reference only** and
re-verify before signing up.

## Table of contents

- [At a glance](#at-a-glance)
- [The pivot: what Polar was vs what it is](#the-pivot-what-polar-was-vs-what-it-is)
- [Current plans & fees](#current-plans--fees)
- [When Polar IS relevant](#when-polar-is-relevant)
- [When Polar is NOT relevant](#when-polar-is-not-relevant)
- [Merchant-of-Record, explained](#merchant-of-record-explained)

## At a glance

| Field | Value |
|-------|-------|
| Status | alive_pivoted |
| Category | billing_mor (Merchant-of-Record) — **not** sponsorship |
| URL | https://polar.sh |
| Docs | https://polar.sh/docs |
| What it is now | AI-era billing / MoR for SaaS/AI products billing usage (tokens, API calls, compute) |
| Role | Calculates, collects, and remits tax worldwide (EU B2B reverse charge & B2C) |
| Best for | SaaS/AI products that need global tax handling. No longer an OSS sponsorship product. |
| Open source | Yes (Apache 2.0) |
| Adapters | 12 frameworks + JS/Python/Go/PHP SDKs |

## The pivot: what Polar was vs what it is

| | Before (OSS funding/rewards) | Now (AI billing / MoR) |
|---|------------------------------|------------------------|
| Purpose | Fund maintainers; issue/PR rewards; sponsorships | Bill usage for SaaS/AI products; handle global tax |
| GitHub Sponsors integration | Yes | **No** — removed |
| Maintainer-funding features | Yes | **No** — gone |
| Donation/sponsorship tools | Yes | **No** — not the product anymore |
| Core value prop | Sponsor OSS work | Be the Merchant-of-Record for a paid product |

The OSS angle is now **incidental**. Polar still ships open-source billing
adapters and SDKs, but the product is billing infrastructure for products that
charge money — not a way to get sponsored for maintaining OSS.

## Current plans & fees

Reference only — verify at [polar.sh/docs](https://polar.sh/docs).

| Plan | Price | Fee per txn | Notes |
|------|-------|-------------|-------|
| Starter | Free | 5.00% + 50¢ | entry tier |
| Pro | $20/mo | 3.80% + 40¢ | — |
| Growth | $100/mo | 3.60% + 35¢ | — |
| Scale | $400/mo | 3.40% + 30¢ | — |
| Startup Program | Free (12 mo) | 3.40% + 30¢ | for qualifying startups |

Payout is via payment providers; international cards may incur extra fees.
Methods are not enumerated on the docs page.

## When Polar IS relevant

Use Polar when **all** of these are true:

- Your OSS project **ships a paid product** (a SaaS, an AI API, a hosted
  service, a usage-billed tool charging for tokens/compute/calls).
- You need a **Merchant-of-Record** to calculate, collect, and remit tax
  worldwide (EU B2B reverse charge, B2C VAT, etc.) so you don't build a tax
  engine yourself.
- You want billing adapters/SDKs (12 frameworks; JS/Python/Go/PHP) integrated
  into your product.

In that case Polar handles tax, refunds, chargebacks, and fraud as full MoR —
strong for a small team that would otherwise drown in international tax
compliance.

## When Polar is NOT relevant

Do **not** use Polar if any of these describe you:

- You want to **be sponsored** for maintaining OSS (use
  [GitHub Sponsors](github-sponsors.md), 0% personal).
- You want to accept **donations/tips** (use
  [GitHub Sponsors](github-sponsors.md) or
  [Open Collective](open-collective.md)).
- You want a **public sponsor ledger** or fiscal host (use
  [Open Collective](open-collective.md)).
- You want a **GitHub "Sponsor" button** via FUNDING.yml — Polar dropped the
  GitHub Sponsors integration; `polar:` is still a valid FUNDING.yml key but it
  points at a billing product, not sponsorship.

If your goal is sponsorship/donation and you sign up for Polar expecting that,
you will be in the wrong product.

## Merchant-of-Record, explained

A **Merchant-of-Record (MoR)** is the legal entity that sells to the end
customer — it is the seller of record on the invoice, collects tax at
point-of-sale, and remits it to each jurisdiction. You hand Polar the tax
compliance burden; Polar takes a per-transaction fee for it.

- EU B2B: reverse-charge handled.
- B2C: VAT/sales tax calculated, collected, and remitted per country.
- Refunds, chargebacks, and fraud are Polar's problem, not yours.

This is a **billing** service, distinct from sponsorship. Sponsorship is a
company giving you money to support your work; MoR is a company buying your
product and Polar handling the sale. Conflating them is the most common mistake
with Polar post-pivot.

## See also

- [getting-started.md](getting-started.md) — the 5-minute path and link map
- [github-sponsors.md](github-sponsors.md) — the actual sponsorship platform (0% personal)
- [open-collective.md](open-collective.md) — fiscal host + public ledger
- [../data/platforms.yml](../data/platforms.yml) — source of truth (Polar entry)
