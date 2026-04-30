---
title: Create a disposal order in the Enterprise Asset Workspace
description: Create a disposal order for an asset that has reached the end of its life cycle or is no longer functional.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Create a disposal order in the Enterprise Asset Workspace

Create a disposal order for an asset that has reached the end of its life cycle or is no longer functional.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## About this task

Only assets that are associated with enterprise or palletmodels can be disposed of using an enterprise disposal order.You can add simple assets; multi-component assets, which include pre-assembled and user-assembled assets; and pallet assets with children to an enterprise disposal order.

**Note:** If you are adding a multi-component asset or a pallet asset with children to a disposal order, any changes that you make to the parent asset are automatically applied to all child assets.

Use the Flow Designer application to create the disposal flow to take you through the entire asset disposal order process.

The disposal order goes through various stages before it’s completed. Each stage is associated with a disposal task. To move through the various stages, close each task until you reach the last stage. After you complete the last task, the disposal order is complete. For more information about the disposal order stages, see disposal order stages.

**Note:** You can cancel a disposal order until it reaches the transit stage of the workflow. Once your disposal order is in the confirmation stage, you can't cancel that order. You can cancel a task that is in a draft, scheduling, or transit stage by selecting **Closed Incomplete** from the State list and closing the task.

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Inventory** &gt; **Disposal orders**.

2.  Select **New**.

    The Create New Enterprise Disposal Order page opens.

3.  On the form, fill in the details.

<table id="table_vcd_y2k_psb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Reference number of the disposal order.

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom where the asset is disposed from.

</td></tr><tr><td>

Location

</td><td>

Location of the stockroom where the asset gets disposed from. The location automatically appears after you select a stockroom.

 If you change the location and no location is associated with the selected stockroom, the stockroom field becomes empty. In this scenario, you can select a stockroom from the stockroom list for a specified location.

</td></tr><tr><td>

Assigned to

</td><td>

Person responsible for disposing of the asset.

</td></tr><tr><td>

Stage

</td><td>

Current stage of the disposal order.

</td></tr><tr><td>

Vendor

</td><td>

Vendor that you want to dispose the asset to.

</td></tr></tbody>
</table>4.  Select **Save**.

    The new disposal order is created and the disposal order workflow is triggered.

5.  On the Pickup Details form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Scheduled date|Date when you want to dispose of the asset.|
    |Pickup contact name|Name of the person from the vendor who will pick up the asset to dispose of.|
    |Pickup details|Details of the pickup.|
    |Additional info|Any message you want to add.|

6.  Open the **Disposable Assets** tab.

7.  Select **Add** to select the assets that you want to dispose of.

8.  Select the assets that you want to dispose of and select **Add**.

    Only assets that are in a non-terminal state appear in the list. A non-terminal state is any state in which the asset can transition into a different state.

    Under the **Enterprise Disposal Tasks** tab, a Verify Assets task is created.

9.  Open the **Enterprise Disposal Tasks** tab and select the Verify Assets task.

10. In the Enterprise Disposal Tasks page, select the assets that you want to dispose of and select **Verify**.

    The state of the asset changes to In stock and the substate changes to Pending disposal.

11. Select **Close task**.

    **Note:** You cannot add additional assets to the disposal order after you complete and close the Verify Assets task.

    The draft stage is completed and the scheduling stage is in progress. The next task in the workflow, Schedule pickup, is automatically created and appears in the **Enterprise Disposal Tasks** tab.

12. Select the Schedule pickup task and in the **Vendor** and **Scheduled date** fields, enter the values that you want.

13. Select **Close Task**.

    The stage changes to transit and the Asset departure task is created.

14. Select the Asset departure task and in the **Vendor order ID** and **Pickup contact name** fields, enter the value that you want.

15. Select the assets that you want to dispose of and in the **Actions on selected rows** picker, select **Depart**.

    The state of the asset changes to in transit and the substate changes to pending disposal.

16. Select **Close Task**.

    The stage changes to confirmation and the Vendor confirmation task is created.

17. Select the Vendor confirmation task and then select **Close Task**.

    The stage changes to documentation and a Disposal Documentation task is created.

18. Select the Disposal Documentation task and do the following:

    1.  Select the Attach File icon to attach disposal documentation for the planned assets.

    2.  Select the assets that you want to dispose of.

        **Note:** If your disposal order contains any multi-component assets or pallet assets with children, the parent-child relationships within those assets are no longer applicable when you reach this task. Any changes that you make to a parent asset are no longer automatically applied to its child assets. You must individually select each asset that you want to dispose of, regardless of whether it is a parent or child asset.

    3.  Select **Dispose**.

        The state of the asset changes to retired and the sub state changes to disposed.

    4.  In the **Certificate of disposal** list, select **Yes**.

19. Select **Close Task**.

    All the enterprise disposal tasks are complete and the enterprise disposal order stage changes to completed.


**Parent Topic:**[Create and manage enterprise asset inventory](../concept/managing-enterprise-asset-inventory.md)

