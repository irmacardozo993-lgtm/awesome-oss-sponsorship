# Outreach campaign checklist

A copy-paste tracker for sponsorship outbound. Score every prospect with [../tools/sponsor-fit-score.md](../tools/sponsor-fit-score.md), log them here, and run the cadence below. This is the engine behind the [first-50-DMs plan](../examples/1000-stars-repo.md#5-the-first-50-dms-plan).

All prices you put in the `revenue` column are **estimate / reference only** until a deal is signed — never log an estimate as booked revenue.

---

## The two rules

### 1. The 50-prospect cadence rule

- Maintain a **rolling list of 50 scored prospects** at all times. The "first 50" is your kickoff batch; after that, replenish as you close prospects out.
- Send in **waves of ~10**, not all at once. After each wave, adapt the pitch (subject line, price, slot) based on what got replies.
- **Never contact more than 50 simultaneously.** Beyond ~50 your replies slip, follow-ups go cold, and you start sending low-effort messages that damage your reputation. Capacity and reputation are the real limits, not list size.
- Only pursue prospects scoring **61–100** (Pursue / Priority). Park **31–60** (Maybe) for later; **0–30** (Skip) never gets messaged.

### 2. The 3-touch-then-close rule

Each prospect gets **exactly three touches**, then you close them out:

| Touch | When | Channel | Content |
|-------|------|---------|---------|
| Initial | Day 0 | Primary channel | Pitch: audience overlap + slot + low-end price + first-month discount. |
| Follow-up #1 | Day +4 | Same channel | One-line bump: "floating this back up — happy to do month one free." |
| Follow-up #2 | Day +9 | Same or alt channel | Final value-add: a real number (downloads/traffic) or a peer sponsor name. |

- After **3 touches with no positive reply**, set `status = closed_lost` and **stop.** Do not send a 4th unsolicited message — it burns reputation and rarely converts.
- Re-engage a `closed_lost` prospect **only if they come inbound** (they star the repo, reply later, or a mutual connection introduces them).
- A "positive reply" = anything that moves to a conversation (a question, a "send the kit", a calendar link). Advance `status` to `replied` and move off the cadence into a 1:1 sales thread.

---

## Markdown table template (copy-paste)

```markdown
| Prospect | Company | Role | Channel | Fit | Template | Sent | FU#1 | FU#2 | Status | Outcome | Revenue/mo |
|----------|---------|------|---------|-----|----------|------|------|------|--------|---------|------------|
| [name] | [company] | [role] | [email\|linkedin\|github_dm\|discord\|intro] | [0–100] | [template-id] | [YYYY-MM-DD] | [YYYY-MM-DD] | [YYYY-MM-DD] | [status] | [1-line] | [$0 until won] |
| Sam Lee | DevHost | Head of Growth | email | 70 | founding-sponsor-dm | 2026-07-01 | 2026-07-05 | 2026-07-10 | replied | sent kit, on call | $0 |
| … | … | … | … | … | … | … | … | … | … | … | … |
```

### Field reference

| Field | Values / format |
|-------|-----------------|
| Prospect | Real name or handle. |
| Company | Employer / brand paying. |
| Role | Head of Growth, DevRel, Founder, Staff Eng, etc. — aim for someone with budget or direct influence. |
| Channel | `email` · `linkedin` · `github_dm` · `discord` · `intro` (warm). |
| Fit | Sponsor Fit Score 0–100 (see [../tools/sponsor-fit-score.md](../tools/sponsor-fit-score.md)). |
| Template | Which DM you used: `founding-sponsor-dm`, `in-kind-credits-dm`, `gold-tier-pitch`, etc. (see [../examples/100-stars-repo.md](../examples/100-stars-repo.md) and [../examples/1000-stars-repo.md](../examples/1000-stars-repo.md)). |
| Sent / FU#1 / FU#2 | ISO dates `YYYY-MM-DD`. FU#1 = Sent +4 days; FU#2 = Sent +9 days. |
| Status | `not_started` · `sent` · `follow_up_1` · `follow_up_2` · `replied` · `closed_won` · `closed_lost` · `parked` |
| Outcome | One line: "sent kit, on call", "no reply after 3 touches", "signed Gold $500/mo", "budget frozen Q3". |
| Revenue/mo | `$0` until `closed_won`; then the actual monthly value (in-kind credits logged at fair-market). **Estimate / reference only** until signed. |

---

## CSV variant (copy-paste into a spreadsheet)

Quote any field that may contain a comma. `revenue` is numeric (0 until won).

```csv
prospect,company,role,channel,fit,template,sent,fu1,fu2,status,outcome,revenue_per_month
"Sam Lee","DevHost","Head of Growth","email",70,"founding-sponsor-dm","2026-07-01","2026-07-05","2026-07-10","replied","sent kit, on call",0
"Jane Doe","Acme Inc","DevRel","github_dm",82,"gold-tier-pitch","2026-07-02","2026-07-06","2026-07-11","sent","awaiting reply",0
"Pat Kim","CloudCo","Founder","intro",88,"platinum-warm","2026-07-02","","","replied","warm intro via mutual",0
```

---

## Weekly operating rhythm

- [ ] **Monday:** review the board. Any `sent` at +4 days with no reply → send Follow-up #1. Any `follow_up_1` at +9 days → send Follow-up #2.
- [ ] **Monday:** any `follow_up_2` with no positive reply → set `closed_lost`, move on.
- [ ] **Mid-week:** send the next wave of ~10 to `not_started` prospects (score 61+).
- [ ] **Friday:** replenish the list back toward 50 scored prospects. Re-score anything stale (>1 quarter old) — see [../tools/sponsor-fit-score.md](../tools/sponsor-fit-score.md) "Re-score quarterly."
- [ ] **Friday:** update `revenue_per_month` for any newly `closed_won` deals; roll up total MRR. Log in-kind deals at fair-market value alongside cash.

## KPIs to watch

- **Reply rate** (replied / sent) — a healthy cold-outbound reply rate is ~10–25%; below 5%, your targeting (fit score) or pitch is wrong, not your volume.
- **Close rate** (closed_won / replied) — track which template and which fit band converts best; double down on that segment.
- **Cycle time** (sent → closed_won) — if it stretches past ~3 weeks, your follow-ups aren't creating urgency; tighten the offer (first-month discount, peer-sponsor social proof).
- **MRR vs. pipeline coverage** — aim for ~3× your MRR target sitting in `sent`+`replied` at any time, since most prospects won't close.

> Don't optimize for messages sent. A 50-prospect list run with a tight 3-touch cadence and good fit-scoring will outperform 200 cold sprays every time — and it keeps your repo's reputation intact for the deals that actually matter. See [../data/sponsor-types.yml](../data/sponsor-types.yml) for which sponsor kind each prospect is, and [../templates/media-kit.md](../templates/media-kit.md) for the kit you attach once they reply.
