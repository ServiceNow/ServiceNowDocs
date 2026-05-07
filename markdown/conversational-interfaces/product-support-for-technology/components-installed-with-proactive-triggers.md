---
title: Components installed with the Proactive Triggers feature
description: When the Proactive Triggers feature is installed, the feature includes required components, such as specific roles and tables. Admins can review these roles and tables to make sure that the feature has been installed correctly.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Proactive Triggers reference, Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Components installed with the Proactive Triggers feature

When the Proactive Triggers feature is installed, the feature includes required components, such as specific roles and tables. Admins can review these roles and tables to make sure that the feature has been installed correctly.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles installed with the Proactive Triggers feature

<table id="table_c4v_bxz_dwb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Proactive\_admin \[sn\_pt.proactive\_admin\]

</td><td>

Allows users to create proactive rules and have access to related tables and related records

</td><td>

-   user\_criteria\_admin
-   sp\_admin

</td></tr></tbody>
</table>## Tables installed with the Proactive Triggers feature

|Table|Description|
|-----|-----------|
|Proactive Custom Trigger Types \[sys\_cs\_ptrigger\_trigger\_type\_list\]|Create and view custom trigger types|
|Proactive Rules \[sys\_cs\_ptrigger\_rule\]|Stores all Proactive Triggers rules|
|Proactive Actions \[sys\_cs\_ptrigger\_action\]|Parent action table|
|Proactive Virtual Agent Topic Action\[sys\_cs\_ptrigger\_va\_topic\_action\] |Extended table from action for Virtual Agent action|
|Proactive Execution History  \[sys\_cs\_ptrigger\_execution\]|Execution history for the last 7 days|
|Proactive Daily Report \[sys\_cs\_ptrigger\_report\_daily\]|Aggregated execution data by user, rule, or action per day|

-   **[Proactive Triggers roles](../reference/PT-roles.md#)**  
Proactive Triggers adds the Proactive Triggers admin role.

**Parent Topic:**[Proactive Triggers reference](../reference/proactive-triggers-reference.md)

