# Worked example: a 100-star repo

> **At 100 stars, your goal is momentum and your first reference sponsor — not money.**
> Star count is a popularity proxy, not a pricing metric. The [komorebi lesson](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) generalizes *downward*: a ~10k-star repo made only ~$155/mo in 2024 because it did no active sales. At 100 stars, with even less leverage, chasing dollars is the wrong KPI. Get one name on the README, ship regularly, and let the tier grow into the audience.

All prices below are **estimate / reference only** — not a quote. They are the LOW end of the 100-star row in [../data/pricing-benchmarks.yml](../data/pricing-benchmarks.yml), which you should raise only after your first three closed deals.

---

## 1. Realistic positioning

You have *signal* (people starred it; some people actually run it) but no *leverage* (no traffic volume, no mailing list, no procurement-ready brand). Position yourself honestly:

- Lead with the **niche and trajectory**, not the star count. "Fastest X for Y, growing 20%/mo" beats "100 stars."
- Name the **real users**: package downloads (npm/PyPI/Docker pulls), GitHub Traffic unique visitors (you can see these; sponsors cannot — see the [traffic caveat](#5-first-deal-strategy) below).
- Sell to **one sponsor at a time.** A 100-star repo cannot deliver impression volume, so do not pitch a "media buy." Pitch goodwill + a cheap logo on a project the sponsor's engineers already touch.

You can sell **1–2 slots max.** Anything more is inventory you cannot fulfill.

## 2. The only slots worth selling

From the 100-star row of the estimate grid (all figures **estimate / reference only**):

| Slot | Monthly range (est.) | Sell at low end | Why / why not |
|------|----------------------|-----------------|---------------|
| README bottom text line | $20–75 | **~$20–50** | Cheapest slot; name + link, BACKERS.md style. Good for individuals. **Sell this.** |
| Release note sponsor | $50–150 | **~$50–100** | Per-release moment; sponsors like version-aligned visibility. **Sell this.** |
| README top banner | $100–300 | — | Too premium for the audience; one banner with no traffic = bad deal for the sponsor. Skip. |
| Docs site ad | $10–40 | — | [EthicalAds requires ~50,000 monthly pageviews](https://www.ethicalads.io/publishers/calculator/); you almost certainly don't have it. Skip. |
| Newsletter per issue | $30–100 | — | You don't have a list yet. Skip. |

**Pricing rule (from the derivation method):** if you can't show traffic or conversion data, price at the LOW end and raise after the first three closed deals. At 100 stars you cannot show traffic, so go low.

## 3. Platform setup (minimal)

Pick **one** cash rail plus an in-kind option. Don't spread thin.

- **GitHub Sponsors** (personal account): 0% platform fee, only payment processing applies. 103 regions; **mainland China is NOT supported** (HK/Macau SAR are). Setup: Sponsors → Get sponsored → enable 2FA → profile (up to 6 repos) → tiers → Stripe Connect (bank region must match residence) → tax (W-9 US / W-8BEN non-US) → Request approval (a few days). See [../data/platforms.yml](../data/platforms.yml).
- **Open Collective** (Discover, $0/mo): use only if you want a public ledger — it makes a 100-star project look "real" to a company procurement team. Free + optional Platform Tips. See [../data/platforms.yml](../data/platforms.yml).
- **In-kind:** [DigitalOcean OSS credits give $60/yr at 100+ stars](https://github.com/Aniket-508/awesome-oss-perks) — **free cloud credits, not cash sponsorship.** Real value; log at fair-market.

### `.github/FUNDING.yml` (minimal, personal)

```yaml
# One cash rail (GitHub Sponsors) + one custom link to your sponsor page.
github: your-username
custom: ["https://your-sponsor-page.example.com/sponsor"]
```

> Any URL containing a colon must be wrapped in quotes. `custom` accepts one URL or an array of up to 4. See the project's own [.github/FUNDING.yml](../.github/FUNDING.yml) for the full annotated key list.

### README bottom Sponsors section (text-only, BACKERS.md style)

```markdown
## Sponsors

Thank you to our backers ([$5/mo and up on GitHub Sponsors](https://github.com/sponsors/your-username)):

<!-- Backers -->
- [Jane Doe](https://example.com) — $25/mo
- [Acme Corp](https://example.com) — $50/mo
<!-- /Backers -->
```

Keep it text-only. Do not fake a logo grid you can't populate — an empty grid looks worse than a short, honest text list.

## 4. Sample outreach DM

Two variants: a **copy-paste template** (bracketed fields) and a **filled example** for a fictional 120-star webhook router, *tinyhook*.

### Template (copy-paste — swap the bracketed fields)

```
Hi [sponsor-first-name],

I maintain [your-repo] ([one-line: what it is / why devs use it]).
It's small but real: [npm/downloads-per-mo or "used by N projects"] downloads/mo,
[stars]-ish stars, and I ship a release roughly every [cadence].

[their-product] users overlap with [your-repo] users — [one concrete reason:
e.g. "anyone routing webhooks to your hosting deploys something like this"].

I'm looking for one founding sponsor to cover infra and a little time.
$[50–100]/mo gets your name + link on the README and a shout-out in release notes.
Happy to do the first month free so you can see it's real.

Worth a quick chat? — [your-name], [your-repo] link
```

### Filled example (tinyhook, 120 stars, ~3k npm downloads/mo)

```
Hi Sam,

I maintain tinyhook — a ~2KB webhook router for Node/edge runtimes.
It's small but real: ~3k npm downloads/mo, 120 stars, and I ship roughly monthly.

Your managed hosting users overlap with tinyhook users — anyone routing inbound
webhooks to a hosted app deploys something exactly like this, and tinyhook is
the lightest option that doesn't pull a framework.

I'm looking for one founding sponsor to cover CI + a little maintenance time.
$75/mo gets your name + link on the README and a shout-out in release notes.
Happy to do the first month free so you can see it's real.

Worth a quick chat? — Alex, https://github.com/your-username/tinyhook
```

**Who to send it to (your prospect pool at this size):**
- A company whose product deploys *with* your repo (ecosystem/adjacent vendor). See `ecosystem` in [../data/sponsor-types.yml](../data/sponsor-types.yml).
- A power user's employer (the person who opens your best issues — ask them, gently, to intro their company).
- An in-kind sponsor (hosting/CI/secrets vendor) trading credits for a logo. See `infrastructure` in [../data/sponsor-types.yml](../data/sponsor-types.yml).

Send **5–10** DMs, not 50. At 100 stars your pool is small and your reputation is fragile — every message should be hand-written. Score each prospect with [../tools/sponsor-fit-score.md](../tools/sponsor-fit-score.md) and track them in [../tools/outreach-checklist.md](../tools/outreach-checklist.md).

## 5. First-deal strategy

You are breaking the **cold-start problem**: a repo with zero sponsors looks unsponsorable, so nobody sponsors it. One logo breaks the loop. Optimize for *getting the first name up*, not for the dollar amount.

Two paths, in priority order:

1. **In-kind credits first.** Easiest close, no cash budget needed on their side, real value to you. [DigitalOcean: $60/yr at 100+ stars](https://github.com/Aniket-508/awesome-oss-perks) (credits, not cash). For infra-adjacent repos, approach hosting/CI/secrets/monitoring vendors for a credits-for-logo deal. Log the fair-market value as sponsorship income in your ledger.
2. **A $50–100/mo backer.** An individual power-user or a small company that depends on your repo. Price at the low end; offer the **first month free** to remove risk. Once the first name is on the README, the second deal is materially easier (social proof).

> **GitHub Traffic caveat:** the traffic numbers you quote (unique visitors, clones) are **self-reported** — only maintainers with push access can read them, the API returns 403 to everyone else, and the window is a rolling 14 days. So any traffic figure you put in a pitch is a short-term, unverifiable snapshot, not a lifetime total. Use it to set a *directional* expectation, never as a hard impression guarantee.

## 6. Momentum checklist (this is the real KPI at 100 stars)

- [ ] Ship on a regular cadence (releases are your sales moments).
- [ ] Write a one-line "what changed + thanks [sponsor]" in every release note.
- [ ] Reply to issues within ~48h; turn good issue reporters into prospects.
- [ ] Keep the README Sponsors section honest and current (remove lapsed backers).
- [ ] Track GitHub Traffic unique visitors and package downloads monthly — when downloads cross ~10k/mo or traffic sustains a higher floor, you've earned the right to raise prices and move to the [1000-star playbook](../docs/1000-stars-playbook.md).

---

**Bottom line:** at 100 stars, get one name on the README (in-kind or $50–100/mo), ship relentlessly, and graduate yourself into a bigger audience. The money follows the momentum, not the other way around.
