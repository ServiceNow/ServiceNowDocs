---
title: Create a shipping carrier record
description: Create a shipping carrier record in the Hardware Asset Workspace.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Track shipments using the integration framework, Use, Hardware Asset Management, IT Asset Management]
---

# Create a shipping carrier record

Create a shipping carrier record in the Hardware Asset Workspace.

## Before you begin

Role required: inventory\_admin

## About this task

Create a shipping carrier record used to associate the carrier with an integration profile.

**Important:** When using the Sourcing and Procurement Operations application with the Asset Management Integration for Sourcing and Procurement Operations \(com.snc.sn\_spend\_asset\) installed, the IT Asset Management application shares shipment details with the Sourcing and Procurement Operations application. To enable the Sourcing and Procurement Operations application to view shipment and tracking numbers associated with Purchase Orders, read-only access has been provided to the Shipping carrier \[sn\_itam\_common\_shipping\_carrier\] table.

For more information about the Asset Management Integration for Sourcing and Procurement Operations \(com.snc.sn\_spend\_asset\) plugin, see [Sourcing and Procurement Operations integration with IT Asset Management](https://www.servicenow.com/docs/access?context=spo-itam-better-together&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Shipment** list, select **Shipping carriers**.

3.  Select **New**.

4.  Provide the contact details of the carrier.

5.  On the form, fill in the remaining fields.

<table id="table_y5c_5d5_kxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the shipping carrier. This field is required.

</td></tr><tr><td>

Company

</td><td>

Core company of the shipping carrier.

</td></tr><tr><td>

Integration profile

</td><td>

Profile for integrating with the third-party carrier's application.For more details, see [View the carrier integration profile details](view-integration-profiles.md).

</td></tr><tr><td>

Status

</td><td>

Status of the carrier. This field is set to **Active** by default.

</td></tr><tr><td>

Max wait days

</td><td>

Maximum days that the carrier takes to deliver a shipment.By default, this field is set to 90. You can change this value.

**Note:** This field isn’t shown on the form by default. You can choose to display this field on the form.

A shipment record that is not updated by the carrier after the integration profile job has run for the specified maximum wait days is marked as stale shipment by The ITAM: Process integration profiles and stale shipment job.

</td></tr><tr><td>

Notes

</td><td>

Additional information about the carrier.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

-   The shipping carrier record is created and added to the Shipping carriers list.
-   The shipping carrier record is saved in the Shipping carrier \[sn\_itam\_common\_shipping\_carrier\] table.

**Parent Topic:**[Track shipments using the integration framework](../concept/tracking-shipments-using-integration-framework.md)

**Related topics**  


[Creating an integration script include for third-party carrier applications](../concept/creating-integration-script-include-ham.md)

[Connect your ServiceNow instance with a shipping carrier application](associate-shipping-carrier-int-profile.md)

[Remove a shipping carrier from an integration profile](remove-shipping-carrier.md)

[Create a carrier integration profile](create-carrier-integration-profile.md)

[View the carrier integration profile details](view-integration-profiles.md)

[Test the integration with the carrier API](test-carrier-api-integration.md)

[View hardware asset shipment details](view-hardware-asset-shipments.md)

[Stale shipments](../concept/stale-shipments.md)

[Track a hardware asset shipment](track-hardware-asset-shipments.md)

