<div align="center">

# 米内 幸輝 — 冷凍アカギ ❄️
**@akagifreeez** · 2007年生 / 岩手県 / フリーランス・個人開発

深いシステムを一人で 設計 → 実装 → テスト/CI → 公開 まで通し、
自作 Web アプリは自宅 Proxmox 上の k3s へコンテナ化してデプロイ・運用、
過程を Zenn で発信しています。
*I design, build, test/CI and ship deep systems solo, deploy containerized web apps to a self-hosted Proxmox→k3s cluster, and write up the journey on Zenn.*

主要言語 / Core: **TypeScript · Python · Rust**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![Tauri](https://img.shields.io/badge/Tauri-24C8DB?logo=tauri&logoColor=white)

![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes (k3s)](https://img.shields.io/badge/Kubernetes_(k3s)-326CE5?logo=kubernetes&logoColor=white)
![KEDA](https://img.shields.io/badge/KEDA-326CE5?logo=kubernetes&logoColor=white)
![Cloudflare Tunnel](https://img.shields.io/badge/Cloudflare_Tunnel-F38020?logo=cloudflare&logoColor=white)
![Proxmox VE](https://img.shields.io/badge/Proxmox_VE-E57000?logo=proxmox&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)

[GitHub](https://github.com/akagifreeez) · [Portfolio](https://akagifreeez.github.io) · [Zenn](https://zenn.dev/akagifreeez) · 📧 akagifreeezworks@gmail.com

</div>

---

## できること / What I do

- **エージェント・LLM 基盤** — 既存 LLM API（Claude / OpenAI / Gemini）を活用したツールユースループ・マルチエージェント協調・RAG・MCP。プロンプト設計から組込み・パイプライン化まで。*(自前の ML 学習はしません。)*
- **耐障害なシステム設計** — retry/backoff・自動再接続・フェイルオーバー・決定論リプレイ・状態機械。テストと GitHub Actions CI を当たり前に回す。
- **クラウドネイティブ運用** — コンテナ化 → k3s デプロイ → KEDA で scale-to-zero/オートスケール → Cloudflare Tunnel でインバウンド開放ゼロ公開。*(自宅個人運用・公開実証ベース。)*
- **Web / デスクトップ** — Next.js（App Router）、Tauri（Rust + Web）でのアプリ実装。

> 受託（クライアント案件）の実務はこれからです。掲載しているものは公開リポジトリ・ライブURL・CI で実際に検証できる範囲だけを書いています。
> *Client/contract work is still ahead of me — everything listed below is verifiable via public repos, live URLs, or green CI.*

---

## ピックアップ作品 / Featured

すべて **自作の公開リポジトリ（public original）** です。

### 🧩 深いシステム / Deep systems
| Repo | 概要 | Tech |
|---|---|---|
| [**hl-read**](https://github.com/akagifreeez/hl-read) | 鍵を預けずに使える読取専用の Hyperliquid MCP ツールキット（取引機能を持たない設計）。MCP 16ツール＋retry/backoff・自動再接続の耐障害層 | Python · MCP |
| [**conductor**](https://github.com/akagifreeez/conductor) | ベンダ非依存 LLM エージェント統制基盤。自作 tool-use ループ＋3バックエンド、実OS隔離サンドボックス（Proxmox LXC / Docker）で snapshot/rollback、決定論リプレイ、グローバル予算。98テスト・CI緑 | Python |
| [**relayforge**](https://github.com/akagifreeez/relayforge) | 不安定回線向け SRT 多リンク・フェイルオーバー制御＋Mission Control 可視化。決定論的な健全性状態機械（GOOD/DEGRADED/DEAD）、SSE/JSONL テレメトリ。GitHub Pages でゼロインストールのライブ実演（[Live](https://akagifreeez.github.io/relayforge/)・リンク断は約3秒で自動切替） | Python |
| [**hl-liqmap**](https://github.com/akagifreeez/hl-liqmap) | HL 清算ヒートマップ＋カスケード価格影響試算。公開オンチェーンポジションから生成、読取専用・鍵不要 | Python |
| [**token-router**](https://github.com/akagifreeez/token-router) | local（Ollama）↔remote API を精度床を保ちつつコスト最小でルーティングするハイブリッドエージェント | Python |

### ☁ クラウドネイティブ / Cloud-native
| Repo | 概要 | Tech |
|---|---|---|
| [**hl-read-live**](https://github.com/akagifreeez/hl-read-live) | 鍵不要 HL MCP のライブ実演。自宅 k3s へコンテナ化デプロイ、KEDA scale-to-zero＋Cloudflare Tunnel。Dockerfile / k8s マニフェスト同梱＝再現可能 | TypeScript · Next.js · k8s |

### 🤖 AI / LLM デモ / Demos
| Repo | 概要 | Tech |
|---|---|---|
| [**mycelium**](https://github.com/akagifreeez/mycelium) | AI エージェントの思考過程を菌糸として可視化 | TypeScript · Claude Agent SDK |
| [**page-to-json**](https://github.com/akagifreeez/page-to-json) | URL → 構造化 JSON。スクレイピング × Claude Haiku、BYOK で $0 | TypeScript |
| [**mini-rag**](https://github.com/akagifreeez/mini-rag) | 小さく正直な RAG。ingest→chunk→embed→cosine 検索→引用付き回答＋recall@k 評価。API キー無しでオフライン動作 | Python |
| [**agent-docsmith**](https://github.com/akagifreeez/agent-docsmith) | Claude Agent SDK 製ドキュメントエージェント。自然言語でのファイル編集＋ライブ差分＋自作 in-process MCP ツール（Markdown→HTML） | TypeScript · Claude Agent SDK |
| [**ai-inbox-triage**](https://github.com/akagifreeez/ai-inbox-triage) | 問い合わせの自動仕分け＋返信ドラフト。オフラインのルールベース＋任意で Claude API | Python |
| [**leviathan**](https://github.com/akagifreeez/leviathan) | 市場（HL）を生き物として描くライブデータアート。鍵不要・読取専用・$0 | TypeScript |

### 📡 配信 / Streaming infra
| Repo | 概要 | Tech |
|---|---|---|
| [**mediamtx-failover-controller**](https://github.com/akagifreeez/mediamtx-failover-controller) | MediaMTX の冗長 SRT ストリーム自動フェイルオーバー＋OBS 自動切替 | Python |
| [**srtla-ipv6-bonding**](https://github.com/akagifreeez/srtla-ipv6-bonding) | VPS なしのセルラー帯域集約を IPv6 dual-stack SRTLA で（レシピ＋設定） | Shell |
| [**CarStream**](https://github.com/akagifreeez/CarStream) | ウォーターマーク無し Android SRT IRL 送信。auto-reconnect・適応ビットレート | Kotlin |

### 🖥 Web / Desktop
| Repo | 概要 | Tech |
|---|---|---|
| [**nextjs-microcms-portfolio**](https://github.com/akagifreeez/nextjs-microcms-portfolio) | Next.js（App Router）× microCMS × Vercel。一覧/詳細を端〜端で実装・公開 | TypeScript · Next.js |
| [**AlphaView**](https://github.com/akagifreeez/AlphaView) | Sony RAW をネイティブ高速現像するデスクトップアプリ | TypeScript · Rust · Tauri |
| [**hangar**](https://github.com/akagifreeez/hangar) | VRChat の .unitypackage を Unity 無しで棚卸し・プレビュー・導入追跡（ローカル限定・読取専用・非公式） | TypeScript |

### 🛠 運用ユーティリティ / Utilities
| Repo | 概要 | Tech |
|---|---|---|
| [**claude-status-discord**](https://github.com/akagifreeez/claude-status-discord) | 外部 API（Claude）の障害を監視し Discord / Slack に自動通知。GitHub Actions cron・ゼロ依存 Python | Python |

> ⓘ CarStream は StreamPack ベース。RelayForge 系の冗長/フェイルオーバーは libsrt / SRTLA / MediaMTX に帰属します。帯域集約（bonding）は未測定で「無瞬断」とは書きません — リンク断の自動切替は **約3秒**（切替ギャップ込み）です。

---

## ☁ クラウドネイティブ運用 / Cloud-native ops

**自宅 Proxmox VE 9 → k3s v1.36（2ノード） → KEDA scale-to-zero → Cloudflare Tunnel（インバウンドポート開放ゼロ） → Zenn 発信** という一貫した物語を、自分のインフラ上で実証しています。

| | |
|---|---|
| 🟢 Live (cold) | [hello.akagifreeez.net](https://hello.akagifreeez.net) → HTTP 200 / 約15.7s（ゼロからのコールドスタートが実際に起動した証拠） |
| 🟢 Live (warm) | [hl.akagifreeez.net](https://hl.akagifreeez.net) → HTTP 200 / 約2.9s（hl-read Live がクラスタ上で稼働） |
| 📈 実測 | コールドスタート **7.2s → 最適化後 3.1s**、ウォーム **0.4s**（Zenn 記事の実測値） |
| ✍ 記事 | [自宅k3sで『アクセスされた時だけ起きる』Webアプリ — KEDA scale-to-zero × Cloudflare Tunnel](https://zenn.dev/akagifreeez/articles/k3s-scale-to-zero-cloudflare-tunnel) |

> ※ 上の **15.7s** は本日ゼロスケール状態へ最初の 1 リクエストで届いたフルコールドパスの実測（Cloudflare Tunnel 経由）、**3.1s** は Zenn 記事の最適化後ベンチ値です。前提が違うため両方を併記しています。

構成: Proxmox VE 9 / k3s v1.36（2ノード）/ cloudflared を Deployment 配置（インバウンドポート開放ゼロ）/ KEDA core + HTTP Add-on / Next.js standalone / ghcr.io。マニフェスト（Dockerfile・k8s/app.yaml・k8s/scaledobject.yaml）は [hl-read-live](https://github.com/akagifreeez/hl-read-live) に commit 済で再現可能。

> **Honest notes:** 2ノードの k3s は同一ホスト上に同居しており **真の HA（高可用）ではありません**。インフラは **自宅個人運用・公開実証ベース** であって、本番運用・チーム運用・受託の実務経験ではありません。scale-to-zero／オートスケール／上記のライブ HTTP 200 と実測値は事実として確認済みです。

---

## OSS コントリビュート / OSS contributions

外部 OSS にフォークから送り、**マージ済みの PR**（自作プロジェクトではなく貢献として）:

- [hahwul/dalfox #1076](https://github.com/hahwul/dalfox/pull/1076) ・ [#1089](https://github.com/hahwul/dalfox/pull/1089) — XSS スキャナ（Go）×2
- [KaotoIO/kaoto #3273](https://github.com/KaotoIO/kaoto/pull/3273) — Red Hat 系 ローコード統合（TypeScript / React）
- [finos/git-proxy #1554](https://github.com/finos/git-proxy/pull/1554) — Linux Foundation / FINOS（Node / TypeScript）
- [emilk/egui #8224](https://github.com/emilk/egui/pull/8224) — Rust 即時モード GUI（★29k）

加えて [ansvisor/ansvisor #147](https://github.com/ansvisor/ansvisor/pull/147)（小規模 OSS・TS）もマージ済み。

---

## 📊 統計 / Stats

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=akagifreeez&layout=compact&langs_count=8)](https://github.com/akagifreeez)
[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=akagifreeez&show_icons=true&hide_rank=true)](https://github.com/akagifreeez)

---

## 連絡 / Contact

- 📧 **akagifreeezworks@gmail.com**
- ✍ Zenn — [zenn.dev/akagifreeez](https://zenn.dev/akagifreeez)
- 🌐 Portfolio — [akagifreeez.github.io](https://akagifreeez.github.io)

<div align="center"><sub>正直・控えめに、実装の中身と公開物で語ります。<br><i>Quiet and honest — let the shipped code and live URLs do the talking.</i></sub></div>
