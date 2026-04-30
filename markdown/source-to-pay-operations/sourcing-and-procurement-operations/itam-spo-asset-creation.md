---
title: Asset creation process in IT Asset Management
description: In IT Asset Management \(ITAM\), assets are created when you acknowledge the receipt of the requested items.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sourcing and Procurement Operations integration with IT Asset Management, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Asset creation process in IT Asset Management

In IT Asset Management \(ITAM\), assets are created when you acknowledge the receipt of the requested items.

After receiving is completed, receiving slips are generated in ITAM, the associated assets are created, and the status of the PO is updated to Received. You can view the created assets in the **Assets** tab of the ITAM purchase order. For more information, see [Receiving assets in IT Asset Management](itam-spo-receiving-assets.md).![Assets tab shows the created assets and the ITAM PO status updates to Received.](../image/itam-spo-assets-tab.png)

Additionally, when receiving slips are generated in ITAM, corresponding read-only receipts are created in SPO.

The following occurs during the asset creation process in ITAM:

-   When a Hardware Asset Management \(HAM\) or Enterprise Asset Management \(EAM\) asset is received, ITAM creates a corresponding record in the alm\_asset table.
-   When a Software Asset Management \(SAM\) item is received, ITAM creates a corresponding entitlement in the alm\_license table.
-   When a consumable is received, ITAM creates a corresponding entitlement in the alm\_consumable table.

**Parent Topic:**[Sourcing and Procurement Operations integration with IT Asset Management](spo-itam-better-together.md)

