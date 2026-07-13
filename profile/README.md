<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="ai2web-logo-white.svg">
  <img alt="AI2Web" src="ai2web-logo-black.svg" width="340">
</picture>

### Describe your website once. AI2Web makes it understandable to every AI.

The open **protocol, specification, framework and reference implementations** that make any website understandable and actionable to AI agents.

[Website](https://ai2web.dev) · [Validator](https://ai2web.dev/#validator) · [Specification](https://github.com/ai2web-foundation/ai2web-spec) · [RFCs](https://github.com/ai2web-foundation/ai2web-spec/tree/main/rfcs) · [Whitepaper](https://github.com/ai2web-foundation/docs)

<a href="https://www.producthunt.com/products/ai2web?embed=true&utm_source=badge-featured&utm_medium=badge&utm_campaign=badge-ai2web" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=1193322&theme=dark&t=1783854932637" alt="AI2Web - Describe your site once. Every AI agent can use it. | Product Hunt" width="250" height="54" /></a>

</div>

---

## What is AI2Web?

AI agents shouldn't have to scrape HTML and guess at forms. AI2Web lets a site **describe its capabilities once**, in a single capability manifest at `/ai2w`, and then be understood and used by any AI: what the site is, what it offers, what actions it supports, and how to do them safely.

From that one description, AI2Web speaks whichever protocol an assistant understands, so you do not rebuild for each one.

**AI2Web is not "the MCP for websites."** It is the **interoperability layer** for AI-enabled websites: one capability model across many agent protocols (MCP, ACP, REST, GraphQL, OpenAPI, feeds and more), plus the discovery, validation, governance and analytics that individual protocol specs intentionally leave out. Like a browser that speaks HTTP/1.1, HTTP/2, HTTP/3, WebSockets and WebRTC behind one experience, AI2Web sits above the transports and negotiates which to use, so any protocol's success is a tailwind.

## Why it matters

- **Less waste, greener AI.** Making every model render a full page to find one price burns compute, bandwidth and energy. A structured layer sends a few kilobytes of meaning instead of megabytes of markup.
- **One place, not a dozen portals.** Enable, validate, monitor and manage your AI presence once, instead of repeating the fragmentation the web already lived through.
- **Safe by design.** Discovery is open, but anything sensitive (a payment, a refund, a data export) always asks the user to approve first.
- **Open and neutral.** The protocol, spec and SDKs are open source. If a neutral discovery standard emerges, AI2Web is carried by it rather than competing with it.

## Repositories

| Repository | What it is |
|---|---|
| [**ai2web-spec**](https://github.com/ai2web-foundation/ai2web-spec) | The protocol: specification, JSON Schema, RFCs (0000 to 0011), conformance suite, reference manifests |
| [**ai2web-js**](https://github.com/ai2web-foundation/ai2web-js) | TypeScript / JavaScript / React framework: the `@ai2web/*` packages (core, validator, adapters, connector) |
| [**ai2web-php**](https://github.com/ai2web-foundation/ai2web-php) | PHP SDK |
| [**ai2web-python**](https://github.com/ai2web-foundation/ai2web-python) | Python SDK |
| [**ai2web-go**](https://github.com/ai2web-foundation/ai2web-go) | Go SDK |
| [**ai2web-dotnet**](https://github.com/ai2web-foundation/ai2web-dotnet) | .NET SDK (C#) |
| [**ai2web-wordpress**](https://github.com/ai2web-foundation/ai2web-wordpress) | WordPress and WooCommerce plugin |
| [**ai2web-directory**](https://github.com/ai2web-foundation/ai2web-directory) | The Discovery Network service (public metadata only) |
| [**ai2web.dev**](https://github.com/ai2web-foundation/ai2web.dev) | The website and live AI Readiness Validator |
| [**ai2web-validator**](https://github.com/ai2web-foundation/ai2web-validator) | The validator API: a Worker that scores any site's AI readiness over REST and MCP (validator.ai2web.dev) |
| [**ai2web-chrome**](https://github.com/ai2web-foundation/ai2web-chrome) | Chrome extension: check any site's AI readiness from the toolbar |
| [**docs**](https://github.com/ai2web-foundation/docs) | Whitepaper, positioning and strategy |

## Reference implementations

The framework is authored in TypeScript but ships as standard JavaScript, so it works in **TypeScript, JavaScript and React**, with SDKs across **PHP, Python, Go and .NET** and a **WordPress** plugin. Every SDK reproduces the same conformance contract, and the JS adapters (MCP, GraphQL, ACP, OpenAPI) all route through one guarded executor so the security rules hold uniformly.

npm packages under the `@ai2web` scope include `@ai2web/core`, `@ai2web/validator`, `@ai2web/mcp-bridge`, `@ai2web/graphql-adapter`, `@ai2web/acp-adapter`, `@ai2web/openapi-adapter`, `@ai2web/react`, `@ai2web/server` and `@ai2web/connector`.

## Make your site AI-ready

1. Publish a capability manifest at `/ai2w` (by hand, via an SDK, or the WordPress plugin).
2. Add the required `/.well-known/ai2w` discovery anchor pointing to it.
3. Validate it and get your **AI Readiness Score** out of 100 at [ai2web.dev](https://ai2web.dev/#validator).
4. Agents discover it, negotiate a capability set, and can act, with approval on anything sensitive.

```
GET  /.well-known/ai2w   discovery anchor (required)
GET  /ai2w               the capability manifest (canonical home)
POST /ai2w/negotiate     agree a capability set + transport
GET  /ai2w/{module}      content · products · actions · events · search · agent
```

## The one primitive everything hangs off

```
Capability Model  ->  Framework  ->  Discovery Network  ->  Analytics
```

## Governance and licence

Stewarded by the **AI2Web Foundation**, with a commercial platform layer by **Polarize**. Code is **MIT**; the specification and docs are **CC-BY-4.0**. Contributions are welcome: see the community health files in this `.github` repository, and open an issue or discussion on any project repo.

<div align="center">

Created by [Roland Farkas](https://rolandfarkas.com) at [Polarize Ltd](https://polarize.ltd)

</div>
