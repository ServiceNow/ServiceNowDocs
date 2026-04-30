---
title: Start an event
description: To initiate an event, first pull the relevant plans into the event, and then review the event tasks listed in the Event tasks tab.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-10-09"
reading_time_minutes: 6
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Start an event

To initiate an event, first pull the relevant plans into the event, and then review the event tasks listed in the **Event tasks** tab.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** and select the event from the list view.

2.  To start the exercise, select **Start Event**.

    Beginning with the Xanadu release, you can monitor the activated plans linked to an exercise, that are now displayed in an **Open** state, instead of the **Work in Progress** state. The **Open** state displays an accurate status of the activated plan. The actual duration of the activated plan is calculated from its start date to the end date. When the tasks linked to an activated plan are updated to the **Work in Progress** state, the status of the activated plan gets updated to **Work in Progress**.

3.  Update the state of the event task to **Work in Progress**.

    When you start an event task in an activated plan and update its state to **Work in Progress**, the status of the activated plan is also updated to **Work in Progress**. The condition for the activated plan to move into **Work in Progress** is that work starts on at least one of the event tasks. Until then, all the activated plans are still in the **Open** state.

    Whenever the state of an activated plan changes from Open to **Work in Progress**, the actual start date is recorded in the **Actual start** field. When all event tasks are completed, the actual end is calculated and recorded in the **Actual end** field. Based on the actual start and actual end, the actual time taken is recorded in the **Actual time taken** field. The time required to complete each task is submitted and stamped in the **Total effort** field in the activated plan.![Total effort for the plan.](../image/total-effort.png)

    You can edit multiple recovery tasks at once.

    A message is displayed that the event task has a circular dependency. You have to trigger the tasks manually for this event.

    Upon initiating an event, the event tasks that do not have any dependency between them are executed. When a task is completed, the subsequent tasks that depend on it are executed. For example, when a task transitions to the **Closed failed** state, you have the option to select the task and review its activity details. If an error message is displayed on the screen, you can examine it to identify the issue and take appropriate corrective measures. For instance, if the error message indicates that the code variable must be a positive value, you can update the code variable accordingly.

    If the task transitions to the **Closed failed** state, then its dependent tasks are not triggered. An email notification is sent to the backup assignee, informing them that the automated flow has encountered an error and manual intervention is necessary from the backup assignee.

4.  To update the dependencies manually, select **Update dependencies**.

    A UI message is displayed that the dependencies are being updated.

5.  To re-trigger as a manual task, select **Re-trigger as a manual task**, if the automated flow fails again.

    You can select **Re-trigger as a manual task**, if the automated flow fails again. The task transitions to the **Open** state.

    1.  Update the event task and select **Work in progress**.

    2.  Mark the task as **Closed complete**.

        Select one of the complete states for the event task and mark it as complete.

        You can update the event task manually by selecting one of these Complete states:

        -   **Closed incomplete**
        -   **Closed complete**
        -   **Closed skipped**
        If the event task is in the **Closed failed** state, then the event task is not considered as complete.

        ![Closed states.](../image/event-task-closed-states.png)

        Once you mark the task as complete, the subsequent event task is automatically triggered. If the next task is a manual task, its assigned user can proceed to complete the workflow for the event task.

        **Note:** Once an event task is in the **Closed complete** state, its phase cannot be changed. However, if you re-trigger it as a manual task, you can modify its phase.

6.  Check the state of the assets in the event.

    The example shows that the Facebook asset is partially recovered as the partially recovered tasks of Facebook asset are completed, but the Photoshop asset is still not recovered because both its partial and full recovery tasks remain incomplete.

    ![Assets.](../image/event-asset-par-recovered.png)![Plan.](../image/event-asset-another-activated-plan.png)

    For an asset to move to partially recovered as shown in the example or recovered, you must close all the related tasks. When all partially recovered tasks are completed, the asset moves to the partially recovered state.

    ![Assets are in the recovered state.](../image/event-assets-par-recovered.png)

    **Note:** To mark an event asset as recovered, you don't need to complete the tasks marked as "partially recovered." Completing all tasks with the "recovered" status moves the asset to the "recovered" status. This simplifies the process by focusing only on tasks designated as requiring full recovery.

    If no specific asset recovery level is chosen, the asset is considered as "Recovered" only after all associated tasks are completed.

    The example shows the assets that are not recovered.

    ![Asset not recovered.](../image/event-task-not-recovered.png)

    The example shows that step 4 is associated with the "Photoshop" asset and it is open.

    ![Event task with open state.](../image/event-task-state-open.png)

    Once you complete that open task \(Step 4 in the example\) and refresh the assets, both assets including the "Photoshop" asset are in the Recovered state.

    ![Recovered assets.](../image/event-asset-recovered.png)

    If a task is retriggered manually during this process, the asset recovery level reverts to its previous level. Any progress made in the recovery process is undone, and the asset is moved back to its prior recovery status.

    **Note:** Once you start an exercise, you cannot delete an event task or update its state to the Pending state.

7.  Add the actual start, actual end, and result in the Results section of the form and select **Save**.

    **Note:**

    If an asset is recovered with the completion of an earlier event task, such as step 4 in the example, the actual start time and actual end time are calculated until the end of the last event task in the plan \(step 6 in this example\).

    ![Event tasks.](../image/event-task-time-taken.png)

    To provide more control over time calculations, the "Don’t include this task in time calculation" column is introduced in recovery and event tasks. It enables you to exclude specific steps. In this example, if Steps 5 and 6 are marked to be excluded from the time calculation, the system calculates the time up to Step 4 only. This flexibility enables you to customize the time calculation according to your requirements.

    Verify that all plans and tasks are closed before submitting the event for an approval.

8.  Update the **Actual start** and **Actual end** dates for the event task the **Results** section on the **Details** tab.

9.  Update the assignment fields as necessary.

10. Enter event task-related information in the **Work notes** field of the **Activity** section.

11. Select **Save**.

12. To generate a PDF, select **Generate PDF**.

    If you have edit access to the crisis event, you can save a copy of the event in PDF format to your local hard drive.

    **Note:** By default, the PDF is generated and attached after the event is closed.

13. Select the refresh icon \(![Refresh icon.](../image/RefreshAlertsIcon.png)\) to display the updated state of the asset or plan, and the actual time taken to recover the asset.


## What to do next

To request an approval, see [Request an approval and approve the event](submit-an-event-task-uib-ws.md).

**Parent Topic:**[Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md)

