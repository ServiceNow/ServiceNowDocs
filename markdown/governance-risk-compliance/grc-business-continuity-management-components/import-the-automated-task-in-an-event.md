---
title: Import automated tasks and start an event
description: Import the automated task from the business continuity plan in an actual event. Utilizing automated tasks during an actual event enhances efficiency and reduces response time for users.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Import automated tasks and start an event

Import the automated task from the business continuity plan in an actual event. Utilizing automated tasks during an actual event enhances efficiency and reduces response time for users.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **crisis events** &gt; **Pending** and select **New**.

    The **Create New Event** form is displayed.

3.  In the **Details** tab of the **Create New Event** form, fill in the required fields.

    **Note:** For a crisis event, the event type is **Actual**.

    For more information on the fields, see [Create Crisis Event form](../reference/create-crisis-event-ref-form.md).

4.  Navigate to the Planning list in the Workspace view and select the plan associated with the event.

    When you select the plan, the associated tasks are pulled into the event. The tasks are displayed on the **Event tasks** tab. When the tasks displayed on the **Event tasks** tab have a dependency between them, they are executed in a sequential order.

5.  Select **Start event**.

    Upon initiating an event, the event tasks that do not have any dependency between them are executed. When a task is completed, the subsequent tasks that depend on it are executed. For example, when a task transitions to the **Closed incomplete** or **Closed failed** state, you have the option to select the task and review its activity details. If an error message is displayed on the screen, you can examine it to identify the issue and take appropriate corrective measures. For instance, if the error message indicates that the code variable must be a positive value, you can update the code variable accordingly.

    If the task transitions to the **Closed failed** state, then its dependent tasks are not triggered. In the event that a task is in the **Closed incomplete** or **Closed failed** state, an email notification is sent to the backup assignee, informing them that the automated flow has encountered an error and manual intervention is necessary from the backup assignee.

6.  Select **Re-trigger automation**.

    The automated flow is triggered for execution once more.

7.  If the automated flow fails again, select **Re-trigger as a manual task**.

    The task transitions to the **Open** state.

    1.  Update the event task and select **Work in progress**.

    2.  Select **Closed complete**.

        You have the option to manually update the event task. Once you mark the task as **Closed complete**, the subsequent event task is automatically triggered. If the next task is a manual task, its assigned user can proceed to complete the workflow for the event task.

8.  Select **Save**.

    The event task is then saved within the instance.


**Parent Topic:**[Structured workflows for crisis events](../concept/perform-tasks-to-manage-crisis-events.md)

