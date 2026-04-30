---
title: Configure the Scheduled state
description: Administrators can optionally enable the Scheduled state flow for work orders and work order tasks. By configuring these settings, you can control when and how tasks are dispatched to technicians.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work order tasks, Work orders and tasks, Configure, Field Service Management]
---

# Configure the Scheduled state

Administrators can optionally enable the Scheduled state flow for work orders and work order tasks. By configuring these settings, you can control when and how tasks are dispatched to technicians.

## Before you begin

Role required: wm\_admin

## Procedure

1.  Navigate to **Field Service** &gt; **Administration** &gt; **Configuration**.

2.  Select the **Assignment** tab.

3.  Select **Use scheduled state**.

    **Note:** When **Dispatch queue** is turned off, **Use scheduled state** is automatically turned off. ​When **Dispatch queue** is enabled, **Use scheduled state** is NOT automatically enabled.

4.  Select **Save**.

5.  Navigate to **Field Service** &gt; **Administration** &gt; **Properties**.

6.  Select a **Mode setting to activate the scheduled state**.

    -   **Duration**

        This mode updates the state of tasks from **Scheduled** to **Assigned** when the start threshold \(in hours\) is reached.

    -   **Number of tasks**

        This mode controls the **Number of tasks** that are in the **Scheduled** state before they’re assigned.

7.  Modify the corresponding property to define when a work order task should be dispatched \(moved from Scheduled to Assigned\).

    -   For **Duration** mode:
        -   Scroll down to **Update task state from Scheduled to Assigned when the scheduled start is within specified hours from current time**.
        -   Default value: 12 hours
        -   Example: If you set the **Duration** mode to 12 hours, any tasks scheduled to start within the next 12 hours are assigned. Tasks scheduled to start after this period remain in the **Scheduled** state.
    -   For **Number of tasks** mode:
        -   Scroll down to **Count of tasks that are in assigned state before they are scheduled**.
        -   Default value: 1
        -   Example: If you set the **Number of tasks** mode to 1, only one task will be assigned to a technician at a time, while all remaining tasks will stay in the **Scheduled** state.
    **Note:** The Scheduled State Processor will move tasks to the **Assigned** state whenever the number of **Assigned** tasks is less than the property value. By default, only tasks that are already scheduled can be assigned.

8.  Select **Save**.

9.  If you selected, **Number of tasks** mode, navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

10. In the **Name** search, type 'Assign number of tasks by number of tasks' and press enter.

11. Click **Assign scheduled tasks by number of tasks** to open the record.

12. Select the **Active** option to enable

13. Enter the desired interval in the **Repeat interval** field.

    By default, the repeat interval is set to 5 minutes.

14. Select **Update**.


## Result

-   On a work order form, the following occurs:
    -   A new state Scheduled appears between Ready For Dispatch and Assigned if qualification isn’t enabled.
    -   A new state Scheduled appears between Qualified and Assigned if qualification is enabled.
-   On a work order task form, a new state Scheduled appears between Pending Dispatch and Assigned.

**Note:** If you turn the **Use scheduled state** property off, a warning appears indicating that tasks have moved from Scheduled to Assigned. Consequently, all work order tasks that are in the Scheduled state are moved to the Assigned state.​

