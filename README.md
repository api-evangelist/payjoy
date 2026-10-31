# PayJoy

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

PayJoy is a fintech that provides financial access to underserved consumers in emerging markets through smartphone financing and a secured credit card that requires only a government ID. Its Partner Developer Portal exposes a REST Partner API (Sales Integration) so retail and OEM partners can integrate PayJoy point-of-sale financing: retrieve cart and sale information, list merchants and sales clerks, offer and process customer repayments, create and pay payment references, redeem and cancel vouchers, pay down payments, and pull transaction history for reconciliation. A separate E-commerce API supports online checkout and credit-application flows. Authentication is by API key; webhooks are HMAC-SHA256 signed. Founded 2015; backed by Greylock and Union Square Ventures.

**Areas:** Company · Fintech · Payments · Lending · Buy Now Pay Later · Point-of-Sale · Emerging Markets · Financial Inclusion · Partner API

## PayJoy on APIs.io

Everything profiled for PayJoy is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/payjoy/](https://apis.io/providers/payjoy/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [PayJoy E-commerce API](https://apis.io/apis/payjoy/payjoy-e-commerce-api/) — REST API for online checkout and credit-application flows: retrieve supported devices, begin a sale, and receive completion webhooks. Bearer-token…
- [PayJoy Carts API](https://apis.io/apis/payjoy/payjoy-carts-api/) — Retrieve cart information.
- [PayJoy Down Payments API](https://apis.io/apis/payjoy/payjoy-down-payments-api/) — The Down Payments API from PayJoy — 1 operation(s) for down payments.
- [PayJoy Merchants API](https://apis.io/apis/payjoy/payjoy-merchants-api/) — Retrieve merchants information.
- [PayJoy Reconciliation API](https://apis.io/apis/payjoy/payjoy-reconciliation-api/) — The Reconciliation API from PayJoy — 1 operation(s) for reconciliation.
- [PayJoy Repayments API](https://apis.io/apis/payjoy/payjoy-repayments-api/) — The Repayments API from PayJoy — 3 operation(s) for repayments.
- [PayJoy SalesClerks API](https://apis.io/apis/payjoy/payjoy-salesclerks-api/) — Retrieve sales clerks information.
- [PayJoy Status API](https://apis.io/apis/payjoy/payjoy-status-api/) — Displays the status of the application.
- [PayJoy Vouchers API](https://apis.io/apis/payjoy/payjoy-vouchers-api/) — Endpoints related to vouchers management

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Payjoy Webhooks](https://apis.io/asyncapis/payjoy/payjoy-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [payjoy-partner](https://apis.io/servers/payjoy/payjoy-partner/)

#### Collections (8)

Postman and Open Collection request collections.

- [PayJoy Partner API V2 Carts API](https://apis.io/collections/payjoy/open-payjoy-carts-api/)
- [PayJoy Partner API V2 Carts Down Payments API](https://apis.io/collections/payjoy/open-payjoy-down-payments-api/)
- [PayJoy Partner API V2 Carts Merchants API](https://apis.io/collections/payjoy/open-payjoy-merchants-api/)
- [PayJoy Partner API V2 Carts Reconciliation API](https://apis.io/collections/payjoy/open-payjoy-reconciliation-api/)
- [PayJoy Partner API V2 Carts Repayments API](https://apis.io/collections/payjoy/open-payjoy-repayments-api/)
- [PayJoy Partner API V2 Carts SalesClerks API](https://apis.io/collections/payjoy/open-payjoy-salesclerks-api/)
- [PayJoy Partner API V2 Carts Status API](https://apis.io/collections/payjoy/open-payjoy-status-api/)
- [PayJoy Partner API V2 Carts Vouchers API](https://apis.io/collections/payjoy/open-payjoy-vouchers-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Payjoy Partner Api Overlay](https://apis.io/overlays/payjoy/payjoy-partner-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Payjoy Authentication](https://apis.io/security/payjoy/payjoy-authentication/)
- [Payjoy Domain Security](https://apis.io/security/payjoy/payjoy-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.payjoy.com/)
- [Documentation](https://developers.payjoy.com/)
- [Getting started](https://developers.payjoy.com/sales-integration/quickstart/quick-start-guide)
- [Sign up](https://app.payjoy.com/admin-console/login)
- [Support](https://developers.payjoy.com/sales-integration/support/faq)
- [Blog](https://www.payjoy.com/blog)
- [Terms of service](https://www.payjoy.com/terms)
- [Privacy policy](https://www.payjoy.com/privacy)
- [GitHub](https://github.com/payjoy)

## API Evangelist rating

**Kin Score 43.3** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 57.1 |
| Contract governance | 4.5 |
| Operational transparency | 10.5 |
| Developer ergonomics | 66.1 |
| Access clarity | 34.2 |

**Agent readiness 31.7** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 22.3** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/payjoy/](https://apis.io/providers/payjoy/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for PayJoy: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/payjoy/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
