# Veritas Acta

**Signed records that recipients can verify themselves.**

An open receipt format, offline verification tools and interoperability work.
Instrumented systems issue signed records; recipients obtain keys independently,
check the records and apply their own trust policies.

**A valid signature does not establish claim truth, complete action coverage,
signer authority or recipient acceptance.**

[Try a signed receipt](https://www.veritasacta.com/verify?sample=current) ·
[Integrate](https://www.veritasacta.com/docs) ·
[Specification](https://www.veritasacta.com/specification) ·
[Conformance evidence](https://www.veritasacta.com/conformance)

## Repository map

| Repository | Responsibility |
| --- | --- |
| [verify](https://github.com/VeritasActa/verify) | Offline CLI, shared browser receipt engine, fixtures and release manifest |
| [drafts](https://github.com/VeritasActa/drafts) | Individual Internet-Draft sources and submission history |
| [Acta](https://github.com/VeritasActa/Acta) | Public-record reference application and protocol website, not the receipt specification |
| [acta-mcp](https://github.com/VeritasActa/acta-mcp) | MCP adapter exposing verification tools |
| [verified-runs-grader](https://github.com/VeritasActa/verified-runs-grader) | A worked governed-run grading/attestation workflow |

## Release and standards status

<!-- release-manifest:start -->
Verifier: **[0.10.27](https://github.com/VeritasActa/verify/releases/tag/v0.10.27)**. Status reviewed 2026-10-21.

- [draft-farley-acta-signed-receipts-03](https://datatracker.ietf.org/doc/draft-farley-acta-signed-receipts/): active individual Internet-Draft.
- [draft-farley-acta-knowledge-units-00](https://datatracker.ietf.org/doc/draft-farley-acta-knowledge-units/): expired individual Internet-Draft (expired 2026-10-08).

Internet-Drafts are proposals, not adopted IETF standards or endorsements.
<!-- release-manifest:end -->

## Inspect the implementation evidence

As of 13 October 2026, the [conformance corpus](https://github.com/ScopeBlind/agent-governance-testvectors)
documents implementation drivers and negative fixtures. Read the
[exact workflow run](https://github.com/ScopeBlind/agent-governance-testvectors/actions),
source commit, package version and skipped checks before drawing conclusions.
A driver or integration reference is not blanket certification or corporate endorsement.

The verifier repository includes current `protectmcp:decision` and historical
receipt fixtures. Its browser and CLI regression tests use the same engine and
check successful signatures, wrong/missing keys and tampered records.

## Who maintains it?

Tom Farley / ScopeBlind maintains this project. Independent verification means
recipients can run checks without the issuer, not that an independent foundation
governs the project. Contributions, negative fixtures and interop reports are welcome
through repository issues and pull requests. Use the verifier's
[security policy](https://github.com/VeritasActa/verify/blob/main/SECURITY.md) for vulnerabilities.

The [Acta public record](https://www.veritasacta.com/record) is a reference application.
[ScopeBlind / Legate](https://scopeblind.com) are commercial applications and enforcement
products. Neither is required to verify an individual receipt.

Consult each repository's license and patent notice. Bundled self-checks detect byte
drift; publisher authentication requires an independently trusted reference.
