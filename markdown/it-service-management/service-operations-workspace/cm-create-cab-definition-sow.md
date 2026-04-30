---
title: Create a Change Advisory Board \(CAB\) definition
description: Create a Change Advisory Board \(CAB\) definition in Service Operations Workspace to set up recurring CAB meetings for reviewing and authorizing change requests.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [CAB in Service Operations Workspace, CAB Workbench in Service Operations Workspace]
breadcrumb: [Change Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a Change Advisory Board \(CAB\) definition

Create a Change Advisory Board \(CAB\) definition in Service Operations Workspace to set up recurring CAB meetings for reviewing and authorizing change requests.

## Before you begin

Role required: sn\_change\_cab.cab\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the list icon \(![List icon.](../image/sow-list.png)\).

3.  In the **Change Advisory Board**, select **My CAB Definitions** or **All CAB Definitions**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_b2s_kdl_2w"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the CAB meeting.

</td></tr><tr><td>

CAB manager

</td><td>

Name of the user who manages the CAB meeting.

</td></tr><tr><td>

Delegates

</td><td>

Delegate CAB members who can substitute as the CAB manager during the meeting.

</td></tr><tr><td>

Board members

</td><td>

Change Advisory Board members who are expected to attend the CAB meeting.

</td></tr><tr><td>

Board groups

</td><td>

Change Advisory Board user groups that are expected to attend the CAB meeting.

</td></tr><tr><td>

Rolling Meeting Window

</td><td>

Number of days for which you want to create CAB meetings.**Note:** The CAB schedule and related schedules, if any, determine the number of CAB meetings that are created. For example, if you have a CAB meeting schedule of once every week and you enter 28 days in the **Rolling Meeting Window** field, then three CAB meetings are created.

</td></tr><tr><td>

CAB Type

</td><td>

Type of CAB meeting this definition is used for: **Normal** or **Emergency**.The CAB type determines the urgency and the required level of scrutiny for the change.

</td></tr><tr><td>

Time zone

</td><td>

Time zone for the CAB meeting.

</td></tr><tr><td>

Locations

</td><td>

One or more locations for your CAB meetings. For example, meeting rooms in different offices.

</td></tr><tr><td>

Active

</td><td>

Option to specify whether the CAB definition is active.

</td></tr><tr><td>

Conference Details

</td><td>

Information such as meeting links, passwords, and phone numbers.

</td></tr></tbody>
</table><table id="table_jyt_klf_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notification lead time

</td><td>

The advanced notification on the number of agenda items that needs to be discussed.

</td></tr><tr><td>

Use filter criteria to drive Change Request date range

</td><td>

Option to choose a time range for the planned start and end date from **Change Request Addition Conditions** instead of selecting specific dates based on meeting schedule.

**Note:** The same field is selected for all CAB meetings in the CAB definition unless individually overridden.

</td></tr><tr><td>

Automatically Add Change Requests

</td><td>

Option to automatically add change requests to the CAB meeting agenda based on the conditions set in the **Change Request Addition Conditions**.

</td></tr><tr><td>

Time per Agenda Item

</td><td>

The time, in minutes and seconds, allotted to discuss each change request on the agenda. The allotted time can be adjusted for agenda items before or during the meeting.

</td></tr><tr><td>

Complete Preapproved Changes

</td><td>

Option to mark each pre-approved change request as Complete in the CAB meeting agenda. Pre-approved changes are automatically marked as complete so that approvers do not have to review them. The pre-approved changes are visible in the CAB Workbench, and can be discussed if necessary.

</td></tr><tr><td>

Auto Add Agenda Decisions

</td><td>

Option to capture agenda decisions automatically on the meeting widget. The agenda decision is captured in the following format:`(CAB Automation) - <*change request number*> - <*decision*> - <*CAB Manager name*> - <*time*><*AM/PM*> <*timezone*>`

</td></tr></tbody>
</table>6.  Select **Save**.

    The CAB definition is saved. The **Related records** tab appears.

7.  Add one or more schedule entries to the CAB definition to schedule a series of CAB meetings.

    These schedule entries let you set valid days and times for holding CAB meetings.

    1.  Select the **Related records** tab and then select **Scheduled Entries**.

    2.  Select **New**.

    3.  On the Schedule Entry fields form, fill in these fields.

<table id="table_dms_nhl_2w"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the schedule entry.

</td></tr><tr><td>

Type

</td><td>

Type of schedule entry for the specified date and time duration, for example, appointment or meeting.-   **Time off**: Shown as planned time-off.
-   **Appointment**: Shown as appointment time.
-   **Meeting**: Shown as meeting time.
-   **Phone call**: Shown as time for making phone calls.
-   **Excluded**: The duration is excluded.


</td></tr><tr><td>

Show as

</td><td>

How the schedule entry is displayed on the CAB calendar, for example, busy or tentative.

</td></tr><tr><td>

When

</td><td>

Start and end date and time for the schedule entry.

</td></tr><tr><td>

All day

</td><td>

Option to make the schedule entry active for the entire duration of the selected dates.

</td></tr><tr><td>

Time zone

</td><td>

Time zone for the schedule entry. The time zone cannot be modified.

</td></tr><tr><td>

Repeats

</td><td>

Frequency with which the schedule entry repeats, for example, daily. weekly, or monthly.When you select **Monthly**, the **Monthly type** field appears. Enter the number of times in a month when the schedule entry repeats.

 When you select **Yearly**, the **Yearly type** field appears. Select an option, as follows:

-   **Day of the year**: Chosen as the current day on which you define the schedule.
-   **Floating**: If you select this option, the following fields appear:
    -   **Float week**: The week of the month when the schedule entry repeats.
    -   **Float day**: The day of that week when the schedule entry repeats.
    -   **Month**: The month when the schedule entry repeats.


</td></tr><tr><td>

Repeat every

</td><td>

If the schedule entry is selected to repeat, specifies how often it repeats. For example, if you select weekly repetitions, specify the frequency such as every week or every two weeks.This field appears when you select the **Weekly**, **Monthly**, or **Yearly** options.

</td></tr><tr><td>

Repeat on

</td><td>

If the schedule entry is selected to repeat, then specify when it repeats. For example, if you select weekly repetitions, specify the days of the week when it repeats.This field appears when you select the **Weekly** option.

</td></tr><tr><td>

Repeat until

</td><td>

If the schedule entry is scheduled to repeat, specifies an end date until which the schedule entry is repeated.

</td></tr></tbody>
</table>    4.  Select **Submit**.

    The scheduled entry is added to the CAB definition and displays in the Scheduled Entries list.

8.  Add one or more related schedules to a CAB definition.

    Related schedules enable you to set valid schedules for holding CAB meetings. For example, if you set the public holiday schedule as a related schedule, it ensures that no CAB meeting is scheduled on a public holiday.

    1.  Select the **Related records** tab and then select **Related Schedules**.

    2.  Select **Add**.

    3.  Select one or more related schedules and select **Add**.

    The related schedule is added to the CAB definition and displays in the Related Schedules list.

9.  Select **Refresh CAB Meetings**.

    CAB meetings are generated based on the rolling meeting window and schedules defined in the CAB definition and listed in the **CAB Meetings** list under the **Related records** tab.

    This CAB meeting series created from CAB definitions inherit the criteria of the CAB definition.


## What to do next

You can modify CAB meeting details and send meeting requests to attendees. You can also manage agendas by reviewing or adding agenda items to each of the CAB meetings.

**Parent Topic:**[Change Management in Service Operations Workspace](../concept/change-sow.md)

**Related topics**  


[Create a change request in Service Operations Workspace](create-change-sow.md)

[Work on a change request in Service Operations Workspace](work-on-change-sow.md)

[Standard change catalog](../concept/standard-change-catalog-sow.md)

[Create a change task in Service Operations Workspace](create-change-task-sow.md)

[Work on a change task in Service Operations Workspace](work-on-change-task-sow.md)

[Create a CAB meeting](cm-create-cab-meeting-sow.md)

[Conduct a CAB meeting in the CAB workbench](cm-manage-cab-meeting-workbench-sow.md)

