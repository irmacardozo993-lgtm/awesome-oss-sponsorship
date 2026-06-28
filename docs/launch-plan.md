# Cold-Start Distribution Plan

How to launch a new OSS project from zero stars to its first real audience. This is a channel-by-channel, anti-spam playbook — each section covers the rules that get you heard and the mistakes that get you flagged. Sponsorship only works once there are people to sponsor; this file builds that audience. See [the 1000-stars playbook](1000-stars-playbook.md) for what to do once stars arrive, and [case studies](case-studies.md) for where this can lead.

> Anti-spam is the throughline: post once per channel, lead with substance, never cross-post identical copy. A flagged launch is worse than no launch — it burns the channel for your next project.

---

## 1. How to publish on GitHub (the foundation)

Before any external channel, the repo itself must convert a curious click into a star, a clone, and eventually a sponsor. Three surfaces do the work:

- **Repo description** — the one line under the repo name in listings and search. See [section 2](#2-repo-description-formula).
- **Topics** — the tagged keywords that make the repo discoverable in GitHub search. See [section 3](#3-topics-design).
- **README** — the landing page. It must answer, in the first screen (above the fold): what this is, what problem it solves, how to install it in one command, and a minimal usage example. Badges (build status, version, license) at the top; a `## Sponsors` section at the bottom once you have sponsors (per [playbook §5](1000-stars-playbook.md#5-how-to-package-the-repo)).

**Publish checklist:**

- [ ] LICENSE present (choose an OSI-approved license — MIT/Apache-2.0 for permissive, GPL for copyleft)
- [ ] README answers what/why/install/example above the fold
- [ ] `.github/FUNDING.yml` present (the sponsor button appears even before you have sponsors — see [playbook §5.1](1000-stars-playbook.md))
- [ ] Repo description set (not blank)
- [ ] 5–20 topics applied
- [ ] First release tagged (a GitHub Release gives you a permalink and a "what's new" surface)
- [ ] Issues + Discussions enabled; a CONTRIBUTING.md exists
- [ ] Screenshots/asciinema/GIF in the README for anything visual

A repo with no description, no topics, and a one-line README will not convert traffic from any channel below. Fix this first.

---

## 2. Repo description formula

The description is 350 chars max but the first ~80 show in search results. Optimize for the snippet, not the full length.

**Formula:** `[What it is] — [the problem it solves / differentiator]. [Language/ecosystem].`

Examples (illustrative, swap in your real project):

- `A fast static site generator — builds 1000 pages in under 5s. Go.`
- `Drop-in Redis alternative for local dev — no server, no config. Rust.`

**Rules:**

- Lead with the noun (what it is), not an adjective ("A fast…" beats "Fast and modern…").
- Include the concrete payoff or differentiator in the first clause.
- Name the language/ecosystem at the end so ecosystem-specific searches find you.
- No emoji pileups, no marketing adjectives ("blazing", "ultimate", "revolutionary").
- No version numbers or status flags that will go stale.

**Anti-pattern:** `A modern, lightweight, blazing-fast tool built with love 💜` — says nothing, stales fast, reads as spam to HN/Reddit moderators.

---

## 3. Topics design

Topics are the GitHub-side discovery engine. You get up to 20.

**Selection strategy:**

- 2–3 **ecosystem/language topics** (`rust`, `python`, `go`, `typescript`).
- 3–5 **category topics** (`cli`, `static-site-generator`, `developer-tools`, `self-hosted`).
- 2–3 **specific-technology topics** that adjacent users search (`redis`, `webpack`, `kubernetes`).
- 1–2 **use-case topics** (`homelab`, `devex`).
- Your **project name** as a topic (so forks/dependents can tag it).

**Rules:**

- Prefer topics that GitHub suggests (they have existing pages with aggregated activity). A topic with its own `/topics/[x]` page is worth more than a one-off tag.
- Do not stuff 20 near-duplicates (`tool`, `tools`, `utility`, `utilities`) — it looks spammy and does not help search.
- Do not use competitor names as topics (will be flagged).

---

## 4. Hacker News (Show HN)

Show HN is the highest-leverage English-language launch for developer tools, but it has strict norms and a single shot.

**Show HN rules that matter:**

- Title must start with `Show HN:` (the site enforces this).
- Title = the project name + a one-line description. No clickbait, no questions, no "I built a…". Example: `Show HN: [Name] – [what it does]`.
- Link to the repo/project URL, not a blog post (blog post is allowed but repo is preferred for Show HN).
- **The maker must post the first comment** explaining the backstory: why you built it, what's different, what you want feedback on. This is the "maker comment" and it is expected.
- Respond to every comment for the first few hours. Engagement in the first hour heavily affects ranking.

**Title:** `Show HN: [Name] – [concrete payoff]`. Keep under 80 chars.

**Timing:** post Tuesday–Thursday, 06:00–09:00 US Pacific (13:00–16:00 UTC) to catch the US morning browse. Avoid weekends and major news cycles. Submit once — reposting a dead Show HN is frowned upon.

**Anti-spam:**

- Do not ask friends to upvote (HN detects vote rings and kills the submission).
- Do not cross-post to Reddit the same hour — split by a day so each post gets your full attention for replies.
- If it flops, do not repost. Move on; HN remembers.

---

## 5. Reddit

Reddit is channel-sensitive — each subreddit has its own rules and culture. Spamming the same link across subs gets you banned site-wide.

**Subreddits and their norms:**

| Subreddit | Fits | Rules to respect |
|---|---|---|
| r/programming | Broad dev audience | No direct link-only posts; write a text post explaining the project. No promotion of commercial products. |
| r/devops | Infra/ops tooling | Text post, lead with the problem solved. Tolerates self-promo if substantive. |
| r/selfhosted | Self-hostable apps | Direct link OK if it's genuinely self-hostable. Discloses self-promo in the title or comments. |
| r/[language] (r/rust, r/python…) | Ecosystem-specific | Check each sub's wiki — most have a "Show and Tell" monthly thread where self-promo belongs instead of the main feed. |

**Rules across all:**

- Read each subreddit's rules and wiki before posting. Many require a text post, not a link.
- Disclose your relationship in the first line ("I'm the author").
- Lead with the problem and the substance, not "check out my project."
- Be an existing community member first — an account that only posts its own launches reads as spam. Comment on others' posts in the weeks before.
- One subreddit at a time, days apart, each with rewritten copy tailored to that audience.

**Anti-spam:** never paste the same title/body into multiple subs. Never use vote-begging. If a mod removes it, message them politely — do not repost.

---

## 6. Product Hunt

Product Hunt fits developer tools with a polished landing page or demo. Less fit for raw libraries without a UI.

**Mechanics:**

- Launch as a "Maker" (you are the builder). Pre-register the product in advance.
- **The maker comment is mandatory** — post it in the first hour explaining why you built it and what's next.
- Line up support in advance (tell your network the launch is coming, but do not beg for upvotes on the platform — PH's algorithm demotes coordinated voting).

**Timing:** launch Tuesday–Thursday, 00:01 US Pacific (PH's day rolls over then). Monday is crowded, Friday–Sunday is weak. Avoid launching the same day as a major product (Apple event, big tech launch) — you'll be buried.

**Copy:** a tagline (one line), a description, a gallery (screenshots/GIF), and a short demo video if you can make one. The tagline carries most of the weight — make it a concrete payoff, not a vibe.

**Anti-spam:** one launch per product (relaunches only for major 2.0 versions). Do not create multiple listings.

---

## 7. V2EX (Chinese dev forum)

V2EX is a Chinese developer community with strict node etiquette. The choice of node (节点选择) determines whether the post is seen or deleted.

**Node selection (节点选择):**

- Post in the node that matches the project's nature: `分享创造` (Show & Tell / creations) is the standard node for self-promoted projects; `程序员` for general dev discussion; a language-specific node if the community gathers there.
- Do **not** post a project link in a discussion node (e.g., `问与答` Q&A) — it will be flagged as misplaced.

**Anti-promotion rules (反软文):**

- V2EX culture is hostile to anything that reads as a sponsored post or ad copy (软文). Write like a developer sharing a side project, not a marketer.
- Disclose that you are the author.
- Lead with the technical problem and how you solved it; the project is the evidence, not the pitch.
- No marketing language, no emoji marketing, no "best/faster/revolutionary."
- Engage genuinely in the replies.

**Anti-spam:** post once, in one node. Cross-posting to multiple nodes is treated as spam and removed.

---

## 8. Juejin / Zhihu / WeChat Official Account (Chinese content channels)

These three reward technical depth (技术深度), not clickbait (非标题党). The model is a long-form technical article that happens to introduce your project, not a launch announcement.

**Juejin (掘金):** a developer article platform. Write a deep technical piece — e.g., "How we made X 10× faster" or "Building a [category] tool from scratch" — that uses your project as the running example. Depth and runnable code win. Avoid listicle/标题党 titles ("10 amazing tools…"); the algorithm and readers both penalize them.

**Zhihu (知乎):** a Q&A + long-form platform. The highest-converting entry is answering an existing question your project solves ("如何 [problem]?") with a substantive answer that references your tool as one solution. Self-authored questions read as spam. Long-form technical columns (专栏) work if the substance is real.

**WeChat Official Account (公众号):** a long-form article channel for a subscriber audience. Effective only if you already have a following or get reposted by a dev-focused account. The article must be technically substantive — a reworded launch tweet will be ignored or, worse, flagged. Lead with a real engineering story.

**Cross-cutting rules (非标题党):**

- Title states the technical content, not a teaser. "实现一个 [X] 的几个工程取舍" beats "你绝对想不到的 [X]".
- Each platform gets a separately written piece, not copy-paste — the audiences and formats differ.
- Disclose authorship; the project link goes in the article body or author bio, not the title.

**Anti-spam:** one piece per platform, spaced days apart. Do not mass-submit the same article to all three on the same day.

---

## 9. Twitter / X thread structure

A thread is the highest-effort, highest-leverage English social format for dev tools. Structure it as a story, not a brochure.

**Thread structure (proven shape):**

1. **Hook tweet (1):** the problem, stated sharply. No "🧵 1/" preamble before the actual content — lead with the insight. Example framing: "[Problem] is harder than it should be. So I built [Name]."
2. **The pain (2–3):** concrete examples of the problem, with code or screenshots. Make it recognizable to someone who has felt it.
3. **The solution (4–6):** how your project solves it, with a minimal install + usage snippet. One command to try.
4. **What's different (7):** the one technical decision that makes it work — this is the part technical readers retweet.
5. **Demo (8):** a GIF or screen recording of it working.
6. **Roadmap / ask (9):** what's next, and a soft ask — "stars help, contributors welcome, feedback wanted." Not a sponsor ask on launch day.
7. **Links (10):** repo URL, docs, your profile.

**Rules:**

- First tweet must stand alone (it's what gets shown). Put the hook before the "🧵".
- Code must be copy-pasteable; use screenshots only for output.
- Tag sparingly — one or two relevant accounts max, not a pile of @-mentions.
- Post in the US morning (13:00–16:00 UTC) for max dev attention.

**Anti-spam:** do not reply-bump your own thread repeatedly. Do not post the same thread multiple times. Do not tag the same big accounts asking for a retweet.

---

## 10. Awesome-list crosslinking

Awesome lists (the `sindresorhus/awesome` ecosystem and its spin-offs) are curated directories that drive durable, high-intent traffic — people searching "best [X] tool" land here for years.

**How to submit:**

- Find the awesome list for your category (`awesome-cli`, `awesome-selfhosted`, `awesome-rust`, etc.). Each has its own CONTRIBUTING.md with entry rules — read it.
- Submit a PR adding your project under the right sub-section, with the entry format the list requires (usually `- [Name] - [description].`).
- The description must follow the list's style (often imperative, no marketing words, no trailing period depending on the list).
- Have a real README and a real release before submitting — curators reject empty repos.

**Mutual links:**

- Link from your README to the awesome lists you're listed in (a "Featured in" or "Listed on" section) — this is legitimate cross-linking and helps SEO.
- Do not run a link farm: a handful of relevant listings, not 50 low-quality directories.

**Anti-spam:** submit to one list per PR. Do not open the same PR across 20 lists in a day — curators talk and you'll be seen as a spammer. If a maintainer rejects your entry, respect it; do not reopen.

---

## 11. How to get OSS authors to repost

A repost from a respected OSS author is worth more than any channel above — it carries their credibility to their audience.

**How to earn it (you cannot ask for it directly):**

- **Use their project, then contribute.** An author is far more likely to boost a tool made by someone who has contributed to or meaningfully depended on their work. Submit a real PR to their repo first.
- **Write about their tool, then yours.** A blog post comparing approaches that credits their project fairly — and happens to introduce yours — is shareable. Never write a hit piece disguised as a comparison.
- **Make a genuine integration.** A plugin/adapter for their ecosystem is a natural reason for them to mention you. ("[Their tool] now works with [your tool] via [adapter].")
- **DM only after a real relationship.** If you must reach out, lead with something useful to *them* (a bug report with a fix, a relevant user signal), and only then mention your launch as context. "Please retweet my project" cold-DMs get ignored and remembered.
- **Make it easy to share.** Provide a one-line description, a screenshot/GIF, and the repo URL in your DM — not a wall of text. Authors repost things they can describe in one sentence.

**Anti-spam:** do not mass-DM authors. Do not @-tag authors into your launch thread unsolicited. One thoughtful contact beats twenty cold asks.

---

## 12. How to sustain updates for organic star growth

The launch gets you a spike. Organic star growth comes from the months after — and it is what sponsors actually underwrite (a repo that is still growing is fundable; a dead repo is not).

**Sustain mechanics:**

- **Ship regular releases.** A predictable release cadence (even monthly) keeps the repo in GitHub's "recently updated" signals and gives you release notes to share (a [release-note sponsor slot](../data/sponsor-types.yml) only exists if you ship releases).
- **Triage issues and PRs in public, fast.** Responsiveness is the strongest signal a repo is alive. Contributors appear when they see PRs merged, not ignored.
- **Write one substantive piece per month** (blog post / Juejin / X thread) tied to a real feature or a hard problem you solved. This is the slow-compound traffic engine.
- **Keep the README current.** Update the install snippet, badges, and screenshots every release. A stale README kills conversion from all the channels above.
- **Watch your GitHub Traffic `popular/referrers`** (admin-only, 14-day — see [playbook §6](1000-stars-playbook.md#6-how-to-prepare-github-traffic-data)) to learn which channel actually sends users, then double down on that one and drop the rest.
- **Curate the contributor experience.** Good-first-issue labels, a CONTRIBUTING.md, and merged first-PRs turn stargazers into maintainers — and maintainers bring their networks.

**The compounding loop:** releases → content → new users → issues/PRs → responsiveness → contributor trust → more users. Each turn adds stars that are real (installed, engaged), not vanity. That is the audience a sponsor will pay to reach.

**Anti-spam (long-term):** do not re-announce the same project on the same channel every month. Newsworthy updates (a 1.0, a major feature, a performance milestone) earn a post; routine patch releases do not. Re-announcing the same thing trains audiences to ignore you.

---

Related: [1000-stars playbook](1000-stars-playbook.md), [case studies](case-studies.md), [platforms](../data/platforms.yml), [sponsor taxonomy](../data/sponsor-types.yml).
