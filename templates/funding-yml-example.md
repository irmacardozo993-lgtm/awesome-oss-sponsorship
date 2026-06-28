# `.github/FUNDING.yml` — annotated examples

> The `.github/FUNDING.yml` file renders the **Sponsor** button on your GitHub repo page. Docs: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/displaying-a-sponsor-button-in-your-repository
> Each key maps to one platform. GitHub renders a button per key; the button deep-links into that platform's profile for you or your project. Platform status/fees: [data/platforms.yml](../data/platforms.yml).

## The 12 current keys (verified 2026-06-29)

| Key | Value format | Notes |
|---|---|---|
| `github` | single username `"foo"` **OR** array up to 4 `["a","b","c","d"]` | GitHub Sponsors. 0% fee personal / up to 6% org. Mainland China NOT supported (HK/Macau SAR are). |
| `open_collective` | collective slug `"my-collective"` | Fiscal host, transparent public ledger. |
| `polar` | username `"foo"` | **Pivoted to AI billing / Merchant-of-Record** — no longer OSS sponsorship. Only relevant if your OSS project ships a paid SaaS/AI product. See [data/platforms.yml](../data/platforms.yml). |
| `buy_me_a_coffee` | username `"foo"` | 5% platform fee + Stripe processing. No PayPal. |
| `ko_fi` | username `"foo"` | **UNVERIFIED** (site returns 403 to fetchers). Reportedly 0% on one-time donations; confirm current numbers in a browser at ko-fi.com/pricing. |
| `patreon` | username `"foo"` | Flat 10% platform fee. |
| `issuehunt` | username `"foo"` | Point readers at **oss.issuehunt.io** (OSS, ©2019, stale), NOT issuehunt.io (now a cybersecurity bug-bounty platform). |
| `tidelift` | `"PLATFORM/PACKAGE"` | **Acquired by Sonar (Dec 2024)**; tidelift.com redirects to sonarsource.com. Historical. Platforms: `npm`, `pypi`, `rubygems`, `maven`, `packagist`, `nuget`. |
| `thanks_dev` | `"u/gh/USERNAME"` | 5% commission. Dependency-tree auto-funding (manifests → tree up to 3 levels deep). |
| `liberapay` | username `"foo"` | Donation platform. |
| `community_bridge` | `"PROJECT-NAME"` | **LFX Mentorship** (formerly CommunityBridge). |
| `custom` | single URL `"https://…"` **OR** array up to 4 `["https://a","https://b","https://c","https://d"]` | Any URL. |

### Rules & limits

- **Max 4 usernames** in the `github` array; **max 4 URLs** in the `custom` array. Beyond that GitHub ignores extras.
- **Colon → quotes rule:** any value containing a colon (i.e. any URL — they all contain `://`) **MUST be wrapped in quotes**. YAML otherwise parses `https://x` as a mapping. Quote every URL value.
- `tidelift` uses a **slash** (`npm/my-package`), not a colon — no quoting required, but harmless if quoted.
- `thanks_dev` uses the form **`u/gh/USERNAME`** (slashes, no colon) — quoting optional but harmless.

### NOT in the current official reference (do not list as supported)

- `otechie`
- `givebutter`
- `lfx_crowdfunding`

(`community_bridge` IS supported — it is the LFX Mentorship key, distinct from the unsupported `lfx_crowdfunding`. Do not confuse the two.)

---

## Example 1 — solo maintainer

A single developer who wants 0% fees on GitHub Sponsors plus a one-off tip jar and a custom sponsor page.

```yaml
# .github/FUNDING.yml — solo maintainer
github: your-username
buy_me_a_coffee: your-username
custom: "https://your-site.example.com/sponsor"
```

---

## Example 2 — project collective

A multi-maintainer project that routes company sponsors through Open Collective (501(c)(6) via Open Source Collective for invoices/tax-deductibility) and individuals through GitHub Sponsors. A custom URL points at the project's own sponsor page.

```yaml
# .github/FUNDING.yml — project collective
github: ["maintainer-one", "maintainer-two"]
open_collective: my-project
custom: "https://my-project.example.com/sponsors"
```

> Use the `github` **array** only when multiple maintainers each have their own GitHub Sponsors profile and you want a button per maintainer. For a single project profile, use a single string.

---

## Example 3 — maxed-out multi-platform

Every supported key in use, including the array limits (4 `github` usernames, 4 `custom` URLs) and the colon-quoting rule applied to every URL. **Do not ship all 12 buttons in production** — too many buttons dilute the CTA. This file exists to document every key plus the array/quote limits.

```yaml
# .github/FUNDING.yml — maxed-out multi-platform (reference, not a recommendation)
github: ["maintainer-one", "maintainer-two", "maintainer-three", "maintainer-four"]
open_collective: my-project
polar: your-username                 # pivoted to AI billing/MoR — see data/platforms.yml
buy_me_a_coffee: your-username
ko_fi: your-username                 # UNVERIFIED (403) — confirm pricing in a browser
patreon: your-username
issuehunt: your-username             # OSS subdomain oss.issuehunt.io; canonical domain is now cybersecurity
tidelift: npm/your-package           # acquired by Sonar Dec 2024 — historical
thanks_dev: "u/gh/your-username"     # u/gh/ form; quoted for consistency (no colon, so optional)
liberapay: your-username
community_bridge: your-project-name  # LFX Mentorship (NOT lfx_crowdfunding, which is unsupported)
custom: ["https://your-site.example.com/sponsor", "https://your-site.example.com/partners", "https://your-site.example.com/enterprise", "https://your-site.example.com/media-kit"]
```

Notes on the maxed file:

- Every URL in the `custom` array is quoted (colon rule).
- `tidelift: npm/your-package` is slash-separated, not quoted (no colon).
- `thanks_dev` shown quoted for consistency; it has no colon so quoting is optional under the colon rule.
- `community_bridge` is the supported LFX Mentorship key; `lfx_crowdfunding` is NOT supported and is omitted.
- Pick 2–4 keys that match your audience (see [data/platforms.yml](../data/platforms.yml)) rather than shipping all 12.

---

## Self-check

- [ ] Only keys from the 12 current keys above are present.
- [ ] No `otechie`, `givebutter`, or `lfx_crowdfunding`.
- [ ] `github` array has ≤ 4 entries; `custom` array has ≤ 4 entries.
- [ ] Every value containing a colon is quoted (every URL, every `https://` value).
- [ ] `tidelift` uses `PLATFORM/PACKAGE` with a slash; `thanks_dev` uses `u/gh/USERNAME`.
- [ ] `issuehunt` resolves to the OSS product — you point readers at oss.issuehunt.io, not issuehunt.io.
