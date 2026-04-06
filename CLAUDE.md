# librtbit-sha1-wrapper

Pluggable SHA1/SHA256 abstraction for the rtbit BitTorrent client.

**Version:** 0.1.0 | **Edition:** Rust 2024 | **License:** MIT

## This Is a Shared Library

### Consumed By

| App | Via | Tag |
|-----|-----|-----|
| rustTorrent | git | v0.1.0 |
| Arz | git | v0.1.0 |
| NGMS | git | v0.1.0 |
| librtbit-core (lib) | git | v0.1.0 |
| librtbit-dht (lib) | git | v0.1.0 |
| librtbit-lsd (lib) | git | v0.1.0 |

### Depends On

- **crypto-hash** (crates.io, v0.3) — default SHA1/SHA256 via system OpenSSL
- **aws-lc-rs** (crates.io, v1.12) — alternative SHA1/SHA256 via AWS-LC

## Features

- `sha1-crypto-hash` (default) — uses crypto-hash (OpenSSL-backed, 2-3x faster)
- `sha1-ring` — uses aws-lc-rs

## BEP Implementations

- BEP 52 — SHA-256 support for BitTorrent v2 via `ISha256` trait

## Public API

- `ISha1` trait — pluggable SHA1 interface
- `ISha256` trait — pluggable SHA256 interface (BEP 52)
- `Sha1` type alias — resolves to active implementation
- `Sha256` type alias — resolves to active implementation
