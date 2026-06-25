---
title: Receive assets
description: Assets can be received and added to the system when they are delivered to a stockroom.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/procurement/c\_ReceiveAssets.html
release: australia
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Procurement, IT Asset Management]
---

# Receive assets

Assets can be received and added to the system when they are delivered to a stockroom.

Users with an appropriate procurement role can receive assets. If one purchase order contains multiple purchase order lines, the lines can be received at different times. This is useful if items arrive at the stockroom in different shipments. The purchase order status does not change to **Received** until all purchase order lines are received.

As an alternative to receiving assets when they arrive, you can create assets [before they arrive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_CreateAssetReserveForRequester.md) and reserve them for the requester.

-   **[Receive an asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_ReceiveAnAsset.md)**  
When assets are received and delivered to a stockroom, they’re added to the system.
-   **[Create a receiving slip](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_CreateAReceivingSlip.md)**  
Receiving slips are created automatically during the process of receiving assets. You can also create receiving slips manually.
-   **[Create a receiving slip line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_CreateAReceivingSlipLine.md)**  
When assets arrive at a stockroom and you receive them, a receiving slip is created on the purchase order. You create a receiving slip line to identify the specific assets and quantities that were received.
-   **[Consumable assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/c_ReceiveAConsumableAsset.md)**  
A consumable asset is one that is purchased in quantity and distributed. It is assigned to the consumable model category, and the asset record tracks the quantity that is available and total cost. When consumable assets are received, they are merged into an existing consumable record, if available.

**Parent Topic:**[Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/c_Procurement.md)

**Related topics**  


[Procurement roles]()

[Procurement workflows]()

[Use the Procurement Overview module]()

[Activate Procurement]()

[Sourcing items in a service catalog request]()

[Procurement purchase order management for assets]()

[Domain separation and Procurement]()

