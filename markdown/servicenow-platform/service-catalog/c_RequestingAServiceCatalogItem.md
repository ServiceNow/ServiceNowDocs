---
title: Service Catalog request screens
description: To place a request from a service catalog, navigate to the catalog home page and select the item to order.When a customer orders something from the catalog, a request is generated to track the order.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Catalog for managers and end users, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog request screens

To place a request from a service catalog, navigate to the catalog home page and select the item to order.

When an item is ordered, the base system generates a request to track the order and displays a summary that includes the order status in the **Stage** column:

![Service Catalog Request Status](../image/SC_RequestCatalogItem.png "Service Catalog Request Status")

Each individual catalog item in a request creates a discrete request item. For example, a request for 2 PCs, 1 chair, and 1 desk would produce four request items on a single request.

## Shopping cart screens

The shopping cart screen displays previews of the cart immediately before an order is placed.

You can configure the layout for either the one-step or two-step catalog checkout process.

## Order status screens

The order status screen is the final summary screen a user sees in the service catalog after placing an order successfully.

**Parent Topic:**[Service Catalog for managers and end users](c_UsingTheServiceCatalog.md)

## Request generation for a Service Catalog item

When a customer orders something from the catalog, a request is generated to track the order.

The user specified in the **Opened By** field of a Requested Item \(sc\_req\_item\) record has read access to it.

Each individual catalog item that is part of a request creates a discrete request item with the request.

For example, a request for 2 PCs, 1 Chair, and 1 Desk would produce:

Request REQ0000001 -- 4 Things

-   Requested item RITM0000001 -- 2 X PC
-   Requested item RITM0000002 -- 1 X Chair
-   Requested item RITM0000003 -- 1 X Desk

After a service catalog request is submitted, a fulfiller may determine that the item is not in stock. The full filler can select the **Backordered** check box, and enter comments about when the item may be back in stock. The backorder status can be used in reports and dashboards.

If a service catalog request is canceled, all associated purchase orders and transfer orders that have not been received are canceled.

**Related topics**  


[Service Catalog home page](c_ViewNavSvrCat.md#)

