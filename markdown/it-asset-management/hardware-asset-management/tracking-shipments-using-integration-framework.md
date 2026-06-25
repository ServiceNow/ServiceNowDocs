---
title: Track shipments using the integration framework
description: Track your shipments in real time by integrating your ServiceNow instance with your third-party carrier's application through the integration framework provided by the IT Asset Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/tracking-shipments-using-integration-framework.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Track shipments using the integration framework

Track your shipments in real time by integrating your ServiceNow instance with your third-party carrier's application through the integration framework provided by the IT Asset Management application.

-   **[Creating an integration script include for third-party carrier applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/creating-integration-script-include-ham.md)**  
In order to integrate with a ServiceNow instance, a third-party carrier application must have a script include that extends the base class `ITAMShipmentIntegration` script on its ServiceNow instance to receive the shipment tracking number from the customer's ServiceNow instance and respond with the carrier-related details.
-   **[Connect your ServiceNow instance with a shipping carrier application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/associate-shipping-carrier-int-profile.md)**  
Associate a shipping carrier with an integration profile to connect your ServiceNow instance to the carrier application.
-   **[Remove a shipping carrier from an integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/remove-shipping-carrier.md)**  
Remove a shipping carrier that you no longer want to associate with an integration profile.
-   **[Create a carrier integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-carrier-integration-profile.md)**  
Create a carrier integration profile for your carrier by specifying the API and connection details that are used to connect your ServiceNow instance to the third-party shipping carrier application.
-   **[View the carrier integration profile details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/view-integration-profiles.md)**  
View the details of the carrier API used to connect your ServiceNow instance to the third-party shipping carrier application.
-   **[Test the integration with the carrier API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/test-carrier-api-integration.md)**  
Check the connection with the carrier API to handle any connection issues such as invalid credentials, incorrect tracking details, and issues with the integration script include.
-   **[Create a shipping carrier record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-shipping-carrier.md)**  
Create a shipping carrier record used to associate the carrier with an integration profile.
-   **[View hardware asset shipment details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/view-hardware-asset-shipments.md)**  
View all hardware asset shipment details in a single place in the Hardware Asset Workspace.
-   **[Stale shipments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/stale-shipments.md)**  
Shipments that are delayed due to various reasons such as an incorrect tracking number, the loss of a shipment package during transit, and invalid connection details are considered stale shipments.
-   **[Track a hardware asset shipment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/track-hardware-asset-shipments.md)**  
Track the progress of your hardware asset shipment that isn't delivered and that has a carrier associated with an active integration profile.

**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Analyze hardware assets using the Generate hardware asset insights generative AI skill]()

[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

