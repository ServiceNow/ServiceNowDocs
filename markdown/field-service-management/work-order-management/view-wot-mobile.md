---
title: Plan your work order tasks
description: Plan how to execute tasks assigned to you using the mobile app. You can prioritize by accessing SLAs and call customers directly from the app.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Prioritizing on ServiceNow Agent, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Plan your work order tasks

Plan how to execute tasks assigned to you using the mobile app. You can prioritize by accessing SLAs and call customers directly from the app.

## Before you begin

Role required: wm\_agent or wm\_dispatcher

## About this task

The task list displays the following information for each work order task:

-   The work order task number.
-   The short description of the work order task.
-   Company for which the work order task is being executed.
-   Asset details appear only if there’s an asset associated with the work order task.
-   Location where the work order task is being executed.
-   The work order task state.
-   Scheduled start date and time for work order task to be executed.
-   For a work order task, if the parent work order has an account, navigate from the work order screen and drill down the account details to see primary contact details, related cases, assets, contracts, and entitlements.

    **Note:** The logged-in user must have sn\_customerservice.customer\_data\_viewer role to drill down and view the account details from work order.

-   For a work order task, if the parent work order has been initiated from a case, navigate from the work order screen and drill down see the case details.

    **Note:** The logged-in user must have the case\_viewer role to navigate to the case screen from work order and sn\_customerservice.proxy\_contact role to add work notes and comments to the **Case Activity Stream**.


## Procedure

1.  Open the ServiceNow Agent application.

2.  Tap **My Work**.

    **Note:** Tap **Quick Actions** and update your status to **ON Shift** to get identified as you are on your shift time.

3.  Perform one of the following actions.

    |To|Complete these steps|
    |---|--------------------|
    |**Search for work order and work order task**|Enter a keyword to search for work orders and work order tasks.|
    |**View the work order tasks assigned to you**|Tap **My Tasks**. You can view all upcoming tasks based on the schedule start date. To view all tasks, tap **See All**.|
    |**View work order tasks for your assignment group**|In the **My Group Tasks** section, view upcoming tasks for your assignment group. To view all tasks, tap **See All**.|

    The list displays all tasks scheduled to start before the end of next week.

    **Note:** You can also [view all work orders for an asset](identify-defect-asset-mobile-app.md).

4.  Select a work order task to view details for the task.

5.  Edit a work order description.

    1.  Tap the overflow icon and select **Edit**.
    2.  Do the following: To edit the task short description, tap the **Short Description** field, to make the necessary edits and select the back icon to go back to the **Edit** screen.
    3.  To edit the task description, tap the **Description** field, enter a description for the task and, select the back icon to go back to the **Edit** screen.
    4.  Perform one of the following actions:
        -   On an iOS device, tap **Submit**.
        -   On an Android device, tap the send icon.
6.  View the SLA for the work order that the task is associated with.

    1.  Tap the work order number.
    2.  Select the work order to view the details.
    3.  Tap **Related**.
    4.  Tap **Task SLA**.
    The screen displays all SLAs related to the work order.

    Tap the arrow at the top-left corner to go back to the work order.

7.  Call the caller identified on the work order.

    1.  Select the **Details** tab.
    2.  Select the caller identified in the **Caller** field.
    3.  Swipe the caller record to the left and select **Call** to call.
    Tap the arrow at the top-left corner to go back to the work order.


**Related topics**  


[Field Service Management SLAs](../../planning-and-policy/concept/c_FieldServiceAutomationSLAs.md)

[Working on tasks when your mobile device is offline](../concept/work-offline-fieldservice-mobile.md#)

