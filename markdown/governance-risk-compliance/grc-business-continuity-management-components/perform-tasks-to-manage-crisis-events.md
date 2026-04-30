---
title: Structured workflows for crisis events
description: Perform the structured workflows to manage a crisis event in Business Continuity Workspace \(also known as BCM Configurable Workspace\).
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Structured workflows for crisis events

Perform the structured workflows to manage a crisis event in Business Continuity Workspace \(also known as BCM Configurable Workspace\).

Typically, the BCM program manager performs the following tasks to respond to a crisis event:

-   Create a crisis event. For more information, see [Start a crisis event](../task/start-crisis-event-in-uib-ws.md).
-   Add an asset and plan to the crisis event. For more information, see [Track impacted assets and add related plans](../task/add-asset-plan-to-crisis-event-uib-ws.md).
-   Add an event task to the crisis event. For more information, see [Add a task to the crisis event](../task/add-event-task-to-crisis-event.md).
-   Submit the event task for the exercise event. For more information, see [Request an approval and approve the crisis event](../task/submit-event-task-for-crisis-event-uib-ws.md).

## Additional information on Crisis events

-   For information on the **Crisis events** tab in the Home page, see [Home page view](home-page-uib-ws.md).
-   For information on the threats, feeds, and alerts in the Crisis map interface, see [Crisis map interface](threats-feeds-alerts-crisis-map.md).
-   For information on the administrative tasks in the Crisis map interface, see [Setup for Crisis map](crisis-map-admin-tasks.md).
-   For information on the crisis events, see [Crisis events](crisis-management-uib.md).

## Bulk editing of tasks from the Event tasks related list

Starting with version 6.1.x of the Business Continuity Management application, users who have editing access to the event record can now perform bulk edits on tasks directly from the Event tasks related list. This feature is beneficial for users who manage multiple event tasks simultaneously.

In the recovery tasks list, users with the necessary edit permissions can modify the following fields simultaneously:

-   **State**
-   **Assigned to**
-   **Actual start**
-   **Actual end**
-   **Assigned group**

Once an event is initiated, these users can also modify the state of an event task either from the list view or the form view. The process for updating the state of an event task from the list view is demonstrated in the following example. If a state transition is not allowed, an error message is displayed to indicate that the update is invalid.

![Bulk edits.](../image/transition-of-the-states.png)

The following table details the permitted state transitions for an event task.

|Transition from state|Pending state|Open state|Work In Progress state|Closed Complete state|Closed Incomplete state|Closed Skipped state|Closed Failed state|
|---------------------|-------------|----------|----------------------|---------------------|-----------------------|--------------------|-------------------|
|Pending|No|Yes|No|No|No|Yes|No|
|Open|No|No|Yes|No|No|Yes|No|
|Work In Progress|No|Yes|No|Yes|Yes|Yes|Yes|
|Closed Complete|No|Yes|No|No|No|No|No|
|Closed Incomplete|No|Yes|No|No|No|No|No|
|Closed Skipped|No|Yes|No|No|No|No|No|
|Closed failed|No|Yes|No|No|No|No|No|

**Note:** All changes to state transitions and updates to the start or end dates are listed in the Task activity log.

Consider the following key details about the state transitions of an event task.

1.  The event task can only be opened from the **Closed complete** state.
2.  Once the event task moves to the **Open** state, users of the event task can edit it further.
3.  The task can then be moved from the **Open** state to the **Closed Skipped** state.
4.  Only users with access to the event can reopen the event task. While recovery task members can change the status of the event task, they cannot reopen it.

The following table summarizes the UI actions available for an event task and their corresponding states:

|UI action|State of the event task|Notes|
|---------|-----------------------|-----|
|**Trigger**|**Pending**|This condition is applicable only when an event has been started.|
|**Skip task**|**Pending**, **Open**, **Work in progress**|-|
|**Work in progress**|**Open**|-|
|**Closed complete**|**Work in progress**|-|
|**Closed incomplete**|**Work in progress**|-|
|**Closed failed**|**Work in progress**|-|
|**Re-trigger as a manual task**|**Closed**|-|
|**Re-trigger automation**|**Work in progress**, **Closed**|This condition is applicable for an automated task only.|

If a task is mistakenly closed, users of the event task can reopen it to make the required edits, ensuring the recovery process remains accurate and complete.

## Updating the event task as a recovery task member

Generally, recovery task members update the status of event tasks. Although they do not have access to the event page or workspace, they can navigate to **My Recovery Tasks** in the instance to access the recovery task. By modifying the UI action, they can change the status of the event task, as demonstrated in the example.

![Update the state of the event task.](../image/updating-ui-states-for-event-task-ui16.png)

For instance, when members of the recovery task mark the task as Closed complete, all fields on the form become locked. This implies that while members of the recovery task cannot modify the fields, they are still able to add activity notes. Only users who have access to the event task can edit the fields on the form.

For information on importing the automated task in an event, see [Import automated tasks and start an event](../task/import-the-automated-task-in-an-event.md).

-   **[Start a crisis event](../task/start-crisis-event-in-uib-ws.md)**  
Report a crisis event in the BCM Configurable Workspace. A crisis event is any significant disruption that threatens business operations. The BCM Configurable Workspace enables you to create crisis records, classify severity levels, set priorities, assign response teams, and document initial actions.
-   **[Using nested plans](creating-nested-plan-in-event.md)**  
Configure a system property to control activated plan levels in an event. The system automatically creates nested plans within an event, reducing the manual effort of adding plans and improving system performance. You can also add dependencies between multiple activated plans by updating the **Dependencies** field in the event tasks.
-   **[Track impacted assets and add related plans](../task/add-asset-plan-to-crisis-event-uib-ws.md)**  
Track the impacted assets and add a related plan during a crisis event. You can monitor the assets and plans for the crisis event in BCM UIB Workspace. You can then recover your assets in the planning stage.
-   **[Add a task to the crisis event](../task/add-event-task-to-crisis-event.md)**  
Add a task to the crisis event in BCM UIB Workspace. You can then monitor and complete the required actions to respond to the crisis event.
-   **[Import automated tasks and start an event](../task/import-the-automated-task-in-an-event.md)**  
Import the automated task from the business continuity plan in an actual event. Utilizing automated tasks during an actual event enhances efficiency and reduces response time for users.
-   **[Creating action items in crisis events](creating-action-items-in-crisis.md)**  
Starting with BCM release 9.0.x, crisis managers can create action tasks for recovery members or teams anytime during a crisis event or exercise, as long as the event remains open. Crisis managers can create these tasks on the fly without mapping them to event assets or recovery plans. These action tasks are also not included in the event recovery timeline.
-   **[Create a similar tasks group in a crisis](../task/create-sim-tasks-grp-crisis.md)**  
Identify and group similar or duplicate tasks related to a crisis event using the **Similar tasks groups** tab. Grouping similar tasks helps you to optimize event task management and minimize redundant work.
-   **[Request an approval and approve the crisis event](../task/submit-event-task-for-crisis-event-uib-ws.md)**  
Approve the crisis event in BCM UIB Workspace.

**Parent Topic:**[Managing BCM workflow tasks](manage-bcm-with-uib-workspace.md)

