---
title: External product inventory ID
description: You can use a product inventory ID from external Configure, Price, and Quote \(CPQ\) systems in the Order Management application to complete the order fulfillment flow for various actions on the product and service orders.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# External product inventory ID

You can use a product inventory ID from external Configure, Price, and Quote \(CPQ\) systems in the Order Management application to complete the order fulfillment flow for various actions on the product and service orders.

## Overview of external product inventory ID

If you're using the Order Management application, you can use the enhanced TM Forum's Open APIs to create, change, disconnect, suspend, and resume product and service orders. After the order capture and fulfillment process, the system-generated IDs are created against the product inventory records to manage any future requests on the inventory for different order action types.

## Using an external ID

With the support of an external inventory ID, you can do the following tasks:

-   Capture the external product inventory ID in the Order Management system through the Product and Service Order APIs.
-   Store the external inventory ID in a new table for new orders and associate them with the product inventory records that were created after the order fulfillment. Also, update the ID in the external product inventory table for any inflight revisions during the order fulfillment process.
-   Allow external CPQ or southbound systems to use the external inventory ID to submit, change, disconnect, suspend, and resume orders on the product inventory in the order management system.

**Note:** You can also map the external product inventory ID with the product inventory record by using the Product Inventory Open API. For more information, see [Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

