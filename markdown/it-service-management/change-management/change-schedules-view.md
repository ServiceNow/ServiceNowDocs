---
title: Change schedules view
description: The Change Schedules module provides a Gantt or timeline view of change requests based on criteria defined within a Change Schedule Definition.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Change schedules, Configure, Change Management, IT Service Management]
---

# Change schedules view

The Change Schedules module provides a Gantt or timeline view of change requests based on criteria defined within a Change Schedule Definition.

The change schedule provides detailed insight to change requests that are included based on the change schedule definition. The change requests can include change timing, duration, related change tasks, blackout periods, and maintenance windows for any given date, week or month.

To view the Change Schedules page, you must activate Change Management - Change Schedule plugin \(com.snc.change\_management.soc\).

Change requests are represented by a span. The duration of the span is defined by the start and end date fields defined in the Change Schedule definition. The Change Schedules page allows conditions to be defined using the condition builder. The condition builder determines which change requests are displayed and sorted in a change schedule.

**Note:** To show the blackout and maintenance windows of the change in the calendar view, the **Affected CI** field for the change must be configured.

![change schedule timeline](../image/change-schedule-timeline.png "Change Schedule timeline page")

<table id="table_cv4_kmd_gdb"><thead><tr><th>

SI \#

</th><th>

UI Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Context Menu

</td><td>

Option to do the following:-   Create new schedule: You can create a new schedule from a simplified wizard.
-   Edit a schedule: Allows the modification of change schedules you own and any changes made are saved to the related Change Schedule Definition record.
-   Copy a schedule: If you are the owner of the change schedule that you want to copy, then a copy of the change schedule is created. If you want to copy a change schedule that is owned by any other user, then you become the owner of the copied schedule and the new schedule is fully editable by you.
-   View schedule definition: You can view the change schedule definition and the related fields associated with it.
-   Delete: Allows users, who own a change schedule, to delete the schedule.

 **Note:**

-   A user who only possesses the ITIL role and is not the owner of a change schedule can only create a schedule, copy a schedule, or view an existing schedule definition.
-   You become the owner of any schedule that you create. The new schedule that you create appears in the Change Schedule page in a tile form under the **Your Schedules** tab.

</td></tr><tr><td>

2

</td><td>

Span styles

</td><td>

Defined span color based on conditions you specify. You can add new span styles by clicking **Add Span Styles**. You can also edit an existing style rule, apply filters to a style rule, or remove a style rule.**Note:** By default, span styles are based on the Risk value of a change.

-   Risk = High – Span style is Red
-   Risk = Moderate – Span style is Orange
-   Risk = Low – Span style is green

</td></tr><tr><td>

3

</td><td>

Share

</td><td>

Schedules to be shared to other users by user name, group, or role. The share pane also provides a check box to share a change schedule with everybody. If change schedules are not shared with anyone, then only the owner, owner group, and administrator can see them. If a change schedule is shared with other users, an option is available to send an email notification to inform them of their access.

</td></tr><tr><td>

4

</td><td>

Configuration

</td><td>

Components of the change schedule including the configuration item, duration, or any related tasks can be hidden or exposed.

</td></tr><tr><td>

5

</td><td>

Keyboard shortcuts

</td><td>

List of available keyboard shortcuts to help you navigate quickly and to provide accessibility to users. The list of navigation shortcuts appears when you click ![keyboard shortcut](../image/keyboard-shortcut.png)

</td></tr><tr><td>

6

</td><td>

Zoom

</td><td>

Zoom levels to control change schedule zoom resolution. The range can vary from hours to a yearly view of change schedules.

</td></tr><tr><td>

7

</td><td>

Arrow keys

</td><td>

Option to navigate forward or back in time in the change schedule based on the current zoom level. Click **Today** to navigate back to the current day and time in a single click.

</td></tr><tr><td>

8

</td><td>

Change record

</td><td>

Summary of the change record when you click any span. Use **Open Record** in the header of the summary to open the change request in the form view. In the form, you can view the entire change request record. **Note:** You can specify the fields that are displayed in this window. On the Change Schedule Definition form, under the **Record Summary** tab, specify required fields on **Left column fields** and **Right column fields**.

</td></tr></tbody>
</table>**Note:** Change schedules are loaded on the timeline page on the client side in batches of 20. You can load a maximum of 1000 records. These numbers can be modified by system administrator. For more information, refer the properties at [Installed with Change Management - Change Schedule](../reference/installed-cm-changeschedule.md#).

**Parent Topic:**[Change schedules](change-schedule.md)

**Related topics**  


[Create a change schedule from the Change Schedules page](../task/create-chng-sch-from-chng-sch-page.md)

[Create a change schedule from the change schedule definition](../task/create-chng-sch-from-chng-sch-def.md)

[Add related tasks to a change schedule](../task/add-related-tasks-to-chng-schedule.md)

[Style rules definition](style-rules-definition.md)

