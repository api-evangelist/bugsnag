---
name: bugsnag-provision-collaborators-scim
description: >-
  Provision and deprovision BugSnag collaborators and teams over SCIM 2.0, or
  over the native collaborator/team operations. Use when asked to add or remove
  users, sync an identity provider, audit who has access, or manage team project
  access.
api: bugsnag:bugsnag-data-access-api
base_url: https://api.bugsnag.com
operations:
  - listScimCollaborators
  - createScimCollaborator
  - getScimCollaborator
  - updateScimCollaborator
  - patchScimCollaborator
  - deleteScimCollaborator
  - listScimGroups
  - createScimGroup
  - updateScimGroup
  - deleteScimGroup
  - listOrganizationCollaborators
  - inviteOrganizationCollaborator
  - deleteOrganizationCollaborator
  - listOrganizationTeams
  - listOrganizationTeamProjectAccesses
---

# Provision BugSnag access

`https://api.bugsnag.com`, `Authorization: token <PERSONAL_AUTH_TOKEN>`,
`X-Version: 2`. Most of these operations require **organization admin** rights;
a non-admin token gets `403`, not `401`.

## Two doors to the same room

BugSnag exposes identity twice, and they manage the same underlying objects:

| Concern | SCIM 2.0 | Native |
|---|---|---|
| User | `/organizations/{organization_id}/scim/v2/Users` | `/organizations/{organization_id}/collaborators` |
| Group | `/organizations/{organization_id}/scim/v2/Groups` | `/organizations/{organization_id}/teams` |

Use **SCIM** when you are syncing an identity provider (Okta, Entra ID,
OneLogin) — it is the standard shape those tools already speak, and BugSnag
implements list, create, get, replace, PATCH and delete for both Users and
Groups, with RFC 7644 PatchOp semantics. Automatic user provisioning via SSO is
a Preferred-tier feature.

Use the **native** operations for BugSnag-specific work SCIM has no vocabulary
for: bulk invitations (`bulkInviteOrganizationCollaborators`), per-project
access grants (`listOrganizationTeamProjectAccesses`,
`updateOrganizationTeamProjectAccesses`), and suggested collaborators/teams.

**Do not mix the two doors inside one workflow.** Pick the one that matches the
source of truth for that tenant and stay in it, or you will produce drift that
neither side reports.

## Audit before you change

1. `listOrganizationCollaborators` — who has access.
2. `getOrganizationCollaboratorProjectAccessCounts` — how broad each person's
   access is.
3. `listOrganizationTeams` then `listOrganizationTeamProjectAccesses` — what a
   team grants.

## Write rules

- **No idempotency key.** A retried create can produce a duplicate invitation.
  List first, then create only what is missing.
- Removing a collaborator or group is reversible only by re-inviting or
  re-creating; there is no restore and no documented retention window.
- `revokeOrganizationAuthToken` and `revokeOrganizationApiKey` are
  **irreversible** — the old credential cannot be restored, and every client
  using it breaks immediately. Never call these without an explicit, specific
  instruction.
- `403 Insufficient organization feature` means the plan tier does not include
  the capability (SAML SSO is Select-tier and up, automatic SSO provisioning is
  Preferred-tier and up). That is a billing answer, not a permissions bug.

## Reporting rules

State which door you used (SCIM or native) in every summary, and list exactly
which principals changed. An access change the requester cannot audit is worse
than no change.
