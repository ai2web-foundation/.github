# Security Policy

AI2Web lets AI agents discover and, with consent, act on websites - so security is a first-class concern. The protocol's own security model lives in [the specification, §9](https://github.com/ai2web-foundation/ai2web-spec/blob/main/spec/ai2w-v0.1.md) ("discovery is safe, execution is controlled").

## Reporting a vulnerability

**Do not open a public issue for security vulnerabilities.**

Email **security@ai2web.dev** with:
- a description of the issue and its impact,
- steps to reproduce (or a proof of concept),
- affected component/version.

We aim to acknowledge within 3 business days and to provide a remediation timeline after triage. Please give us reasonable time to fix before public disclosure. We credit reporters unless you prefer to remain anonymous.

## Scope

In scope: the spec, `@ai2web/*` packages, the WordPress plugin, the PHP SDK, the Discovery Network service, and the connector.

## Security principles implementers must follow

- **Discovery is not execution** - the manifest never performs actions.
- **Least privilege + explicit consent** - high-risk actions (purchase, payment, data change/export, booking confirmation, account deletion) MUST require user approval.
- **OAuth2 + PKCE** for delegated agent actions; short-lived, scoped, revocable tokens. Avoid static consumer API keys.
- **Audit logging** of agent identity, action, approval status, and result.
- **Rate limiting** and abuse controls on all write paths.
- **Privacy by design** - the Discovery Network stores only public metadata; never customer data.
