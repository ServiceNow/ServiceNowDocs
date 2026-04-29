---
title: View event details and monitor event task completion
description: View the event details and add impacted items to start an event.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Structured workflows for Exercise and Crisis Management, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# View event details and monitor event task completion

View the event details and add impacted items to start an event.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  To update an active exercise or crisis event from the Home page of the Business continuity workspace, click the link to the event record in the **Event** column of the **My exercises** section.

3.  To update the event from the lists view of the workspace, click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

4.  If the record is an exercise event and is in pending state, Click **Pending** link in the Exercises list.

5.  Click the link to the event record in the **Number** column.

6.  Review the event details in the **Details** tab.

    You can view and update all the details of an event. However, you cannot edit the event type.

    A crisis manager should be able to report a crisis event with the information provided in the details tab. For more information, see [Manage a crisis event](manage-crisis-event.md).

7.  Click the **Impacts** tab to add impacted items.

    To add a list of impacted items and activated plans to the event, see [Add impacted assets and plans to an event](associate-plan-task-event.md).

8.  Click **Event Tasks** tab.

    This tab appears for all crisis events but exercises that are of **Functional** type events only.

    The Plans section, which appears as a side panel, displays all the activated plans that are added to the event.

    When a plan is activated, all the recovery tasks where the scope is empty and tasks where the scope match with the impacted asset of the plan that is activated are added as event tasks for that activated plan.

    Each activated plan is an interactive card that shows you the number of assets that are in the process of being recovered and the number of event tasks that are completed for that activated plan. When you add an activated plan to the event task, all the recovery tasks of the plan are added as event tasks to the event.

    You can also create a task for the event that is not covered in any of the existing plans for the event as an ad hoc task.

    1.  Click an activated plan card to view the associated event tasks.

        The selected activated plan card is highlighted in green and displays all the event tasks for that plan in a grid on the right pane.

        If the plan is pre-grouped, then the event task is also pre-grouped. Use the first column of the grid, which is the task Group column, to view the pre-grouped event tasks.

        ![Grouping event tasks.](../image/EventTaskGrouping.png "Grouping event tasks")

        **Note:** If the activated plan refers to a different plan to recover a related asset, then all those related plans are listed below the main activated plan as **Related plans** in the left pane.

        For more information on the planning and execution of a recovery event, see [Data flow, planning, execution, and recovery of related plan assets in event](../concept/planning-execution-event-bcm.md).

    2.  To add an ad hoc task to the event, click the **Add ad hoc task** button.

        |Field|Description|
        |-----|-----------|
        |Short description|Brief note about the event task.|
        |Task ID|Defaults to the next number of existing event tasks for the plan.|
        |Assignment group|Group to which the event task is assigned.|
        |Assigned to|User or users from the Assignment group. If **Assignment group** field is empty, then select any user.|
        |Additional assignee list|Additional users.|
        |Impacted assets|Assets that are impacted for the event task.|
        |State|Defaults to **Pending** state.|
        |Dependencies|For tasks copied from plan level, dependencies are copied from plan recovery task. Dependencies cannot be added for ad hoc tasks.|
        |Description|Information about the event task.|
        |Activity|
        |Work notes|Information about the event task shared internally.|

    3.  Click **Save**.

        **Note:** You cannot create an ad hoc task for activated plans that are in **Closed Complete** or **Closed Incomplete** state.

    4.  To update an existing event task, click the ![Information icon.](../image/InformationIcon.png) of the task in the grid.

    5.  Update the **Actual start** and **Actual end** dates for the event task.

    6.  Update the assignment fields, if required.

    7.  Enter any event task related information in the **Work notes** field of the **Activity** section.

    8.  Click **Save**.

    Calculation of actual duration and total effort to recover an event asset:

    Actual duration to recover an event asset is calculated by `Actual end – Actual start of an event asset`

    -   the actual start of an event asset is the minimum start time of the event task executed for the event asset that is, event task that has the event asset as impacted asset. And the minimum start time of the activated plan without a task.
    -   the actual end of an event asset is the maximum end time of the event task executed for the event asset that is, event task that has the event asset as impacted asset. And the maximum end time of the activated plan without a task.
    Total effort of an event asset is calculated by rolling up the actual time taken by all the event tasks that are executed for the event asset that is, the impacted asset in event task that contains the event asset. And the total effort of all activated plans associated with the asset without a task.

    -   **Actual duration of an event task**

        The difference in time between the actual start and actual end time.

    -   **Actual duration of an activated plan with a task**

        The difference between the actual start and actual end of the activated plan, where

        -   the actual start of an activated plan is the minimum start time of the event task for that plan
        -   the actual end of an activated plan is the maximum end time of the event task for the plan
    -   **Actual duration of an activated plan without a task**

        The difference between the actual start and actual end of the activated plan.

    -   **Total effort of an activated plan with a task**

        Sum of the actual durations of all event tasks that belong to the plan.

    -   **Total effort of an activated plan without a task**

        The difference between the actual start and actual end of the activated plan.

    State transitions of an event task:

    -   **Open**

        When an event is started, its event tasks that do not have a dependent recovery task move to the **Open** state.

    -   **Pending**

        The event tasks that are dependent on other recovery tasks are in **Pending** state when the event is started. After the dependent tasks are closed, the parent event task moves to **Open** state.

    -   **Skip Task**

        This button is available only if you have logged in as a BCM program manager. **Skip** button appears when the task is in **Pending** or **Open** state and the event must be in Work in Progress state. Clicking **Skip Task** moves the task to **Closed Skipped** state. The actual start and actual end time at this state are blank.

    -   **Trigger**

        This button is available only if you have logged in as a BCM program manager. The task is in **Pending** state. Clicking **Trigger** moves the task to **Open** state irrespective of its dependencies.

    -   **Work In Progress**

        The task is in **Open** state. Clicking **Work In Progress** button moves the task to **Work in Progress** state. You can update the actual start time of the task in the **Actual start** field in this state. If you do not update the actual start, the current date and time is recorded as the actual start time. The next available options are **Closed Complete** or **Closed Incomplete** state.

    -   **Closed Complete**

        The task is closed and complete. Actual end time of the task is recorded in the **Actual end** field. If you do not update the actual end, the current date and time is recorded as the actual end time.

    -   **Closed Incomplete**

        Actual end time of the task is recorded in the **Actual end** field. If you do not update the actual end, the current date and time is recorded as the actual end time. Update necessary information in the **Work notes** field and save the task.


