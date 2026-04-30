---
title: Start work
description: What to do when you are ready to begin traveling to the first task.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage tasks on the map, Execute a task from the agent map, Execute work order tasks, Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Start work

What to do when you are ready to begin traveling to the first task.

## Before you begin

Role required: wm\_agent.

## About this task

As a field service agent, to provide a more accurate representation of the work order task activities, you can use two sub states "On Route" and "Onsite Arrival," to document your travel time and on-site activities.

## Procedure

1.  Open the task record from the map.

2.  Click **Start Travel** when you begin your travel to work on the task.

    This is mandatory if the **Scheduled travel start** field is completed.

    -   When the agent clicks **Start Travel**, the customer receives a notification email and SMS that an agent is coming.
    -   A sub state **On Route** is automatically set to determine that you have started travel for the work order task.
    -   The **Check-In** option appears when `Enable/Disable Onsite Arrival Check-in for Agents` property is enabled. For more information, see [Global domain configurations](t_ConfigureFieldService.md) and [Onsite arrival and check-in](../../field-service-management/reference/onsite-arrival-and-check-in.md).
3.  Open the task record and do either of the following to mark your arrival or check-in at the work location.

    -   To perform any task related activities before starting work, click **Check-In**

        **Note:** At this stage, a notification is sent to the customer, informing them that the agent has arrived on-site and is ready to begin the work. For more information, see [Customer notifications for work order tasks](../../field-service-management/concept/Customer-notification-work-order-tasks.md). The substate **Onsite Arrival** is automatically set, indicating that you have reached your travel destination for the work order task.

    -   To start work directly and check-in automatically, click **Start Work**.
    -   The **Actual work start** field is automatically updated with the current system time, marking the beginning of the task.
    -   The work order task's state changes to **Work In Progress** to reflect that the task is actively being worked on.
    -   The **Actual travel duration** field is automatically calculated by the system. It measures the time difference between the **Actual travel start** and **Actual onsite arrival** timestamps, unless manually set.
    -   If the system properties `work.management.allow.auto.timecard` and `work.management.allow.travel.task.timecard` are enabled, time cards are automatically created. These time cards capture the duration of your work on the task, including the task's travel time.
    -   The generated time card for the task's travel duration is stored under the **Time Worked** related list. This provides a record of the time spent traveling to the task location.
4.  When the work is done, open the task record and add a work note describing what you did to complete the task.

5.  Click **Close Complete** under **Related Links**.

    The system redraws the map and removes the icon for the completed task. The next accepted task in the route is relabeled as number **1**. The agent icon appears at the site of the last location update.


## Result

The cumulative amount of time worked on the task is captured in the **Actual Work Duration** field. This total includes the time you started working on the task until you closed work on the task, excluding any time paused on the work.

**Parent Topic:**[Manage tasks on the map](../concept/c_ManageTasksOnTheMap.md)

