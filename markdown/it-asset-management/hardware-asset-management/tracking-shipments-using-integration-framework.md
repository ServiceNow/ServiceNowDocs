---
title: Track shipments using the integration framework
description: Track your shipments in real time by integrating your ServiceNow instance with your third-party carrier's application through the integration framework provided by the IT Asset Management application.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Track shipments using the integration framework

Track your shipments in real time by integrating your ServiceNow instance with your third-party carrier's application through the integration framework provided by the IT Asset Management application.

-   **[Creating an integration script include for third-party carrier applications](creating-integration-script-include-ham.md)**  
In order to integrate with a ServiceNow instance, a third-party carrier application must have a script include that extends the base class `ITAMShipmentIntegration` script on its ServiceNow instance to receive the shipment tracking number from the customer's ServiceNow instance and respond with the carrier-related details.
-   **[Connect your ServiceNow instance with a shipping carrier application](../task/associate-shipping-carrier-int-profile.md)**  
Associate a shipping carrier with an integration profile to connect your ServiceNow instance to the carrier application.
-   **[Remove a shipping carrier from an integration profile](../task/remove-shipping-carrier.md)**  
Remove a shipping carrier that you no longer want to associate with an integration profile.
-   **[Create a carrier integration profile](../task/create-carrier-integration-profile.md)**  
Create a carrier integration profile for your carrier by specifying the API and connection details that are used to connect your ServiceNow instance to the third-party shipping carrier application.
-   **[View the carrier integration profile details](../task/view-integration-profiles.md)**  
View the details of the carrier API used to connect your ServiceNow instance to the third-party shipping carrier application.
-   **[Test the integration with the carrier API](../task/test-carrier-api-integration.md)**  
Check the connection with the carrier API to handle any connection issues such as invalid credentials, incorrect tracking details, and issues with the integration script include.
-   **[Create a shipping carrier record](../task/create-shipping-carrier.md)**  
Create a shipping carrier record used to associate the carrier with an integration profile.
-   **[View hardware asset shipment details](../task/view-hardware-asset-shipments.md)**  
View all hardware asset shipment details in a single place in the Hardware Asset Workspace.
-   **[Stale shipments](stale-shipments.md)**  
Shipments that are delayed due to various reasons such as an incorrect tracking number, the loss of a shipment package during transit, and invalid connection details are considered stale shipments.
-   **[Track a hardware asset shipment](../task/track-hardware-asset-shipments.md)**  
Track the progress of your hardware asset shipment that isn't delivered and that has a carrier associated with an active integration profile.

**Parent Topic:**[Using Hardware Asset Management](using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](Work-with-hardware-normalization.md)

[Manage asset bundles from your inventory](../task/create-bundled-assets.md)

[Manage your inventory through pallet assets](pallets-for-inventory-management.md)

[Manage loaner assets](../task/manage-loaner-asset.md)

[Donate assets to charity organizations](donate-asset-to-charity-organizations.md)

[Use Advanced Shipment Notification](../task/advanced-shipment-notification.md)

[Manage RMA requests](manage-rma-req.md)

[Create an inventory stock order request](../task/create-inventory-stock-order.md)

[Create a disposal order](../task/create-disposal-order.md)

[Use a hardware asset request flow](../task/hardware-request-flow.md)

[Audit hardware asset inventory](ham-inventory-audit.md)

[Request a Hardware Asset Refresh](../task/hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](../task/manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](manage-asset-reclaim.md)

[View RFID information of assets](../task/view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](receive-warranty-details-lenovo.md)

[Manage stockrooms](manage-your-stockrooms.md)

[Track asset location using indoor maps](../task/track-asset-location-using-indoor-maps.md)

[Assess performance of Hardware Asset Management](suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](configure-ham-tco.md)

[Manage and monitor hardware asset performance](manage-and-monitor-hardware-asset-performance.md)

[Manage Hardware Asset Management subscriptions](managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](manage-asset-picking-stockroom-ham-ws.md)

[Manage asset put away using the Hardware Asset Workspace](manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Manage hardware asset tasks using the Mobile Agent application](manage-hardware-asset-tasks-mobile-agent.md)

[Audit your hardware assets by using Asset Attestation](audit-hardware-assets-attestation.md)

[Acknowledge receipt of assets on the Employee Center portal](../task/receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](../task/trigger-flow-ham.md)

