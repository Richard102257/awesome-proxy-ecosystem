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
  <img src="https://img.shields.io/badge/客户端-20+-green" alt="Clients"/>
  <img src="https://img.shields.io/badge/平台-8+-orange" alt="Platforms"/>
  <img src="https://img.shields.io/badge/license-MIT-success" alt="License"/>
</p>

---

## 📖 项目简介

本项目是一个全面的、精心整理的代理协议、实现、客户端和生态系统资源集合。整合了来自 [jichangzhu.org/protocols](https://jichangzhu.org/protocols/) 以及多个 GitHub awesome 列表的信息。

无论您是开发者、研究人员还是注重隐私的用户，本指南都能帮助您穿越复杂的代理技术版图。

> 📌 数据基于对市面上 **35+ 种协议** 的深度实测与评估。

## 📑 目录

- [快速入门](#-快速入门)
- [协议分类总览](#-协议分类总览)
- [核心协议深度解析](#-核心协议深度解析)
- [客户端软件](#-客户端软件)
- [服务端面板与管理](#-服务端面板与管理)
- [代理平台与框架](#-代理平台与框架)
- [免费代理列表](#-免费代理列表)
- [工具与实用程序](#-工具与实用程序)
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

| 客户端 | 平台 | 支持协议 | GitHub |
|--------|------|---------|--------|
| **sing-box** | Win/Mac/Linux/Android/iOS | 全部主流 | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) |
| **Clash Meta (Mihomo)** | Win/Mac/Linux | VMess/VLESS/SS/Trojan/TUIC/H2 | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) |
| **Hiddify** | 全平台 | 全部主流 | [hiddify/hiddify-app](https://github.com/hiddify/hiddify-app) |
| **Clash Verge Rev** | Win/Mac/Linux | 基于 Clash | [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev) |
| **NekoBox** | Android | SS/V2Ray/sing-box | [MatsuriDayo/NekoBoxForAndroid](https://github.com/MatsuriDayo/NekoBoxForAndroid) |
| **v2rayN** | Windows | VMess/VLESS/SS/Trojan | [2dust/v2rayN](https://github.com/2dust/v2rayN) |
| **v2rayNG** | Android | VMess/VLESS/SS/Trojan | [2dust/v2rayNG](https://github.com/2dust/v2rayNG) |
| **Shadowrocket** | iOS/tvOS | 全部主流 | App Store |
| **Surge** | macOS/iOS | 全部主流 | 商业软件 |
| **Stash** | macOS/iOS | 全部主流 | App Store |
| **V2RayA** | Linux (Web GUI) | V2Ray/Xray/sing-box | [v2rayA/v2rayA](https://github.com/v2rayA/v2rayA) |

---

## 🖥️ 服务端面板与管理

| 面板 | 支持协议 | 特性 | GitHub |
|------|---------|------|--------|
| **3X-UI** | VLESS/VMess/Trojan/H2/TUIC | Web GUI，多用户，流量控制 | [MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui) |
| **X-UI** | VLESS/VMess/Trojan | 简洁 Web 面板 | [FranzKafkaYu/x-ui](https://github.com/FranzKafkaYu/x-ui) |
| **Hiddify Manager** | 全部主流 | 多服务器管理 | [hiddify/hiddify-manager](https://github.com/hiddify/hiddify-manager) |
| **Marzban** | VLESS/VMess/Trojan | 多协议，Telegram Bot | [Gozargah/Marzban](https://github.com/Gozargah/Marzban) |

---

## 🏗️ 代理平台与框架

### 通用代理平台

| 项目 | 语言 | 支持协议 | GitHub |
|------|------|---------|--------|
| **sing-box** | Go | SS/VMess/VLESS/Trojan/TUIC/H2/Naive/WG | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) |
| **Xray-core** | Go | VLESS/VMess/Trojan/Reality/XTLS | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) |
| **v2ray-core** | Go | VMess/VLESS/SS/Trojan | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) |
| **Clash** | Go | SS/VMess/VLESS/Trojan/SOCKS5/HTTP | [Dreamacro/clash](https://github.com/Dreamacro/clash) |
| **mihomo** | Go | Clash + TUIC/H2/Reality | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) |
| **GOST** | Go | 多协议链式代理 | [go-gost/gost](https://github.com/go-gost/gost) |

### 反向代理与负载均衡

| 项目 | 描述 | GitHub |
|------|------|--------|
| **Nginx** | 高性能 HTTP/反向代理 | [nginx/nginx](https://github.com/nginx/nginx) |
| **Caddy** | 自动 HTTPS 反向代理 | [caddyserver/caddy](https://github.com/caddyserver/caddy) |
| **Traefik** | 云原生反向代理 | [traefik/traefik](https://github.com/traefik/traefik) |
| **Envoy** | 服务网格 L7 代理 | [envoyproxy/envoy](https://github.com/envoyproxy/envoy) |
| **HAProxy** | TCP/HTTP 负载均衡 | [haproxy/haproxy](https://github.com/haproxy/haproxy) |
| **FRP** | 快速反向代理 | [fatedier/frp](https://github.com/fatedier/frp) |
| **Rathole** | 高性能反向代理 | [rapiz1/rathole](https://github.com/rapiz1/rathole) |

---

## 📋 免费代理列表

| 项目 | 协议 | 更新频率 | GitHub |
|------|------|---------|--------|
| **OpenRay** | VMess/VLESS/Trojan/SS/H2/TUIC/Juicity | 每小时 | [sakha1370/OpenRay](https://github.com/sakha1370/OpenRay) |
| **free-proxy-list** | SS/SSSR/V2Ray/Trojan/H2/TUIC/WG | 每 30 分钟 | [gfpcom/free-proxy-list](https://github.com/gfpcom/free-proxy-list) |
| **openproxylist** | HTTPS/SOCKS4/SOCKS5/V2Ray | 每小时 | [roosterkid/openproxylist](https://github.com/roosterkid/openproxylist) |
| **proxylist** | HTTP/SOCKS5 | 实时 | [elliottophellia/proxylist](https://github.com/elliottophellia/proxylist) |

---

## 🔧 工具与实用程序

### 代理检测与抓取

| 工具 | 语言 | 特性 | GitHub |
|------|------|------|--------|
| **ProxyBroker** | Python | 发现、检测、服务 | [constverum/ProxyBroker](https://github.com/constverum/ProxyBroker) |
| **proxy-scraper-checker** | Rust | 快速抓取+检测 | [monosans/proxy-scraper-checker](https://github.com/monosans/proxy-scraper-checker) |
| **checked-proxy-list** | Go | TUI 命令行 | [ClearProxy/checked-proxy-list](https://github.com/ClearProxy/checked-proxy-list) |
| **Valid8Proxy** | Python | 多线程验证 | [spyboy-productions/Valid8Proxy](https://github.com/spyboy-productions/Valid8Proxy) |

### 轮换与管理

| 工具 | 描述 | GitHub |
|------|------|--------|
| **rota** | 高性能轮换引擎 | [alpkeskin/rota](https://github.com/alpkeskin/rota) |
| **proxybroker2** | 自动轮换代理发现 | [bluet/proxybroker2](https://github.com/bluet/proxybroker2) |
| **singbox2proxy** | 在 HTTP 客户端中使用 sing-box 代理 | [nichind/singbox2proxy](https://github.com/nichind/singbox2proxy) |

---

## 📚 学习资源

### 官方文档
- [sing-box 官方文档](https://sing-box.sagernet.org/)
- [Xray-core 文档](https://xtls.github.io/)
- [Clash Wiki](https://wiki.clash.wiki/)
- [Hysteria 2 文档](https://hysteria.network/)

### 社区
- [r/dumbclub](https://reddit.com/r/dumbclub) — 代理讨论
- [r/V2Ray](https://reddit.com/r/V2Ray) — V2Ray 社区

---

## 🔮 2026 技术趋势

1. **从 TCP 转向 UDP/QUIC** — HTTP/3 普及驱动基于 QUIC 的协议（Masque、Juicity、TUIC）
2. **从加密转向伪装** — 简单 AES 已不够，指纹伪装（uTLS）和身份偷取（Reality）才是核心
3. **后量子加密 (PQC)** — SSH 和 WireGuard 开始引入抗量子算法
4. **AI 流量分析对抗** — 协议必须能抵御基于机器学习的流量分类
5. **多协议叠加** — 同时运行多种协议类型以增强韧性

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
  <sub>最后更新：2026-10-29</sub>
</p>
