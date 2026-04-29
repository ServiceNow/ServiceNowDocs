---
title: Components installed with Task Mining
description: Several types of components are installed with the Task Mining application, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Task Mining, Platform Analytics]
---

# Components installed with Task Mining

Several types of components are installed with the Task Mining application, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_klq_vrc_kcc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Task Mining admin

 \[sn\_tm\_core.admin\]

</td><td>

Access all Task Mining system configurations and settings. The admin role contains the power user role.

</td><td>

\[sn\_tm\_core.power\_user\]

</td></tr><tr><td>

Task Mining power user

 \[sn\_tm\_core.power\_user\]

</td><td>

Access all Task Mining system configurations and settings. The power user role contains the analyst role.

</td><td>

\[sn\_tm\_core.analyst\]

</td></tr><tr><td>

Task Mining analyst

 \[sn\_tm\_core.analyst\]

</td><td>

Create and share Task Mining projects, and access projects that another user has shared with them. Request data logging to be enabled for workstation users.

</td><td>

-   \[canvas\_user\]
-   \[workspace\_user\]

</td></tr></tbody>
</table>## Tables installed

<table id="table_olq_vrc_kcc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task Dashboard

 \[sn\_tm\_core\_dashboard\]

</td><td>

Dashboard template configurations and displayed information.

</td></tr><tr><td>

Permission

 \[sn\_tm\_core\_permission\]

</td><td>

Information about a project's permissions that are applied to users, user groups, roles, or domains.

</td></tr><tr><td>

User Information

 \[sn\_tm\_core\_user\_data\]

</td><td>

Activities collected from workstations that are linked to the workstation user. Created from data logs aggregated by application name, screen name, and URL.

</td></tr><tr><td>

Task Definition

 \[sn\_tm\_core\_task\_definition\]

</td><td>

Definitions of tasks with start and end points.

</td></tr><tr><td>

Event Filter

 \[sn\_tm\_core\_event\_filter\]

</td><td>

List of combinations of event, application name, window name, and window class name filtered by the agent. These combinations can be either excluded so the events aren’t stored or replaced so targeted events are replaced as a block-listed application.

</td></tr><tr><td>

Object Attribute

 \[sn\_tm\_core\_object\_attribute\]

</td><td>

Replaceable event filter object attributes that can't be modified.

</td></tr><tr><td>

Project user data

 \[sn\_tm\_core\_project\_user\_data\]

</td><td>

Categorized workstation user activity connected with projects.

</td></tr><tr><td>

Task Instance

 \[sn\_tm\_core\_task\_instance\]

</td><td>

Task records with timestamps.

</td></tr><tr><td>

Task segment percentage

 \[sn\_tm\_core\_task\_segment\_percentage\]

</td><td>

Task segment measurement used in data mining.

</td></tr><tr><td>

User task data

 \[sn\_tm\_core\_user\_task\_data\]

</td><td>

Workstation data combined with task instance data used in the data mining process.

</td></tr><tr><td>

Application

 \[sn\_tm\_core\_application\]

</td><td>

Categories for Task Mining applications.

</td></tr><tr><td>

Task Mining User Information

 \[sn\_tm\_core\_user\]

</td><td>

Contains the following information for active or inactive workstation users listed on workstation data log requests and whether the agent is requested, installed, or uninstalled.

</td></tr><tr><td>

Event Translation

 \[sn\_tm\_core\_event\_translation\]

</td><td>

Translation of events to simple language shown in the UI that can't be modified.

</td></tr><tr><td>

Task Mining Project

 \[sn\_tm\_core\_project\]

</td><td>

Projects created by the Task Mining analyst.

</td></tr><tr><td>

Application Category

 \[sn\_tm\_core\_application\_category\]

</td><td>

Existing records for Task Mining application categories.

</td></tr><tr><td>

Task Mining Configuration

 \[sn\_tm\_core\_configuration\]

</td><td>

Configurable parameters in the application.

</td></tr><tr><td>

Project User Anonymization

 \[sn\_tm\_core\_project\_user\_anonymization\]

</td><td>

All user aliases with references to related project and workstation users.

</td></tr><tr><td>

Project Mining Job History

 \[sn\_tm\_core\_project\_mining\_job\]

</td><td>

Information about project mining jobs, including mining and datamart deletion.

</td></tr><tr><td>

Activity Categorization Rule

 \[sn\_tm\_core\_activity\_categorization\_rule\]

</td><td>

All activity categorization rules. The table is prepopulated with default fixed rules and user-created rules are then added.

</td></tr></tbody>
</table>**Parent Topic:**[Task Mining Reference](../concept/reference-task-mining.md)

