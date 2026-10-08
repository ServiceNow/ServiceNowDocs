---
title: Role requirements for Unified Secrets Gateway
description: Learn about the roles required to configure Unified Secrets Gateway \(USG\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/usg-roles.html
release: brazil
topic_type: reference
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [unified secrets gateway, roles, permissions, cryptographic manager]
breadcrumb: [Configuring Unified Secrets Gateway, Unified Secrets Gateway, Encryption]
---

# Role requirements for Unified Secrets Gateway

Learn about the roles required to configure Unified Secrets Gateway \(USG\).

## Required roles

Managing Unified Secrets Gateway requires the following roles. Since USG is based on the Key Management Framework, there are roles common to both.

-   Admin
-   sn\_kmf.cryptographic\_manager

For complete details on roles, see [Roles installed with Key Management Framework](https://www.servicenow.com/docs/r/oL66E_cwDD_tnWQYzYPRdA/myGk4UCF~sLwalD0AjDxdA?section=kmf-roles).

## Admin or KMF Cryptographic Manager

Users with the Admin or KMF Cryptographic Manager role can create and update alias groups, identity groups, and consumer grants. Admins and KMF cryptographic managers can also create and add members to identity groups.

## Assign a role to a user

Use the following procedure to assign the KMF Cryptographic Manager role to a user.

1.  Navigate to **All** &gt; **System Security** &gt; **Users**.
2.  Select a user that needs to configure USG.
3.  In the **Roles** related list, select **Edit**.
4.  Search for sn\_kmf.cryptographic\_manager and add the role to the selected user.
5.  Select **Save**.

**Parent Topic:**[Configuring Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-configuring.md)

