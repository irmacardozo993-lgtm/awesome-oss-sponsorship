# Affiliate & Referral Programs

Affiliate/referral is the **performance** half of monetization: $0 fixed, you earn a
commission only when a user you refer converts. It pairs naturally with sponsorship —
the "fixed fee + affiliate hybrid" is the single best deal model for an OSS repo,
because it gives the sponsor a guaranteed retainer *and* lets you share upside when
their users actually convert. See [`../data/sponsor-types.yml`](../data/sponsor-types.yml)
`deal_models.fixed_plus_affiliate`.

> **All commissions below are reference only and change frequently.** Re-verify at the
> official URL before promoting. This doc only lists programs **confirmed at the
> company's own site** as of 2026-06-29. See
> [`../data/affiliate-programs.yml`](../data/affiliate-programs.yml) for the structured DB.

---

## 1. The honest picture

Most developer-tool companies **do not run a public affiliate program**. The biggest
names in the OSS/devtool world — OpenAI, Anthropic, GitHub, Supabase, Vercel (outside v0),
Cloudflare, AWS — have **no individual-earner referral commission**. Their "partner
programs" are B2B channel programs for consultancies and resellers, not for an OSS
author with a README.

That means two things:

1. **Do not trust third-party affiliate directories** (OpenAffiliate, AffiliPilot,
   Awin listings). They frequently publish programs that do not exist on the company's
   own site. This file is the de-bunked list.
2. **The listable programs are concentrated in scraping/automation, hosting, and a few
   AI-voice/learning SaaS.** If your repo's audience is in one of those verticals,
   affiliate is a real revenue line. If your audience is "AI API consumers," there is
   almost nothing to monetize via referral today.

---

## 2. Active, listable programs (verified 2026-06-29)

| Company | Category | Commission (reference only) | Cookie | Payout / min | Fit |
|---|---|---|---|---|---|
| [Railway](https://railway.com/affiliate-program) | Cloud deploy | 15% recurring, 12 mo | n/d | GitHub Sponsors / BMC, no min | ★★★ best devtool fit, cash via Sponsors |
| [Neon](https://neon.com/programs/open-source) | Serverless Postgres | $20 cash per qualifying referral | n/d | GitHub Sponsors, monthly | ★★★ OSS-program purpose-built for maintainers |
| [ElevenLabs](https://elevenlabs.io/affiliates) | AI voice API | 22% recurring 12 mo (11% Business) | n/d | PartnerStack, $5 min | ★★★ TTS/voice in devtools/agents |
| [Apify](https://apify.com/partners/affiliate) | Scraping | 20%→30% (3 mo then lifetime, cap $2,500/customer) | 45 d | PayPal/bank/Wise, $100 + ≥3 customers | ★★★ scrape/automate |
| [Bright Data](https://brightdata.com/affiliate) | Proxies/scraping | 50% up to $2,500/customer + 15% 2nd-tier | 90 d | PartnerStack | ★★★ proxy infra |
| [ScrapingBee](https://www.scrapingbee.com/affiliates/) | Scraping API | 25% recurring lifetime (cap $62.25/mo) | n/d | PayPal, $50 + ≥2 customers | ★★★ scrape API |
| [Browserless](https://www.browserless.io/affiliate) | Headless browser | 20–30% tiered recurring, 12 mo | 90 d | PayPal/bank, $50 | ★★★ Puppeteer/Playwright |
| [n8n](https://n8n.io/affiliates/) | Automation | 30% recurring 12 mo (Cloud only) | n/d | PayPal, €100 | ★★★ self-hostable automation |
| [Make](https://www.make.com/en/affiliate) | Automation | 35% recurring 12 mo | 30 d | Wise, $100 + ≥3 users | ★★ low-code automation |
| [Raycast](https://www.raycast.com/blog/affiliate-program) | macOS devtool | 30% recurring (Pro) | n/d | Wise, £50 | ★★ macOS audience only |
| [Pluralsight](https://www.pluralsight.com/affiliate) | Dev learning | $1/free trial + 30%/10%/5% one-time | 7 d | CJ | ★★ dev-learning audience |
| [DigitalOcean](https://www.digitalocean.com/affiliates) | Cloud hosting | 10% recurring 12 mo (affiliate) OR $25 credit (referral) | n/d | Network (Awin/CJ) | ★★ deploy/host; use affiliate for cash |
| [Netlify](https://www.netlify.com/partners/) | Jamstack hosting | 20% recurring, up to 12–24 mo | n/d | PartnerStack (application required) | ★★ frontend deploy |
| [Vercel / v0](https://partners.dub.co/v0) | Frontend deploy | v0: 30% recurring 6 mo + $5/lead | n/d | Dub | ★★ v0/AI-editor centric |

`n/d` = not documented on the official page. ★★★ = strong OSS/devtool audience fit.

---

## 3. Closed / sunset / dead (do not promote)

| Company | Status | Note |
|---|---|---|
| [Hetzner](https://www.hetzner.com/legal/referrals) | **sunset 2026-06-15** | Personal referral links dead; now a generic €20 new-customer promo. No cash. |
| [Notion](https://www.notion.com/affiliates) | **closed to new** | $50/signup + 20% yr1, 180-day cookie — but "not accepting new affiliates." |
| [ShareASale](https://www.shareasale.com) | **defunct 2025-10-06** | Merged into Awin. Sign up at awin.com (consumer-retail-skewed). |
| [Heroku](https://www.heroku.com/partnering/) | **dead** | No cash referral program; Enterprise End of Sale for new customers (Feb 2026). |

---

## 4. No public program found (verified absent — ignore third-party listings)

These were **confirmed absent at the official site** as of 2026-06-29. Third-party
directories that list them are wrong; do not promote them as affiliate programs.

**AI API / model platforms (the big blind spot):** OpenAI, Anthropic, Replicate, Together
AI, OpenRouter, Mistral, Groq, Hugging Face, DeepSeek. Their "partner networks"
(OpenAI Partner Network, Claude Partner Network) are B2B enablement programs with
**no commissions**. Mistral's Ambassador pays in API credits, not cash. There is
effectively **no affiliate monetization for an "AI API consumer" audience today.**

**Cloud/hosting:** Render, Fly.io (both confirmed "we do not have one"), Cloudflare
(channel-only, no individual program; Warp+ credits ended Nov 2024), AWS
(organization-only via Partner Network; "AWS affiliate" pages misdirect to Amazon
Associates retail).

**Database / backend / monitoring:** Supabase, PlanetScale, Upstash, Sentry, PostHog,
Meilisearch, Axiom — none run a referral/affiliate program. (Upstash has a $1,000/mo
credit **grant** for accepted OSS projects — that's sponsorship, not affiliate.
Sentry has a sponsored-account application for OSS/edu/startup — also not affiliate.
PostHog explicitly states "we do not have any official partners.") Turso launched a
Partner Program (May 2026) that says "earn revenue share" but discloses **no rates** —
a closed partner network, not a listable affiliate (status: unverified).

**Dev SaaS:** Linear, JetBrains, Egghead, Frontend Masters (now Master.dev), Zapier —
no public affiliate program. (Zapier's referral benefit is restricted to certified
Solution Partners with a professional website; not open to OSS authors.)

**GitHub itself:** No public referral/affiliate/reseller-commission program. Verified
across github.com/partners, the Copilot Partner Program, and third-party directories.
GitHub Sponsors is donations, **not** affiliate. Individual OSS authors cannot earn
referral commissions on GitHub paid plans.

---

## 5. Networks you can join as a publisher

If you want to browse many devtool affiliate offers in one dashboard, join a network.
Only two are true open marketplaces; the rest are per-merchant infrastructure.

| Network | Type | Best for | Signup | Min payout |
|---|---|---|---|---|
| [PartnerStack](https://partnerstack.com) | Open marketplace | **Best for devtool/SaaS** — 2,500+ programs, devtool-dense (Netlify, n8n, ElevenLabs, Bright Data) | Free self-serve, no invite | $5 |
| [Impact](https://impact.com) | Open marketplace | Broad cross-brand; less devtool-dense, more marketing SaaS (Shopify, Semrush, Canva, Hostinger) | Free self-serve | $10 |
| [Lemon Squeezy](https://www.lemonsqueezy.com) | Per-merchant MoR | Indie/dev SaaS (acquired by Stripe, still active) | Join each merchant individually | ~$10 |
| [Rewardful](https://www.rewardful.com) | Per-merchant infra | SaaS infra (Stripe/Paddle); Raycast, Replit, Beehiiv, Baremetrics | Join each brand's portal | per-merchant |
| [Tolt](https://tolt.com) | Per-merchant infra | SaaS startups; Typefully, Fathom, Folk.app | Join each brand's portal | ~$50 |
| [Awin](https://www.awin.com) | Open marketplace | Former ShareASale parent; **consumer-retail-skewed**, not devtool-relevant | Free, 1–3 day approval | $20 |

**Practical move:** create a free PartnerStack account (it has the densest devtool
inventory and a $5 payout floor), then apply to each brand's program individually.
Some auto-approve; some review. Add tax info before withdrawing.

---

## 6. The fixed + affiliate hybrid (the best deal model)

Pure affiliate pays nothing if conversions are slow; pure fixed sponsorship caps your
upside. The hybrid captures both:

> "**$[X]/mo retainer** guarantees you a spot and baseline exposure; **+[Y]% of
> converted users** from your referral link lets you share upside when it works.
> Estimated — reference only; we'll show you the click/signup numbers monthly."

This is the model to pitch `founder_growth` and `ecosystem` prospects (see
[`../data/sponsor-types.yml`](../data/sponsor-types.yml)). Sponsors like it because
their downside is capped; you like it because a hit converts asymmetrically. Use the
[Sponsor Fit Score](../tools/sponsor-fit-score.md) `conversion_path` dimension to
decide whether a prospect can even attribute conversions — if not, drop the affiliate
leg and sell fixed-only.

---

## 7. Ethical disclosure (non-negotiable)

Affiliate links in an OSS repo must be disclosed, or you will lose the trust that makes
the repo valuable in the first place.

- **FTC requirement (US) / similar in EU/UK/AU:** clearly and conspicuously disclose
  that you earn a commission on linked products, before the link or at the point of the
  link. "Affiliate" or "we may earn a commission" is the standard phrasing.
- **README convention:** a one-line disclosure near the affiliate link, e.g.
  `> ⚄ Affiliate link — we earn a commission on signups, at no cost to you.` See the
  copy-paste snippet in [`../templates/readme-sponsor-block.md`](../templates/readme-sponsor-block.md).
- **Separate from sponsorship logos:** a sponsor who pays a fixed retainer is a
  sponsor; a vendor you link for commission is an affiliate. Do not blur them —
  label each clearly.
- **Never link a product you wouldn't recommend unpaid.** The conversion hit from a
  single bad recommendation outlasts the commission.
- **Pick vendors your audience actually converts on.** A 30% recurring commission on a
  product your users don't buy is worth $0. A 10% commission on the hosting they
  already use is real money.

---

## 8. Tracking

Log every affiliate deal in [`../templates/affiliate-tracker.csv`](../templates/affiliate-tracker.csv)
(date, company, program, referral URL, commission type/rate, cookie days, clicks,
signups, conversions, revenue, payout method/min, status). Reconcile monthly against
the network's dashboard. Affiliate revenue is **recognized on conversion/payout, not
on click** — do not log clicks as revenue.

---

## 9. Domestic (China) note

Most domestic AI-API platforms (国内大模型 API) and major cloud vendors do **not** run
public individual affiliate programs comparable to the above. Domestic monetization for
an OSS repo leans on **fixed sponsorship + 分销 (reseller/distribution) deals negotiated
directly** with 国内 AI-API 平台、云服务商、开发者工具商, often as a "固定费用 + 返佣"
hybrid. See the Chinese README ([`../README.zh-CN.md`](../README.zh-CN.md)) for 国内
私信模板 and the ¥500–¥5,000/mo band. Treat any 国内 "affiliate" listing on a
third-party directory as unverified unless the vendor's own site confirms it.

See also: [sponsor-types](../data/sponsor-types.yml) · [sponsor-fit-score](../tools/sponsor-fit-score.md) · [readme-monetization](readme-monetization.md) · [pricing](pricing.md)
