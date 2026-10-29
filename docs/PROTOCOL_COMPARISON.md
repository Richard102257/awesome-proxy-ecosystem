# Protocol Comparison Matrix

> Detailed technical comparison of all major proxy protocols.

## Feature Matrix

| Protocol | Transport | Encryption | Multiplex | UDP Support | Domain Required | Active Probe Resistant | DPI Resistant | Post-Quantum |
|----------|-----------|------------|-----------|-------------|-----------------|----------------------|---------------|--------------|
| VLESS-Reality | TCP/QUIC | TLS 1.3 | ✅ | ✅ | ❌ | ✅ | ✅ | ❌ |
| NaiveProxy | HTTP/2 | TLS 1.3 | ✅ | ❌ | ✅ | ✅ | ✅ | ❌ |
| AnyTLS | TCP | TLS 1.3 | ❌ | ❌ | ❌ | ✅ | ✅ | ❌ |
| Hysteria 2 | UDP/QUIC | TLS 1.3 | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| TUIC v5 | UDP/QUIC | TLS 1.3 | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| Juicity | UDP/QUIC | TLS 1.3 | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| SS-2022 | TCP | AEAD 2022 | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Brook | TCP | AES-256-GCM | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Trojan | TCP | TLS | ❌ | ✅ | ✅ | ⚠️ | ⚠️ | ❌ |
| VMess | TCP | AES/ChaCha | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| WireGuard | UDP | ChaCha20 | ❌ | ✅ | ❌ | ❌ | ❌ | ⚠️ |
| Tor | TCP | Multi-layer | ✅ | ❌ | ❌ | ✅ | ✅ | ❌ |

## Performance Benchmarks

> Note: These are approximate values. Actual performance depends on network conditions.

| Protocol | Handshake Latency | Throughput | CPU Usage | Memory Usage |
|----------|------------------|------------|-----------|-------------|
| VLESS-Reality | ~1 RTT | ★★★★★ | Medium | Medium |
| Hysteria 2 | ~1 RTT | ★★★★★ | Medium | Low |
| SS-2022 | ~0.5 RTT | ★★★★☆ | Very Low | Very Low |
| TUIC v5 | ~0.5 RTT (0-RTT) | ★★★★★ | Low | Low |
| NaiveProxy | ~1.5 RTT | ★★★☆☆ | High (browser stack) | High |
| WireGuard | ~1 RTT | ★★★★★ | Very Low | Very Low |
| Trojan | ~1 RTT | ★★★★☆ | Low | Low |
| VMess | ~1 RTT | ★★★☆☆ | Low | Low |

## Network Compatibility

| Protocol | Works on Restricted Networks | Works Behind NAT | IPv6 Support | Mobile Friendly |
|----------|----------------------------|-----------------|-------------|----------------|
| VLESS-Reality | ✅ | ✅ | ✅ | ✅ |
| NaiveProxy | ✅ | ✅ | ✅ | ⚠️ |
| Hysteria 2 | ⚠️ (UDP may be blocked) | ✅ | ✅ | ✅ |
| TUIC v5 | ⚠️ (UDP may be blocked) | ✅ | ✅ | ✅ |
| SS-2022 | ⚠️ | ✅ | ✅ | ✅ |
| Brook | ⚠️ | ✅ | ✅ | ✅ |
| WireGuard | ⚠️ (UDP may be blocked) | ✅ | ✅ | ✅ |

## Recommended Combinations

### For Maximum Resilience
- **Primary:** VLESS-Reality (stealth)
- **Fallback:** Hysteria 2 (speed on poor networks)

### For Performance
- **Primary:** VLESS-XTLS-Vision (with domain)
- **Fallback:** TUIC v5 (mobile)

### For Low Latency
- **Primary:** Shadowsocks-2022
- **Fallback:** ShadowQUIC

### For Apple Ecosystem
- **Primary:** Snell or Mieru
- **Fallback:** Trojan

### For Embedded/Router
- **Primary:** Shadowsocks-2022
- **Fallback:** Brook
