# 🌐 Awesome Proxy Ecosystem

<p align="center">
  <b>프록시 프로토콜, 도구 및 리소스의 궁극큐레이션</b><br/>
  <i>The Ultimate Curated List of Proxy Protocols, Tools, and Resources</i>
</p>

<p align="center">
  <a href="../../README.md">English</a> ｜
  <a href="../zh-CN/README.md">简体中文</a> ｜
  <a href="../ja/README.md">日本語</a> ｜
  <a href="README.md">한국어</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/프로토콜-35+-blue" alt="Protocols"/>
  <img src="https://img.shields.io/badge/클라이언트-20+-green" alt="Clients"/>
  <img src="https://img.shields.io/badge/플랫폼-8+-orange" alt="Platforms"/>
  <img src="https://img.shields.io/badge/license-MIT-success" alt="License"/>
</p>

---

## 📖 개요

이 프로젝트는 프록시 프로토콜, 구현, 클라이언트 및 에코시스템 리소스를 포괄적으로 큐레이션한 리스트입니다. [jichangzhu.org/protocols](https://jichangzhu.org/protocols/) 및 여러 GitHub awesome 리스트에서 정보를 통합했습니다.

개발자, 연구자, 프라이버시 중심 사용자 관계없이, 이 가이드는 복잡한 프록시 기술 세계를 탐색하는 데 도움을 줍니다.

> 📌 데이터는 **35+ 프로토콜**의 상세한 테스트 및 평가를 기반으로 합니다.

## 📑 목차

- [빠른 시작](#-빠른-시작)
- [프로토콜 분류](#-프로토콜-분류)
- [핵심 프로토콜 상세](#-핵심-프로토콜-상세)
- [클라이언트 소프트웨어](#-클라이언트-소프트웨어)
- [서버 패널 및 관리](#-서버-패널-및-관리)
- [프록시 플랫폼 및 프레임워크](#-프록시-플랫폼-및-프레임워크)
- [무료 프록시 목록](#-무료-프록시-목록)
- [도구 및 유틸리티](#-도구-및-유틸리티)
- [학습 리소스](#-학습-리소스)
- [2026 기술 동향](#-2026-기술-동향)

---

## 🚀 빠른 시작

### 프로토콜 선택 가이드

| 당신의 필요 | 추천 프로토콜 | 이유 |
|-----------|-------------|------|
| 최고 스텔스 | **VLESS-Reality**, **NaiveProxy** | 핑거프린트 도용, 무특징 |
| 최고 속도 | **Hysteria 2**, **TUIC v5** | UDP 브루트포스, 0-RTT |
| 게이밍 저지연 | **Shadowsocks-2022**, **ShadowQUIC** | 얇은 암호화, 효율적 UDP |
| 라우터/임베디드 | **SS-2022**, **Brook** | 최소 리소스 사용 |
| Apple 에코시스템 | **Mieru**, **Trojan**, **Sudoku** | 저유지보수, 프라이빗 프로토콜 |
| 범용 | **VMess**, **VLESS-XTLS** | 성숙한 에코시스템 |

### 의사결정 트리

```
도메인이 있습니까?
├── 있음 → 최고 성능이 필요합니까?
│   ├── 예 → VLESS-XTLS-Vision
│   └── 아니오 → VLESS-Reality
└── 없음 → 최고 스텔스가 필요합니까?
    ├── 예 → AnyTLS-Reality 또는 VLESS-Reality
    └── 아니오 → Hysteria 2 (네트워크가 나쁜 경우) 또는 SS-2022 (하드웨어가 제한된 경우)
```

---

## 📊 프로토콜 분류

### 종합력 평가

| 카테고리 | 대표 프로토콜 | 추천도 | 핵심 강점 | 적용 상황 |
|---------|-------------|--------|----------|----------|
| **스텔스 최고위** | VLESS-Reality, Naive, AnyTLS | ⭐⭐⭐⭐⭐ | 핑거프린트 위장, 완벽은폐 | 극도로 엄격한 환경, 장기 안정 |
| **고속 가속파** | Hysteria 2, TUIC v5, Juicity | ⭐⭐⭐⭐⭐ | UDP 브루트포스, 0-RTT, 8K 즉시 | 약한 네트워크, 동영상, 게임 |
| **경량 성능파** | SS-2022, Brook, Vlite | ⭐⭐⭐⭐ | 최소 리소스, 빠른 핸드셰이크 | 라우터, 임베디드, 구형 기기 |
| **극소 스텔스파** | Mieru, Trojan, Sudoku | ⭐⭐⭐⭐ | 능동 탐지 저항, 프라이빗 최적화 | Apple 에코, 저유지보수 |
| **정통 만능형** | VMess, VLESS-XTLS, SSR | ⭐⭐⭐ | 성숙 에코, 풍부 기능, 높은 호환성 | 일상 사용, 멀티 업무 |
| **기반 보안** | WireGuard, Tor, SSH, kcptun | ⭐⭐⭐ | 산업급 보안, 익명 라우팅 | 원격 근무, 극도 익명, 약한 망 최적화 |

### 🏆 Tier 1 — 스텔스 최고위

| 프로토콜 | 상태 | GitHub | 특징 |
|---------|------|--------|------|
| **VLESS-Reality** | ✅ 활성 | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | 실제 웹사이트 핑거프린트 도용 |
| **NaiveProxy** | ✅ 활성 | [klzgrad/naiveproxy](https://github.com/klzgrad/naiveproxy) | Chrome 네트워크 스택 사용 |
| **AnyTLS** | ✅ 활성 | [anytls/anytls-go](https://github.com/anytls/anytls-go) | 최소 TLS 프록시, 탐지 극히 어려움 |

### 🚀 Tier 2 — 고속 가속파

| 프로토콜 | 상태 | GitHub | 특징 |
|---------|------|--------|------|
| **Hysteria 2** | ✅ 활성 | [apernet/hysteria](https://github.com/apernet/hysteria) | Brutal 혼잡 제어, 20% 손실에도 만속 |
| **TUIC v5** | ✅ 활성 | [tuic-protocol/tuic](https://github.com/tuic-protocol/tuic) | QUIC 기반, 다중화, 모바일 절전 |
| **Juicity** | ✅ 활성 | [juicity/juicity](https://github.com/juicity/juicity) | QUIC 프로토콜의 정점 |

### ⚡ Tier 3 — 경량 성능파

| 프로토콜 | 상태 | GitHub | 특징 |
|---------|------|--------|------|
| **Shadowsocks-2022** | ✅ 활성 | [shadowsocks/shadowsocks-rust](https://github.com/shadowsocks/shadowsocks-rust) | 저지연 벤치마크, AEAD 2022 암호화 |
| **Brook** | ✅ 활성 | [txthinking/brook](https://github.com/txthinking/brook) | 단순, 빠름, 크로스 플랫폼 |
| **Vlite** | ✅ 활성 | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | 경량 V2Ray 변종 |

### 👻 Tier 4 — 극소 스텔스파

| 프로토콜 | 상태 | GitHub | 특징 |
|---------|------|--------|------|
| **Mieru** | ✅ 활성 | [enclica/mieru](https://github.com/enclica/mieru) | 분류 어려움, 탐지 어려움 |
| **Trojan** | ✅ 활성 | [trojan-gfw/trojan](https://github.com/trojan-gfw/trojan) | HTTPS 트래픽 위장 |
| **Sudoku** | ✅ 활성 | [SUDOKU-ASCII/sudoku](https://github.com/SUDOKU-ASCII/sudoku) | 수도쿠 기반 저엔트로피 핑거프린트 |

### 🔄 Tier 5 — 정통 만능형

| 프로토콜 | 상태 | GitHub | 특징 |
|---------|------|--------|------|
| **VMess** | ⚠️ 아카이브 | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) | 성숙 에코, 광범위 지원 |
| **VLESS-XTLS** | ✅ 활성 | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) | XTLS Vision/Reality 흐름 제어 |
| **SSR** | ❌ 폐기 | [shadowsocksrr](https://github.com/shadowsocksrr) | 역사적 의의 |

### 🔐 Tier 6 — 기반 보안

| 프로토콜 | 상태 | GitHub | 특징 |
|---------|------|--------|------|
| **WireGuard** | ✅ 활성 | [WireGuard](https://github.com/WireGuard) | 산업급 VPN, PQC 준비 |
| **Tor** | ✅ 활성 | [torproject/tor](https://github.com/torproject/tor) | 익명 라우팅, 온니온 서비스 |
| **SSH** | ✅ 활성 | [openssh](https://github.com/openssh/openssh-portable) | SOCKS5 터널링, PQC 지원 |
| **kcptun** | ✅ 활성 | [xtaci/kcp-go](https://github.com/xtaci/kcp-go) | UDP 신뢰성 전송 가속 |

### 🌐 Tier 7 — 트랜스포트 및 레거시

| 프로토콜 | 상태 | GitHub | 특징 |
|---------|------|--------|------|
| **Shadow-TLS** | ✅ 활성 | [ihciah/shadow-tls](https://github.com/ihciah/shadow-tls) | TLS 래핑하여 일반 HTTPS 위장 |
| **Snell** | ✅ 활성 | [Surge](https://kb.nssurge.com) | Surge 개발자 제작, Apple 에코 |
| **Masque** | ✅ 활성 | [quic-go/masque-go](https://github.com/quic-go/masque-go) | QUIC/HTTP-3 터널링 |
| **MTProto** | ✅ 활성 | [Telegram](https://core.telegram.org/mtproto) | Telegram 프록시 프로토콜 |
| **ShadowQUIC** | ✅ 활성 | [spongebob888/shadowquic](https://github.com/spongebob888/shadowquic) | SS 스텔스 + QUIC 다중화 |
| **GOST** | ✅ 활성 | [go-gost/gost](https://github.com/go-gost/gost) | 멀티프로토콜 보안 프록시 |
| **TrustTunnel** | ✅ 활성 | [TrustTunnel/TrustTunnel](https://github.com/TrustTunnel/TrustTunnel) | AdGuard 난독화 VPN |

---

## 🔬 핵심 프로토콜 상세

### VLESS + Reality — 2026년 검열 우회의 골드 스탠다드

```
[클라이언트] → VLESS → Reality (TLS 도용하여 target.com 위장) → [서버]
```

**핵심 강점:**
- 🚫 **도메인 불필요** — 실제 웹사이트 인증서 차용
- 🔒 **제로 TLS 특징** — uTLS로 실제 브라우저 모방
- 🔑 **전방 비밀성** — 각 세션에 고유 키

**구현:** [XTLS/Xray-core](https://github.com/XTLS/Xray-core) · [SagerNet/sing-box](https://github.com/SagerNet/sing-box)

### Hysteria 2 — 나쁜 네트워크를 위한 브루트포스 가속

```
[클라이언트] → Hysteria 2 (Brutal CC) → UDP 플러드 → [서버]
```

**핵심 강점:**
- 💪 **Brutal 알고리즘** — 손실과 관계없이 선언 속도로 전송
- 📉 **20% 손실에서도 작동** — 열악한 국제 회선 설계
- ⚡ **QUIC 기반** — 모던 트랜스포트 프로토콜

**구현:** [apernet/hysteria](https://github.com/apernet/hysteria)

### Shadowsocks-2022 — 저지연 벤치마크

```
[클라이언트] → SS-2022 (AEAD 2022) → 세션 암호화 → [서버]
```

**핵심 강점:**
- 🔑 **세션 키** — HKDF에서 각 세션의 고유 키 파생
- 📡 **UDP over TCP** — 효율적 UDP 처리
- 📦 **최소 오버헤드** — 얇은 암호화 레이어

**구현:** [shadowsocks/shadowsocks-rust](https://github.com/shadowsocks/shadowsocks-rust)

### NaiveProxy — 궁극의 위장

```
[클라이언트] → NaiveProxy (Chrome 넷 스택) → Chrome과 완전 동일 → [서버]
```

**핵심 강점:**
- 🌐 **Chrome 네트워크 스택 사용** — Chrome과 동일한 TLS 핑거프린트
- 🔀 **HTTP/2 다중화** — 효율적 병렬 스트림
- 🛡️ **Chrome 차단 없이는 차단 불가**

**구현:** [klzgrad/naiveproxy](https://github.com/klzgrad/naiveproxy)

---

## 💻 클라이언트 소프트웨어

### 크로스 플랫폼 클라이언트

| 클라이언트 | 플랫폼 | 지원 프로토콜 | GitHub |
|-----------|--------|-------------|--------|
| **sing-box** | Win/Mac/Linux/Android/iOS | 전체 주요 | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) |
| **Clash Meta (Mihomo)** | Win/Mac/Linux | VMess/VLESS/SS/Trojan/TUIC/H2 | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) |
| **Hiddify** | 전체 플랫폼 | 전체 주요 | [hiddify/hiddify-app](https://github.com/hiddify/hiddify-app) |
| **Clash Verge Rev** | Win/Mac/Linux | Clash 기반 | [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev) |
| **NekoBox** | Android | SS/V2Ray/sing-box | [MatsuriDayo/NekoBoxForAndroid](https://github.com/MatsuriDayo/NekoBoxForAndroid) |
| **v2rayN** | Windows | VMess/VLESS/SS/Trojan | [2dust/v2rayN](https://github.com/2dust/v2rayN) |
| **v2rayNG** | Android | VMess/VLESS/SS/Trojan | [2dust/v2rayNG](https://github.com/2dust/v2rayNG) |
| **Shadowrocket** | iOS/tvOS | 전체 주요 | App Store |
| **Surge** | macOS/iOS | 전체 주요 | 상용 |
| **Stash** | macOS/iOS | 전체 주요 | App Store |
| **V2RayA** | Linux (Web GUI) | V2Ray/Xray/sing-box | [v2rayA/v2rayA](https://github.com/v2rayA/v2rayA) |

---

## 🖥️ 서버 패널 및 관리

| 패널 | 지원 프로토콜 | 기능 | GitHub |
|------|-------------|------|--------|
| **3X-UI** | VLESS/VMess/Trojan/H2/TUIC | Web GUI, 다중 사용자, 트래픽 제어 | [MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui) |
| **X-UI** | VLESS/VMess/Trojan | 간단한 Web 패널 | [FranzKafkaYu/x-ui](https://github.com/FranzKafkaYu/x-ui) |
| **Hiddify Manager** | 전체 주요 | 다중 서버 관리 | [hiddify/hiddify-manager](https://github.com/hiddify/hiddify-manager) |
| **Marzban** | VLESS/VMess/Trojan | 멀티프로토콜, Telegram Bot | [Gozargah/Marzban](https://github.com/Gozargah/Marzban) |

---

## 🏗️ 프록시 플랫폼 및 프레임워크

### 범용 프록시 플랫폼

| 프로젝트 | 언어 | 지원 프로토콜 | GitHub |
|---------|------|-------------|--------|
| **sing-box** | Go | SS/VMess/VLESS/Trojan/TUIC/H2/Naive/WG | [SagerNet/sing-box](https://github.com/SagerNet/sing-box) |
| **Xray-core** | Go | VLESS/VMess/Trojan/Reality/XTLS | [XTLS/Xray-core](https://github.com/XTLS/Xray-core) |
| **v2ray-core** | Go | VMess/VLESS/SS/Trojan | [v2fly/v2ray-core](https://github.com/v2fly/v2ray-core) |
| **Clash** | Go | SS/VMess/VLESS/Trojan/SOCKS5/HTTP | [Dreamacro/clash](https://github.com/Dreamacro/clash) |
| **mihomo** | Go | Clash + TUIC/H2/Reality | [MetaCubeX/mihomo](https://github.com/MetaCubeX/mihomo) |
| **GOST** | Go | 멀티프로토콜 체인 | [go-gost/gost](https://github.com/go-gost/gost) |

### 리버스 프록시 및 로드 밸런서

| 프로젝트 | 설명 | GitHub |
|---------|------|--------|
| **Nginx** | 고성능 HTTP/리버스 프록시 | [nginx/nginx](https://github.com/nginx/nginx) |
| **Caddy** | 자동 HTTPS 리버스 프록시 | [caddyserver/caddy](https://github.com/caddyserver/caddy) |
| **Traefik** | 클라우드 네이티브 리버스 프록시 | [traefik/traefik](https://github.com/traefik/traefik) |
| **Envoy** | 서비스 메시 L7 프록시 | [envoyproxy/envoy](https://github.com/envoyproxy/envoy) |
| **HAProxy** | TCP/HTTP 로드 밸런서 | [haproxy/haproxy](https://github.com/haproxy/haproxy) |
| **FRP** | 고속 리버스 프록시 | [fatedier/frp](https://github.com/fatedier/frp) |

---

## 📋 무료 프록시 목록

| 프로젝트 | 프로토콜 | 업데이트 주기 | GitHub |
|---------|---------|-------------|--------|
| **OpenRay** | VMess/VLESS/Trojan/SS/H2/TUIC/Juicity | 매시간 | [sakha1370/OpenRay](https://github.com/sakha1370/OpenRay) |
| **free-proxy-list** | SS/SSSR/V2Ray/Trojan/H2/TUIC/WG | 30분마다 | [gfpcom/free-proxy-list](https://github.com/gfpcom/free-proxy-list) |
| **openproxylist** | HTTPS/SOCKS4/SOCKS5/V2Ray | 매시간 | [roosterkid/openproxylist](https://github.com/roosterkid/openproxylist) |

---

## 🔧 도구 및 유틸리티

### 프록시 체크 및 스크래퍼

| 도구 | 언어 | 기능 | GitHub |
|------|------|------|--------|
| **ProxyBroker** | Python | 발견, 체크, 서버화 | [constverum/ProxyBroker](https://github.com/constverum/ProxyBroker) |
| **proxy-scraper-checker** | Rust | 고속 스크래핑+체크 | [monosans/proxy-scraper-checker](https://github.com/monosans/proxy-scraper-checker) |
| **checked-proxy-list** | Go | TUI 포함 CLI | [ClearProxy/checked-proxy-list](https://github.com/ClearProxy/checked-proxy-list) |

### 로테이션 및 관리

| 도구 | 설명 | GitHub |
|------|------|--------|
| **rota** | 고성능 로테이션 엔진 | [alpkeskin/rota](https://github.com/alpkeskin/rota) |
| **singbox2proxy** | HTTP 클라이언트에서 sing-box 프록시 사용 | [nichind/singbox2proxy](https://github.com/nichind/singbox2proxy) |

---

## 📚 학습 리소스

### 공식 문서
- [sing-box 공식 문서](https://sing-box.sagernet.org/)
- [Xray-core 문서](https://xtls.github.io/)
- [Clash Wiki](https://wiki.clash.wiki/)
- [Hysteria 2 문서](https://hysteria.network/)

---

## 🔮 2026 기술 동향

1. **TCP → UDP/QUIC 전환** — HTTP/3 보급으로 QUIC 기반 프로토콜이 주류로
2. **암호화에서 위장으로** — 단순 AES 불충분, 핑거프린트 위장과 Reality가 핵심
3. **포스트 양자 암호 (PQC)** — SSH와 WireGuard가 양자 내성 알고리즘 도입
4. **AI 트래픽 분석 저항** — 프로토콜은 기계학습 기반 트래픽 분류를 극복해야
5. **멀티프로토콜 중첩** — 여러 프로토콜 동시 운용으로 내강화

> 💡 권장: 클라이언트에 최소 2가지 유형의 프로토콜(예: Reality + Hysteria 2)을 비축하세요.

---

## 🤝 기여

기여 환영! [CONTRIBUTING.md](../../CONTRIBUTING.md)을 읽어주세요.

## 📜 라이선스

MIT 라이선스 — 자세한 내용은 [LICENSE](../../LICENSE)를 참조하세요.

---

<p align="center">
  <sub>커뮤니티에 의해, 커뮤니티를 위해.</sub><br/>
  <sub>최종 업데이트: 2026-10-29</sub>
</p>
