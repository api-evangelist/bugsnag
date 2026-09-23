---
name: bugsnag-performance-investigation
description: >-
  Investigate a slow screen, request or app start in BugSnag Performance — find
  the worst span groups by percentile, drill into individual slow spans, and
  walk the full distributed trace to locate the bottleneck. Use when asked why
  something is slow, which operation regressed, or where latency is going.
api: bugsnag:bugsnag-data-access-api
base_url: https://api.bugsnag.com
operations:
  - listProjectTraceFields
  - listProjectSpanGroups
  - listProjectSpanGroupSummaries
  - getProjectSpanGroup
  - getProjectSpanGroupTimeline
  - getProjectSpanGroupDistribution
  - listSpansBySpanGroupId
  - listSpansByTraceId
  - getProjectPerformanceScoreOverview
  - getProjectNetworkGroupingRuleset
---

# Investigate a BugSnag performance problem

`https://api.bugsnag.com`, `Authorization: token <PERSONAL_AUTH_TOKEN>`,
`X-Version: 2`.

## 1. Discover the filterable attributes

`listProjectTraceFields` — `GET /projects/{project_id}/trace_fields`.

These are the performance equivalent of event fields: per-project custom
attributes you can filter spans on. Read them before filtering, not after a
`400`.

## 2. Start wide

`getProjectPerformanceScoreOverview` — `GET /projects/{project_id}/performance_overview`
for the project's headline picture.

`listProjectSpanGroups` — `GET /projects/{project_id}/span_groups` (or
`listProjectSpanGroupSummaries`) for the named operations: screen loads, HTTP
calls, app starts. Sort by a duration percentile.

**Sort by p95 or p99, not p50.** A median that looks fine hides the tail that
users actually complain about. `listProjectStarredSpanGroups` narrows to the
operations the team already cares about.

## 3. Characterise one operation

- `getProjectSpanGroup` — `GET /projects/{project_id}/span_groups/{id}` for
  p50/p75/p90/p95/p99.
- `getProjectSpanGroupTimeline` — has it always been this slow, or did it move?
- `getProjectSpanGroupDistribution` — one slow mode or two? A bimodal
  distribution is a different bug from a uniformly slow operation.
- `listProjectSpanGroupPerformanceTargets` — is there a registered target this
  is breaching, or are you inventing a threshold?

## 4. Drill to instances

`listSpansBySpanGroupId` — `GET /projects/{project_id}/span_groups/{id}/spans`.
Sort by duration and take the worst. Each span carries a `trace_id`.

## 5. Walk the trace

`listSpansByTraceId` — `GET /projects/{project_id}/traces/{trace_id}/spans`
returns every span in that trace, with `parent_span_id` giving the hierarchy.
Reconstruct the tree and find where the time actually goes — the slow span group
is often the victim of a child, not the cause.

## If HTTP spans look fragmented

`getProjectNetworkGroupingRuleset` —
`GET /projects/{project_id}/network_endpoint_grouping` shows the URL patterns
used to consolidate network spans. Thousands of one-request span groups usually
means an unparameterised URL (`/users/12345` instead of `/users/{userId}`).

The fix is `updateProjectNetworkGroupingRuleset`
(`PUT /projects/{project_id}/network_endpoint_grouping`), which is a **write**:
it uses OpenAPI path templating with curly braces and wildcard domains
(`https://*.example.com`). It has no dry-run and no documented undo beyond
writing the previous ruleset back. **Read and keep the current ruleset before
you replace it**, and get explicit confirmation before changing it — it changes
how every future span in the project is grouped.

## Reporting rules

- Always name the percentile behind a number.
- Quote the trace id for any example you cite, so a human can open it.
- If the distribution is bimodal, say so; reporting one mean over two
  populations is the most common way to mislead here.
