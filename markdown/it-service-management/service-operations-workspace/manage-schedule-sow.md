---
title: Manage your schedule using the Service Operations Workspace
description: Look up your schedule, create an event of custom event type, request time off for an on-call or work shift, or swap your shift with your peers using the calendar in Service Operations Workspace.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Service Operations Workspace - Scheduling, Workforce Optimization for ITSM in the Service Operations Workspace, Optimize, Service Operations Workspace for ITSM, IT Service Management]
---

# Manage your schedule using the Service Operations Workspace

Look up your schedule, create an event of custom event type, request time off for an on-call or work shift, or swap your shift with your peers using the calendar in Service Operations Workspace.

## Before you begin

-   If your system administrator has enabled the **sn\_uib\_agent\_sp.allow\_agent\_edit\_break** system property, you can edit the start and end time of your break time in a shift span.
-   If your system administrator has enabled the **sn\_uib\_agent\_sp.allow\_agent\_add\_remove\_break** system property, you can add or remove your break time in a shift span.

Role required: sn\_shift\_planning.agent

## About this task

If you can work during the requested shift, you can also approve your peer's request for shift swap. When you request time off for an on-call shift, you can also propose an agent to cover the shift. You can also filter agents in the team calendar based on team member, location, skills, shift plan or events.

You can:

-   Swap shifts with agents that are within your assignment group.
-   Add attendees to the meeting or training event types.
-   Edit or delete meeting or training event types that you have created.
-   Edit or delete work event types if you're the logged-in user and if the event has been assigned to you.

**Note:**

-   If the agent's calendar in Workforce Optimization for ITSM is integrated with their Microsoft Outlook calendar, they can view their shifts, schedules, and events such as meetings, trainings, and time-off in your Microsoft Outlook calendar. For more information, see [Synchronize agent calendar in Workforce Optimization for ITSM with the Microsoft Outlook calendar](../../configurable-workforce-optimization-itsm/concept/synchronize-microsoft-outlook-wfo-itsm.md).
-   When you create an event of types meeting or training, the logged-in user will always be part of the attendees list and cannot be removed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Click the Schedule icon.

    Access the schedule:

    -   View your schedule by clicking the **My Calendar** tab. Then, use the list ![List icon](../../itsm-manager-workspace/image/lists_icon.png) to select the schedule that you want to view by day, week, or month.
    -   View another agent's schedule by clicking the **Team Calendar** tab. Then, click an agent's schedule to see that agent's work and break times.
    **Note:** You can view the schedule for the primary assignment group and the on-call group you’re part of.

3.  Create an event of custom event type.

    You can create, edit, or delete events of custom event types that your system administrator has enabled for agent access.

    1.  Click **New** and select the name of the custom event type.
    2.  In the custom event type form, fill in the fields as required.
    3.  Click **Save**.
    To edit the event, select the event, and then the edit icon \(![Edit icon](../../configurable-workforce-optimization-itsm/image/edit-icon.png)\) to make the necessary changes and save the event. To delete it, select the delete icon.

4.  Make a request.

    -   You can use the **Compose** field in the time-off request to communicate with your manager.
    -   You can use the **Compose** field in the shift swap request to communicate with your peers.
<table id="table_d5p_ggx_glb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Request a shift swap

</td><td>

Create a shift swap or swap by selecting a shift.To create a shift swap:

1.  Click **New** and select **Shift Swap**.
2.  Fill in the requestor details.

Your name is automatically populated in the **Requestor** field.

    1.  In the **Date** field, select the date for which you want to swap the shift.
    2.  In the **Shift** field, select the shift to swap. If you have only one shift for the selected date, this field is auto-populated.
3.  Fill in the details for the agent with whom you want to swap the shift.
    1.  In the **Agent** field, select the name of the agent.
    2.  In the **Date** field, select the date for which you want to swap the shift.
    3.  In the **Shift** field, select the shift to swap. If you have only one shift for the selected date, this field is auto-populated.
4.  Click **Submit**.
To swap by selecting a shift:

1.  Select a shift on the calendar and click the swap shift icon.
2.  From the Shift menu for your shift, select the shift that you want to swap with another agent. This information is auto-populated when you open the request using the swap shift icon.
3.  In the **Agent** field for the requested shift, select the agent that you want to swap with.
4.  From the Shift menu for the requested shift, select the agent's shift that you want to swap with.
5.  Click **Submit**.


</td></tr><tr><td>

Request time off for a work shift

</td><td>

Create a new time-off request or select a work shift for which you want to take time off.To create a new time-off request:

1.  Click **New** and select **Time Off**.
2.  In the **Start date** field, click the calendar icon and select the date to start taking time off.
3.  In the **End date** field, click the calendar icon and select the date you want to the end time off.
4.  Click **Save**.
To create a request from a work shift:

1.  Select the work shift in the calendar for which you want to take time off and click the Request Time-off icon \( ![Request time-off icon](../../itsm-workspace/image/time-off-calendar-icon.png)\).

The start date and time and the end date and time are automatically populated.

2.  In the **Title** field, enter a name for the work shift.
3.  In the Description field, enter a reason for the time-off.
4.  Click **Save**.
**Note:**

-   To edit a work shift, select the shift span for which you want to edit the break time, select the edit icon \(![Edit icon](../../configurable-workforce-optimization-itsm/image/edit-icon.png)\) in the work shift, edit the desired break times and click **Save**.
-   If you edit your time-off request after you submit it, the request changes to **Requested** state.


</td></tr><tr><td>

Request time off for an on-call shift

</td><td>

Create a new on-call time-off request or select an on-call shift for which you want to take time off.**Note:** The PTO approval preferences for each on-call group are set by your administrator. For more information, see [Configure preferences for a user group](../../../administer/on-call-scheduling/task/config-group-prefs-oncall.md).The **com.snc.on\_call\_rotation.pto.approval.required** property must be set `true`. For more information, see [System properties for On-Call Scheduling](../../../administer/on-call-scheduling/reference/on-call-properties.md).

 To create a new request:

1.  Click **New** and select **On Call Time Off**.
2.  In the **Start date** field, click the calendar icon and select the date to start taking time off.
3.  In the **End date** field, click the calendar icon and select the date you want to the end time off.
4.  In the **Group** field, select the group in which the agent that you propose for cover belongs.
5.  In the **Proposed Cover** field, select the name of the agent.
6.  Click **Save**.
 To create a request from an on-call shift:

 1.  Select an on-call work shift in the calendar for which you want to take time off.
2.  Click the Request Time-off icon \( ![Request time-off icon](../../itsm-workspace/image/time-off-calendar-icon.png)\).

The start date and time, the end date and time, and the group are automatically populated.

3.  In the **Proposed Cover** field, select the name of the agent.
4.  Request time off.
5.  Click **Save**.


</td></tr></tbody>
</table>    The shift-swap request moves to the approval queue of the agent that you’ve requested to swap with. For more information, see [Approve or reject a shift swap](approve-reject-shift-swaps-sow.md)

    The time-off request moves to your manager's approval queue. For more information about approvals, go to [Track and manage your teams' schedule](../../configurable-workforce-optimization-itsm/task/approve-time-off-shift-swaps-wfo-itsm.md)


**Parent Topic:**[Service Operations Workspace - Scheduling](../concept/itsm-sow-workspace-scheduling.md)

