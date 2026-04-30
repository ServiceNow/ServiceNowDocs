---
title: Order types in Sales Customer Relationship Management
description: Customer orders and service orders are the two main type of sales orders in ServiceNow Order Management. Learn about their differences and how to select an appropriate order type for your use case.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-07"
reading_time_minutes: 3
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Order types in Sales Customer Relationship Management

Customer orders and service orders are the two main type of sales orders in ServiceNow Order Management. Learn about their differences and how to select an appropriate order type for your use case.

Use customer orders for ordering products or services. Use service orders for the activation of new services or for the post-sales requests for the services that were activated for and delivered to customers at earlier dates. By using this process, you ensure that service orders are correct and handled efficiently throughout the entire fulfillment process. The following table compares customer and service orders and lists the differences between the two.

<table id="table_ozp_d21_kgc"><thead><tr><th>

Aspect

</th><th>

Customer order

</th><th>

Service order

</th></tr></thead><tbody><tr><td>

Definition

</td><td>

Orders for products \(tangible or digital\) that a customer wants to purchase or change.

</td><td>

Orders for services that are non commercial in nature and only require technical fulfillment.

 Use service orders for the activation of new services or for the post-sales requests for the services that were activated for and delivered to customers at earlier dates.

</td></tr><tr><td>

Order record structure

</td><td>

-   Customer order record with one or more line items based on the product offering.
-   Includes product specification, characteristics, and values.

</td><td>

-   Service order record with one or more line items based on service specification.
-   Includes service specification, characteristics, and values.

</td></tr><tr><td>

TMF APIs for order capture

</td><td>

TMF622: Product Ordering API

</td><td>

TMF641: Service Ordering API

</td></tr><tr><td>

MACD order options

</td><td>

-   Add
-   Change
-   Delete

</td><td>

-   Add
-   Change
-   Disconnect
-   Suspend
-   Resume

</td></tr><tr><td>

Decomposition

</td><td>

-   It's based on product, service, and resource specification, and rules.
-   Upon approval, order is decomposed into product, service, and resource orders.
-   Can create multiple domain orders \(product, service, resource\) per line item.

</td><td>

-   It's based on service specification and rules.
-   Upon approval, order is decomposed into service and resource orders.
-   Typically creates service and resource orders per line item.

</td></tr><tr><td>

Unique roles

</td><td>

-   Order agent \[sn\_ind\_tmt\_orm.order\_agent\]
-   Order fulfillment manager \[sn\_ind\_tmt\_orm.order\_fulfilment\_manager\]

</td><td>

-   Service order agent \[sn\_ind\_tmt\_orm.service\_order\_agent\]
-   Service order manager \[sn\_ind\_tmt\_orm.service\_order\_manager\]

</td></tr><tr><td>

Inventory impact

</td><td>

Sold products

</td><td>

Product inventory

</td></tr><tr><td>

Suitable for

</td><td>

All industries

</td><td>

All industries, highly preferred for the telecommunication industry

</td></tr></tbody>
</table>## Differences between the pre- and post-approval service orders

Like customer orders, captured service orders also have an ID with a prefix of ORD\(nnn\). The **Order Category** field in the order forms indicates if the order is for a **Product** \(a customer order\) or a **Service** \(a service order\). These labels enable you to identify the type of order.

When you approve a captured service order for fulfillment, the post-approval decomposition process generates actionable service orders and resource orders. You may see a single service order, multiple service orders, and resource orders that are associated with your approved service order.

-   Service orders with a prefix of SO\(nnn\) are referred to as domain orders. These orders, and their related resource orders, with a prefix of RO\(nnn\), must be fulfilled to complete the service order line items on the captured service orders.
-   The resource order manages the resources required to fulfill the services that the customer is requesting.
-   These domain orders manage the fulfillment of the requested service orders.

To learn more, see [Order decomposition](order-mgt-order-decomposition.md).

## Order types for service orders

The following are the two key fulfillment actions for service orders:

-   Deliver: Involves providing the ordered items to the customer once the order is ready.
-   Qualify: Validates whether a service or product can be fulfilled before actual execution.

Service qualification request orders with fulfillment type as Qualify can only be created in the ServiceNow Order Management system using APIs from external qualification request systems. When you capture an order using Order Management, the orders are created with the fulfillment type as Deliver.

**Related topics**  


[Service qualification requests](order-mgt-tsq-about.md)

