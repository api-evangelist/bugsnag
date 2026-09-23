---
name: bugsnag-triage-errors
description: >-
  Triage open errors in a BugSnag project — discover the project's filter
  fields, list open errors ranked by user impact, pull full diagnostic detail on
  one, and set its status. Use when asked to find what is breaking in an app,
  investigate a crash, or mark an error fixed or ignored.
api: bugsnag:bugsnag-data-access-api
base_url: https://api.bugsnag.com
operations:
  - listUserOrganizations
  - getOrganizationProjects
  - listProjectEventFields
  - listProjectErrors
  - viewErrorOnProject
  - viewLatestEventOnError
  - listEventsOnError
  - updateErrorOnProject
  - createCommentOnError
---

# Triage BugSnag errors

Every call goes to `https://api.bugsnag.com` with
`Authorization: token <PERSONAL_AUTH_TOKEN>`. Send `X-Version: 2` explicitly —
the default API version changes as old versions are retired.

## 1. Resolve the project

1. `listUserOrganizations` — `GET /user/organizations`. Pick the organization id.
2. `getOrganizationProjects` — `GET /organizations/{organization_id}/projects`.
   Match on name, slug, or the `api_key` you find in the app's BugSnag SDK
   configuration.

Skip this whole step if you were given a `project_id`.

## 2. Discover the filters before you filter

`listProjectEventFields` — `GET /projects/{project_id}/event_fields`.

Filter fields are **per project**. Do not hardcode them. Time values accept
extended ISO 8601 UTC (`2018-05-20T00:00:00Z`) or relative shorthand (`7d`,
`24h`). Filters that do not match a project's fields come back as `400
Improperly formatted filters`.

## 3. List the open errors

`listProjectErrors` — `GET /projects/{project_id}/errors`.

- Sort with `sort` (`last_seen`, `first_seen`, `users`, `events`, `unsorted`)
  and `direction`.
- Sorting by `users` answers "what is hurting the most people", which is
  usually the right opening question.
- Paginate by following the `Link` response header. Do not build your own
  paging URLs — the paging style differs between resources. `X-Total-Count`
  carries the total.
- A `422` here can mean the sorted result set exceeded what the endpoint will
  sort (it references code 60000). Narrow with filters rather than retrying.

## 4. Get the full picture on one error

- `viewErrorOnProject` — `GET /projects/{project_id}/errors/{error_id}` for the
  aggregate: status, severity, assignment, first/last seen, occurrence and user
  counts.
- `viewLatestEventOnError` — `GET /errors/{error_id}/latest_event` for the most
  recent occurrence with stacktrace, breadcrumbs, user, device and app context.
- `listEventsOnError` — `GET /projects/{project_id}/errors/{error_id}/events`
  when you need a spread of occurrences rather than the latest one.

Pass the same filters you used in step 3 so the detail matches the list.

## 5. Act on it

`updateErrorOnProject` — `PATCH /projects/{project_id}/errors/{error_id}`.

`operation` is one of `override_severity`, `assign`, `create_issue`,
`link_issue`, `unlink_issue`, `open`, `snooze`, `fix`, `ignore`, `delete`,
`discard`, `undiscard`.

`createCommentOnError` — `POST /projects/{project_id}/errors/{error_id}/comments`
leaves a note for the team. `message` is required or you get `422`.

### Rules before you write

- **There is no idempotency key.** A retried `PATCH` or comment `POST` can
  double-apply. Read the current status first; do not blind-retry a write that
  timed out.
- **`discard` is reversible, `delete` is not.** `undiscard` restores a discarded
  error. `delete` (and `deleteAllErrorsInProject`) has no documented restore
  path or retention window. Never call a delete operation on a user's behalf
  without explicit confirmation naming the error.
- **No dry run exists.** There is no preview or validate-only mode.

## Errors you will actually hit

| Status | Meaning | Do |
|---|---|---|
| 400 | Bad filters or malformed request | Re-read `listProjectEventFields` |
| 401 | Missing or wrong auth token | Check `Authorization: token <...>` |
| 403 | Needs org admin, or the plan lacks the feature | Stop; escalate |
| 404 | Wrong `project_id` / `error_id` | Re-resolve the id |
| 422 | Missing field, or result set too large to sort | Fix payload / add filters |
| 429 | Rate limited | Sleep `Retry-After` seconds |

Rate limits run on a 1-minute window. Successful responses carry
`X-RateLimit-Limit` and `X-RateLimit-Remaining` — read the ceiling from there,
because the number is not published. Note that `429` is **not** declared in the
OpenAPI, so handle it even though the spec does not mention it.
