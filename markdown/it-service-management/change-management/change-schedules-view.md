---
title: Change schedules view
description: The Change Schedules module provides a Gantt or timeline view of change requests based on criteria defined within a Change Schedule Definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/change-schedules-view.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Change schedules, Configure, Change Management, IT Service Management]
---

# Change schedules view

The Change Schedules module provides a Gantt or timeline view of change requests based on criteria defined within a Change Schedule Definition.

The change schedule provides detailed insight into change requests that are included based on the change schedule definition. The change requests can include change timing, duration, related change tasks, blackout periods, and maintenance windows for any given date, week, or month.

To view the Change Schedules page, you must activate the Change Management - Change Schedule plugin \(com.snc.change\_management.soc\).

Change requests are represented by a span. The duration of the span is defined by the start and end date fields defined in the Change Schedule definition. On the Change Schedules page, you can define conditions by using the condition builder. The condition builder determines which change requests are displayed and sorted in a change schedule.

**Note:** To show the blackout and maintenance windows of the change in the calendar view, the **Configuration item** field for the change must be populated. The change schedule view displays related blackout and maintenance windows only for the primary configuration item \(CI\) of each change request.

\[Omitted image "change-schedule-view-annotated.png"\] Alt text: Change Schedule timeline page with numbered UI components. For descriptions, see the following table.

<table id="table_cv4_kmd_gdb"><thead><tr><th>

SI \#

</th><th>

UI component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Context Menu

</td><td>

Option to do the following:-   Create new schedule: You can create a new schedule from a simplified wizard.
-   Edit a schedule: Modify change schedules that you own. Changes are saved to the related Change Schedule Definition record.
-   Copy a schedule: If you are the owner of the change schedule that you want to copy, then a copy of the change schedule is created. If you copy a change schedule that another user owns, you become the owner of the copied schedule and the new schedule is fully editable by you.
-   View schedule definition: You can view the change schedule definition and the related fields associated with it.
-   Delete: Delete a change schedule that you own.

 **Note:**

-   A user with only the itil role who doesn't own a change schedule can only create a schedule, copy a schedule, or view an existing schedule definition.
-   You become the owner of any schedule that you create. The new schedule that you create appears in the Change Schedule page in a tile form under the **Your Schedules** tab.

</td></tr><tr><td>

2

</td><td>

Span styles

</td><td>

Defined span color based on conditions you specify. You can add new span styles by selecting **Add Span Styles**. You can also edit an existing style rule, apply filters to a style rule, or remove a style rule.**Note:** By default, span styles are based on the Risk value of a change.

-   Risk = High – Span style is Red
-   Risk = Moderate – Span style is Orange
-   Risk = Low – Span style is Green

</td></tr><tr><td>

3

</td><td>

Share

</td><td>

Option to share schedules with other users by user name, group, or role. The share pane also provides a check box to share a change schedule with everybody. If change schedules are not shared with anyone, then only the owner, owner group, and administrator can see them. If a change schedule is shared with other users, an option is available to send an email notification to inform them of their access.

</td></tr><tr><td>

4

</td><td>

Configuration

</td><td>

Option to show or hide components of the change schedule, such as the configuration item, duration, or related tasks.

</td></tr><tr><td>

5

</td><td>

Keyboard shortcuts

</td><td>

List of available keyboard shortcuts to help you navigate quickly and to provide accessibility to users. The list of navigation shortcuts appears when you select the keyboard shortcuts icon \[Omitted image "keyboard-shortcut.png"\] Alt text:.

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

Option to navigate forward or back in time in the change schedule based on the current zoom level. Select **Today** to return to the current day and time.

</td></tr><tr><td>

8

</td><td>

Change record

</td><td>

Summary of the change record when you select any span. Use **Open Record** in the header of the summary to open the change request in the form view. In the form, you can view the entire change request record. **Note:** You can specify the fields that are displayed in this window. On the Change Schedule Definition form, under the **Record Summary** tab, specify required fields on **Left column fields** and **Right column fields**.

</td></tr></tbody>
</table>**Note:** Change schedules are loaded on the timeline page on the client side in batches of 20. You can load a maximum of 1000 records. System administrators can modify these numbers. For more information, see the properties in [Installed with Change Management - Change Schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/installed-cm-changeschedule.md).

**Parent Topic:**[Change schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-schedule.md)

**Related topics**  


[Create a change schedule from the Change Schedules page]()

[Create a change schedule from the change schedule definition]()

[Add related tasks to a change schedule]()

[Style rules definition]()

