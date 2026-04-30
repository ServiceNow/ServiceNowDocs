---
title: Identity and Access Management
description: Use the tools in the Identity and Access Management \(IAM\) section verify that your data is only accessible to the users and processes that need it.
locale: en-US
release: zurich
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Center, Platform Security]
---

# Identity and Access Management

Use the tools in the Identity and Access Management \(IAM\) section verify that your data is only accessible to the users and processes that need it.

![Identity and Access Management in Security Center](../images/iam1.png)

IAM consists of three tools you can use to manage access to the data on your instance.

-   **[Machine Identity Management](../../../integrate/machine-identity/concept/machine-identity-console.md)**

    Machine identities are digital credentials such as certificates, keys, and tokens. Servers, applications, containers, and cloud services use these identities authenticate with each other. Use the **Machine Identity Console** to manage the machine identities used for integrations with ServiceNow.

-   **[Access analyzer](../../../integrate/identity/concept/access-analyzer.md)**

    Use the **Analyze Access and Permissions** console to view permissions for a selected user, role, group, or compare access between two users.

-   **Scripting Governance for default group**

    Use the Scripting Governance Tool to configure preferences for the Conditional Script Writer group. Users in this group are assigned the **snc\_required\_script\_writer\_permission** role, which allows users to access scripts and script-like fields across the platform.

    With the settings on this console you can turn auto-assignment of this role on or off, as well manually assign users to the group. You can also see information on who is assigned, and scan your instance to find users who have scripted in a specific time frame.


**Parent Topic:**[Security Center](sec-center-v2.md)

