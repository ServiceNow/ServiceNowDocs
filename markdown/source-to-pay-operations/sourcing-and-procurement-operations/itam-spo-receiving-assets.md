---
title: Receiving assets in IT Asset Management
description: As part of the Better Together integration, all asset receiving is handled within IT Asset Management \(ITAM\). When an item is initially received in ITAM, a receipt is automatically generated in SPO in the Pending Submission state.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sourcing and Procurement Operations integration with IT Asset Management, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Receiving assets in IT Asset Management

As part of the Better Together integration, all asset receiving is handled within IT Asset Management \(ITAM\). When an item is initially received in ITAM, a receipt is automatically generated in SPO in the Pending Submission state.

After the buyer confirms receipt against the purchase order in ITAM, a corresponding receipt is automatically created for the associated purchase order in Sourcing and Procurement Operations. For more information about receiving assets in ITAM, see [Receive an asset](https://www.servicenow.com/docs/access?context=t_ReceiveAnAsset&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

After the receipt is posted to the ERP system, the status of the SPO receipt changes to Posted.

**Note:** The SPO receipt is read-only and cannot be modified.

To support seamless integration between SPO and ITAM, both the receipt and shipment tables in each application are retained. The required field mappings have been configured to enable data flow between both the applications.

As part of the receiving process, the ITAM receipt passes relevant data to the SPO receipt, which is read-only. ITAM also creates the associated assets.

As part of the shipment process, the ITAM shipment record passes shipment details to the SPO shipment record, which is also read-only.

After receiving the requested items, the asset manager or an employee can acknowledge receipt using the following ITAM receiving experiences:

-   Mobile barcode scanning. For more information, see [Acknowledge receipt of an asset on a mobile device](https://www.servicenow.com/docs/access?context=receive-assets-from-ztr&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

    ![Asset receiving via mobile barcode scanning.](../image/itam-spo-barcode.png)

-   From the Employee Center portal. For more information, see [Acknowledge receipt of assets on the Employee Center portal](https://www.servicenow.com/docs/access?context=receive-assets-employee-center&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

    ![Asset receiving from Employee Center.](../image/itam-spo-receive-ec.png)

-   From the ITAM purchase order. For more information, see [Receive an asset](https://www.servicenow.com/docs/access?context=t_ReceiveAnAsset&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

    .![Asset receiving via ITAM purchase orders.](../image/itam-spo-receive-po.png)


**Parent Topic:**[Sourcing and Procurement Operations integration with IT Asset Management](spo-itam-better-together.md)

