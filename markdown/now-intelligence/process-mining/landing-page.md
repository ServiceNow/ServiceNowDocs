---
title: Projects landing page
description: From the projects landing page for Process Mining, you can access generated projects, business process insights, and Analyst workbench.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Process Mining workspace, Exploring Process Mining, Process Mining, Platform Analytics]
---

# Projects landing page

From the projects landing page for Process Mining, you can access generated projects, business process insights, and Analyst workbench.

The projects landing page shows project cards for projects that have been created by or shared with you for viewing. A project that has been created but not yet generated shows a warning icon ![warning icon](../image/warning-icon.png) next to its grayed out title. The warning indicates that the project isn’t available to view.

Some projects may be marked as Retricted. The owner and the users they explicitly share it with have access to the restricted projects. Administrators and power users don't have access to the mined data unless the project is shared with them. Only the owner can clear the **Restricted** field. When you are dealing with sensitive data and need to restrict access, you can use this option. For more information , see [Set objectives for Process Mining projects](../task/set-objectives.md).

![Restricted project on Projects landing page](../image/restricted-project.png)

![Projects landing page](../image/landing-page2.png "Projects landing page")

Project cards show overview details of mined projects. You can filter them by table, created by, project, activity definition, name, or short description.

|Field|Description|
|-----|-----------|
|Project name|The name of the project. You can select a project name to open Analyst workbench and access business findings.|
|Status|Designation of usage status of the project.|
|Short description of the project.|Brief description provided about the project.|
|Created by|The user who created the project.|
|Tables|The selected table the project reports on.|
|Last mined|When the project's data was last mined, in days.|
|\# of records|The number of records that apply to the selected data table and filter configurations for the project.|
|Process Variation|The percentage profile of uncertainty in process steps. Example: Users taking multiple routes versus the ideal path to a goal. The percentage is calculated by the number of variants divided by the number of records.|
|Average Duration|The average time across all closed filtered records from the time of their being opened to being closed.|

From a project card, relevant user roles can perform the following tasks by selecting a card's menu.

![Project card menu](../image/project-card.png)

<table id="table_jc3_c3w_z4b"><thead><tr><th>

Menu item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open

</td><td>

Select to open a project.

</td></tr><tr><td>

Edit

</td><td>

Select to edit a project.

</td></tr><tr><td>

Copy

</td><td>

Select to copy the configuration and create a project definition.When you copy a project, the associated improvement opportunities also get copied.

</td></tr><tr><td>

Mine Project \(Sample\)

</td><td>

Mines a sample project using limited data instead of performing a full data extraction.

</td></tr><tr><td>

Mine Project \(Full\)

</td><td>

Mines a full data extraction for a project.

</td></tr><tr><td>

Delete

</td><td>

Deletes a project.

</td></tr></tbody>
</table>**Parent Topic:**[Process Mining workspace](analyst-workbench-overview.md)

