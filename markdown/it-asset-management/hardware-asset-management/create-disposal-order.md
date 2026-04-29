---
title: Create a disposal order
description: Create a disposal order for hardware or consumable assets. You can create a disposal order for an asset reaching its end of life cycle or an asset that is no longer functional.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create a disposal order

Create a disposal order for hardware or consumable assets. You can create a disposal order for an asset reaching its end of life cycle or an asset that is no longer functional.

## Before you begin

Role required: asset

**Note:** Install the Hardware Asset Management application from the ServiceNow Store.

## About this task

To add the consumables to a disposal order, select **Mark for disposal**. This will set the Planned for disposal field to **true**. For more details, see [Dispose of consumable assets](dispose-consumables.md).

Use the Workflow Studio application to create the Hardware Asset Disposal flow to take you through the entire hardware disposal order process.

The hardware disposal order goes through various stages before it’s completed. Each stage is associated with a hardware disposal task. To move through the various stages, close each task until you reach the last stage. After you complete the last task, the hardware disposal order is complete. For more information about the hardware disposal order stages, see [Hardware disposal order stages](../reference/hardware-disposal-stages.md).

You can cancel a disposal order until it reaches the transit stage in the workflow. After your disposal order is in the confirmation stage, you can't cancel that order. You can cancel a task that is in a draft, scheduling, or transit stage by selecting **Closed Incomplete** from the **State** list and closing the task.

Starting with Hardware Asset Management 15.0.0 version, the asset resale option is integrated at the final stage of the disposal workflow that is the Documentation stage. When the Disposal order task is in the Documentation stage, you can choose either to dispose of or to resell the assets. For more information about asset resale, see [Resale hardware assets](create-resale-order.md).

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory view**.

<table id="choicetable_l5h_scg_kyb"><thead><tr><th align="left" id="d325105e131">

Interface

</th><th align="left" id="d325105e134">

Action

</th></tr></thead><tbody><tr><td id="d325105e140">

**Core UI**

</td><td>

Navigate to **All** &gt; **Inventory** &gt; **Create Disposal Order**.

</td></tr><tr><td id="d325105e161">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory view**.
2.  Select the **Disposal orders** tab.
3.  Select **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_pf4_34w_nrb"><thead><tr><th>

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

Vendor

</td><td>

Vendor that you want to dispose the asset to.

</td></tr><tr><td>

Location

</td><td>

Location of the stockroom where the asset gets disposed from. The location automatically appears after you select a stockroom. If you change the location and no location is associated with the selected stockroom, the stockroom field becomes empty. In this scenario, you can select a stockroom from the stockroom list for a specified location.

</td></tr><tr><td>

Assigned to

</td><td>

Person responsible for disposing of the asset.

</td></tr></tbody>
</table>3.  Select **Save**.

    The disposal order is created and the hardware asset disposal workflow is triggered.

4.  In the Pickup details section of the Hardware Disposal Order Pickup Details form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Scheduled date|Date when you want to dispose of the asset.|
    |Pickup contact name|Name of the person from the vendor who will pick up the asset to dispose of.|
    |Pickup details|Details of the pickup.|
    |Additional info|Any message if you want to add.|

5.  Select the **Planned Assets** tab.

6.  Select **Add**.

7.  From the list of available assets, select the assets that you want to dispose of.

    The assets that you selected are shown in the **Planned Assets** tab. Also, the Verify Asset task is created as a hardware disposal task.

8.  Select the Verify Asset task.

9.  Select the asset that you want to verify and select **Verify**.

    You can't select an excluded asset. For more information, see [Hardware Asset Management license exclusion](../concept/ham-license-exclusion.md).

    The state of the asset changes to retired and the substate changes to pending disposal. The Scheduled Pickup task is created as a hardware disposal task.

10. Update the Schedule Details section with the details of the Vendor, Vendor order ID, Scheduled date, and Pickup contact name and select **Close task**.

    The Asset Departure task is created as a hardware disposal task.

11. In the Schedule Details section of the Asset Departure task, specify the details in the Shipped to, Shipping carrier, and Tracking number fields.

12. Select **Save**.

13. In the Asset Departure task, select the **Planned Assets** tab.

14. Select the assets that you want to depart and select **Depart**.

    **Note:** Planned assets that aren't departed are canceled automatically.

    The state of the asset changes to in transit and the substate changes to pending disposal. The Vendor confirmation task is created as a hardware disposal task.

15. Select the Vendor confirmation task and then select **Close task**.

    The stage changes to documentation. The Disposal Documentation task is created as a hardware disposal task.

16. Select the Disposal Documentation task and do the following:

    1.  Select the Attach File icon to attach disposal documentation for the planned assets.

    2.  In the **Certificate of disposal** list, select **Yes**.

        You must attach disposal documentation to the order and set the field to **Yes** to close the Disposal order to Completed.

17. Select **Close Task**.

    -   All the hardware disposal tasks are complete and the hardware disposal order stage changes to completed.
    -   The **Disposal date** field in the **Disposal** section of the asset form is populated.
    -   For any maintenance contracts that are associated with the disposed asset, the **Date removed** field in the **Contracts** tab is populated and the disposed asset is no longer part of the contract.
    -   Any entitlements that are associated with the disposed asset are also removed.

-   **[Resale hardware assets](create-resale-order.md)**  
Enhance asset management by reselling eligible retired hardware assets instead of disposing of them.
-   **[Perform bulk update of resale value for the assets](bulk-update-resale-value-asset-state.md)**  
Update the resale values for assets planned for disposal, and indicate that you want to resell them instead of disposing of them, to streamline the asset resale process.

**Parent Topic:**[Using Hardware Asset Management](../concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

[Manage asset bundles from your inventory](create-bundled-assets.md)

[Manage your inventory through pallet assets](../concept/pallets-for-inventory-management.md)

[Manage loaner assets](manage-loaner-asset.md)

[Donate assets to charity organizations](../concept/donate-asset-to-charity-organizations.md)

[Use Advanced Shipment Notification](advanced-shipment-notification.md)

[Manage RMA requests](../concept/manage-rma-req.md)

[Create an inventory stock order request](create-inventory-stock-order.md)

[Use a hardware asset request flow](hardware-request-flow.md)

[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

[Request a Hardware Asset Refresh](hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](../concept/manage-asset-reclaim.md)

[View RFID information of assets](view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](../concept/manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](../concept/receive-warranty-details-lenovo.md)

[Manage stockrooms](../concept/manage-your-stockrooms.md)

[Track shipments using the integration framework](../concept/tracking-shipments-using-integration-framework.md)

[Track asset location using indoor maps](track-asset-location-using-indoor-maps.md)

[Assess performance of Hardware Asset Management](../concept/suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](../concept/refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](../concept/configure-ham-tco.md)

[Manage Hardware Asset Management subscriptions](../concept/managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](../concept/manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](../concept/manage-asset-picking-stockroom-ham-ws.md)

[Manage hardware asset tasks using the Mobile Agent application](../concept/manage-hardware-asset-tasks-mobile-agent.md)

[Manage asset put away using the Hardware Asset Workspace](../concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Audit your hardware assets by using Asset Attestation](../concept/audit-hardware-assets-attestation.md)

[Acknowledge receipt of assets on the Employee Center portal](receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](trigger-flow-ham.md)

[Resale hardware assets](create-resale-order.md)

