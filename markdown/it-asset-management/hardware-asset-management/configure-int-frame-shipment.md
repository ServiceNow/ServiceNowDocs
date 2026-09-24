---
title: Integration framework configuration for shipment tracking
description: Configure the integration framework for Hardware Asset Management \(HAM\) to connect to external shipping carriers so that inbound shipments are tracked in real time and asset records are updated automatically when hardware asset arrives.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/configure-int-frame-shipment.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Integrations and advanced configuration, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Integration framework configuration for shipment tracking

Configure the integration framework for Hardware Asset Management \(HAM\) to connect to external shipping carriers so that inbound shipments are tracked in real time and asset records are updated automatically when hardware asset arrives.

The following configuration tasks enable shipment tracking for a carrier. For details on requirements for integration with third-party carrier applications, see [Managing shipments by integrating with third-party carrier applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/integrating-with-third-party-carrier-apps.md).

|Step|Configuration task|Purpose|Required|
|----|------------------|-------|--------|
|1|[Create an integration script include](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/creating-integration-script-include-ham.md)|Defines the logic HAM uses to communicate with the carrier API|Yes|
|2|[Create a carrier integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-carrier-integration-profile.md)|Stores the carrier API credentials and endpoint details|Yes|
|3|[Associate a shipping carrier with an integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/associate-shipping-carrier-int-profile.md)|Links a carrier record to its integration profile so HAM knows which profile to use for each carrier|Yes|
|4|[Test the carrier API integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/test-carrier-api-integration.md)|Validates that HAM can connect to the carrier API and retrieve shipment data|Yes|
|5|[Create a shipping carrier record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-shipping-carrier.md)|Creates the carrier record that HAM associates with shipments|Yes|
|6|[Remove a shipping carrier from an integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/remove-shipping-carrier.md)Remove a shipping carrier|Removes a carrier record that is no longer in use|As needed|

-   **[Creating an integration script include for third-party carrier applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/creating-integration-script-include-ham.md)**  
In order to integrate with a ServiceNow instance, a third-party carrier application must have a script include that extends the base class `ITAMShipmentIntegration` script on its ServiceNow instance to receive the shipment tracking number from the customer's ServiceNow instance and respond with the carrier-related details.
-   **[Create a carrier integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-carrier-integration-profile.md)**  
Create a carrier integration profile for your carrier by specifying the API and connection details that are used to connect your ServiceNow instance to the third-party shipping carrier application.
-   **[Connect your ServiceNow instance with a shipping carrier application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/associate-shipping-carrier-int-profile.md)**  
Associate a shipping carrier with an integration profile to connect your ServiceNow instance to the carrier application.
-   **[Test the integration with the carrier API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/test-carrier-api-integration.md)**  
Check the connection with the carrier API to handle any connection issues such as invalid credentials, incorrect tracking details, and issues with the integration script include.
-   **[Create a shipping carrier record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-shipping-carrier.md)**  
Create a shipping carrier record used to associate the carrier with an integration profile.
-   **[Remove a shipping carrier from an integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/remove-shipping-carrier.md)**  
Remove a shipping carrier that you no longer want to associate with an integration profile.

**Parent Topic:**[Integrations and advanced configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/integrations-advncd-configs.md)

