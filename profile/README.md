# Veritas Acta

**Open protocol for contestable public records.**

Cryptographic infrastructure for trust, verification, and privacy-preserving accountability. Issuer-blind verification, signed artifacts, tamper-evident records. No surveillance required.

### Core

| Project | Description | License |
|---------|-------------|---------|
| **[@veritasacta/verify](https://github.com/VeritasActa/verify)** | Issuer-blind credential verification using VOPRF ([RFC 9497](https://datatracker.ietf.org/doc/rfc9497/)). Offline, deterministic. | Apache-2.0 |
| **[@veritasacta/artifacts](https://www.npmjs.com/package/@veritasacta/artifacts)** | Signed artifact envelope — canonical JSON + Ed25519 signatures | Apache-2.0 |
| **[@veritasacta/protocol](https://www.npmjs.com/package/@veritasacta/protocol)** | Protocol primitives for the Acta signed receipt format | Apache-2.0 |
| **[Acta](https://github.com/VeritasActa/Acta)** | A contestable, checkable, versioned public record for humans and AI | Apache-2.0 |

### Tools

| Project | Description | License |
|---------|-------------|---------|
| **[acta-mcp](https://github.com/VeritasActa/acta-mcp)** | MCP server for contestable public records from AI coding tools | MIT |
| **[acta-truth-check](https://github.com/VeritasActa/acta-truth-check)** | Independent external verification of Acta instance claims | MIT |
| **attestation** | Proof-of-unique-device via BRASS tokens | MIT |

### Architecture

```
Veritas Acta (open source)
│
│ Protocol layer (Apache-2.0 — patent grant included)
├── verify ─────── VOPRF issuer-blind verification (npm: @veritasacta/verify)
├── artifacts ──── signed envelope format (npm: @veritasacta/artifacts)
├── protocol ───── receipt primitives (npm: @veritasacta/protocol)
│
│ Record layer
├── Acta ────────── contestable public record (acta.today)
│
│ Tools (MIT)
├── acta-mcp ────── MCP server for AI tools
└── acta-truth-check ─ independent claim verification
```

### Key properties

- **Issuer-blind** — the verifier never learns who issued the credential ([patent pending](https://scopeblind.com))
- **Offline verification** — the issuer is never contacted at redemption
- **Deterministic privacy** — same token + same scope = same nullifier; different scope = unlinkable
- **No surveillance required** — verify behaviour without tracking identity
- **IETF standards track** — [draft-farley-acta-signed-receipts-00](https://datatracker.ietf.org/doc/draft-farley-acta-signed-receipts/)

### Part of the ScopeBlind stack

Veritas Acta is the open protocol layer. [ScopeBlind](https://scopeblind.com) is the commercial managed service for agent governance, dashboards, and enforcement. [protect-mcp](https://www.npmjs.com/package/protect-mcp) is the free gateway.

### Links

- [acta.today](https://acta.today) — live public record instance
- [scopeblind.com/verify](https://scopeblind.com/verify) — browser-based receipt verifier
- [IETF Internet-Draft](https://datatracker.ietf.org/doc/draft-farley-acta-signed-receipts/)
- [Protocol specification](https://github.com/VeritasActa/verify/blob/main/PROTOCOL.md)
- [npm packages](https://www.npmjs.com/org/veritasacta)
