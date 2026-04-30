---
title: Close an Asset put away task in the Enterprise Asset Workspace
description: Add the asset drop-off location for an open Asset put away task and close it in the Enterprise Asset Workspace.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [close asset put away task, asset put away task]
breadcrumb: [Manage asset put away using the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Close an Asset put away task in the Enterprise Asset Workspace

Add the asset drop-off location for an open Asset put away task and close it in the Enterprise Asset Workspace.

## Before you begin

Role required: inventory\_user

## About this task

You can bulk close selected Asset put away tasks that are open and assigned to you by specifying a drop-off location, which moves all associated assets to that location. You can also close individual tasks by specifying a drop-off location.

**Note:** When you make the following changes to an enterprise asset, the associated Asset put away task is closed:

-   When the asset’s **Aisle and Space** value is filled, the associated Asset put away task for the asset is closed, and the **State** field is updated to **Closed Complete**.
-   When the asset’s **State** is updated from In stock to some other value without adding the **Aisle and Space** field value, the associated Asset put away task is closed and its **State** field is updated to **Closed Incomplete**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Open the put away task either from the Inventory overview section or the **All Stockrooms** tab.

    -   In the Inventory overview section, select the **Open put away tasks** card and select the **Number** link to open the Asset put away task.
    -   In the **All Stockrooms** tab, select a stockroom. In the Open stockroom tasks section, select the **Open put away tasks** card and then select the **Number** link to open the Asset put away task.
3.  In the Put away task form, select the **Drop off location** value.

4.  Save your modifications or close the put away task.

    -   To close the put away task, select **Close task**.
    -   To save your changes and stay on the same page, select **Save**.
    -   To close multiple put away tasks, select **Bulk close**.

        The **Select Assets** dialog box is displayed listing the Asset put away tasks assigned to you. Select the tasks that you want to close and select **Close Task**.


## Result

-   Closed tasks aren’t displayed in the Open put away tasks list.
-   The task closure is captured in the **Activity** tab. The name of the user who closed the task is shown in the work notes.

.

**Parent Topic:**[Manage asset put away using the Enterprise Asset Workspace](../concept/manage-asset-putaway-stockroom-enterprise-asset-workspace.md)

