---
title: Asset creation process in Asset Management
description: In ServiceNow's Asset Management product suite, assets are created when you acknowledge the receipt of the requested items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-asset-creation.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sourcing and Procurement Operations and Asset Management integration, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Asset creation process in Asset Management

In ServiceNow's Asset Management product suite, assets are created when you acknowledge the receipt of the requested items.

After receiving is completed, receiving slips are generated in Asset Management, the associated assets are created, and the status of the PO is updated to Received. You can view the created assets in the **Assets** tab of the Asset Management purchase order. For more information, see [Receiving assets in Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-receiving-assets.md).\[Omitted image "itam-spo-assets-tab.png"\] Alt text: Assets tab shows the created assets and the Asset Management PO status updates to Received.

Additionally, when receiving slips are generated in Asset Management, corresponding read-only receipts are created in SPO.

The following occurs during the asset creation process in Asset Management:

-   When a Hardware Asset Management \(HAM\) or Enterprise Asset Management \(EAM\) asset is received, Asset Management creates a corresponding record in the alm\_asset table.
-   When a Software Asset Management \(SAM\) item is received, Asset Management creates a corresponding entitlement in the alm\_license table.
-   When a consumable is received, Asset Management creates a corresponding entitlement in the alm\_consumable table.

**Parent Topic:**[Sourcing and Procurement Operations integration with Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-itam-better-together.md)

