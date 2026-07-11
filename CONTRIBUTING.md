# Contributing to AI2Web

Thanks for helping build the open capability layer for the agentic web. AI2Web is stewarded by the **AI2Web Foundation**; the commercial platform is operated separately by Polarize (see [GOVERNANCE.md](GOVERNANCE.md)).

## Repository layout

| Path | What | Language |
|---|---|---|
| `ai2web-spec/` | Protocol spec, JSON Schema, RFCs, conformance suite | Markdown / JSON |
| `ai2web-js/` | `@ai2web/*` framework (core, validator, server, mcp-bridge, connector) | TypeScript |
| `ai2web-php/` | PHP SDK | PHP |
| `ai2web-wordpress/` | WordPress + WooCommerce plugin | PHP |
| `ai2web-directory/` | Discovery Network service | TypeScript |
| `ai2web.dev/` | Marketing + docs + web validator | HTML |
| `docs/` | Strategy & positioning | Markdown |

Each top-level directory is designed to become its own repository under `github.com/ai2web-foundation`. Keep changes scoped to one area per PR where possible.

## Development

```bash
# JS/TS framework
cd ai2web-js && npm install && npm run build
node --experimental-strip-types scripts/test-logic.ts   # core logic smoke test
node --experimental-strip-types scripts/spike.ts         # both-sided end-to-end
node scripts/validate.mjs ../ai2web-spec/examples/ecommerce.json

# Conformance (any implementation should pass this)
node --experimental-strip-types ai2web-spec/conformance/run.mjs

# PHP SDK
cd ai2web-php && php tests/run.php
```

Requires **Node 22+** (native TypeScript execution) and **PHP 8.1+**.

## Changing the protocol

The spec is normative. Any change to `ai2web-spec/` that alters behaviour MUST:
1. Be proposed as an **RFC** (`ai2web-spec/rfcs/`, copy `rfc-template.md`).
2. Update the **JSON Schema** and the **conformance cases** together.
3. Keep reference implementations (`@ai2web/core`, `ai2web-php`) in sync.
4. Respect the permanent boundary: **AI2Web does not define transports.**

## Pull requests

- Conventional, focused commits. Add/adjust tests. Update docs.
- CI must pass (typecheck, tests, conformance) - see `.github/workflows/ci.yml`.
- By contributing you agree your code is MIT and spec/docs are CC-BY-4.0.
