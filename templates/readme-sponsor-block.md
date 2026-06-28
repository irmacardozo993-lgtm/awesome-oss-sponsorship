# README sponsor blocks — copy-paste snippets

> Snippets for rendering sponsor logos/text inside a README. Pair with [sponsor-kit.md](sponsor-kit.md) (the kit you send sponsors) and [funding-yml-example.md](funding-yml-example.md) (the Sponsor button).
> Slot values/taxonomy: [data/sponsor-types.yml](../data/sponsor-types.yml).

## Why dynamic, not hand-edited

The dominant real-repo pattern (Vue, Vite, Astro, Homebrew) is a **bottom "## Sponsors" section rendering a remotely-hosted SVG/PNG logo grid**, generated from a sponsors endpoint/JSON so the README never needs editing when a sponsor joins or leaves. Tier labels (Diamond/Platinum/Gold) are **rare inside READMEs** — they live on an external sponsor page; the README just renders the grid. Add a sponsor = append one row to `sponsors.json` and republish the SVG; the README is untouched.

---

## 1. README TOP sponsor block (above the fold, 1–2 logos)

Highest-visibility real estate. One or two premium logos max. Put it right under the title/badges, before the description.

```md
<a href="https://[sponsor-url]"><img align="right" src="https://[cdn]/logos/[sponsor].svg" width="220" alt="[Sponsor Name]"></a>

# [project-name]

> [one-line description]

Sponsored by <a href="https://[sponsor-url]">[Sponsor Name]</a>.
```

For two logos side by side:

```md
<p align="center">
  <a href="https://[sponsor-a-url]"><img src="https://[cdn]/logos/[sponsor-a].svg" width="200" alt="[Sponsor A]"></a>
  &nbsp;
  <a href="https://[sponsor-b-url]"><img src="https://[cdn]/logos/[sponsor-b].svg" width="200" alt="[Sponsor B]"></a>
</p>

# [project-name]
```

---

## 2. README BOTTOM sponsor block — dynamic SVG logo grid (recommended)

The dominant pattern. The README renders a single `<img>` pointing at a generated SVG; **adding a sponsor never touches the README**.

### 2a. Render the grid from an endpoint

```md
## Sponsors

Is your company using [project-name]? Help keep it healthy by [becoming a sponsor](https://[project].tld/sponsors).

<p align="center">
  <a href="https://[project].tld/sponsors"><img src="https://[project].tld/sponsors.svg" alt="Sponsors" /></a>
</p>
```

The `sponsors.svg` endpoint reads `sponsors.json` and renders a grid. A minimal `sponsors.json`:

```json
{
  "gold": [
    { "name": "Sponsor One", "url": "https://sponsor-one.example.com", "img": "https://cdn.example.com/sponsor-one.svg" }
  ],
  "silver": [
    { "name": "Sponsor Two", "url": "https://sponsor-two.example.com", "img": "https://cdn.example.com/sponsor-two.svg" }
  ],
  "bronze": [
    { "name": "Backer Three", "url": "https://backer-three.example.com", "img": "https://cdn.example.com/backer-three.svg" }
  ]
}
```

### 2b. Generated SVG (serverless, cache-busted)

If you don't run a server, generate the SVG in CI from `sponsors.json` and publish it to a CDN. Append a version or content hash to the `src` so GitHub's image cache invalidates on change:

```md
<p align="center">
  <a href="https://[project].tld/sponsors">
    <img src="https://[cdn]/sponsors.svg?v=2026-06" alt="Sponsors" />
  </a>
</p>
```

A tiny SVG layout sketch (single row, three logos) — adapt the width/height to your count:

```html
<svg xmlns="http://www.w3.org/2000/svg" width="640" height="120">
  <a href="https://sponsor-one.example.com"><image href="https://cdn.example.com/sponsor-one.svg" x="40"  y="20" width="160" height="60"/></a>
  <a href="https://sponsor-two.example.com"><image href="https://cdn.example.com/sponsor-two.svg" x="220" y="20" width="160" height="60"/></a>
  <a href="https://backer-three.example.com"><image href="https://cdn.example.com/backer-three.svg" x="400" y="20" width="160" height="60"/></a>
</svg>
```

> GitHub renders `<svg>` containing `<image>` and `<a>` in READMEs; strip scripts/foreignObjects. For dark mode, ship a second variant and switch via `<picture>` + `media` if your README supports themes.

---

## 3. Text-only BACKERS.md-style list

Cheapest slot — name + link. Good for individuals and small backers. Maintain as a separate `BACKERS.md` (the Vue pattern) or as a section in the README.

```md
## Backers

Thank you to all our backers! [Become a backer](https://[project].tld/sponsors).

**Gold**
- [Sponsor One](https://sponsor-one.example.com)
- [Sponsor Two](https://sponsor-two.example.com)

**Silver**
- [Backer Three](https://backer-three.example.com)

**Bronze**
- Jane Doe
- @githubuser
```

For a fully dynamic text list (no manual edits), generate `BACKERS.md` from the same `sponsors.json` in CI — one data source feeds both the SVG grid and the text list.

---

## 4. Logo sponsor example with tier labels

When you do label tiers in the README (less common — usually they live on the sponsor page), group logos by tier with descending widths:

```md
## Sponsors

### Platinum

<p align="center">
  <a href="https://[sponsor-url]"><img src="https://[cdn]/logos/[sponsor].svg" width="260" alt="[Sponsor]"></a>
</p>

### Gold

<p align="center">
  <a href="https://[sponsor-a-url]"><img src="https://[cdn]/logos/[sponsor-a].svg" width="180" alt="[Sponsor A]"></a>
  &nbsp;
  <a href="https://[sponsor-b-url]"><img src="https://[cdn]/logos/[sponsor-b].svg" width="180" alt="[Sponsor B]"></a>
</p>

### Silver

<p align="center">
  <a href="https://[sponsor-c-url]"><img src="https://[cdn]/logos/[sponsor-c].svg" width="140" alt="[Sponsor C]"></a>
</p>
```

---

## 5. Affiliate disclosure snippet

Required wherever affiliate/referral links are used (FTC and most platform policies). Track these deals in [affiliate-tracker.csv](affiliate-tracker.csv).

Block disclosure for a page/site that contains affiliate links:

```md
> **Affiliate disclosure:** Some links on this page are affiliate/referral links. If you sign up through them, [project-name] may earn a commission at no extra cost to you. This helps fund development. We only link products we use or would recommend regardless.
```

Inline disclosure on a single affiliate link:

```md
We recommend [Service X](https://[service].example.com/?ref=[project]) *(affiliate link — we earn a commission if you sign up)*.
```

---

## Alternative: the "no-README-sponsor" pattern

2 of 6 sampled real repos (Tailwind CSS, esbuild) keep their READMEs minimal and **route sponsorship entirely externally** — a single line or the `.github/FUNDING.yml` Sponsor button points to `tailwindcss.com/sponsor` or a personal page; no logo grid, no BACKERS list in the repo. This is a legitimate pattern when:

- You want total control of sponsor presentation on your own site.
- Your README is a concise quickstart and you don't want it to grow.
- Sponsors are sold via direct relationships, not inbound README traffic.

If you take this route, still ship `.github/FUNDING.yml` (see [funding-yml-example.md](funding-yml-example.md)) so the GitHub "Sponsor" button works, and put your rate card on the external page.
