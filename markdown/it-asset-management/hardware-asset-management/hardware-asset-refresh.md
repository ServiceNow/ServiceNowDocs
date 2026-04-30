---
title: Request a Hardware Asset Refresh
description: Use the Hardware Refresh request flow to track the aged hardware assets that are nearing the end of their life cycle. Replace them with new hardware assets.Replace aged hardware assets by sourcing new hardware assets.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Request a Hardware Asset Refresh

Use the Hardware Refresh request flow to track the aged hardware assets that are nearing the end of their life cycle. Replace them with new hardware assets.

## Before you begin

Role required: Inventory\_user

## About this task

When hardware assets get old, their maintenance costs and risks of failure increase, while their performance decreases. You can choose to replace all the old hardware assets with the same or different models of new hardware assets. After your Hardware Asset Refresh request is approved, the Hardware Asset Refresh flow takes you through sourcing and it triggers the Hardware Asset Refresh Line flow. The Hardware Asset Refresh Line flow uses Refresh Line tasks to take you through the steps of preparing the new asset, scheduling it for delivery, deploying it, and reclaiming the aged asset.

The Flow Designer application is used to create the Hardware Asset Refresh flow and the Hardware Asset Refresh Line flow. While customizing the Hardware Asset Refresh module, don't remove or customize the **Update Sourcing set Variable** step in the Hardware Asset Refresh flow.

**Note:** You can check if a hardware model is eligible for refresh by using the Eligible for refresh field of the Hardware \[alm\_hardware\] table. The SAM - Calculate Asset Refresh Eligibility scheduled job runs weekly and invokes the **Process** method in the **SAMRefreshEligibityCalculator** Script Include. The Script Include fetches the hardware product model records for the assets for which the useful\_life field \(in months\) is specified. The date on which the asset record was created is compared with the useful\_life field to determine if the asset is in the useful life period. The Eligible for refresh flag is set to true for assets that aren't in the useful life period.

![Hardware Asset Refresh flow.](../image/hardware-asset-refresh-flow.png "Hardware Asset Refresh Flow")

While customizing a Hardware Asset Refresh catalog item on the Catalog Item form, don't remove or change the following variables.

|Tabs in the Catalog Item|Variables|
|------------------------|---------|
|Variables|Type of refresh|
|Process|
|Variable Sets|Hardware Asset Management process set|
|Hardware Asset Management sourcing set|

**Note:** There are readily available decision tables that you can use to customize the Hardware Asset Refresh Line Flow. For more details, see [Hardware Asset Management flow customization](../concept/readily-available-dec-tables-ham.md).

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Asset Lifecycle**.

    The **Asset Lifecycle** category isn’t on the Service Catalog page by default. To add this category, select the add content icon \(![Add content icon.](../image/add_content_icon.png)\) beside the search catalog bar and then select **Asset Lifecycle**.

2.  Open **Hardware Asset Refresh Order**.

3.  If you want to replace all the aged hardware assets with the same model of new hardware assets, do the following:

    1.  From the **Type of refresh list** field, select **Single model**.

    2.  On the form, fill in the fields.

<table id="table_mzn_b4q_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Replacement model

</td><td>

New hardware asset model that you want to replace the aged hardware assets with.

</td></tr><tr><td>

Location

</td><td>

Location where you want to deploy the new asset.By default, this field is set to the location of the logged-in user. However, you can select a location from the list of available locations.

</td></tr><tr><td>

Assets

</td><td>

Aged Hardware assets that you want to replace. You can use a filter to search for hardware assets that you want to replace.

</td></tr></tbody>
</table>4.  If you want to replace the aged hardware assets with different models of new hardware assets, do the following:

    1.  From the **Type of refresh** field, select **Multi model**.

    2.  Select **Add**.

    3.  For each new hardware asset that you want to use, add a row to enter the hardware model.

        **Note:**

        You can create 50 rows.

        You can’t create multiple rows for the same aged hardware asset that you want to replace.

5.  Select **Order Now**.

    You can't view an excluded asset. For more information, see [Hardware Asset Management license exclusion](../concept/ham-license-exclusion.md).


## Result

The aged assets are set to get refreshed. In the Hardware table under the Disposal related list of the aged assets, the **Refresh request line** field is populated.

An Order status page appears and it displays the details of the order. A request is created to source the new hardware assets and to replace the aged hardware assets. The Request form shows the total price of all the new hardware asset models.

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

[Create a disposal order](create-disposal-order.md)

[Use a hardware asset request flow](hardware-request-flow.md)

[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

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

## Use Hardware Asset Refresh Lines tasks to replace the aged assets

Replace aged hardware assets by sourcing new hardware assets.

### Before you begin

Role required:

-   proc\_user for sourcing.
-   asset and itil for Refresh Line tasks.

### About this task

When refreshing hardware assets, you don't have to update the asset records manually. When closing the hardware asset refresh lines, the asset records and the assets are automatically updated. Close each task to go to the next task, complete the refresh, and reclaim the aged assets.

After sourcing the new assets, the asset refresh is completed through the following stages:

-   Prepare asset task: Prepare the new asset before you hand it over to the requester. For example, install any software that's required.
-   Schedule refresh task: Schedule a date to hand over the asset to the requester.
-   Deploy new asset: Hand over the asset to the requester or install the asset at the requester's location if necessary.
-   Reclaim aged asset: Collect the aged asset.

### Procedure

1.  Select the hardware asset refresh request.

<table id="choicetable_upl_qst_ywb"><thead><tr><th align="left" id="d263536e750">

Interface

</th><th align="left" id="d263536e753">

Action

</th></tr></thead><tbody><tr><td id="d263536e759">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Open Record** &gt; **Requests**.
2.  Select the request number of the hardware asset refresh request that you want to fulfill.


</td></tr><tr><td id="d263536e792">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Procurement view**.
2.  Select the **Requests** tab.
3.  Select the request number of the hardware asset refresh request that you want to fulfill.


</td></tr></tbody>
</table>    After your hardware asset refresh request is approved, the following events happen:

    -   The Source Request flow is triggered to source new assets.
    -   In the **Catalog Tasks** tab, a catalog task is created for the procurement of the new hardware asset.
2.  Source items in the request.

    You can source items in the request by consuming the local stock, through purchase orders, or through transfer orders.

    For more details on sourcing items, see [Sourcing items in a service catalog request](../../procurement/concept/c_SourcingRequestItems.md).

    After the new asset is received, the following events happens:

    -   The Hardware Asset Refresh Line flow is triggered for the asset.
    -   The Hardware Asset Refresh Line tab is displayed next to the Asset Tasks tab on the requested item form.
    -   The Asset pick task is created under the Refresh Line Tasks only if the requested item is consumed from the local stockroom for which the Asset pick task is enabled. Otherwise thePrepare asset task is createddirectly without the Pick task. For details, see [Enable the Asset pick task for your stockroom in the Hardware Asset Workspace](enable-pick-task-for-stockroom-ham.md).
3.  Select the **Hardware Asset Refresh Line** tab.

4.  Select the hardware asset refresh line.

5.  Select the **Refresh line tasks** tab.

6.  Complete the Asset pick task by using the Mobile Agent application.

    For details on completing this step, see [Locate and pick the hardware assets in your stockroom using the Mobile Agent application](locate-and-pick-hardware-asset-using-mobile-app.md).

7.  Prepare the asset.

    1.  Select the **Prepare asset** task.

    2.  In the **Asset** field, select the hardware asset that you want to replace.

    3.  Select **Save**.

    4.  Select **Close Task**.

    -   A Schedule refresh task is created under the Refresh Line Tasks.
    -   The state of the Replacement asset changes to In stock.
    -   The substate changes to Reserved.
    -   The **Reserved for** field is populated with the requester details.
8.  Complete the Schedule refresh task.

    1.  Select the **Schedule refresh** task.

    2.  In the **Scheduled deployment date** field, select the date on which the new asset will be deployed.

    3.  Select **Close Task**.

    -   The Deploy new asset task is created under the Refresh Line Tasks.
    -   The state of the Replacement asset changes to In stock and the substate changes to Pending install.
9.  Complete the Deploy new asset task.

    1.  Select the **Deploy new asset** task.

    2.  Confirm if you have reclaimed the old asset in the **Is reclaimed** list.

        -   If you’ve collected the aged asset, select **Yes**.
        -   If you didn’t collect the aged asset, select **No**.
        The Location field shows the location where the new asset should be deployed.

    3.  Select **Close task**.

        **Note:** If you select **Yes** from the Is reclaimed list, then the Reclaim aged asset task is also closed by default.

    -   Reclaim aged asset task is created under the Refresh Line Tasks.
    -   The state of the replacement asset changes to In use.
    -   The allocations are transferred from the aged asset to the replacement asset.
10. Complete reclaiming the aged assets.

    1.  Select the **Reclaim aged asset** task.

    2.  Confirm if you have reclaimed the old asset in the **Is reclaimed** list.

        -   If you’ve collected the aged asset, select **Yes**.
        -   If you didn’t collect the aged asset, select **No**.
    3.  Select **Close task**.

    **Note:** You can cancel the hardware asset Refresh Line either by selecting **Cancel** or by changing the **State** field to **Closed Incomplete** in the Refresh Line task.


### Result

After the aged hardware asset is reclaimed, the following changes happen on the Hardware form:

-   The state of the aged asset changes to In stock.
-   The substate changes to Pending disposal.

