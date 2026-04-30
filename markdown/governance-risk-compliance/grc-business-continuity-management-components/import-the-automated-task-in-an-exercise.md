---
title: Import plans and recovery tasks
description: Import the business continuity plans and associated recovery tasks in the event. Using automated tasks during an exercise enhances efficiency and reduces response time for users.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Import plans and recovery tasks

Import the business continuity plans and associated recovery tasks in the event. Using automated tasks during an exercise enhances efficiency and reduces response time for users.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Exercises** &gt; **Pending** and select **New**.

    The **Create New Event** form is displayed.

3.  Fill in the required fields in the **Details** tab.

    For more information on the fields, see [Create New Event Task form](../reference/create-new-event-task-form-uib-ws.md).

4.  Select the plan associated with the event from the Planning list in the Workspace view.

    -   **Enhanced plan management for events**

        When adding a plan to an event, the system can now automatically include downstream plans based on the main node configuration. This feature provides flexibility by offering two options:

        -   Pull in related plans: This is the existing functionality that brings in related plans associated with the added plan.
        -   Pull in downstream plans: This new option automatically adds downstream plans connected to the main node configuration, streamlining the process of managing complex recovery plans.
        Scenarios and considerations: The system evaluates various scenarios as described in this section:

        -   Adding or removing plans from an event.
        -   Adding assets, which may trigger the addition of related plans.
        -   Removing plans or assets and the associated downstream plans.
        User interface enhancements: A new UI action, **Add all plans related to asset**, is available on the Event Asset form, allowing you to easily add related plans to the event.

        By automating the inclusion of downstream plans, this feature enhances the efficiency and effectiveness of recovery planning and execution. It verifies that all relevant plans are considered and included in the event, reducing the risk of overlooking critical recovery steps.

    When you select the plan, its associated recovery tasks are pulled into the event. The tasks are then displayed on the **Event tasks** tab. When the tasks displayed on the **Event tasks** tab have a dependency between them, they are executed in a sequential order.

    Plan activation and task copying: When a plan is activated during an event, its associated recovery tasks are copied into event tasks. This includes the asset recovery level details. If the recovery progress is already complete, the **View progress** button may not be visible. The recovery tasks from the original plan are accurately replicated in the event tasks, maintaining the same step sequence. For instance, if steps 2, 3, and 4 were defined in the plan, they are copied over to the event tasks in the same order.


**Parent Topic:**[Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md)

