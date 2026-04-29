---
title: Create a single CAB meeting occurrence
description: Depending on your requirements, you can create an individual Change Advisory Board \(CAB\) meeting occurrence.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with the CAB Workbench, Use, Change Management, IT Service Management]
---

# Create a single CAB meeting occurrence

Depending on your requirements, you can create an individual Change Advisory Board \(CAB\) meeting occurrence.

## Before you begin

Role required: sn\_change\_cab.cab\_manager

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Change Advisory Board** &gt; **My CAB Meetings**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Click **New**.

3.  On the CAB Meeting form, fill in the fields.

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

Name of the user who manages the CAB meeting. The default is the user that is currently logged in.

</td></tr><tr><td>

Delegates

</td><td>

Delegate CAB members who can substitute as the CAB manager during the meeting.

</td></tr><tr><td>

Board groups

</td><td>

 

</td></tr><tr><td>

Board members

</td><td>

 

</td></tr><tr><td>

State

</td><td>

-   **Pending**: Indicates that the meeting is yet to begin. It is the default state of the meeting.
-   **In progress**: Indicates that the meeting has begun and is in progress.
-   **Complete**: Indicates that the meeting has occurred and is finished.
-   **Canceled**: Indicates that the meeting has been canceled.
 **Note:** The system automatically updates the **State** field when the meeting starts and ends from within the CAB workbench. There is no need to manually change this field, unless, for example, the CAB manager wants to cancel a future meeting. If the CAB workbench closes unexpectedly, the CAB manager must manually update the **State** field.

</td></tr><tr><td>

Meeting start time

</td><td>

Start date and time for the meeting.**Note:** When you add an agenda item to a CAB meeting, the **CAB date** field in the change request is automatically updated with this date.

</td></tr><tr><td>

Meeting end time

</td><td>

End date and time for the meeting.

</td></tr><tr><td>

Meeting Notes

</td><td>

Enter notes for the meeting, if any.

</td></tr><tr><td>

Locations

</td><td>

One or more locations for your CAB meetings. For example, meeting rooms in different offices.

</td></tr><tr><td class="subhead" colspan="2">

Conference Information

</td></tr><tr><td>

Conference details

</td><td>

Information such as meeting links, passwords, and phone numbers.

</td></tr><tr><td class="subhead" colspan="2">

Agenda Management

</td></tr><tr><td>

Use filter criteria to drive Change Request date range

</td><td>

If selected, helps to choose a time range for the planned start and end date from **Change Request additional condition** instead of selecting specific dates based on meeting schedule.

**Note:** If you select **the Use filter criteria to drive Change Request date range** field in a cab meeting, the **Change Requests starting after** field and the **Change Requests starting on or before** field is disabled for the meeting, and therefore ignored. The change request additional conditions drive the date range.

</td></tr><tr><td>

Change Requests starting after

</td><td>

Change requests that starts after this date and time should be added to the CAB meeting.

</td></tr><tr><td>

Change Requests starting on or before

</td><td>

Change requests that starts on or before this date and time should be added to the CAB meeting.

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
</table>4.  Open the form context menu and select **Save**.

    The **Agenda Items** and **Attendees** related lists appear.


## What to do next

You can now add agenda items and attendees to the cab meeting.

-   **[View CAB meeting details](view-cab-meeting-details.md)**  
You can view the details of any past, scheduled, or in-progress CAB meeting.
-   **[Modify CAB meeting details](refresh-cab-meeting-agenda-items.md)**  
You can modify the agenda items for a specific CAB meeting.
-   **[Send CAB meeting request to attendees](send-cab-meeting-request-attendees.md)**  
You can send CAB meeting invitations to attendees for each CAB meeting.

**Parent Topic:**[Working with the CAB Workbench](../concept/using-cab-workbench-cf.md)

