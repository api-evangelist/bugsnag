# Bugsnag

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

BugSnag is an application stability monitoring platform from SmartBear that helps software teams detect, diagnose and fix errors in web, mobile, desktop and back-end applications. It combines error monitoring, real user monitoring and end-to-end distributed tracing behind a stability score that tells a team whether a release is safe to ship. BugSnag publishes six OpenAPI 3.0 definitions on SwaggerHub under the smartbear-public organization: a 141-operation Data Access API on api.bugsnag.com (errors, events, projects, releases, span groups, traces, feature flags and a full SCIM 2.0 provisioning surface), plus ingest and build-time APIs for error reporting (notify.bugsnag.com), session tracking (sessions.bugsnag.com), OTLP trace ingest (otlp.bugsnag.com), build notification (build.bugsnag.com) and symbol/source-map upload (upload.bugsnag.com). Agent access is first class: SmartBear runs a hosted MCP server at bugsnag.mcp.smartbear.com behind OAuth 2.1, and ships the same 19 BugSnag tools in the local @smartbear/mcp npm package.

**Areas:** Monitoring · Observability · Error Monitoring · Application Performance Monitoring · Distributed Tracing · Developer Tools · SmartBear

## Bugsnag on APIs.io

Everything profiled for Bugsnag is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/bugsnag/](https://apis.io/providers/bugsnag/)** — or go straight to one of the APIs or properties below.

### APIs (26)

- [bugsnag Builds API](https://apis.io/apis/bugsnag/bugsnag-builds-api/) — Notify Bugsnag about application builds and deployments. Build notifications are used to track releases, identify regressions, and associate source control…
- [bugsnag Collaborators API](https://apis.io/apis/bugsnag/bugsnag-collaborators-api/) — Manage collaborators within an organization or project. Collaborators are users who have access to view and manage Bugsnag data.
- [bugsnag Comments API](https://apis.io/apis/bugsnag/bugsnag-comments-api/) — Manage comments on errors. Comments allow team members to discuss and annotate specific errors.
- [bugsnag Errors API](https://apis.io/apis/bugsnag/bugsnag-errors-api/) — Access and manage errors within projects. Errors represent groups of similar events that have been detected by Bugsnag.
- [bugsnag EventFields API](https://apis.io/apis/bugsnag/bugsnag-eventfields-api/) — Access event field definitions for projects. Event fields describe the available data dimensions for filtering and searching events.
- [bugsnag Events API](https://apis.io/apis/bugsnag/bugsnag-events-api/) — Access individual error events. Events represent individual occurrences of an error within a project.
- [bugsnag Organizations API](https://apis.io/apis/bugsnag/bugsnag-organizations-api/) — Access and manage organizations. An organization is the top-level entity in Bugsnag that contains projects and collaborators.
- [bugsnag Pivots API](https://apis.io/apis/bugsnag/bugsnag-pivots-api/) — Access pivot data for errors. Pivots allow you to group and analyze error data by various dimensions such as browser, device, or location.
- [bugsnag Projects API](https://apis.io/apis/bugsnag/bugsnag-projects-api/) — Access and manage projects within an organization. Projects represent individual applications being monitored by Bugsnag.
- [bugsnag Releases API](https://apis.io/apis/bugsnag/bugsnag-releases-api/) — Access release information for projects. Releases represent deployed versions of your application and their associated error data.
- [bugsnag Sessions API](https://apis.io/apis/bugsnag/bugsnag-sessions-api/) — Report session data to Bugsnag for stability score calculations. Sessions represent periods of user activity and are used to compute crash-free session and…
- [bugsnag Stability API](https://apis.io/apis/bugsnag/bugsnag-stability-api/) — Access stability metrics for projects. Stability data provides crash-free session and user percentages across releases.
- [bugsnag Traces API](https://apis.io/apis/bugsnag/bugsnag-traces-api/) — Send OpenTelemetry trace data to Bugsnag for performance monitoring. Spans represent individual operations and are assembled into traces that visualize…
- [bugsnag Trends API](https://apis.io/apis/bugsnag/bugsnag-trends-api/) — Access trend data for errors and projects. Trends provide time-series data showing how error rates and stability change over time.
- [Bugsnag Current User API](https://apis.io/apis/bugsnag/bugsnag-current-user-api/) — Access information about the currently authenticated user.
- [Bugsnag Android API](https://apis.io/apis/bugsnag/bugsnag-android-api/) — ProGuard/DexGuard/R8 mappings for obfuscated Java/Kotlin and NDK symbol files for shared object (.so) files
- [Bugsnag Apple API](https://apis.io/apis/bugsnag/bugsnag-apple-api/) — Debug symbol (.dSYM) files for release builds
- [Bugsnag Dart API](https://apis.io/apis/bugsnag/bugsnag-dart-api/) — Symbol files for split debug Dart builds
- [Bugsnag Integrations API](https://apis.io/apis/bugsnag/bugsnag-integrations-api/) — The Integrations API from Bugsnag — 8 operation(s) for integrations.
- [Bugsnag JavaScript API](https://apis.io/apis/bugsnag/bugsnag-javascript-api/) — Source maps for minified JavaScript
- [Bugsnag Linux API](https://apis.io/apis/bugsnag/bugsnag-linux-api/) — Symbol files for shared object (.so) files
- [Bugsnag Minidump API](https://apis.io/apis/bugsnag/bugsnag-minidump-api/) — Upload minidump files and optional associated event data. The minidump file must be included in the request as the `upload_file_minidump` request part.…
- [Bugsnag Minidumps API](https://apis.io/apis/bugsnag/bugsnag-minidumps-api/) — Breakpad symbol files for Minidumps
- [Bugsnag Nintendo API](https://apis.io/apis/bugsnag/bugsnag-nintendo-api/) — Symbol files for Nintendo Switch
- [Bugsnag SCIM API](https://apis.io/apis/bugsnag/bugsnag-scim-api/) — The SCIM API from Bugsnag — 4 operation(s) for scim.
- [Bugsnag Unity API](https://apis.io/apis/bugsnag/bugsnag-unity-api/) — IL2CPP mapping files for Unity

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Bugsnag Webhook Events](https://apis.io/asyncapis/bugsnag/bugsnag-webhooks-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/webhook](https://apis.io/channels/bugsnag/webhook/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [BugSnag MCP (SmartBear MCP Server)](https://apis.io/servers/bugsnag/bugsnag-mcp-smartbear-mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Bugsnag Agentic Access](https://apis.io/agentic-access/bugsnag/bugsnag-agentic-access/)

#### JSON Schema (45)

The data models the API reads and writes.

- [ApplicationInfo](https://apis.io/schemas/bugsnag/bugsnag-applicationinfo/)
- [Breadcrumb](https://apis.io/schemas/bugsnag/bugsnag-breadcrumb/)
- [BreadcrumbPayload](https://apis.io/schemas/bugsnag/bugsnag-breadcrumbpayload/)
- [Bugsnag Build](https://apis.io/schemas/bugsnag/bugsnag-build/)
- [BuildPayload](https://apis.io/schemas/bugsnag/bugsnag-buildpayload/)
- [BuildResponse](https://apis.io/schemas/bugsnag/bugsnag-buildresponse/)
- [Collaborator](https://apis.io/schemas/bugsnag/bugsnag-collaborator/)
- [CollaboratorInvite](https://apis.io/schemas/bugsnag/bugsnag-collaboratorinvite/)
- [CollaboratorUpdate](https://apis.io/schemas/bugsnag/bugsnag-collaboratorupdate/)
- [Comment](https://apis.io/schemas/bugsnag/bugsnag-comment/)
- [CommentCreate](https://apis.io/schemas/bugsnag/bugsnag-commentcreate/)
- [DeviceInfo](https://apis.io/schemas/bugsnag/bugsnag-deviceinfo/)
- [Error](https://apis.io/schemas/bugsnag/bugsnag-error/)
- [Bugsnag Error Event](https://apis.io/schemas/bugsnag/bugsnag-error-event/)
- [ErrorItem](https://apis.io/schemas/bugsnag/bugsnag-erroritem/)
- [ErrorResponse](https://apis.io/schemas/bugsnag/bugsnag-errorresponse/)
- [ErrorUpdate](https://apis.io/schemas/bugsnag/bugsnag-errorupdate/)
- [Event](https://apis.io/schemas/bugsnag/bugsnag-event/)
- [EventField](https://apis.io/schemas/bugsnag/bugsnag-eventfield/)
- [EventPayload](https://apis.io/schemas/bugsnag/bugsnag-eventpayload/)
- [Exception](https://apis.io/schemas/bugsnag/bugsnag-exception/)
- [ExceptionPayload](https://apis.io/schemas/bugsnag/bugsnag-exceptionpayload/)
- [ExportTraceServiceRequest](https://apis.io/schemas/bugsnag/bugsnag-exporttraceservicerequest/)
- [ExportTraceServiceResponse](https://apis.io/schemas/bugsnag/bugsnag-exporttraceserviceresponse/)
- [KeyValue](https://apis.io/schemas/bugsnag/bugsnag-keyvalue/)
- …and 20 more published on APIs.io

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Bugsnag Structure](https://apis.io/json-structure/bugsnag/bugsnag-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Bugsnag Context](https://apis.io/jsonld/bugsnag/bugsnag-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Bugsnag Domain Vocabulary](https://apis.io/vocabularies/bugsnag/bugsnag-vocabulary/)

#### Collections (21)

Postman and Open Collection request collections.

- [Bugsnag Build API](https://apis.io/collections/bugsnag/open-bugsnag-build/)
- [Bugsnag Build Builds API](https://apis.io/collections/bugsnag/open-bugsnag-builds-api/)
- [Bugsnag Build Builds Collaborators API](https://apis.io/collections/bugsnag/open-bugsnag-collaborators-api/)
- [Bugsnag Build Builds Comments API](https://apis.io/collections/bugsnag/open-bugsnag-comments-api/)
- [Bugsnag Build Builds CurrentUser API](https://apis.io/collections/bugsnag/open-bugsnag-currentuser-api/)
- [Bugsnag Data Access API](https://apis.io/collections/bugsnag/open-bugsnag-data-access/)
- [Bugsnag Error Reporting API](https://apis.io/collections/bugsnag/open-bugsnag-error-reporting/)
- [Bugsnag Build Builds Errors API](https://apis.io/collections/bugsnag/open-bugsnag-errors-api/)
- [Bugsnag Build Builds EventFields API](https://apis.io/collections/bugsnag/open-bugsnag-eventfields-api/)
- [Bugsnag Build Builds Events API](https://apis.io/collections/bugsnag/open-bugsnag-events-api/)
- [Bugsnag Build Builds Notifications API](https://apis.io/collections/bugsnag/open-bugsnag-notifications-api/)
- [Bugsnag Build Builds Organizations API](https://apis.io/collections/bugsnag/open-bugsnag-organizations-api/)
- [Bugsnag Build Builds Pivots API](https://apis.io/collections/bugsnag/open-bugsnag-pivots-api/)
- [Bugsnag Build Builds Projects API](https://apis.io/collections/bugsnag/open-bugsnag-projects-api/)
- [Bugsnag Build Builds Releases API](https://apis.io/collections/bugsnag/open-bugsnag-releases-api/)
- [Bugsnag Session Tracking API](https://apis.io/collections/bugsnag/open-bugsnag-session-tracking/)
- [Bugsnag Build Builds Sessions API](https://apis.io/collections/bugsnag/open-bugsnag-sessions-api/)
- [Bugsnag Build Builds Stability API](https://apis.io/collections/bugsnag/open-bugsnag-stability-api/)
- [Bugsnag Trace API](https://apis.io/collections/bugsnag/open-bugsnag-trace/)
- [Bugsnag Build Builds Traces API](https://apis.io/collections/bugsnag/open-bugsnag-traces-api/)
- [Bugsnag Build Builds Trends API](https://apis.io/collections/bugsnag/open-bugsnag-trends-api/)

#### Overlays (32)

OpenAPI overlays, including conversational phrasing for each operation.

- [Bugsnag Android Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-android-api-phrasing-overlay/)
- [Bugsnag Apple Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-apple-api-phrasing-overlay/)
- [Bugsnag Build Api Overlay](https://apis.io/overlays/bugsnag/bugsnag-build-api-overlay/)
- [Bugsnag Builds Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-builds-api-phrasing-overlay/)
- [Bugsnag Collaborators Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-collaborators-api-phrasing-overlay/)
- [Bugsnag Comments Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-comments-api-phrasing-overlay/)
- [Bugsnag Current User Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-current-user-api-phrasing-overlay/)
- [Bugsnag Dart Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-dart-api-phrasing-overlay/)
- [Bugsnag Data Access Api Overlay](https://apis.io/overlays/bugsnag/bugsnag-data-access-api-overlay/)
- [Bugsnag Error Reporting Api Overlay](https://apis.io/overlays/bugsnag/bugsnag-error-reporting-api-overlay/)
- [Bugsnag Errors Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-errors-api-phrasing-overlay/)
- [Bugsnag Eventfields Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-eventfields-api-phrasing-overlay/)
- [Bugsnag Events Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-events-api-phrasing-overlay/)
- [Bugsnag Integrations Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-integrations-api-phrasing-overlay/)
- [Bugsnag Javascript Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-javascript-api-phrasing-overlay/)
- [Bugsnag Linux Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-linux-api-phrasing-overlay/)
- [Bugsnag Minidump Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-minidump-api-phrasing-overlay/)
- [Bugsnag Minidumps Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-minidumps-api-phrasing-overlay/)
- [Bugsnag Nintendo Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-nintendo-api-phrasing-overlay/)
- [Bugsnag Organizations Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-organizations-api-phrasing-overlay/)
- [Bugsnag Pivots Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-pivots-api-phrasing-overlay/)
- [Bugsnag Projects Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-projects-api-phrasing-overlay/)
- [Bugsnag Releases Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-releases-api-phrasing-overlay/)
- [Bugsnag Scim Api Phrasing Overlay](https://apis.io/overlays/bugsnag/bugsnag-scim-api-phrasing-overlay/)
- [Bugsnag Session Tracking Api Overlay](https://apis.io/overlays/bugsnag/bugsnag-session-tracking-api-overlay/)
- …and 7 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Bugsnag — asyncapi rules](https://apis.io/rules/bugsnag/bugsnag-asyncapi-spectral-rules/)
- [Bugsnag — jsonschema rules](https://apis.io/rules/bugsnag/bugsnag-jsonschema-spectral-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Bugsnag Authentication](https://apis.io/security/bugsnag/bugsnag-authentication/)
- [Bugsnag Domain Security](https://apis.io/security/bugsnag/bugsnag-domain-security/)
- [Bugsnag Trust Center](https://apis.io/security/bugsnag/bugsnag-trust-center/)
- [Bugsnag Vulnerability Disclosure](https://apis.io/security/bugsnag/bugsnag-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Bugsnag Scopes](https://apis.io/scopes/bugsnag/bugsnag-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Bugsnag Plans Pricing](https://apis.io/plans/bugsnag/bugsnag-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Bugsnag Rate Limits](https://apis.io/rate-limits/bugsnag/bugsnag-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Bugsnag Finops](https://apis.io/finops/bugsnag/bugsnag-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://bugsnag.com)
- [Documentation](https://docs.bugsnag.com/)
- [Getting started](https://developer.smartbear.com/bugsnag/docs/getting-started)
- [API reference](https://developer.smartbear.com/bugsnag)
- [Pricing](https://www.bugsnag.com/pricing/)
- [Sign up](https://app.bugsnag.com/user/new/)
- [Support](https://docs.bugsnag.com/support/)
- [Blog](https://smartbear.com/blog/)
- [Terms of service](https://smartbear.com/terms-of-use/)
- [Privacy policy](https://smartbear.com/privacy/)
- [GitHub](https://github.com/bugsnag)
- [Status](https://status.bugsnag.com/)

## API Evangelist rating

**Kin Score 76.9** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.3 |
| Contract quality | 62.1 |
| Contract governance | 45.5 |
| Operational transparency | 81.6 |
| Developer ergonomics | 73.2 |
| Access clarity | 92.1 |

**Agent readiness 53.1** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 45.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/bugsnag/](https://apis.io/providers/bugsnag/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Bugsnag: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/bugsnag/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
