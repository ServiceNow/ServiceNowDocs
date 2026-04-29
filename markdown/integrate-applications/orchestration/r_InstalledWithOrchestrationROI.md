---
title: Installed with Orchestration ROI
description: Several types of components are installed with the Orchestration - ROI plugin \(com.snc.runbook\_automation.roi\).Tables are added with activation of Orchestration ROI.Plugins are installed with activation of Orchestration ROI, if they are not already active.Roles are added with activation of Orchestration ROI.UI actions are added with activation of Orchestration ROI.Script includes are added with activation of Orchestration ROI.Client scripts are added with activation of Orchestration ROI.Business rules are added with activation of Orchestration ROI.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Orchestration ROI, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Installed with Orchestration ROI

Several types of components are installed with the Orchestration - ROI plugin \(com.snc.runbook\_automation.roi\).

**Parent Topic:**[Orchestration ROI](../concept/c_OrchestrationROI.md)

## Tables installed with Orchestration ROI

Tables are added with activation of Orchestration ROI.

<table id="table_on4_5sp_ps"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expense and Savings\[run\_rate\_predicted\_savings\]

</td><td>

Contains the data for the reports in **Orchestration** &gt; **ROI Reports** &gt; **Predicted Savings**.

</td></tr><tr><td>

Savings Report\[savings\_report\]

</td><td>

Contains the number of automations that have been run before the date specified in the **Processed On** column, based on:-   Each automation entry’s associated workflows
-   Estimated savings based on the estimated duration per task.
-   Calculated savings based on calculated duration.

</td></tr><tr><td>

Detailed Savings Report\[detailed\_savings\_report\]

</td><td>

Contains a detailed list for the Savings Report \[savings\_report\] table. This list contains each automation’s run date and savings for that automation.

</td></tr><tr><td>

Automation Entries\[automation\_entry\_form\]

</td><td>

Contains automation entries that couple labor resources to specific manual tasks. You can specify the estimated duration to perform a task manually and the estimated number of times that a task is performed per month. If this automation entry already has workflow automations implemented, you can specify the associated workflows. The system calculates the savings, based on the labor rate card and the number of workflow automations that have been performed.

</td></tr><tr><td>

Roadmap Planning\[roadmap\_planning\]

</td><td>

Contains roadmap planning for each automation entry to be implemented. You can provide estimated hours to implement a workflow automation, the automation percentage anticipated by the end of the year, and the starting month to implement the workflow.

</td></tr><tr><td>

Correlated Tasks\[manual\_mapping\_records\]

</td><td>

Contains all matching manual tasks for each automation entry. Each tasks’s information is stored in this table for the system to use to calculate the actual duration and volume for each manual task.

</td></tr><tr><td>

Correlated Tasks Rules\[manual\_mapping\_conditions\]

</td><td>

Contains the correlated task rules the system uses to look up manual tasks corresponding to each automation entry.

</td></tr></tbody>
</table>## Plugins installed with Orchestration ROI

Plugins are installed with activation of Orchestration ROI, if they are not already active.

<table id="table_q1x_r4l_qs"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost Management\[com.snc.cost\_management\]

</td><td>

Provides the labor rate cards Orchestration ROI uses to determine the savings for each automated task. See [Cost Management](https://www.servicenow.com/docs/access?context=r_CostManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>## Roles installed with Orchestration ROI

Roles are added with activation of Orchestration ROI.

<table id="table_mbl_pvp_ps"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Orchestration manager\[orchestration\_manager\]

</td><td>

Manages all activities in the Orchestration ROI module.

</td><td>

-   pa\_admin
-   report\_admin

</td></tr></tbody>
</table>## UI actions installed with Orchestration ROI

UI actions are added with activation of Orchestration ROI.

<table id="table_nrj_1yp_ps"><thead><tr><th>

UI action

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Savings Report

</td><td>

Automation Entry Form\[automation\_entry\_form\]

</td><td>

Displays the savings report specific to this automation entry, if the associated workflows are not empty.

</td></tr><tr><td>

Estimated and Projected Savings

</td><td>

Automation Entry Form\[automation\_entry\_form\]

</td><td>

Displays the estimated savings, based on the estimated duration of the task, and calculated savings, based on the calculated duration of the task.

</td></tr><tr><td>

Show Workflow Context

</td><td>

Detailed Savings Report\[detailed\_savings\_report\]

</td><td>

Shows the related workflow context.

</td></tr><tr><td>

Submit AND process now

</td><td>

Automation Entry Form\[automation\_entry\_form\]

</td><td>

Processes this new entry

</td></tr><tr><td>

Correlated Tasks

</td><td>

Correlated Tasks Rules\[manual\_mapping\_conditions\]

</td><td>

Displays all matching tasks from the Correlated Tasks \[manual\_mapping\_records\] table.

</td></tr><tr><td>

Detailed Savings Report

</td><td>

Automation Entry Form\[automation\_entry\_form\]

</td><td>

Displays the list of automations that have been run, based on associated workflows.

</td></tr><tr><td>

Task

</td><td>

Correlated Tasks\[manual\_mapping\_records\]

</td><td>

Displays the task record.

</td></tr><tr><td>

Submit AND process now

</td><td>

Correlated Tasks Rules\[manual\_mapping\_conditions\]

</td><td>

Processes a correlated task rule. This action performs matching on the specified table and the filter conditions.

</td></tr></tbody>
</table>## Script includes installed with Orchestration ROI

Script includes are added with activation of Orchestration ROI.

|Script include|Description|
|--------------|-----------|
|OrchestrationROIAjax|Script that calculates the actual duration and volume of a task.|
|OrchestrationROI|Script that calculates the number of workflow contexts, looks up all matching tasks, calculates savings, and other functions used in the UI actions.|
|ROIDemoDataUtil|Script that updates demo data timestamps.|

## Client scripts installed with Orchestration ROI

Client scripts are added with activation of Orchestration ROI.

<table id="table_pgk_pwq_ps"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display info for processing rules

</td><td>

Correlated Tasks Rules\[manual\_mapping\_conditions\]

</td><td>

Displays annotation on the Correlated Task Rule form advising that new task rules are not evaluated until the time specified in the ROI schedule.

</td></tr></tbody>
</table>## Business rules installed with Orchestration ROI

Business rules are added with activation of Orchestration ROI.

<table id="table_n4s_czq_ps"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delete corresponding records

</td><td>

Automation Entry Form\[automation\_entry\_form\]

</td><td>

When a record is deleted from the Automation Entry Form \[automation\_entry\_form\] table, this business rule deletes all records in other ROI tables that reference this entry.

</td></tr><tr><td>

Insert into Run Rate &amp; Savings

</td><td>

Automation Entry Form\[automation\_entry\_form\]

</td><td>

When a new automation entry is provided, this business rule calculates the estimated savings, based on the estimated duration of a task and its associated labor rate card.

</td></tr><tr><td>

Insert into Savings Reports

</td><td>

Automation Entry Form\[automation\_entry\_form\]

</td><td>

When a new automation entry is provided, this business rule inserts a new record into the Savings Report \[savings\_report\] table with the**automations\_run** field set to **0**.

</td></tr></tbody>
</table>