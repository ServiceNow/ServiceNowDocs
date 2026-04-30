---
title: CAB meeting attendance using the CAB workbench
description: As an itil user, you can attend a Change Advisory Board \(CAB\) meeting, view the agenda items, and the change schedule. If you are an approver, you can approve a change request.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Working with the CAB Workbench, Using Change Management, Change Management, IT Service Management]
---

# CAB meeting attendance using the CAB workbench

As an itil user, you can attend a Change Advisory Board \(CAB\) meeting, view the agenda items, and the change schedule. If you are an approver, you can approve a change request.

View the details of a CAB meeting and its agenda by navigating to **Change** &gt; **Change Advisory Board** &gt; **CAB Workbench**. From the calendar, you can view the CAB meeting schedule for a day, week, or month. To view details of a meeting, click the meeting and then click **Open** in the pop-up window.

![CAB meeting details.](../image/cab-meeting.png "CAB Workbench")

The following components describe the different activities that you can perform in the interface:

<table id="table_nnn_dhy_nz"><thead><tr><th>

Level

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

View the timer that displays the total elapsed time, the meeting name, and the scheduled date and time of the meeting. The timer count starts from zero. The color code in the timer changes based on the overall percentage of time elapsed from the total duration of the meeting:-   0% - 50%: Green
-   50% - 70%: Yellow
-   75% - 100%: Orange
-   &gt; 100%: Red

The text below the meeting name displays the total time allotted for the meeting.

</td></tr><tr><td>

2

</td><td>

View the current agenda item. The timer displays the amount of time spent discussing the current meeting agenda item. The form area displays the details of the current agenda item that you have selected. When the current agenda item changes, the details on the form and the calendar change accordingly. If you select an agenda item that is not the current agenda item, the form area displays the details of the selected agenda item. The form area does not display details of the current agenda item even when the current agenda item is changed to the next agenda item. **Note:** If you are one of the approvers for the agenda item, the **Approve** and **Reject** buttons appear below the timer.

You can click **Approve** or **Reject** as appropriate, enter your comments in the Confirmation pop-up window, and click **Approve** or **Reject**.

</td></tr><tr><td>

3

</td><td>

Filter the agenda items that you want to view and click **Notify me** to receive a notification before the agenda item starts. Click the **Pending Agenda Items** list, and select the **All Agenda Items**, **My Agenda Items**, or **Approved Agenda Items** option. The list of agenda items appears under the filter condition list, in the order that the items appear in the agenda.

</td></tr><tr><td>

4

</td><td>

-   **Meeting Notes**: Displays the document note entered by the host of the meeting.
-   **Attendees**: Displays the list of attendees and also indicates whether the attendees are currently connected to the meeting.
-   **Conference Information**: Displays any content that was stored in the **Conference Information** field from the related CAB meeting record.

</td></tr><tr><td>

5

</td><td>

View the details of a current change in the form view or in the calendar view.**Show form**: Click the show form icon \(![Show form icon.](../image/show-form.png)\) to display change details in the form view. The **Change**, **Planning**, and **Schedule** tabs provide information about the change request meeting, planning, and scheduling.

 **Show calendar**: Click the show calendar icon \(![Show calendar icon.](../image/show-calendar.png)\) to display change details on the calendar form. You can select the day or the month that you want to view details of a change for. In a day view, you can click the settings icon \(![Settings icon.](../image/settings-icon.png)\) and then click the configuration icon \(![Configuration icon.](../image/cab-workbench-configuration-icon.png)\) to set relevant filter conditions. If you turn on any of the configuration filter conditions, the related change records are displayed. The change records appear in the time slot of the day that the current change implementation is planned for. In the configuration settings, you can view other potential conflicts. The conflicts can be other change requests that are scheduled for implementation by the same assignee, assignment group, or for the same configuration item.

 The day and month view of the calendar displays the Blackout Schedule time, Maintenance Window, and the agenda item that is in progress. In the day view, the specific time slot of the planned blackout and maintenance window is highlighted. In the calendar view, the entire day is highlighted.

 **Note:** For standard change proposals, the **Change**, **Proposal**, and **Change Request Values** tabs provide information on change request meeting, proposal, and change request values. The show form \(![Show form icon.](../image/show-form.png)\) and the show calendar \(![Show calendar icon.](../image/show-calendar.png)\) icons do not appear for standard change proposals.

</td></tr></tbody>
</table>**Parent Topic:**[Working with the CAB Workbench](using-cab-workbench-cf.md)

