---
title: Maintenance schedule fields for Enterprise Asset Management
description: A detailed description of all maintenance schedule fields in the Enterprise Asset Management application.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Enterprise Asset Management reference, Enterprise Asset Management, IT Asset Management]
---

# Maintenance schedule fields for Enterprise Asset Management

A detailed description of all maintenance schedule fields in the Enterprise Asset Management application.

## Maintenance Schedule

<table id="table_vy5_pyv_hvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the maintenance schedule.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the maintenance schedule.

</td></tr><tr><td>

Trigger

</td><td>

Trigger that specifies the type of conditions that must be met for the maintenance to run.

 Select one of the following options:

-   **Duration**: Triggers the maintenance to run based on time. If you select this option, the Duration Details form section appears, where you can specify more details about the trigger.
-   **Meter**: Triggers the maintenance to run based on a specific enterprise asset field value. If you select this option, the Meter Details form section appears, where you can specify more details about the trigger.
-   **Condition**: Triggers the maintenance to run based on filter conditions. If you select this option, the Condition Details form section appears, where you can specify more details about the trigger.
-   **Script**: Triggers the maintenance to run based on advanced script criteria. If you select this option, the Script Details form section appears, where you can specify more details about the trigger.
-   **Duration or Meter**: Triggers the maintenance to run based on time or a specific enterprise asset field value, whichever comes first. If you select this option, the Duration Details and Meter Details form sections appear, where you can specify more details about the trigger.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the maintenance schedule is active.

</td></tr></tbody>
</table>## Duration Details

**Note:** This form section appears only if you set the **Trigger** field to **Duration** or **Duration or Meter** in the Maintenance Schedule form section.

<table id="table_wd2_pvw_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger type

</td><td>

Frequency at which you want the maintenance to run.

 Select one of the following options:

-   **Interval**: Runs the maintenance at a specified time interval. If you select this option, the **Days**, **Hours**, **Minutes**, and **Seconds** fields appear, where you can specify the amount of time that must pass before the maintenance runs again.
-   **Weekly**: Runs the maintenance once a week. If you select this option, the**Due day of week** and **Due time** fields appear, where you can specify the day and time at which you want the maintenance to run each week.
-   **Monthly**: Runs the maintenance once a month on a specific date. If you select this option, the **Due day of month** and **Due time** fields appear, where you can specify the date and time at which you want the maintenance to run each month.
-   **Annually**: Runs the maintenance once a year on a specific date and month. If you select this option, the **Due month**, **Due day of month**, and **Due time** fields appear, where you can specify the month, date, and time at which you want the maintenance to run each year.
-   **Week in Month**: Runs the maintenance once a month during a specific week of the month. If you select this option, the **Due week in month** and **Due time** fields appear, where you can specify the week and time at which you want the maintenance to run each month.
-   **Day in Week in Month in Year**: Runs the maintenance once a year on a specific day, week, and month. If you select this option, the **Due month**, **Due week in month**, **Due day of week**, and **Due time** fields appear, where you can specify the month, week, day, and time at which you want the maintenance to run each year.

</td></tr><tr><td>

Lead time

</td><td>

Number days required for the scheduled maintenance work.

</td></tr></tbody>
</table>## Meter Details

**Note:** This form section appears only if you set the **Trigger** field to **Meter** or **Duration or Meter** in the Maintenance Schedule form section.

|Field|Description|
|-----|-----------|
|Field|Enterprise asset field that you want to match against to trigger the maintenance to run.|
|Every|Field value that an enterprise asset must match to trigger the maintenance to run.|

## Condition Details

**Note:** This form section appears only if you set the **Trigger** field to **Condition** in the Maintenance Schedule form section.

<table id="table_k52_2ww_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filter Condition

</td><td>

Filter conditions that trigger the maintenance to run

 You can add multiple filter conditions to the trigger using the following options:

-   **or**: Enables you to specify any of the conditions that an enterprise asset can meet to trigger the maintenance to run.
-   **and**: Enables you to specify all the conditions that an enterprise asset must meet to trigger the maintenance to run.
-   **+ New condition set**: Enables you to specify additional sets of conditions that an enterprise asset can meet to trigger the maintenance to run.

</td></tr></tbody>
</table>## Script Details

**Note:** This form section appears only if you set the **Trigger** field to **Script** in the Maintenance Schedule form section.

|Field|Description|
|-----|-----------|
|Script|Script specifying the advanced criteria that triggers the maintenance to run.|

**Parent Topic:**[Enterprise Asset Management reference](../concept/reference-enterprise-asset-management.md)

**Related topics**  


[Domain separation and Enterprise Asset Management](../concept/domain-separation-eam.md)

[Enterprise Asset Management roles](eam-roles.md)

[Enterprise model categories and corresponding classes](enterprise-model-categories.md)

[Mandatory fields in the bulk import spreadsheets](mandatory-bulk-fields.md)

[Normalization status for enterprise models](norm-status-eam.md)

[Model fields for Enterprise Asset Management](eam-model-fields.md)

[Contract fields for Enterprise Asset Management](contract-fields-eam.md)

[Maintenance plan fields for Enterprise Asset Management](maintenance-plan-fields-eam.md)

[Work plan fields for Enterprise Asset Management](wp-fields-eam.md)

[Work plan schedule fields for Enterprise Asset Management](work-plan-schedule-fields-eam.md)

[Expense line fields for Enterprise Asset Management](expense-line-fields-eam.md)

[Fields inherited from a parent asset group to a sub group](subgroups-parent-fields-eam.md)

[Enterprise asset disposal order stages](eamasset-disposalorder-stages.md)

[Terminology for linear assets](terms-eam.md)

[Installed with Enterprise Asset Management for Healthcare](installed-with-eam-healthcare.md)

[Installed with OT Asset Management](installed-with-otam.md)

[Asset put away task fields](put-away-task-form-eam.md)

