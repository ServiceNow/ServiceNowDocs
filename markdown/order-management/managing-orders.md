---
title: Managing post-fulfillment order changes
description: Efficiently handle a variety of post-fulfillment changes to maintain service quality and operational accuracy after initial order fulfillment. These changes include canceling, suspending, resuming, disconnecting, and modifying orders. Each change type has distinct workflows, dependencies, and impacts on inventory and service states.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Managing post-fulfillment order changes

Efficiently handle a variety of post-fulfillment changes to maintain service quality and operational accuracy after initial order fulfillment. These changes include canceling, suspending, resuming, disconnecting, and modifying orders. Each change type has distinct workflows, dependencies, and impacts on inventory and service states.

After an initial order is fulfilled, existing customers may want to disconnect, suspend, or resume a product or service or change specifications or location for a product they’ve purchased. For example, a customer might want to disconnect their current 4G connectivity and upgrade it to 5G connectivity. You can manage such requests by creating orders with action type as Change, Move, Disconnect, Suspend, and Resume. For more information, see [Action types for customer and service orders](order-mgt-customer-order-types.md).

When you change a product or service inventory record, the ServiceNow AI Platform creates the order line items from the specifications that you have defined. In a change service order inventory, the order line items are created only for your selected service inventories. If you select inventories that are top-order parent items, the order line items are created only for the parent items, not for the child order items. When the additional product is added to the change order, an inventory record is created for the added product. The new inventory is mapped to the new hierarchy.

When you’re canceling a product or service order inventory, the ServiceNow AI Platform creates the order line items according to the specifications that you have defined. To cancel a product order inventory record, if your selected inventories are top-order parent items, the order line items are created for both the parent items and the child order items. If your selected inventories are child-order items, the order line items are created only for the child items.

As a part of post-fulfillment order changes, Return Merchandise Authorization \(RMA\) is also possible through modify, add, change, and disconnect \(MACD\) has a part of out of box process. For more information about RMA, see [Return Merchandise Authorization](return-merchandise-authorization.md).

Validation is required to successfully create the move order. To complete the validation and approve the move order, check the following:

-   All the associated child line items of the move order must have the move operation selected as **true** and the Order line action must have one of the actions **Change** or **Add** or **Disconnect**.
-   All the associated child line items of the move order the service location must be the same.
-   All the inventory associated with a product being moved must be available in the move order.

For

The process to capture post-sale modification requests is similar to order capture and fulfillment. The high-level steps are as follows:

1.  Create an order with the required action type.
2.  Select product inventory items that you want to modify from the catalog.
3.  Review and submit the order for approval.
4.  Approve the order.

    The order is decomposed and order tasks are created.

5.  Fulfill the orders by closing the order tasks, domain orders, and work orders, if any.

You can also manage post-sale change requests from the customer accounts page, not only for products and services sold to a customer, but also to contracts and entitlements associated with the products and services. For more information about customer life cycle workflows, see [Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

-   **[Request post-sale change orders](../task/create-macd-orders.md)**  
Learn how to create orders for disconnecting, suspending, resuming products or services and changing specifications, characteristics, or service location for orders after an initial order has been fulfilled.
-   **[Move order](move-order.md)**  
The move order helps agents to change the location for product inventory at the order line level.
-   **[Suspend and resume products and services](order-mgt-suspend-resume-action.md)**  
You can use suspend and resume actions to temporarily suspend or inactivate your product and service inventories. That way, you can capture a customer's suspend request and resume the products and services later.

**Parent Topic:**[Using Order Management](using-order-management.md)

