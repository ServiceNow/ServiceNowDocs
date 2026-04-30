---
title: Map a time card category with operational work types
description: Map custom time card categories with operational work types so you can select only the operational resource plans that are associated with the user for a specific time card period and category while posting time.
locale: en-US
release: yokohama
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Time cards, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Map a time card category with operational work types

Map custom time card categories with operational work types so you can select only the operational resource plans that are associated with the user for a specific time card period and category while posting time.

## Before you begin

Role required: pps\_admin

## About this task

By default, all base system time card categories are mapped with the base system operational work types. If mapping is not done for custom categories, the **Resource Plan** field displays all the operational resource plans associated with the user for that time period when you create a time card.

During time card creation, after you select a time card category and task or during time sheet submission for other category time cards, operational resource plans are populated for that category and task as described in the following table.

<table id="table_kjg_t3j_ylb"><thead><tr><th>

Category

</th><th>

Task

</th><th>

Resource Plan

</th></tr></thead><tbody><tr><td>

-   Admin
-   External labor
-   Meeting
-   Phone call
-   Training
-   Out of office
-   Appointment
-   Time off
-   KTLO

</td><td>

Task, project, demand, project task, or demand task, or no value is selected in the **Task** field.

</td><td>

Displays the resource plans associated with the task, project, demand, project task, or demand task when a task is selected.

 If no resource plans are associated with the selected task, or no task is selected, then the mapped operational resource plan for that operational work type for that category is displayed.

</td></tr><tr><td>

Custom

</td><td>

Any of the task/project/demand/ project task/demand task

</td><td>

Displays the resource plans associated with the task, project, demand, project task, or demand task when a task is selected.

 If no resource plans are associated with the selected task, or no task is selected, then the mapped operational resource plan for that custom operational work type for that category is displayed.

 If mapping is not done, then all the operational resource plans are displayed.

</td></tr><tr><td>

Other category \(custom and OOTB\) from Time Sheet Portal

</td><td>

N/A

</td><td>

Displays the mapped operational resource plans.

 If mapping is not done, then all the operational resource plans are displayed.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Time Card Category Mapping**.

2.  Click **New**.

3.  From the **Time card category** menu, select the required time card category.

4.  From the **Operational work type** menu, select the operational work type you want to map to the time card category you selected in the previous step.

5.  Click **Submit**.


**Parent Topic:**[Time cards](../concept/c_TimeCards.md)

