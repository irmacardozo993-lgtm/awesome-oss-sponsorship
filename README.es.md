<div align="center">

# awesome-oss-sponsorship

**Una guía de campo para conseguir que los proyectos open source cobren — patrocinadores, redes publicitarias, acuerdos de afiliados y el outreach que de verdad cierra.**

Plataformas curadas · anclajes de precios verificados · plantillas para copiar y pegar · casos de estudio reales · un plan de arranque en frío de 7 días.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Made for maintainers](https://img.shields.io/badge/for-100%2B%20%E2%86%92%2010k%2B%20star%20repos-blueviolet)](#para-quién-es-esta-guía)

</div>

🌐 **Languages:** [English](README.md) · [中文](README.zh-CN.md) · [Español](README.es.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

> **El patrocinio es un canal de ventas, no una recompensa por número de estrellas.** Las
> estrellas son un indicador de popularidad — los verdaderos motores del precio son los
> **visitantes únicos mensuales** (GitHub Traffic), las **descargas del paquete** (npm /
> PyPI / Docker Hub) y el **encaje audiencia-patrocinador**. Este repositorio es el
> manual para gestionar ese canal de ventas de forma profesional: qué plataformas, qué
> espacios, a qué precio, a quién escribirle y qué enviar.

Todo lo que encontrarás aquí se puede **copiar y pegar** y se basa en **fuentes públicas
verificadas** (documentación oficial, páginas de OpenCollective, blogs de maintainers,
páginas de precios de redes publicitarias). Todos los precios son **estimaciones / solo
de referencia** — nunca una cotización, nunca una promesa. Consulta
[el aviso legal](#aviso-legal).

---

## Agradecimientos

- **[Telegram OpenClaw 中文社区](https://t.me/OpenClaw_Group)** — la comunidad de OpenClaw en chino en Telegram, por su apoyo y debate.
- **[Linux.do](https://linux.do)** — comunidad de desarrolladores y tecnología en chino (Discourse) cuyos miembros y comentarios dieron forma a la guía de distribución en China de este repositorio.

---

## Tabla de contenidos

- [Para quién es esta guía](#para-quién-es-esta-guía)
- [Inicio rápido (5 minutos)](#inicio-rápido-5-minutos)
- [Si solo tienes 1,000 estrellas](#si-solo-tienes-1000-estrellas)
- [Comparativa de plataformas](#comparativa-de-plataformas)
- [Referencia de precios (estimación)](#referencia-de-precios-estimación)
- [Programas de afiliados que de verdad pagan](#programas-de-afiliados-que-de-verdad-pagan)
- [Cómo encontrar patrocinadores](#cómo-encontrar-patrocinadores)
  - [Canales locales (comunidades en español)](#canales-locales-comunidades-en-español)
- [El plan de arranque en frío de 7 días](#el-plan-de-arranque-en-frío-de-7-días)
- [Plantillas y herramientas](#plantillas-y-herramientas)
- [Documentación](#documentación)
- [Anclas de casos de estudio reales](#anclas-de-casos-de-estudio-reales)
- [Contribuir](#contribuir)
- [Historial de estrellas](#historial-de-estrellas)
- [Aviso legal](#aviso-legal)

---

## Para quién es esta guía

| Tú eres | Empieza aquí |
|---------|-----------|
| **Maintainer con 100 estrellas** (CLI/SDK inicial) | GitHub Sponsors (0% de comisión) + `.github/FUNDING.yml`. Céntrate en el impulso, no en el dinero. → [ejemplo de 100 estrellas](examples/100-stars-repo.md) |
| **Maintainer con 1,000 estrellas** (el punto óptimo) | GitHub Sponsors + Open Collective + una tarifa. Ejecuta el plan de los primeros 50 DMs. → [playbook de 1000 estrellas](docs/1000-stars-playbook.md) · [ejemplo](examples/1000-stars-repo.md) |
| **Maintainer con 10,000 estrellas** | Programa por niveles + página de patrocinador independiente + EthicalAds en la docs. → [ejemplo de 10000 estrellas](examples/10000-stars-repo.md) |
| **Indie / dev en solitario** | GitHub Sponsors (recurrente) + Buy Me a Coffee (propinas puntuales). Sáltate el fiscal host. |
| **Maintainer de Devtool / CLI / SDK** | GitHub Sponsors + thanks.dev (inbound desde el árbol de dependencias) + híbrido de afiliados. |
| **Maintainer que gestiona un newsletter** | GitHub Sponsors + Paved (anuncios en newsletter — mayor $/impresión). |
| **Maintainer que lanza un producto SaaS/AI de pago** | Polar (Merchant-of-Record) — **no** para patrocinio. |

---

## Inicio rápido (5 minutos)

1. **Elige una plataforma.** En solitario → [GitHub Sponsors](docs/github-sponsors.md) (0% de comisión personal). Varios contribuyentes/proveedores → [Open Collective](docs/open-collective.md) (fiscal host + libro contable público).
2. **Añade `.github/FUNDING.yml`.** Activa el botón "Sponsor". Copia la [plantilla anotada](templates/funding-yml-example.md) (12 claves actuales; `otechie`/`givebutter`/`lfx_crowdfunding` **no** están soportadas).
3. **Define los niveles.** GitHub Sponsors: hasta 10 puntuales + 10 mensuales, máximo $12,000/mes; **el precio es inmutable una vez publicado** (retíralo y vuélvelo a crear para cambiarlo). Ancla a escaleras reales — Vite `$5/$15/$50/$150/$500`, Astro `$10/$100/$200/$250/$1,000/$10,000` — pero etiqueta los tuyos como **estimación / solo de referencia**.
4. **Haz un inventario de tus espacios.** Vendes *exposición*, no estrellas. Taxonomía de espacios en [`data/sponsor-types.yml`](data/sponsor-types.yml): banner superior del README, rejilla de logos al pie del README (el patrón dominante — SVG dinámico, nunca edites el README), anuncio en el sitio de docs, release-note, newsletter.
5. **Empieza el outreach.** Construye una [tarifa](templates/rate-card.md) de una página anclada al **tu** tráfico, y envía la plantilla de [cold-email](templates/cold-email.md) a empresas de tu árbol de dependencias o de tus Popular Referrers. Pon precio en el extremo **bajo** hasta que cierres 3 acuerdos.

> El camino de 5 minutos se detalla en [docs/getting-started.md](docs/getting-started.md).

---

## Si solo tienes 1,000 estrellas

1,000 estrellas es el punto óptimo: usuarios reales, descargas reales, conversaciones reales de compras — pero todavía lo bastante cerca del terreno como para venderlo tú mismo. La estrategia completa es el [playbook de 1000 estrellas](docs/1000-stars-playbook.md); lo esencial:

- **Tiene valor comercial** — pero solo si vendes. [komorebi (~10k estrellas) sacó solo ~$155/mes](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) sin ventas; [Caleb Porzio llegó a ~$112,680/año](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) vendiendo activamente sobre una base mayor.
- **Pon precio en el extremo bajo** de la [rejilla de estimación](#referencia-de-precios-estimación); súbelo tras cerrar 3 acuerdos.
- **Lanza un pipeline de 50 prospectos**, puntuado con el [Sponsor Fit Score](tools/sponsor-fit-score.md), con una cadencia de 3 toques y cierre — consulta el [plan de los primeros 50 DMs](examples/1000-stars-repo.md#5-the-first-50-dms-plan).
- **Ofrece una prueba de un mes** al 50% de descuento (o gratis) para eliminar el riesgo de un patrocinador fundador.
- **No dañes el repo.** Una política de revisión + una divulgación limpia de afiliados + sin bombardeo de spam protege la reputación que hace que el repo sea patrocinable en primer lugar.

---

## Comparativa de plataformas

Estados verificados el 2026-06-29 contra sitios oficiales. Las comisiones son **solo de referencia**.

| Plataforma | Tipo | Estado | Comisión (ref.) | Mejor para |
|---|---|---|---|---|
| [GitHub Sponsors](docs/github-sponsors.md) | patrocinio | ✅ activo | 0% personal / ≤6% org | maintainers en solitario; botón nativo de GitHub. ⚠ China continental **no** soportada |
| [Open Collective](docs/open-collective.md) | fiscal host | ✅ activo | plan $0/$60/$320; o 5% | libro contable público; varios contribuyentes |
| Open Source Collective | fiscal host | ✅ activo | vía OC | paraguas 501(c)(6) de EE. UU., deducible de impuestos |
| [Polar](docs/polar.md) | facturación MoR | 🔄 pivotado | 5%+50¢ → 3.40%+30¢ | facturación+impuestos de SaaS/AI de pago. **No es patrocinio** |
| Buy Me a Coffee | donación | ✅ activo | 5% + procesamiento Stripe | propinas puntuales |
| Ko-fi | donación | ⚠ sin verificar | 0% donaciones; Gold ~$12/mes (verificar) | propinas directas vía PayPal/Stripe |
| Patreon | suscripción | ✅ activo | 10% | membresías recurrentes |
| thanks.dev | donación | ✅ activo | 5% | autofinancia tu árbol de dependencias |
| StackAid | donación | ✅ activo | suscripciones desde $15/mes | financia dependencias directas y transitivas |
| Tidelift | suscripción | ❌ adquirida | — | histórico; adquirida por Sonar (dic 2024) |
| IssueHunt | bounty | ⚠ estancado | n/d | bounty sobre issue — usa **oss.issuehunt.io**, verifica disponibilidad |
| Algora | recruiting | 🔄 pivotado | n/d | contratación OSS + bounty lateral |
| [EthicalAds](docs/ad-networks.md) | anuncios (CPM) | ✅ activo | 70% revshare, ~$2.50 CPM | sitios de docs para devs (50k+ pageviews) |
| Carbon Ads | anuncios (CPC) | ✅ activo | asistido por ventas | sitios dev curados ($5–10k mín. anunciante) |
| BuySellAds | anuncios (multi) | ✅ activo | gestionado | email/native/sponsored/podcast |
| Passionfroot | anuncios/marketplace | 🔄 pivotado→Zest | 2% / 15% | acuerdos de marca en newsletters |
| Paved | anuncios (newsletter) | ✅ activo | tarifa plana + PPC | newsletters (25k subs / 1M pv) |

Base de datos estructurada completa: [`data/platforms.yml`](data/platforms.yml).

---

## Referencia de precios (estimación)

> **Estimación / solo de referencia.** **No** existe un mercado público estandarizado que
> vincule $/mes con el número de estrellas. El número de estrellas es un indicador de
> popularidad, no una métrica de precio. Dedúcelo de **tu** tráfico: anuncio en docs ≈
> `monthly_pageviews / 1000 × ~$2.50` (CPM de publisher de EthicalAds); newsletter ≈
> `subs × open_rate × CTR × target_cpc`, anclado a los [JavaScript Weekly's $3,590/issue a
> 180k subs](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf).
> Pon precio en el extremo **bajo** sin datos de tráfico/conversión; súbelo tras cerrar 3 acuerdos.

USD mensual por nivel de estrellas × espacio (estimación):

| Estrellas | Banner superior README | Logo al pie README | Texto al pie README | Anuncio en docs | Release note | Newsletter / issue |
|------:|---:|---:|---:|---:|---:|---:|
| 100 | $100–300 | $50–150 | $20–75 | $10–40 | $50–150 | $30–100 |
| 500 | $200–500 | $100–300 | $50–150 | $25–80 | $100–300 | $100–250 |
| 1,000 | $400–1,000 | $200–600 | $100–300 | $50–200 | $200–600 | $200–500 |
| 5,000 | $1,000–3,000 | $500–1,500 | $250–750 | $150–600 | $500–1,500 | $500–1,500 |
| 10,000 | $2,000–6,000 | $1,000–3,000 | $500–1,500 | $300–1,500 | $1,000–3,000 | $1,000–2,500 |
| 50,000 | $5,000–15,000 | $3,000–10,000 | $1,500–5,000 | $1,000–5,000 | $2,500–8,000 | $2,500–7,000 |

Modificadores del modelo de acuerdo (est.): exhibición de 12 meses puntual ≈ 8–10× mensual (15–20% de descuento); anual ≈ 10–12× mensual (15–20% de descuento); afiliado puro = $0 fijo + 10–30% recurrente; **híbrido fijo + afiliado** = retainer menor + comisión (el mejor modelo). Rejilla completa + banda nacional en RMB en [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml); tarifa para copiar y pegar en [`templates/rate-card.md`](templates/rate-card.md).

---

## Programas de afiliados que de verdad pagan

La mayoría de las empresas de devtools **no** tienen un programa de afiliados público (OpenAI, Anthropic, GitHub, Supabase, Cloudflare, AWS — todos confirmados ausentes). Los que sí tienen, verificados el 2026-06-29:

| Programa | Comisión (ref.) | Cookie | Pago | Encaje |
|---|---|---|---|---|
| [Railway](https://railway.com/affiliate-program) | 15% recurrente, 12 meses | n/d | GitHub Sponsors / BMC | ★★★ efectivo vía Sponsors |
| [Neon](https://neon.com/programs/open-source) | $20 efectivo / referido | n/d | GitHub Sponsors | ★★★ programa OSS |
| [ElevenLabs](https://elevenlabs.io/affiliates) | 22% recurrente, 12 meses | n/d | PartnerStack, $5 | ★★★ voz con IA |
| [Apify](https://apify.com/partners/affiliate) | 20%→30%, tope $2,500/cliente | 45 d | PayPal/banco, $100 | ★★★ scraping |
| [Bright Data](https://brightdata.com/affiliate) | 50% hasta $2,500 + 15% 2º nivel | 90 d | PartnerStack | ★★★ proxies |
| [ScrapingBee](https://www.scrapingbee.com/affiliates/) | 25% recurrente de por vida | n/d | PayPal, $50 | ★★★ scraping |
| [Browserless](https://www.browserless.io/affiliate) | 20–30% por niveles, 12 meses | 90 d | PayPal/banco, $50 | ★★★ navegador headless |
| [n8n](https://n8n.io/affiliates/) | 30% recurrente, 12 meses (Cloud) | n/d | PayPal, €100 | ★★★ automatización |
| [Make](https://www.make.com/en/affiliate) | 35% recurrente, 12 meses | 30 d | Wise, $100 | ★★ automatización |
| [Raycast](https://www.raycast.com/blog/affiliate-program) | 30% recurrente (Pro) | n/d | Wise, £50 | ★★ macOS |
| [Pluralsight](https://www.pluralsight.com/affiliate) | $1/trial + 30%/10%/5% puntual | 7 d | CJ | ★★ aprendizaje dev |
| [DigitalOcean](https://www.digitalocean.com/affiliates) | 10% recurrente, 12 meses | n/d | Awin/CJ | ★★ hosting |
| [Netlify](https://www.netlify.com/partners/) | 20% recurrente, 12–24 meses | n/d | PartnerStack | ★★ Jamstack |
| [Vercel / v0](https://partners.dub.co/v0) | 30% recurrente, 6 meses + $5/lead | n/d | Dub | ★★ frontend |

Cerrados/muertos: Hetzner (cerrado 2026-06-15), Notion (cerrado a nuevos), ShareASale (difunto→Awin), Heroku (muerto).
Redes a las que unirse como publisher: **PartnerStack** (mejor densidad de devtools, mín. $5) e **Impact** (amplia, mín. $10). Base de datos completa + la lista de de-bunk "no se ha encontrado programa" en [`data/affiliate-programs.yml`](data/affiliate-programs.yml) y [docs/affiliate-programs.md](docs/affiliate-programs.md).

---

## Cómo encontrar patrocinadores

No dispares a ciegas. Construye una lista puntuada de 50 prospectos. Fuentes prioritarias (método completo en [docs/outreach.md](docs/outreach.md)):

1. **Empresas de tu árbol de dependencias** — ¿quién publica software que *usa* tu proyecto? Sus equipos de DevRel/growth son los mejores encajes.
2. **Stargazers/forkers que son empresas** — organizaciones de GitHub que te marcan con estrella o hacen fork; encuentra el contacto de DevRel/fundador/growth vía LinkedIn/X.
3. **Proveedores adyacentes** — productos que se despliegan *con* el tuyo (hosting, ORM, observabilidad, CI).
4. **Patrocinadores en especie** — proveedores de hosting/CI/secrets/monitoring que intercambian créditos por un logo (patrón Homebrew: MacStadium, 1Password).
5. **Reporters de issues power-users** — pídeles que te presenten a su empresa.

Puntúa cada prospecto con el [Sponsor Fit Score](tools/sponsor-fit-score.md) (0–100). Persigue **61–100**; descarta **0–30**. Envía las plantillas de [cold-email](templates/cold-email.md) / [DM](templates/dm-template.md) con una cadencia de 3 toques y cierre. Haz seguimiento de todo en la [checklist de outreach](tools/outreach-checklist.md).

### Canales locales (comunidades en español)

> **Solo de referencia.** Espacios y comunidades en español para dar a conocer tu proyecto
> y construir la audiencia que los patrocinadores compran; verifica la actualidad de cada
> comunidad antes de participar.

- **Dev.to y Medium (etiquetas en español):** publica contenido técnico de valor primero —tutoriales, comparativas, lecciones aprendidas— en español; el tráfico orgánico hacia tu repo construye la audiencia que los patrocinadores acaban comprando.
- **Grupos regionales de Telegram y Discord:** comunidades de desarrolladores de España y Latinoamérica; participa de forma genuina (resuelve dudas, comparte releases) antes de pedir nada.
- **Conferencias técnicas de Latinoamérica y España:** espacio para presentar tu proyecto y conversar con equipos de DevRel; muchas empresas LATAM patrocinan OSS desde presupuestos de developer relations.
- **Enfoque value-first en español:** crea contenido que resuelva problemas reales de la comunidad hispanohablante antes de hacer outreach; la audiencia en español está menos saturada que la anglófona.

---

## El plan de arranque en frío de 7 días

Una semana para pasar de "sin programa de patrocinio" a "primeros pitches enviados + repo lanzado". Cada día es una checklist en [docs/launch-plan.md](docs/launch-plan.md) y [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md).

| Día | Haz esto | Resultado |
|---|---|---|
| **1** | Elige plataforma; añade `.github/FUNDING.yml`; define 3–5 niveles (extremo bajo) | Botón Sponsor activo + escalera de niveles |
| **2** | Lista los espacios de inventario; construye una [tarifa](templates/rate-card.md) de una página | Tarifa (ancla interna) |
| **3** | Extrae GitHub Traffic + descargas de npm/PyPI/Docker; construye un [sponsor kit](templates/sponsor-kit.md) de una página | Kit con la salvedad de tráfico autoinformado |
| **4** | Construye una lista de 50 prospectos (árbol de dependencias, orgs stargazers, proveedores adyacentes); puntúa con el [Sponsor Fit Score](tools/sponsor-fit-score.md) | Lista de prospectos puntuada |
| **5** | Envía la oleada 1 (10 prospectos) vía [cold-email](templates/cold-email.md) / [DM](templates/dm-template.md) | 10 salidas, con seguimiento |
| **6** | Envía la oleada 2 (10); redacta los posts de lanzamiento (HN / Reddit / V2EX / X) | Recursos de lanzamiento listos |
| **7** | Lanza + publica una página de patrocinador independiente; registra todo en la [checklist de outreach](tools/outreach-checklist.md) | Repo en vivo, pipeline en marcha |

Tras el día 7: mantén el pipeline rotativo de 50 prospectos, ejecuta cadencias de 3 toques y sostén las actualizaciones para un crecimiento orgánico de estrellas (consulta [docs/launch-plan.md](docs/launch-plan.md) §12).

---

## Plantillas y herramientas

Copia y pega, rellena los `[brackets]`, publica.

| Archivo | Qué es |
|---|---|
| [templates/funding-yml-example.md](templates/funding-yml-example.md) | `.github/FUNDING.yml` anotado — las 12 claves, 3 ejemplos completos |
| [templates/rate-card.md](templates/rate-card.md) | Tarifa de una página (USD + RMB, rejilla nivel de estrellas × espacio) |
| [templates/cold-email.md](templates/cold-email.md) | Cold email + follow-ups + respuestas de sí/no (EN + chino) |
| [templates/dm-template.md](templates/dm-template.md) | DMs para LinkedIn / X / Discord / 微信 / V2EX-掘金 |
| [templates/sponsor-kit.md](templates/sponsor-kit.md) | Sponsor kit completo (plantilla + ejemplo resuelto) |
| [templates/media-kit.md](templates/media-kit.md) | Media kit estilo TLDR (todos los componentes + ejemplo) |
| [templates/readme-sponsor-block.md](templates/readme-sponsor-block.md) | Snippets de README superior/inferior/logo/texto/afiliados |
| [templates/affiliate-tracker.csv](templates/affiliate-tracker.csv) | CSV para hacer seguimiento de acuerdos de afiliados |
| [tools/sponsor-fit-score.md](tools/sponsor-fit-score.md) | Modelo de puntuación de prospectos 0–100 + ejemplo resuelto |
| [tools/outreach-checklist.md](tools/outreach-checklist.md) | Tracker de pipeline de 50 prospectos (markdown + CSV) |

---

## Documentación

| Doc | Cubre |
|---|---|
| [docs/getting-started.md](docs/getting-started.md) | Orientación + el camino de 5 minutos + mapa de enlaces |
| [docs/github-sponsors.md](docs/github-sponsors.md) | Elegibilidad, regiones (caveat de China), configuración, niveles, comisiones, exhibición en README |
| [docs/open-collective.md](docs/open-collective.md) | Fiscal hosts, OSC 501(c)(6), libro contable público, planes/comisiones |
| [docs/polar.md](docs/polar.md) | El pivot a facturación de IA / MoR — cuándo encaja y cuándo no |
| [docs/ad-networks.md](docs/ad-networks.md) | EthicalAds, Carbon, BuySellAds, Passionfroot, Paved |
| [docs/affiliate-programs.md](docs/affiliate-programs.md) | Programas de afiliados verificados + la lista de de-bunk + redes |
| [docs/pricing.md](docs/pricing.md) | Cómo poner precio (tráfico, no estrellas) + rejilla de estimación |
| [docs/sponsor-kit.md](docs/sponsor-kit.md) | Cómo construir un sponsor kit (guía) + datos de GitHub Traffic |
| [docs/readme-monetization.md](docs/readme-monetization.md) | Monetización del README + de cada superficie (todos los espacios) |
| [docs/outreach.md](docs/outreach.md) | Cómo encontrar patrocinadores de forma proactiva |
| [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md) | El playbook de 10 secciones para 1k estrellas |
| [docs/launch-plan.md](docs/launch-plan.md) | Distribución de arranque en frío (HN/Reddit/PH/V2EX/掘金/X) |
| [docs/case-studies.md](docs/case-studies.md) | Cifras divulgadas y verificadas (Astro/Vue/Vite/Tailwind/Sentry/…) |
| [docs/faq.md](docs/faq.md) | 15+ preguntas y respuestas |

Datos (fuente de verdad): [`data/platforms.yml`](data/platforms.yml) · [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml) · [`data/sponsor-types.yml`](data/sponsor-types.yml) · [`data/affiliate-programs.yml`](data/affiliate-programs.yml).

---

## Anclas de casos de estudio reales

Cifras divulgadas públicamente (citadas en [docs/case-studies.md](docs/case-studies.md)). Las estimaciones van marcadas.

| Proyecto | Lo divulgado (fuente) | Conclusión |
|---|---|---|
| [Astro](https://opencollective.com/astrodotbuild) | $836k acumulado en OC; niveles hasta $10,000/mes | Escalera limpia + página de patrocinador + fiscal host = el techo |
| [Vue.js](https://opencollective.com/vuejs) | $852k acumulado en OC | Página de patrocinador self-hosted + BACKERS.md funciona |
| [Vite](https://opencollective.com/vite) | $162k acumulado en OC; Bronze $50 → Gold $500 | Una escalera más simple también funciona |
| [Homebrew](https://opencollective.com/homebrew) | $486k acumulado en OC | Mezcla en especie (MacStadium/1Password) + efectivo |
| [Tailwind CSS](https://tailwindcss.com/sponsor) | Partner $5,000/mes (est. ~$200k/mes de ~70 empresas) | Los niveles de patrocinio funcionan a escala insignia; comercial ≠ patrocinio |
| [Sentry](https://blog.sentry.io) | $155k→$750k/año de desembolso en OSS; compromiso de $2,000/ingeniero/año | Lo que presupuesta un *patrocinador* |
| [Caleb Porzio](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) | $112,680/año en GitHub Sponsors | Venta activa sobre una base real |
| [komorebi (~10k★)](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) | $1,861/año (~$155/mes) | **10k estrellas ≠ patrocinio sin ventas** |

---

## Contribuir

Se aceptan correcciones y nuevas plataformas/programas — **con una fuente oficial citada**. Consulta [CONTRIBUTING.md](CONTRIBUTING.md). La única regla: **no publiques datos sin verificar**; marca como `unverified` cualquier cosa incierta en lugar de adivinar.

---

## Historial de estrellas

<a href="https://star-history.com/#irmacardozo993-lgtm/awesome-oss-sponsorship&Date">
  <img src="https://api.star-history.com/svg?repos=irmacardozo993-lgtm/awesome-oss-sponsorship&type=Date" alt="Star History">
</a>

---

## Aviso legal

Todos los precios, comisiones, tasas de comisión y cifras de ingresos de este repositorio son
**estimaciones / solo de referencia**. No son cotizaciones, ni garantías, ni asesoramiento
financiero, legal ni fiscal. Los precios reales dependen del sector, el tráfico, la calidad
de los usuarios, la tasa de conversión, la geografía de la audiencia y el presupuesto del
patrocinador. **Verifica las condiciones vigentes con cada plataforma antes de fiarte de
ellas.** Los estados de las plataformas se comprobaron el 2026-06-29 y cambian con
frecuencia. Este proyecto no promete ningún ingreso y no es ningún esquema de "enriquecimiento
rápido" — es una guía de campo para maintainers que quieren gestionar el patrocinio de forma
profesional.

Licencia: [CC-BY-4.0](LICENSE) para el contenido; MIT para los fragmentos de código embebidos. Consulta [LICENSE](LICENSE).
