---
title: Add a task to the crisis event
description: Add a task to the crisis event in BCM UIB Workspace. You can then monitor and complete the required actions to respond to the crisis event.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add a task to the crisis event

Add a task to the crisis event in BCM UIB Workspace. You can then monitor and complete the required actions to respond to the crisis event.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

Users with an edit access to the event record can edit the fields in the recovery tasks list simultaneously:

-   **State**
-   **Assigned to**
-   **Actual start**
-   **Actual end**
-   **Assigned group**

For more information, see [Structured workflows for crisis events](../concept/perform-tasks-to-manage-crisis-events.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Crisis events** &gt; **Pending** and select the crisis event in the list.

3.  Select the **Event tasks** tab.

    **Note:** For the crisis events, the event type is **Actual**.

    When you add or update the plan to the crisis event, the related plans, assets, and event tasks that are associated with the plan also get pulled into the event.

4.  To add an ad-hoc task to the event, select **New ad-hoc task**.

    **Note:** An ad-hoc task is added to the crisis event so that you can take corrective actions for the crisis event. When you add an ad-hoc task to the crisis event that is in the **Work in progress** state and if the activated plan is in the **Work in progress** state, the tasks will be in the **Open** state. If the activated plan is the **Pending** state, the task will be in the **Pending** state.

    For more information on the fields in the New Event Task form, see [Create New Event Task form](../reference/create-new-event-task-form-uib-ws.md).

    **Note:** You cannot create an ad-hoc task for the activated plans that are in **Closed Complete** or **Closed Incomplete** state.

5.  To start the crisis event, select **Start Event**.

    After you start the event, the event state is updated to **Work in Progress**.

    **Note:** If the event task has a circular dependency, you have to trigger the tasks manually for this event.

6.  Select the first task and select **Trigger**.

7.  Complete all the activated plans of the event tasks for the crisis event and select **Submit for Approval**.

8.  To generate a PDF, select **Generate PDF**.

    If you have edit access to the crisis event, you can save a copy of the event in PDF format to your local hard drive.

    **Note:** By default, the PDF is generated and attached after the event is closed.

9.  Navigate to the **Results** section on the **Details** tab and update the **Actual start** and **Actual end** dates for the event task.

10. Update the assignment fields, if necessary.

11. Enter any event task-related information in the **Work notes** field of the **Activity** section.

12. Select **Save**.

13. Select the refresh icon \(![Refresh icon.](../image/RefreshAlertsIcon.png)\) to display the updated state of the asset or plan, and the actual time taken to recover the asset.


**Parent Topic:**[Structured workflows for crisis events](../concept/perform-tasks-to-manage-crisis-events.md)

