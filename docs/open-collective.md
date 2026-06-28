# Open Collective & Open Source Collective

Guide to receiving sponsorship through **Open Collective** (the platform) and
**Open Source Collective / OSC** (the US 501(c)(6) fiscal host that runs on top
of it). Choose this over GitHub Sponsors when your project needs to pay
multiple contributors or vendors, or wants a fully transparent public ledger.

All fees are reference only — re-verify at
[docs.opencollective.com](https://docs.opencollective.com) before relying.

## Table of contents

- [At a glance](#at-a-glance)
- [What is a fiscal host?](#what-is-a-fiscal-host)
- [Open Source Collective (OSC)](#open-source-collective-osc)
- [Plans & fees](#plans--fees)
- [The transparent public ledger](#the-transparent-public-ledger)
- [Regional fiscal hosts](#regional-fiscal-hosts)
- [GitHub Sponsors vs Open Collective](#github-sponsors-vs-open-collective)
- [Setting up a collective](#setting-up-a-collective)
- [Integrations](#integrations)

## At a glance

| Field | Open Collective | Open Source Collective |
|-------|-----------------|------------------------|
| Status | alive | alive |
| Category | fiscal host (platform) | fiscal host (US entity) |
| URL | https://opencollective.com | https://www.oscollective.org |
| Best for | Public, transparent ledger with a fiscal host handling legal/tax | US-leaning OSS projects needing a 501(c)(6) legal/financial umbrella |
| Legal status | Stewarded by Open Finance Consortium (OFiCo), 501(c)(6) nonprofit | US 501(c)(6); multi-country/currency payouts |
| Plans | Discover $0 / Basic $60 / Pro $320 per fiscal host | Runs on the Open Collective platform (see OC /pricing) |
| Fees | Free + optional Platform Tips, OR 5% Crowdfunding Fee | Not disclosed on landing page |
| Scale | 10,000+ collectives, $40M+ managed | Same platform |
| Docs | https://docs.opencollective.com | https://docs.oscollective.org |

## What is a fiscal host?

A **fiscal host** is a legal/financial umbrella that holds funds on behalf of
your project. Instead of sponsors paying you personally (and you handling tax,
accounting, and liability), sponsors pay the host, and the host pays your
contributors, vendors, and expenses according to a public budget.

You do **not** incorporate, open a bank account, or file tax forms yourself —
the host does. The trade-off is a layer of approval/expense workflow: every
expense passes through the host before payout.

When you need one:

- You pay **multiple contributors** (core team, contractors).
- You pay **vendors** (hosting, design, security audits).
- You want **tax-deductible sponsorship** for US-based company sponsors (via
  OSC's 501(c)(6) status).
- You want a **public, auditable ledger** of income and expenses.

When you do **not** need one: you are a solo maintainer receiving recurring
sponsorship with no expenses to pay — GitHub Sponsors at 0% is simpler. See
[github-sponsors.md](github-sponsors.md).

## Open Source Collective (OSC)

OSC is the **US 501(c)(6) fiscal host** that runs on top of the Open Collective
platform. Pick it when you need a legal entity to hold project funds and pay
contributors.

- **501(c)(6) status** — tax-deductible for US sponsors in many cases (verify
  deductibility with the sponsor's accountant; 501(c)(6) is a business league,
  not a 501(c)(3) charity).
- **Accounting, invoicing, grants, trademark, and employment** are handled by
  the host.
- **Automated 990 tax forms.**
- **Real-time open budgets**; integrates with GitHub Sponsors and thanks.dev.
- Multi-country/multi-currency payouts via bank or PayPal.
- Fee structure is not disclosed on its own site — see Open Collective /pricing
  for the plan/host structure.

EU and other regions use sibling hosts (Open Collective Europe, etc.).

## Plans & fees

Open Collective plans are **per fiscal host** (not per collective):

| Plan | Price | Included | Overage |
|------|-------|----------|---------|
| Discover | $0/mo | free host | +$10/extra collective, +$1/extra expense |
| Basic | $60/mo | — | — |
| Pro | $320/mo | — | +$20/extra collective, +$2/extra expense |

**Fee model (two options):**

- **Free with optional Platform Tips** — sponsors can add a tip on top of their
  contribution; the platform is funded by tips.
- **OR a 5% Crowdfunding Fee** in place of tips — a flat 5% of funds raised.

Payment-processing fees apply on top and are **not itemized** on the /pricing
page. Treat all figures as reference only — verify at
[opencollective.com/pricing](https://opencollective.com/pricing).

## The transparent public ledger

Every collective has a **public ledger**: all income and expenses are visible
on the collective's page. This is the defining feature and the reason companies
trust OC with sponsorship — there is no hidden spend.

Verified live snapshots (2026-06-29):

| Collective | Total raised | Annual est (reference only) | Tiers (monthly) | Source |
|------------|-------------|------------------------------|------------------|--------|
| Astro | $836,294.61 | $438,118.47 | Backer $10 / Sponsor $100 / Gold $250 / Theme $200 / Platinum $1,000 / Exclusive $10,000 | [opencollective.com/astrodotbuild](https://opencollective.com/astrodotbuild) |
| Vue.js | $852,880.86 | $219,061.00 | (Evan You historical ~$8,000/mo 2016 → ~$9,800/mo 2017) | [opencollective.com/vuejs](https://opencollective.com/vuejs) |
| Vite | $162,400.34 | $102,536.16 | Backer $5 / Supporter $15 / Bronze $50 / Silver $150 / Gold $500 | [opencollective.com/vite](https://opencollective.com/vite) |
| Homebrew | $486,870.56 | — | Backer $5 / Sponsor $100 | [opencollective.com/homebrew](https://opencollective.com/homebrew) |

Total-raised and tier prices are publicly disclosed (cited). The "annual est"
column is a derived estimate / reference only.

## Regional fiscal hosts

Funds route through regional fiscal hosts so payouts land in local currency
and banking:

- **US** — Open Source Collective (501(c)(6))
- **EU** — Open Collective Europe
- **NZ** — Open Collective New Zealand
- **UK** — Open Collective UK (as available)

Pick the host whose region matches where your project operates and where your
contributors bank. The fiscal host is chosen at collective creation.

## GitHub Sponsors vs Open Collective

| Criterion | GitHub Sponsors | Open Collective |
|-----------|----------------|-----------------|
| Solo maintainer, no expenses | ✅ best (0%) | overkill |
| Multiple contributors/vendors | ❌ personal only | ✅ fiscal host pays them |
| Public expense ledger | ❌ | ✅ transparent |
| US tax-deductible for sponsors | ❌ | ✅ via OSC 501(c)(6) |
| Fee | 0% personal / up to 6% org | $0–$320/mo host + 5% or tips |
| Setup speed | fast (a few days approval) | slower (host onboarding) |
| China mainland payout | ❌ not supported | via regional host (verify) |

Many projects run **both**: GitHub Sponsors for direct recurring personal
sponsorship, Open Collective for the project's collective budget and expenses.
They integrate (see below).

## Setting up a collective

1. **Create an account** at [opencollective.com](https://opencollective.com).
2. **Create a collective** and pick a **fiscal host** (e.g. OSC for US-leaning
   projects). The host is chosen at creation and is hard to switch later.
3. **Publish tiers** (monthly and/or one-time). Anchor to the verified ladders
   above; label your own prices estimate / reference only.
4. **Connect GitHub** so the collective links from your repo's
   `.github/FUNDING.yml` (`open_collective:` key — see
   [funding-yml-example.md](../templates/funding-yml-example.md)).
5. **Submit expenses** through the host as you incur them; the host approves
   and pays. Everything is public.

## Integrations

- **GitHub Sponsors** — a collective can receive GitHub Sponsors funds; the two
  coexist (direct sponsorship via Sponsors, project budget via OC).
- **thanks.dev** — dependency-tree auto-funding can route into an Open
  Collective collective. Companies fund their whole dep graph; OC receives and
  distributes. (Canonical committed $120k/12mo across 358 GitHub users/orgs —
  [thanks.dev](https://thanks.dev).)
- **EthicalAds** — publisher payouts can go to OpenCollective (among PayPal,
  GitHub Sponsors, or Stripe bank). See [ad-networks.md](ad-networks.md).

## See also

- [getting-started.md](getting-started.md) — the 5-minute path and link map
- [github-sponsors.md](github-sponsors.md) — the 0%-fee solo alternative
- [case-studies.md](case-studies.md) — verified disclosed collective numbers
- [../data/platforms.yml](../data/platforms.yml) — the source of truth
