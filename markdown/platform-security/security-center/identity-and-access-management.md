---
title: Access Management
description: Use the tools in the Access Management section verify that your data is only accessible to the users and processes that need it.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Center, Platform Security]
---

# Access Management

Use the tools in the Access Management section verify that your data is only accessible to the users and processes that need it.

![Identity and Access Management in Security Center](../images/iam1.png)

IAM consists of three tools you can use to manage access to the data on your instance. You can also select **Go to Console** to view these and other tools within the [Access management console](../../contextual-security/concept/access-management-console.md).

-   **[Access findings](../../contextual-security/concept/access-findings.md)**

    Access findings feature displays the potential vulnerabilities that are discovered the last time access checks were ran on your ServiceNow AI Platform.

-   **[Access Analyzer](../../../integrate/identity/concept/access-analyzer.md)**

    Use the **Analyze Access and Permissions** console to view permissions for a selected user, role, group, or compare access between two users.

-   **[Scripting Governance for default group](../../security/concept/scripting-governance.md)**

    Use the Scripting Governance Tool to configure preferences for the Conditional Script Writer group. Users in this group are assigned the **snc\_required\_script\_writer\_permission** role, which allows users to access scripts and script-like fields across the platform.

    With the settings on this console you can turn auto-assignment of this role on or off, as well manually assign users to the group. You can also see information on who is assigned, and scan your instance to find users who have scripted in a specific time frame.


**Parent Topic:**[Security Center](sec-center-v2.md)

