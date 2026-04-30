---
title: Place a change request on hold
description: You can put a change request on hold to get additional information for the created change request.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Process a change request, Using Change Management, Change Management, IT Service Management]
---

# Place a change request on hold

You can put a change request on hold to get additional information for the created change request.

## Before you begin

The following plugins need to be activated to avail the synchronization of the **On Hold** functionality between change task and change request:

-   Change Management — Core \[com.snc.change\_management\]
-   Change Management — State Model \[com.snc.change\_management.state\_model\]

Roles required: itil, admin, sn\_change\_write, or change manager

## About this task

Change tasks inherit some state conditions from the parent change request they are related to. When a change request is placed on hold, these conditions are applied to it:

-   If the change is waiting for approval, the pending approvals are marked **No Longer Required**. When the change request is no longer **On Hold**, the pending approvals are reinstated and are **Awaiting approval**.
-   The change can progress only to the **Canceled** state while it is **On Hold**.
-   If a change request is canceled while it is **On Hold**, then its **On Hold** flag is set to **false** so the change cannot be canceled and still be **On Hold**.
-   If the change request is set to **On Hold**, the value of the **On Hold** field for all the active change tasks for that change request is set to **true** and the **On hold reason** is copied from the change request to the change tasks.
-   If you clear the **On Hold** check box in a change request, the **On Hold** field for all the active change tasks for that change request is set to **false** and the **On hold reason** is cleared from the change tasks.
-   If the change request is canceled, all the active change tasks related to that change request are also canceled.
-   A change request can only be closed when all the active change tasks related to that change request are closed or canceled otherwise a pop-up appears notifying that there are open change tasks that require to be closed.
-   If there are existing change tasks that are manually placed on hold, those change tasks do not get overwritten when the change request is placed to the **On Hold** state. Similarly, when the change request is taken off the hold state, the change tasks that were placed on hold manually stays in the **On Hold** state.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Open the specific change request.

3.  Select the **On Hold** check box.

4.  In the **On hold reason** field, enter the reason for placing the change request on hold.

5.  Click **Update**.


**Parent Topic:**[Process a change request](t_ProcessAChangeRequest.md)

**Related topics**  


[State model and transitions](../concept/c_ChangeStateModel.md)

[Create a change request](t_CreateAChange.md)

