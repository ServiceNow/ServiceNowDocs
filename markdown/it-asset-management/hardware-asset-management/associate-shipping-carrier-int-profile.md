---
title: Connect your ServiceNow instance with a shipping carrier application
description: Associate a shipping carrier with an integration profile to connect your ServiceNow instance to the carrier application.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Track shipments using the integration framework, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Connect your ServiceNow instance with a shipping carrier application

Associate a shipping carrier with an integration profile to connect your ServiceNow instance to the carrier application.

## Before you begin

Make sure that the shipping carrier that you want to associate with an integration profile has a shipping carrier record. For more details, see [Create a shipping carrier record](create-shipping-carrier.md).

Role required: admin or domain\_admin

## About this task

A shipping carrier can be associated with only one active integration profile.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Shipment** list, select **Carrier integration profiles**.

3.  Select the carrier integration profile that you want to associate with a shipping carrier.

    **Note:** The third-party carrier application automatically inserts records into the Carrier integration profiles list. If the integration profile associated with your carrier isn't listed, make sure that the prerequisites for the integration with the carrier are fulfilled. For more information, see [Managing shipments by integrating with third-party carrier applications](../concept/integrating-with-third-party-carrier-apps.md).

4.  Select the **Shipping Carriers** tab.

5.  Associate the shipping carrier with the carrier integration profile.

    1.  Select **Add**.

    2.  In the **Add carriers** dialog box, select the carrier and select **Add**.

        **Note:** If the carrier you intended to associate is not listed, it likely is already associated with an integration profile.


## Result

The shipping carrier is associated with the profile and the carrier details are shown in the **Shipping Carriers** tab.

**Parent Topic:**[Track shipments using the integration framework](../concept/tracking-shipments-using-integration-framework.md)

**Related topics**  


[Creating an integration script include for third-party carrier applications](../concept/creating-integration-script-include-ham.md)

[Remove a shipping carrier from an integration profile](remove-shipping-carrier.md)

[Create a carrier integration profile](create-carrier-integration-profile.md)

[View the carrier integration profile details](view-integration-profiles.md)

[Test the integration with the carrier API](test-carrier-api-integration.md)

[Create a shipping carrier record](create-shipping-carrier.md)

[View hardware asset shipment details](view-hardware-asset-shipments.md)

[Stale shipments](../concept/stale-shipments.md)

[Track a hardware asset shipment](track-hardware-asset-shipments.md)

