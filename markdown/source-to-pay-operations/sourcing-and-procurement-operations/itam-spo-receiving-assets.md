---
title: Receiving assets in Asset Management
description: As part of the Better Together integration, all asset receiving is handled within ServiceNow's Asset Management product suite. When an item is initially received in Asset Management, a receipt is automatically generated in SPO in the Pending Submission state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-receiving-assets.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sourcing and Procurement Operations and Asset Management integration, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Receiving assets in Asset Management

As part of the Better Together integration, all asset receiving is handled within ServiceNow's Asset Management product suite. When an item is initially received in Asset Management, a receipt is automatically generated in SPO in the Pending Submission state.

After the buyer confirms receipt against the purchase order in Asset Management, a corresponding receipt is automatically created for the associated purchase order in Sourcing and Procurement Operations. For more information about receiving assets in Asset Management, see [Receive an asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/t_ReceiveAnAsset.md).

After the receipt is posted to the ERP system, the status of the SPO receipt changes to Posted.

**Note:** The SPO receipt is read-only and cannot be modified.

To support seamless integration between SPO and Asset Management, both the receipt and shipment tables in each application are retained. The required field mappings have been configured to enable data flow between both the applications.

As part of the receiving process, the Asset Management receipt passes relevant data to the SPO receipt, which is read-only. Asset Management also creates the associated assets.

As part of the shipment process, the Asset Management shipment record passes shipment details to the SPO shipment record, which is also read-only.

After receiving the requested items, the asset manager or an employee can acknowledge receipt using the following Asset Management receiving experiences:

-   Mobile barcode scanning. For more information, see [Acknowledge receipt of an asset on a mobile device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/receive-assets-from-ztr.md).

    \[Omitted image "itam-spo-barcode.png"\] Alt text: Asset receiving via mobile barcode scanning.

-   From the Employee Center portal. For more information, see [Acknowledge receipt of assets on the Employee Center portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/receive-assets-employee-center.md).

    \[Omitted image "itam-spo-receive-ec.png"\] Alt text: Asset receiving from Employee Center.

-   From the Asset Management purchase order. For more information, see [Receive an asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/t_ReceiveAnAsset.md).

    .\[Omitted image "itam-spo-receive-po.png"\] Alt text: Asset receiving via Asset Management purchase orders.


**Parent Topic:**[Sourcing and Procurement Operations integration with Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-itam-better-together.md)

