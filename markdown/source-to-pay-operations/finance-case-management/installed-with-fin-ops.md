---
title: Components installed with Finance Case Management
description: Several types of components are installed with the activation of the Finance Case Management plugin, including roles, flows, and tables.
locale: en-US
release: australia
product: Finance Case Management
classification: finance-case-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Finance Case Management, Configure, Finance Case Management, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Components installed with Finance Case Management

Several types of components are installed with the activation of the Finance Case Management plugin, including roles, flows, and tables.

## Roles installed

The following roles are installed with Finance Case Management:

<table id="table_n2y_by1_q2c"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_fin\_ops.admin

</td><td>

Can access all the features and capabilities of Finance Case Management, including Finance Operations workspace

</td><td>

-   sla\_admin
-   sn\_fin\_ops.specialist

</td></tr><tr><td>

sn\_fin\_ops.requester

</td><td>

Can create finance-related cases

</td><td>

 

</td></tr><tr><td>

sn\_fin\_ops.specialist

</td><td>

Can view and update the finance-related cases

</td><td>

-   sn\_fin\_ops.requester
-   workspace\_user
-   canvas user
-   email\_composer

</td></tr><tr><td>

sn\_fin\_ops.task\_owner

</td><td>

Can view and update the tasks associated with the finance case

</td><td>

 

</td></tr></tbody>
</table>## Tables installed

No new tables are installed with Finance Case Management. However, the labels of the following tables are changed:

|Table|New label|Description|
|-----|---------|-----------|
|sn\_spend\_sdc\_service\_request|Finance case|Stores the finance cases|
|sn\_spend\_sdc\_service\_request\_line|Finance case lines|Represents individual items or components related to the finance case|
|sn\_spend\_sdc\_service\_task|Finance task|Stores the finance tasks|

-   **[Application plugin installation sequence in Finance Case Management](app-plugin-install-seq-fin-ops.md)**  
View the consolidated list of plugins, high-level description of each plugin, and the dependencies that are required before installing each plugin in Finance Case Management.
-   **[Activate the Create Finance Inquiry for inbound email flow](../task/activate-fin-case-inquiry-flow.md)**  
Activate the **Create Finance case on Inbound email inquiry** flow to create a finance inquiry case automatically based on the information in an inbound email.

**Parent Topic:**[Install Finance Case Management](../task/install-fin-case-mgmt.md)

