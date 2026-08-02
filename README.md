# Teikametrics

Teikametrics builds **ARI (Artificial Retail Intelligence)**, an AI platform for brands and
sellers on Amazon, Walmart and TikTok Shop. Founded by Alasdair McLean-Foreman, the platform
pulls advertising, catalog, sales and inventory data from marketplace APIs and applies
retail-trained models to bid management, keyword harvesting, listing and feed optimization,
demand forecasting and profit-based reporting. Product surfaces include Compass, the
Recommendation Hub, Product Catalog, Advertising Optimization, Inventory Optimization,
Market IQ and Business Intelligence, plus an Agency Edition with nested client accounts.

- Website — https://www.teikametrics.com/
- Platform — https://www.teikametrics.com/platform/
- Help Center — https://help.teikametrics.com/en/
- Application — https://app.teikametrics.com/
- GitHub — https://github.com/teikametrics
- Secondary-market listing — https://forgeglobal.com/teikametrics_stock/

## API posture

**Teikametrics is an API consumer, not an API producer.** Contract discovery on 2026-08-02
found no developer portal, no API reference, and no machine-readable contract of any kind
(OpenAPI/Swagger, GraphQL, AsyncAPI, gRPC, MCP, A2A agent card) on any Teikametrics host —
`api.teikametrics.com`, `developer.teikametrics.com` and `docs.teikametrics.com` do not
resolve. Customers integrate through in-app OAuth channel connections to Amazon Advertising,
Amazon Selling Partner, Walmart Marketplace/Advertising and TikTok Shop.

The full probe matrix, including the `app.teikametrics.com` SPA catch-all that answers HTTP
200 with an HTML shell for every `/.well-known/*` path, is recorded in
[`well-known/teikametrics-well-known.yml`](well-known/teikametrics-well-known.yml).

## Artifacts

| Path | Type | Method |
|---|---|---|
| [`llms/teikametrics-llms.txt`](llms/teikametrics-llms.txt) | LLMsTxt | searched — verbatim from `help.teikametrics.com/llms.txt` (70 articles) |
| [`well-known/teikametrics-well-known.yml`](well-known/teikametrics-well-known.yml) | — | probed — full discovery matrix; no first-party well-known document exists |
| [`well-known/teikametrics-help-intercom-security.txt`](well-known/teikametrics-help-intercom-security.txt) | — | probed — evidence only; this is **Intercom's** security.txt, not Teikametrics' |
| [`packages/teikametrics-packages.yml`](packages/teikametrics-packages.yml) | Packages | searched — two first-party npm packages, both internal tooling, zero API SDKs |
| [`security/teikametrics-domain-security.yml`](security/teikametrics-domain-security.yml) | DomainSecurity | probed — TLS 1.3 everywhere; no HSTS, no CAA, no DNSSEC, DMARC `p=quarantine` |

No vulnerability disclosure programme, trust center, status page, changelog, CLI, sandbox or
event surface was found. Nothing was authored on the provider's behalf.
