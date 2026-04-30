---
title: Purchase order status
description: Purchase orders follow a specific life cycle. The Status field on the purchase order record is always read-only.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a purchase order, Procurement purchase order management for assets, Procurement, Asset Management, IT Service Management]
---

# Purchase order status

Purchase orders follow a specific life cycle. The **Status** field on the purchase order record is always read-only.

![Purchase order status](../image/PurchaseOrderStatus.png "Purchase order status")

|Status|Description|
|------|-----------|
|Requested|The status is **Requested** when you create a purchase order.|
|Ordered|The status changes to **Ordered** when you add [purchase order line items](../task/t_CreateAPurchaseOrderLineItem.md), and click **Order**.|
|Pending Delivery|When you [create assets before receiving them](../task/t_CreateAssetReserveForRequester.md) as a purchase order line item, the status of purchase orders and purchase order line items changes to **Pending Delivery** status.|
|Received|When ordered assets arrive in the specified stockroom and you click **Receive**, the status of purchase orders and purchase order line items changes to **Received**.|
|Canceled|You can cancel a purchase order if its status is **Requested**, **Ordered**, or **Pending Delivery**. For more information, see [Cancel a purchase order](../task/t_CancelAPurchaseOrder.md).|

**Parent Topic:**[Create a purchase order](../task/t_CreateAPurchaseOrder.md)

