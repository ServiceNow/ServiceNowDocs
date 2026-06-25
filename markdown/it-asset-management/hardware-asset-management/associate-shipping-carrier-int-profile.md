---
title: Connect your ServiceNow instance with a shipping carrier application
description: Associate a shipping carrier with an integration profile to connect your ServiceNow instance to the carrier application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/associate-shipping-carrier-int-profile.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Track shipments using the integration framework, Use, Hardware Asset Management, IT Asset Management]
---

# Connect your ServiceNow instance with a shipping carrier application

Associate a shipping carrier with an integration profile to connect your ServiceNow instance to the carrier application.

## Before you begin

Make sure that the shipping carrier that you want to associate with an integration profile has a shipping carrier record. For more details, see [Create a shipping carrier record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-shipping-carrier.md).

Role required: admin or domain\_admin

## About this task

A shipping carrier can be associated with only one active integration profile.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset operations**.

2.  From the **Shipment** list, select **Carrier integration profiles**.

3.  Select the carrier integration profile that you want to associate with a shipping carrier.

    **Note:** The third-party carrier application automatically inserts records into the Carrier integration profiles list. If the integration profile associated with your carrier isn't listed, make sure that the prerequisites for the integration with the carrier are fulfilled. For more information, see [Managing shipments by integrating with third-party carrier applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/integrating-with-third-party-carrier-apps.md).

4.  Select the **Shipping Carriers** tab.

5.  Associate the shipping carrier with the carrier integration profile.

    1.  Select **Add**.

    2.  In the **Add carriers** dialog box, select the carrier and select **Add**.

        **Note:** If the carrier you intended to associate is not listed, it likely is already associated with an integration profile.


## Result

The shipping carrier is associated with the profile and the carrier details are shown in the **Shipping Carriers** tab.

**Parent Topic:**[Track shipments using the integration framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/tracking-shipments-using-integration-framework.md)

**Related topics**  


[Creating an integration script include for third-party carrier applications]()

[Remove a shipping carrier from an integration profile]()

[Create a carrier integration profile]()

[View the carrier integration profile details]()

[Test the integration with the carrier API]()

[Create a shipping carrier record]()

[View hardware asset shipment details]()

[Stale shipments]()

[Track a hardware asset shipment]()

