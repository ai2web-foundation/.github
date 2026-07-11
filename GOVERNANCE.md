# AI2Web Governance

AI2Web deliberately separates the **open standard** from the **commercial platform** so the protocol can be trusted as vendor-neutral while a sustainable business funds its development.

## Two entities

**AI2Web Foundation** - stewards the open standard.
- Owns: the `ai2w` protocol specification, JSON Schema, RFCs, reference SDKs (`@ai2web/*`, PHP), the WordPress plugin, the validator, the conformance suite, and documentation.
- Licences: specification & docs under **CC-BY-4.0**; code under **MIT**.
- Mandate: keep the protocol small, vendor-neutral, backwards-compatible, and implementable by anyone.

**Polarize Ltd** - operates the commercial platform.
- Owns: AI2Web Cloud (hosted endpoints, monitoring, event delivery), capability-level analytics, the Enterprise Gateway, Discovery-Network-Pro, and certification.
- Builds on the open standard like anyone else; holds no special protocol privileges.

## Decision-making (bootstrap phase)

While the project is young, the Foundation maintainers make decisions by lazy consensus on GitHub. As adoption grows this will formalise into:
- a maintainers group with published membership,
- an RFC process (already in `ai2web-spec/rfcs/`) as the path for all normative changes,
- semantic versioning of the protocol with a public changelog.

## The RFC process

All changes to protocol behaviour go through an RFC (copy `ai2web-spec/rfcs/rfc-template.md`). An RFC is **Accepted** only when it updates the spec, the JSON Schema, and the conformance cases together, and keeps the reference implementations in sync.

## Trademark

"AI2Web" and the AI²W mark are held by the Foundation. Conformant implementations may state "AI2Web-compatible"; use of the marks otherwise requires permission.
