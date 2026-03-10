# Veritas Acta

**Primitives for trust, verification, and privacy.**

Veritas Acta builds open-source cryptographic infrastructure for anonymous credential verification, contestable public records, and privacy-preserving accountability.

### Projects

| Project | Description | License |
|---------|-------------|---------|
| **[Acta](https://github.com/VeritasActa/Acta)** | A contestable, checkable, versioned public record for humans and AI | MIT |
| **[@veritasacta/verify](https://github.com/VeritasActa/verify)** | Anonymous credential verification using VOPRF ([RFC 9497](https://datatracker.ietf.org/doc/rfc9497/)) | MIT |

### How it fits together

```
Veritas Acta (open source, MIT)
├── Acta ─── contestable public record
└── verify ─ VOPRF verification primitive (npm: @veritasacta/verify)
```

The **BRASS protocol** (Blind Rate-limiting with Anonymous Scope Separation) enables systems to count anonymous requests without learning who makes them. Tokens are issued blind, verified offline, and produce deterministic nullifiers bound to scope — not identity.

Acta provides a tamper-evident, append-only record where entries can be contested, superseded, and resolved — with anonymous but sybil-resistant authorship via BRASS tokens.

### Design principles

- **No surveillance required** — verify behaviour without tracking identity
- **Offline verification** — the issuer is never contacted at redemption
- **Deterministic privacy** — same token + same scope = same nullifier; different scope = unlinkable
- **Pluggable storage** — bring your own backend (KV, Redis, Durable Objects, in-memory)
- **Audited dependencies** — built on [@noble/curves](https://github.com/paulmillr/noble-curves) and [@noble/hashes](https://github.com/paulmillr/noble-hashes)

### Get started

```bash
npm install @veritasacta/verify
```

```js
import { verify } from '@veritasacta/verify';

const result = await verify(token, context, config, store);
// { ok: true, nullifier: 'base64url...', remaining: 4 }
```

### Links

- [Protocol specification](https://github.com/VeritasActa/verify/blob/main/PROTOCOL.md)
- [Acta Charter](https://github.com/VeritasActa/Acta/blob/main/CHARTER.md)
- [npm package](https://www.npmjs.com/package/@veritasacta/verify)
