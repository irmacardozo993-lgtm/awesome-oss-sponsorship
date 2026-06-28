# README & Surface Monetization

Where sponsorship physically lives across your project's surfaces. Every slot from [`../data/sponsor-types.yml`](../data/sponsor-types.yml) maps to a real location; this doc covers each one, the real-repo conventions to follow, and the one hard rule (CLI startup must be opt-in and silent).

For the fill-in sponsor-block markup, use [`../templates/readme-sponsor-block.md`](../templates/readme-sponsor-block.md). For pricing each slot, see [pricing.md](pricing.md).

---

## 1. The slot map

| Slot | Location | Value | Intrusiveness | Real-repo convention |
|---|---|---|---|---|
| README top banner | Top of README, above the fold | High | Medium | One–two logos max. Premium price. |
| README bottom logo grid | Bottom `## Sponsors` section | Medium-high | Low | **Dominant pattern** — dynamic SVG grid (Vue/Vite/Astro/Homebrew). |
| README bottom text list | Bottom Sponsors section | Low | Low | BACKERS.md style; name + link. Cheapest slot. |
| Docs site ad | Sidebar/banner on docs site | Medium | Low | EthicalAds/Carbon Ads; traffic-driven, not star-driven. |
| Release note sponsor | GitHub Release / CHANGELOG entry | Medium | Low | Per-release; sponsors like version-aligned moments. |
| Issue/PR template sponsor | Footer of issue/PR templates | Low | Low | Subtle; avoid making issues feel like ad pages. |
| Demo / landing site sponsor | Demo site footer or "powered by" | Medium | Low | Strong when the demo/playground gets real traffic. |
| CLI startup / `--help` | One line on CLI launch or update check | Low-medium | Medium | **MUST be opt-in / silent by default. Never block or slow startup.** |
| Newsletter | Dedicated email / classified / primary spot | High | Medium | Highest $ per impression if you have a list. |
| Discord / Slack / 微信群 | Pinned message, channel name, role | Low-medium | Low | Engaged but small; often bundled, rarely standalone. |
| Standalone sponsors page | `project.tld/sponsors` | Medium | None | Where tier ladders actually live (Vue pattern). README just links here. |

Slot value/intrusiveness from [`../data/sponsor-types.yml`](../data/sponsor-types.yml). Prices are **estimates / reference only** — see [pricing.md](pricing.md) §3 for the grid.

---

## 2. README top banner

The highest-visibility real estate in the repo. One or two logos max, above the fold, before the project description.

- **Price:** top of the star-tier grid (e.g., 1k stars → $400–$1,000/mo; estimate / reference only).
- **Convention:** keep it minimal — a single centered logo with a link. Do not stack a wall of logos at the top; that is what the bottom grid is for.
- **Risk:** highest intrusiveness of the README slots. A loud top banner can read as "ad-first" to contributors. Reserve it for a platinum/title sponsor.

---

## 3. README bottom logo grid (the dominant pattern)

This is what Vue, Vite, Astro, and Homebrew all do, and it is the default you should adopt.

**Convention — render a remotely-hosted dynamic SVG/PNG grid:**

- The grid is **generated from a sponsors endpoint or JSON file**, so the README never needs manual editing. Add a sponsor → the SVG regenerates → the README image updates on next render.
- **Tier labels (Diamond/Platinum/Gold) are RARE inside the README itself.** They live on an external sponsor page (`project.tld/sponsors`); the README just renders the grid, optionally grouped by tier silently.
- A `## Sponsors` section at the bottom of the README, above the license, is the standard placement.

Use the markup in [`../templates/readme-sponsor-block.md`](../templates/readme-sponsor-block.md) — it points an `<img>` at your dynamic sponsors endpoint and degrades to a text list if the image fails.

**Price:** medium-high (1k stars → $200–$600/mo for a logo slot; estimate / reference only). Tier the grid: Gold/Silver/Bronze rows, each priced per [pricing.md](pricing.md).

---

## 4. README bottom text list

The cheapest slot and the lowest intrusiveness. A simple bulleted list of names + links, often maintained in a separate `BACKERS.md` that the README includes or links.

- **Price:** low (1k stars → $100–$300/mo; estimate / reference only). Also the natural home for individual backers at $2–$50/mo.
- **Convention:** Vue self-hosts `vuejs.org/sponsor/` **and** keeps an in-repo `BACKERS.md`. Both patterns coexist; the text list is for the long tail of small backers.

---

## 5. Documentation site ad

Decouples revenue from star count — it is driven by docs traffic, not popularity. This is the slot where downloads/traffic matter most (see [pricing.md](pricing.md) §2: `monthly_pageviews / 1000 × ~$2.50`).

- **Platforms:** EthicalAds (self-serve, privacy-first, ~$2.50 CPM after 70% revshare, min $50 payout, requires ~50,000 monthly pageviews, **one ad per page, above the fold, dev-only audience, no newsletter/README**) or Carbon Ads (curated, sales-assisted, advertiser min $5,000–$10,000/mo). See [`../data/platforms.yml`](../data/platforms.yml).
- **Convention:** one unobtrusive ad unit in the docs sidebar or above the fold. Do not let ads push content below the fold on mobile.

All ad-platform figures are **estimates / reference only** except where cited: EthicalAds publisher CPM ~$2.25–$2.75 (source: https://www.ethicalads.io/publishers/calculator/); Carbon Ads advertiser min $5,000–$10,000/mo (source: https://carbonads.net).

---

## 6. Release note sponsor

A sponsor line/section inside the GitHub Release notes or CHANGELOG entry for a version.

- **Price:** medium (1k stars → $200–$600/mo; estimate / reference only).
- **Convention:** sponsors like version-aligned moments — a launch, a major release, a blog post. Offer per-release sponsorship so a sponsor can align with a specific version's buzz.
- **Format:** a short "Sponsored by [logo]" line at the top or bottom of the release notes, with a disclosure that it is a paid placement.

---

## 7. Issue / PR template sponsor

A subtle footer line in `.github/ISSUE_TEMPLATE/*.yml` and the PR template.

- **Price:** low; rarely sold standalone, usually bundled.
- **Convention:** keep it subtle and avoid making support issues feel like ad pages. A one-line footer is the ceiling. Contributors opening their first issue should not feel pitched at.

---

## 8. Demo / landing site sponsor

A "powered by" or footer credit on the project's demo site or playground.

- **Price:** medium (estimate / reference only).
- **Convention:** only valuable when the demo site gets real traffic (e.g., a live playground). A demo site with no visitors is not a sellable slot — check the traffic first.

---

## 9. CLI startup / `--help` (the hard rule)

A single line on CLI launch or update check. **This slot has a non-negotiable constraint:**

> **MUST be opt-in or silent by default. Never block or slow startup.**

- Default behavior: **no sponsor output on launch.** The line appears only if the user opts in (e.g., `--show-sponsors`) or it is displayed silently on update-check, never on every run.
- **Never** block startup to fetch an ad, **never** add latency to `--help`, **never** require network for the sponsor line on a normal command.
- **Cache-bust carefully:** if you fetch a sponsor logo/line, cache it locally and refresh on a slow path (update check), not on every invocation.
- **Price:** low-medium (estimate / reference only). The constraint is the point — a CLI that delays startup to show an ad loses users faster than it earns.

This is the one slot where violating the convention actively harms the project. When in doubt, omit it.

---

## 10. Newsletter

The highest $-per-impression slot if you have a list. Anchored to JavaScript Weekly: **$3,590/issue** primary spot at 179,802 subs / 41% open (source: https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf — disclosed rate card).

- **Price:** high (1k stars → $200–$500/issue; estimate / reference only). Derive from `subs × open_rate × CTR × target_cpc` (see [pricing.md](pricing.md) §2).
- **Convention:** offer a primary spot, a secondary/classified spot, and a sponsored-links spot at different price points. Disclose paid placements clearly.
- **Platforms for selling:** Paved (newsletter-only, 3,000+ newsletters, 25k-sub floor for flat-fee / 1M-impression floor for PPC) or Passionfroot (now "Zest", B2B GTM, 2% self-managed / 15% platform-matched). See [`../data/platforms.yml`](../data/platforms.yml).
- Only run a newsletter if you will sustain it — a dead list is worse than none. See [faq.md](faq.md) "Should I run a newsletter?"

---

## 11. Discord / Slack / 微信群 (community channel)

A pinned message, channel name, or a sponsor role in your community.

- **Price:** low-medium; engaged but small audiences. **Often bundled with a README slot, rarely standalone.**
- **Convention:** a `#sponsors` channel or a sponsor role is low-intrusiveness and adds perceived value to the sponsorship package without much marginal cost.
- For 微信群 (WeChat groups), this is also a domestic-sponsor acquisition channel (see [outreach.md](outreach.md) §2).

---

## 12. Standalone sponsors page

`project.tld/sponsors` — where the **tier ladder actually lives**. This is the Vue pattern: the README renders a dynamic grid and links out to this page, which shows full tiers, goals, the public budget ledger, and the FUNDING.yml CTA.

- **Price:** no direct price (it is the storefront, not a slot), but it is what makes the other slots sellable.
- **Convention:** this page is the canonical home for `Partner/ Ambassador/ Supporter`-style tier labels (Tailwind: Partner $5,000/mo, Ambassador $2,500/mo, Supporter $500/mo, Individual $120/yr — source: https://tailwindcss.com/sponsor). The README should **not** duplicate the full ladder; it links here.

---

## 13. The "no-README-sponsor" pattern (legitimate)

2 of 6 sampled repos (Tailwind, esbuild) keep their READMEs minimal and **route sponsorship entirely externally** — no sponsor section in the README at all, just a single link to an external sponsor page. This is a legitimate pattern, not a failure:

- Use it when your README is a reference document that contributors read often, and you want zero commercial noise in it.
- The trade-off: you lose the free top-of-funnel visibility a bottom grid gives. Make up for it with a prominent `Sponsor` button (via `.github/FUNDING.yml`) and a well-trafficked external page.

---

## 14. `.github/FUNDING.yml` (the CTA target)

Every surface above should funnel to a single machine-readable CTA: `.github/FUNDING.yml`, which renders the GitHub "Sponsor" button. Current 12 supported keys: `community_bridge, github` (single user OR array up to 4), `issuehunt, ko_fi, liberapay, open_collective, patreon, tidelift` (format `PLATFORM/PACKAGE`; platforms: npm, pypi, rubygems, maven, packagist, nuget), `polar, buy_me_a_coffee, thanks_dev` (value `u/gh/USERNAME`), `custom` (single URL OR array up to 4; any URL containing a colon MUST be wrapped in quotes).

**Not supported** (do not list as supported): `otechie, givebutter, lfx_crowdfunding`. See [`../data/platforms.yml`](../data/platforms.yml).

---

## 15. README monetization checklist

- [ ] Bottom `## Sponsors` section renders a **dynamic** logo grid from an endpoint (no manual README edits).
- [ ] Tier labels live on `project.tld/sponsors`, not duplicated in the README.
- [ ] Top banner reserved for one platinum/title sponsor, minimal markup.
- [ ] Text list / `BACKERS.md` for the long tail of small backers.
- [ ] `.github/FUNDING.yml` committed with the right keys (12 supported).
- [ ] Docs site ad via EthicalAds/Carbon — one unit, above the fold, traffic-priced.
- [ ] Release-note sponsor aligned to version moments; disclosed as paid.
- [ ] Issue/PR template footer is one subtle line max.
- [ ] CLI startup sponsor is **opt-in/silent, never blocks or slows startup.**
- [ ] Newsletter only if sustained; primary/secondary/classified tiers.
- [ ] Community channel sponsor bundled, not standalone.
- [ ] Decided explicitly: README-sponsor vs no-README-sponsor pattern.

See also: [`../templates/readme-sponsor-block.md`](../templates/readme-sponsor-block.md) (markup), [pricing.md](pricing.md) (slot prices), [sponsor-kit.md](sponsor-kit.md) (the page the sponsors link points to), [faq.md](faq.md).
