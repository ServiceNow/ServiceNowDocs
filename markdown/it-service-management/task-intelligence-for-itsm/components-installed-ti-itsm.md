---
title: Components installed with Task Intelligence for ITSM
description: Several types of components are installed with the activation of the Task Intelligence for ITSM application plugin \(com.snc.itsm\_ml\_task\), including tables, user roles, and ServiceNow store applications.
locale: en-US
release: zurich
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Task Intelligence for ITSM, IT Service Management]
---

# Components installed with Task Intelligence for ITSM

Several types of components are installed with the activation of the Task Intelligence for ITSM application plugin \(com.snc.itsm\_ml\_task\), including tables, user roles, and ServiceNow store applications.

## Roles installed

<table id="table_cmk_tjf_cyb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Task Intelligence Admin

 \[sn\_itsm\_ml\_task.ti\_admin\]

</td><td>

Admin user with rights to all actions in the application. Creates, edits, and monitors all Task Intelligence models.

</td><td>

-   sn\_incident\_read
-   sn\_ti\_admin.tia\_admin

</td></tr><tr><td>

Task Intelligence Analyst\[sn\_itsm\_ml\_task.ti\_analyst\]

</td><td>

Views and monitors Task Intelligence models through the Analytics dashboard.

</td><td>

-   sn\_incident\_read
-   sn\_ti\_admin.tia\_analyst

</td></tr><tr><td>

Task Intelligence User\[sn\_itsm\_ml\_task.ti\_user\]

</td><td>

View-only access to the ITSM Task Intelligence Monitoring Dashboard. No ability to perform administrative actions, modify configurations, or manage models.

</td><td>

-   sn\_incident\_read
-   sn\_ti\_admin.tia\_user

</td></tr></tbody>
</table>## Tables installed

<table id="table_gmk_tjf_cyb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task Intelligence Admin Template \[sn\_ti\_admin\_template\]

</td><td>

Contains template records, which are inserted by other applications, that specify the defaults for model training settings, implementation plans, and UI display information.

</td></tr><tr><td>

Task Intelligence Admin Help \[sn\_ti\_admin\_help\]

</td><td>

Contains help records that are displayed in a collapsible panel inside the application. Contents are filtered by the chosen template and setup page.

</td></tr><tr><td>

Task Intelligence Admin Feature \[sn\_ti\_admin\_feature\]

</td><td>

High-level business unit feature for incident categorization and incident field detection.

</td></tr><tr><td>

Task Intelligence Admin Statistic \[sn\_ti\_admin\_statistic\]

</td><td>

Groups statistic cards to a template and UI page.

</td></tr><tr><td>

Task Intelligence Admin Page \[sn\_ti\_admin\_page\]

</td><td>

Records of URL page fragments that are referenced in the help table.

</td></tr><tr><td>

Task Intelligence Admin Statistic Card \[sn\_ti\_admin\_statistic\_card\]

</td><td>

Stores the statistic card’s three-line scriptable content and its card description used in a card flip or tooltip.

</td></tr><tr><td>

Task Intelligence Admin Solution \[sn\_ti\_admin\_solution\]

</td><td>

Stores how the state of each ML model set progresses for the solution types, such as incident categorization and classification.

</td></tr><tr><td>

Task Intelligence Admin Model Prediction \[sn\_ti\_admin\_model\_prediction\]

</td><td>

Stores the model test prediction for prebuilt models.

</td></tr><tr><td>

Task Intelligence Admin Tag \[sn\_ti\_admin\_tag\]

</td><td>

Contains the tags provided by other business units and a created solution by an admin. Tags help business unit partners search the models.

</td></tr><tr><td>

Task Intelligence Admin Implementation Detail \[sn\_ti\_admin\_implementation\_detail\]

</td><td>

Contains implementation options specified by business units, which are listed as options for a chosen template. When an Admin Console user role chooses an implementation plan, the business unit decides how to display model results for end users.

</td></tr><tr><td>

Task Intelligence Admin Model \[sn\_ti\_admin\_model\]

</td><td>

Stores the snapshot configuration view of the production and staging models for a solution.

</td></tr><tr><td>

Task Intelligence Admin Context \[sn\_ti\_admin\_context\]

</td><td>

Contains context-specific data from monitoring graphs that show different model performance.

</td></tr><tr><td>

Task Intelligence Admin Application Page \[sn\_ti\_admin\_application\_page\]

</td><td>

Contains data related to the application page, fields, and forms.

</td></tr><tr><td>

Task Intelligence Admin Landing Card \[sn\_ti\_admin\_landing\_card\]

</td><td>

Contains data related to the information cards displayed on the landing page of Task Intelligence for ITSM.

</td></tr><tr><td>

Task Intelligence Admin Landing Page \[sn\_ti\_admin\_landing\_page\]

</td><td>

Contains information related to the landing page of the admin console.

</td></tr></tbody>
</table>## Store applications installed

<table id="table_acw_kng_cyb"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Advanced Recommended actions for ITSM \[com.snc.uib.sow\_itsm\_ra\_advanced\]

</td><td>

Enables you to configure and display relevant actions to agents based on record context. Agents can follow the actions to help customers and resolve issues.

</td></tr><tr><td>

Task Intelligence Admin Console \[com.sn\_ti\_admin\]

</td><td>

Enables you to setup, manage, and monitor incident prediction models that help categorize incidents.

</td></tr></tbody>
</table>**Parent Topic:**[Task Intelligence for ITSM reference](task-intelligence-itsm-reference.md)

