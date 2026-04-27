# Veritas Acta

**Open protocol for signed, independently verifiable machine decisions.**

Every consequential machine action (tool calls, delegations, policy evaluations,
sensor outputs) produces an Ed25519-signed receipt. Anyone can verify the receipt
offline using only the public key. No vendor trust required, no phone-home.

> **Receipt format:** ScopeBlind emits Veritas Acta receipts. Legacy ScopeBlind
> receipts remain verifiable, but Acta v0.1 is the canonical format going forward.

## Start here

| Pin | What it is | Path |
|---|---|---|
| **[Acta](https://github.com/VeritasActa/Acta)** | Protocol charter, ontology, and reference site | `veritasacta.com` |
| **[verify](https://github.com/VeritasActa/verify)** | Apache-2.0 offline verifier CLI | `npm i @veritasacta/verify` |
| **[drafts](https://github.com/VeritasActa/drafts)** | IETF Internet-Draft sources for `draft-farley-acta-signed-receipts` | live on datatracker |
| **[acta-mcp](https://github.com/VeritasActa/acta-mcp)** | MCP server exposing the Acta verifier as a tool | `npm i acta-mcp` |

## Standards

| Document | Where | Status |
|---|---|---|
| `draft-farley-acta-signed-receipts-01` | [datatracker.ietf.org](https://datatracker.ietf.org/doc/draft-farley-acta-signed-receipts/) | Live IETF Internet-Draft (individual submission) |
| `draft-farley-acta-knowledge-units-00` | [datatracker.ietf.org](https://datatracker.ietf.org/doc/draft-farley-acta-knowledge-units/) | Live IETF Internet-Draft |
| Receipt Format Specification | [github.com/VeritasActa/Acta](https://github.com/VeritasActa/Acta/blob/main/docs/protocol-spec.md) | v0.1 |
| Charter (10 invariants) | [github.com/VeritasActa/Acta](https://github.com/VeritasActa/Acta/blob/main/CHARTER.md) | Ratified |
| Cross-implementation conformance fixtures | [github.com/ScopeBlind/agent-governance-testvectors](https://github.com/ScopeBlind/agent-governance-testvectors) | 14+ implementations cross-verifying byte-identical canonical output |

## Implementations

| Package | Purpose | License |
|---|---|---|
| [`@veritasacta/verify`](https://npmjs.com/package/@veritasacta/verify) | Unified offline verifier (Ed25519, VOPRF, selective disclosure, Knowledge Units) | Apache-2.0 |
| [`@veritasacta/artifacts`](https://npmjs.com/package/@veritasacta/artifacts) | Signed artifact envelope (canonical JCS, Ed25519) | Apache-2.0 |
| [`@veritasacta/protocol`](https://npmjs.com/package/@veritasacta/protocol) | Receipt format types and conformance helpers | Apache-2.0 |
| [`protect-mcp`](https://npmjs.com/package/protect-mcp) | Runtime receipt signing for MCP servers (Cedar policies, Ed25519) | MIT |
| [`acta-mcp`](https://npmjs.com/package/acta-mcp) | MCP server exposing the Acta verifier as an agent tool | MIT |

## External adoption

- **Microsoft Agent Governance Toolkit**: listed as [Appendix A.9 conformant implementation](https://datatracker.ietf.org/doc/draft-farley-acta-signed-receipts/) in the IETF draft. Tutorial 33 covers offline-verifiable decision receipts. Tutorial 46 covers selective-disclosure receipts via RFC 6962 Merkle commitments.
- **AWS Cedar**: integrated as policy backend for `protect-mcp`. Two PRs merged in `cedar-policy/cedar-for-agents`.
- **Foundation submissions in flight**: Microsoft AGT submitted to AAIF, OpenSSF (Sandbox), LF AI & Data, CoSAI / OASIS WS4, OWASP ASI, MITRE ATLAS, with the Acta receipt format cited as the open-standards integration evidence.
- **In-toto / SLSA**: Decision Receipt predicate proposal at [in-toto/attestation#549](https://github.com/in-toto/attestation/pull/549).

## Live instances

- [`veritasacta.com`](https://veritasacta.com): protocol reference instance. Hash-chained ledger with daily Ed25519-signed anchors.
- [`acta.today/wiki`](https://acta.today/wiki): verified knowledge base. 50+ entries produced by frontier AI models through adversarial deliberation.

## Verify

```bash
npx @veritasacta/verify receipt.json
```

No server. No account. No trust required. Apache-2.0.
