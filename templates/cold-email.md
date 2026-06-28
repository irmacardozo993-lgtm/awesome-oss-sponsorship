# Cold Email Templates — OSS Sponsorship Outreach

Peer-to-peer emails to devtool companies that already use or overlap with your
project. The goal of the **first** email is always a single ask: a 15-minute
call, or "is sponsorship worth exploring?" Never quote a price as a quote in
the opening email — anchor to a rate card only as "estimate / reference only"
and let the call do the pricing.

## How to use

1. **Personalize or don't send.** Replace every `[bracket]` field. The line
   that references *their* product must be specific (a feature, a recent post,
   a release) — a generic compliment reads as spam and gets flagged.
2. **One ask per email.** Cold email that asks for a call *and* a logo *and* a
   retainer gets ignored. First email = call only.
3. **Sequence, don't blast.** Send the opener, then Follow-up #1 after 3–4
   business days, then Follow-up #2 after 7–10 days, then the close-out.
   Stop after the close-out. Three touches with no reply = move on.
4. **All prices are estimates.** If you mention a number, label it
   "estimate / reference only" and point to the full [rate card](rate-card.md).
5. **For LinkedIn / X / 微信 / Discord**, use the short-form templates in
   [dm-template.md](dm-template.md) — those channels punish long copy.
6. **Audit your deliverability.** Cold email that lands in spam does nothing.
   Use a warmed sending domain, set SPF/DKIM/DMARC, and keep the first email
   under ~150 words with no attachments and no tracking pixel.

> Pricing reference for slot tiers (all **estimate / reference only**, not a
> quote): see [rate-card.md](rate-card.md). Ground rules and verified case
> studies: [../docs/case-studies.md](../docs/case-studies.md). Platform data:
> [../data/platforms.yml](../data/platforms.yml).

---

## 1. English cold email — devtool company (peer-to-peer)

**Subject:** [their-product] + [your-repo] — a sponsorship worth 15 minutes?

> Hi [first-name],
>
> I maintain [your-repo] ([your-repo-url]) — [one-line what it does], with
> [star-count] GitHub stars and ~[monthly-visitors-or-downloads] monthly
> [visitors / npm downloads / Docker pulls].
>
> I'm reaching out because [their-product] shows up in how people use
> [your-repo] — specifically, [one concrete overlap: e.g. "your CLI is the
> default in our quickstart" / "teams running [your-repo] on [their-cloud]
> are our fastest-growing segment" / "you shipped [feature] last month, which
> unblocks the [x] use case we get asked about most"].
>
> That overlap is exactly what a README/docs sponsorship is designed to reach:
> developers at the moment they're choosing tooling. I keep a rate card
> (estimate / reference only — [rate-card-link] or [../templates/rate-card.md])
> and would rather walk you through it live than dump numbers here.
>
> One ask: **a 15-minute call** to see if sponsorship is worth exploring for
> [their-company]. If it's not a fit, I'll say so on the call — no hard sell.
>
> If easier, here's my calendar: [scheduling-link]. Otherwise just reply.
>
> Thanks for [their-product]. We use it for [specific thing you actually use].
>
> — [your-name]
> [your-title / maintainer of your-repo]
> [your-email] · [your-github]

---

## 2. Chinese cold email — 开发者工具公司（中文，正式得体）

**Subject（主题）:** [their-product] 与 [your-repo] —— 是否值得聊一次赞助合作？

> [first-name] 您好，
>
> 我是 [your-repo]（[your-repo-url]）的维护者，[一句话说明项目用途]，
> 目前 GitHub [star-count] stars，月均 [月访问量 / npm 下载量 / Docker 拉取量]。
>
> 之所以联系贵司，是因为在 [your-repo] 的使用场景里，[their-product]
> 经常出现——具体来说，[一处具体的交集：例如"我们的快速上手文档默认接你们的 CLI"／
> "在 [their-cloud] 上跑 [your-repo] 的团队是我们增长最快的用户群"／
> "贵司上月发布的 [feature] 正好打通了我们被问得最多的 [x] 场景"]。
>
> 这种交集正是 README / 文档站赞助投放的价值点：在开发者选型当下触达他们。
> 我有一份报价参考表（**仅供参考，非正式报价**——见 [rate-card-link] 或
> [../templates/rate-card.md]），更希望在电话里当面过一遍，而非直接丢数字。
>
> 一个请求：**能否约 15 分钟通话**，看看赞助合作对 [their-company] 是否值得推进。
> 若确实不合适，我会在电话里直说，不会强推。
>
> 方便的话这是我的日历：[scheduling-link]；或者您直接回复即可。
>
> 感谢 [their-product]，我们在 [你确实在用的具体场景] 用到它。
>
> —— [your-name]
> [your-repo] 维护者
> [your-email] · [your-github]

---

## 3. Follow-up #1 — 3–4 business days later (same thread, brief)

**Subject:** re: [their-product] + [your-repo] — a sponsorship worth 15 minutes?

> Hi [first-name],
>
> Bumping this in case it slipped past — I know DevRel/growth inboxes are loud.
>
> Short version: [your-repo] reaches [star-count] stars and ~[monthly-metric]
> monthly [visitors / downloads] at exactly the tool-selection moment, and
> [their-product] is already in that workflow. I'm asking for **15 minutes** to
> see if a README/docs sponsorship makes sense. No deck, no prep on your side.
>
> Calendar: [scheduling-link]. Or reply with a time that works.
>
> — [your-name]

> **中文版（同一邮件线程，简短）：**
>
> [first-name] 您好，
> 怕邮件被淹没，再跟进一次。简短说：[your-repo] 有 [star-count] stars、月均
> [monthly-metric] [访问量／下载量]，覆盖的正是开发者选型当下，而 [their-product]
> 已在这条工作流里。想约 **15 分钟**看看 README／文档站赞助是否合适，无需您准备。
> 日历：[scheduling-link]；或回复您方便的时间。
> —— [your-name]

---

## 4. Follow-up #2 — 7–10 days later (different angle: discounted first-month test)

**Subject:** [their-product] × [your-repo] — try one month, on a discount?

> Hi [first-name],
>
> Last note from me on this. Instead of asking you to commit to a call cold,
> here's a lower-risk path: a **one-month test slot** on the [README top banner
> / docs sidebar] at roughly [discounted-rate] (estimate / reference only —
> that's about [X]% under the standard monthly anchor in my
> [rate card](rate-card.md)). You'd get logo placement + a release-note mention
> for the [upcoming-version] release on [release-date], and we both find out
> if the audience converts before either of us signs anything longer.
>
> If that's interesting, I can have the slot live within [N] days of a yes.
> If it's not, no problem — I'll stop here and won't keep pinging.
>
> — [your-name]

> **Notes on the discount:** Offer ~15–25% off the **monthly** anchor for a
> single test month (this is *not* the annual 12-month deal, which is 8–10×
> monthly with 15–20% off — see [rate-card.md](rate-card.md)). Frame the test
> month as "we both learn whether the audience converts" so the discount reads
> as a trial, not desperation.

---

## 5. Reply when sponsor says YES — next steps

**Subject:** Great — here's how we get [their-company] live on [your-repo]

> Hi [first-name],
>
> Excellent — let's get it done. Here's the sequence so nothing stalls:
>
> | Step | What I need from you | When |
> |------|----------------------|------|
> | 1. Confirm slot & dates | Which slot ([README top banner / bottom logo / docs ad / release note]) and start/end dates | Now |
> | 2. Logo + link | SVG/PNG logo (transparent, ≤[width]px wide) + target URL + alt text | Within [N] days |
> | 3. Invoice / payment | I'll send an invoice via [GitHub Sponsors / Open Collective / direct] — confirm billing contact + PO number if needed | Within [N] days |
> | 4. Go-live | I push the logo to the sponsors endpoint; you verify the live render | On start date |
> | 5. Report | I send a post-slot traffic/engagement snapshot ([note: GitHub Traffic is admin-only, 14-day rolling, self-reported — see media kit](media-kit.md)) | End of slot |
>
> A few specifics:
> - **Slot type:** you said [slot] — confirmed at [monthly-rate] (estimate / reference only; final in the invoice).
> - **Billing:** via [platform — e.g. GitHub Sponsors 0% personal / up to 6% org; Open Collective fiscal host]. Bank/region and tax (W-8BEN for non-US) handled at the platform.
> - **Logo render:** the README renders a **dynamically-generated logo grid** from a sponsors endpoint, so you never need me to edit the README manually — I just add your entry to the JSON. (This is the Vue/Vite/Astro pattern.)
>
> Reply with the slot + dates and the logo and I'll have the invoice out today.
>
> — [your-name]

---

## 6. Reply when sponsor says NO — keep the door open

**Subject:** re: [their-product] × [your-repo] — thanks, and one ask

> Hi [first-name],
>
> Totally understand — timing and budgets shift, and [their-product] being in
> the workflow doesn't mean sponsorship is the right lever right now. Thanks
> for the straight answer.
>
> Two small things, then I'll close out:
>
> 1. **Feedback (optional, 30 seconds):** was it budget, audience fit, slot
>    type, or just "not now"? It genuinely helps me price the next slot right —
>    no need to be diplomatic.
> 2. **Affiliate option (no upfront cost):** if a paid slot is off the table
>    but you'd still pay for *converted* users, I'm open to a
>    **fixed + affiliate hybrid** — a small retainer + commission on signups
>    attributable to the README/docs placement (estimate: 10–30% recurring or
>    $5–$50 flat per converted user, volume-dependent — see
>    [rate-card.md](rate-card.md)). Zero risk if nothing converts.
>
> Either way, the door stays open. If Q[next-quarter] looks different, my
> [rate card](rate-card.md) and calendar ([scheduling-link]) don't move.
>
> — [your-name]

---

## 7. Close-out — after 3 touches with no reply

**Subject:** closing the loop on [your-repo] sponsorship

> Hi [first-name],
>
> I've sent a couple of notes and don't want to clutter your inbox, so this is
> my last one on this thread. If [their-product] × [your-repo] sponsorship
> becomes interesting later — different quarter, a launch, a DevRel campaign —
> my [rate card](rate-card.md) (estimate / reference only) and calendar
> ([scheduling-link]) are always live.
>
> Thanks again for [their-product]. Genuinely useful to us.
>
> — [your-name]

---

## Quick reference — sequence cadence

| Touch | When | Channel | Ask |
|-------|------|---------|-----|
| Opener (#1 or #2) | Day 0 | Email | 15-min call |
| Follow-up #1 | Day +3–4 (same thread) | Email | Re-state the 15-min ask |
| Follow-up #2 | Day +7–10 | Email | Discounted 1-month test slot |
| Close-out | Day +14–16 | Email | Door stays open, stop here |

> Stop after the close-out. Pestering a non-responder burns the relationship
> for the next time budgets open. Re-engage only with a genuine new trigger
> (their funding round, your major release, a mutual contact intro).
