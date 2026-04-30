---
title: Create an Orchestration ROI automation entry record
description: The ROI automation entry record couples the cost of performing a task with the specific workflow that automates the task, for the purpose of calculating the resulting savings.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Orchestration ROI, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an Orchestration ROI automation entry record

The ROI automation entry record couples the cost of performing a task with the specific workflow that automates the task, for the purpose of calculating the resulting savings.

## Before you begin

Role required: orchestration\_manager

Before starting this procedure, verify that the appropriate [labor rate cards](t_CreateOrchROILaborRateCard.md) were created.

## About this task

Use this record to apply a manual hourly rate to a task that is performed automatically by your instance. To determine the savings realized from orchestrating a task, the system can evaluate whether those savings were estimated or calculated.

-   **Estimated savings**: Uses the labor rate, the time estimates for completion of the task, and the number of automations that have been run to determine savings.
-   **Calculated savings**: Uses the labor rate, the time calculated for completion of the task, based on the configured evaluation period, and the number of automations that have been run to determine savings.

## Procedure

1.  Navigate to **All** &gt; **Orchestration** &gt; **ROI** &gt; **Automation Entry Form**.

2.  Fill in the fields on the form, as appropriate.

<table id="table_t5v_xcs_ps"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

Category of the selected workflow automation. The following categories are provided in the base Orchestration - ROI system:-   **Access &amp; Identity Management**
-   **Datacenter Automation**
-   **IT Service Management**
-   **Other**
 **Note:** To create a category, open the dictionary record for the Automation Entry Form \[automation\_entry\_form\] table and add an option to the choice list.

</td></tr><tr><td>

Item

</td><td>

Unique name for the specific task within the category. This value represents the work to which the labor rate card applies, such as **Password Reset**.

</td></tr><tr><td>

Resource

</td><td>

Labor rate card to apply to this automation entry. You must have IT Cost Management active on the instance for this field to appear.

</td></tr><tr><td>

Associated Workflows

</td><td>

Workflow automations created to automate this manual task. The system uses this field to identify the number of automations that have been run.

</td></tr><tr><td>

Estimated Duration \(min\) per Task

</td><td>

Estimated time to perform this task manually.

</td></tr><tr><td>

Estimated Volume per Month

</td><td>

Estimated number of times needed to perform this task manually per month.

</td></tr><tr><td class="sub-head" colspan="2">

Read-only fields

</td></tr><tr><td>

Start time

</td><td>

Start time for the evaluation period. Configure this value in the Time Range for Calculated Averages module.

</td></tr><tr><td>

End time

</td><td>

End time of the evaluation period. Configure this value in the Time Range for Calculated Averages module.

</td></tr><tr><td>

Calculated average duration per task \(min\)

</td><td>

Actual time required to perform this task manually.

</td></tr><tr><td>

Calculated average volume per month

</td><td>

Actual average number of times this task is performed manually per month.

</td></tr></tbody>
</table>3.  Select one of these submission options:

    -   **Submit**: Saves the record to the table without running any calculations.
    -   **Submit and process now**: Saves the record and calculates the savings based on the hourly rate and the number of workflow contexts for this automation entry.

**Parent Topic:**[Orchestration ROI](../concept/c_OrchestrationROI.md)

