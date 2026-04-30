---
title: Stale shipments
description: Shipments that are delayed due to various reasons such as an incorrect tracking number, the loss of a shipment package during transit, and invalid connection details are considered stale shipments.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Track shipments using the integration framework, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Stale shipments

Shipments that are delayed due to various reasons such as an incorrect tracking number, the loss of a shipment package during transit, and invalid connection details are considered stale shipments.

The ITAM: Process integration profiles and stale shipment job runs daily to check for any stale shipments. A shipment record that is not updated by the carrier even after the integration profile job has run for the maximum wait days for a carrier is marked as stale shipment.

The tracking number of the shipment record that is marked stale isn’t sent to the carrier for further tracking. If you know the reason that a shipment is late, you can decide to continue tracking it. For more information, see [Continue to track delayed shipments](../task/track-delayed-shipments.md).

**Note:** You can view the list of shipments that weren’t updated with the tracking information from the integrated carrier through the Stale shipments important actions card in the Inventory view. For more information, see [Inventory view](inventory-view.md).

-   **[Continue to track delayed shipments](../task/track-delayed-shipments.md)**  
Continue to track a stale hardware asset shipment that is delayed if the reason for the delay is known.

**Parent Topic:**[Track shipments using the integration framework](tracking-shipments-using-integration-framework.md)

**Related topics**  


[Creating an integration script include for third-party carrier applications](creating-integration-script-include-ham.md)

[Connect your ServiceNow instance with a shipping carrier application](../task/associate-shipping-carrier-int-profile.md)

[Remove a shipping carrier from an integration profile](../task/remove-shipping-carrier.md)

[Create a carrier integration profile](../task/create-carrier-integration-profile.md)

[View the carrier integration profile details](../task/view-integration-profiles.md)

[Test the integration with the carrier API](../task/test-carrier-api-integration.md)

[Create a shipping carrier record](../task/create-shipping-carrier.md)

[View hardware asset shipment details](../task/view-hardware-asset-shipments.md)

[Track a hardware asset shipment](../task/track-hardware-asset-shipments.md)

