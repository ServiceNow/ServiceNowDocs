---
title: Create a shipping carrier record
description: Create a shipping carrier record used to associate the carrier with an integration profile.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Track shipments using the integration framework, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create a shipping carrier record

Create a shipping carrier record used to associate the carrier with an integration profile.

## Before you begin

Role required: inventory\_admin

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

The shipping carrier record is created and added to the Shipping carriers list.

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

