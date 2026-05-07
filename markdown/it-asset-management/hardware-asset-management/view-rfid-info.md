---
title: View RFID information of assets
description: View the Radio Frequency Identification \(RFID\) information of assets to manage and locate important assets easily.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# View RFID information of assets

View the Radio Frequency Identification \(RFID\) information of assets to manage and locate important assets easily.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to a hardware asset for which you want to view the RFID information.

<table id="choicetable_l5h_2mg_ywb"><thead><tr><th align="left" id="d340677e50">

Interface

</th><th align="left" id="d340677e53">

Action

</th></tr></thead><tbody><tr><td id="d340677e59">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Hardware Assets**.
2.  Select an Asset tag for which you want to view the RFID information.
3.  Select the Preview icon \(![Preview icon](../../software-asset-management2/image/preview-icon.png)\) beside the **RFID tag** field in the **General** tab.
4.  Select **Open Record** to view the RFID information of the asset.


</td></tr><tr><td id="d340677e107">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Hardware Asset Workspace** &gt; **Asset estate**.
2.  Select the **Hardware assets** tab.
3.  Select the display name of a hardware asset for which you want to view the RFID information.
4.  Select the Open Record icon ![Preview icon.](../../software-asset-management2/image/preview-icon.png) in the **RFID tag** field under the **Details** tab.


</td></tr></tbody>
</table>    **Note:** The RFID tag field doesn't exist for an excluded asset.

    |Field|Description|
    |-----|-----------|
    |RFID tag|Unique identifier of the RFID tag in the RFID system.|
    |Site name|Name of the site as defined in the RFID system.|
    |Type|Resource type as defined in the RFID system.|
    |Zone group|Zone group as defined in the RFID system.|
    |Serial number|Unique identifier as defined in the RFID system.|
    |Zone group dwell|Length of time the asset has been in the current zone group relative to the timestamp of the data import.|
    |Tag source|The application source of RFID data.|
    |Zone|Zone as defined in the RFID system.|
    |Last blink time|Last time the RFID tag was scanned.|
    |Zone dwell|Duration for which the asset has been in the current zone as compared to the timestamp of the data import.|
    |Last blink elapsed time|Duration for which the asset has been scanned in the RFID system as compared to the timestamp of the data import.|
    |Grid-x, Grid-y, Grid-z|Physical location as defined in the RFID system.|
    |Status|Status of the matching of RFID information to the resource.|
    |Active|Option to map RFID information to the Asset \[alm\_asset\] table. This option is selected by default.|

    **Note:**

    The activity history is captured only for RFID tag and Zone.


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

[Integrating Zebra technology RFID system](../concept/integrating-rfid.md)

