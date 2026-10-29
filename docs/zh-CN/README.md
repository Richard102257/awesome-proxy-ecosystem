# 🌐 Awesome Proxy Ecosystem

<p align="center">
  <b>终极代理协议、工具与资源精选</b><br/>
  <i>The Ultimate Curated List of Proxy Protocols, Tools, and Resources</i>
</p>

<p align="center">
  <a href="../../README.md">English</a> ｜
  <a href="README.md">简体中文</a> ｜
  <a href="../ja/README.md">日本語</a> ｜
  <a href="../ko/README.md">한국어</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/协议-35+-blue" alt="Protocols"/>
  <img src="https://img.shields.io/badge/客户端-30+-green" alt="Clients"/>
  <img src="https://img.shields.io/badge/面板-15+-orange" alt="Panels"/>
  <img src="https://img.shields.io/badge/工具-25+-purple" alt="Tools"/>
  <img src="https://img.shields.io/badge/总条目-150+-red" alt="Total"/>
  <img src="https://img.shields.io/badge/语言-4-success" alt="Languages"/>
  <img src="https://img.shields.io/badge/license-MIT-success" alt="License"/>
</p>

---

## 📖 项目简介

本项目是目前最全面的代理协议、实现、客户端、面板、隧道工具和生态系统资源精选集合。整合了来自多个来源的信息：

- [jichangzhu.org/protocols](https://jichangzhu.org/protocols/) — 深度协议测试与对比
- [drsoft-oss/awesome-proxy](https://github.com/drsoft-oss/awesome-proxy) — 协作代理资源列表
- [awesome-tunneling](https://github.com/anderspitman/awesome-tunneling) — 隧道工具（21k+ stars）
- [awesome-wireguard](https://github.com/cedrickchee/awesome-wireguard) — WireGuard 生态（1.5k+ stars）
- [awesome-anticensor](https://github.com/marzneshin/awesome-anticensor) — 审查对抗工具
- [awesome-freedom](https://github.com/erfjab/awesome-freedom) — 面板、脚本、Bot（153+ stars）
- 以及更多 GitHub awesome 列表和独立项目

**150+ 条目**，覆盖 12 大类。

## 📑 目录

- [快速入门](#-快速入门)
- [协议分类总览](#-协议分类总览)
- [核心协议深度解析](#-核心协议深度解析)
- [客户端软件](#-客户端软件)
- [服务端面板与管理](#-服务端面板与管理)
- [代理平台与框架](#-代理平台与框架)
- [隧道工具](#-隧道工具)
- [订阅管理](#-订阅管理)
- [路由规则](#-路由规则)
- [一键安装脚本](#-一键安装脚本)
- [免费代理列表](#-免费代理列表)
- [工具与实用程序](#-工具与实用程序)
- [Cloudflare & WARP](#-cloudflare--warp)
- [抗审查资源](#-抗审查资源)
- [学习资源](#-学习资源)
- [2026 技术趋势](#-2026-技术趋势)

---

## 🚀 快速入门

### 协议速查表

| 你的需求 | 推荐协议 | 原因 |
|---------|---------|------|
| 极致隐匿 | **VLESS-Reality**、**NaiveProxy** | 指纹偷取、无特征 |
| 极致速度 | **Hysteria 2**、**TUIC v5** | UDP 暴力重传、0-RTT |
| 游戏低延迟 | **Shadowsocks-2022**、**ShadowQUIC** | 薄加密、UDP 高效 |
| 路由器/嵌入式 | **SS-2022**、**Brook** | 极低资源占用 |
| 苹果生态 | **Mieru**、**Trojan**、**Sudoku** | 低维护、私有协议 |
| 日常通用 | **VMess**、**VLESS-XTLS** | 生态成熟 |

### 快速选型决策树

```
你有域名吗？
├── 有 → 追求极致性能？
│   ├── 是 → VLESS-XTLS-Vision
│   └── 否 → VLESS-Reality
└── 没有 → 追求极致隐匿？
    ├── 是 → AnyTLS-Reality 或 VLESS-Reality
    └── 否 → Hysteria 2（网络差）或 SS-2022（硬件有限）
```

### 一键安装

```bash
# 一键安装（选一个）：
# 方案 A：sing-box 多协议（推荐）
bash -c "$(curl -fsSL https://raw.githubusercontent.com/yonggekkk/sing-box-yg/main/install.sh)"

# 方案 B：Xray/Tuic/Hysteria2 八合一
bash -c "$(curl -fsSL https://raw.githubusercontent.com/mack-a/v2ray-agent/main/install.sh)"

# 方案 C：V2Ray 经典
curl -Ls https://raw.githubusercontent.com/233boy/v2ray/master/v2ray.sh | bash
```

---

## 📊 协议分类总览

### 综合实力横评

| 协议类别 | 代表协议 | 推荐指数 | 核心优势 | 适用场景 |
|---------|---------|---------|---------|---------|
| **隐匿天花板** | VLESS-Reality, Naive, AnyTLS | ⭐⭐⭐⭐⭐ | 指纹偷取、无特征、完美伪装 | 极严苛环境、追求长效稳定 |
| **暴力加速派** | Hysteria 2, TUIC v5, Juicity | ⭐⭐⭐⭐⭐ | UDP 暴力重传、0-RTT、秒开 8K | 弱网、视频党、跨境游戏 |
| **轻量性能派** | SS-2022, Brook, Vlite | ⭐⭐⭐⭐ | 资源占用极低、握手快、稳定 | 路由器、嵌入式设备、老旧手机 |
| **极简隐形派** | Mieru, Trojan, Sudoku | ⭐⭐⭐⭐ | 抗主动探测、私有协议优化 | 苹果全家桶、低维护需求 |
| **经典全能型** | VMess, VLESS-XTLS, SSR | ⭐⭐⭐ | 生态成熟、功能丰富、兼容性广 | 个人日常使用、多业务分流 |
| **底层安全类** | WireGuard, Tor, SSH, kcptun | ⭐⭐⭐ | 工业级安全、匿名路由、底层加速 | 远程办公、极致匿名、弱网优化 |

### 🏆 第一梯队 — 隐匿天花板

| 协议 | 状态 | GitHub | 特性 |
|------|------|--------|------|
| **VLESS-Reality** | ✅ 维护中 | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | 偷取真实网站指纹，零 TLS 特征 |
| **NaiveProxy** | ✅ 维护中 | [klzgrad/naiveproxy](https://github.com/klzgrad/naiveproxy) | 调用 Chrome 网络栈，融入浏览器流量 |
| **AnyTLS** | ✅ 维护中 | [anytls/anytls-go](https://github.com/anytls/anytls-go) | 极简 TLS 代理，极难检测 |

### 🚀 第二梯队 — 暴力加速派

| 协议 | 状态 | GitHub | 特性 |
|------|------|--------|------|
| **Hysteria 2** | ✅ 维护中 | [apernet/hysteria](https://github.com/apernet/hysteria) | Brutal 拥塞控制，20% 丢包仍满速 |
| **TUIC v5** | ✅ 维护中 | [tuic-protocol/tuic](https://github.com/tuic-protocol/tuic) | 基于 QUIC，多路复用，移动端省电 |
| **Juicity** | ✅ 维护中 | [juicity/juicity](https://github.com/juicity/juicity) | QUIC 协议巅峰，快速轻量 |

### ⚡ 第三梯队 — 轻量性能派

| 协议 | 状态 | GitHub | 特性 |
|------|------|--------|------|
| **Shadowsocks-2022** | ✅ 维护中 | [shadowsocks/shadowsocks-rust](https://github.com/shadowsocks/shadowsocks-rust) | 低延迟标杆，AEAD 2022 加密 |
| **Brook** | ✅ 维护中 | [txthinking/brook](https://github.com/txthinking/brook) | 简单快速，全平台支持 |
| **Vlite** | ✅ 维护中 | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | 轻量级 V2Ray 变体 |

### 👻 第四梯队 — 极简隐形派

| 协议 | 状态 | GitHub | 特性 |
|------|------|--------|------|
| **Mieru** | ✅ 维护中 | [enclica/mieru](https://github.com/enclica/mieru) | 难以分类、难以探测 |
| **Trojan** | ✅ 维护中 | [trojan-gfw/trojan](https://github.com/trojan-gfw/trojan) | 伪装 HTTPS 流量 |
| **Sudoku** | ✅ 维护中 | [SUDOKU-ASCII/sudoku](https://github.com/SUDOKU-ASCII/sudoku) | 基于数独的低熵指纹混淆 |

### 🔄 第五梯队 — 经典全能型

| 协议 | 状态 | GitHub | 特性 |
|------|------|--------|------|
| **VMess** | ⚠️ 停更 | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | 生态成熟，广泛支持 |
| **VLESS-XTLS** | ✅ 维护中 | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | XTLS Vision/Reality 流控 |
| **SSR** | ❌ 弃用 | [shadowsocksrr](https://github.com/shadowsocksrr) | 历史意义 |

### 🔐 第六梯队 — 底层安全类

| 协议 | 状态 | GitHub | 特性 |
|------|------|--------|------|
| **WireGuard** | ✅ 维护中 | [WireGuard](https://github.com/WireGuard) | 工业级 VPN，后量子加密就绪 |
| **Tor** | ✅ 维护中 | [torproject/tor](https://github.com/torproject/tor) | 匿名路由，洋葱服务 |
| **SSH** | ✅ 维护中 | [openssh](https://github.com/openssh/openssh-portable) | SOCKS5 隧道，后量子支持 |
| **kcptun** | ✅ 维护中 | [xtaci/kcp-go](https://github.com/xtaci/kcp-go) | UDP 可靠传输加速 |

### 🌐 第七梯队 — 传输与传统协议

| 协议 | 状态 | GitHub | 特性 |
|------|------|--------|------|
| **Shadow-TLS** | ✅ 维护中 | [ihciah/shadow-tls](https://github.com/ihciah/shadow-tls) | 包装 TLS 伪装正常 HTTPS |
| **Snell** | ✅ 维护中 | [Surge](https://kb.nssurge.com) | Surge 开发者出品，苹果生态 |
| **Masque** | ✅ 维护中 | [quic-go/masque-go](https://github.com/quic-go/masque-go) | QUIC/HTTP-3 隧道 |
| **MTProto** | ✅ 维护中 | [Telegram](https://core.telegram.org/mtproto) | Telegram 代理协议 |
| **SOCKS5** | ✅ 标准 | 标准协议 | 通用代理协议 |
| **HTTP Proxy** | ✅ 标准 | 标准协议 | 基础正向代理 |
| **Fragment** | ✅ 维护中 | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) | TCP 分片抗审查 |
| **ShadowQUIC** | ✅ 维护中 | [spongebob888/shadowquic](https://github.com/spongebob888/shadowquic) | SS 隐蔽 + QUIC 多路复用 |
| **GOST** | ✅ 维护中 | [go-gost/gost](https://github.com/go-gost/gost) | 多协议安全代理 |
| **TrustTunnel** | ✅ 维护中 | [TrustTunnel/TrustTunnel](https://github.com/TrustTunnel/TrustTunnel) | AdGuard 混淆 VPN |

---

## 🔬 核心协议深度解析

### VLESS + Reality — 2026 年审查规避的黄金标准

```
[客户端] → VLESS → Reality（偷取 TLS 伪装成 target.com）→ [服务端]
```

**核心优势：**
- 🚫 **无需域名** — 借用真实网站的证书
- 🔒 **零 TLS 特征** — 使用 uTLS 模拟真实浏览器
- 🔑 **前向保密** — 每次会话使用唯一密钥

**实现项目：** [XTLS/Xray-core](https://github.com/XTLS/Xray-core) · [SagerNet/sing-box](https://github.com/SagerNet/sing-box)

### Hysteria 2 — 差网络的暴力加速器

```
[客户端] → Hysteria 2（Brutal 拥塞控制）→ UDP 洪泛 → [服务端]
```

**核心优势：**
- 💪 **Brutal 算法** — 无视丢包按声明速率发送
- 📉 **20% 丢包仍可用** — 专为糟糕国际线路设计
- ⚡ **基于 QUIC** — 现代传输协议

**实现项目：** [apernet/hysteria](https://github.com/apernet/hysteria)

### Shadowsocks-2022 — 低延迟标杆

```
[客户端] → SS-2022（AEAD 2022）→ 会话加密 → [服务端]
```

**核心优势：**
- 🔑 **会话密钥** — 每次会话通过 HKDF 派生唯一密钥
- 📡 **UDP over TCP** — 高效的 UDP 处理
- 📦 **最小开销** — 薄加密层

**实现项目：** [shadowsocks/shadowsocks-rust](https://github.com/shadowsocks/shadowsocks-rust)

### NaiveProxy — 终极伪装

```
[客户端] → NaiveProxy（Chrome 网络栈）→ 看起来完全像 Chrome → [服务端]
```

**核心优势：**
- 🌐 **使用 Chrome 网络栈** — 与 Chrome 完全一致的 TLS 指纹
- 🔀 **HTTP/2 多路复用** — 高效的并行流
- 🛡️ **无法在不封禁 Chrome 的情况下封禁**

**实现项目：** [klzgrad/naiveproxy](https://github.com/klzgrad/naiveproxy)

---

## 💻 客户端软件

### 全平台客户端

| 客户端 | 平台 | 支持协议 | GitHub | Stars |
|--------|------|---------|--------|-------|
| **sing-box** | Win/Mac/Linux/Android/iOS | 全部主流 | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) | ⭐ 25k+ |
| **Clash Verge Rev** | Win/Mac/Linux | 基于 Clash | [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev) | ⭐ 126k+ |
| **v2rayN** | Win/Mac/Linux | Xray/sing-box | [2dust/v2rayN](https://github.com/2dust/v2rayN) | ⭐ 118k+ |
| **Hiddify** | 全平台 | 全部主流 | [hiddify/hiddify-app](https://github.com/hiddify/hiddify-app) | ⭐ 33k+ |
| **FlClash** | Win/Mac/Linux/Android | Clash Meta | [chen08209/FlClash](https://github.com/chen08209/FlClash) | ⭐ 42k+ |
| **Clash Meta (Mihomo)** | Win/Mac/Linux | VMess/VLESS/SS/Trojan/TUIC/H2 | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) | ⭐ 25k+ |
| **NekoBox** | Android | SS/V2Ray/sing-box | [MatsuriDayo/NekoBoxForAndroid](https://github.com/MatsuriDayo/NekoBoxForAndroid) | ⭐ 21k+ |
| **nekoray** | Win/Mac/Linux | sing-box/Xray | [MatsuriDayo/nekoray](https://github.com/MatsuriDayo/nekoray) | ⭐ 15k+ |
| **v2rayNG** | Android | VMess/VLESS/SS/Trojan | [2dust/v2rayNG](https://github.com/2dust/v2rayNG) | ⭐ 30k+ |
| **Karing** | Win/Mac/Linux/Android/iOS | Clash/sing-box | [KaringX/karing](https://github.com/KaringX/karing) | ⭐ 11k+ |
| **GUI.for.SingBox** | Win/Mac/Linux | sing-box | [GUI-for-Cores/GUI.for.SingBox](https://github.com/GUI-for-Cores/GUI.for.SingBox) | ⭐ 7.6k+ |
| **V2RayA** | Linux (Web GUI) | V2Ray/Xray/sing-box | [v2rayA/v2rayA](https://github.com/v2rayA/v2rayA) | ⭐ 8.5k+ |
| **Throne** | Win/Mac/Linux | sing-box | [throneproj/Throne](https://github.com/throneproj/Throne) | ⭐ 5.4k+ |
| **Shadowrocket** | iOS/tvOS | 全部主流 | App Store | — |
| **Surge** | macOS/iOS | 全部主流 | 商业软件 | — |
| **Stash** | macOS/iOS | 全部主流 | App Store | — |

### 客户端平台支持矩阵

| 客户端 | Windows | macOS | Linux | Android | iOS | 路由器 |
|--------|---------|-------|-------|---------|-----|--------|
| Clash Verge Rev | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| FlClash | ✅ | ✅ | ✅ | ✅ | ❌ | ❌ |
| Hiddify | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| v2rayN | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| NekoBox | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ |
| v2rayNG | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ |
| Karing | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| Shadowrocket | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |
| OpenClash | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| PassWall | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |

---

## 🖥️ 服务端面板与管理

### Xray / Sing-box 面板

| 面板 | 支持协议 | 特性 | GitHub | Stars |
|------|---------|------|--------|-------|
| **3X-UI** | 13+ 协议，XTLS+REALITY | Web GUI，多用户，Bot，PostgreSQL | [MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui) | ⭐ 35k+ |
| **X-UI** | VLESS/VMess/Trojan | 简洁 Web 面板 | [vaxilu/x-ui](https://github.com/vaxilu/x-ui) | ⭐ 19k+ |
| **s-ui** | sing-box | 高级 Web 面板 | [alireza0/s-ui](https://github.com/alireza0/s-ui) | ⭐ 8.6k+ |
| **x-ui (EN)** | VLESS/VMess/Trojan | 英文版 + Telegram Bot | [alireza0/x-ui](https://github.com/alireza0/x-ui) | ⭐ 4k+ |
| **x-ui-yg** | H2, Xhttp, ENC, Argo, Psiphon | 增强版 x-ui | [yonggekkk/x-ui-yg](https://github.com/yonggekkk/x-ui-yg) | ⭐ 3.5k+ |
| **XUI-PRO** | 15+ 协议 + WARP + Psiphon | Nginx 反向代理集成 | [GFW4Fun/x-ui-pro](https://github.com/GFW4Fun/x-ui-pro) | ⭐ 1.2k+ |

### 多协议 / Python 面板

| 面板 | 支持协议 | 特性 | GitHub | Stars |
|------|---------|------|--------|-------|
| **Hiddify Manager** | 20+ 协议 | 多服务器，反过滤 | [hiddify/Hiddify-Manager](https://github.com/hiddify/Hiddify-Manager) | ⭐ 9.4k+ |
| **Marzban** | VLESS/VMess/Trojan | 可扩展，Telegram Bot | [Gozargah/Marzban](https://github.com/Gozargah/Marzban) | ⭐ 6.6k+ |
| **Remnawave** | Xray-core | TypeScript，现代 UI | [remnawave/panel](https://github.com/remnawave/panel) | ⭐ 3.8k+ |
| **Libertea** | VLESS | 简洁轻量 | [Libertea/Libertea](https://github.com/Libertea/Libertea) | ⭐ 1k+ |
| **sspanel-uim** | 多协议 | 商业级面板 | [anankke/sspanel-uim](https://github.com/anankke/sspanel-uim) | ⭐ 10k+ |
| **Marzneshin** | Xray-based | Marzban 继任者 | [marzneshin/marzneshin](https://github.com/marzneshin/marzneshin) | ⭐ 2k+ |

---

## 🏗️ 代理平台与框架

### 通用代理平台

| 项目 | 语言 | 支持协议 | GitHub | Stars |
|------|------|---------|--------|-------|
| **sing-box** | Go | SS/VMess/VLESS/Trojan/TUIC/H2/Naive/WG/Shadow-TLS | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) | ⭐ 25k+ |
| **Xray-core** | Go | VLESS/VMess/Trojan/Reality/XTLS | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | ⭐ 35k+ |
| **v2ray-core** | Go | VMess/VLESS/SS/Trojan | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | ⭐ 25k+ |
| **Clash** | Go | SS/VMess/VLESS/Trojan/SOCKS5/HTTP | [Dreamacro/clash](https://github.com/Dreamacro/clash) | 已归档 |
| **mihomo** | Go | Clash + TUIC/H2/Reality | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) | ⭐ 25k+ |
| **clash-rs** | Rust | Clash 协议 Rust 重写 | [Watfaq/clash-rs](https://github.com/Watfaq/clash-rs) | ⭐ 1.6k+ |
| **GOST** | Go | 多协议链式代理 | [go-gost/gost](https://github.com/go-gost/gost) | ⭐ 7k+ |
| **dae** | Go | 内核级代理 | [daeuniverse/dae](https://github.com/daeuniverse/dae) | ⭐ 5k+ |

### 反向代理与负载均衡

| 项目 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **Nginx** | 高性能 HTTP/反向代理 | [nginx/nginx](https://github.com/nginx/nginx) | ⭐ 25k+ |
| **Caddy** | 自动 HTTPS 反向代理 | [caddyserver/caddy](https://github.com/caddyserver/caddy) | ⭐ 60k+ |
| **Traefik** | 云原生反向代理 | [traefik/traefik](https://github.com/traefik/traefik) | ⭐ 55k+ |
| **Envoy** | 服务网格 L7 代理 | [envoyproxy/envoy](https://github.com/envoyproxy/envoy) | ⭐ 25k+ |
| **HAProxy** | TCP/HTTP 负载均衡 | [haproxy/haproxy](https://github.com/haproxy/haproxy) | ⭐ 5k+ |
| **FRP** | 快速反向代理 | [fatedier/frp](https://github.com/fatedier/frp) | ⭐ 90k+ |
| **Rathole** | 高性能反向代理 (Rust) | [rapiz1/rathole](https://github.com/rapiz1/rathole) | ⭐ 10k+ |
| **Pangolin** | 身份感知 VPN/代理 | [fosrl/pangolin](https://github.com/fosrl/pangolin) | ⭐ 5k+ |

### SOCKS/HTTP 正向代理

| 项目 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **Dante** | 免费 SOCKS 服务器 | [dante](https://www.inet.no/dante/) | — |
| **microsocks** | 极简便携 SOCKS5 | [micro11/microsocks](https://github.com/micro11/microsocks) | ⭐ 1.5k+ |
| **3proxy** | 通用代理 | [3proxy/3proxy](https://github.com/3proxy/3proxy) | ⭐ 1k+ |
| **tinyproxy** | 轻量级 HTTP/HTTPS 代理 | [tinyproxy/tinyproxy](https://github.com/tinyproxy/tinyproxy) | ⭐ 5.9k+ |
| **g3proxy** | 字节跳动 HTTP/SOCKS/SNI 代理 | [bytedance/g3proxy](https://github.com/bytedance/g3proxy) | ⭐ 3k+ |
| **snail007/goproxy** | 高性能 Go 代理 | [snail007/goproxy](https://github.com/snail007/goproxy) | ⭐ 5k+ |

---

## 🚇 隧道工具

> 用于穿透 NAT/防火墙、暴露本地服务的必备工具。

| 工具 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **FRP** | 快速反向代理（最流行） | [fatedier/frp](https://github.com/fatedier/frp) | ⭐ 90k+ |
| **ngrok** | localhost 公网 URL | [ngrok/ngrok](https://github.com/ngrok/ngrok) | ⭐ 2.5k+ |
| **Cloudflare Tunnel** | 零配置 CF 隧道 | [cloudflare/cloudflared](https://github.com/cloudflare/cloudflared) | ⭐ 10k+ |
| **Chisel** | 基于 HTTP 的快速 TCP/UDP 隧道 | [jpillora/chisel](https://github.com/jpillora/chisel) | ⭐ 15k+ |
| **bore** | 端口转发到公网 | [ekzhang/bore](https://github.com/ekzhang/bore) | ⭐ 9k+ |
| **Tailscale** | 零配置网状 VPN | [tailscale/tailscale](https://github.com/tailscale/tailscale) | ⭐ 25k+ |
| **ZeroTier** | 虚拟网络覆盖 | [zerotier/ZeroTierOne](https://github.com/zerotier/ZeroTierOne) | ⭐ 15k+ |
| **sshuttle** | 透明 SSH 代理 | [sshuttle/sshuttle](https://github.com/sshuttle/sshuttle) | ⭐ 10k+ |
| **localtunnel** | 将 localhost 暴露到公网 | [localtunnel/localtunnel](https://github.com/localtunnel/localtunnel) | ⭐ 20k+ |

📚 **完整隧道列表：** [awesome-tunneling](https://github.com/anderspitman/awesome-tunneling)（21k+ stars）

---

## 🔄 订阅管理

| 工具 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **Sub-Store** | 高级订阅管理器，格式转换 | [sub-store-org/Sub-Store](https://github.com/sub-store-org/Sub-Store) | ⭐ 9.9k+ |
| **subconverter** | 订阅格式转换器（全部客户端格式） | [tindy2013/subconverter](https://github.com/tindy2013/subconverter) | ⭐ 15.9k+ |
| **ACL4SSR** | 规则集生成与转换 | [acl4ssr/ACL4SSR](https://github.com/acl4ssr/ACL4SSR) | ⭐ 5.8k+ |
| **singbox2proxy** | 在 HTTP 客户端中使用 sing-box 代理 | [nichind/singbox2proxy](https://github.com/nichind/singbox2proxy) | ⭐ 1k+ |

---

## 📋 路由规则

| 规则集 | 描述 | GitHub | Stars |
|--------|------|--------|-------|
| **clash-rules** | Clash Premium 规则集（最流行） | [Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules) | ⭐ 26k+ |
| **chn-iplist** | 中国 IP 路由规则（多客户端） | [PaPerseller/chn-iplist](https://github.com/PaPerseller/chn-iplist) | ⭐ 1.2k+ |
| **china_ip_list** | 中国 IP 列表 | [17mon/china_ip_list](https://github.com/17mon/china_ip_list) | ⭐ 4k+ |
| **geoip/Geolite2** | MaxMind GeoIP 数据库 | [P3TERX/GeoLite.mmdb](https://github.com/P3TERX/GeoLite.mmdb) | ⭐ 3k+ |
| **domain-list-community** | Clash 社区域名列表 | [v2fly/domain-list-community](https://github.com/v2fly/domain-list-community) | ⭐ 5k+ |

---

## ⚡ 一键安装脚本

| 脚本 | 协议 | 特性 | GitHub | Stars |
|------|------|------|--------|-------|
| **v2ray-agent** | Xray/Tuic/H2/sing-box 八合一 | 最全面 | [mack-a/v2ray-agent](https://github.com/mack-a/v2ray-agent) | ⭐ 20k+ |
| **233boy/v2ray** | V2Ray 经典 | 最流行 | [233boy/v2ray](https://github.com/233boy/v2ray) | ⭐ 28.8k+ |
| **sing-box-yg** | sing-box 五合一 | Argo 隧道、Psiphon | [yonggekkk/sing-box-yg](https://github.com/yonggekkk/sing-box-yg) | ⭐ 8.3k+ |
| **Xray_onekey** | VLESS + XTLS | 早期流行安装器 | [wulabing/Xray_onekey](https://github.com/wulabing/Xray_onekey) | ⭐ 9.3k+ |
| **reality-ezpz** | VLESS/TuIC/H2/ShadowTLS | Docker Compose, Telegram Bot | [aleskxyz/reality-ezpz](https://github.com/aleskxyz/reality-ezpz) | ⭐ 1.5k+ |
| **ArgoX** | Argo + Xray | Cloudflare Argo 集成 | [fscarmen/ArgoX](https://github.com/fscarmen/ArgoX) | ⭐ 1.8k+ |

---

## 📋 免费代理列表

### 高频自动更新列表

| 项目 | 协议 | 更新频率 | GitHub | Stars |
|------|------|---------|--------|-------|
| **Free-servers** | VMess/VLESS/Trojan/SS | 每 6 小时 | [Pawdroid/Free-servers](https://github.com/Pawdroid/Free-servers) | ⭐ 19.6k+ |
| **v2rayfree** | V2Ray 免费节点 | 每 6 小时 + 测速 | [aiboboxx/v2rayfree](https://github.com/aiboboxx/v2rayfree) | ⭐ 14k+ |
| **aggregator** | 全部主流 | 自动爬取 + 验证 | [wzdnzd/aggregator](https://github.com/wzdnzd/aggregator) | ⭐ 6.7k+ |
| **ermaozi/get_subscribe** | Clash/V2Ray/Trojan/SSR | 自动 | [ermaozi/get_subscribe](https://github.com/ermaozi/get_subscribe) | ⭐ 8.7k+ |
| **AutoMergePublicNodes** | 全部主流 | 自动爬取 | [chengaopan/AutoMergePublicNodes](https://github.com/chengaopan/AutoMergePublicNodes) | ⭐ 7.3k+ |
| **V2RayAggregator** | SS/SSR/Trojan/VMess | 速度过滤 | [mahdibland/V2RayAggregator](https://github.com/mahdibland/V2RayAggregator) | ⭐ 4k+ |
| **Barabama/FreeNodes** | V2Ray/Clash | 自动更新 | [Barabama/FreeNodes](https://github.com/Barabama/FreeNodes) | ⭐ 2.7k+ |
| **proxypool** | 代理/节点/VPN | Go 代理池 | [snakem982/proxypool](https://github.com/snakem982/proxypool) | ⭐ 1.8k+ |
| **vxiaov/free_proxy_ss** | SS/SSR/V2Ray/Clash | 每 2 小时 | [vxiaov/free_proxy_ss](https://github.com/vxiaov/free_proxy_ss) | ⭐ 2.4k+ |
| **ripaojiedian/freenode** | SS/SSR/VMess/VLESS/Trojan | 永久链接 | [ripaojiedian/freenode](https://github.com/ripaojiedian/freenode) | ⭐ 2.2k+ |

### 专项列表

| 项目 | 协议 | 独特功能 | GitHub |
|------|------|---------|--------|
| **OpenRay** | VMess/VLESS/Trojan/SS/H2/TUIC/Juicity | 按国家分类 | [sakha1370/OpenRay](https://github.com/sakha1370/OpenRay) |
| **free-proxy-list** | 10+ 协议含 mtproto | 每 30 分钟更新 | [gfpcom/free-proxy-list](https://github.com/gfpcom/free-proxy-list) |
| **ProxyCollector** | VMess/VLESS/Trojan/SS/H2/TUIC | 50+ 源订阅，sing-box 测试 | [Mahdi0024/ProxyCollector](https://github.com/Mahdi0024/ProxyCollector) |
| **v2ray-configs** | VLESS/VMess/SS/Trojan | 每 5 分钟更新 | [Epodonios/v2ray-configs](https://github.com/Epodonios/v2ray-configs) |
| **v2ray-config** | V2Ray | 每个链接通过 TLS 隧道验证 | [morpheusadam/v2ray-config](https://github.com/morpheusadam/v2ray-config) |
| **am-cf-tunnel** | VLESS/Trojan | Cloudflare Workers/Pages 脚本 | [amclubs/am-cf-tunnel](https://github.com/amclubs/am-cf-tunnel) |

---

## 🔧 工具与实用程序

### 代理检测与抓取

| 工具 | 语言 | 特性 | GitHub | Stars |
|------|------|------|--------|-------|
| **ProxyBroker** | Python | 发现、检测、服务 | [constverum/ProxyBroker](https://github.com/constverum/ProxyBroker) | ⭐ 3k+ |
| **proxy_pool** | Python | 收集、验证、HTTP API 服务 | [jhao104/proxy_pool](https://github.com/jhao104/proxy_pool) | ⭐ 23k+ |
| **proxy-scraper-checker** | Rust | 快速抓取 + 验证 + GeoIP | [monosans/proxy-scraper-checker](https://github.com/monosans/proxy-scraper-checker) | ⭐ 1.3k+ |
| **checked-proxy-list** | Go | TUI 命令行 | [ClearProxy/checked-proxy-list](https://github.com/ClearProxy/checked-proxy-list) | ⭐ 97+ |
| **Valid8Proxy** | Python | 多线程验证 | [spyboy-productions/Valid8Proxy](https://github.com/spyboy-productions/Valid8Proxy) | ⭐ 267+ |

### 轮换与管理

| 工具 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **rota** | 高性能轮换引擎 | [alpkeskin/rota](https://github.com/alpkeskin/rota) | ⭐ 1k+ |
| **proxybroker2** | 自动轮换代理发现 | [bluet/proxybroker2](https://github.com/bluet/proxybroker2) | ⭐ 500+ |

### 透明代理

| 工具 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **ss-tproxy** | ss/v2ray/xray/trojan/hysteria 透明代理 | [zfl9/ss-tproxy](https://github.com/zfl9/ss-tproxy) | ⭐ 2.4k+ |
| **python-proxy** | 异步 HTTP/HTTPS/SOCKS4/5/SS/SSH 代理 | [qwj/python-proxy](https://github.com/qwj/python-proxy) | ⭐ 2.2k+ |

### 开发库

| 库 | 语言 | 用途 | GitHub | Stars |
|----|------|------|--------|-------|
| **kcp-go** | Go | UDP 可靠传输 | [xtaci/kcp-go](https://github.com/xtaci/kcp-go) | ⭐ 4k+ |
| **quic-go** | Go | QUIC 协议 | [quic-go/quic-go](https://github.com/quic-go/quic-go) | ⭐ 10k+ |
| **masque-go** | Go | MASQUE 代理 | [quic-go/masque-go](https://github.com/quic-go/masque-go) | ⭐ 500+ |

### 配置示例

| 项目 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **integrated-examples** | Nginx/Caddy + V2Ray/Xray/Hysteria/TUIC 配置 | [lxhao61/integrated-examples](https://github.com/lxhao61/integrated-examples) | ⭐ 2.5k+ |

---

## ☁️ Cloudflare & WARP

| 项目 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **am-cf-tunnel** | CF Workers/Pages 用于 VLESS/Trojan | [amclubs/am-cf-tunnel](https://github.com/amclubs/am-cf-tunnel) | ⭐ 3k+ |
| **ArgoX** | Argo + Xray for VPS | [fscarmen/ArgoX](https://github.com/fscarmen/ArgoX) | ⭐ 1.8k+ |
| **cloudflared** | 官方 CF Tunnel 客户端 | [cloudflare/cloudflared](https://github.com/cloudflare/cloudflared) | ⭐ 10k+ |
| **wgcf** | 生成 WARP WireGuard 配置 | [Vi3merH/wgcf](https://github.com/Vi3merH/wgcf) | ⭐ 6k+ |
| **warp-plus** | 生成无限 WARP+ 流量 | [YirsisFers/warp-plus](https://github.com/YirsisFers/warp-plus) | ⭐ 3k+ |

---

## 🛡️ 抗审查资源

| 资源 | 描述 | GitHub | Stars |
|------|------|--------|-------|
| **awesome-anticensor** | 结构化审查对抗列表 | [marzneshin/awesome-anticensor](https://github.com/marzneshin/awesome-anticensor) | ⭐ 38+ |
| **awesome-freedom** | 面板、脚本、Bot、教程 | [erfjab/awesome-freedom](https://github.com/erfjab/awesome-freedom) | ⭐ 153+ |
| **awesome-vpn** | 免费代理节点聚合 + 列表 | [awesome-vpn/awesome-vpn](https://github.com/awesome-vpn/awesome-vpn) | ⭐ 6.8k+ |
| **awesome-tunneling** | ngrok/CF Tunnel 替代方案 | [anderspitman/awesome-tunneling](https://github.com/anderspitman/awesome-tunneling) | ⭐ 21k+ |
| **awesome-wireguard** | WireGuard 工具与项目 | [cedrickchee/awesome-wireguard](https://github.com/cedrickchee/awesome-wireguard) | ⭐ 1.5k+ |

---

## 📚 学习资源

### 官方文档
- [sing-box 官方文档](https://sing-box.sagernet.org/)
- [Xray-core 文档](https://xtls.github.io/)
- [Clash Wiki](https://wiki.clash.wiki/)
- [Hysteria 2 文档](https://hysteria.network/)
- [Mihomo 文档](https://wiki.metacubex.one/)

### 社区
- [r/dumbclub](https://reddit.com/r/dumbclub) — 代理讨论
- [r/V2Ray](https://reddit.com/r/V2Ray) — V2Ray 社区

### 文章与指南
- [VLESS + Reality + XTLS 配置指南](https://www.jamesflare.com/vless-tcp-reality-xtls-utls-xudp)
- [用 sing-box 搭建私有代理](https://www.scrapingbee.com/blog/how-to-build-private-proxy-server)
- [9 个开源反向代理](https://carlosmv.hashnode.dev/9-open-source-reverse-proxies-you-need-to-know)
- [yonggekkk 博客](https://github.com/yonggekkk) — 大量部署教程

---

## 🔮 2026 技术趋势

1. **从 TCP 转向 UDP/QUIC** — HTTP/3 普及驱动基于 QUIC 的协议
2. **从加密转向伪装** — 简单 AES 已不够，指纹伪装和 Reality 才是核心
3. **后量子加密 (PQC)** — SSH 和 WireGuard 开始引入抗量子算法
4. **AI 流量分析对抗** — 协议必须能抵御基于机器学习的流量分类
5. **多协议叠加** — 同时运行多种协议类型以增强韧性
6. **Cloudflare Worker 代理** — 无服务器代理部署成为主流
7. **内核级代理** — dae/sing-box TUN 替代用户态代理以提升性能

> 💡 建议：在您的客户端中至少储备两种不同类型的协议（如一个 Reality 搭配一个 Hysteria 2），以应对不同时期的网络波动。

---

## 🤝 贡献指南

欢迎贡献！请参阅 [CONTRIBUTING.md](../../CONTRIBUTING.md)。

### 贡献方向
- 添加新协议或工具
- 翻译文档
- 更新失效链接
- 改进分类
- 添加性能基准测试

## 📜 许可证

本项目采用 MIT 许可证 — 详见 [LICENSE](../../LICENSE)。

---

<p align="center">
  <sub>由社区用心构建，服务社区。</sub><br/>
  <sub>150+ 条目 · 12 大类 · 4 种语言</sub><br/>
  <sub>最后更新：2026-10-29</sub>
</p>
