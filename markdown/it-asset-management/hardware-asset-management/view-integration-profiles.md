---
title: View the carrier integration profile details
description: View the details of the carrier API used to connect your ServiceNow instance to the third-party shipping carrier application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/view-integration-profiles.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Track shipments using the integration framework, Use, Hardware Asset Management, IT Asset Management]
---

# View the carrier integration profile details

View the details of the carrier API used to connect your ServiceNow instance to the third-party shipping carrier application.

## Before you begin

Role required: admin, domain\_admin, asset, inventory\_admin, or sn\_hamp.ham\_system\_admin

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Shipment** list, select **Carrier integration profiles**.

    The third-party carrier application automatically inserts records into the Carrier integration profiles list. You can also create a carrier integration profile.

3.  Select the carrier integration profile of your carrier.

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

Name of the scheduled job that invokes the carrier API to fetch the shipments details. This job is created by a job that runs daily, The ITAM: Process integration profiles and stale shipment job.

</td></tr><tr><td>

Active

</td><td>

Option that indicates the status of the integration profile.**Note:** Only users with the admin or domain\_admin role can deactivate the integration profile but they can’t delete the integration profile. When an integration profile is deactivated, the associated job that invokes the carrier API is deactivated automatically.

</td></tr></tbody>
</table>
**Parent Topic:**[Track shipments using the integration framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/tracking-shipments-using-integration-framework.md)

**Related topics**  


[Creating an integration script include for third-party carrier applications]()

[Connect your ServiceNow instance with a shipping carrier application]()

[Remove a shipping carrier from an integration profile]()

[Create a carrier integration profile]()

[Test the integration with the carrier API]()

[Create a shipping carrier record]()

[View hardware asset shipment details]()

[Stale shipments]()

[Track a hardware asset shipment]()

