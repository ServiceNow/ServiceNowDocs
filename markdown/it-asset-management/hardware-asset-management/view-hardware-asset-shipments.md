---
title: View hardware asset shipment details
description: View all hardware asset shipment details in a single place in the Hardware Asset Workspace.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Track shipments using the integration framework, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# View hardware asset shipment details

View all hardware asset shipment details in a single place in the Hardware Asset Workspace.

## Before you begin

Role required: inventory\_user \(read\) or inventory\_admin

## About this task

The Shipment list shows all the shipment records initiated by the shipment tasks of various flows. For details, see [Task closures that create shipment records](../reference/shipment-record-sources.md).

A shipment record is created automatically whenever a shipment task of a flow or process is closed.

**Note:**

The Shipment \[sn\_itam\_common\_shipment\] table also has the Currency, Delivery services cost, and Parcel weight fields. However, these fields aren’t shown on the Shipment form.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Shipment** list, select **Shipments**.

3.  Select a shipment record to view the shipment details.

<table id="table_l4v_cqf_4xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shipment number

</td><td>

Auto-generated and unique identifier for the shipment record.

</td></tr><tr><td>

Tracking number

</td><td>

Unique carrier tracking number for the shipment.Multiple orders or line items can have the same tracking number when they belong to the same shipment. Also, multiple line items that belong to the same order can have different tracking numbers when they’re part of different shipments.

</td></tr><tr><td>

Stage

</td><td>

Stage of the shipment record.A shipment can be in one of the following stages:

-   Draft
-   On Order
-   Prepare
-   In Transit
-   Delivered
-   Canceled
When a shipment has multiple orders, the Stage of the shipment record changes to **Delivered** when the shipment assets of an order are delivered.

</td></tr><tr><td>

Shipped from

</td><td>

Location from where the assets are shipped.This field is populated with the corresponding field of the order that created this record.

</td></tr><tr><td>

Shipped to

</td><td>

Location to which the assets are shipped.This field is populated with the corresponding field of the order that created this record.

</td></tr><tr><td>

Shipped by

</td><td>

Name of the person who shipped the assets.This field is populated with the corresponding field of the order that created this record.

</td></tr><tr><td>

Ship date

</td><td>

Date on which the assets are shipped.This field is populated with the corresponding field of the order that created this record.

The date corresponds to the date on which the ship task of the source is closed.

</td></tr><tr><td>

Shipment quantity

</td><td>

Quantity of assets shipped for the shipment record.This field value is automatically populated when the assets are shipped to the destination.

The shipment quantity is the sum of the asset quantities shipped for each shipment line.

**Important:** The **Shipment quantity** field is available with Hardware Asset Management version 14.0.0 onwards.

</td></tr><tr><td>

Receive date

</td><td>

Date on which the assets are received.This field is populated with the corresponding field of the order that is received first as part of the shipment.

The date corresponds to the date on which the receive task of the source is closed.

</td></tr><tr><td>

Received by

</td><td>

Name of the person to whom the assets are sent.This field is populated with the corresponding field of the order that is received first as part of the shipment.

</td></tr><tr><td>

Carrier

</td><td>

Reference to the shipping carrier record.

</td></tr><tr><td>

Carrier status

</td><td>

Status of the shipment.**Note:** This field is populated only when you integrate with your third-party carrier applications.

</td></tr><tr><td>

Carrier pick-up date

</td><td>

Date on which the carrier picked up the assets.**Note:** This field is populated only when you integrate with your third-party carrier applications.

</td></tr><tr><td>

Carrier delivered

</td><td>

Date on which the carrier delivered the assets.**Note:** This field is populated only when you integrate with your third-party carrier applications.

</td></tr><tr><td>

Carrier link

</td><td>

Link provided by the carrier to track the shipment.

</td></tr><tr><td>

Stale shipment

</td><td>

Option that indicates whether the shipment record is stale. This option is read-only.

</td></tr></tbody>
</table>
**Parent Topic:**[Track shipments using the integration framework](../concept/tracking-shipments-using-integration-framework.md)

**Related topics**  


[Creating an integration script include for third-party carrier applications](../concept/creating-integration-script-include-ham.md)

[Connect your ServiceNow instance with a shipping carrier application](associate-shipping-carrier-int-profile.md)

[Remove a shipping carrier from an integration profile](remove-shipping-carrier.md)

[Create a carrier integration profile](create-carrier-integration-profile.md)

[View the carrier integration profile details](view-integration-profiles.md)

[Test the integration with the carrier API](test-carrier-api-integration.md)

[Create a shipping carrier record](create-shipping-carrier.md)

[Stale shipments](../concept/stale-shipments.md)

[Track a hardware asset shipment](track-hardware-asset-shipments.md)

