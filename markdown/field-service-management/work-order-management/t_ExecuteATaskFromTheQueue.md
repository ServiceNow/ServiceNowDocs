---
title: Execute a task from the queue
description: If the agent task map is not used in your organization, you can manage assigned tasks from the task queue.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Execute work order tasks, Updating task status in web interface, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Execute a task from the queue

If the agent task map is not used in your organization, you can manage assigned tasks from the task queue.

## Before you begin

Role required: wm\_agent or wm\_dispatcher

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Agent** &gt; **Assigned to me**.

2.  When parts are delivered or picked up from a stockroom, acknowledge the delivery of parts.

    1.  Open a work order task.

    2.  In the **Transfer Orders** related list, open the transfer order.

    3.  Open the related transfer order and access a record in the **Transfer Order Lines** list.

    4.  Acknowledge the delivery by clicking **Receive** or **Deliver** based on the part's location.

3.  Click **Start Travel** when initiating travel for the task.

    **Note:** If the **Scheduled travel start** field is completed, this step is mandatory.

    -   Upon clicking **Start Travel**, a notification email and SMS are sent to the customer, signaling the agent's arrival.
    -   A sub-state, **On Route**, is automatically set, indicating the commencement of travel for the work order task.
    -   The option to **Check-In** appears when `Enable/Disable Onsite Arrival Check-in for Agents` property is enabled. For more information, see [Global domain configurations](t_ConfigureFieldService.md) and [Onsite arrival and check-in](../../field-service-management/reference/onsite-arrival-and-check-in.md)
4.  Open the work order task and do either of the following.

    -   Select **Check-In** to notify the customer of your arrival and perform any pre-work activities.

        **Note:** At this stage, a notification is sent to the customer, informing your on-site arrival and ready to begin the work. The substate **Onsite Arrival** is automatically set, indicating that you have reached your travel destination for the work order task. Additionally, the check-in status is stored in the database.

    -   Select **Start Work** to automatically check-in and commence work directly.
    -   The **Actual work start** field is automatically updated with the current system time, marking the beginning of the task.
    -   The work order task's state changes to **Work In Progress** to reflect that the task is actively being worked on.
    -   The **Actual travel duration** field is automatically calculated by the system. It measures the time difference between the **Actual travel start** and **Actual onsite arrival** timestamps, unless manually set.
    -   The generated time card for the task's travel duration is stored under the **Time Worked** related list. This provides a record of the time spent traveling to the task location.
    -   If the system properties `work.management.allow.auto.timecard` and `work.management.allow.travel.task.timecard` are enabled, time cards are automatically created. These time cards capture the duration of your work on the task, including the task's travel time.
5.  When work is complete, [record any asset usage](t_RecordAssetUsage.md).

6.  Add a description of the work you did to the **Work notes** field.

    This is required to close the task.

7.  [Close the task](t_CloneAWorkOrderTask.md).


## Result

The cumulative amount of time worked on the task is captured in the **Actual Work Duration** field. This total includes the time you started working on the task until you closed work on the task, excluding any time paused on the work.

**Parent Topic:**[Execute work order tasks](../concept/c_ExecuteWorkOrderTasks.md)

**Related topics**  


[Customer notifications for work order tasks](../../field-service-management/concept/Configuring-cust-exp.md#)

