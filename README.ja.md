<div align="center">

# awesome-oss-sponsorship

**オープンソースプロジェクトを収益化するための実践ガイド — スポンサー、広告ネットワーク、アフィリエイト契約、そして実際に成約につなげるアウトリーチ。**

キュレーションされたプラットフォーム · 検証済みの価格アンカー · コピペテンプレート · 実際の事例 · 7日間のコールドスタート計画。

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Made for maintainers](https://img.shields.io/badge/for-100%2B%20%E2%86%92%2010k%2B%20star%20repos-blueviolet)](#対象読者)

</div>

🌐 **Languages:** [English](README.md) · [中文](README.zh-CN.md) · [Español](README.es.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

> **スポンサーシップは営業チャネルであり、スター数への報酬ではない。** スターは人気の
> 代用指標にすぎない — 本当の価格ドライバーは **月間ユニーク訪問者数**（GitHub Traffic）、
> **パッケージダウンロード数**（npm / PyPI / Docker Hub）、そして **視聴者とスポンサーの適合度** だ。
> このリポジトリは、その営業チャネルをプロフェッショナルに運営するためのプレイブックだ：どの
> プラットフォーム、どの枠、いくらで、誰にメッセージし、何を送るか。

ここにあるものはすべて **コピペ可能** で、**検証済みの公開ソース**（公式ドキュメント、
OpenCollective のページ、メンテナーのブログ、広告ネットワークの価格ページ）に基づいている。価格はすべて
**推定 / 参考のみ** であり、見積もりでも約束でもない。[免責事項](#免責事項)を参照のこと。

---

## 目次

- [対象読者](#対象読者)
- [クイックスタート（5分）](#クイックスタート5分)
- [スター数が1,000しかない場合](#スター数が1000しかない場合)
- [プラットフォーム比較](#プラットフォーム比較)
- [料金の目安（推定）](#料金の目安推定)
- [実際に報酬が支払われるアフィリエイトプログラム](#実際に報酬が支払われるアフィリエイトプログラム)
- [スポンサーの見つけ方](#スポンサーの見つけ方)
- [7日間のコールドスタート計画](#7日間のコールドスタート計画)
- [テンプレートとツール](#テンプレートとツール)
- [ドキュメント](#ドキュメント)
- [実際の事例アンカー](#実際の事例アンカー)
- [コントリビュート](#コントリビュート)
- [Star History](#star-history)
- [免責事項](#免責事項)

---

## 対象読者

| あなたが | ここから始める |
|---------|-----------|
| **100スターのメンテナー**（初期のCLI/SDK） | GitHub Sponsors（手数料0%）+ `.github/FUNDING.yml`。金銭ではなく勢いに注力。→ [100スターの事例](examples/100-stars-repo.md) |
| **1,000スターのメンテナー**（最適なスポット） | GitHub Sponsors + Open Collective + レートカード。最初の50件DM計画を実行。→ [1000スターのプレイブック](docs/1000-stars-playbook.md) · [事例](examples/1000-stars-repo.md) |
| **10,000スターのメンテナー** | 段階制プログラム + 独立したスポンサーページ + ドキュメントの EthicalAds。→ [10000スターの事例](examples/10000-stars-repo.md) |
| **インディー / 個人開発者** | GitHub Sponsors（継続）+ Buy Me a Coffee（単発のチップ）。フィスカルホストは不要。 |
| **開発者ツール / CLI / SDK メンテナー** | GitHub Sponsors + thanks.dev（依存ツリーからの流入）+ アフィリエイトのハイブリッド。 |
| **ニュースレターを運営するメンテナー** | GitHub Sponsors + Paved（ニュースレター広告 — インプレッション単価が最も高い）。 |
| **有料の SaaS/AI プロダクトを出荷するメンテナー** | Polar（Merchant-of-Record）— スポンサーシップには**不適切**。 |

---

## クイックスタート（5分）

1. **プラットフォームを選ぶ。** 個人 → [GitHub Sponsors](docs/github-sponsors.md)（個人手数料0%）。複数のコントリビューター/ベンダー → [Open Collective](docs/open-collective.md)（フィスカルホスト + 公開台帳）。
2. **`.github/FUNDING.yml` を追加する。** 「Sponsor」ボタンを有効化する。[注釈付きテンプレート](templates/funding-yml-example.md)をコピー（現在12個のキーに対応。`otechie`/`givebutter`/`lfx_crowdfunding` は**サポート対象外**）。
3. **ティアを設定する。** GitHub Sponsors：最大10個の単発 + 10個の月額、月額上限 $12,000。**価格は一度公開すると変更不可**（変更するには廃止して作り直す）。実際の階層にアンカーする — Vite `$5/$15/$50/$150/$500`、Astro `$10/$100/$200/$250/$1,000/$10,000` — ただし自分のティアは **推定 / 参考のみ** と明記すること。
4. **在庫をリストアップする。** 売るのはスターではなく*露出*だ。[`data/sponsor-types.yml`](data/sponsor-types.yml) のスロット分類：README 上部バナー、README 下部のロゴグリッド（主流のパターン — 動的 SVG で README は直接編集しない）、ドキュメントサイトの広告、リリースノート、ニュースレター。
5. **アウトリーチを始める。** 1ページの[レートカード](templates/rate-card.md)を**自分の**トラフィックにアンカーして作成し、依存ツリーや Popular Referrers にある企業に[コールドメール](templates/cold-email.md)テンプレートを送る。3件成約するまでは**下限**価格で勝負する。

> 5分間の手順は [docs/getting-started.md](docs/getting-started.md) で詳しく解説している。

---

## スター数が1,000しかない場合

1,000スターは最適なスポットだ：本物のユーザー、本物のダウンロード、本物の調達の会話がある — それでいて、自分で直接売れるほど現場に近い。完全な戦略は [1000スターのプレイブック](docs/1000-stars-playbook.md) に譲るとして、要点は以下の通り：

- **商業的な価値はある** — ただし売る場合に限る。[komorebi（~10kスター）は売上活動なしで月わずか ~$155](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) しか得られなかった一方、[Caleb Porzio はより大きな足場で積極的に売り、~$112,680/yr に達した](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it)。
- [推定グリッド](#料金の目安推定)の**下限**で価格設定し、3件成約後に引き上げる。
- [Sponsor Fit Score](tools/sponsor-fit-score.md) でスコアリングした **50件のプロスペクトパイプライン** を、3回接触してクローズするリズムで回す — [最初の50件DM計画](examples/1000-stars-repo.md#5-the-first-50-dms-plan) を参照。
- 初月を50%オフ（または無料）のテストとして提供し、初期スポンサーのリスクを取り除く。
- **リポジトリを傷つけない。** 審査ポリシー + クリーンなアフィリエイト開示 + スパム送信なし が、そもそもそのリポジトリをスポンサー可能にする評判を守る。

---

## プラットフォーム比較

ステータスは 2026-06-29 時点で公式サイトに照らして検証済み。手数料は**参考のみ**。

| プラットフォーム | 種別 | ステータス | 手数料（参考のみ） | 向いている用途 |
|---|---|---|---|---|
| [GitHub Sponsors](docs/github-sponsors.md) | スポンサーシップ | ✅ 稼働中 | 個人 0% / 組織 ≤6% | 個人メンテナー；GitHub ネイティブのボタン。⚠ 中国本土は**サポート対象外** |
| [Open Collective](docs/open-collective.md) | フィスカルホスト | ✅ 稼働中 | $0/$60/$320 プラン、または 5% | 公開台帳；複数のコントリビューター |
| Open Source Collective | フィスカルホスト | ✅ 稼働中 | OC 経由 | 米国 501(c)(6) の傘下団体、寄付控除対象 |
| [Polar](docs/polar.md) | 決済 MoR | 🔄 ピボット済み | 5%+50¢ → 3.40%+30¢ | 有料 SaaS/AI の決済+税。**スポンサーシップではない** |
| Buy Me a Coffee | 寄付 | ✅ 稼働中 | 5% + Stripe 処理料 | 単発のチップ |
| Ko-fi | 寄付 | ⚠ 未検証 | 寄付 0%；Gold ~$12/mo（要確認） | PayPal/Stripe への直接チップ |
| Patreon | サブスクリプション | ✅ 稼働中 | 10% | 継続メンバーシップ |
| thanks.dev | 寄付 | ✅ 稼働中 | 5% | 依存ツリーを自動支援 |
| StackAid | 寄付 | ✅ 稼働中 | $15/mo からのサブスク | 直接依存と推移的依存を支援 |
| Tidelift | サブスクリプション | ❌ 買収済み | — | 過去の情報；Sonar に買収（2024年12月） |
| IssueHunt | バウンティ | ⚠ 停滞中 | n/d | イシュー単位のバウンティ — **oss.issuehunt.io** を使用、稼働状況は要確認 |
| Algora | リクルーティング | 🔄 ピボット済み | n/d | OSS 採用 + バウンティサイドバー |
| [EthicalAds](docs/ad-networks.md) | 広告（CPM） | ✅ 稼働中 | 70% 収益分配、~$2.50 CPM | 開発者向けドキュメントサイト（5万 PV 以上） |
| Carbon Ads | 広告（CPC） | ✅ 稼働中 | 営業支援型 | キュレーションされた開発者向けサイト（広告主最低 $5–10k） |
| BuySellAds | 広告（複合） | ✅ 稼働中 | 管理型 | メール/ネイティブ/スポンサー/ポッドキャスト |
| Passionfroot | 広告/マーケットプレイス | 🔄 ピボット済み→Zest | 2% / 15% | ニュースレターのブランド契約 |
| Paved | 広告（ニュースレター） | ✅ 稼働中 | 固定 + PPC | ニュースレター（25k 登録 / 1M PV） |

構造化された完全な DB：[`data/platforms.yml`](data/platforms.yml)。

---

## 料金の目安（推定）

> **推定 / 参考のみ。** $/月 をスター数に結びつける標準化された公開市場は**存在しない**。
> スター数は人気の代用指標であり、価格指標ではない。**自分の**トラフィックから再導出すること：
> ドキュメント広告 ≈ `monthly_pageviews / 1000 × ~$2.50`（EthicalAds のパブリッシャー CPM）、
> ニュースレター ≈ `subs × open_rate × CTR × target_cpc`、
> [JavaScript Weekly の 180k 登録で $3,590/号](https://cooperpress.com/files/cooperpress-media-kit-q2-2024.pdf)
> にアンカー。トラフィック/コンバージョンデータがない間は**下限**で価格設定し、3件成約後に引き上げる。

スター段階 × スロットごとの月額 USD（推定）：

| スター数 | README 上部バナー | README 下部ロゴ | README 下部テキスト | ドキュメント広告 | リリースノート | ニュースレター / 号 |
|------:|---:|---:|---:|---:|---:|---:|
| 100 | $100–300 | $50–150 | $20–75 | $10–40 | $50–150 | $30–100 |
| 500 | $200–500 | $100–300 | $50–150 | $25–80 | $100–300 | $100–250 |
| 1,000 | $400–1,000 | $200–600 | $100–300 | $50–200 | $200–600 | $200–500 |
| 5,000 | $1,000–3,000 | $500–1,500 | $250–750 | $150–600 | $500–1,500 | $500–1,500 |
| 10,000 | $2,000–6,000 | $1,000–3,000 | $500–1,500 | $300–1,500 | $1,000–3,000 | $1,000–2,500 |
| 50,000 | $5,000–15,000 | $3,000–10,000 | $1,500–5,000 | $1,000–5,000 | $2,500–8,000 | $2,500–7,000 |

取引モデルの修飾子（推定）：12ヶ月一括表示 ≈ 月額の 8–10倍（15–20%割引）、年契約 ≈ 月額の 10–12倍（15–20%割引）、純アフィリエイト = 固定 $0 + 10–30% の継続、**固定 + アフィリエイトのハイブリッド** = 低めの固定報酬 + コミッション（最良のモデル）。完全なグリッドと中国国内（RMB）バンドは [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml) に、コピペ用レートカードは [`templates/rate-card.md`](templates/rate-card.md) にある。

---

## 実際に報酬が支払われるアフィリエイトプログラム

ほとんどの開発者ツール企業には公開されたアフィリエイトプログラムが**ない**（OpenAI、Anthropic、GitHub、Supabase、Cloudflare、AWS — いずれも不在を確認済み）。存在するもの（2026-06-29 検証済み）：

| プログラム | 報酬（参考） | Cookie | 支払 | 向き |
|---|---|---|---|---|
| [Railway](https://railway.com/affiliate-program) | 15% 継続、12ヶ月 | n/d | GitHub Sponsors / BMC | ★★★ Sponsors 経由の現金 |
| [Neon](https://neon.com/programs/open-source) | $20 現金 / 紹介 | n/d | GitHub Sponsors | ★★★ OSS プログラム |
| [ElevenLabs](https://elevenlabs.io/affiliates) | 22% 継続、12ヶ月 | n/d | PartnerStack, $5 | ★★★ AI 音声 |
| [Apify](https://apify.com/partners/affiliate) | 20%→30%、上限 $2,500/顧客 | 45日 | PayPal/銀行, $100 | ★★★ スクレイピング |
| [Bright Data](https://brightdata.com/affiliate) | 50%（上限 $2,500）+ 15% の2段階 | 90日 | PartnerStack | ★★★ プロキシ |
| [ScrapingBee](https://www.scrapingbee.com/affiliates/) | 25% 終身継続 | n/d | PayPal, $50 | ★★★ スクレイピング |
| [Browserless](https://www.browserless.io/affiliate) | 20–30% 段階、12ヶ月 | 90日 | PayPal/銀行, $50 | ★★★ ヘッドレスブラウザ |
| [n8n](https://n8n.io/affiliates/) | 30% 継続、12ヶ月（Cloud） | n/d | PayPal, €100 | ★★★ オートメーション |
| [Make](https://www.make.com/en/affiliate) | 35% 継続、12ヶ月 | 30日 | Wise, $100 | ★★ オートメーション |
| [Raycast](https://www.raycast.com/blog/affiliate-program) | 30% 継続（Pro） | n/d | Wise, £50 | ★★ macOS |
| [Pluralsight](https://www.pluralsight.com/affiliate) | $1/トライアル + 30%/10%/5% 単発 | 7日 | CJ | ★★ 開発者学習 |
| [DigitalOcean](https://www.digitalocean.com/affiliates) | 10% 継続、12ヶ月 | n/d | Awin/CJ | ★★ ホスティング |
| [Netlify](https://www.netlify.com/partners/) | 20% 継続、12–24ヶ月 | n/d | PartnerStack | ★★ Jamstack |
| [Vercel / v0](https://partners.dub.co/v0) | 30% 継続、6ヶ月 + $5/リード | n/d | Dub | ★★ フロントエンド |

終了/廃止：Hetzner（2026-06-15 終了）、Notion（新規受付終了）、ShareASale（廃止→Awin）、Heroku（廃止）。
パブリッシャーとして参加すべきネットワーク：**PartnerStack**（開発者ツール密度が最も高い、最低 $5）と **Impact**（幅広い、最低 $10）。完全な DB と「プログラム不在」の否認リストは [`data/affiliate-programs.yml`](data/affiliate-programs.yml) と [docs/affiliate-programs.md](docs/affiliate-programs.md) にある。

---

## スポンサーの見つけ方

手当たり次第にばらまかない。スコアリングした50件のプロスペクトリストを作る。優先ソース（完全な手法は [docs/outreach.md](docs/outreach.md) に）：

1. **依存ツリー内の企業** — あなたのプロジェクトを*利用する*ソフトウェアを出荷しているのは誰か？彼らの DevRel/グロースチームが最適。
2. **スター/フォークしている企業** — あなたにスター/フォークする GitHub org。LinkedIn/X 経由で DevRel/創業者/グロースの連絡先を探す。
3. **隣接するベンダー** — あなたのプロダクトと*一緒に*デプロイされる製品（ホスティング、ORM、可観測性、CI）。
4. **現物スポンサー** — クレジットと引き換えにロゴを掲載するホスティング/CI/シークレット/モニタリングベンダー（Homebrew のパターン：MacStadium、1Password）。
5. **パワーユーザーのイシュー報告者** — 彼らに雇用主への紹介を頼む。

すべてのプロスペクトを [Sponsor Fit Score](tools/sponsor-fit-score.md)（0–100）でスコアリングする。**61–100** を追跡し、**0–30** はスキップ。[コールドメール](templates/cold-email.md) / [DM](templates/dm-template.md) テンプレートを、3回接触してクローズするリズムで送る。すべてを [アウトリーチチェックリスト](tools/outreach-checklist.md) で追跡する。

### ローカルチャンネル（日本）

日本の開発者コミュニティとスポンサー獲得の参考チャンネル（参考のみ / 実際の条件は各社へ確認のこと）：

- **Qiita / Zenn** — 技術記事を執筆して認知を高める。スポンサー獲得の入り口として有効。
- **はてなブックマーク** — 技術記事の拡散経路として活用できる。
- **X / Twitter Japan** — メンテナーや企業の DevRel と直接つながれる。
- **GitHub Sponsors** — 日本をサポートしており、国内の個人スポンサーも利用可能。
- **DevRel チームを擁する日本企業** — スポンサー先としてアプローチ可能。

---

## 7日間のコールドスタート計画

「スポンサープログラムなし」から「最初のピッチ送信 + リポジトリ公開」までの1週間。各日は [docs/launch-plan.md](docs/launch-plan.md) と [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md) のチェックリスト。

| 日 | やること | 成果物 |
|---|---|---|
| **1** | プラットフォーム選定、`.github/FUNDING.yml` 追加、3–5ティア設定（下限） | 稼働中の Sponsor ボタン + ティア段階 |
| **2** | 在庫スロットをリスト化、1ページの[レートカード](templates/rate-card.md)を作成 | レートカード（社内アンカー） |
| **3** | GitHub Traffic + npm/PyPI/Docker のダウンロードを取得、1ページの[スポンサーキット](templates/sponsor-kit.md)を作成 | キット（自己申告トラフィックの注意書き付き） |
| **4** | 50件のプロスペクトリストを作成（依存ツリー、スター org、隣接ベンダー）、[Sponsor Fit Score](tools/sponsor-fit-score.md) でスコアリング | スコア済みプロスペクトリスト |
| **5** | [コールドメール](templates/cold-email.md) / [DM](templates/dm-template.md) で第1波（10件）を送信 | 10件の送信（追跡済み） |
| **6** | 第2波（10件）を送信、公開用投稿を起草（HN / Reddit / V2EX / X） | 公開アセット準備完了 |
| **7** | 公開 + 独立したスポンサーページを公開、すべてを [アウトリーチチェックリスト](tools/outreach-checklist.md) に記録 | リポジトリ公開、パイプライン稼働 |

7日目以降：50件のローリングプロスペクトパイプラインを維持し、3回接触のリズムを回し、オーガニックなスター成長のためにアップデートを継続する（[docs/launch-plan.md](docs/launch-plan.md) §12 参照）。

---

## テンプレートとツール

コピペして、`[brackets]` を埋めて、リリースする。

| ファイル | 内容 |
|---|---|
| [templates/funding-yml-example.md](templates/funding-yml-example.md) | 注釈付き `.github/FUNDING.yml` — 全12キー、完全例3つ |
| [templates/rate-card.md](templates/rate-card.md) | 1ページのレートカード（USD + RMB、スター段階 × スロットグリッド） |
| [templates/cold-email.md](templates/cold-email.md) | コールドメール + フォローアップ + yes/no 返信（EN + 中国語） |
| [templates/dm-template.md](templates/dm-template.md) | LinkedIn / X / Discord / WeChat / V2EX-掘金 DM |
| [templates/sponsor-kit.md](templates/sponsor-kit.md) | 完全なスポンサーキット（穴埋め + 実例） |
| [templates/media-kit.md](templates/media-kit.md) | TLDR 風のメディアキット（全構成要素 + 実例） |
| [templates/readme-sponsor-block.md](templates/readme-sponsor-block.md) | README の上部/下部/ロゴ/テキスト/アフィリエイトのスニペット |
| [templates/affiliate-tracker.csv](templates/affiliate-tracker.csv) | アフィリエイト契約を追跡する CSV |
| [tools/sponsor-fit-score.md](tools/sponsor-fit-score.md) | 0–100 のプロスペクトスコアリングモデル + 実例 |
| [tools/outreach-checklist.md](tools/outreach-checklist.md) | 50件プロスペクトパイプラインのトラッカー（markdown + CSV） |

---

## ドキュメント

| ドキュメント | 対象 |
|---|---|
| [docs/getting-started.md](docs/getting-started.md) | オリエンテーション + 5分間の手順 + リンクマップ |
| [docs/github-sponsors.md](docs/github-sponsors.md) | 適格条件、地域（中国の注意点）、セットアップ、ティア、手数料、README 表示 |
| [docs/open-collective.md](docs/open-collective.md) | フィスカルホスト、OSC 501(c)(6)、公開台帳、プラン/手数料 |
| [docs/polar.md](docs/polar.md) | AI 決済 / MoR へのピボット — 適する場合とそうでない場合 |
| [docs/ad-networks.md](docs/ad-networks.md) | EthicalAds、Carbon、BuySellAds、Passionfroot、Paved |
| [docs/affiliate-programs.md](docs/affiliate-programs.md) | 検証済みアフィリエイトプログラム + 否認リスト + ネットワーク |
| [docs/pricing.md](docs/pricing.md) | 価格の付け方（スターではなくトラフィック）+ 推定グリッド |
| [docs/sponsor-kit.md](docs/sponsor-kit.md) | スポンサーキットの作成（ガイド）+ GitHub Traffic の事実 |
| [docs/readme-monetization.md](docs/readme-monetization.md) | README + 表面の収益化（全スロット） |
| [docs/outreach.md](docs/outreach.md) | スポンサーを能動的に見つける |
| [docs/1000-stars-playbook.md](docs/1000-stars-playbook.md) | 10セクションの 1k スタープレイブック |
| [docs/launch-plan.md](docs/launch-plan.md) | コールドスタートの配信（HN/Reddit/PH/V2EX/掘金/X） |
| [docs/case-studies.md](docs/case-studies.md) | 検証済みの公開数値（Astro/Vue/Vite/Tailwind/Sentry/…） |
| [docs/faq.md](docs/faq.md) | 15以上の Q&A |

データ（情報源）：[`data/platforms.yml`](data/platforms.yml) · [`data/pricing-benchmarks.yml`](data/pricing-benchmarks.yml) · [`data/sponsor-types.yml`](data/sponsor-types.yml) · [`data/affiliate-programs.yml`](data/affiliate-programs.yml)。

🌐 **Languages:** [English](README.md) · [中文](README.zh-CN.md) · [Español](README.es.md) · [日本語](README.ja.md) · [Français](README.fr.md) · [Deutsch](README.de.md)

---

## 実際の事例アンカー

公開されている数値（[docs/case-studies.md](docs/case-studies.md) で引用）。推定には明示あり。

| プロジェクト | 公開されている内容（ソース） | 示唆 |
|---|---|---|
| [Astro](https://opencollective.com/astrodotbuild) | OC で累計 $836k、ティアは $10,000/mo まで | クリーンな階層 + スポンサーページ + フィスカルホスト = 上限 |
| [Vue.js](https://opencollective.com/vuejs) | OC で累計 $852k | 自己ホストのスポンサーページ + BACKERS.md が機能する |
| [Vite](https://opencollective.com/vite) | OC で累計 $162k、Bronze $50 → Gold $500 | よりシンプルな階層でも機能する |
| [Homebrew](https://opencollective.com/homebrew) | OC で累計 $486k | 現物（MacStadium/1Password）+ 現金のミックス |
| [Tailwind CSS](https://tailwindcss.com/sponsor) | Partner $5,000/mo（~70社から ~$200k/mo と推定） | スポンサーシップティアは旗艦規模で機能、商用 ≠ スポンサーシップ |
| [Sentry](https://blog.sentry.io) | $155k→$750k/yr の OSS 支出、$2,000/エンジニア/yr の誓約 | *スポンサー*の予算感 |
| [Caleb Porzio](https://calebporzio.com/i-just-hit-dollar-100000yr-on-github-sponsors-heres-how-i-did-it) | GitHub Sponsors で $112,680/yr | 本物の足場での積極的な販売 |
| [komorebi (~10k★)](https://lgug2z.com/articles/github-sponsorship-breakdown-for-2024/) | $1,861/yr（~$155/mo） | **10kスターでも販売がなければスポンサーシップではない** |

---

## コントリビュート

訂正や新しいプラットフォーム/プログラムを歓迎する — **引用可能な公式ソース付きで**。[CONTRIBUTING.md](CONTRIBUTING.md) を参照。唯一のルール：**未検証の事実を公開しない**こと。不確かなものは推測せず `unverified` と明記する。

---

## Star History

<a href="https://star-history.com/#irmacardozo993-lgtm/awesome-oss-sponsorship&Date">
  <img src="https://api.star-history.com/svg?repos=irmacardozo993-lgtm/awesome-oss-sponsorship&type=Date" alt="Star History">
</a>

---

## 免責事項

このリポジトリ内のすべての価格、手数料、コミッション率、収益数値は **推定 / 参考のみ** である。これらは見積もりではなく、保証ではなく、金融・法務・税務の助言でもない。実際の価格は、業種、トラフィック、ユーザー品質、コンバージョン率、視聴者の地理、スポンサーの予算に依存する。**依存する前に各プラットフォームの現在の条件を確認すること。** プラットフォームのステータスは 2026-06-29 時点で確認しており、頻繁に変わる。本プロジェクトはいかなる収益も約束せず、「一攫千金」の仕組みではない — スポンサーシップをプロフェッショナルに運営したいメンテナー向けの実践ガイドである。

ライセンス：コンテンツは [CC-BY-4.0](LICENSE)、埋め込みコードスニペットは MIT。[LICENSE](LICENSE) を参照。
