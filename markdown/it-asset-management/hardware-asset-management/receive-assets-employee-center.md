---
title: Acknowledge receipt of assets on the Employee Center portal
description: After receiving hardware or consumable assets that were in transit and reserved for you, confirm their receipt on the Employee Center portal.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Acknowledge receipt of assets on the Employee Center portal

After receiving hardware or consumable assets that were in transit and reserved for you, confirm their receipt on the Employee Center portal.

## Before you begin

Role required: Log in as an employee.

To view the **My Assets** option on the global header navigation bar of the Employee Center portal, the value of the **enable\_assets** option must be set to **true** on the Additional options, JSON format field of the Employee Center menu record. For more details, see Enable or disable global header options.

**Note:** The **My Assets** option requires the Hardware Asset Management application to be activated.

## About this task

When an asset reserved for you is in transit, you will receive an email notification with a link to the Employee Center Portal, where you can acknowledge its receipt. You can receive an asset even if the asset is excluded from Hardware Asset Management workflows or if the associated resource category isn't opted in.

## Procedure

1.  View the assets that are reserved for you on the Employee Center portal.

    -   Select the **Receive assets** link in the email notification that you received.

        The link opens the **My Assets** page on the Employee Center portal.

    -   View assets using any of the options available in the global header navigation bar of the Employee Center portal.

<table id="table_opg_qvq_pfc"><thead><tr><th>

UI option

</th><th>

Action

</th></tr></thead><tbody><tr><td>

**My Assets**

</td><td>

Select **My Assets** in the global header navigation bar of the Employee Center portal.**Note:** The number displayed on the **My Assets** option represents the total count of assets that must be attested and received.

</td></tr><tr><td>

**Profile**

</td><td>

1.  Select **Profile** on the global header navigation bar of the Employee Center portal.
2.  Select the **Assets** tab.


</td></tr></tbody>
</table>    The page displays all the hardware and consumable assets that are assigned to you, in transit, and reserved for you. You can acknowledge the receipt of hardware and consumable assets that are in transit.

2.  Acknowledge after you receive the asset.

<table id="choicetable_rv3_cx5_jfc"><thead><tr><th align="left" id="d95245e214">

Asset

</th><th align="left" id="d95245e217">

Action

</th></tr></thead><tbody><tr><td id="d95245e223">

**Hardware**

</td><td>

1.  For the hardware asset that you want to receive, select **Receive asset**.
2.  In the Receive asset dialog box, follow any of these steps:
    -   If the **Asset tag** and **Serial number** fields have values, verify them and then select **Submit**.
    -   If either the **Asset tag** or **Serial number** field is empty, enter the value and then select **Submit**.

**Note:** You can only enter values in the empty **Asset tag** or **Serial number** fields if the value of the **sn\_hamp.enable\_asset\_tag\_serial\_number\_edits** system property is set to **true**. This system property can be updated with the admin role.

 -   **Result:**
    -   Asset is received successfully.
    -   Status of the asset changes from **In transit** to **In use**, and the asset is assigned to you.
    -   The **Receive asset** option is no longer available for that asset.
    -   Any receive task associated with that asset is automatically closed.
 **Note:** If the details of the asset that you received don't match the information shown in the Receive Asset dialog box, you can raise an issue by selecting the **Raise issue** option. For more details, see [Raise issue related to your asset on the Employee Center portal](report-asset-issue-attestation.md).

</td></tr><tr><td id="d95245e336">

**Consumables**

</td><td>

1.  For the consumable asset that you want to receive, select **Receive asset**.
2.  In the Receive asset dialog box, enter the quantity of consumables that you received in the **Quantity** field.

**Note:** By default, this field displays the consumable quantity that you requested. You can enter a value that is lesser than or equal to the requested quantity, but it must be a positive number and not zero.

3.  Select **Submit**.
 -   **Result:**
    -   If you received the full requested quantity of consumables, then the Status of the asset changes from **In transit** to **Consumed**, and the asset is assigned to you.
    -   If you received only a partial quantity of the requested consumables, the following changes occur:

        -   The status of the assets that you received changes from **In transit** to **Consumed**, and the assets are assigned to you.
        -   The status of the assets that you didn't receive remains **In transit**.
**Note:** Consumed and in transit consumables are displayed separately.

</td></tr></tbody>
</table>
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

[Update associated Decision tables for HAM flows](trigger-flow-ham.md)

