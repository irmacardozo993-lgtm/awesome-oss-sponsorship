<div align="center">

# awesome-oss-sponsorship

**Ein Praxisleitfaden, um Open-Source-Projekte bezahlt zu bekommen — Sponsoren, Werbenetzwerke, Affiliate-Deals und die Ansprache, die wirklich zum Abschluss führt.**

Kuratierte Plattformen · verifizierte Preisanker · Copy-Paste-Vorlagen · echte Fallstudien · ein 7-Tage-Kaltstart-Plan.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Made for maintainers](https://img.shields.io/badge/for-100%2B%20%E2%86%92%2010k%2B%20star%20repos-blueviolet)](#für-wen-das-ist)

</div>

🌐 **Languages:** [English](README.md) · [中文](README.zh-CN.md) · [Español](README.es.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

> **Sponsoring ist ein Vertriebskanal, keine Belohnung für Sternzahlen.** Sterne sind
> ein Beliebtheits-Proxy — die eigentlichen Preistreiber sind **eindeutige monatliche
> Besucher** (GitHub Traffic), **Paket-Downloads** (npm / PyPI / Docker Hub) und die
> **Passung zwischen Zielgruppe und Sponsor**. Dieses Repo ist das Playbook, um diesen
> Vertriebskanal professionell zu betreiben: welche Plattformen, welche Werbeplätze,
> welcher Preis, wen man anschreibt und was man sendet.

Alles hier ist **copy-paste-fähig** und auf **verifizierten öffentlichen Quellen**
fundiert (offizielle Doku, OpenCollective-Seiten, Maintainer-Blogs, Preisseiten der
Werbenetzwerke). Alle Preise sind **Schätzungen / nur als Referenz** — nie ein Angebot,
nie ein Versprechen. Siehe [den Haftungsausschluss](#haftungsausschluss).

---

## Inhaltsverzeichnis

- [Für wen das ist](#für-wen-das-ist)
- [Schnellstart (5 Minuten)](#schnellstart-5-minuten)
- [Wenn du nur 1,000 Sterne hast](#wenn-du-nur-1000-sterne-hast)
- [Plattformvergleich](#plattformvergleich)
- [Preisreferenz (Schätzung)](#preisreferenz-schätzung)
- [Affiliate-Programme, die wirklich zahlen](#affiliate-programme-die-wirklich-zahlen)
- [Wie man Sponsoren findet](#wie-man-sponsoren-findet)
- [Lokale Kanäle (DACH)](#lokale-kanäle-dach)
- [Der 7-Tage-Kaltstart-Plan](#der-7-tage-kaltstart-plan)
- [Vorlagen & Werkzeuge](#vorlagen--werkzeuge)
- [Dokumentation](#dokumentation)
- [Reale Fallstudien-Anker](#reale-fallstudien-anker)
- [Mitwirken](#mitwirken)
- [Star History](#star-history)
- [Haftungsausschluss](#haftungsausschluss)

---

## Für wen das ist

| Du bist | Starte hier |
|---------|-----------|
| **100-Sterne-Maintainer** (frühes CLI/SDK) | GitHub Sponsors (0% Gebühr) + `.github/FUNDING.yml`. Fokus auf Momentum, nicht auf Geld. → [100-Sterne-Beispiel](examples/100-stars-repo.md) |
| **1,000-Sterne-Maintainer** (der Sweet Spot) | GitHub Sponsors + Open Collective + eine Preiskarte. Starte den First-50-DMs-Plan. → [1000-Sterne-Playbook](docs/1000-stars-playbook.md) · [Beispiel](examples/1000-stars-repo.md) |
| **10,000-Sterne-Maintainer** | Gestaffeltes Programm + eigenständige Sponsorenseite + EthicalAds in der Doku. → [10000-Sterne-Beispiel](examples/10000-stars-repo.md) |
| **Indie / Solo-Entwickler** | GitHub Sponsors (wiederkehrend) + Buy Me a Coffee (einmalige Tipps). Lass den Fiscal Host weg. |
| **Devtool-/CLI-/SDK-Maintainer** | GitHub Sponsors + thanks.dev (eingehend über den Abhängigkeitsbaum) + Affiliate-Hybrid. |
| **Newsletter-betreibender Maintainer** | GitHub Sponsors + Paved (Newsletter-Anzeigen — höchster $/Impression). |
| **Maintainer, der ein kostenpflichtiges SaaS-/AI-Produkt ausliefert** | Polar (Merchant-of-Record) — **nicht** für Sponsoring. |

---

## Schnellstart (5 Minuten)

1. **Wähle eine Plattform.** Solo → [GitHub Sponsors](docs/github-sponsors.md) (0% persönliche Gebühr). Mehrere Mitwirkende/Anbieter → [Open Collective](docs/open-collective.md) (Fiscal Host + öffentliches Ledger).
2. **Füge `.github/FUNDING.yml` hinzu.** Verdrahtet den "Sponsor"-Button. Kopiere die [annotierte Vorlage](templates/funding-yml-example.md) (12 aktuelle Schlüssel; `otechie`/`givebutter`/`lfx_crowdfunding` werden **nicht** unterstützt).
3. **Setze Tiers.** GitHub Sponsors: bis zu 10 einmalig + 10 monatlich, max. $12,000/Monat; **der Preis ist nach Veröffentlichung unveränderlich** (deaktivieren + neu anlegen zum Ändern). Orientiere dich an echten Stufen — Vite `$5/$15/$50/$150/$500`, Astro `$10/$100/$200/$250/$1,000/$10,000` — aber kennzeichne deine eigenen als **Schätzung / nur als Referenz**.
4. **Liste dein Inventar.** Du verkaufst *Sichtbarkeit*, keine Sterne. Werbeplatz-Taxonomie in [`data/sponsor-types.yml`](data/sponsor-types.yml): README-Top-Banner, README-Bottom-Logo-Raster (das dominante Muster — dynamisches SVG, niemals das README editieren), Doku-Seiten-Anzeige, Release-Note, Newsletter.
5. **Starte die Ansprache.** Erstelle eine einseitige [Preiskarte](templates/rate-card.md), orientiert an **deinem** Traffic, und sende dann die [Cold-E-Mail](templates/cold-email.md)-Vorlage an Unternehmen in deinem Abhängigkeitsbaum oder deine Popular Referrers. Preis am **unteren** Ende ansetzen, bis du 3 Deals abgeschlossen hast.

> Der 5-Minuten-Pfad ist in [docs/getting-started.md](docs/getting-started.md) detailliert beschrieben.

---

## Wenn du nur 1,000 Sterne hast

1,000 Sterne sind der Sweet Spot: echte Nutzer, echte Downloads, echte Beschaffungsgespräche — aber noch nah genug an der Basis, dass du es selbst verkaufen kannst. Die vollständige Strategie ist das [1000-Sterne-Playbook](docs/1000-stars-playbook.md); das Wesentliche:

- **Es ist kommerziell wertvoll** — aber nur, wenn du verkaufst. [komorebi (~10k Sterne) verdiente nur ~$155/Monat](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) ohne Vertrieb; [Caleb Porchio erreichte ~$112,680/Jahr](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) durch aktiven Verkauf auf einer größeren Basis.
- **Preis am unteren Ende** des [Schätzrasters](#preisreferenz-schätzung); anheben nach 3 abgeschlossenen Deals.
- **Betreibe eine 50-Lead-Pipeline**, bewertet mit dem [Sponsor Fit Score](tools/sponsor-fit-score.md), in einem 3-Kontakte-dann-Abschluss-Rhythmus — siehe den [First-50-DMs-Plan](examples/1000-stars-repo.md#5-the-first-50-dms-plan).
- **Biete einen ersten Monat als Test** mit 50% Rabatt (oder gratis) an, um das Risiko für einen Gründungssponsor zu minimieren.
- **Schade dem Repo nicht.** Eine Prüfrichtlinie + saubere Affiliate-Kennzeichnung + kein Spam-Bombardement schützt den Ruf, der das Repo überhaupt erst sponsorsfähig macht.

---

## Plattformvergleich

Status am 2026-06-29 gegen offizielle Seiten verifiziert. Gebühren sind **nur als Referenz**.

| Plattform | Typ | Status | Gebühr (nur Ref.) | Am besten für |
|---|---|---|---|---|
| [GitHub Sponsors](docs/github-sponsors.md) | Sponsoring | ✅ aktiv | 0% persönlich / ≤6% Org | Solo-Maintainer; nativer GitHub-Button. ⚠ Festlandchina **nicht** unterstützt |
| [Open Collective](docs/open-collective.md) | Fiscal Host | ✅ aktiv | $0/$60/$320-Plan; oder 5% | öffentliches Ledger; mehrere Mitwirkende |
| Open Source Collective | Fiscal Host | ✅ aktiv | via OC | US-501(c)(6)-Dachverband, steuerlich absetzbar |
| [Polar](docs/polar.md) | Billing MoR | 🔄 gepivottet | 5%+50¢ → 3.40%+30¢ | kostenpflichtige SaaS-/AI-Abrechnung + Steuern. **Kein Sponsoring** |
| Buy Me a Coffee | Spende | ✅ aktiv | 5% + Stripe-Verarbeitung | einmalige Tipps |
| Ko-fi | Spende | ⚠ unbestätigt | 0% Spenden; Gold ~$12/Monat (verifizieren) | direkte PayPal-/Stripe-Tipps |
| Patreon | Abo | ✅ aktiv | 10% | wiederkehrende Mitgliedschaften |
| thanks.dev | Spende | ✅ aktiv | 5% | automatisch deinen Abhängigkeitsbaum finanzieren |
| StackAid | Spende | ✅ aktiv | Abos ab $15/Monat | direkte + transitive Abhängigkeiten finanzieren |
| Tidelift | Abo | ❌ übernommen | — | historisch; von Sonar übernommen (Dez. 2024) |
| IssueHunt | Bounty | ⚠ veraltet | n/d | Bounty-pro-Issue — **oss.issuehunt.io** nutzen, Aktivität verifizieren |
| Algora | Recruiting | 🔄 gepivottet | n/d | OSS-Hiring + Bounty-Sidebar |
| [EthicalAds](docs/ad-networks.md) | Werbung (CPM) | ✅ aktiv | 70% Umsatzbeteiligung, ~$2.50 CPM | Dev-Doku-Seiten (50k+ Pageviews) |
| Carbon Ads | Werbung (CPC) | ✅ aktiv | vertriebsgestützt | kuratierte Dev-Seiten ($5–10k Advertiser-Min.) |
| BuySellAds | Werbung (Multi) | ✅ aktiv | gemanagt | E-Mail/Native/Sponsored/Podcast |
| Passionfroot | Werbung/Marktplatz | 🔄 gepivottet→Zest | 2% / 15% | Newsletter-Brand-Deals |
| Paved | Werbung (Newsletter) | ✅ aktiv | Pauschale + PPC | Newsletter (25k Abos / 1M PV) |

Vollständige strukturierte DB: [`data/platforms.yml`](data/platforms.yml).

---

## Preisreferenz (Schätzung)

> **Schätzung / nur als Referenz.** Es gibt **keinen** standardisierten öffentlichen
> Markt, der $/Monat an die Sternzahl koppelt. Sternzahl ist ein Beliebtheits-Proxy,
> keine Preismetrik. Leite es aus **deinem** Traffic ab: Doku-Anzeige ≈
> `monthly_pageviews / 1000 × ~$2.50` (EthicalAds-Publisher-CPM); Newsletter ≈
> `subs × open_rate × CTR × target_cpc`, angebunden an [JavaScript Weeklys $3,590/Issue
> bei 180k Abos](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf). Preis
> ohne Traffic-/Konversionsdaten am **unteren** Ende ansetzen; anheben nach 3
> abgeschlossenen Deals.

Monatliche USD nach Stern-Tier × Werbeplatz (Schätzung):

| Sterne | README-Top-Banner | README-Bottom-Logo | README-Bottom-Text | Doku-Seiten-Anzeige | Release-Note | Newsletter / Issue |
|------:|---:|---:|---:|---:|---:|---:|
| 100 | $100–300 | $50–150 | $20–75 | $10–40 | $50–150 | $30–100 |
| 500 | $200–500 | $100–300 | $50–150 | $25–80 | $100–300 | $100–250 |
| 1,000 | $400–1,000 | $200–600 | $100–300 | $50–200 | $200–600 | $200–500 |
| 5,000 | $1,000–3,000 | $500–1,500 | $250–750 | $150–600 | $500–1,500 | $500–1,500 |
| 10,000 | $2,000–6,000 | $1,000–3,000 | $500–1,500 | $300–1,500 | $1,000–3,000 | $1,000–2,500 |
| 50,000 | $5,000–15,000 | $3,000–10,000 | $1,500–5,000 | $1,000–5,000 | $2,500–8,000 | $2,500–7,000 |

Deal-Modell-Modifikatoren (geschätzt): einmalige 12-Monats-Anzeige ≈ 8–10× monatlich (15–20% Rabatt); jährlich ≈ 10–12× monatlich (15–20% Rabatt); reines Affiliate = $0 Fixanteil + 10–30% wiederkehrend; **Fix + Affiliate-Hybrid** = niedrigerer Retainer + Provision (das beste Modell). Vollständiges Raster + inländisches RMB-Preisband in [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml); Copy-Paste-Preiskarte in [`templates/rate-card.md`](templates/rate-card.md).

---

## Affiliate-Programme, die wirklich zahlen

Die meisten Devtool-Unternehmen haben **kein** öffentliches Affiliate-Programm (OpenAI, Anthropic, GitHub, Supabase, Cloudflare, AWS — alle bestätigt nicht vorhanden). Die, die eines haben, verifiziert am 2026-06-29:

| Programm | Provision (Ref.) | Cookie | Auszahlung | Passung |
|---|---|---|---|---|
| [Railway](https://railway.com/affiliate-program) | 15% wiederkehrend, 12 Monate | n/d | GitHub Sponsors / BMC | ★★★ Cash via Sponsors |
| [Neon](https://neon.com/programs/open-source) | $20 Cash / Vermittlung | n/d | GitHub Sponsors | ★★★ OSS-Programm |
| [ElevenLabs](https://elevenlabs.io/affiliates) | 22% wiederkehrend, 12 Monate | n/d | PartnerStack, $5 | ★★★ AI-Voice |
| [Apify](https://apify.com/partners/affiliate) | 20%→30%, Deckel $2,500/Kunde | 45 Tage | PayPal/Bank, $100 | ★★★ Scraping |
| [Bright Data](https://brightdata.com/affiliate) | 50% bis zu $2,500 + 15% 2. Tier | 90 Tage | PartnerStack | ★★★ Proxys |
| [ScrapingBee](https://www.scrapingbee.com/affiliates/) | 25% wiederkehrend, lebenslang | n/d | PayPal, $50 | ★★★ Scraping |
| [Browserless](https://www.browserless.io/affiliate) | 20–30% gestaffelt, 12 Monate | 90 Tage | PayPal/Bank, $50 | ★★★ Headless-Browser |
| [n8n](https://n8n.io/affiliates/) | 30% wiederkehrend, 12 Monate (Cloud) | n/d | PayPal, €100 | ★★★ Automatisierung |
| [Make](https://www.make.com/en/affiliate) | 35% wiederkehrend, 12 Monate | 30 Tage | Wise, $100 | ★★ Automatisierung |
| [Raycast](https://www.raycast.com/blog/affiliate-program) | 30% wiederkehrend (Pro) | n/d | Wise, £50 | ★★ macOS |
| [Pluralsight](https://www.pluralsight.com/affiliate) | $1/Trial + 30%/10%/5% einmalig | 7 Tage | CJ | ★★ Dev-Lernen |
| [DigitalOcean](https://www.digitalocean.com/affiliates) | 10% wiederkehrend, 12 Monate | n/d | Awin/CJ | ★★ Hosting |
| [Netlify](https://www.netlify.com/partners/) | 20% wiederkehrend, 12–24 Monate | n/d | PartnerStack | ★★ Jamstack |
| [Vercel / v0](https://partners.dub.co/v0) | 30% wiederkehrend, 6 Monate + $5/Lead | n/d | Dub | ★★ Frontend |

Geschlossen/eingestellt: Hetzner (eingestellt 2026-06-15), Notion (für Neuzugänge geschlossen), ShareASale (eingestellt→Awin), Heroku (eingestellt).
Netzwerke, denen du als Publisher beitreten kannst: **PartnerStack** (beste Devtool-Dichte, $5 Min.) und **Impact** (breit, $10 Min.). Vollständige DB + die "kein Programm gefunden"-Entlarvungsliste in [`data/affiliate-programs.yml`](data/affiliate-programs.yml) und [docs/affiliate-programs.md](docs/affiliate-programs.md).

---

## Wie man Sponsoren findet

Kein Spray-and-Pray. Baue eine bewertete 50-Lead-Liste auf. Prioritäre Quellen (vollständige Methode in [docs/outreach.md](docs/outreach.md)):

1. **Unternehmen in deinem Abhängigkeitsbaum** — wer liefert Software aus, die dein Projekt *nutzt*? Ihre DevRel-/Growth-Teams sind die beste Passung.
2. **Stargazer/Forker, die Unternehmen sind** — GitHub-Orgs, die dich staren/forken; finde den DevRel-/Gründer-/Growth-Kontakt via LinkedIn/X.
3. **Angrenzende Anbieter** — Produkte, die *mit* deinem deployt werden (Hosting, ORM, Observability, CI).
4. **Sachleistung-Sponsoren** — Hosting-/CI-/Secrets-/Monitoring-Anbieter, die Credits gegen ein Logo tauschen (Homebrew-Muster: MacStadium, 1Password).
5. **Power-User-Issue-Reporter** — bitte sie, ihren Arbeitgeber vorzustellen.

Bewerte jeden Lead mit dem [Sponsor Fit Score](tools/sponsor-fit-score.md) (0–100). Verfolge **61–100**; überspringe **0–30**. Sende die [Cold-E-Mail](templates/cold-email.md)-/[DM](templates/dm-template.md)-Vorlagen in einem 3-Kontakte-dann-Abschluss-Rhythmus. Tracke alles in der [Outreach-Checkliste](tools/outreach-checklist.md).

---

## Lokale Kanäle (DACH)

Regionale Ansprache für den deutschsprachigen Raum — alle Angaben **nur als Referenz**, keine verifizierten konkreten Sponsoring-Deals:

- **Fachmedien & Artikel:** heise Developer und Golem.de erreichen eine große deutschsprachige Entwickler-Leserschaft; gut geschriebene deutsche Fachartikel eignen sich als Sichtbarkeit und Eisbrecher für die Sponsoring-Ansprache.
- **Lokale Meetups:** regionale Dev-Meetups (JavaScript, Python, Cloud u. a.) sind niedrigschwellige Orte, um DACH-Unternehmen und Maintainer direkt zu treffen.
- **Konferenzen:** JAX und OOP ziehen Enterprise- und Devtool-Entscheider aus der DACH-Region an — gut für Networking und Kontaktaufbau.
- **DACH-Unternehmen:** Firmen mit OSS-freundlichen Richtlinien sind grundsätzlich ansprechbar; vorab prüfen, ob sie ein öffentliches OSS- oder Sponsoring-Budget ausweisen.

---

## Der 7-Tage-Kaltstart-Plan

Eine Woche, um von "kein Sponsoren-Programm" zu "erste Pitches raus + Repo gelauncht" zu kommen. Jeder Tag ist eine Checkliste in [docs/launch-plan.md](docs/launch-plan.md) und [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md).

| Tag | Tue dies | Output |
|---|---|---|
| **1** | Plattform wählen; `.github/FUNDING.yml` hinzufügen; 3–5 Tiers setzen (unteres Ende) | Live Sponsor-Button + Tier-Leiter |
| **2** | Werbeplätze auflisten; eine einseitige [Preiskarte](templates/rate-card.md) bauen | Preiskarte (interner Anker) |
| **3** | GitHub Traffic + npm/PyPI/Docker-Downloads ziehen; ein einseitiges [Sponsor Kit](templates/sponsor-kit.md) bauen | Kit mit Selbstauskunfts-Traffic-Vorbehalt |
| **4** | Eine 50-Lead-Liste bauen (Abhängigkeitsbaum, Stargazer-Orgs, angrenzende Anbieter); mit [Sponsor Fit Score](tools/sponsor-fit-score.md) bewerten | Bewertete Lead-Liste |
| **5** | Welle 1 senden (10 Leads) via [Cold-E-Mail](templates/cold-email.md) / [DM](templates/dm-template.md) | 10 Outbounds, getrackt |
| **6** | Welle 2 senden (10); Launch-Posts entwerfen (HN / Reddit / V2EX / X) | Launch-Assets bereit |
| **7** | Launchen + eigenständige Sponsorenseite veröffentlichen; alles in der [Outreach-Checkliste](tools/outreach-checklist.md) festhalten | Repo live, Pipeline läuft |

Nach Tag 7: die rollende 50-Lead-Pipeline weiterführen, 3-Kontakte-Rhythmen durchlaufen und Updates für organisches Sternenwachstum aufrechterhalten (siehe [docs/launch-plan.md](docs/launch-plan.md) §12).

---

## Vorlagen & Werkzeuge

Copy-Paste, `[Klammern]` ausfüllen, ausliefern.

| Datei | Was es ist |
|---|---|
| [templates/funding-yml-example.md](templates/funding-yml-example.md) | Annotierte `.github/FUNDING.yml` — alle 12 Schlüssel, 3 vollständige Beispiele |
| [templates/rate-card.md](templates/rate-card.md) | Einseitige Preiskarte (USD + RMB, Stern-Tier × Werbeplatz-Raster) |
| [templates/cold-email.md](templates/cold-email.md) | Cold-E-Mail + Follow-ups + Ja/Nein-Antworten (EN + 中文) |
| [templates/dm-template.md](templates/dm-template.md) | LinkedIn / X / Discord / 微信 / V2EX-掘金 DMs |
| [templates/sponsor-kit.md](templates/sponsor-kit.md) | Vollständiges Sponsor Kit (Ausfüllen + durchgerechnetes Beispiel) |
| [templates/media-kit.md](templates/media-kit.md) | Media-Kit im TLDR-Stil (alle Komponenten + Beispiel) |
| [templates/readme-sponsor-block.md](templates/readme-sponsor-block.md) | README-Top/Bottom/Logo/Text/Affiliate-Snippets |
| [templates/affiliate-tracker.csv](templates/affiliate-tracker.csv) | CSV zum Tracken von Affiliate-Deals |
| [tools/sponsor-fit-score.md](tools/sponsor-fit-score.md) | 0–100-Lead-Bewertungsmodell + durchgerechnetes Beispiel |
| [tools/outreach-checklist.md](tools/outreach-checklist.md) | 50-Lead-Pipeline-Tracker (Markdown + CSV) |

---

## Dokumentation

| Doku | Behandelt |
|---|---|
| [docs/getting-started.md](docs/getting-started.md) | Orientierung + der 5-Minuten-Pfad + Link-Map |
| [docs/github-sponsors.md](docs/github-sponsors.md) | Voraussetzungen, Regionen (China-Vorbehalt), Setup, Tiers, Gebühren, README-Anzeige |
| [docs/open-collective.md](docs/open-collective.md) | Fiscal Hosts, OSC 501(c)(6), öffentliches Ledger, Pläne/Gebühren |
| [docs/polar.md](docs/polar.md) | Der Pivot zu AI-Abrechnung / MoR — wann es passt und wann nicht |
| [docs/ad-networks.md](docs/ad-networks.md) | EthicalAds, Carbon, BuySellAds, Passionfroot, Paved |
| [docs/affiliate-programs.md](docs/affiliate-programs.md) | Verifizierte Affiliate-Programme + die Entlarvungsliste + Netzwerke |
| [docs/pricing.md](docs/pricing.md) | Wie man Preise festlegt (Traffic, nicht Sterne) + Schätzraster |
| [docs/sponsor-kit.md](docs/sponsor-kit.md) | Ein Sponsor Kit bauen (Leitfaden) + GitHub-Traffic-Fakten |
| [docs/readme-monetization.md](docs/readme-monetization.md) | README + Flächen-Monetarisierung (jeder Werbeplatz) |
| [docs/outreach.md](docs/outreach.md) | Proaktiv Sponsoren finden |
| [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md) | Das 10-Abschnitte-1k-Sterne-Playbook |
| [docs/launch-plan.md](docs/launch-plan.md) | Kaltstart-Verteilung (HN/Reddit/PH/V2EX/掘金/X) |
| [docs/case-studies.md](docs/case-studies.md) | Verifizierte offengelegte Zahlen (Astro/Vue/Vite/Tailwind/Sentry/…) |
| [docs/faq.md](docs/faq.md) | 15+ Q&A |

Daten (Source of Truth): [`data/platforms.yml`](data/platforms.yml) · [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml) · [`data/sponsor-types.yml`](data/sponsor-types.yml) · [`data/affiliate-programs.yml`](data/affiliate-programs.yml).

---

## Reale Fallstudien-Anker

Öffentlich offengelegte Zahlen (zitiert in [docs/case-studies.md](docs/case-studies.md)). Schätzungen gekennzeichnet.

| Projekt | Offengelegt (Quelle) | Erkenntnis |
|---|---|---|
| [Astro](https://opencollective.com/astrodotbuild) | $836k insgesamt auf OC; Tiers bis zu $10,000/Monat | Saubere Leiter + Sponsorenseite + Fiscal Host = die Obergrenze |
| [Vue.js](https://opencollective.com/vuejs) | $852k insgesamt auf OC | Selbstgehostete Sponsorenseite + BACKERS.md funktioniert |
| [Vite](https://opencollective.com/vite) | $162k insgesamt auf OC; Bronze $50 → Gold $500 | Eine einfachere Leiter funktioniert ebenfalls |
| [Homebrew](https://opencollective.com/homebrew) | $486k insgesamt auf OC | Sachleistung (MacStadium/1Password) + Cash-Mix |
| [Tailwind CSS](https://tailwindcss.com/sponsor) | Partner $5,000/Monat (geschätzt ~$200k/Monat von ~70 Untern.) | Sponsoring-Tiers funktionieren im Flagship-Maßstab; kommerziell ≠ Sponsoring |
| [Sentry](https://blog.sentry.io) | $155k→$750k/Jahr OSS-Outflow; $2,000/Ingenieur/Jahr-Zusage | Was ein *Sponsor* budgetiert |
| [Caleb Porchio](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) | $112,680/Jahr auf GitHub Sponsors | Aktiver Verkauf auf einer realen Basis |
| [komorebi (~10k★)](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) | $1,861/Jahr (~$155/Monat) | **10k Sterne ≠ Sponsoring ohne Vertrieb** |

---

## Mitwirken

Korrekturen und neue Plattformen/Programme sind willkommen — **mit einer zitierten offiziellen Quelle**. Siehe [CONTRIBUTING.md](CONTRIBUTING.md). Die eine Regel: **veröffentliche keine unbestätigten Fakten**; markiere alles Unsichere als `unverified`, anstatt zu raten.

---

## Star History

<a href="https://star-history.com/#irmacardozo993-lgtm/awesome-oss-sponsorship&Date">
  <img src="https://api.star-history.com/svg?repos=irmacardozo993-lgtm/awesome-oss-sponsorship&type=Date" alt="Star History">
</a>

---

## Danksagung

- **[Linux.do](https://linux.do)** — chinesischsprachige Entwickler- und Tech-Community (Discourse), deren Mitglieder und Feedback die China-Verbreitungsanleitung in diesem Repo geprägt haben.
- **Telegram OpenClaw 中文社区** — die chinesischsprachige OpenClaw-Community auf Telegram, für Support und Diskussion.

---

## Haftungsausschluss

Alle Preis-, Gebühren-, Provisionssatz- und Umsatzzahlen in diesem Repository sind
**Schätzungen / nur als Referenz**. Sie sind keine Angebote, keine Garantien und keine
Finanz-, Rechts- oder Steuerberatung. Echte Preise hängen von der Branche, dem Traffic,
der Nutzerqualität, der Konversionsrate, der Geografie der Zielgruppe und dem
Sponsorenbudget ab. **Verifiziere die aktuellen Konditionen bei jeder Plattform, bevor
du dich auf sie verlässt.** Plattform-Status wurde am 2026-06-29 geprüft und ändert sich
häufig. Dieses Projekt verspricht keine Einnahmen und ist kein "Schnell-reich-werden"-
Schema — es ist ein Praxisleitfaden für Maintainer, die Sponsoring professionell betreiben
wollen.

Lizenz: [CC-BY-4.0](LICENSE) für Inhalte; MIT für eingebettete Code-Snippets. Siehe [LICENSE](LICENSE).
