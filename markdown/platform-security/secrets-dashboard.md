---
title: Secrets management dashboard
description: Use the secrets management dashboard to review the secret groups configured on your instance, and learn about any security issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Secrets Management, Platform Security]
---

# Secrets management dashboard

Use the secrets management dashboard to review the secret groups configured on your instance, and learn about any security issues.

## Secret Group Overview

![Secrets management dashboard](../images/sm_dash.png)

The **Secret Group Overview** tab displays information about your configured secret groups. Use this tab to see information about the secrets groups configured on your instance.

-   **Secret Group by Type**

    Displays a pie chart showing secret groups installed on your instance, grouped by secret type \(instance side of client side\).

-   **Secret Group by Criterion Type**

    Displays a pie chart showing secret groups with criteria configured on your instance by the type of criteria used.

-   **Number of Inactive Secrets Groups**

    Displays a count of the inactive secret groups configured on your instance.

-   **Number of Dedicated Secrets**

    Displays a count of secrets within basic secret groups.


## Secret Group Warnings

![Secrets management dashboard](../images/sm_dash_2.png)

The **Secret Group Warnings** tab displays warnings related to your secret groups and identity groups.

-   **Instance Accessible Secret Groups - Warnings**

    This card displays warnings if there are secret groups with no active access policies in place. Select a secret group name to view that record.

-   **Client Accessible Secret Groups - Warnings**

    This card displays warnings if there are client accessible secret groups that don’t have an active identity module access policy \(MAP\). Select a secret group name to view that record.

-   **Identity Groups - Warnings**

    This card displays warnings if there are identity groups that don’t have group members configured. Select the identity group name to view the record.


**Note:** The Secrets Management Dashboard is a part of Secrets Management Enterprise. Secrets Management Enterprise is a paid plugin that ServiceNow personnel must activate on your production instance.

-   **[Secrets management roles](../reference/roles-sec-man.md#)**  
Secrets management adds these roles.
-   **[Create a secret group cryptographic module](../task/create-sm-crypto-module.md)**  
Create a secret group cryptographic module to perform encryption and decryption.
-   **[Create a basic secret group](../task/sm-create-basic-group.md)**  
Create a basic secret group to group any secrets, regardless of their criteria.
-   **[Create a secret group with criteria](../task/sm-create-criteria-group.md)**  
Create a secret group with criteria to organize secrets entered in Password2 fields automatically when they share a common criteria, such as table, scope, or application.
-   **[Upload a public key for Secrets Management](../task/sm-upload-key.md)**  
Upload a public key for to encrypt your secrets.
-   **[Run secrets management security jobs](../task/sm-security-jobs.md)**  
Schedule a secrets management job to perform encryption tasks on secrets fields on your instance.

**Parent Topic:**[Secrets Management](secrets-management.md)

