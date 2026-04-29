---
title: Secrets management roles
description: Secrets management adds these roles.Assign non-admin secrets roles to other users. Secrets administrators have the same privileges as secrets manager and viewer.Grant this role to users who must be able to perform any of the following functions.Grant this role to users who must be able to view secret and secret group records.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Secrets management dashboard, Secrets Management, Platform Security]
---

# Secrets management roles

Secrets management adds these roles.

**Parent Topic:**[Secrets management dashboard](../concept/secrets-dashboard.md)

## Secrets administrator \[sn\_secrets.admin\]

Assign non-admin secrets roles to other users. Secrets administrators have the same privileges as secrets manager and viewer.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

-   A user must have both the admin and security\_admin roles to be assigned the sn\_secret.admin role.
-   Avoid granting an admin role when more targeted roles are available.

## Secrets manager \[sn\_secrets.secret\_manager\]

Grant this role to users who must be able to perform any of the following functions.

-   View secret and secret group records
-   View access history, and other usage activity info
-   Create secret groups and filters
-   Create secret providers
-   Move secrets across secret groups
-   Change secret group and secret provider settings

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Secrets managers can’t see secrets in plain text.

## Secrets viewer \[sn\_secrets.viewer\]

Grant this role to users who must be able to view secret and secret group records.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

