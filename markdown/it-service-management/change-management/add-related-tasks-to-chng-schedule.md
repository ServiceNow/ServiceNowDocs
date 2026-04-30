---
title: Add related tasks to a change schedule
description: Create related definitions to present related tasks for change requests in the change schedule. For example, to view the change tasks associated with a change request, you need to define a related definition. You can also add style rules specific to a related task.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Change schedules, Configure, Change Management, IT Service Management]
---

# Add related tasks to a change schedule

Create related definitions to present related tasks for change requests in the change schedule. For example, to view the change tasks associated with a change request, you need to define a related definition. You can also add style rules specific to a related task.

## Before you begin

-   You have activated Change Management - Change Schedule plugin \(com.snc.change\_management.soc\).
-   Parent change schedule is defined.
-   Role required: itil, sn\_chg\_soc.change\_soc\_admin, sn\_change\_role, sn\_change\_write roles, sn\_change\_write, or admin

## Procedure

1.  Navigate to **All** &gt; **Schedules** &gt; **Change Schedule Definitions**.

2.  Select a Change schedule definition.

3.  Select **New** in **Related Definition** tab.

4.  On the form, fill in the fields.

<table id="table_shn_gqf_gdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the related definition.

</td></tr><tr><td>

Change schedule definition

</td><td>

Reference for the parent change schedule.

</td></tr><tr><td>

Active

</td><td>

Check box to select whether the child schedule is active.

</td></tr><tr><td class="sub-head" colspan="2">

Related Records

</td></tr><tr><td>

Table name

</td><td>

Choice list to select the table on which the Related Definition is based.

</td></tr><tr><td>

Reference field

</td><td>

Reference the Related Definition is based on, for example, change request.

</td></tr><tr><td>

Start date field

</td><td>

Start date field from the related record.

</td></tr><tr><td>

End date field

</td><td>

End date field from the related record.

</td></tr><tr><td>

Condition

</td><td>

Conditions included in the change schedule and the associated ordering of the conditions. For example, to display only implementation tasks, you must build a specific condition that displays implementation tasks.

</td></tr><tr><td class="sub-head" colspan="2">

Record Summary**Note:** The record summary pop-up appears when you click any span on the change schedule timeline.

</td></tr><tr><td>

Left column fields

</td><td>

List of fields that appear on the left column of the record summary pop-up. The record summary pop-up appears when you click any span on the change schedule timeline.

</td></tr><tr><td>

Right column fields

</td><td>

List of fields that appear on the right column of the record summary pop-up. The record summary pop-up appears when you click any span on the change schedule timeline.

</td></tr></tbody>
</table>    **Note:** You can also add style rules specific to a related task. You can configure the change schedule page to show related tasks for the change, such as implementation tasks.

5.  Click **Submit**.


**Parent Topic:**[Change schedules](../concept/change-schedule.md)

**Related topics**  


[Change schedules view](../concept/change-schedules-view.md)

[Create a change schedule from the Change Schedules page](create-chng-sch-from-chng-sch-page.md)

[Create a change schedule from the change schedule definition](create-chng-sch-from-chng-sch-def.md)

[Style rules definition](../concept/style-rules-definition.md)

