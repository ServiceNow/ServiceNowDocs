---
title: CAB meeting management using the CAB Workbench
description: As a Change Advisory Board \(CAB\) manager, you can view and manage details of a CAB meeting and its agenda items through the CAB Workbench.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/manage-cab-meeting-using-cab-workbench.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Working with the CAB Workbench, Use, Change Management, IT Service Management]
---

# CAB meeting management using the CAB Workbench

As a Change Advisory Board \(CAB\) manager, you can view and manage details of a CAB meeting and its agenda items through the CAB Workbench.

You can view the details of a CAB meeting and its agenda by navigating to **Change** &gt; **Change Advisory Board** &gt; **CAB Workbench**. The calendar offers a view of your CAB meeting schedules for the day, week, or month. To view your meeting details, select the meeting and then select **Open** in the pop-up calendar. To start a meeting, select **Start meeting**.

**Note:** When you select the first agenda item for the first time, a confirmation window appears. To start the meeting, select **Yes**. Otherwise, select **No**.

\[Omitted image "start-cab-meeting.png"\] Alt text: CAB Workbench calendar with the Start meeting button

The details of the change request meeting appear.

\[Omitted image "cab-meeting.png"\] Alt text: CAB Workbench with numbered areas. For descriptions, see the following table.

The following table describes the CAB Workbench components.

<table id="table_fs3_vky_nz"><thead><tr><th>

Level

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

You can view the timer that displays the total elapsed time, the meeting name, and the scheduled date and time of the meeting. The timer count starts from zero. The color code in the timer changes based on the overall percentage elapsed from the total duration of the meeting:-   0% - 50%: Green
-   50% - 70%: Yellow
-   75% - 100%: Orange
-   &gt; 100%: Red

The text that follows the meeting name displays the total time allotted for the meeting.

</td></tr><tr><td>

2

</td><td>

-   Select **Pause** to pause an agenda item.
-   Select **Next** to skip an agenda item.

**Note:** The agenda item is added to the **All Agenda Items** list.

-   Select **Restore** to return the agenda item to the **Pending Agenda Items** list.

**Note:** The agenda item is added to the end of the **Pending Agenda Items** list.

-   Select **Promote** to move the agenda item to the top of the list.
-   Select **Demote** to append the current agenda item in the **Pending Agenda Items** list so that you can discuss the agenda item later.

**Note:** The timer displays the amount of time spent discussing the current meeting agenda item.

-   Select **End meeting** to end a meeting.

</td></tr><tr><td>

3

</td><td>

You can filter the agenda items to view. -   Select the **Pending Agenda Items** list, and select the **All Agenda Items**, **My Agenda Items**, or **Approved Agenda Items** option.

**Note:** The list of agenda items appears under the filter condition list, in the order that the items appear in the agenda.

-   Select **Promote** to move an agenda item to the top of the agenda item list.

</td></tr><tr><td>

4

</td><td>

You can take meeting notes whether you are a host or a delegate. You can view the list of attendees and conference information.-   **Meeting Notes**: Enables the CAB manager and delegates to document notes for the overall meeting. The notes captured in the widget can be shared from the widget. The widget emails the contents to the list of attendees, which are automatically saved to the corresponding **Meeting Notes** field in the CAB Meeting record.

Any notes specific to a change request can be added directly to the change request. To add a note, use the editable view of the form under the edit icon \[Omitted image "cab-workbench-edit.png"\] Alt text: Edit icon. in the upper left of the form widget.

**Note:** The agenda decisions made by the CAB and change approvers, such as whether the agenda item is approved or rejected or when CAB manager skips to another agenda item without making a decision, are automatically captured in the meeting notes widget. The agenda decisions are stored in the **Meeting Notes** field in the related CAB Meeting record.

-   **Attendees**: Displays the list of attendees and indicates if the attendees are currently connected to the meeting with the green Presence icon. The list also displays the attendee's response to the meeting invitation such as Accept, Tentative, Decline, or No response.
-   **Conference Information**: Displays any content that was stored in the **Conference Information** field on the related CAB Meeting record.

</td></tr><tr><td>

5

</td><td>

You can view the details of a current change in the form view or in the calendar view.**Show form**: Select the show form icon \[Omitted image "show-form.png"\] Alt text: Show form. to display change details in the form view. The **Change**, **Planning**, and **Schedule** tabs provide information about the change request meeting, planning, and scheduling. You can edit the form view by using the edit icon \[Omitted image "cab-workbench-edit.png"\] Alt text: Edit icon..

 To customize the view, select the list context menu icon \[Omitted image "cab-workbench-list-context.png"\] Alt text: List contextual menu icon. and then select **View** &gt; **cab\_workbench**. On the Change Request form, open the context menu and navigate to **Configure** &gt; **Form Layout**. On the Configuring Change Request form, you can add fields and sections that you want to display in the form view.

 **Show calendar**: Select the show calendar icon \[Omitted image "show-calendar.png"\] Alt text: Show calendar icon. to display current change details on the calendar form. You can select the day or month for which to view meeting details. In the day view, select the settings icon \[Omitted image "settings-icon.png"\] Alt text: Settings icon. and then select the configuration icon \[Omitted image "cab-workbench-configuration-icon.png"\] Alt text: Configuration icon. to set relevant filter conditions. If you turn on any of the configuration filter conditions, the related change records are displayed. The change records appear in the time slot of the day that the current change implementation is planned for. In the configuration settings, you can view other potential conflicts. The conflicts can be other change requests that are scheduled for implementation by the same assignee, assignment group, or for the same configuration item.

 The day and month view of the calendar displays the blackout schedule, the maintenance window, and the agenda item that is in progress. In the day view, the specific time slot of the planned blackout and maintenance window is highlighted. In the calendar view, the entire day is highlighted.

</td></tr></tbody>
</table>**Parent Topic:**[Working with the CAB Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/using-cab-workbench-cf.md)

