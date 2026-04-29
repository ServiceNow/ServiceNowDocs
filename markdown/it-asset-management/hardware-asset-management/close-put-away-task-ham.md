---
title: Close an Asset put away task
description: Add the asset drop-off location for an open Asset put away task and close it in the Hardware Asset Workspace.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [close asset put away task, asset put away task]
breadcrumb: [Manage asset put away using the Hardware Asset Workspace, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Close an Asset put away task

Add the asset drop-off location for an open Asset put away task and close it in the Hardware Asset Workspace.

## Before you begin

Role required: inventory\_user

## About this task

You can bulk close selected Asset put away tasks that are open and assigned to you by specifying a drop-off location, which moves all associated assets to that location. You can also close individual tasks by specifying a drop-off location.

**Note:** When you make the following changes to a hardware asset, the associated Asset put away task is closed:

-   When the asset’s **Aisle and Space** value is filled, the associated Asset put away task for the asset is closed, and the **State** field is updated to **Closed Complete**.
-   When the asset’s State field is updated from In stock to some other value without adding the **Aisle and Space** field value, the associated Asset put away task is closed and its state is updated to Closed Incomplete.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Open the put away task either from the Inventory overview section or the **All Stockrooms** tab.

<table id="choicetable_t5y_1ct_xfc"><thead><tr><th align="left" id="d270299e107">

Option

</th><th align="left" id="d270299e110">

Description

</th></tr></thead><tbody><tr><td id="d270299e116">

**From the Inventory overview section**

</td><td>

1.  In the Inventory overview section, select the **Open put away tasks** card.
2.  Select the **Number** link to open the Asset put away task.


</td></tr><tr><td id="d270299e140">

**From the __All Stockrooms__ tab.**

</td><td>

-   In the **All Stockrooms** tab, select a stockroom.
-   In the Open stockroom tasks section, select the **Open put away tasks** card.
-   Select the **Number** link to open the Asset put away task.


</td></tr></tbody>
</table>3.  In the Put away task form, select the **Drop off location** value.

4.  Save your modifications or close the put away task.

    -   To close the put away task, select **Close task**.
    -   To save your changes and stay on the same page, select **Save**.
    -   To close multiple put away tasks, select **Bulk close**.

        The **Select Assets** dialog box is displayed listing the Asset put away tasks assigned to you. Select the tasks that you want to close and select **Close Task**.


## Result

-   Closed tasks aren’t displayed in the Open put away tasks list.
-   The task closure is captured in the **Activity** tab. The name of the user who closed the task is shown in the work notes.

**Parent Topic:**[Manage asset put away using the Hardware Asset Workspace](../concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

