---
title: Multi-factor authentication criteria
description: Use multi-factor criteria to determine which users and roles must use two-step multi-factor verification.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Multi-factor authentication, Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor authentication criteria

Use multi-factor criteria to determine which users and roles must use two-step multi-factor verification.

## Multi-factor criteria

Use multi-factor criteria to determine which users and roles must use two-step multi-factor verification. You can use one of these criteria or a combination of them to suit your business needs. You can use one of these criteria or a combination of them to suit your business needs.

**Note:** It is recommended to use Adaptive Authentication policy based MFA.

-   **User-based multi-factor criteria**

    Use user-based multi-factor criteria to select individual users who are required to log in using MFA. Administrators update the **Enable Multifactor Authentication** field on a user record to enable or disable MFA requirements for a user. For details on this process, see [Configure user-based multi-factor criteria](../task/t_RequireMultifactorAuthForAUser.md).

-   **Role-based multi-factor criteria**

    Use role-based multi-factor criteria to require MFA login for all users assigned to a specific role. The **Role-based multi-factor authentication** record on the **Multi-factor Criteria** \[multi\_factor\_criteria\] table contains the list of roles that require an MFA login. For details on maintaining this list, see [Configure role-based multi-factor criteria](../task/mfa-role-criteria.md).

-   **Adaptive authentication policy-based multi-factor criteria**

    Use adaptive authentication to determine when your instance requires MFA. Adaptive authentication uses authentication policies to evaluate criteria like a user's IP address or user groups. For details on the adaptive authentication feature, see [Adaptive authentication](adaptive-authentication.md).


