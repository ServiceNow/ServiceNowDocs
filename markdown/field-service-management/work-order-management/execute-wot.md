---
title: Execute and track external work order tasks
description: Execute and track the time required for work order tasks that you have accepted.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Work order tasks on the Field Service Contractor Portal, Contractor Portal, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Execute and track external work order tasks

Execute and track the time required for work order tasks that you have accepted.

## Before you begin

Role required: wm\_ext\_agent and wm\_ext\_manager

## Procedure

1.  Navigate to **All** &gt; **Field Service Contractor Portal** &gt; **Homepage**.

2.  Click **Start Travel** when you begin your travel to work on the task.

    This is mandatory if the **Scheduled travel start** field is completed.

    -   When the agent clicks **Start Travel**, the customer receives a notification email and SMS that an agent is coming.
    -   A sub state **On Route** is automatically set to determine that you have started travel for the work order task.
    -   The **Check-In** option appears when `Enable/Disable Onsite Arrival Check-in for Agents` property is enabled. For more information, see [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md).
3.  Open the task record and do either of the following to mark your arrival or check-in at the work location.

    -   To perform any task related activities before starting work, click **Check-In**

        **Note:** At this stage, a notification is sent to the customer, informing them that the agent has arrived on-site and is ready to begin the work. For more information, see [Customer notifications for work order tasks](../concept/Configuring-cust-exp.md#). The substate **Onsite Arrival** is automatically set, indicating that you have reached your travel destination for the work order task.

    -   To by-pass the check-in option and start work directly, click **Start Work**.
    -   The **Actual work start** field is automatically updated with the current system time, marking the beginning of the task.
    -   The work order task's state changes to **Work In Progress** to reflect that the task is actively being worked on.
    -   The **Actual travel duration** field is automatically calculated by the system. It measures the time difference between the **Actual travel start** and **Actual onsite arrival** timestamps, unless manually set.
    -   If the system properties `work.management.allow.auto.timecard` and `work.management.allow.travel.task.timecard` are enabled, time cards are automatically created. These time cards capture the duration of your work on the task, including the task's travel time.
    -   The generated time card for the task's travel duration is stored under the **Time Worked** related list. This provides a record of the time spent traveling to the task location.
4.  If you take a break from the task activity, pause and then resume work on the task.

    -   When you take a break from the task activity, click **Pause Work**. The button toggles to **Resume Work**.
    -   When you are ready to work on the activity again, click **Resume Work**.
    Each time you pause or resume work on the task, the timestamp is captured in the activity stream and the actual time you worked on the task is automatically calculated. An entry for the time worked is created in the **Time Worked** related list.

5.  When the work is done, open the task record and add a work note describing what you did to complete the task.

6.  Click **Close Complete**.

7.  If you want to close the task when the work is pending, open the task record, and click**Close Incomplete**.

    For more information about closing incomplete work order tasks, see [Close an external work order task as incomplete](close-ext-wot-incomplete.md).


## Result

The cumulative amount of time worked on the task is captured in the **Actual Work Duration** field. This total includes the time you started working on the task until you closed work on the task, excluding any time paused on the work.

**Parent Topic:**[Work order tasks on the Field Service Contractor Portal](../concept/work-order-tasks.md)

