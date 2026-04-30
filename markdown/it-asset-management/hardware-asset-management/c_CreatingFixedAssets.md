---
title: Create fixed assets
description: Fixed assets are containers that can hold multiple assets. Fixed assets are commonly tracked at the corporate level by a finance or accounting department, but may contain IT assets such as hardware and software.You can calculate depreciation for a fixed asset using a choice of depreciation schedules. Calculating depreciation for a fixed asset can help IT coordinate with the corporate fixed asset system to report correct valuation and book value.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create fixed assets

Fixed assets are containers that can hold multiple assets. Fixed assets are commonly tracked at the corporate level by a finance or accounting department, but may contain IT assets such as hardware and software.

The **Fixed Asset** option in the Cost application shows the IT assets related to a fixed asset record. This link can help IT stay coordinated with the corporate asset system. Users with the financial\_mgmt\_admin and financial\_mgmt\_user roles can create fixed assets. After creating a fixed asset and adding assets, the residual value can be automatically calculated.

To create a fixed asset:

1.  Navigate to **Cost** &gt; **Fixed Assets**.
2.  Click **New**.
3.  Enter a name for the fixed asset.
4.  Click **Submit**.

To add assets to a fixed asset:

1.  Navigate to **Cost** &gt; **Fixed Assets**.
2.  Click a fixed asset.
3.  In the **Covered assets** related list, click **Edit**.
4.  In the **Collection** list, double-click an asset to add it to the **Covers Assets List**.
5.  Click **Save**.

To sum the residual values of all assets in a fixed asset:

1.  Navigate to **Cost** &gt; **Fixed Assets**.
2.  Click a fixed asset.
3.  Click **Sum Residual Value**.

    The ServiceNow platform calculates the**Residual Value**, **Total cost,** and **Total depreciation** based on information in the **Financial** and **Depreciation** sections on the individual asset records.


**Parent Topic:**[Using Hardware Asset Management](../../hardware-asset-management/concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../../hardware-asset-management/concept/Work-with-hardware-normalization.md)

[Work with Asset and CI](../../hardware-asset-management/concept/work-with-asset-ci.md)

[Consumables life cycle](c_FollowLifeCycleConsumbl.md)

[Manage asset bundles from your inventory](../../hardware-asset-management/task/create-bundled-assets.md)

[Manage various assets through asset classes](c_AssetClasses.md)

[Manage your inventory through pallet assets](../../hardware-asset-management/concept/pallets-for-inventory-management.md)

[Manage pre-allocated assets](../../hardware-asset-management/concept/manage-preallocated-asset.md)

[Manage loaner assets](../../hardware-asset-management/task/manage-loaner-asset.md)

[Donate assets to charity organizations](../../hardware-asset-management/concept/donate-asset-to-charity-organizations.md)

[Exclude assets](../../hardware-asset-management/task/exclude-assets.md)

[Use Advanced Shipment Notification](../../hardware-asset-management/task/advanced-shipment-notification.md)

[Use Organization Management](../reference/org-mgmt.md#)

[Manage RMA requests](../../hardware-asset-management/concept/manage-rma-req.md)

[Create an inventory stock order request](../../hardware-asset-management/task/create-inventory-stock-order.md)

[Transfer orders for Asset Management](transfer-orders-for-am.md#)

[Create a transfer order for Asset Management](../task/t_CreateATransferOrder.md#)

[Transfer order line asset tracking](../reference/r_TransferOrderLineAssetTracking.md#)

[Create a disposal order](../../hardware-asset-management/task/create-disposal-order.md)

[Use a hardware asset request flow](../../hardware-asset-management/task/hardware-request-flow.md)

[Audit your inventory](../../hardware-asset-management/task/audit-your-inventory.md)

[Request a Hardware Asset Refresh](../../hardware-asset-management/task/hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](../../hardware-asset-management/task/manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](../../hardware-asset-management/concept/manage-asset-reclaim.md)

[View RFID information of assets](../../hardware-asset-management/task/view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](../../hardware-asset-management/concept/manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](../../hardware-asset-management/concept/receive-warranty-details-lenovo.md)

[Manage stockrooms](../../hardware-asset-management/concept/manage-your-stockrooms.md)

[Track shipments using the integration framework](../../hardware-asset-management/concept/tracking-shipments-using-integration-framework.md)

[Track asset location using indoor maps](../../hardware-asset-management/task/track-asset-location-using-indoor-maps.md)

[Assess performance of Hardware Asset Management](../../hardware-asset-management/concept/suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](../../hardware-asset-management/concept/refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](../../hardware-asset-management/concept/configure-ham-tco.md)

[Manage and monitor hardware asset performance](../../hardware-asset-management/concept/manage-and-monitor-hardware-asset-performance.md)

[Manage Hardware Asset Management subscriptions](../../hardware-asset-management/concept/managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](../../hardware-asset-management/concept/manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](../../hardware-asset-management/concept/manage-asset-picking-stockroom-ham-ws.md)

[Manage asset put away using the Hardware Asset Workspace](../../hardware-asset-management/concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Manage hardware asset tasks using the Mobile Agent application](../../hardware-asset-management/concept/manage-hardware-asset-tasks-mobile-agent.md)

[Acknowledge receipt of assets on the Employee Center portal](../../hardware-asset-management/task/receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](../../hardware-asset-management/task/trigger-flow-ham.md)

## Use depreciation with fixed assets

You can calculate depreciation for a fixed asset using a choice of depreciation schedules. Calculating depreciation for a fixed asset can help IT coordinate with the corporate fixed asset system to report correct valuation and book value.

### Before you begin

Role required: financial\_mgmt\_admin or financial\_mgmt

### About this task

When creating a new depreciation schedule, select the **Declining Balance** or **Straight Line** depreciation **Category**. The two categories depreciate an asset by the same overall amount during the asset life cycle, but do so on different schedules.

-   **Declining Balance**: depreciates an asset by a greater amount in earlier accounting periods than in later periods.
-   **Straight Line**: depreciates an asset by an equal amount each accounting period.

The following example shows depreciated value on a $10,000.00 asset over five years using the two different methods.

|Year|Declining balance|Straight line|
|----|-----------------|-------------|
|1|$5000.00|$8000.00|
|2|$2500.00|$6000.00|
|3|$1250.00|$4000.00|
|4|$625.00|$2000.00|
|5|$0|$0|

### Procedure

1.  To view a depreciation schedule, navigate to **Financial Management** &gt; **Depreciation** and click the **Category**.

2.  To create a new depreciation schedule, click **New**.

3.  Enter a **Name**.

4.  Select a **Category**.

5.  Add a **Script** to calculate depreciation value.

    ![Depreciation schedule](../image/DepreciationSchedule.png "Example depreciation schedule script")

6.  Click **Submit**.

    The depreciation schedule is now available in the **Depreciation** field on the asset record.


