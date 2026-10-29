# 🌐 Awesome Proxy Ecosystem

<p align="center">
  <b>プロトコル・ツール・リソースの究極キュレーション</b><br/>
  <i>The Ultimate Curated List of Proxy Protocols, Tools, and Resources</i>
</p>

<p align="center">
  <a href="../../README.md">English</a> ｜
  <a href="../zh-CN/README.md">简体中文</a> ｜
  <a href="README.md">日本語</a> ｜
  <a href="../ko/README.md">한국어</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/プロトコル-35+-blue" alt="Protocols"/>
  <img src="https://img.shields.io/badge/クライアント-20+-green" alt="Clients"/>
  <img src="https://img.shields.io/badge/プラットフォーム-8+-orange" alt="Platforms"/>
  <img src="https://img.shields.io/badge/license-MIT-success" alt="License"/>
</p>

---

## 📖 概要

本プロジェクトは、プロキシプロトコル、実装、クライアント、およびエコシステムリソース包括的にキュレーションされたリストです。[jichangzhu.org/protocols](https://jichangzhu.org/protocols/) や複数の GitHub awesome リストから情報を統合しています。

開発者、研究者、プライバシーを重視するユーザーに関わらず、このガイドが複雑なプロキシ技術の世界をナビゲートします。

> 📌 データは **35+ プロトコル** の詳細なテストと評価に基づいています。

## 📑 目次

- [クイックスタート](#-クイックスタート)
- [プロトコル分類](#-プロトコル分類)
- [コアプロトコル詳細](#-コアプロトコル詳細)
- [クライアントソフトウェア](#-クライアントソフトウェア)
- [サーバーパネル＆管理](#-サーバーパネル--管理)
- [プロキシプラットフォーム＆フレームワーク](#-プロキシプラットフォーム--フレームワーク)
- [フリープロキシリスト](#-フリープロキシリスト)
- [ツール＆ユーティリティ](#-ツール--ユーティリティ)
- [学習リソース](#-学習リソース)
- [2026 年技術動向](#-2026-年技術動向)

---

## 🚀 クイックスタート

### プロトコル選択ガイド

| あなたのニーズ | 推奨プロトコル | 理由 |
|---------------|---------------|------|
| 最高のステルス | **VLESS-Reality**、**NaiveProxy** | フィンガープリント盗取、ノー特徴 |
| 最高速度 | **Hysteria 2**、**TUIC v5** | UDP ブルートフォース、0-RTT |
| ゲーミング低遅延 | **Shadowsocks-2022**、**ShadowQUIC** | 薄い暗号化、効率的な UDP |
| ルーター/組み込み | **SS-2022**、**Brook** | 最小リソース使用 |
| Apple エコシステム | **Mieru**、**Trojan**、**Sudoku** | 低メンテナンス、プライベートプロトコル |
| 汎用 | **VMess**、**VLESS-XTLS** | 成熟したエコシステム |

### 決定ドリームツリー

```
ドメインはありますか？
├── あり → 最高の性能が必要？
│   ├── はい → VLESS-XTLS-Vision
│   └── いいえ → VLESS-Reality
└── なし → 最高のステルスが必要？
    ├── はい → AnyTLS-Reality または VLESS-Reality
    └── いいえ → Hysteria 2（ネットワークが悪い場合）または SS-2022（ハードウェアが限られている場合）
```

---

## 📊 プロトコル分類

### 総合力評価

| カテゴリ | 代表プロトコル | 推奨度 | コア強み | 適用シーン |
|---------|--------------|--------|---------|-----------|
| **ステルス最高位** | VLESS-Reality, Naive, AnyTLS | ⭐⭐⭐⭐⭐ | フィンガープリント偽装、完璧な隠蔽 | 極めて厳しい環境、長期的安定 |
| **高速加速派** | Hysteria 2, TUIC v5, Juicity | ⭐⭐⭐⭐⭐ | UDP ブルートフォース、0-RTT、8K 瞬開 | 弱ネットワーク、動画、ゲーム |
| **軽量性能派** | SS-2022, Brook, Vlite | ⭐⭐⭐⭐ | 最小リソース、高速ハンドシェイク | ルーター、組み込み、旧型端末 |
| **極小ステルス派** | Mieru, Trojan, Sudoku | ⭐⭐⭐⭐ | 能動的探知耐性、プライベート最適化 | Apple エコ、低メンテナンス |
| **定番万能型** | VMess, VLESS-XTLS, SSR | ⭐⭐⭐ | 成熟エコ、機能豊富、互換性高 | 日常使用、マルチ業務 |
| **基盤セキュリティ** | WireGuard, Tor, SSH, kcptun | ⭐⭐⭐ | 工業級セキュリティ、匿名ルーティング | リモートワーク、匿名性、弱網最適化 |

### 🏆  Tier 1 — ステルス最高位

| プロトコル | ステータス | GitHub | 特徴 |
|-----------|----------|--------|------|
| **VLESS-Reality** | ✅ 稼働中 | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | 実際のWebサイトのフィンガープリントを盗用 |
| **NaiveProxy** | ✅ 稼働中 | [klzgrad/naiveproxy](https://github.com/klzgrad/naiveproxy) | Chrome ネットワークスタックを使用 |
| **AnyTLS** | ✅ 稼働中 | [anytls/anytls-go](https://github.com/anytls/anytls-go) | 最小TLSプロキシ、検出困難 |

### 🚀 Tier 2 — 高速加速派

| プロトコル | ステータス | GitHub | 特徴 |
|-----------|----------|--------|------|
| **Hysteria 2** | ✅ 稼働中 | [apernet/hysteria](https://github.com/apernet/hysteria) | Brutal 輻輳制御、20% ロスでも満速 |
| **TUIC v5** | ✅ 稼働中 | [tuic-protocol/tuic](https://github.com/tuic-protocol/tuic) | QUIC ベース、多重化、モバイル省電力 |
| **Juicity** | ✅ 稼働中 | [juicity/juicity](https://github.com/juicity/juicity) | QUIC プロトコルの頂点 |

### ⚡ Tier 3 — 軽量性能派

| プロトコル | ステータス | GitHub | 特徴 |
|-----------|----------|--------|------|
| **Shadowsocks-2022** | ✅ 稼働中 | [shadowsocks/shadowsocks-rust](https://github.com/shadowsocks/shadowsocks-rust) | 低遅延の指標、AEAD 2022 暗号化 |
| **Brook** | ✅ 稼働中 | [txthinking/brook](https://github.com/txthinking/brook) | シンプル、高速、クロスプラットフォーム |
| **Vlite** | ✅ 稼働中 | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | 軽量 V2Ray 変種 |

### 👻 Tier 4 — 極小ステルス派

| プロトコル | ステータス | GitHub | 特徴 |
|-----------|----------|--------|------|
| **Mieru** | ✅ 稼働中 | [enclica/mieru](https://github.com/enclica/mieru) | 分類困難、探知困難 |
| **Trojan** | ✅ 稼働中 | [trojan-gfw/trojan](https://github.com/trojan-gfw/trojan) | HTTPS トラフィックを偽装 |
| **Sudoku** | ✅ 稼働中 | [SUDOKU-ASCII/sudoku](https://github.com/SUDOKU-ASCII/sudoku) | 数独ベースの低エントロピー指紋 |

### 🔄 Tier 5 — 定番万能型

| プロトコル | ステータス | GitHub | 特徴 |
|-----------|----------|--------|------|
| **VMess** | ⚠️ アーカイブ | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | 成熟エコ、広範なサポート |
| **VLESS-XTLS** | ✅ 稼働中 | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | XTLS Vision/Reality フロー制御 |
| **SSR** | ❌ 非推奨 | [shadowsocksrr](https://github.com/shadowsocksrr) | 歴史的意義 |

### 🔐 Tier 6 — 基盤セキュリティ

| プロトコル | ステータス | GitHub | 特徴 |
|-----------|----------|--------|------|
| **WireGuard** | ✅ 稼働中 | [WireGuard](https://github.com/WireGuard) | 工業級VPN、PQC 対応 |
| **Tor** | ✅ 稼働中 | [torproject/tor](https://github.com/torproject/tor) | 匿名ルーティング、オニオンサービス |
| **SSH** | ✅ 稼働中 | [openssh](https://github.com/openssh/openssh-portable) | SOCKS5 トンネリング、PQC 対応 |
| **kcptun** | ✅ 稼働中 | [xtaci/kcp-go](https://github.com/xtaci/kcp-go) | UDP 信頼性傳輸加速 |

### 🌐 Tier 7 — トランスポート＆レガシー

| プロトコル | ステータス | GitHub | 特徴 |
|-----------|----------|--------|------|
| **Shadow-TLS** | ✅ 稼働中 | [ihciah/shadow-tls](https://github.com/ihciah/shadow-tls) | TLS をラップして通常の HTTPS に偽装 |
| **Snell** | ✅ 稼働中 | [Surge](https://kb.nssurge.com) | Surge 開発者製、Apple エコ |
| **Masque** | ✅ 稼働中 | [quic-go/masque-go](https://github.com/quic-go/masque-go) | QUIC/HTTP-3 トンネリング |
| **MTProto** | ✅ 稼働中 | [Telegram](https://core.telegram.org/mtproto) | Telegram プロキシプロトコル |
| **ShadowQUIC** | ✅ 稼働中 | [spongebob888/shadowquic](https://github.com/spongebob888/shadowquic) | SS ステルス + QUIC 多重化 |
| **GOST** | ✅ 稼働中 | [go-gost/gost](https://github.com/go-gost/gost) | マルチプロトコルセキュリティプロキシ |
| **TrustTunnel** | ✅ 稼働中 | [TrustTunnel/TrustTunnel](https://github.com/TrustTunnel/TrustTunnel) | AdGuard の難読化 VPN |

---

## 🔬 コアプロトコル詳細

### VLESS + Reality — 2026 年検閲回避のゴールドスタンダード

```
[クライアント] → VLESS → Reality（TLSを盗んでtarget.comに偽装）→ [サーバー]
```

**コア強み：**
- 🚫 **ドメイン不要** — 実際のWebサイトの証明書を借用
- 🔒 **ゼロTLS特徴** — uTLS で実際のブラウザを模倣
- 🔑 **前方秘匿性** — 各セッションに固有のキー

**実装：** [XTLS/Xray-core](https://github.com/XTLS/Xray-core) · [SagerNet/sing-box](https://github.com/SagerNet/sing-box)

### Hysteria 2 — 悪いネットワークのためのブルートフォース加速

```
[クライアント] → Hysteria 2（Brutal CC）→ UDP フラッド → [サーバー]
```

**コア強み：**
- 💪 **Brutal アルゴリズム** — ロスに関係なく宣言速度で送信
- 📉 **20% ロスでも機能** — 悪い国際回線向けに設計
- ⚡ **QUIC ベース** — モダントランスポートプロトコル

**実装：** [apernet/hysteria](https://github.com/apernet/hysteria)

### Shadowsocks-2022 — 低遅延の指標

```
[クライアント] → SS-2022（AEAD 2022）→ セッション暗号化 → [サーバー]
```

**コア強み：**
- 🔑 **セッション鍵** — HKDF から各セッションの固有キーを派生
- 📡 **UDP over TCP** — 効率的な UDP 処理
- 📦 **最小オーバーヘッド** — 薄い暗号化レイヤー

**実装：** [shadowsocks/shadowsocks-rust](https://github.com/shadowsocks/shadowsocks-rust)

### NaiveProxy — 究極のカモフラージュ

```
[クライアント] → NaiveProxy（Chrome ネットスタック）→ Chrome と完全同一 → [サーバー]
```

**コア強み：**
- 🌐 **Chrome ネットワークスタック使用** — Chrome と同一の TLS フィンガープリント
- 🔀 **HTTP/2 多重化** — 効率的な並列ストリーム
- 🛡️ **Chrome をブロックしないとブロック不可**

**実装：** [klzgrad/naiveproxy](https://github.com/klzgrad/naiveproxy)

---

## 💻 クライアントソフトウェア

### クロスプラットフォームクライアント

| クライアント | プラットフォーム | 対応プロトコル | GitHub |
|-------------|----------------|---------------|--------|
| **sing-box** | Win/Mac/Linux/Android/iOS | 全主要 | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) |
| **Clash Meta (Mihomo)** | Win/Mac/Linux | VMess/VLESS/SS/Trojan/TUIC/H2 | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) |
| **Hiddify** | 全プラットフォーム | 全主要 | [hiddify/hiddify-app](https://github.com/hiddify/hiddify-app) |
| **Clash Verge Rev** | Win/Mac/Linux | Clash ベース | [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev) |
| **NekoBox** | Android | SS/V2Ray/sing-box | [MatsuriDayo/NekoBoxForAndroid](https://github.com/MatsuriDayo/NekoBoxForAndroid) |
| **v2rayN** | Windows | VMess/VLESS/SS/Trojan | [2dust/v2rayN](https://github.com/2dust/v2rayN) |
| **v2rayNG** | Android | VMess/VLESS/SS/Trojan | [2dust/v2rayNG](https://github.com/2dust/v2rayNG) |
| **Shadowrocket** | iOS/tvOS | 全主要 | App Store |
| **Surge** | macOS/iOS | 全主要 | 商用 |
| **Stash** | macOS/iOS | 全主要 | App Store |
| **V2RayA** | Linux (Web GUI) | V2Ray/Xray/sing-box | [v2rayA/v2rayA](https://github.com/v2rayA/v2rayA) |

---

## 🖥️ サーバーパネル＆管理

| パネル | 対応プロトコル | 機能 | GitHub |
|--------|---------------|------|--------|
| **3X-UI** | VLESS/VMess/Trojan/H2/TUIC | Web GUI、多ユーザー、トラフィック制御 | [MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui) |
| **X-UI** | VLESS/VMess/Trojan | シンプル Web パネル | [FranzKafkaYu/x-ui](https://github.com/FranzKafkaYu/x-ui) |
| **Hiddify Manager** | 全主要 | マルチサーバー管理 | [hiddify/hiddify-manager](https://github.com/hiddify/hiddify-manager) |
| **Marzban** | VLESS/VMess/Trojan | マルチプロトコル、Telegram Bot | [Gozargah/Marzban](https://github.com/Gozargah/Marzban) |

---

## 🏗️ プロキシプラットフォーム＆フレームワーク

### 汎用プロキシプラットフォーム

| プロジェクト | 言語 | 対応プロトコル | GitHub |
|-------------|------|---------------|--------|
| **sing-box** | Go | SS/VMess/VLESS/Trojan/TUIC/H2/Naive/WG | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) |
| **Xray-core** | Go | VLESS/VMess/Trojan/Reality/XTLS | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) |
| **v2ray-core** | Go | VMess/VLESS/SS/Trojan | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) |
| **Clash** | Go | SS/VMess/VLESS/Trojan/SOCKS5/HTTP | [Dreamacro/clash](https://github.com/Dreamacro/clash) |
| **mihomo** | Go | Clash + TUIC/H2/Reality | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) |
| **GOST** | Go | マルチプロトコルチェーン | [go-gost/gost](https://github.com/go-gost/gost) |

### リバースプロキシ＆ロードバランサー

| プロジェクト | 説明 | GitHub |
|-------------|------|--------|
| **Nginx** | 高性能 HTTP/リバースプロキシ | [nginx/nginx](https://github.com/nginx/nginx) |
| **Caddy** | 自動 HTTPS リバースプロキシ | [caddyserver/caddy](https://github.com/caddyserver/caddy) |
| **Traefik** | クラウドネイティブリバースプロキシ | [traefik/traefik](https://github.com/traefik/traefik) |
| **Envoy** | サービスメッシュ L7 プロキシ | [envoyproxy/envoy](https://github.com/envoyproxy/envoy) |
| **HAProxy** | TCP/HTTP ロードバランサー | [haproxy/haproxy](https://github.com/haproxy/haproxy) |
| **FRP** | 高速リバースプロキシ | [fatedier/frp](https://github.com/fatedier/frp) |

---

## 📋 フリープロキシリスト

| プロジェクト | プロトコル | 更新頻度 | GitHub |
|-------------|-----------|---------|--------|
| **OpenRay** | VMess/VLESS/Trojan/SS/H2/TUIC/Juicity | 毎時 | [sakha1370/OpenRay](https://github.com/sakha1370/OpenRay) |
| **free-proxy-list** | SS/SSSR/V2Ray/Trojan/H2/TUIC/WG | 30分毎 | [gfpcom/free-proxy-list](https://github.com/gfpcom/free-proxy-list) |
| **openproxylist** | HTTPS/SOCKS4/SOCKS5/V2Ray | 毎時 | [roosterkid/openproxylist](https://github.com/roosterkid/openproxylist) |

---

## 🔧 ツール＆ユーティリティ

### プロキシチェッカー＆スクレイパー

| ツール | 言語 | 機能 | GitHub |
|--------|------|------|--------|
| **ProxyBroker** | Python | 発見、チェック、サーバー化 | [constverum/ProxyBroker](https://github.com/constverum/ProxyBroker) |
| **proxy-scraper-checker** | Rust | 高速スクレイピング+チェック | [monosans/proxy-scraper-checker](https://github.com/monosans/proxy-scraper-checker) |
| **checked-proxy-list** | Go | TUI 付き CLI | [ClearProxy/checked-proxy-list](https://github.com/ClearProxy/checked-proxy-list) |

### ローテーション＆管理

| ツール | 説明 | GitHub |
|--------|------|--------|
| **rota** | 高性能ローテーションエンジン | [alpkeskin/rota](https://github.com/alpkeskin/rota) |
| **singbox2proxy** | HTTP クライアントで sing-box プロキシを使用 | [nichind/singbox2proxy](https://github.com/nichind/singbox2proxy) |

---

## 📚 学習リソース

### 公式ドキュメント
- [sing-box 公式ドキュメント](https://sing-box.sagernet.org/)
- [Xray-core ドキュメント](https://xtls.github.io/)
- [Clash Wiki](https://wiki.clash.wiki/)
- [Hysteria 2 ドキュメント](https://hysteria.network/)

---

## 🔮 2026 年技術動向

1. **TCP → UDP/QUIC 移行** — HTTP/3 普及により QUIC ベースプロトコルが主流に
2. **暗号化から偽装へ** — 単純な AES は不十分、フィンガープリント偽装と Realit が鍵
3. **ポスト量子暗号 (PQC)** — SSH と WireGuard が量子耐性アルゴリズムを導入
5. **マルチプロトコル重ね合わせ** — 複数のプロトコルを同時稼働して耐性を強化

> 💡 推奨：クライアントに少なくとも2種類のプロトコル（Reality + Hysteria 2 など）を備蓄しましょう。

---

## 🤝 貢献

貢献歓迎！[CONTRIBUTING.md](../../CONTRIBUTING.md) をお読みください。

## 📜 ライセンス

MIT ライセンス — 詳細は [LICENSE](../../LICENSE) をご覧ください。

---

<p align="center">
  <sub>コミュニティによって、コミュニティのために。</sub><br/>
  <sub>最終更新：2026-10-29</sub>
</p>
