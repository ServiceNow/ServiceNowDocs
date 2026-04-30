---
title: Create a CAB meeting
description: Create a Change Advisory Board \(CAB\) meeting in Service Operations Workspace to review and authorize change requests.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [CAB in Service Operations Workspace, CAB Workbench in Service Operations Workspace]
breadcrumb: [Change Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a CAB meeting

Create a Change Advisory Board \(CAB\) meeting in Service Operations Workspace to review and authorize change requests.

## Before you begin

Role required: sn\_change\_cab.cab\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the list icon \(![List icon.](../image/sow-list.png)\).

3.  In the **Change Advisory Board**, select All CAB meetings.

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

Board groups

</td><td>

Change Advisory Board user groups that are expected to attend the CAB meeting.

</td></tr><tr><td>

Board members

</td><td>

Change Advisory Board members who are expected to attend the CAB meeting.

</td></tr><tr><td>

State

</td><td>

-   **Pending**: Indicates that the meeting is yet to begin. It’s the default state of the meeting.
-   **In progress**: Indicates that the meeting has begun and is in progress.
-   **Complete**: Indicates that the meeting has occurred and is finished.
-   **Canceled**: Indicates that the meeting has been canceled.
 **Note:** The system automatically updates the **State** field when the meeting starts and ends from within the CAB workbench. However, the CAB manager can manually update this field when a future meeting has to be canceled or if the CAB workbench closes unexpectedly during the meeting.

</td></tr><tr><td>

Meeting start time

</td><td>

Start date and time for the meeting.**Note:** When you add an agenda item to a CAB meeting, the **CAB date** field in the change request is automatically updated with this date.

</td></tr><tr><td>

Meeting end time

</td><td>

End date and time for the meeting.

</td></tr><tr><td>

Locations

</td><td>

One or more locations for your CAB meetings. For example, meeting rooms in different offices.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Meeting Notes|Enter notes for the meeting, if any.|

<table id="table_jyt_klf_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use filter criteria to drive Change Request date range

</td><td>

Option to choose a time range for the planned start and end date from **Change Request additional condition** instead of selecting specific dates based on meeting schedule.

**Note:** If you select **the Use filter criteria to drive Change Request date range** field in a cab meeting, the **Change Requests starting after** and the **Change Requests starting on or before** fields are turned off for the meeting, and therefore ignored. The change request additional conditions drive the date range.

</td></tr><tr><td>

Change Requests starting after

</td><td>

Change requests that start after this date and time should be added to the CAB meeting.

</td></tr><tr><td>

Change Requests starting on or before

</td><td>

Change requests that start on or before this date and time should be added to the CAB meeting.

</td></tr><tr><td>

Complete Pre-approved Changes

</td><td>

Check box to mark each pre-approved change request as **Complete** in the CAB meeting agenda. **Note:** Pre-approved changes are automatically marked as complete so that approvers do not have to review them. The pre-approved changes are visible in the CAB Workbench, and can be discussed if necessary.

</td></tr><tr><td>

Time per Agenda Item

</td><td>

The time, in minutes and seconds, allotted to discuss each change request on the agenda. The allotted time can be adjusted for agenda items before or during the meeting.

</td></tr><tr><td>

Notification lead time

</td><td>

The advanced notification on the number of agenda items that needs to be discussed.

</td></tr><tr><td>

Auto Add Agenda Decisions

</td><td>

Check box to capture agenda decisions automatically on the meeting widget. The agenda decision is captured in the following format:`(CAB Automation) - <*change request number*> - <*decision*> - <*CAB Manager name*> - <*time*><*AM/PM*> <*timezone*>`

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Conference details|Information such as meeting links, passwords, and phone numbers.|

6.  Select **Save**.


-   **[Add an agenda item to a CAB meeting](cm-add-agenda-cab-meeting-sow.md)**  
Add change requests to your CAB meeting agenda for review.
-   **[Manage attendees in a CAB meeting](cm-manage-attendees-cab-meeting-sow.md)**  
Manage attendees of your CAB meeting who will review the change requests during the meeting.

**Parent Topic:**[Change Management in Service Operations Workspace](../concept/change-sow.md)

**Related topics**  


[Create a change request in Service Operations Workspace](create-change-sow.md)

[Work on a change request in Service Operations Workspace](work-on-change-sow.md)

[Standard change catalog](../concept/standard-change-catalog-sow.md)

[Create a change task in Service Operations Workspace](create-change-task-sow.md)

[Work on a change task in Service Operations Workspace](work-on-change-task-sow.md)

[Create a Change Advisory Board \(CAB\) definition](cm-create-cab-definition-sow.md)

[Conduct a CAB meeting in the CAB workbench](cm-manage-cab-meeting-workbench-sow.md)

