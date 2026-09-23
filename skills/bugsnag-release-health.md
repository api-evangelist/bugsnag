---
name: bugsnag-release-health
description: >-
  Answer "is this release healthy?" — read stability scores across releases and
  builds, compare a new release against its predecessors, and correlate a drop
  with the errors introduced in it. Use when asked whether to roll back, whether
  a deploy regressed, or how a version is performing.
api: bugsnag:bugsnag-data-access-api
base_url: https://api.bugsnag.com
operations:
  - listProjectReleaseGroups
  - getReleaseGroup
  - listReleaseGroupReleases
  - listProjectReleases
  - getProjectReleaseById
  - getProjectStabilityTrend
  - listProjectErrors
  - viewErrorOnProject
---

# Assess BugSnag release health

`https://api.bugsnag.com`, `Authorization: token <PERSONAL_AUTH_TOKEN>`,
`X-Version: 2`.

## Get the vocabulary right first

BugSnag's two release concepts are easy to swap, and swapping them produces a
confidently wrong answer:

- **Release group** (`/release_groups/{id}`) — an app version across all of its
  builds. This is what the BugSnag MCP server calls a "release", and it is what
  carries the headline stability score.
- **Release** (`/projects/{project_id}/releases/{release_id}`) — a single build,
  with its own source-control metadata. This is what the MCP server calls a
  "build", and what the BugSnag CLI's `create-build` command creates.

## 1. List what shipped

`listProjectReleaseGroups` — `GET /projects/{project_id}/release_groups`.
Filter by release stage; `production` is the default worth asking about first.

Follow the `Link` header to page.

## 2. Read one version in depth

- `getReleaseGroup` — `GET /release_groups/{id}` for the aggregate stability.
- `listReleaseGroupReleases` — `GET /release_groups/{release_group_id}/releases`
  for the individual builds inside it.
- `getProjectReleaseById` — `GET /projects/{project_id}/releases/{release_id}`
  for one build's source-control info and metadata.

Stability is expressed as crash-free sessions and crash-free users. A version
with a good session score and a poor user score is hitting a small group hard.

## 3. Put it on a curve

`getProjectStabilityTrend` — `GET /projects/{project_id}/stability_trend`.

A single release's score means little without the project's baseline. Compare
against the preceding releases before calling anything a regression.

## 4. Explain the drop

`listProjectErrors` with an errors-introduced filter scoped to the release
stage, then `viewErrorOnProject` on the top offenders. The 2026-03 release notes
added release-stage matching to the errors-introduced filter, so you can ask for
errors new to `production` specifically rather than new anywhere.

## Reporting rules

- Say which release **stage** every number came from. A staging score is not a
  production score.
- Quote crash-free **sessions** and crash-free **users** separately.
- If the stability trend has fewer data points than the comparison needs, say
  so rather than comparing two points and calling it a trend.
- All operations in this skill are reads. Nothing here needs a write, an
  approval, or a rollback plan.
