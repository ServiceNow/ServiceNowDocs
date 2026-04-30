---
title: Components installed with SPW Jira Integrations
description: Learn about the roles and tables installed with the SPW Jira Integrations application.
locale: en-US
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2025-12-05"
reading_time_minutes: 1
breadcrumb: [Reference, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Components installed with SPW Jira Integrations

Learn about the roles and tables installed with the SPW Jira Integrations application.

## Roles installed

<table id="table_jkd_xbl_nhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Jira integration admin\[sn\_jira\_int.admin\]

</td><td>

Has complete access to the SPW Jira Integrations application

</td><td>

-   sn\_int\_common.admin
-   sn\_jira\_int.user

</td></tr><tr><td>

Jira integration user\[sn\_jira\_int.user\]

</td><td>

-   Sets up integration between Jira and Strategic Planning
-   Can create new or update the existing map configurations between Jira and Strategic Planning

</td><td>

-   connection\_admin
-   sn\_int\_common.user
-   credential\_admin

</td></tr></tbody>
</table>## Tables installed

<table id="table_nkd_xbl_nhc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choice Map\[sn\_int\_common\_choice\_map\]

</td><td>

Stores the list of workflow state mapping for Jira projects.

</td></tr><tr><td>

Event Type \[sn\_int\_common\_input\_event\_type\]

</td><td>

Stores information of the type of webhook events such as create, update, or delete of a work item.

</td></tr><tr><td>

External Identifiers \[sn\_int\_common\_external\_identifiers\]

</td><td>

Stores the list of all Jira reference identifiers such as External ID, External Key, External Project, External URL, and so on.

</td></tr><tr><td>

External Project\[sn\_int\_common\_project\]

</td><td>

Stores information of the Jira project such as project ID, the Jira instance of this project, project name, and so on.

</td></tr><tr><td>

External system\[sn\_int\_common\_external\_system\]

</td><td>

Stores information of Jira application used for the integration.

</td></tr><tr><td>

External System Version\[sn\_int\_common\_external\_system\_version\]

</td><td>

Stores version information of Jira application used for the integration.

</td></tr><tr><td>

Field Map\[sn\_int\_common\_field\_map\]

</td><td>

Stores the list of field mapping of different issue types for Jira projects.

</td></tr><tr><td>

Jira Board\[sn\_jira\_int\_board\]

</td><td>

Stores the list of imported boards from Jira.

</td></tr><tr><td>

Jira Import Request\[sn\_jira\_int\_import\_request\]

</td><td>

Stores the list of all import requests created to import projects, boards, and project style mappings from Jira.

</td></tr><tr><td>

Jira Instance\[sn\_jira\_int\_instance\]

</td><td>

Stores the list of all Jira instances.

</td></tr><tr><td>

Jira Project\[sn\_jira\_int\_project\]

</td><td>

Stores the list of all imported projects from Jira.

</td></tr><tr><td>

Team Integration Settings\[sn\_agile\_jira\_int\_import\_settings\]

</td><td>

Stores the list of one-to-one relation between a Jira project, board, and an EAP Team.

</td></tr><tr><td>

Project Style Mapping\[sn\_jira\_int\_prj\_style\_mapping\]

</td><td>

Store the list of map configuration templates per Jira project style.

</td></tr><tr><td>

Table Map\[sn\_int\_common\_table\_map\]

</td><td>

Stores the list of table maps for Jira projects.

</td></tr></tbody>
</table>**Parent Topic:**[SPW Jira Integrations reference](spw-jira-integrations-reference.md)

