# Veritas Acta

**Open protocol for signed, independently verifiable machine decisions.**

Every consequential machine action -- tool calls, delegations, policy evaluations -- produces an Ed25519-signed receipt. Anyone can verify the receipt offline, without trusting the system that created it. The verification is issuer-blind: the verifier cannot learn what it is verifying.

## Protocol

| Standard | Status |
|----------|--------|
| [draft-farley-acta-signed-receipts](https://datatracker.ietf.org/doc/draft-farley-acta-signed-receipts/) | IETF Internet-Draft |
| [Receipt Format Specification](https://github.com/VeritasActa/Acta/blob/main/docs/protocol-spec.md) | v1.0 |
| [Charter -- 10 Invariants](https://github.com/VeritasActa/Acta/blob/main/CHARTER.md) | Ratified |

## Implementations

| Package | Purpose | License | Downloads |
|---------|---------|---------|-----------|
| [@veritasacta/verify](https://npmjs.com/package/@veritasacta/verify) | Offline receipt verification | Apache-2.0 | 820/mo |
| [@veritasacta/artifacts](https://npmjs.com/package/@veritasacta/artifacts) | Signed artifact envelope | Apache-2.0 | 857/mo |
| [@veritasacta/protocol](https://npmjs.com/package/@veritasacta/protocol) | Protocol type definitions | Apache-2.0 | 530/mo |
| [protect-mcp](https://npmjs.com/package/protect-mcp) | Runtime receipt signing | MIT | 2,307/mo |

## Live Instances

- **[veritasacta.com](https://veritasacta.com)** -- Protocol reference instance. Hash-chained ledger with daily Ed25519-signed anchors.
- **[acta.today/wiki](https://acta.today/wiki)** -- Verified knowledge base. 50+ entries produced by 8 frontier AI models through adversarial deliberation.

## Integrations

- [Microsoft Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit/pull/667) -- Receipt verification adapter
- [ScopeBlind](https://scopeblind.com) -- Commercial managed issuance and enforcement

## Verify

```bash
npx @veritasacta/verify receipt.json
```

No server. No account. No trust required. Apache-2.0.
