---
title: Audit your inventory
description: Perform scheduled or blind audits of asset stockrooms and other locations such as offices or datacenters.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Audit your inventory

Perform scheduled or blind audits of asset stockrooms and other locations such as offices or datacenters.

## Before you begin

Role required: asset

The asset or inventory\_user role can only access the Asset Audits \[sn\_hamp\_asset\_audit\] reports.

-   Hardware Asset Management
-   [ServiceNow Agent app](../../asset-management/concept/agent-mobile-asset.md#)

## About this task

The asset audit process involves verifying and reconciling assets between a physical location or stockroom and the ServiceNow instance. This process includes identifying assets at a physical location by scanning QR codes attached to them and then checking if the corresponding asset records are present in the ServiceNow instance to generate the audit results. You can view precise inventory information through detailed lists and reports.

You can create an audit on the ServiceNow AI Platform or the ServiceNow Agent app. Use the ServiceNow AI Platform to create scheduled audits and the ServiceNow Agent app for blind audits. For more details on scanning the assets, see [Scan assets by using ServiceNow Agent app](scan-assets-agent-app.md).

## Procedure

1.  Create an audit.

<table id="choicetable_upl_qst_ywb"><thead><tr><th align="left" id="d123722e108">

Interface

</th><th align="left" id="d123722e111">

Action

</th></tr></thead><tbody><tr><td id="d123722e117">

**Core UI**

</td><td>

1.  Navigate to **Asset Audits** &gt; **Asset Audits** form.
2.  Select **New**.


</td></tr><tr><td id="d123722e147">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory view**.
2.  Select the **Asset audit** tab. The **Asset audit** tab displays a list of existing asset audits.
3.  Select **New**.


</td></tr><tr><td id="d123722e189">

**ServiceNow Agent app**

</td><td>

1.  Tap **Assets**.
2.  Select the audit that you want to perform.
    -   To perform stockroom audits, tap **Stockroom audits**.
        1.  Tap the more actions icon \(![More actions icon](../image/more-actions-icon.png)\).
        2.  Tap **New stockroom audit**.
    -   To perform location audits, tap **Location audits**.
        1.  Tap the more actions icon \(![More actions icon](../image/more-actions-icon.png)\).
        2.  Tap **New location audit**.


</td></tr></tbody>
</table>2.  On the Create New Asset Audits form, fill in the fields.

<table id="table_kt4_5lw_nrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audit number

</td><td>

Audit reference number.

</td></tr><tr><td>

Assigned to

</td><td>

Person responsible for the audit.

</td></tr><tr><td>

Type

</td><td>

Type of the audit. The available values are-   Location
-   Stockroom


</td></tr><tr><td>

Status

</td><td>

Present status of the audit.

</td></tr><tr><td>

Stockroom

</td><td>

Location where you want to perform the audit.

</td></tr><tr><td>

Scan date

</td><td>

Date when you want to scan the assets.

</td></tr><tr><td>

Scheduled date

</td><td>

Scheduled date when you want to perform the audit.

</td></tr></tbody>
</table>3.  Select **Save**.

    The Audit Results section is activated and shows the details of the audit result.

4.  View audit results on the ServiceNow AI Platform.

    1.  Navigate to **Asset Audits** &gt; **Asset Audits**.

    2.  Select the audit.

        You can view the Asset audit form and the audit results. For more information, see [Audit results](../reference/audit-results.md).

        ![Audit Results shows a pie chart of assets grouped by state](../image/ham-asset-audit.png "Asset audit form")


## What to do next

[Scan assets by using ServiceNow Agent app](scan-assets-agent-app.md).

-   **[View audit results](view-audit-results.md)**  
View the audit results after you audit your inventory. The Audit Results section is activated and shows the details of the audit result.
-   **[Scan assets by using ServiceNow Agent app](scan-assets-agent-app.md)**  
Scan your assets by using the ServiceNow Agent app.

**Parent Topic:**[Using Hardware Asset Management](../concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

[Work with Asset and CI](../concept/work-with-asset-ci.md)

[Consumables life cycle](../../asset-management/concept/c_FollowLifeCycleConsumbl.md)

[Manage asset bundles from your inventory](create-bundled-assets.md)

[Manage various assets through asset classes](../../asset-management/concept/c_AssetClasses.md)

[Manage your inventory through pallet assets](../concept/pallets-for-inventory-management.md)

[Create fixed assets](../../asset-management/concept/c_CreatingFixedAssets.md#)

[Manage pre-allocated assets](../concept/manage-preallocated-asset.md)

[Manage loaner assets](manage-loaner-asset.md)

[Donate assets to charity organizations](../concept/donate-asset-to-charity-organizations.md)

[Exclude assets](exclude-assets.md)

[Use Advanced Shipment Notification](advanced-shipment-notification.md)

[Use Organization Management](../../asset-management/reference/org-mgmt.md#)

[Manage RMA requests](../concept/manage-rma-req.md)

[Create an inventory stock order request](create-inventory-stock-order.md)

[Transfer orders for Asset Management](../../asset-management/concept/transfer-orders-for-am.md#)

[Create a transfer order for Asset Management](../../asset-management/task/t_CreateATransferOrder.md#)

[Transfer order line asset tracking](../../asset-management/reference/r_TransferOrderLineAssetTracking.md#)

[Create a disposal order](create-disposal-order.md)

[Use a hardware asset request flow](hardware-request-flow.md)

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

[Manage and monitor hardware asset performance](../concept/manage-and-monitor-hardware-asset-performance.md)

[Manage Hardware Asset Management subscriptions](../concept/managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](../concept/manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](../concept/manage-asset-picking-stockroom-ham-ws.md)

[Manage asset put away using the Hardware Asset Workspace](../concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Manage hardware asset tasks using the Mobile Agent application](../concept/manage-hardware-asset-tasks-mobile-agent.md)

[Acknowledge receipt of assets on the Employee Center portal](receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](trigger-flow-ham.md)

