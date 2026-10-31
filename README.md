# 🌐 Awesome Proxy Ecosystem

<p align="center">
  <b>The Ultimate Curated List of Proxy Protocols, Tools, and Resources</b><br/>
  <i>终极代理协议、工具与资源精选</i>
</p>

<p align="center">
  <a href="README.md">English</a> ｜
  <a href="docs/zh-CN/README.md">简体中文</a> ｜
  <a href="docs/ja/README.md">日本語</a> ｜
  <a href="docs/ko/README.md">한국어</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/protocols-35+-blue" alt="Protocols"/>
  <img src="https://img.shields.io/badge/clients-30+-green" alt="Clients"/>
  <img src="https://img.shields.io/badge/panels-15+-orange" alt="Panels"/>
  <img src="https://img.shields.io/badge/tools-25+-purple" alt="Tools"/>
  <img src="https://img.shields.io/badge/total%20entries-150+-red" alt="Total"/>
  <img src="https://img.shields.io/badge/languages-4-success" alt="Languages"/>
  <img src="https://img.shields.io/github/license/awesome-proxy-ecosystem/awesome-proxy-ecosystem" alt="License"/>
</p>

---

## 📖 Overview

This project is the most comprehensive, curated collection of proxy protocols, implementations, clients, panels, tunneling tools, and ecosystem resources. It consolidates information from:

- [jichangzhu.org/protocols](https://jichangzhu.org/protocols/) — In-depth protocol testing and comparison
- [drsoft-oss/awesome-proxy](https://github.com/drsoft-oss/awesome-proxy) — Collaborative proxy resources
- [awesome-tunneling](https://github.com/anderspitman/awesome-tunneling) — Tunneling tools (21k+ stars)
- [awesome-wireguard](https://github.com/cedrickchee/awesome-wireguard) — WireGuard ecosystem (1.5k+ stars)
- [awesome-anticensor](https://github.com/marzneshin/awesome-anticensor) — Censorship circumvention
- [awesome-freedom](https://github.com/erfjab/awesome-freedom) — Panels, scripts, bots (153+ stars)
- And many more GitHub awesome lists and standalone projects

**150+ entries** across protocols, clients, panels, platforms, tools, scripts, and resources.

## 📑 Table of Contents

- [Quick Start Guide](#-quick-start-guide)
- [Protocol Classification](#-protocol-classification)
- [Core Protocols Deep Dive](#-core-protocols-deep-dive)
- [💻 Client Software](#-client-software)
- [Server Panels & Management](#-server-panels--management)
- [Proxy Platforms & Frameworks](#-proxy-platforms--frameworks)
- [Tunneling Tools](#-tunneling-tools)
- [Subscription Management](#-subscription-management)
- [Routing Rules](#-routing-rules)
- [One-Click Install Scripts](#-one-click-install-scripts)
- [Free Proxy Lists](#-free-proxy-lists)
- [Tools & Utilities](#-tools--utilities)
- [Cloudflare & WARP](#-cloudflare--warp)
- [Anti-Censorship Resources](#-anti-censorship-resources)
- [Learning Resources](#-learning-resources)
- [2026 Technology Trends](#-2026-technology-trends)
- [Contributing](#-contributing)

## 🚀 Quick Start Guide

### Choose Your Protocol

| Your Need | Recommended Protocol | Why |
|-----------|---------------------|-----|
| Maximum stealth | **VLESS-Reality**, **NaiveProxy** | Fingerprint spoofing, untraceable |
| Maximum speed | **Hysteria 2**, **TUIC v5** | UDP brute-force, 0-RTT |
| Gaming / Low latency | **Shadowsocks-2022**, **ShadowQUIC** | Thin encryption, efficient UDP |
| Router / Embedded | **SS-2022**, **Brook** | Minimal resource usage |
| Apple ecosystem | **Mieru**, **Trojan**, **Sudoku** | Low maintenance, private protocols |
| General purpose | **VMess**, **VLESS-XTLS** | Mature ecosystem |

### Decision Tree

```
Do you have a domain name?
├── YES → Do you need maximum performance?
│   ├── YES → VLESS-XTLS-Vision
│   └── NO → VLESS-Reality
└── NO → Do you need maximum stealth?
    ├── YES → AnyTLS-Reality or VLESS-Reality
    └── NO → Hysteria 2 (if bad network) or SS-2022 (if limited hardware)
```

### Quick Setup

```bash
# One-click install (choose one):
# Option A: sing-box multi-protocol (recommended)
bash -c "$(curl -fsSL https://raw.githubusercontent.com/yonggekkk/sing-box-yg/main/install.sh)"

# Option B: Xray/Tuic/Hysteria2 8-in-one
bash -c "$(curl -fsSL https://raw.githubusercontent.com/mack-a/v2ray-agent/main/install.sh)"

# Option C: V2Ray classic
curl -Ls https://raw.githubusercontent.com/233boy/v2ray/master/v2ray.sh | bash
```

## 📊 Protocol Classification

### 🏆 Tier 1 — Stealth Champions (隐匿天花板)

| Protocol | Status | GitHub | Features |
|----------|--------|--------|----------|
| **VLESS-Reality** | ✅ Active | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | Steals real website fingerprints, zero TLS features |
| **NaiveProxy** | ✅ Active | [klzgrad/naiveproxy](https://github.com/klzgrad/naiveproxy) | Uses Chrome network stack, blends with browser traffic |
| **AnyTLS** | ✅ Active | [anytls/anytls-go](https://github.com/anytls/anytls-go) | Minimal TLS proxy, extremely hard to detect |

### 🚀 Tier 2 — Speed Demons (暴力加速派)

| Protocol | Status | GitHub | Features |
|----------|--------|--------|----------|
| **Hysteria 2** | ✅ Active | [apernet/hysteria](https://github.com/apernet/hysteria) | Brutal congestion control, works on 20% packet loss |
| **TUIC v5** | ✅ Active | [tuic-protocol/tuic](https://github.com/tuic-protocol/tuic) | QUIC-based, multiplexed, mobile-friendly |
| **Juicity** | ✅ Active | [juicity/juicity](https://github.com/juicity/juicity) | QUIC protocol, fast & lightweight |

### ⚡ Tier 3 — Lightweight Performers (轻量性能派)

| Protocol | Status | GitHub | Features |
|----------|--------|--------|----------|
| **Shadowsocks-2022** | ✅ Active | [shadowsocks/shadowsocks-rust](https://github.com/shadowsocks/shadowsocks-rust) | Low latency, efficient AEAD, UDP optimized |
| **Brook** | ✅ Active | [txthinking/brook](https://github.com/txthinking/brook) | Simple, fast, cross-platform |
| **Vlite** | ✅ Active | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | Lightweight V2Ray variant |

### 👻 Tier 4 — Stealth Minimalists (极简隐形派)

| Protocol | Status | GitHub | Features |
|----------|--------|--------|----------|
| **Mieru** | ✅ Active | [enclica/mieru](https://github.com/enclica/mieru) | Hard to classify, hard to probe |
| **Trojan** | ✅ Active | [trojan-gfw/trojan](https://github.com/trojan-gfw/trojan) | Mimics HTTPS traffic |
| **Sudoku** | ✅ Active | [SUDOKU-ASCII/sudoku](https://github.com/SUDOKU-ASCII/sudoku) | Novel obfuscation via Sudoku puzzles |

### 🔄 Tier 5 — Classic All-Rounders (经典全能型)

| Protocol | Status | GitHub | Features |
|----------|--------|--------|----------|
| **VMess** | ⚠️ Archived | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | Mature ecosystem, widely supported |
| **VLESS-XTLS** | ✅ Active | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | XTLS Vision/Reality flow control |
| **SSR** | ❌ Deprecated | [shadowsocksrr](https://github.com/shadowsocksrr) | Historical significance |

### 🔐 Tier 6 — Infrastructure Security (底层安全类)

| Protocol | Status | GitHub | Features |
|----------|--------|--------|----------|
| **WireGuard** | ✅ Active | [WireGuard](https://github.com/WireGuard) | Industrial-grade VPN, post-quantum ready |
| **Tor** | ✅ Active | [torproject/tor](https://github.com/torproject/tor) | Anonymous routing, onion services |
| **SSH** | ✅ Active | [openssh](https://github.com/openssh/openssh-portable) | SOCKS5 tunneling, post-quantum support |
| **kcptun** | ✅ Active | [xtaci/kcp-go](https://github.com/xtaci/kcp-go) | UDP-based reliable acceleration |

### 🌐 Tier 7 — Transport & Legacy Protocols (传输与传统协议)

| Protocol | Status | GitHub | Features |
|----------|--------|--------|----------|
| **Shadow-TLS** | ✅ Active | [ihciah/shadow-tls](https://github.com/ihciah/shadow-tls) | Wraps TLS to look like normal HTTPS |
| **Snell** | ✅ Active | [Surge](https://kb.nssurge.com) | By Surge developer, Apple ecosystem |
| **Masque** | ✅ Active | [quic-go/masque-go](https://github.com/quic-go/masque-go) | QUIC/HTTP-3 tunneling |
| **MTProto** | ✅ Active | [Telegram](https://core.telegram.org/mtproto) | Telegram proxy protocol |
| **SOCKS5** | ✅ Active | Standard | Universal proxy protocol |
| **HTTP Proxy** | ✅ Active | Standard | Basic forward proxy |
| **Fragment** | ✅ Active | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) | TCP fragmentation against censorship |
| **ShadowQUIC** | ✅ Active | [spongebob888/shadowquic](https://github.com/spongebob888/shadowquic) | SS stealth + QUIC multiplexing |
| **GOST** | ✅ Active | [go-gost/gost](https://github.com/go-gost/gost) | Multi-protocol security proxy |
| **TrustTunnel** | ✅ Active | [TrustTunnel/TrustTunnel](https://github.com/TrustTunnel/TrustTunnel) | AdGuard's obfuscated VPN |

## 🔬 Core Protocols Deep Dive

### VLESS + Reality

The gold standard for censorship circumvention in 2026.

```
[Client] → VLESS → Reality (spoofs TLS to look like target.com) → [Server]
```

- **No domain required** — borrows real website certificates
- **Zero TLS fingerprint** — uses uTLS to mimic real browsers
- **Forward secrecy** — each session has unique keys

**Implementation:** [XTLS/Xray-core](https://github.com/XTLS/Xray-core) · [SagerNet/sing-box](https://github.com/SagerNet/sing-box)

### Hysteria 2

UDP-based brute-force protocol for terrible networks.

```
[Client] → Hysteria 2 (Brutal CC) → UDP flood → [Server]
```

- **Brutal congestion control** — sends data at declared rate regardless of loss
- **Works at 20%+ packet loss** — designed for terrible international routes
- **Based on QUIC** — modern transport protocol

**Implementation:** [apernet/hysteria](https://github.com/apernet/hysteria)

### Shadowsocks-2022

The low-latency champion.

```
[Client] → SS-2022 (AEAD 2022) → Session-based encryption → [Server]
```

- **Session-based keys** — each session derives unique keys from HKDF
- **UDP over TCP tunneling** — efficient UDP handling
- **Minimal overhead** — thin encryption layer

**Implementation:** [shadowsocks/shadowsocks-rust](https://github.com/shadowsocks/shadowsocks-rust)

### NaiveProxy

The ultimate camouflage.

```
[Client] → NaiveProxy (Chrome net stack) → Looks exactly like Chrome → [Server]
```

- **Uses Chrome's network stack** — identical TLS fingerprint to Chrome
- **HTTP/2 multiplexing** — efficient parallel streams
- **Hard to block without blocking Chrome itself**

**Implementation:** [klzgrad/naiveproxy](https://github.com/klzgrad/naiveproxy)

## 💻 Client Software

### Cross-Platform Clients

| Client | Platforms | Protocols | GitHub | Stars |
|--------|-----------|-----------|--------|-------|
| **sing-box** | Win/Mac/Linux/Android/iOS | All major | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) | ⭐ 25k+ |
| **Clash Verge Rev** | Win/Mac/Linux | Clash-based | [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev) | ⭐ 126k+ |
| **v2rayN** | Win/Mac/Linux | Xray/sing-box | [2dust/v2rayN](https://github.com/2dust/v2rayN) | ⭐ 118k+ |
| **Hiddify** | All platforms | All major | [hiddify/hiddify-app](https://github.com/hiddify/hiddify-app) | ⭐ 33k+ |
| **FlClash** | Win/Mac/Linux/Android | Clash Meta | [chen08209/FlClash](https://github.com/chen08209/FlClash) | ⭐ 42k+ |
| **Clash Meta (Mihomo)** | Win/Mac/Linux | VMess/VLESS/SS/Trojan/TUIC/H2 | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) | ⭐ 25k+ |
| **NekoBox** | Android | SS/V2Ray/sing-box | [MatsuriDayo/NekoBoxForAndroid](https://github.com/MatsuriDayo/NekoBoxForAndroid) | ⭐ 21k+ |
| **nekoray** | Win/Mac/Linux | sing-box/Xray | [MatsuriDayo/nekoray](https://github.com/MatsuriDayo/nekoray) | ⭐ 15k+ |
| **v2rayNG** | Android | VMess/VLESS/SS/Trojan | [2dust/v2rayNG](https://github.com/2dust/v2rayNG) | ⭐ 30k+ |
| **Karing** | Win/Mac/Linux/Android/iOS | Clash/sing-box | [KaringX/karing](https://github.com/KaringX/karing) | ⭐ 11k+ |
| **GUI.for.SingBox** | Win/Mac/Linux | sing-box | [GUI-for-Cores/GUI.for.SingBox](https://github.com/GUI-for-Cores/GUI.for.SingBox) | ⭐ 7.6k+ |
| **V2RayA** | Linux (Web GUI) | V2Ray/Xray/sing-box | [v2rayA/v2rayA](https://github.com/v2rayA/v2rayA) | ⭐ 8.5k+ |
| **Throne** | Win/Mac/Linux | sing-box | [throneproj/Throne](https://github.com/throneproj/Throne) | ⭐ 5.4k+ |
| **Shadowrocket** | iOS/tvOS | All major | App Store | — |
| **Surge** | macOS/iOS | All major | Commercial | — |
| **Stash** | macOS/iOS | All major | App Store | — |
| **Qv2ray** | Win/Mac/Linux | V2Ray (plugin) | [Qv2ray/Qv2ray](https://github.com/Qv2ray/Qv2ray) | Archived |

### Client Platform Support Matrix

| Client | Windows | macOS | Linux | Android | iOS | Router/OpenWrt |
|--------|---------|-------|-------|---------|-----|----------------|
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

## 🖥️ Server Panels & Management

### Xray / Sing-box Panels

| Panel | Protocols | Features | GitHub | Stars |
|-------|-----------|----------|--------|-------|
| **3X-UI** | 13+ protocols, XTLS+REALITY | Web GUI, multi-user, bots, PostgreSQL | [MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui) | ⭐ 35k+ |
| **X-UI** | VLESS/VMess/Trojan | Simple web panel | [vaxilu/x-ui](https://github.com/vaxilu/x-ui) | ⭐ 19k+ |
| **s-ui** | sing-box | Advanced Web Panel | [alireza0/s-ui](https://github.com/alireza0/s-ui) | ⭐ 8.6k+ |
| **x-ui (EN)** | VLESS/VMess/Trojan | English + Telegram bot | [alireza0/x-ui](https://github.com/alireza0/x-ui) | ⭐ 4k+ |
| **x-ui-yg** | H2, Xhttp, ENC, Argo, Psiphon | Modified x-ui with extra features | [yonggekkk/x-ui-yg](https://github.com/yonggekkk/x-ui-yg) | ⭐ 3.5k+ |
| **XUI-PRO** | 15+ protocols + WARP + Psiphon | Nginx reverse proxy integration | [GFW4Fun/x-ui-pro](https://github.com/GFW4Fun/x-ui-pro) | ⭐ 1.2k+ |

### Multi-Protocol / Python Panels

| Panel | Protocols | Features | GitHub | Stars |
|-------|-----------|----------|--------|-------|
| **Hiddify Manager** | 20+ protocols | Multi-server, anti-filtering | [hiddify/Hiddify-Manager](https://github.com/hiddify/Hiddify-Manager) | ⭐ 9.4k+ |
| **Marzban** | VLESS/VMess/Trojan | Scalable, Telegram bot | [Gozargah/Marzban](https://github.com/Gozargah/Marzban) | ⭐ 6.6k+ |
| **Remnawave** | Xray-core | TypeScript-based, modern UI | [remnawave/panel](https://github.com/remnawave/panel) | ⭐ 3.8k+ |
| **Libertea** | VLESS | Simple, lightweight | [Libertea/Libertea](https://github.com/Libertea/Libertea) | ⭐ 1k+ |
| **sspanel-uim** | Multi-protocol | Commercial-grade panel | [anankke/sspanel-uim](https://github.com/anankke/sspanel-uim) | ⭐ 10k+ |
| **Marzneshin** | Xray-based | Successor to Marzban | [marzneshin/marzneshin](https://github.com/marzneshin/marzneshin) | ⭐ 2k+ |

## 🏗️ Proxy Platforms & Frameworks

### Universal Proxy Platforms

| Project | Language | Protocols | GitHub | Stars |
|---------|----------|-----------|--------|-------|
| **sing-box** | Go | SS/VMess/VLESS/Trojan/TUIC/H2/Naive/WG/Shadow-TLS | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) | ⭐ 25k+ |
| **Xray-core** | Go | VLESS/VMess/Trojan/Reality/XTLS | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | ⭐ 35k+ |
| **v2ray-core** | Go | VMess/VLESS/SS/Trojan | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | ⭐ 25k+ |
| **Clash** | Go | SS/VMess/VLESS/Trojan/SOCKS5/HTTP | [Dreamacro/clash](https://github.com/Dreamacro/clash) | Archived |
| **mihomo** | Go | Clash + TUIC/H2/Reality | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) | ⭐ 25k+ |
| **clash-rs** | Rust | Clash protocol reimplementation | [Watfaq/clash-rs](https://github.com/Watfaq/clash-rs) | ⭐ 1.6k+ |
| **GOST** | Go | Multi-protocol chain proxy | [go-gost/gost](https://github.com/go-gost/gost) | ⭐ 7k+ |
| **dae** | Go | dae/daeunified (kernel-based) | [daeuniverse/dae](https://github.com/daeuniverse/dae) | ⭐ 5k+ |

### Reverse Proxies & Load Balancers

| Project | Description | GitHub | Stars |
|---------|-------------|--------|-------|
| **Nginx** | High-performance HTTP/reverse proxy | [nginx/nginx](https://github.com/nginx/nginx) | ⭐ 25k+ |
| **Caddy** | Auto-HTTPS reverse proxy | [caddyserver/caddy](https://github.com/caddyserver/caddy) | ⭐ 60k+ |
| **Traefik** | Cloud-native reverse proxy | [traefik/traefik](https://github.com/traefik/traefik) | ⭐ 55k+ |
| **Envoy** | Service mesh L7 proxy | [envoyproxy/envoy](https://github.com/envoyproxy/envoy) | ⭐ 25k+ |
| **HAProxy** | TCP/HTTP load balancer | [haproxy/haproxy](https://github.com/haproxy/haproxy) | ⭐ 5k+ |
| **FRP** | Fast Reverse Proxy | [fatedier/frp](https://github.com/fatedier/frp) | ⭐ 90k+ |
| **Rathole** | High-performance reverse proxy (Rust) | [rapiz1/rathole](https://github.com/rapiz1/rathole) | ⭐ 10k+ |
| **Gost** | Security proxy tunnel | [ginuerzh/gost](https://github.com/ginuerzh/gost) | ⭐ 5k+ |
| **Pangolin** | Identity-aware VPN/proxy | [fosrl/pangolin](https://github.com/fosrl/pangolin) | ⭐ 5k+ |

### SOCKS/HTTP Forward Proxies

| Project | Description | GitHub | Stars |
|---------|-------------|--------|-------|
| **Dante** | Free SOCKS server | [dante](https://www.inet.no/dante/) | — |
| **microsocks** | Tiny portable SOCKS5 | [micro11/microsocks](https://github.com/micro11/microsocks) | ⭐ 1.5k+ |
| **3proxy** | Universal proxy | [3proxy/3proxy](https://github.com/3proxy/3proxy) | ⭐ 1k+ |
| **tinyproxy** | Lightweight HTTP/HTTPS proxy | [tinyproxy/tinyproxy](https://github.com/tinyproxy/tinyproxy) | ⭐ 5.9k+ |
| **g3proxy** | ByteDance HTTP/SOCKS/SNI proxy | [bytedance/g3proxy](https://github.com/bytedance/g3proxy) | ⭐ 3k+ |
| **snail007/goproxy** | High-performance Go proxy | [snail007/goproxy](https://github.com/snail007/goproxy) | ⭐ 5k+ |

## 🚇 Tunneling Tools

> Essential for bypassing NAT/firewalls and exposing local services.

| Tool | Description | GitHub | Stars |
|------|-------------|--------|-------|
| **FRP** | Fast Reverse Proxy (most popular) | [fatedier/frp](https://github.com/fatedier/frp) | ⭐ 90k+ |
| **ngrok** | Public URLs for localhost | [ngrok/ngrok](https://github.com/ngrok/ngrok) | ⭐ 2.5k+ |
| **Cloudflare Tunnel** | Zero-config CF tunneling | [cloudflare/flared](https://github.com/cloudflare/cloudflared) | ⭐ 10k+ |
| **Chisel** | Fast TCP/UDP tunnel over HTTP | [jpillora/chisel](https://github.com/jpillora/chisel) | ⭐ 15k+ |
| **bore** | Port forwarding to public | [ekzhang/bore](https://github.com/ekzhang/bore) | ⭐ 9k+ |
| **Tailscale** | Zero-config mesh VPN | [tailscale/tailscale](https://github.com/tailscale/tailscale) | ⭐ 25k+ |
| **ZeroTier** | Virtual network overlay | [zerotier/ZeroTierOne](https://github.com/zerotier/ZeroTierOne) | ⭐ 15k+ |
| **WireGuard** | Modern VPN protocol | [WireGuard](https://github.com/WireGuard) | ⭐ 10k+ |
| **sshuttle** | Transparent proxy over SSH | [sshuttle/sshuttle](https://github.com/sshuttle/sshuttle) | ⭐ 10k+ |
| **gost** | Multi-protocol tunnel | [ginuerzh/gost](https://github.com/ginuerzh/gost) | ⭐ 5k+ |
| **PageKite** | Reverse proxy for localhost | [pagekite](https://pagekite.net/) | — |
| **localtunnel** | Expose localhost to web | [localtunnel/localtunnel](https://github.com/localtunnel/localtunnel) | ⭐ 20k+ |

📚 **Full tunneling list:** [awesome-tunneling](https://github.com/anderspitman/awesome-tunneling) (21k+ stars)

## 🔄 Subscription Management

| Tool | Description | GitHub | Stars |
|------|-------------|--------|-------|
| **Sub-Store** | Advanced subscription manager, format conversion | [sub-store-org/Sub-Store](https://github.com/sub-store-org/Sub-Store) | ⭐ 9.9k+ |
| **subconverter** | Subscription format converter (all client formats) | [tindy2013/subconverter](https://github.com/tindy2013/subconverter) | ⭐ 15.9k+ |
| **ACL4SSR** | Rule set generation & conversion | [acl4ssr/ACL4SSR](https://github.com/acl4ssr/ACL4SSR) | ⭐ 5.8k+ |
| **singbox2proxy** | Use sing-box proxies in HTTP clients | [nichind/singbox2proxy](https://github.com/nichind/singbox2proxy) | ⭐ 1k+ |

## 📋 Routing Rules

| Rule Set | Description | GitHub | Stars |
|----------|-------------|--------|-------|
| **clash-rules** | Clash Premium rule sets (most popular) | [Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules) | ⭐ 26k+ |
| **chn-iplist** | Chinese IP routing rules for many clients | [PaPerseller/chn-iplist](https://github.com/PaPerseller/chn-iplist) | ⭐ 1.2k+ |
| **china_ip_list** | China IP list for routing | [17mon/china_ip_list](https://github.com/17mon/china_ip_list) | ⭐ 4k+ |
| **geoip/Geolite2** | MaxMind GeoIP databases | [P3TERX/GeoLite.mmdb](https://github.com/P3TERX/GeoLite.mmdb) | ⭐ 3k+ |
| **domain-list-community** | Community domain lists for Clash | [v2fly/domain-list-community](https://github.com/v2fly/domain-list-community) | ⭐ 5k+ |

## ⚡ One-Click Install Scripts

| Script | Protocols | Features | GitHub | Stars |
|--------|-----------|----------|--------|-------|
| **v2ray-agent** | Xray/Tuic/H2/sing-box 8-in-one | Most comprehensive | [mack-a/v2ray-agent](https://github.com/mack-a/v2ray-agent) | ⭐ 20k+ |
| **233boy/v2ray** | V2Ray classic | Most popular V2Ray script | [233boy/v2ray](https://github.com/233boy/v2ray) | ⭐ 28.8k+ |
| **sing-box-yg** | sing-box 5-in-one | Argo tunnels, Psiphon | [yonggekkk/sing-box-yg](https://github.com/yonggekkk/sing-box-yg) | ⭐ 8.3k+ |
| **Xray_onekey** | VLESS + XTLS | Early popular installer | [wulabing/Xray_onekey](https://github.com/wulabing/Xray_onekey) | ⭐ 9.3k+ |
| **reality-ezpz** | VLESS/TuIC/H2/ShadowTLS | Docker Compose, Telegram bot | [aleskxyz/reality-ezpz](https://github.com/aleskxyz/reality-ezpz) | ⭐ 1.5k+ |
| **ArgoX** | Argo + Xray | Cloudflare Argo integration | [fscarmen/ArgoX](https://github.com/fscarmen/ArgoX) | ⭐ 1.8k+ |

## 📋 Free Proxy Lists

### High-Frequency Auto-Updated Lists

| Project | Protocols | Update Frequency | GitHub | Stars |
|---------|-----------|-----------------|--------|-------|
| **Free-servers** | VMess/VLESS/Trojan/SS | Every 6 hours | [Pawdroid/Free-servers](https://github.com/Pawdroid/Free-servers) | ⭐ 19.6k+ |
| **v2rayfree** | V2Ray free nodes | Every 6 hours + speed test | [aiboboxx/v2rayfree](https://github.com/aiboboxx/v2rayfree) | ⭐ 14k+ |
| **aggregator** | All major | Auto-crawl + verify | [wzdnzd/aggregator](https://github.com/wzdnzd/aggregator) | ⭐ 6.7k+ |
| **ermaozi/get_subscribe** | Clash/V2Ray/Trojan/SSR | Automated | [ermaozi/get_subscribe](https://github.com/ermaozi/get_subscribe) | ⭐ 8.7k+ |
| **AutoMergePublicNodes** | All major | Auto-scrape | [chengaopan/AutoMergePublicNodes](https://github.com/chengaopan/AutoMergePublicNodes) | ⭐ 7.3k+ |
| **V2RayAggregator** | SS/SSR/Trojan/VMess | Speed-filtered | [mahdibland/V2RayAggregator](https://github.com/mahdibland/V2RayAggregator) | ⭐ 4k+ |
| **Barabama/FreeNodes** | V2Ray/Clash | Auto-updated | [Barabama/FreeNodes](https://github.com/Barabama/FreeNodes) | ⭐ 2.7k+ |
| **proxypool** | Proxies/Nodes/VPN | Go-based pool | [snakem982/proxypool](https://github.com/snakem982/proxypool) | ⭐ 1.8k+ |
| **vxiaov/free_proxy_ss** | SS/SSR/V2Ray/Clash | Every 2 hours | [vxiaov/free_proxy_ss](https://github.com/vxiaov/free_proxy_ss) | ⭐ 2.4k+ |
| **ripaojiedian/freenode** | SS/SSR/VMess/VLESS/Trojan | Permanent links | [ripaojiedian/freenode](https://github.com/ripaojiedian/freenode) | ⭐ 2.2k+ |

### Specialized Lists

| Project | Protocols | Unique Feature | GitHub |
|---------|-----------|---------------|--------|
| **OpenRay** | VMess/VLESS/Trojan/SS/H2/TUIC/Juicity | Per-country categorization | [sakha1370/OpenRay](https://github.com/sakha1370/OpenRay) |
| **free-proxy-list** | 10+ protocols including mtproto | 30-min updates | [gfpcom/free-proxy-list](https://github.com/gfpcom/free-proxy-list) |
| **ProxyCollector** | VMess/VLESS/Trojan/SS/H2/TUIC | 50+ source subscriptions, sing-box testing | [Mahdi0024/ProxyCollector](https://github.com/Mahdi0024/ProxyCollector) |
| **v2ray-configs** | VLESS/VMess/SS/Trojan | 5-min update cycle | [Epodonios/v2ray-configs](https://github.com/Epodonios/v2ray-configs) |
| **v2ray-config** | V2Ray | Each link verified via TLS tunnel to GitHub | [morpheusadam/v2ray-config](https://github.com/morpheusadam/v2ray-config) |
| **am-cf-tunnel** | VLESS/Trojan | Cloudflare Workers/Pages script | [amclubs/am-cf-tunnel](https://github.com/amclubs/am-cf-tunnel) |

## 🔧 Tools & Utilities

### Proxy Checkers & Scrapers

| Tool | Language | Features | GitHub | Stars |
|------|----------|----------|--------|-------|
| **ProxyBroker** | Python | Find, check, serve | [constverum/ProxyBroker](https://github.com/constverum/ProxyBroker) | ⭐ 3k+ |
| **proxy_pool** | Python | Collect, validate, serve via API | [jhao104/proxy_pool](https://github.com/jhao104/proxy_pool) | ⭐ 23k+ |
| **proxy-scraper-checker** | Rust | Fast scraper + checker + GeoIP | [monosans/proxy-scraper-checker](https://github.com/monosans/proxy-scraper-checker) | ⭐ 1.3k+ |
| **checked-proxy-list** | Go | CLI with TUI | [ClearProxy/checked-proxy-list](https://github.com/ClearProxy/checked-proxy-list) | ⭐ 97+ |
| **Valid8Proxy** | Python | Multi-thread validation | [spyboy-productions/Valid8Proxy](https://github.com/spyboy-productions/Valid8Proxy) | ⭐ 267+ |
| **proxycheck** | Bash | Async feed checker | [almroot/proxycheck](https://github.com/almroot/proxycheck) | ⭐ 4+ |

### Rotation & Management

| Tool | Description | GitHub | Stars |
|------|-------------|--------|-------|
| **rota** | High-performance rotation engine | [alpkeskin/rota](https://github.com/alpkeskin/rota) | ⭐ 1k+ |
| **proxybroker2** | Auto-rotate proxy finder | [bluet/proxybroker2](https://github.com/bluet/proxybroker2) | ⭐ 500+ |

### Proxy Diagnostics

| Tool | Description | GitHub | Stars |
|------|-------------|--------|-------|
| **Kilobat CLI** | Active macOS network diagnostic CLI; queries a configured Clash-compatible controller for routes and delay | [seifip/kilobat-cli](https://github.com/seifip/kilobat-cli) | ⭐ 1 |

### Transparent Proxy

| Tool | Description | GitHub | Stars |
|------|-------------|--------|-------|
| **ss-tproxy** | Transparent proxy for ss/v2ray/xray/trojan/hysteria | [zfl9/ss-tproxy](https://github.com/zfl9/ss-tproxy) | ⭐ 2.4k+ |
| **python-proxy** | Async HTTP/HTTPS/SOCKS4/5/SS/SSH proxy | [qwj/python-proxy](https://github.com/qwj/python-proxy) | ⭐ 2.2k+ |

### Development Libraries

| Library | Language | Purpose | GitHub | Stars |
|---------|----------|---------|--------|-------|
| **kcp-go** | Go | UDP reliable transport | [xtaci/kcp-go](https://github.com/xtaci/kcp-go) | ⭐ 4k+ |
| **quic-go** | Go | QUIC protocol | [quic-go/quic-go](https://github.com/quic-go/quic-go) | ⭐ 10k+ |
| **masque-go** | Go | MASQUE proxy | [quic-go/masque-go](https://github.com/quic-go/masque-go) | ⭐ 500+ |

### Configuration Examples

| Project | Description | GitHub | Stars |
|---------|-------------|--------|-------|
| **integrated-examples** | Nginx/Caddy + V2Ray/Xray/Hysteria/TUIC configs | [lxhao61/integrated-examples](https://github.com/lxhao61/integrated-examples) | ⭐ 2.5k+ |

## ☁️ Cloudflare & WARP

| Project | Description | GitHub | Stars |
|---------|-------------|--------|-------|
| **am-cf-tunnel** | CF Workers/Pages for VLESS/Trojan | [amclubs/am-cf-tunnel](https://github.com/amclubs/am-cf-tunnel) | ⭐ 3k+ |
| **ArgoX** | Argo + Xray for VPS | [fscarmen/ArgoX](https://github.com/fscarmen/ArgoX) | ⭐ 1.8k+ |
| **cloudflared** | Official CF Tunnel client | [cloudflare/cloudflared](https://github.com/cloudflare/cloudflared) | ⭐ 10k+ |
| **wgcf** | Generate WireGuard configs for WARP | [Vi3merH/wgcf](https://github.com/Vi3merH/wgcf) | ⭐ 6k+ |
| **warp-plus** | Generate unlimited WARP+ data | [YirsisFers/warp-plus](https://github.com/YirsisFers/warp-plus) | ⭐ 3k+ |
| **XUI-PRO** | Panel with WARP integration | [GFW4Fun/x-ui-pro](https://github.com/GFW4Fun/x-ui-pro) | ⭐ 1.2k+ |

## 🛡️ Anti-Censorship Resources

| Resource | Description | GitHub | Stars |
|----------|-------------|--------|-------|
| **awesome-anticensor** | Structured censorship circumvention list | [marzneshin/awesome-anticensor](https://github.com/marzneshin/awesome-anticensor) | ⭐ 38+ |
| **awesome-freedom** | Panels, scripts, bots, tutorials | [erfjab/awesome-freedom](https://github.com/erfjab/awesome-freedom) | ⭐ 153+ |
| **awesome-vpn** | Free proxy node aggregator + list | [awesome-vpn/awesome-vpn](https://github.com/awesome-vpn/awesome-vpn) | ⭐ 6.8k+ |
| **awesome-tunneling** | ngrok/CF Tunnel alternatives | [anderspitman/awesome-tunneling](https://github.com/anderspitman/awesome-tunneling) | ⭐ 21k+ |
| **awesome-wireguard** | WireGuard tools & projects | [cedrickchee/awesome-wireguard](https://github.com/cedrickchee/awesome-wireguard) | ⭐ 1.5k+ |

## 📚 Learning Resources

### Documentation
- [sing-box Official Docs](https://sing-box.sagernet.org/)
- [Xray-core Documentation](https://xtls.github.io/)
- [Clash Wiki](https://wiki.clash.wiki/)
- [Hysteria 2 Docs](https://hysteria.network/)
- [Mihomo Docs](https://wiki.metacubex.one/)

### Community
- [r/dumbclub](https://reddit.com/r/dumbclub) — Proxy discussion
- [r/V2Ray](https://reddit.com/r/V2Ray) — V2Ray community
- [Telegram: ProxyMTProto](https://t.me/ProxyMTProto)

### Articles & Guides
- [VLESS + Reality + XTLS Setup Guide](https://www.jamesflare.com/vless-tcp-reality-xtls-utls-xudp)
- [Building Private Proxy with sing-box](https://www.scrapingbee.com/blog/how-to-build-private-proxy-server)
- [9 Open Source Reverse Proxies](https://carlosmv.hashnode.dev/9-open-source-reverse-proxies-you-need-to-know)
- [yonggekkk Blog](https://github.com/yonggekkk) — Extensive deployment tutorials

## 🔮 2026 Technology Trends

1. **TCP → UDP/QUIC Migration** — HTTP/3 adoption drives QUIC-based protocols (Masque, Juicity, TUIC)
2. **Encryption → Camouflage** — Simple AES insufficient; fingerprint spoofing (uTLS) and identity theft (Reality) are key
3. **Post-Quantum Cryptography (PQC)** — SSH and WireGuard introducing quantum-resistant algorithms
4. **AI Traffic Analysis Resistance** — Protocols must defeat machine learning-based traffic classification
5. **Multi-Protocol Stacking** — Running multiple protocol types simultaneously for resilience
6. **Cloudflare Worker Proxies** — Serverless proxy deployment becoming mainstream
7. **Kernel-Level Proxies** — dae/sing-box TUN replacing userspace proxies for performance

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### How to Contribute
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingAddition`)
3. Commit your changes (`git commit -m 'Add some AmazingAddition'`)
4. Push to the branch (`git push origin feature/AmazingAddition`)
5. Open a Pull Request

### Contribution Areas
- Adding new protocols or tools
- Translating documentation
- Updating broken links
- Improving categorization
- Adding performance benchmarks

## 📜 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

## 🙏 Acknowledgments

- [jichangzhu.org](https://jichangzhu.org/protocols/) — Comprehensive protocol testing and comparison
- [drsoft-oss/awesome-proxy](https://github.com/drsoft-oss/awesome-proxy) — Collaborative proxy resource list
- [dariubs/awesome-proxy](https://github.com/dariubs/awesome-proxy) — Proxy servers and resources
- [anderspitman/awesome-tunneling](https://github.com/anderspitman/awesome-tunneling) — Tunneling tools
- [cedrickchee/awesome-wireguard](https://github.com/cedrickchee/awesome-wireguard) — WireGuard ecosystem
- [marzneshin/awesome-anticensor](https://github.com/marzneshin/awesome-anticensor) — Censorship circumvention
- [erfjab/awesome-freedom](https://github.com/erfjab/awesome-freedom) — Panels, scripts, bots
- All open-source proxy protocol developers and maintainers

---

<p align="center">
  <sub>Built with ❤️ by the community, for the community.</sub><br/>
  <sub>150+ entries across 12 categories · 4 languages</sub><br/>
  <sub>Last updated: 2026-10-29</sub>
</p>
