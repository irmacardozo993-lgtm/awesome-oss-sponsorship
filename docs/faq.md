# FAQ

Short, practical answers. Every price/fee figure is **estimate / reference only** unless it carries an inline source URL.

For deeper detail: [pricing.md](pricing.md), [sponsor-kit.md](sponsor-kit.md), [outreach.md](outreach.md), [readme-monetization.md](readme-monetization.md). Platform facts: [`../data/platforms.yml`](../data/platforms.yml).

---

### Q1. Am I too small to sponsor?

No. The minimum viable kit is audience size (downloads-led) + rate card + fiscal host + `.github/FUNDING.yml` + contact (see [sponsor-kit.md](sponsor-kit.md) §7). At 100 stars you can sell a README bottom-text slot for an estimated $20–75/mo and a docs ad for $10–40/mo (estimate / reference only). One sponsor beats zero. Start with the cheapest slot and the smallest credible price.

### Q2. Will ads hurt my project reputation?

Only if they are intrusive. EthicalAds and Carbon Ads are the dev-audience defaults precisely because they are unobtrusive: one ad per page, above the fold, no tracking, no third-party scripts (EthicalAds), curated native formats (Carbon). Avoid pop-overs, interstitials, and mid-content ads. The README bottom logo grid (Vue/Vite/Astro pattern) is widely accepted and does not read as "ad-first." See [readme-monetization.md](readme-monetization.md) §5.

### Q3. GitHub Sponsors isn't in my country (China) — what now?

Mainland China (PRC) is **not** supported by GitHub Sponsors; Hong Kong SAR and Macao SAR are. Options: (a) use **Open Collective** with a regional fiscal host (Open Source Collective for US-leaning; Open Collective Europe for EU) — sponsors pay the host, the host pays you via bank/PayPal; (b) for domestic RMB sponsors, quote a ¥500–¥5,000/mo band for ~1k-star repos and collect via WeChat/Alipay direct transfer or a domestic entity. Domestic sponsors are best reached via V2EX / 掘金 / 知乎 / 微信群, not GitHub (see [outreach.md](outreach.md) §2). All RMB figures estimate / reference only.

### Q4. How do I disclose affiliate links ethically?

State clearly that the link is an affiliate/referral link and that you may earn a commission, at or near the link itself — not buried in a footer. Track conversions in `affiliate-tracker.csv` (see [outreach.md](outreach.md) §5) so invoicing is auditable. Typical commission: 10–30% recurring or $5–$50 flat per converted user (estimate / reference only, per [`../data/pricing-benchmarks.yml`](../data/pricing-benchmarks.yml)). Never present an affiliate link as a neutral recommendation.

### Q5. Open Collective vs GitHub Sponsors?

**GitHub Sponsors** = 0% fee on personal sponsorships, native GitHub UX, but mainland China/Russia unsupported, no PayPal, org sponsorships up to 6%, tier prices immutable once published. **Open Collective** = public transparent ledger, fiscal host handles legal/tax (great for paying multiple contributors or vendors), plans $0/$60/$320 per host, 5% crowdfunding fee or optional tips. Rule of thumb: solo maintainer receiving funds → GitHub Sponsors (0%); project paying multiple contributors/vendors or needing a legal entity → Open Collective with a fiscal host. Many projects run both. See [`../data/platforms.yml`](../data/platforms.yml).

### Q6. Can I lose stars or reputation by monetizing?

There is no evidence that tasteful sponsorship loses stars — Vue, Vite, Astro, and Homebrew all monetize openly and keep growing. Reputation risk comes from **how** you monetize, not whether: a CLI that blocks startup to show an ad, hidden affiliate links, or selling to a spyware/gambling sponsor will cost trust. Follow the conventions in [readme-monetization.md](readme-monetization.md) and publish a vetting policy (accept/reject categories).

### Q7. How many sponsors is realistic at 1k stars?

Expect **1–4** sponsors with active sales, not dozens. komorebi had ~10k stars and earned only ~$155/mo because it did not actively sell (source: https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/). Caleb Porzio cleared $112,680/yr (source: https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) through active outreach, not star count. Stars get you into conversations; the 50-prospect/3-touch cadence in [outreach.md](outreach.md) closes them.

### Q8. Should I use a fiscal host?

Yes, if you take **company** sponsors or pay anyone other than yourself. A fiscal host (Open Source Collective, 501(c)(6); Open Collective Europe) gives sponsors a legal entity to pay and often to deduct, handles tax forms (automated 990s via OSC), and lets you pay contributors/vendors/bounties. If you are a solo maintainer receiving personal tips only, GitHub Sponsors direct is simpler. See [`../data/platforms.yml`](../data/platforms.yml).

### Q9. Is Tidelift still an option?

**No, not as a fresh option.** Tidelift was **acquired by Sonar** (press release Dec 17, 2024); `tidelift.com` redirects to `sonarsource.com`. The press release says "no immediate planned changes," and it still appears in `.github/FUNDING.yml` as a supported key, but list it as historical/acquired, not something to sign up for fresh. See [`../data/platforms.yml`](../data/platforms.yml).

### Q10. Is Polar still for OSS sponsorship?

**No.** Polar **pivoted** to AI billing / Merchant-of-Record for SaaS/AI products (Starter Free 5.00% + 50¢/txn up to Scale $400/mo 3.40% + 30¢). It no longer has GitHub-Sponsors integration or maintainer-funding features. It is only relevant if your OSS project ships a **paid SaaS/AI product** and needs global tax handling — not for sponsoring maintainers. See [`../data/platforms.yml`](../data/platforms.yml).

### Q11. How do I price with no traffic data?

Price at the **low end** of your star-tier cell in the [pricing.md](pricing.md) grid (e.g., 1k stars → README bottom logo $200/mo, the floor of $200–600). Pitch 50 prospects. After **3 closed deals** at or above that price, raise the published rate 15–25%. As soon as you have traffic/downloads, switch to the derivation method (`monthly_pageviews / 1000 × ~$2.50` for docs; `subs × open_rate × CTR × target_cpc` for newsletter), which is more credible than a star table. All figures estimate / reference only.

### Q12. What if a sponsor wants exclusivity?

Charge a premium — exclusivity removes your ability to sell the same slot to others, so price it at the **top of the slot's range or above** (estimate / reference only), typically as an annual deal (~10–12× monthly). Require a minimum commitment (e.g., 6–12 months) so you are not locked out of the market for a short deal. Exclusivity per **slot** (e.g., "sole README top banner sponsor") is more common and safer than project-wide exclusivity, which can starve your tier ladder. Get it in writing.

### Q13. Should I run a newsletter?

Only if you will **sustain it** — a dead list is worse than none, and a dormant newsletter signals project decay. If you can commit to a consistent cadence, it is the highest $-per-impression slot (anchored to JavaScript Weekly's $3,590/issue at 179,802 subs / 41% open — source: https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf). Sell via Paved (newsletter-only, 25k-sub floor for flat-fee) or Passionfroot/"Zest". Derive your price from `subs × open_rate × CTR × target_cpc` (see [pricing.md](pricing.md) §2). If you cannot sustain it, skip it and grow the docs-site ad instead.

### Q14. How do I handle sponsor churn?

First, find out **why** — ask on exit (budget cut, low ROI, acquisition, personnel change). Second, **keep the slot sold** — a churned logo should be replaced within 2–4 weeks; an empty grid signals decline. Third, **diversify deal models**: mix monthly recurring (MRR) with annual (paid yearly, ~10–12× monthly, −15–20%) so a single monthly cancellation does not zero your revenue. Fourth, keep prospecting continuously — the 50-prospect pipeline in [outreach.md](outreach.md) is not a one-time effort. Log every churn in your tracker with the reason.

### Q15. What about bounties?

Bounties are a **different model** — pay-for-issue/PR, not sponsorship. A funder pays a fixed bounty for a specific issue; a maintainer or contributor claims it on merge (per [`../data/sponsor-types.yml`](../data/sponsor-types.yml)). Platforms: **IssueHunt** — but use `oss.issuehunt.io` (BoostIO), **not** `issuehunt.io` (which is now a cybersecurity bug-bounty platform), and note the OSS side is stale (©2019, no fresh activity). **Algora** still runs OSS bounties but has pivoted to recruiting, so bounties are a secondary sidebar. Bounties fund **specific work**, not your overall project budget — pair them with sponsorship, do not substitute them. See [`../data/platforms.yml`](../data/platforms.yml).

### Q16. Can I use GitHub Sponsors tiers for one-time and monthly at the same time?

Yes. GitHub Sponsors allows **up to 10 one-time + 10 monthly tiers**, max $12,000/mo, per [`../data/platforms.yml`](../data/platforms.yml). One-time tiers suit release-aligned or seasonal sponsors; monthly tiers build MRR. Note: a tier price is **immutable once published** — to change a price you must retire the tier and recreate it (existing sponsors on the retired tier continue at their old price until they move). Plan tier prices before publishing.

### Q17. What is the difference between sponsorship and commercial revenue?

Sponsorship = a company pays you for **reach/brand** to your dev audience (logo, tier, ad slot). Commercial revenue = you sell a **product** (e.g., Tailwind UI, a hosted SaaS). They are separate streams and should not be conflated in a sponsor kit. Example: Tailwind's sponsorship tiers (Partner $5,000/mo etc.) are sponsorship; Tailwind UI's product revenue is commercial and is **not** sponsorship, even though both benefit the maintainer. See the case-study anchors in [pricing.md](pricing.md) §4.

### Q18. How do I price an in-kind / credits sponsor?

Log it at **fair-market value** as sponsorship, even though no cash changes hands. Example: a hosting vendor gives you credits worth $X/yr → record $X/yr of in-kind sponsorship and place their logo in the tier corresponding to that value. DigitalOcean gives free cloud credits tiered by stars ($60/yr at 100+ → up to $20,000/yr at 10,000+) — these are **credits, not cash** (source: https://github.com/Aniket-508/awesome-oss-perks). In-kind deals are real value; do not undercount them when reporting total sponsorship.

### Q19. Do I need a vetting policy?

Yes. Publish which sponsors you accept and reject (e.g., no gambling, no surveillance/spyware, no adult, no competing projects). It protects contributor trust and gives you a clean reason to decline a misfit offer without burning the relationship. It is component #13 in the [sponsor-kit.md](sponsor-kit.md) checklist. Without one, a single bad-logo incident can cost more reputation than the deal pays.

### Q20. How do I disclose that a placement is paid?

At or near the placement itself, in plain language: "Sponsored by [logo]" in a release note, a "Sponsored" label on a newsletter section, a footer note in the README sponsor grid stating logos are paid placements. Disclosure is not optional for affiliate links (Q4) and is best practice for all paid slots — it preserves the trust that makes the audience worth sponsoring in the first place.
