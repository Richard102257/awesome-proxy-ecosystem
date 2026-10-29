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
  <img src="https://img.shields.io/badge/clients-20+-green" alt="Clients"/>
  <img src="https://img.shields.io/badge/platforms-8+-orange" alt="Platforms"/>
  <img src="https://img.shields.io/github/license/awesome-proxy-ecosystem/awesome-proxy-ecosystem" alt="License"/>
</p>

---

## 📖 Overview

This project is a comprehensive, curated collection of proxy protocols, implementations, clients, and ecosystem resources. It consolidates information from various sources including [jichangzhu.org/protocols](https://jichangzhu.org/protocols/) and multiple GitHub awesome lists.

Whether you're a developer, researcher, or privacy-conscious user, this guide helps you navigate the complex landscape of proxy technologies.

## 📑 Table of Contents

- [Quick Start Guide](#-quick-start-guide)
- [Protocol Classification](#-protocol-classification)
- [Core Protocols Deep Dive](#-core-protocols-deep-dive)
- [Client Software](#-client-software)
- [Server Panels & Management](#-server-panels--management)
- [Proxy Platforms & Frameworks](#-proxy-platforms--frameworks)
- [Free Proxy Lists](#-free-proxy-lists)
- [Tools & Utilities](#-tools--utilities)
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
| **Juicity** | ✅ Active | [juicity/juicity](https://github.com/juicity/juicity) | QUIC protocol, "Justicity" — fast & lightweight |

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

| Client | Platforms | Protocols | GitHub |
|--------|-----------|-----------|--------|
| **sing-box** | Win/Mac/Linux/Android/iOS | All major | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) |
| **Clash Meta (Mihomo)** | Win/Mac/Linux | VMess/VLESS/SS/Trojan/TUIC/H2 | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) |
| **Hiddify** | Win/Mac/Linux/Android/iOS | All major | [hiddify/hiddify-app](https://github.com/hiddify/hiddify-app) |
| **Clash Verge Rev** | Win/Mac/Linux | Clash-based | [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev) |
| **NekoBox** | Android | SS/V2Ray/sing-box | [MatsuriDayo/NekoBoxForAndroid](https://github.com/MatsuriDayo/NekoBoxForAndroid) |
| **v2rayN** | Windows | VMess/VLESS/SS/Trojan | [2dust/v2rayN](https://github.com/2dust/v2rayN) |
| **v2rayNG** | Android | VMess/VLESS/SS/Trojan | [2dust/v2rayNG](https://github.com/2dust/v2rayNG) |
| **Shadowrocket** | iOS/tvOS | All major | App Store |
| **Surge** | macOS/iOS | All major | Commercial |
| **Stash** | macOS/iOS | All major | App Store |
| **V2RayA** | Linux (Web GUI) | V2Ray/Xray/sing-box | [v2rayA/v2rayA](https://github.com/v2rayA/v2rayA) |
| **Qv2ray** | Win/Mac/Linux | V2Ray (plugin) | [Qv2ray/Qv2ray](https://github.com/Qv2ray/Qv2ray) |

### Desktop GUI Comparison

| Feature | Clash Verge | v2rayN | V2RayA | Hiddify |
|---------|-------------|--------|--------|---------|
| Platform | Win/Mac/Linux | Windows | Linux | All |
| Subscription | ✅ | ✅ | ✅ | ✅ |
| TUN Mode | ✅ | ✅ | ✅ | ✅ |
| Profile Switch | ✅ | ✅ | ✅ | ✅ |
| Traffic Stats | ✅ | ✅ | ✅ | ✅ |
| Rule Engine | ✅ | ✅ | ✅ | ✅ |

## 🖥️ Server Panels & Management

| Panel | Protocols | Features | GitHub |
|-------|-----------|----------|--------|
| **3X-UI** | VLESS/VMess/Trojan/H2/TUIC | Web GUI, multi-user, traffic control | [MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui) |
| **X-UI** | VLESS/VMess/Trojan | Simple web panel | [FranzKafkaYu/x-ui](https://github.com/FranzKafkaYu/x-ui) |
| **Hiddify Manager** | All major | Multi-server management | [hiddify/hiddify-manager](https://github.com/hiddify/hiddify-manager) |
| **Marzban** | VLESS/VMess/Trojan | Multi-protocol, Telegram bot | [Gozargah/Marzban](https://github.com/Gozargah/Marzban) |
| **Libertea** | VLESS/Panel | Simple, lightweight | [Libertea/Libertea](https://github.com/Libertea/Libertea) |

## 🏗️ Proxy Platforms & Frameworks

### Universal Proxy Platforms

| Project | Language | Protocols | GitHub |
|---------|----------|-----------|--------|
| **sing-box** | Go | SS/VMess/VLESS/Trojan/TUIC/H2/Naive/WG | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) |
| **Xray-core** | Go | VLESS/VMess/Trojan/Reality/XTLS | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) |
| **v2ray-core** | Go | VMess/VLESS/SS/Trojan | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) |
| **Clash** | Go | SS/VMess/VLESS/Trojan/SOCKS5/HTTP | [Dreamacro/clash](https://github.com/Dreamacro/clash) |
| **mihomo** | Go | Clash + TUIC/H2/Reality | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) |
| **GOST** | Go | Multi-protocol chain proxy | [go-gost/gost](https://github.com/go-gost/gost) |

### Reverse Proxies & Load Balancers

| Project | Description | GitHub |
|---------|-------------|--------|
| **Nginx** | High-performance HTTP/reverse proxy | [nginx/nginx](https://github.com/nginx/nginx) |
| **Caddy** | Auto-HTTPS reverse proxy | [caddyserver/caddy](https://github.com/caddyserver/caddy) |
| **Traefik** | Cloud-native reverse proxy | [traefik/traefik](https://github.com/traefik/traefik) |
| **Envoy** | Service mesh L7 proxy | [envoyproxy/envoy](https://github.com/envoyproxy/envoy) |
| **HAProxy** | TCP/HTTP load balancer | [haproxy/haproxy](https://github.com/haproxy/haproxy) |
| **FRP** | Fast Reverse Proxy | [fatedier/frp](https://github.com/fatedier/frp) |
| **Rathole** | High-performance reverse proxy | [rapiz1/rathole](https://github.com/rapiz1/rathole) |
| **Gost** | Security proxy tunnel | [ginuerzh/gost](https://github.com/ginuerzh/gost) |
| **Pangolin** | Identity-aware VPN/proxy | [fosrl/pangolin](https://github.com/fosrl/pangolin) |

### SOCKS/HTTP Forward Proxies

| Project | Description | GitHub |
|---------|-------------|--------|
| **Dante** | Free SOCKS server | [dante](https://www.inet.no/dante/) |
| **microsocks** | Tiny portable SOCKS5 | [micro11/microsocks](https://github.com/micro11/microsocks) |
| **3proxy** | Universal proxy | [3proxy/3proxy](https://github.com/3proxy/3proxy) |
| **tinyproxy** | Lightweight HTTP/HTTPS proxy | [tinyproxy/tinyproxy](https://github.com/tinyproxy/tinyproxy) |
| **g3proxy** | ByteDance HTTP/SOCKS proxy | [bytedance/g3proxy](https://github.com/bytedance/g3proxy) |
| **snail007/goproxy** | High-performance Go proxy | [snail007/goproxy](https://github.com/snail007/goproxy) |

## 📋 Free Proxy Lists

| Project | Protocols | Update Frequency | GitHub |
|---------|-----------|-----------------|--------|
| **OpenRay** | VMess/VLESS/Trojan/SS/H2/TUIC/Juicity | Hourly | [sakha1370/OpenRay](https://github.com/sakha1370/OpenRay) |
| **free-proxy-list** | SS/SSSR/V2Ray/Trojan/H2/TUIC/WG | Every 30 min | [gfpcom/free-proxy-list](https://github.com/gfpcom/free-proxy-list) |
| **openproxylist** | HTTPS/SOCKS4/SOCKS5/V2Ray | Hourly | [roosterkid/openproxylist](https://github.com/roosterkid/openproxylist) |
| **proxylist** | HTTP/SOCKS5 | Real-time | [elliottophellia/proxylist](https://github.com/elliottophellia/proxylist) |
| **F0rc3Run** | VMess/VLESS/SS/SSTP | Automated | [F0rc3Run/F0rc3Run](https://github.com/F0rc3Run/F0rc3Run) |
| **Proxy-Master** | HTTP/SOCKS5 | Every 10 min | [MuRongPIG/Proxy-Master](https://github.com/MuRongPIG/Proxy-Master) |
| **Free-Proxy** | HTTP/SOCKS5 | Every 5 min | [proxifly/free-proxy-list](https://github.com/proxifly/free-proxy-list) |

## 🔧 Tools & Utilities

### Proxy Checkers & Scrapers

| Tool | Language | Features | GitHub |
|------|----------|----------|--------|
| **ProxyBroker** | Python | Find, check, serve | [constverum/ProxyBroker](https://github.com/constverum/ProxyBroker) |
| **proxy-scraper-checker** | Rust | Fast scraper + checker | [monosans/proxy-scraper-checker](https://github.com/monosans/proxy-scraper-checker) |
| **checked-proxy-list** | Go | CLI with TUI | [ClearProxy/checked-proxy-list](https://github.com/ClearProxy/checked-proxy-list) |
| **Valid8Proxy** | Python | Multi-thread validation | [spyboy-productions/Valid8Proxy](https://github.com/spyboy-productions/Valid8Proxy) |
| **proxycheck** | Bash | Async feed checker | [almroot/proxycheck](https://github.com/almroot/proxycheck) |

### Rotation & Management

| Tool | Description | GitHub |
|------|-------------|--------|
| **rota** | High-performance rotation engine | [alpkeskin/rota](https://github.com/alpkeskin/rota) |
| **proxybroker2** | Auto-rotate proxy finder | [bluet/proxybroker2](https://github.com/bluet/proxybroker2) |
| **singbox2proxy** | Use sing-box proxies in HTTP clients | [nichind/singbox2proxy](https://github.com/nichind/singbox2proxy) |

### Development Libraries

| Library | Language | Purpose | GitHub |
|---------|----------|---------|--------|
| **kcp-go** | Go | UDP reliable transport | [xtaci/kcp-go](https://github.com/xtaci/kcp-go) |
| **quic-go** | Go | QUIC protocol | [quic-go/quic-go](https://github.com/quic-go/quic-go) |
| **masque-go** | Go | MASQUE proxy | [quic-go/masque-go](https://github.com/quic-go/masque-go) |

## 📚 Learning Resources

### Documentation
- [sing-box Official Docs](https://sing-box.sagernet.org/)
- [Xray-core Documentation](https://xtls.github.io/)
- [Clash Wiki](https://wiki.clash.wiki/)
- [Hysteria 2 Docs](https://hysteria.network/)

### Community
- [r/dumbclub](https://reddit.com/r/dumbclub) — Proxy discussion
- [r/V2Ray](https://reddit.com/r/V2Ray) — V2Ray community
- [Telegram: ProxyMTProto](https://t.me/ProxyMTProto)

### Articles & Guides
- [VLESS + Reality + XTLS Setup Guide](https://www.jamesflare.com/vless-tcp-reality-xtls-utls-xudp)
- [Building Private Proxy with sing-box](https://www.scrapingbee.com/blog/how-to-build-private-proxy-server)
- [9 Open Source Reverse Proxies](https://carlosmv.hashnode.dev/9-open-source-reverse-proxies-you-need-to-know)

## 🔮 2026 Technology Trends

1. **TCP → UDP/QUIC Migration** — HTTP/3 adoption drives QUIC-based protocols (Masque, Juicity, TUIC)
2. **Encryption → Camouflage** — Simple AES insufficient; fingerprint spoofing (uTLS) and identity theft (Reality) are key
3. **Post-Quantum Cryptography (PQC)** — SSH and WireGuard introducing quantum-resistant algorithms
4. **AI Traffic Analysis Resistance** — Protocols must defeat machine learning-based traffic classification
5. **Multi-Protocol Stacking** — Running multiple protocol types simultaneously for resilience

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
- All open-source proxy protocol developers and maintainers

---

<p align="center">
  <sub>Built with ❤️ by the community, for the community.</sub><br/>
  <sub>Last updated: 2026-10-29</sub>
</p>
