---
title: Create a milestone for an engagement
description: Create a milestone for an engagement to track the progress of an engagement. You can also add audit tasks to a milestone.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Audit Supervisor Workspace, Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Create a milestone for an engagement

Create a milestone for an engagement to track the progress of an engagement. You can also add audit tasks to a milestone.

## Before you begin

Role required: sn\_audit.manager, sn\_audit\_ws.supervisor

## About this task

A milestone is used to track the progress of an engagement.

After you create milestones for an engagement, you can also add audit tasks to the milestone. You can track those tasks as milestones.

You can assign a milestone to a user who is responsible for the milestone. The assigned user must have the sn\_audit.user role. The assigned user then receives a notification about the assignment.

If an engagement moves to the Follow Up state, and if there are no open audit tasks, open milestones, or open observations, then the engagement moves to the **Closed** state.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Select the lists icon \(![List icon.](../image/ListsIcon.jpg)\).

3.  Select **All engagements** or **My engagements** in the Execution list.

4.  Select the link to the engagement record in the **Name** column.

5.  Select the **Milestones** tab.

6.  Select **New**.

7.  On the form, fill in the fields.

<table id="table_yfp_crw_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the milestone. This number is automatically generated.

</td></tr><tr><td>

Name

</td><td>

Name of the milestone.

</td></tr><tr><td>

Parent

</td><td>

Parent engagement of the milestone.

</td></tr><tr><td>

Type

</td><td>

Audit milestone type. The choices are:-   Scoping
-   Planning
-   Fieldwork
-   Follow up
-   Reporting
-   Closure


</td></tr><tr><td>

State

</td><td>

State of the milestone. The default state is **Open**.

</td></tr><tr><td>

Percent complete

</td><td>

Percentage of milestone completed.When a value is entered in this field, the state changes to **Work in progress**.

</td></tr><tr><td>

Key milestone

</td><td>

Option to mark the milestone as important.

</td></tr><tr><td>

Auto complete and close

</td><td>

Option to mark the milestone as close complete when all the associated audit tasks are completed and closed.If this option is enabled, then the percent complete is automatically updated according to the number of tasks marked as closed complete.

</td></tr><tr><td>

Description

</td><td>

Brief description of the milestone.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group responsible for the milestone.The group members must have the sn\_audit.user role assigned.

</td></tr><tr><td>

Assigned to

</td><td>

Person responsible for working on the milestone.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

Expected completion date of the milestone.

</td></tr><tr><td>

Completion date

</td><td>

Actual completion date of the milestone.

</td></tr><tr><td>

Closed date

</td><td>

Actual close date of the milestone.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Additional comments

</td><td>

Comments that customers can also view.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Comments that only the administrator and audit supervisor can view.

</td></tr></tbody>
</table>8.  Select **Save**.

    You can view the description of the Milestone record and monitor its status in the **State** banner of the default Overview page.


