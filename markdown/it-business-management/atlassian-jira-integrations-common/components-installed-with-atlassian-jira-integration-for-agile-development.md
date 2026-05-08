---
title: Components installed with Atlassian Jira integration for Agile Development
description: Several types of components are installed with activation of the Atlassian Jira integration for Agile Development application, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Atlassian Jira Integration for Agile Development, Strategic Portfolio Management]
---

# Components installed with Atlassian Jira integration for Agile Development

Several types of components are installed with activation of the Atlassian Jira integration for Agile Development application, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Jira integration admin\[sn\_jira\_int.admin\]

</td><td>

Has complete access to the application

</td><td>

-   sn\_int\_common.admin
-   sn\_jira\_int.user

</td></tr><tr><td>

Jira integration user\[sn\_jira\_int.user\]

</td><td>

-   Sets up integration between Jira and Agile Development
-   Can create new or update the existing map configurations between Jira and Agile Development

</td><td>

-   connection\_admin
-   sn\_int\_common.user
-   credential\_admin

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import Jira Issue

</td><td>

Imports issues and sprints from Jira automatically at a scheduled time.This job is inactive by default.

 For more information, see [Schedule a job to auto-import issues from Jira to Agile Development 2.0](schedule-jobs-to-import-issue-from-jira.md).

</td></tr></tbody>
</table>## Tables installed

<table id="table_tg5_hck_hmb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attachment Map\[sn\_int\_common\_attachment\_map\]

</td><td>

Stores the mapping of attachments to issues between Jira and Agile Development.

</td></tr><tr><td>

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

Project Integration Settings\[sn\_agile\_jira\_int\_import\_settings\]

</td><td>

Stores the list of one-to-one relation between a Jira project, board, and an Agile assignment group.

</td></tr><tr><td>

Project Style Mapping\[sn\_jira\_int\_prj\_style\_mapping\]

</td><td>

Store the list of map configuration templates per Jira project style.

</td></tr><tr><td>

Table Map\[sn\_int\_common\_table\_map\]

</td><td>

Stores the list of table maps for Jira projects.

</td></tr><tr><td>

Webhook Registry\[sn\_int\_common\_webhook\_registry\]

</td><td>

Stores details of the registry callback path for webhooks registered in Jira to receive event updates.

</td></tr></tbody>
</table>**Parent Topic:**[Atlassian Jira Integration for Agile Development](../concept/agile-jira-integration-overview.md)

