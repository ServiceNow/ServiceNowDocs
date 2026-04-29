---
title: Task closures that create shipment records
description: A shipment record is created automatically when any shipment task is closed. You can track a shipment easily by specifying a tracking number and shipping carrier on the shipment task.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Hardware Asset Management reference, Hardware Asset Management, IT Asset Management]
---

# Task closures that create shipment records

A shipment record is created automatically when any shipment task is closed. You can track a shipment easily by specifying a tracking number and shipping carrier on the shipment task.

<table id="table_rr2_fkb_qxb"><thead><tr><th>

Source flow

</th><th>

Task source for shipment record creation

</th><th>

Source for updating the shipment record to Closed or Delivered

</th></tr></thead><tbody><tr><td>

Asset Donation

</td><td>

The Select the assets departing for donation task is closed.

</td><td>

The Confirmation from charity organization task is closed.

</td></tr><tr><td>

Asset disposal

</td><td>

The Asset departure task is closed.

</td><td>

The Vendor confirmation task is closed.**Note:** You can change the tracking number until this task is closed. If you don't specify any tracking number, a shipment record is created with the Vendor order ID as the tracking number.

</td></tr><tr><td>

Purchase order

</td><td>

-   [Create hardware assets prior to delivery](../../procurement/task/t_CreateAssetReserveForRequester.md): When the hardware asset records are automatically created.
-   [Advanced shipment notification](../task/advanced-shipment-notification.md): When the assets are imported for every unique tracking number specified in the import file.

**Note:**

If the shipping carrier specified for a row in the import file isn't available in the Shipping carrier \[sn\_itam\_shipping\_carrier\] table, then that row isn’t imported. Also, no shipment record is created. You must do one of the following and reimport the file:

    -   The shipping carrier must be included in the Shipping Carriers list. For more details, see [Create a shipping carrier record](../task/create-shipping-carrier.md).
    -   The value of the sn\_hamp.enable\_shipping\_carrier\_validation\_asn system property must be set to **false**.
-   [Receive an asset](../../procurement/task/t_ReceiveAnAsset.md): When the assets are received.

**Note:** The shipment record is created in the Delivered stage.


</td><td>

The purchase order is received.

</td></tr><tr><td>

Transfer order

</td><td>

The Ship task of the Transfer order line item is closed.

</td><td>

The transfer order line item is delivered.**Note:** You can change the tracking number until the Transfer order line item is in the In Transit stage.

</td></tr><tr><td>

Lease expiration

</td><td>

The Ship task of the Return lease action is closed.

</td><td>

Return confirmation task is closed.

</td></tr><tr><td>

Return Merchandise Authorization \(RMA\)

</td><td>

1.  The Shipment task of the Off-site return action is closed.
2.  The Vendor RMA decision task is closed.

</td><td>

1.  Vendor RMA decision task is closed.
2.  The Receive task is closed.

</td></tr><tr><td>

Asset reclamation

</td><td>

The Schedule shipment task for the Ship reclaim method is closed.

</td><td>

The Receive asset task is closed.

</td></tr><tr><td>

Zero Touch Refresh

</td><td>

The Request shipment task is closed.

</td><td>

The User asset receive task is closed.

</td></tr></tbody>
</table>**Parent Topic:**[Hardware Asset Management reference](../concept/reference-hardware-asset-management.md)

