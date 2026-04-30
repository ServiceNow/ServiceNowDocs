---
title: Project definition form
description: Use the Project definition form to create a project.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Process Mining reference, Process Mining, Platform Analytics]
---

# Project definition form

Use the Project definition form to create a project.

<table id="table_bsh_kb3_3yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Project number. This number is automatically generated when the record is created.

</td></tr><tr><td>

Project status

</td><td>

Status of the project.-   **New**

Project is new. This is the default state for newly created projects.

-   **Draft**

A project in the setup phase that is not yet in use.

-   **Published**

Project is ready for use by entitled users.

-   **Retired**

Project should no longer be used to analyze the process.


Process analyst users must manually update this field, to track the state of the project. This can be essential if there are multiple projects for a given process.

</td></tr><tr><td>

Name

</td><td>

Name of the project

</td></tr><tr><td>

Mining state

</td><td>

Current mining state for this project.

</td></tr><tr><td>

Short description

</td><td>

Short description for the project.

</td></tr><tr><td>

Last mined

</td><td>

Date of the last time the project was mined.

</td></tr><tr><td>

Goal

</td><td>

The goal associated to this project selected from existing goal records.

</td></tr><tr><td>

Auto Retire

</td><td>

Select the **Auto Retire** check box if you want to automatically retire the project based on inactivity for a specified number of days \(Default: 90 days\).

 You can extend the retirement by moving it back to published or draft state before the versions get cleaned in another 90 Days \(default\).

 If you don’t change the retired status within the specified days, the mined versions are permanently deleted. However, the project definition isn’t deleted. You can opt out of auto retirement by clearing this check box.

 The default value of 90 days can be changed by the administrator in the System Properties. For more information see, [Data cleanup properties](../concept/data-cleanup.md#).

</td></tr><tr><td>

Template

</td><td>

Whether to create a default or Workforce Optimization template.

</td></tr><tr><td>

Watch list

</td><td>

Users who receive notifications regarding the status of the generated project.

</td></tr><tr><td>

KPI dashboard

</td><td>

The PAR dashboard \[par\_dashboard\] associated with this project. Select an existing dashboard or use the Plus \(+\) icon to create a dashboard.

 For details on creating these dashboards, see [Create and use dashboards](../../../use/dashboards/concept/create-and-edit-dashboards.md)

 **Note:** Adding a dashboard in this field links the dashboard at the project level. To add the dashboard at the process configuration level, use the same field on the process configuration \[promin\_process\_def\] record.

</td></tr></tbody>
</table>**Parent Topic:**[Process Mining reference](../concept/process-mining-reference.md)

