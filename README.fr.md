<div align="center">

# awesome-oss-sponsorship

**Un guide de terrain pour faire payer les projets open source — sponsors, régies publicitaires, accords d'affiliation et la prospection qui conclut vraiment.**

Plateformes sélectionnées · repères de prix vérifiés · modèles prêts à copier · études de cas réelles · un plan de démarrage à froid sur 7 jours.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Made for maintainers](https://img.shields.io/badge/for-100%2B%20%E2%86%92%2010k%2B%20star%20repos-blueviolet)](#à-qui-sadresse-ce-guide)

</div>

🌐 **Languages:** [English](README.md) · [中文](README.zh-CN.md) · [Español](README.es.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

> **Le sponsoring est un canal de vente, pas une récompense liée au nombre d'étoiles.** Les
> étoiles sont un indicateur de popularité — les véritables leviers de prix sont les
> **visiteurs uniques mensuels** (GitHub Traffic), les **téléchargements de packages** (npm
> / PyPI / Docker Hub) et l'**adéquation audience-sponsor**. Ce dépôt est le manuel pour
> gérer ce canal de vente de façon professionnelle : quelles plateformes, quels emplacements,
> quel prix, qui contacter et quoi envoyer.

Tout ici est **prêt à copier-coller** et fondé sur des **sources publiques vérifiées**
(documentation officielle, pages OpenCollective, blogs de mainteneurs, pages de tarifs des
régies publicitaires). Tous les prix sont des **estimations / référence uniquement** —
jamais un devis, jamais une promesse. Voir [l'avertissement](#avertissement).

---

## Table des matières

- [À qui s'adresse ce guide](#à-qui-sadresse-ce-guide)
- [Démarrage rapide (5 minutes)](#démarrage-rapide-5-minutes)
- [Si vous n'avez que 1,000 étoiles](#si-vous-navez-que-1000-étoiles)
- [Comparatif des plateformes](#comparatif-des-plateformes)
- [Référentiel de tarifs (estimation)](#référentiel-de-tarifs-estimation)
- [Programmes d'affiliation qui paient vraiment](#programmes-daffiliation-qui-paient-vraiment)
- [Comment trouver des sponsors](#comment-trouver-des-sponsors)
  - [Canaux locaux (communautés francophones)](#canaux-locaux-communautés-francophones)
- [Le plan de démarrage à froid sur 7 jours](#le-plan-de-démarrage-à-froid-sur-7-jours)
- [Modèles et outils](#modèles-et-outils)
- [Documentation](#documentation)
- [Ancres d'études de cas réelles](#ancres-détudes-de-cas-réelles)
- [Contribuer](#contribuer)
- [Historique des étoiles](#historique-des-étoiles)
- [Avertissement](#avertissement)

---

## À qui s'adresse ce guide

| Vous êtes | Commencez ici |
|---------|-----------|
| **Mainteneur à 100 étoiles** (CLI/SDK émergent) | GitHub Sponsors (0% de frais) + `.github/FUNDING.yml`. Concentrez-vous sur l'élan, pas sur l'argent. → [exemple 100 étoiles](examples/100-stars-repo.md) |
| **Mainteneur à 1,000 étoiles** (le point idéal) | GitHub Sponsors + Open Collective + une carte de tarifs. Lancez le plan des 50 premiers DMs. → [playbook 1000 étoiles](docs/1000-stars-playbook.md) · [exemple](examples/1000-stars-repo.md) |
| **Mainteneur à 10,000 étoiles** | Programme par paliers + page sponsor dédiée + EthicalAds sur la doc. → [exemple 10000 étoiles](examples/10000-stars-repo.md) |
| **Indie / dev solo** | GitHub Sponsors (récurrent) + Buy Me a Coffee (pourboires ponctuels). Sautez l'hôte fiscal. |
| **Mainteneur Devtool / CLI / SDK** | GitHub Sponsors + thanks.dev (entrées depuis l'arbre des dépendances) + hybride affiliation. |
| **Mainteneur qui édite une newsletter** | GitHub Sponsors + Paved (annonces en newsletter — meilleur $/impression). |
| **Mainteneur qui lance un produit SaaS/AI payant** | Polar (Merchant-of-Record) — **pas** pour le sponsoring. |

---

## Démarrage rapide (5 minutes)

1. **Choisissez une plateforme.** En solo → [GitHub Sponsors](docs/github-sponsors.md) (0% de frais personnels). Plusieurs contributeurs/fournisseurs → [Open Collective](docs/open-collective.md) (hôte fiscal + livre comptable public).
2. **Ajoutez `.github/FUNDING.yml`.** Active le bouton « Sponsor ». Copiez le [modèle annoté](templates/funding-yml-example.md) (12 clés actuelles ; `otechie`/`givebutter`/`lfx_crowdfunding` **ne sont pas** pris en charge).
3. **Définissez les paliers.** GitHub Sponsors : jusqu'à 10 ponctuels + 10 mensuels, maximum $12,000/mo ; **le prix est immuable une fois publié** (retirez + recréez pour changer). Ancrez sur des échelles réelles — Vite `$5/$15/$50/$150/$500`, Astro `$10/$100/$200/$250/$1,000/$10,000` — mais étiquetez les vôtres **estimation / référence uniquement**.
4. **Listez votre inventaire.** Vous vendez de la *visibilité*, pas des étoiles. Taxonomie des emplacements dans [`data/sponsor-types.yml`](data/sponsor-types.yml) : bannière en haut du README, grille de logos en bas du README (le motif dominant — SVG dynamique, ne jamais éditer le README), annonce sur le site de doc, release-note, newsletter.
5. **Lancez la prospection.** Construisez une [carte de tarifs](templates/rate-card.md) d'une page ancrée sur **votre** trafic, puis envoyez le modèle d'[e-mail à froid](templates/cold-email.md) aux entreprises de votre arbre des dépendances ou de vos Popular Referrers. Fixez les prix sur la **fourchette basse** jusqu'à 3 accords signés.

> Le parcours en 5 minutes est détaillé dans [docs/getting-started.md](docs/getting-started.md).

---

## Si vous n'avez que 1,000 étoiles

1,000 étoiles, c'est le point idéal : de vrais utilisateurs, de vrais téléchargements, de vraies discussions d'achat — mais toujours assez près du terrain pour pouvoir vendre vous-même. La stratégie complète est le [playbook 1000 étoiles](docs/1000-stars-playbook.md) ; l'essentiel :

- **Cela a une valeur commerciale** — mais seulement si vous vendez. [komorebi (~10k étoiles) n'a généré que ~$155/mo](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) sans vente ; [Caleb Porzio a atteint ~$112,680/yr](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) en vendant activement sur une base plus large.
- **Fixez les prix sur la fourchette basse** de la [grille d'estimation](#référentiel-de-tarifs-estimation) ; montez après 3 accords signés.
- **Faites tourner un pipeline de 50 prospects**, scorés avec le [Sponsor Fit Score](tools/sponsor-fit-score.md), sur une cadence en 3 prises de contact puis clôture — voir le [plan des 50 premiers DMs](examples/1000-stars-repo.md#5-the-first-50-dms-plan).
- **Proposez un test le premier mois** à 50% de réduction (ou gratuit) pour lever le risque pour un sponsor fondateur.
- **Préservez le dépôt.** Une politique de validation + une divulgation d'affiliation claire + l'absence de spam en masse protègent la réputation qui rend le dépôt sponsorisable en premier lieu.

---

## Comparatif des plateformes

Statuts vérifiés le 2026-06-29 sur les sites officiels. Les frais sont **de référence uniquement**.

| Plateforme | Type | Statut | Frais (réf. uniquement) | Idéal pour |
|---|---|---|---|---|
| [GitHub Sponsors](docs/github-sponsors.md) | sponsoring | ✅ actif | 0% personnel / ≤6% org | mainteneurs en solo ; bouton GitHub natif. ⚠ Chine continentale **non** prise en charge |
| [Open Collective](docs/open-collective.md) | hôte fiscal | ✅ actif | plan $0/$60/$320 ; ou 5% | livre comptable public ; plusieurs contributeurs |
| Open Source Collective | hôte fiscal | ✅ actif | via OC | organisation parapluie 501(c)(6) américaine, déductible fiscalement |
| [Polar](docs/polar.md) | facturation MoR | 🔄 pivoté | 5%+50¢ → 3.40%+30¢ | facturation + taxes pour SaaS/AI payant. **Pas du sponsoring** |
| Buy Me a Coffee | don | ✅ actif | 5% + frais Stripe | pourboires ponctuels |
| Ko-fi | don | ⚠ non vérifié | 0% dons ; Gold ~$12/mo (à vérifier) | pourboires directs via PayPal/Stripe |
| Patreon | abonnement | ✅ actif | 10% | adhésions récurrentes |
| thanks.dev | don | ✅ actif | 5% | financez automatiquement votre arbre des dépendances |
| StackAid | don | ✅ actif | abonnements dès $15/mo | financez les dépendances directes + transitives |
| Tidelift | abonnement | ❌ acquis | — | historique ; acquis par Sonar (déc. 2024) |
| IssueHunt | bounty | ⚠ stagnant | n/d | bounty sur issue — utilisez **oss.issuehunt.io**, vérifiez qu'il est actif |
| Algora | recrutement | 🔄 pivoté | n/d | recrutement OSS + bounty en encart latéral |
| [EthicalAds](docs/ad-networks.md) | annonces (CPM) | ✅ actif | 70% revshare, ~$2.50 CPM | sites de doc pour devs (50k+ pageviews) |
| Carbon Ads | annonces (CPC) | ✅ actif | assisté par les ventes | sites dev sélectionnés ($5–10k min. annonceur) |
| BuySellAds | annonces (multi) | ✅ actif | géré | email/natif/sponsorisé/podcast |
| Passionfroot | annonces/marketplace | 🔄 pivoté→Zest | 2% / 15% | accords de marque en newsletter |
| Paved | annonces (newsletter) | ✅ actif | forfait + PPC | newsletters (25k subs / 1M pv) |

Base de données structurée complète : [`data/platforms.yml`](data/platforms.yml).

---

## Référentiel de tarifs (estimation)

> **Estimation / référence uniquement.** Il n'existe **aucun** marché public standardisé
> reliant les $/mois au nombre d'étoiles. Le nombre d'étoiles est un indicateur de
> popularité, pas une métrique de prix. Recalculez à partir de **votre** trafic : annonce
> sur la doc ≈ `monthly_pageviews / 1000 × ~$2.50` (CPM éditeur EthicalAds) ; newsletter ≈
> `subs × open_rate × CTR × target_cpc`, ancré aux [$3,590/numéro de JavaScript Weekly
> pour 180k abonnés](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf).
> Fixez les prix sur la **fourchette basse** sans données de trafic/conversion ; montez
> après 3 accords signés.

USD mensuel par palier d'étoiles × emplacement (estimation) :

| Étoiles | Bannière haut README | Logo bas README | Texte bas README | Annonce sur doc | Release note | Newsletter / numéro |
|------:|---:|---:|---:|---:|---:|---:|
| 100 | $100–300 | $50–150 | $20–75 | $10–40 | $50–150 | $30–100 |
| 500 | $200–500 | $100–300 | $50–150 | $25–80 | $100–300 | $100–250 |
| 1,000 | $400–1,000 | $200–600 | $100–300 | $50–200 | $200–600 | $200–500 |
| 5,000 | $1,000–3,000 | $500–1,500 | $250–750 | $150–600 | $500–1,500 | $500–1,500 |
| 10,000 | $2,000–6,000 | $1,000–3,000 | $500–1,500 | $300–1,500 | $1,000–3,000 | $1,000–2,500 |
| 50,000 | $5,000–15,000 | $3,000–10,000 | $1,500–5,000 | $1,000–5,000 | $2,500–8,000 | $2,500–7,000 |

Modificateurs selon le modèle d'accord (est.) : affichage ponctuel sur 12 mois ≈ 8–10× mensuel (15–20% de réduction) ; annuel ≈ 10–12× mensuel (15–20% de réduction) ; affiliation pure = $0 fixe + 10–30% récurrent ; **hybride fixe + affiliation** = retainer réduit + commission (le meilleur modèle). Grille complète + fourchette nationale en RMB dans [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml) ; carte de tarifs prête à copier dans [`templates/rate-card.md`](templates/rate-card.md).

---

## Programmes d'affiliation qui paient vraiment

La plupart des éditeurs de devtools n'ont **aucun** programme d'affiliation public (OpenAI, Anthropic, GitHub, Supabase, Cloudflare, AWS — tous confirmés absents). Ceux qui en ont, vérifiés le 2026-06-29 :

| Programme | Commission (réf.) | Cookie | Paiement | Adéquation |
|---|---|---|---|---|
| [Railway](https://railway.com/affiliate-program) | 15% récurrent, 12 mo | n/d | GitHub Sponsors / BMC | ★★★ cash via Sponsors |
| [Neon](https://neon.com/programs/open-source) | $20 cash / parrainage | n/d | GitHub Sponsors | ★★★ programme OSS |
| [ElevenLabs](https://elevenlabs.io/affiliates) | 22% récurrent, 12 mo | n/d | PartnerStack, $5 | ★★★ voix IA |
| [Apify](https://apify.com/partners/affiliate) | 20%→30%, plafond $2,500/client | 45 j | PayPal/banque, $100 | ★★★ scraping |
| [Bright Data](https://brightdata.com/affiliate) | 50% jusqu'à $2,500 + 15% 2e niveau | 90 j | PartnerStack | ★★★ proxies |
| [ScrapingBee](https://www.scrapingbee.com/affiliates/) | 25% récurrent à vie | n/d | PayPal, $50 | ★★★ scraping |
| [Browserless](https://www.browserless.io/affiliate) | 20–30% par paliers, 12 mo | 90 j | PayPal/banque, $50 | ★★★ navigateur headless |
| [n8n](https://n8n.io/affiliates/) | 30% récurrent, 12 mo (Cloud) | n/d | PayPal, €100 | ★★★ automatisation |
| [Make](https://www.make.com/en/affiliate) | 35% récurrent, 12 mo | 30 j | Wise, $100 | ★★ automatisation |
| [Raycast](https://www.raycast.com/blog/affiliate-program) | 30% récurrent (Pro) | n/d | Wise, £50 | ★★ macOS |
| [Pluralsight](https://www.pluralsight.com/affiliate) | $1/essai + 30%/10%/5% ponctuel | 7 j | CJ | ★★ apprentissage dev |
| [DigitalOcean](https://www.digitalocean.com/affiliates) | 10% récurrent, 12 mo | n/d | Awin/CJ | ★★ hébergement |
| [Netlify](https://www.netlify.com/partners/) | 20% récurrent, 12–24 mo | n/d | PartnerStack | ★★ Jamstack |
| [Vercel / v0](https://partners.dub.co/v0) | 30% récurrent, 6 mo + $5/lead | n/d | Dub | ★★ frontend |

Fermés/morts : Hetzner (arrêté 2026-06-15), Notion (fermé aux nouveaux), ShareASale (disparu→Awin), Heroku (mort).
Réseaux à rejoindre en tant qu'éditeur : **PartnerStack** (meilleure densité de devtools, min. $5) et **Impact** (large, min. $10). Base de données complète + la liste de débunkage « no program found » dans [`data/affiliate-programs.yml`](data/affiliate-programs.yml) et [docs/affiliate-programs.md](docs/affiliate-programs.md).

---

## Comment trouver des sponsors

Pas d'arrosage à l'aveugle. Construisez une liste scorée de 50 prospects. Sources prioritaires (méthode complète dans [docs/outreach.md](docs/outreach.md)) :

1. **Entreprises de votre arbre des dépendances** — qui publie du logiciel qui *utilise* votre projet ? Leurs équipes DevRel/growth sont les mieux adaptées.
2. **Stargazers/forkers qui sont des entreprises** — les organisations GitHub qui vous mettent en étoile ou font un fork ; trouvez le contact DevRel/fondateur/growth via LinkedIn/X.
3. **Fournisseurs adjacents** — des produits qui se déploient *avec* le vôtre (hosting, ORM, observabilité, CI).
4. **Sponsors en nature** — fournisseurs d'hosting/CI/secrets/monitoring qui échangent des crédits contre un logo (modèle Homebrew : MacStadium, 1Password).
5. **Auteurs d'issues power-users** — demandez-leur de vous présenter leur employeur.

Attribuez un score à chaque prospect avec le [Sponsor Fit Score](tools/sponsor-fit-score.md) (0–100). Visez **61–100** ; ignorez **0–30**. Envoyez les modèles d'[e-mail à froid](templates/cold-email.md) / [DM](templates/dm-template.md) sur une cadence en 3 prises de contact puis clôture. Suivez tout dans la [checklist de prospection](tools/outreach-checklist.md).

### Canaux locaux (communautés francophones)

> **À titre de référence uniquement.** Espaces et communautés francophones pour faire
> connaître votre projet et bâtir l'audience que les sponsors achètent ; vérifiez
> l'actualité de chaque communauté avant de vous impliquer.

- **LinuxFr.org :** média historique de la communauté libre francophone ; y publier un article technique à valeur ajoutée (retour d'expérience, mise en production) construit une audience technique qualifiée et du trafic vers le dépôt.
- **Discord et Meetups francophones :** groupes de développeurs en France, Belgique, Suisse et dans la francophonie ; participez de manière authentique (répondre, partager des releases) avant de demander quoi que ce soit.
- **Conférences (Paris Web, Devoxx France) :** lieux de présentation de votre projet et d'échanges avec les équipes DevRel ; de nombreuses entreprises y allouent des budgets de developer relations.
- **Billets techniques en français :** un contenu qui résout de vrais problèmes de la communauté francophone avant la prospection construit une audience moins saturée que l'anglophone.
- **Meetups locaux :** les rencontres régionales permettent de nouer des contacts directs avec des mainteneurs et des sponsors potentiels.

---

## Le plan de démarrage à froid sur 7 jours

Une semaine pour passer de « aucun programme de sponsoring » à « premières propositions envoyées + dépôt lancé ». Chaque jour est une checklist dans [docs/launch-plan.md](docs/launch-plan.md) et [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md).

| Jour | À faire | Résultat |
|---|---|---|
| **1** | Choisir la plateforme ; ajouter `.github/FUNDING.yml` ; définir 3–5 paliers (fourchette basse) | Bouton Sponsor actif + échelle de paliers |
| **2** | Lister les emplacements d'inventaire ; construire une [carte de tarifs](templates/rate-card.md) d'une page | Carte de tarifs (ancre interne) |
| **3** | Récupérer le GitHub Traffic + les téléchargements npm/PyPI/Docker ; construire un [sponsor kit](templates/sponsor-kit.md) d'une page | Kit avec la réserve sur le trafic auto-déclaré |
| **4** | Construire une liste de 50 prospects (arbre des dépendances, orgs stargazers, fournisseurs adjacents) ; attribuer un score avec le [Sponsor Fit Score](tools/sponsor-fit-score.md) | Liste de prospects scorée |
| **5** | Envoyer la vague 1 (10 prospects) via [e-mail à froid](templates/cold-email.md) / [DM](templates/dm-template.md) | 10 sorties, suivies |
| **6** | Envoyer la vague 2 (10) ; rédiger les posts de lancement (HN / Reddit / V2EX / X) | Ressources de lancement prêtes |
| **7** | Lancer + publier une page sponsor dédiée ; tout journaliser dans la [checklist de prospection](tools/outreach-checklist.md) | Dépôt en ligne, pipeline en marche |

Après le jour 7 : conservez le pipeline roulant de 50 prospects, enchaînez les cadences en 3 prises de contact, et maintenez les mises à jour pour une croissance organique des étoiles (voir [docs/launch-plan.md](docs/launch-plan.md) §12).

---

## Modèles et outils

Copiez-collez, remplissez les `[brackets]`, publiez.

| Fichier | Ce que c'est |
|---|---|
| [templates/funding-yml-example.md](templates/funding-yml-example.md) | `.github/FUNDING.yml` annoté — les 12 clés, 3 exemples complets |
| [templates/rate-card.md](templates/rate-card.md) | Carte de tarifs d'une page (USD + RMB, grille palier d'étoiles × emplacement) |
| [templates/cold-email.md](templates/cold-email.md) | E-mail à froid + relances + réponses oui/non (EN + 中文) |
| [templates/dm-template.md](templates/dm-template.md) | DMs LinkedIn / X / Discord / 微信 / V2EX-掘金 |
| [templates/sponsor-kit.md](templates/sponsor-kit.md) | Sponsor kit complet (à remplir + exemple résolu) |
| [templates/media-kit.md](templates/media-kit.md) | Media kit style TLDR (tous les composants + exemple) |
| [templates/readme-sponsor-block.md](templates/readme-sponsor-block.md) | Snippets README haut/bas/logo/texte/affiliation |
| [templates/affiliate-tracker.csv](templates/affiliate-tracker.csv) | CSV pour suivre les accords d'affiliation |
| [tools/sponsor-fit-score.md](tools/sponsor-fit-score.md) | Modèle de scoring de prospects 0–100 + exemple résolu |
| [tools/outreach-checklist.md](tools/outreach-checklist.md) | Suivi de pipeline de 50 prospects (markdown + CSV) |

---

## Documentation

| Doc | Couvre |
|---|---|
| [docs/getting-started.md](docs/getting-started.md) | Orientation + le parcours 5 minutes + carte des liens |
| [docs/github-sponsors.md](docs/github-sponsors.md) | Éligibilité, régions (réserve sur la Chine), configuration, paliers, frais, affichage README |
| [docs/open-collective.md](docs/open-collective.md) | Hôtes fiscaux, OSC 501(c)(6), livre comptable public, plans/frais |
| [docs/polar.md](docs/polar.md) | Le pivot vers la facturation IA / MoR — quand c'est adapté vs non |
| [docs/ad-networks.md](docs/ad-networks.md) | EthicalAds, Carbon, BuySellAds, Passionfroot, Paved |
| [docs/affiliate-programs.md](docs/affiliate-programs.md) | Programmes d'affiliation vérifiés + la liste de débunkage + réseaux |
| [docs/pricing.md](docs/pricing.md) | Comment fixer le prix (trafic, pas les étoiles) + grille d'estimation |
| [docs/sponsor-kit.md](docs/sponsor-kit.md) | Construire un sponsor kit (guide) + données GitHub Traffic |
| [docs/readme-monetization.md](docs/readme-monetization.md) | Monétisation README + de chaque surface (tous les emplacements) |
| [docs/outreach.md](docs/outreach.md) | Trouver des sponsors de manière proactive |
| [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md) | Le playbook 1k étoiles en 10 sections |
| [docs/launch-plan.md](docs/launch-plan.md) | Distribution au démarrage à froid (HN/Reddit/PH/V2EX/掘金/X) |
| [docs/case-studies.md](docs/case-studies.md) | Chiffres divulgués et vérifiés (Astro/Vue/Vite/Tailwind/Sentry/…) |
| [docs/faq.md](docs/faq.md) | 15+ Q/R |

Données (source de vérité) : [`data/platforms.yml`](data/platforms.yml) · [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml) · [`data/sponsor-types.yml`](data/sponsor-types.yml) · [`data/affiliate-programs.yml`](data/affiliate-programs.yml).

---

## Ancres d'études de cas réelles

Chiffres divulgués publiquement (cités dans [docs/case-studies.md](docs/case-studies.md)). Estimations marquées.

| Projet | Ce qui est divulgué (source) | Enseignement |
|---|---|---|
| [Astro](https://opencollective.com/astrodotbuild) | $836k au total sur OC ; paliers jusqu'à $10,000/mo | Échelle propre + page sponsor + hôte fiscal = le plafond |
| [Vue.js](https://opencollective.com/vuejs) | $852k au total sur OC | Page sponsor auto-hébergée + BACKERS.md fonctionne |
| [Vite](https://opencollective.com/vite) | $162k au total sur OC ; Bronze $50 → Gold $500 | Une échelle plus simple fonctionne aussi |
| [Homebrew](https://opencollective.com/homebrew) | $486k au total sur OC | Mix en nature (MacStadium/1Password) + cash |
| [Tailwind CSS](https://tailwindcss.com/sponsor) | Partenaire $5,000/mo (est. ~$200k/mo de ~70 sociétés) | Les paliers de sponsoring fonctionnent à l'échelle d'un projet phare ; commercial ≠ sponsoring |
| [Sentry](https://blog.sentry.io) | $155k→$750k/an de décaissement OSS ; engagement $2,000/ingénieur/an | Ce qu'un *sponsor* budgète |
| [Caleb Porzio](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) | $112,680/an sur GitHub Sponsors | Vente active sur une base réelle |
| [komorebi (~10k★)](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) | $1,861/an (~$155/mo) | **10k étoiles ≠ sponsoring sans vente** |

---

## Contribuer

Les corrections et les nouvelles plateformes/programmes sont les bienvenues — **avec une source officielle citée**. Voir [CONTRIBUTING.md](CONTRIBUTING.md). La seule règle : **ne publiez pas de faits non vérifiés** ; marquez `unverified` tout élément incertain plutôt que de deviner.

---

## Historique des étoiles

<a href="https://star-history.com/#irmacardozo993-lgtm/awesome-oss-sponsorship&Date">
  <img src="https://api.star-history.com/svg?repos=irmacardozo993-lgtm/awesome-oss-sponsorship&type=Date" alt="Star History">
</a>

---

## Avertissement

Tous les prix, frais, taux de commission et chiffres de revenus de ce dépôt sont des
**estimations / référence uniquement**. Ce ne sont ni des devis, ni des garanties, ni des
conseils financiers, juridiques ou fiscaux. Les prix réels dépendent du secteur, du trafic,
de la qualité des utilisateurs, du taux de conversion, de la géographie de l'audience et du
budget du sponsor. **Vérifiez les conditions en vigueur auprès de chaque plateforme avant de
vous y fier.** Les statuts des plateformes ont été vérifiés le 2026-06-29 et changent
fréquemment. Ce projet ne promet aucun revenu et n'est pas un système pour « devenir riche »
— c'est un guide de terrain pour les mainteneurs qui veulent gérer le sponsoring de façon
professionnelle.

Licence : [CC-BY-4.0](LICENSE) pour le contenu ; MIT pour les extraits de code intégrés. Voir [LICENSE](LICENSE).
