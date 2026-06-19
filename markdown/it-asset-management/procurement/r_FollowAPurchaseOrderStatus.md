---
title: Purchase order status
description: Purchase orders follow a specific life cycle. The Status field on the purchase order record is always read-only.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/procurement/r\_FollowAPurchaseOrderStatus.html
release: australia
product: Procurement
classification: procurement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a purchase order, Procurement purchase order management for assets, Procurement, IT Asset Management]
---

# Purchase order status

Purchase orders follow a specific life cycle. The **Status** field on the purchase order record is always read-only.

\[Omitted image "mmasset0021989-purchase-order-status.png"\] Alt text: Purchase Order status

|Status|Description|
|------|-----------|
|Requested|The status is **Requested** when you create a purchase order.|
|Ordered|The status changes to **Ordered** when you add [purchase order line items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_CreateAPurchaseOrderLineItem.md), and select **Order**.|
|Pending Delivery|When you [create assets before receiving them](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_CreateAssetReserveForRequester.md) as a purchase order line item, the status of purchase orders and purchase order line items changes to **Pending Delivery** status.|
|Received|When ordered assets arrive in the specified stockroom and you click **Receive**, the status of purchase orders and purchase order line items changes to **Received**.|
|Canceled|You can cancel a purchase order if its status is **Requested**, **Ordered**, or **Pending Delivery**. For more information, see [Cancel a purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_CancelAPurchaseOrder.md).|

**Parent Topic:**[Create a purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_CreateAPurchaseOrder.md)

