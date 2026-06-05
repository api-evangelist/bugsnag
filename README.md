# bugsnag (bugsnag)

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
