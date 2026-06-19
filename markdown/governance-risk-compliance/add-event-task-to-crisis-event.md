---
title: Add a task to the crisis event
description: Add a task to the crisis event in BCM UIB Workspace. You can then monitor and complete the required actions to respond to the crisis event.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-event-task-to-crisis-event.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Structured workflows for Crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
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

For more information, see [Structured workflows for Crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/perform-tasks-to-manage-crisis-events.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Crisis events** &gt; **Pending** and select the crisis event in the list.

3.  Select the **Event tasks** tab.

    **Note:** For the crisis events, the event type is **Actual**.

    When you add or update the plan to the crisis event, the related plans, assets, and event tasks that are associated with the plan also get pulled into the event.

4.  To add event tasks in bulk from a task template group, on the **Event tasks** tab select **More Actions** &gt; **Add groups**.

    The **Select task template groups** dialog opens as a two-step wizard. In step 1, select one or more groups. In step 2, select the activated plan that the new event tasks should be associated with. Step 2 is skipped when you invoke **Add groups** from the **Event tasks** tab of an activated plan, because the activated plan is already known.

    The dialog filters groups by **Active** = true. Filters that are currently applied to the **Event tasks** list — for example, **Phase** = **Recovery validation** — are applied as default values on the created tasks. Phase values that are already set on a task template take precedence over the list filter.

    \[Omitted image "event-task-more-actions-menu.png"\] Alt text: Crisis event Event tasks tab More Actions menu showing Add groups, Add tasks, Export to Excel, and New ad-hoc task.

    \[Omitted image "exercise-event-select-task-template-groups-step-one.png"\] Alt text: Select task template groups wizard with step 1 active and step 2 upcoming.

5.  To add individual task templates without a group, on the **Event tasks** tab select **More Actions** &gt; **Add tasks**.

    The **Select task templates** dialog uses the same two-step wizard and the same filter rules as **Add groups**.

    \[Omitted image "select-task-templates-dialog.png"\] Alt text: Select task templates dialog listing recovery task templates with Active status.

6.  After the bulk add completes, wait for the auto-refresh banner to dismiss, or select **Refresh** to refresh the **Event tasks** list manually.

    The **Event tasks** list does not auto-refresh row by row. Instead, the banner **The event tasks are updated. Select Refresh to see updated data. List will auto-refresh once all tasks are created.** is displayed while the system creates the tasks. About ten seconds after the last task is created, the list refreshes once. This avoids repeated refreshes on event tasks lists that contain a large number of rows. For more information, see [Event task creation progress in exercise and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-event-task-template-progress.md).

    \[Omitted image "event-tasks-auto-refresh-banner.png"\] Alt text: Yellow banner stating the event tasks are updated with a Refresh button.

7.  To save a set of crisis event tasks as a reusable task template group, select the tasks in the **Event tasks** list and then select **Save as group** &gt; **Save tasks**.

    To append them to an existing group, you can select **Save as group** &gt; **Add to group**. Event tasks are saved as task templates that can later be applied from a crisis event, an exercise event, an activated plan, a plan, a loss scenario, or a recovery strategy. The element definition associated with each event task is preserved on the resulting templates so element-definition filtering still applies when the group is reused.

    \[Omitted image "save-as-group-create-dialog.png"\] Alt text: Create task template group modal showing You selected 2 task\(s\) and the Group name field.

8.  To add an ad-hoc task to the event, select **New ad-hoc task**.

    **Note:** An ad-hoc task is added to the crisis event so that you can take corrective actions for the crisis event. When you add an ad-hoc task to the crisis event that is in the **Work in progress** state and if the activated plan is in the **Work in progress** state, the tasks will be in the **Open** state. If the activated plan is the **Pending** state, the task will be in the **Pending** state.

    For more information on the fields in the New Event Task form, see [Create Event Task form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-event-task-form-uib-ws.md).

    **Note:** You cannot create an ad-hoc task for the activated plans that are in **Closed Complete** or **Closed Incomplete** state.

9.  To start the crisis event, select **Start Event**.

    After you start the event, the event state is updated to **Work in Progress**.

    **Note:** If the event task has a circular dependency, you have to trigger the tasks manually for this event.

10. Select the first task and select **Trigger**.

11. Complete all the activated plans of the event tasks for the crisis event and select **Submit for Approval**.

12. To generate a PDF, select **Generate PDF**.

    If you have edit access to the crisis event, you can save a copy of the event in PDF format to your local hard drive.

    **Note:** By default, the PDF is generated and attached after the event is closed.

13. Navigate to the **Results** section on the **Details** tab and update the **Actual start** and **Actual end** dates for the event task.

14. Update the assignment fields, if necessary.

15. Enter any event task-related information in the **Work notes** field of the **Activity** section.

16. Select **Save**.

17. Select the refresh icon \(\[Omitted image "RefreshAlertsIcon.png"\] Alt text: Refresh icon.\) to display the updated state of the asset or plan, and the actual time taken to recover the asset.


**Parent Topic:**[Structured workflows for Crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/perform-tasks-to-manage-crisis-events.md)

