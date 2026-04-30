---
title: Receive assets
description: Assets can be received and added to the system when they are delivered to a stockroom.
locale: en-US
release: yokohama
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Procurement, Asset Management, IT Service Management]
---

# Receive assets

Assets can be received and added to the system when they are delivered to a stockroom.

Users with an appropriate procurement role can receive assets. If one purchase order contains multiple purchase order lines, the lines can be received at different times. This is useful if items arrive at the stockroom in different shipments. The purchase order status does not change to **Received** until all purchase order lines are received.

As an alternative to receiving assets when they arrive, you can create assets [before they arrive](../task/t_CreateAssetReserveForRequester.md) and reserve them for the requester.

-   **[Receive an asset](../task/t_ReceiveAnAsset.md)**  
When assets are received and delivered to a stockroom, they’re added to the system.
-   **[Create a receiving slip](../task/t_CreateAReceivingSlip.md)**  
Receiving slips are created automatically during the process of receiving assets. You can also create receiving slips manually.
-   **[Create a receiving slip line](../task/t_CreateAReceivingSlipLine.md)**  
When assets arrive at a stockroom and you receive them, a receiving slip is created on the purchase order. You create a receiving slip line to identify the specific assets and quantities that were received.
-   **[Consumable assets](c_ReceiveAConsumableAsset.md)**  
A consumable asset is one that is purchased in quantity and distributed. It is assigned to the consumable model category, and the asset record tracks the quantity that is available and total cost. When consumable assets are received, they are merged into an existing consumable record, if available.

**Parent Topic:**[Procurement](c_Procurement.md)

**Related topics**  


[Procurement roles](../reference/r_ProcurementRoles.md)

[Procurement workflows](c_ProcurementWorkflows.md)

[Use the Procurement Overview module](../task/t_UsingTheProcurementOverviewModule.md)

[Activate Procurement](../task/t_ActivateProcurement.md)

[Sourcing items in a service catalog request](c_SourcingRequestItems.md)

[Procurement purchase order management for assets](c_UseProcurement.md)

[Domain separation and Procurement](domain-separation-procurement.md)

