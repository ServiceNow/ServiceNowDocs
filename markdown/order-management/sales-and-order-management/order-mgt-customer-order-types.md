---
title: Action types for customer and service orders
description: Learn how you can take various types of actions for your customer orders. Action types include move, add, change, disconnect, suspension, resume, or no-change of services.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Action types for customer and service orders

Learn how you can take various types of actions for your customer orders. Action types include move, add, change, disconnect, suspension, resume, or no-change of services.

By using an order action type, you can define the type of actions that you want to do with an order. The following table lists the order action types.

<table id="table_j2b_fgt_v4b"><thead><tr><th>

Order action type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add

</td><td>

Add a customer order that isn’t associated with an existing order from the same customer. This customer order results in new order management and fulfillment activities.For example, you place a new order for a home internet service.

</td></tr><tr><td>

Change

</td><td>

Change an existing order, which changes a previously ordered or fulfilled product or service. This order action type includes the following scenarios:-   Addition of a child product specification that the customer didn’t previously order.
-   Deletion of an optional child product specification that the customer already has. For example, you upgrade the download speed of your home internet from 100 Mbps to 1000 Mbps.
-   Change characteristics for existing products.

</td></tr><tr><td>

Disconnect \(delete for TMF API\)

</td><td>

Disconnect an existing customer service order. For example, you can disconnect your home internet service.**Note:** When a mandatory product is deleted, all the products are deleted.

</td></tr><tr><td>

Suspend

</td><td>

Product or service order to temporarily inactivate the product inventory of its order line items.**Note:** To learn more, see [Using suspend and resume actions](order-mgt-suspend-resume-action.md).

</td></tr><tr><td>

Resume

</td><td>

Product or service order to activate the product inventory of its order line items that were previously suspended.**Note:** To learn more, see [Using suspend and resume actions](order-mgt-suspend-resume-action.md).

</td></tr><tr><td>

No change

</td><td>

Order line items with No change action are included in the order for informational purpose only. For example, an order contains multiple items, but only one of those items must be changed \(such as the speed, which has changed from 100 Mbps to 1000 Mbps\), which affects the parent line item. However, all the other line items in the order remain unchanged.

</td></tr></tbody>
</table>