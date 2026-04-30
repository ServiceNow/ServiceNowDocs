---
title: Create a carrier integration profile
description: Create a carrier integration profile for your carrier by specifying the API and connection details that are used to connect your ServiceNow instance to the third-party shipping carrier application.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Track shipments using the integration framework, Use, Hardware Asset Management, IT Asset Management]
---

# Create a carrier integration profile

Create a carrier integration profile for your carrier by specifying the API and connection details that are used to connect your ServiceNow instance to the third-party shipping carrier application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Shipment** list, select **Carrier integration profiles**.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_ejc_bcz_lxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the integration profile.

</td></tr><tr><td>

Connection details

</td><td>

Reference to the Connection and Credentials Aliases table that stores the credentials of the customer.**Note:** Your credentials must be updated in the Connection and Credentials Aliases table so that you’re authenticated to connect to the carrier API.

</td></tr><tr><td>

API

</td><td>

Name of the script that has the integration business logic.

</td></tr><tr><td>

Job

</td><td>

Name of the scheduled job that invokes the carrier API to fetch the shipment details.This job is automatically created by a job that runs daily, The ITAM: Process integration profiles and stale shipment job.

</td></tr><tr><td>

Active

</td><td>

Option that indicates the status of the integration profile.**Note:** You can only deactivate the integration profile but can’t delete the integration profile. When an integration profile is deactivated, the associated job that invokes the carrier API is deactivated automatically.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

The carrier integration profile is created and added to the Carrier integration profiles list.

**Parent Topic:**[Track shipments using the integration framework](../concept/tracking-shipments-using-integration-framework.md)

**Related topics**  


[Creating an integration script include for third-party carrier applications](../concept/creating-integration-script-include-ham.md)

[Connect your ServiceNow instance with a shipping carrier application](associate-shipping-carrier-int-profile.md)

[Remove a shipping carrier from an integration profile](remove-shipping-carrier.md)

[View the carrier integration profile details](view-integration-profiles.md)

[Test the integration with the carrier API](test-carrier-api-integration.md)

[Create a shipping carrier record](create-shipping-carrier.md)

[View hardware asset shipment details](view-hardware-asset-shipments.md)

[Stale shipments](../concept/stale-shipments.md)

[Track a hardware asset shipment](track-hardware-asset-shipments.md)

