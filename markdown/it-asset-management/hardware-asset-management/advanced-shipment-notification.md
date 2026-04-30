---
title: Use Advanced Shipment Notification
description: Use Advanced Shipment Notification \(ASN\) to automate and create asset records when your assets are in transit.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Use Advanced Shipment Notification

Use Advanced Shipment Notification \(ASN\) to automate and create asset records when your assets are in transit.

## Before you begin

Download your ASN template and get it updated by your asset vendor. Then upload the updated template to your ServiceNow instance. Before you import asset records using the ASN template, check that your ServiceNow instance has the model ID defined and that the same model ID is mentioned in the template.

The shipping address in the ASN template must match the shipping address in the Location \[cmn\_location\] table.

The shipping carrier in the ASN template must be available in the Shipping carrier \[sn\_itam\_shipping\_carrier\] table.

Role required: admin

## About this task

Creating asset records manually is time consuming and can cause errors in your records. Use ASN to automate and create asset records when the assets are in transit. The Tracking number in the ASN template helps to track the assets that are in transit.

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Orders** &gt; **Import Shipment Notification**.

2.  On the Import Template page, select the **Download Template File \(.xlsx\)** link to download an ASN template.

    The ASN template has fields such as the following:

    -   Serial number: Unique identifier of the asset.
    -   Asset tag: Alphanumeric tag assigned by your organization to help track the asset.
    -   Vendor: Vendor from which the asset was purchased.
    -   PO number: Number associated with the purchase order.

        **Note:** This isn't the vendor PO number.

    -   Model id: Model number of the product model.
    -   SVC contract end date: Warranty expiration date of the asset.
    -   Carrier: Name of the shipping carrier.
3.  Send the ASN template to your asset vendor, such as via email.

    The vendor has to update the template with the details of each asset that will be delivered to you. The vendor can enter values in each column based on the column header. For example, `TrackASN1`in the Tracking number column and `CarrierABC` in the Carrier column. The vendor then shares the updated template with you.

4.  After you receive an updated ASN template from your vendor, select **Browse files** and select the updated ASN template.

5.  Select **Upload**.

    The upload may take some time. The import process is asynchronous so wait for the import process to complete and for all assets to be created.

6.  Check the status of importing the template in one of the following ways.

    -   Navigate to **Procurement** &gt; **Orders** &gt; **Import Status**.
    -   To open directly the import set record, select the link on the message bar that shows `View import progress here`.
    The Import Sets page shows a list of import set records.

7.  Select the import set record that shows the status of importing your template.

    The import set record shows if the asset record was created successfully. If the import wasn’t successful, then do the following:

    1.  On the import set record, select the **Import Set Rows** tab.
    2.  To understand the failure, check the **Comment** field.
    3.  Try to import an updated template again.

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

[Use Organization Management](../../asset-management/reference/org-mgmt.md#)

[Manage RMA requests](../concept/manage-rma-req.md)

[Create an inventory stock order request](create-inventory-stock-order.md)

[Transfer orders for Asset Management](../../asset-management/concept/transfer-orders-for-am.md#)

[Create a transfer order for Asset Management](../../asset-management/task/t_CreateATransferOrder.md#)

[Transfer order line asset tracking](../../asset-management/reference/r_TransferOrderLineAssetTracking.md#)

[Create a disposal order](create-disposal-order.md)

[Use a hardware asset request flow](hardware-request-flow.md)

[Audit your inventory](audit-your-inventory.md)

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

