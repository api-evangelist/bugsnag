# Bugsnag (bugsnag)
Bugsnag is an application stability management platform that helps development teams detect, prioritize, and fix errors and performance issues across their software. Their developer platform provides APIs for error reporting, session tracking, build notifications, performance tracing, and programmatic access to error and project data.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/bugsnag/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Error Monitoring, Application Stability, Error Reporting, Performance, Observability

## Timestamps

- **Created:** 2026-03-20
- **Modified:** 2026-03-20

## APIs

### Bugsnag Data Access API
The Bugsnag Data Access API provides programmatic access to information about your organization, projects, errors, events, and more. It allows developers to build custom integrations and dashboards using their Bugsnag data. The REST API uses JSON and requires authentication via an API token, which can be found in Bugsnag account settings. It supports querying error trends, project configurations, collaborators, and release information.

**Human URL:** [https://docs.bugsnag.com/api/data-access/](https://docs.bugsnag.com/api/data-access/)


#### Tags:

 - Error Monitoring, Application Stability, Data Access, Analytics

#### Properties

- [Documentation](https://docs.bugsnag.com/api/data-access/)
- [OpenAPI](openapi/bugsnag-data-access-openapi.yml)

### Bugsnag Error Reporting API
The Bugsnag Error Reporting API allows applications to report error and exception details directly to the Bugsnag dashboard. If there is no official SDK available for your platform, you can use this API to send error payloads manually. The API accepts structured JSON payloads containing exception details, stack traces, device information, and application metadata. It is the underlying mechanism used by all official Bugsnag notifier SDKs to deliver error data.

**Human URL:** [https://docs.bugsnag.com/api/error-reporting/](https://docs.bugsnag.com/api/error-reporting/)


#### Tags:

 - Error Reporting, Error Monitoring, Notifications, Events

#### Properties

- [Documentation](https://docs.bugsnag.com/api/error-reporting/)
- [OpenAPI](openapi/bugsnag-error-reporting-openapi.yml)

### Bugsnag Session Tracking API
The Bugsnag Session Tracking API enables applications to report session data, which is used to calculate release stability scores in the Bugsnag dashboard. By tracking when user sessions start and end, Bugsnag can determine crash rates and overall application stability. This API works in conjunction with the Error Reporting API to provide a complete picture of application health. Session data is required for accurate stability metrics and crash-free user percentages.

**Human URL:** [https://docs.bugsnag.com/api/sessions/](https://docs.bugsnag.com/api/sessions/)


#### Tags:

 - Sessions, Stability, Application Monitoring

#### Properties

- [Documentation](https://docs.bugsnag.com/api/sessions/)
- [OpenAPI](openapi/bugsnag-session-tracking-openapi.yml)

### Bugsnag Build API
The Bugsnag Build API allows you to provide information about your application builds, releases, and deployments. By notifying Bugsnag when you deploy, you can track which releases introduced new errors, view error trends across releases, and identify regressions. The API accepts build metadata including version numbers, source control information, and release stages. It integrates with CI/CD pipelines to automate release tracking.

**Human URL:** [https://docs.bugsnag.com/api/build/](https://docs.bugsnag.com/api/build/)


#### Tags:

 - Builds, Releases, Deployments, CI/CD

#### Properties

- [Documentation](https://docs.bugsnag.com/api/build/)
- [OpenAPI](openapi/bugsnag-build-openapi.yml)

### Bugsnag Trace API
The Bugsnag Trace API allows applications to send OpenTelemetry span data to Bugsnag for performance monitoring and analysis. It enables developers to track request latency, identify slow operations, and monitor application performance alongside error data. The API accepts trace data in the OpenTelemetry format, making it compatible with existing instrumentation libraries and observability tooling. Performance data is displayed in the Bugsnag dashboard alongside error information.

**Human URL:** [https://docs.bugsnag.com/api/](https://docs.bugsnag.com/api/)


#### Tags:

 - Performance, Tracing, OpenTelemetry, Observability

#### Properties

- [Documentation](https://docs.bugsnag.com/api/)
- [OpenAPI](openapi/bugsnag-trace-openapi.yml)

## Common Properties

- [Portal](https://docs.bugsnag.com/)
- [Documentation](https://docs.bugsnag.com/api/)
- [Website](https://www.bugsnag.com/)
- [PrivacyPolicy](https://smartbear.com/privacy/)
- [TermsOfService](https://smartbear.com/terms-of-use/)
- [Support](https://docs.bugsnag.com/support/)
- [Blog](https://www.bugsnag.com/blog/)
- [Login](https://app.bugsnag.com/user/sign_in)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
