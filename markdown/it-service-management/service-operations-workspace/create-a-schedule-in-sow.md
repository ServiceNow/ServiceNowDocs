---
title: Create and edit shift in Service Operations Workspace
description: Shift manager can create a new shift using the Schedule menu or Teams menu in Service Operations Workspace
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/create-a-schedule-in-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring On-Call Scheduling in Service Operations Workspace, On-Call Scheduling in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Create and edit shift in Service Operations Workspace

Shift manager can create a new shift using the **Schedule** menu or **Teams** menu in Service Operations Workspace

## About this task

There are two ways to create and edit a shift:

-   Navigate to **Workspaces** &gt; **Service Operation Workspace** and select \[Omitted image "icon-sr-teams.png"\] Alt text: Teams menu. Select a team to view details and click **schedules** tab.
-   Navigate to **Workspaces** &gt; **Service Operation Workspace** and select \[Omitted image "show-schedules-icon.png"\] Alt text: Schedules menu.

Get an overview of how to create and edit a shift in this video.

## Before you begin

Role required: rota\_manager, rota\_admin

## Procedure

1.  On **Schedules** page, select **Create shift** and provide values for the following fields on the **Create new** shift form:

    If you select **Create New**, provide the following details and select **Create shift**: \[Omitted image "create\_shift\_schedule\_sow.png"\] Alt text: Create shift form

<table id="table_d1x_z3z_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shift name

</td><td>

Name for the shift.

</td></tr><tr><td>

All day shift

</td><td>

Toggle for all day commitment.

</td></tr><tr><td>

Shift starts

</td><td>

Date and time the shift begins.

</td></tr><tr><td>

Shift ends

</td><td>

Date and time the shift ends.

</td></tr><tr><td>

Repeats

</td><td>

Shift repetition. Choices are:

-   Never
-   Daily
-   Weekly


</td></tr><tr><td>

Every

</td><td>

How often to repeat. Display depends on the time frame chosen.

</td></tr><tr><td colspan="2">

**More options**

</td></tr><tr><td>

Timezone

</td><td>

User timezone.

</td></tr><tr><td>

Holiday schedule

</td><td>

Schedule to use for the holiday.

</td></tr><tr><td>

Repeats until

</td><td>

Date and time to end repetition.

</td></tr></tbody>
</table>    For **Use shift template**, fill in the fields, as appropriate.

<table id="table_zl1_djz_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shift name

</td><td>

Name for the shift.

</td></tr><tr><td>

Template/Schedule

</td><td>

Existing templates for shifts.Choices are:

-   24 x 7
-   Off hours \(workday 8:00 - 5:00\)
-   Off hours \(workday 9:00 - 5:00\)
-   Workday 8:00 - 5:00
-   Workday 9:00 - 5:00


</td></tr></tbody>
</table>    You have successfully created a new shift.

2.  To edit a shift, right-click the shift card and select the icon\[Omitted image "edit-icon.png"\] Alt text: Edit shift

    Shift details open up in the side panel.

3.  From the shift details in the side panel, you can update the following shift details:

<table id="table_qd4_jtm_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Details** tab

</td><td>

Update the shift details:\[Omitted image "edit\_shift\_details\_tab\_sow.png"\] Alt text: Shift details form

-   All day shift
-   Shift starts
-   Shift ends
-   Repeats
-   Timezone
-   Holiday schedule
-   Repeats until


</td></tr><tr><td>

**Members** tab

</td><td>

Update the shift details:\[Omitted image "edit\_shift\_members\_tab\_sow.png"\] Alt text: Members form

-   Type of rotation interval. Possible options are:
    -   Daily
    -   Weekly
    -   Monthly

**Note:** This option is available only for the 2024 schedule engine. For information about this schedule engine, see [On-Call Scheduling new schedule engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/oncall-schedule-engine.md).

-   Rotation frequency for weekly interval
-   Rotation frequency for monthly interval. Also, specify if the roster rotation should start on the last day of the month or any specific day of the month.
-   Day of the week or month for rotation
-   Add rotation
-   Add/delete/rename responder level


</td></tr><tr><td>

**Escalation policies** tab

</td><td>

View escalation policy and click **Open Team Record** go to the team record. \[Omitted image "edit\_shift\_escalation\_policies\_tab\_sow.png"\] Alt text: Escalation policies form

</td></tr></tbody>
</table>4.  After updating the shift details, click **Save &amp; publish** to save the changes.

5.  Select the \[Omitted image "icon-sr-more-actions-vertical.png"\] Alt text: More icon icon to change shift to draft mode, delete, or deactivate/activate the selected shift.

6.  Select **Back to all shifts** to view all the shifts for a selected team.

    You can also select \[Omitted image "icon-sr-more-actions-vertical.png"\] Alt text: More icon to change shift color.


**Parent Topic:**[Configuring On-Call Scheduling in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configuring-oncall-scheduling-sow.md)

