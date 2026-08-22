# bugsnag (bugsnag)

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

Bugsnag is an application stability monitoring platform that helps software teams detect, diagnose, and fix errors in web, mobile, and back-end applications.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/apis.yml)

## Timestamps

- **Modified:** 2026-05-19

## APIs

### Bugsnag Data Access API

The Bugsnag Data Access API provides programmatic access to information about your organization, projects, errors, events, and more. It allows developers to build custom integrations and dashboards using their Bugsnag data. The REST API uses JSON and requires authentication via an API token, which can be found in Bugsnag account settings. It supports querying error trends, project configurations, collaborators, and release information.

- **Human URL:** [https://docs.bugsnag.com/api/data-access/](https://docs.bugsnag.com/api/data-access/)
- **Base URL:** `https://api.bugsnag.com`

#### Tags

- Analytics
- Application Stability
- Data Access
- Error Monitoring

#### Properties

- [Documentation](https://docs.bugsnag.com/api/data-access/)
- [OpenAPI](openapi/bugsnag-data-access-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bugsnag-data-access.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bugsnag-data-access.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bugsnag Error Reporting API

The Bugsnag Error Reporting API allows applications to report error and exception details directly to the Bugsnag dashboard. If there is no official SDK available for your platform, you can use this API to send error payloads manually. The API accepts structured JSON payloads containing exception details, stack traces, device information, and application metadata. It is the underlying mechanism used by all official Bugsnag notifier SDKs to deliver error data.

- **Human URL:** [https://docs.bugsnag.com/api/error-reporting/](https://docs.bugsnag.com/api/error-reporting/)
- **Base URL:** `https://notify.bugsnag.com`

#### Tags

- Error Monitoring
- Error Reporting
- Events
- Notifications

#### Properties

- [Documentation](https://docs.bugsnag.com/api/error-reporting/)
- [OpenAPI](openapi/bugsnag-error-reporting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bugsnag-error-reporting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bugsnag-error-reporting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bugsnag Session Tracking API

The Bugsnag Session Tracking API enables applications to report session data, which is used to calculate release stability scores in the Bugsnag dashboard. By tracking when user sessions start and end, Bugsnag can determine crash rates and overall application stability. This API works in conjunction with the Error Reporting API to provide a complete picture of application health. Session data is required for accurate stability metrics and crash-free user percentages.

- **Human URL:** [https://docs.bugsnag.com/api/sessions/](https://docs.bugsnag.com/api/sessions/)
- **Base URL:** `https://sessions.bugsnag.com`

#### Tags

- Application Monitoring
- Sessions
- Stability

#### Properties

- [Documentation](https://docs.bugsnag.com/api/sessions/)
- [OpenAPI](openapi/bugsnag-session-tracking-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bugsnag-session-tracking.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bugsnag-session-tracking.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bugsnag Build API

The Bugsnag Build API allows you to provide information about your application builds, releases, and deployments. By notifying Bugsnag when you deploy, you can track which releases introduced new errors, view error trends across releases, and identify regressions. The API accepts build metadata including version numbers, source control information, and release stages. It integrates with CI/CD pipelines to automate release tracking.

- **Human URL:** [https://docs.bugsnag.com/api/build/](https://docs.bugsnag.com/api/build/)
- **Base URL:** `https://build.bugsnag.com`

#### Tags

- Builds
- CI/CD
- Deployments
- Releases

#### Properties

- [Documentation](https://docs.bugsnag.com/api/build/)
- [OpenAPI](openapi/bugsnag-build-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bugsnag-build.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bugsnag-build.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Bugsnag Trace API

The Bugsnag Trace API allows applications to send OpenTelemetry span data to Bugsnag for performance monitoring and analysis. It enables developers to track request latency, identify slow operations, and monitor application performance alongside error data. The API accepts trace data in the OpenTelemetry format, making it compatible with existing instrumentation libraries and observability tooling. Performance data is displayed in the Bugsnag dashboard alongside error information.

- **Human URL:** [https://docs.bugsnag.com/api/](https://docs.bugsnag.com/api/)
- **Base URL:** `https://otlp.bugsnag.com`

#### Tags

- Observability
- OpenTelemetry
- Performance
- Tracing

#### Properties

- [Documentation](https://docs.bugsnag.com/api/)
- [OpenAPI](openapi/bugsnag-trace-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/bugsnag-trace.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/bugsnag-trace.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/bugsnag)
- [LinkedIn](https://www.linkedin.com/company/bugsnag2)
- [AsyncAPI](asyncapi/bugsnag-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Schema](json-schema/bugsnag-error-event-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/bugsnag-build-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/bugsnag-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Features](undefined)
