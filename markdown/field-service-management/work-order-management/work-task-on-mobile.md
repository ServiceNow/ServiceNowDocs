---
title: Start work on a work order task
description: You can record both the time you begin traveling to the work site and the time you start the work.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Prioritizing on ServiceNow Agent, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Start work on a work order task

You can record both the time you begin traveling to the work site and the time you start the work.

## Before you begin

Role required: wm\_agent or wm\_dispatcher

## About this task

Administrators can configure the **wm\_notification.upcoming.task.reminder.minutes.before** system property to set the number of minutes before which a task reminder is sent. By default, you receive a notification 45 minutes before the work start time.

Administrators can enable push notifications in Studio. For information on setting up push notifications, see Mobile push notifications.

## Procedure

1.  Open the ServiceNow Agent application.

2.  Tap **My Work**.

3.  In the **My Tasks** section, click **See All**.

4.  Select the work order task you want to get started with.

    You can only start work on tasks that are in the **Accepted** state.

5.  Perform any of the following actions.

<table id="choicetable_jsf_24s_4fb"><thead><tr><th align="left" id="d148864e130">

Option

</th><th align="left" id="d148864e133">

Details

</th></tr></thead><tbody><tr><td id="d148864e139">

**To start traveling to the job site**

</td><td>

Perform one of the following actions:-   To record your travel start time using the work order task list, swipe the desired task to the left and select **Start Travel**.
-   To record your travel start time after you review the work order task details:

    -   Select and open the desired task.
    -   Review the task details.
    -   Tap **Start Travel**.
**Note:**

    -   The **Sub state** and **Work agent status** are automatically updated as **On Route** to determine that you have started traveling to work on a task.
    -   The **Start Travel** button transforms into**Check-In** before initiating check-in actions. The **Check-In** option is visible only when the `Enable/Disable Onsite Arrival Check-in for Agents` property is enabled. For more information, see [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md).


</td></tr><tr><td id="d148864e213">

**To check-in at job site before starting work**

</td><td>

Tap **Check-In** after reaching the destination.**Note:**

-   The system checks geofence boundary. If you are offline, the system can bypass geofence check with confirmation and sets the status as "Offline Mode. Geofence could not be validated". For more information on the check-in process, see [Onsite arrival and check-in](../reference/onsite-arrival-and-check-in.md).
-   The substate **Onsite Arrival** is automatically set, indicating that you have reached your travel destination for the work order task.
-   A notification is sent to the customer, informing them that the agent has arrived on-site and is ready to begin the work. For more information, see [Customer notifications for work order tasks](../concept/Configuring-cust-exp.md#).


</td></tr><tr><td id="d148864e254">

**To start directly working on the task with automatic check-in**

</td><td>

Perform one of the following actions:-   To record the work start time using the work order task list, swipe the desired task to the left and tap **Start Work**.
-   To record the work start time after you review the work order task details:

    -   Select and open the desired task.
    -   Review the task details.
    -   Tap **Start Work**.
**Note:**

    -   The system checks geofence boundary. If you are offline, the system can bypass geofence check with confirmation and sets the status as "Offline Mode. Geofence could not be validated".
    -   A message appears that your time card was created and your time worked has been accounted for.
    -   Your **Work agent status** is automatically updated as **On Site** to determine that you have started working on a task.
-   Tap **Quick Actions** and update your status to **On break** if you want to take a break from the task or **Off Shift** if you are out of your shift time.


</td></tr><tr><td id="d148864e318">

**To change the expected start or estimated end time for the task**

</td><td>

1.  Open the task.
2.  Tap the More actions ![More actions icon](../image/OverflowIcon.png)icon in the upper right hand corner, and tap **Edit task**.
3.  Tap the calendar icon next to either **Expected start** or **Estimated end**.

**Note:** You cannot update the expected start time once a task is in the Work in Progress state.

4.  Update the time or date you plan to start or end the task.
5.  Tap **OK**, then tap **Submit**.
The task expected start or estimated end time is updated.

</td></tr></tbody>
</table>
## Result

The following fields are updated in the work order task:

-   The work order task's state changes to **Work In Progress** to reflect that the task is actively being worked on.
-   The **Actual work start** field is automatically updated with the current system time, marking the beginning of the task.
-   The **Actual travel duration** field is automatically calculated by the system. It measures the time difference between the **Actual travel start** and **Actual onsite arrival** timestamps, unless manually set.
-   The **Actual onsite arrival** time is automatically populated as **Actual work start** date time when check-in is skipped.
-   The generated time card for the task's travel duration is stored under the **Time Worked** related list. This provides a record of the time spent traveling to the task location.
-   If the system properties `work.management.allow.auto.timecard` and `work.management.allow.travel.task.timecard` are enabled, time cards are automatically created. These time cards capture the duration of your work on the task, including the task's travel time.

**Related topics**  


[bundle-mobile.notification-preference-settings]

[Complete a questionnaire for a work order task](complete-questionnaire-mobile-app.md)

[Create a sales opportunity](create-opportunity.md)

