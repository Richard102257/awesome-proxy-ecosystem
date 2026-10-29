# Protocol Decision Tree

```
                    ┌─────────────────────┐
                    │  What's your need?   │
                    └──────────┬──────────┘
                               │
            ┌──────────────────┼──────────────────┐
            │                  │                  │
            ▼                  ▼                  ▼
    ┌───────────────┐  ┌───────────────┐  ┌───────────────┐
    │   STEALTH     │  │    SPEED      │  │   GAMING      │
    │  (Never drop) │  │  (8K video)   │  │ (Low latency) │
    └───────┬───────┘  └───────┬───────┘  └───────┬───────┘
            │                  │                  │
            ▼                  ▼                  ▼
    ┌───────────────┐  ┌───────────────┐  ┌───────────────┐
    │ Have domain?  │  │ Network OK?   │  │ Budget HW?    │
    └───────┬───────┘  └───────┬───────┘  └───────┬───────┘
       YES │  NO           OK │  BAD          YES │  NO
            │                  │                  │
            ▼                  ▼                  ▼
 ┌──────────────────┐ ┌────────────────┐ ┌────────────────┐
 │  VLESS-Reality   │ │   TUIC v5      │ │ SS-2022        │
 │  or NaiveProxy   │ │   Juicity      │ │ ShadowQUIC     │
 └──────────────────┘ └────────────────┘ └────────────────┘
            │                  │
            ▼                  ▼
 ┌──────────────────┐ ┌────────────────┐
 │  AnyTLS-Reality  │ │  Hysteria 2    │
 │  VLESS-Reality   │ │  (Brutal CC)   │
 └──────────────────┘ └────────────────┘
```

## Quick Reference Cards

### 🥷 Stealth Card
```
┌─────────────────────────────────────────┐
│           STEALTH PROTOCOLS              │
├─────────────────────────────────────────┤
│  🥇 VLESS-Reality                       │
│     → No domain needed                  │
│     → Steals real website fingerprints  │
│     → Best overall stealth              │
│                                         │
│  🥈 NaiveProxy                          │
│     → Uses Chrome's network stack       │
│     → Blends with billions of users     │
│     → Higher resource usage             │
│                                         │
│  🥉 AnyTLS                              │
│     → Minimal TLS proxy                 │
│     → Simple to deploy                  │
│     → Very hard to detect               │
└─────────────────────────────────────────┘
```

### 🚀 Speed Card
```
┌─────────────────────────────────────────┐
│            SPEED PROTOCOLS               │
├─────────────────────────────────────────┤
│  🥇 Hysteria 2                          │
│     → Brutal congestion control         │
│     → Works at 20%+ packet loss         │
│     → Best for terrible networks        │
│                                         │
│  🥈 TUIC v5                             │
│     → QUIC-based, 0-RTT                 │
│     → Mobile-friendly, battery-saving   │
│     → Great multiplexing                │
│                                         │
│  🥉 Juicity                             │
│     → QUIC protocol peak                │
│     → Lightweight and fast              │
│     → Modern architecture               │
└─────────────────────────────────────────┘
```

### 🎮 Gaming Card
```
┌─────────────────────────────────────────┐
│           GAMING PROTOCOLS               │
├─────────────────────────────────────────┤
│  🥇 Shadowsocks-2022                    │
│     → Lowest latency                    │
│     → Thin encryption layer             │
│     → Efficient UDP handling            │
│                                         │
│  🥈 ShadowQUIC                          │
│     → SS stealth + QUIC multiplexing    │
│     → Reduces ping spikes               │
│     → Modern QUIC transport             │
│                                         │
│  🥉 Hysteria 2                          │
│     → Good for high-loss networks       │
│     → UDP-based, low jitter             │
│     → Brutal CC prevents lag            │
└─────────────────────────────────────────┘
```

### 📱 Platform-Specific Recommendations

```
┌──────────────┬──────────────────────────────────┐
│  Platform    │  Recommended                     │
├──────────────┼──────────────────────────────────┤
│  iOS         │  Shadowrocket + VLESS-Reality     │
│  Android     │  NekoBox + Hysteria 2             │
│  Windows     │  v2rayN + Mihomo                  │
│  macOS       │  Stash / Surge + VLESS-Reality    │
│  Linux       │  V2RayA + sing-box                │
│  Router      │  SS-2022 / Brook                 │
│  Apple TV    │  Shadowrocket + Snell             │
└──────────────┴──────────────────────────────────┘
```
