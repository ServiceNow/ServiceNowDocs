---
title: Manage assets in a work order task
description: Add, remove, or move enterprise assets across work order tasks to manage the work performed on specific assets.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Affected assets, Add assets, Remove assets, Move assets to cloned work order task]
breadcrumb: [Create a work order for an enterprise asset, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Manage assets in a work order task

Add, remove, or move enterprise assets across work order tasks to manage the work performed on specific assets.

## Before you begin

The work order task must be in one of the following states:

-   Draft
-   Pending assignment
-   Accepted

Before you move assets to another work order task, consider the following points:

-   You can't move all assets out of a work order task.
-   The **Move to cloned task** option isn't available if the work order task has only one asset.

Role required: sn\_eam.asset\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Work management**.

2.  Select the **Work order tasks**.

3.  Select the work order task for which you want to manage assets.

4.  Select the **Affected assets** tab.

5.  Perform the required asset action.

<table id="choicetable_qfw_xxr_33c"><thead><tr><th align="left" id="d216683e141">

Asset action

</th><th align="left" id="d216683e144">

Steps

</th></tr></thead><tbody><tr><td id="d216683e150">

**Add assets to the work order task**

</td><td>

1.  Select **Add asset\(s\)**.
2.  Select the assets that you want to add to the work order task.

**Note:** The list of available assets when adding depends on the work order association:

    -   If the work order is for an asset group, assets that are in the asset group but not yet in the Affected assets list are shown.
    -   If the work order is for an asset or location, all assets in that location are shown.
3.  Select **Add**.


</td></tr><tr><td id="d216683e187">

**Remove assets from the work order task**

</td><td>

1.  Select the assets that you want to remove.
2.  Select **Remove**.
3.  In the Delete dialog box, select **Delete all** to confirm.


</td></tr><tr><td id="d216683e214">

**Move assets to another work order task**

</td><td>

1.  Select the assets that you want to move to another work order task.
2.  Select **Move to cloned task**.
3.  In the Confirm task cloning and asset reassignment dialog box, select **Confirm**.


</td></tr></tbody>
</table>    **Note:** You can also add and remove assets from the work order by using the **Add asset\(s\)** and **Remove** options.


## Result

-   Add assets: The asset appears in the **Affected assets** tab.
-   Remove: The asset is removed from the Affected assets list. If the work order is associated with an asset group, the asset is removed from the Affected assets list only, not from the asset group.
-   Move to cloned task: A new work order task is created for the same work order, and the asset is moved to that task. The asset no longer appears in the Affected assets list of the original work order task.

