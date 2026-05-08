---
title: Components installed with Microsoft Azure DevOps integration for Agile Development
description: Several types of components are installed with activation of the Microsoft Azure DevOps integration for Agile Development application, including user roles, scheduled jobs, and tables.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Components installed with Microsoft Azure DevOps integration for Agile Development

Several types of components are installed with activation of the Microsoft Azure DevOps integration for Agile Development application, including user roles, scheduled jobs, and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Azure DevOps integration admin\[sn\_ado\_int.admin\]

</td><td>

Has complete access to the application

</td><td>

-   sn\_int\_common.admin
-   sn\_ado\_int.user

</td></tr><tr><td>

Azure DevOps integration user\[sn\_ado\_int.user\]

</td><td>

-   Sets up integration between Azure DevOps and Agile Development
-   Can create new or update the existing map configurations between Azure DevOps and Agile Development

</td><td>

-   connection\_admin
-   sn\_int\_common.user
-   credential\_admin

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Discover Azure Project Job|Discovers new Azure DevOps projects at a scheduled time and imports them automatically.|
|Import Azure DevOps Teams Areas and Iterations|Imports teams, areas, and iterations from Azure DevOps automatically at a scheduled time.|
|Import Azure DevOps Work Items|Imports work items from Azure DevOps automatically at a scheduled time.|

All the scheduled jobs are inactive by default. For more information, see [Schedule jobs to import projects, teams, areas, and work items from Azure DevOps](schedule-jobs-import-projects-azure.md).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Area Team M2M\[sn\_ado\_int\_m2m\_area\_team\]

</td><td>

Stores the relationship between teams and areas.

</td></tr><tr><td>

Attachment Map\[sn\_int\_common\_attachment\_map\]

</td><td>

Stores the mapping of attachments to issues between Azure DevOps and Agile Development.

</td></tr><tr><td>

Azure DevOps Area\[sn\_ado\_int\_area\]

</td><td>

Stores the list of imported areas from Azure DevOps.

</td></tr><tr><td>

Azure DevOps Import Request\[sn\_ado\_int\_import\_request\]

</td><td>

Stores the list of all import requests created to import projects and process mappings from Azure DevOps.

</td></tr><tr><td>

Azure DevOps Instance\[sn\_ado\_int\_instance\]

</td><td>

Stores the list of all Azure DevOps instances.

</td></tr><tr><td>

Azure DevOps Iteration\[sn\_ado\_int\_iteration\]

</td><td>

Stores the list of imported iterations from Azure DevOps.

</td></tr><tr><td>

Azure DevOps project\[sn\_ado\_int\_project\]

</td><td>

Stores the list of imported projects from Azure DevOps.

</td></tr><tr><td>

Azure DevOps Subscriptions\[sn\_ado\_int\_subscription\]

</td><td>

Stores the subscription IDs of the event type for the webhooks registered in Azure.

</td></tr><tr><td>

Azure DevOps Team\[sn\_ado\_int\_team\]

</td><td>

Stores the list of imported Azure DevOps teams.

</td></tr><tr><td>

Choice Map\[sn\_int\_common\_choice\_map\]

</td><td>

Stores the list of workflow state mapping for Azure DevOps projects.

</td></tr><tr><td>

Event Type\[sn\_int\_common\_input\_event\_type\]

</td><td>

Stores information of the type of webhook events such as creating, updating, or deleting a work item.

</td></tr><tr><td>

External Identifiers\[sn\_int\_common\_external\_identifiers\]

</td><td>

Stores the list of all Azure DevOps reference identifiers such as External ID, External Key, External Project, External URL, and so on.

</td></tr><tr><td>

External Project\[sn\_int\_common\_project\]

</td><td>

Stores information of the Azure DevOps project such as project ID, the Azure DevOps instance of this project, project name, and so on.

</td></tr><tr><td>

External System\[sn\_int\_common\_external\_system\]

</td><td>

Stores information of the Azure DevOps application used for the integration.

</td></tr><tr><td>

External System Version\[sn\_int\_common\_external\_system\_version\]

</td><td>

Stores the API version information of the Azure DevOps application used for the integration.

</td></tr><tr><td>

Field Map\[sn\_int\_common\_field\_map\]

</td><td>

Stores the list of field mapping of different work items for Azure DevOps projects.

</td></tr><tr><td>

Process Mapping\[sn\_ado\_int\_process\_mapping\]

</td><td>

Stores the list of map configuration templates per Azure DevOps process.

</td></tr><tr><td>

Table Map\[sn\_int\_common\_table\_map\]

</td><td>

Stores the list of table maps for Azure DevOps projects.

</td></tr><tr><td>

Team Integration Settings\[sn\_agile\_ado\_int\_import\_settings\]

</td><td>

Stores the list of one-to-one relation between Azure DevOps project, team, and an Agile assignment group.

</td></tr><tr><td>

Webhook Registry\[sn\_int\_common\_webhook\_registry\]

</td><td>

Stores details of the registry callback path for webhooks registered in Azure DevOps to receive event updates.

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft Azure DevOps Integration for Agile Development](../concept/agile-azure-integration-overview.md)

