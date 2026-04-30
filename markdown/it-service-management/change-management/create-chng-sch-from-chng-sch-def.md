---
title: Create a change schedule from the change schedule definition
description: You can define a change schedule from a change schedule definition record. Change schedule definitions help you to define the content that displays in the change summary popover, the users, groups or roles with whom a schedule is to be shared, and related span style colors.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Change schedules, Configure, Change Management, IT Service Management]
---

# Create a change schedule from the change schedule definition

You can define a change schedule from a change schedule definition record. Change schedule definitions help you to define the content that displays in the change summary popover, the users, groups or roles with whom a schedule is to be shared, and related span style colors.

## Before you begin

-   You have activated Change Management - Change Schedule plugin \(com.snc.change\_management.soc\).
-   Role required: itil, sn\_chg\_soc.change\_soc\_admin, sn\_change\_role, sn\_change\_write roles, sn\_change\_write, or admin

## About this task

To create a new Change Schedule, specify the start and end date fields that you want to be represented in the user interface and also specify the conditions to determine which change requests to display.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Schedules** &gt; **Change Schedule Definitions** and click **New**.

2.  On the form, fill in the fields.

<table id="table_am1_qmf_gdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the change schedule.

</td></tr><tr><td>

Active

</td><td>

Check box to select if a schedule is active.

</td></tr><tr><td class="sub-head" colspan="2">

Changes

</td></tr><tr><td>

Start date field

</td><td>

Field from the change request form that determines the start date of the span.

</td></tr><tr><td>

End date field

</td><td>

Field from the change request form that determines the end date of the span.

</td></tr><tr><td>

Condition

</td><td>

Conditions which determine which change requests display in the Change Schedule interface and the order those change requests are sorted.

</td></tr><tr><td class="sub-head" colspan="2">

Record Summary

</td></tr><tr><td>

Left column fields

</td><td>

List of fields which appear on the left column of the record summary pop-up. The record summary pop-up appears when you click any span on the change schedule timeline.

</td></tr><tr><td>

Right column fields

</td><td>

List of fields that appear on the right of the window when you click any span on the change schedule timeline. The record summary pop-up appears when you click any span on the change schedule timeline.

</td></tr><tr><td class="sub-head" colspan="2">

Blackout and Maintenance

</td></tr><tr><td>

Show blackout window

</td><td>

Check box to select if blackout window associated to a change request appears in the change schedule timeline.

</td></tr><tr><td>

Blackout window color

</td><td>

Color to represent blackout window in the change schedule timeline.

</td></tr><tr><td>

Show maintenance window

</td><td>

Check box to select if maintenance window associated to a change request appears in the change schedule.

</td></tr><tr><td>

Maintenance window color

</td><td>

Color to represent maintenance window in the change schedule timeline.

</td></tr><tr><td class="sub-head" colspan="2">

Sharing

</td></tr><tr><td>

Share with

</td><td>

Option to share the schedule with everyone associated with the change or with specific users and groups.

</td></tr><tr><td>

Owner

</td><td>

Owner of the change schedule.

</td></tr><tr><td>

Group Owner

</td><td>

Group that owns a change schedule and has administrative rights to the change schedule.

</td></tr><tr><td class="sub-head" colspan="2">

Related Link

</td></tr><tr><td>

Show Schedule

</td><td>

Link to the change schedule that you have defined.

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

Related Definitions

</td><td>

Details of related child schedules

</td></tr><tr><td>

Style Rules

</td><td>

Options to define style conditions to determine the color of a span using a condition builder. For example, if you want all changes of type Emergency to show as a red span, a span style can be defined for that condition.

</td></tr></tbody>
</table>3.  Click **Submit**.


**Parent Topic:**[Change schedules](../concept/change-schedule.md)

**Related topics**  


[Change schedules view](../concept/change-schedules-view.md)

[Create a change schedule from the Change Schedules page](create-chng-sch-from-chng-sch-page.md)

[Add related tasks to a change schedule](add-related-tasks-to-chng-schedule.md)

[Style rules definition](../concept/style-rules-definition.md)

