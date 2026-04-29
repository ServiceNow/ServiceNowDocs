---
title: Multi-factor Authentication criteria
description: Use MFA criteria to determine which users and roles must use two-step verification.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor Authentication criteria

Use MFA criteria to determine which users and roles must use two-step verification.

## Multi-factor criteria

Use MFA criteria to determine which users and roles must use two-step verification. You can use one of these criteria or a combination of them to suit your business needs. You can use one of these criteria or a combination of them to suit your business needs.

**Note:** It is recommended to use Adaptive Authentication policy based MFA.

-   **User-based multi-factor criteria**

    Use user-based multi-factor criteria to select individual users who are required to log in using MFA. Administrators update the **Enable Multifactor Authentication** field on a user record to enable or disable MFA requirements for a user. For details on this process, see [Configure user-based multi-factor criteria](../task/t_RequireMultifactorAuthForAUser.md).

-   **Role-based multi-factor criteria**

    Use role-based multi-factor criteria to require MFA login for all users assigned to a specific role. The **Role-based multi-factor authentication** record on the **Multi-factor Criteria** \[multi\_factor\_criteria\] table contains the list of roles that require an MFA login. For details on maintaining this list, see [Configure role-based multi-factor criteria](../task/mfa-role-criteria.md).

-   **Adaptive authentication policy-based multi-factor criteria**

    Use adaptive authentication to determine when your instance requires MFA. Adaptive authentication uses authentication policies to evaluate criteria like a user's IP address or user groups. For details on the adaptive authentication feature, see [Adaptive authentication](adaptive-authentication.md).


