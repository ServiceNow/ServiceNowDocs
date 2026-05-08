---
title: Methods of creating orders in Sales Customer Relationship Management
description: Orders can be created by agents, customers, or using APIs in ServiceNow Order Management. Irrespective of where or how you create orders, all orders can be managed, tracked, and fulfilled using Order Management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order Management, Use, Sales Customer Relationship Management]
---

# Methods of creating orders in Sales Customer Relationship Management

Orders can be created by agents, customers, or using APIs in ServiceNow Order Management. Irrespective of where or how you create orders, all orders can be managed, tracked, and fulfilled using Order Management.

## Order capture by the agents

Order agents and service agents can capture orders for existing customers from the CSM/FSM Configurable Workspace. Sales agents can create orders by converting an approved quote. The following table lists the various order creation channels and their benefits.

<table id="table_ar5_brv_4gc"><thead><tr><th>

Channel

</th><th>

Persona

</th><th>

Benefit

</th></tr></thead><tbody><tr><td>

Converting a quote to an order

</td><td>

Sales agents

</td><td>

The quote-to-order conversion supports post-quote workflows such as order capture, fulfillment, and contract creation. Benefits include:-   Reduced errors from manual data handling
-   Consistency across systems by using a unified data model
-   Support for complex product configurations and pricing strategies, including bundles and multi-currency pricing

</td></tr><tr><td>

Creating orders from Accounts page

</td><td>

Order or service agents

</td><td>

The Accounts Information tab provides a 360-degree view of customer interactions, including quotes, contracts, entitlements, and previous orders. Creating orders from this context promotes:-   Better-informed decisions based on historical data
-   Fewer errors due to pre-filled fields and validated account details
-   Faster order initiation based on pre-existing account data

</td></tr><tr><td>

Creating orders from Customer Orders or Service Orders list view

</td><td>

Order or service agents

</td><td>

Alternate way to create an order for an account or a consumer with a different set of contact information or parameters.

</td></tr></tbody>
</table>## Order creation using TM Forum \(TMF\) APIs

Most of the service orders that you process are captured from third-party customer order management systems through the Service Order Open API. The Service Order Open API is a ServiceNow implementation of the TM Forum TMF641 Service Ordering Open API specification. To learn more, see Service Order Open API.

Order creators and order integrators for a Communications Service Provider \(CSP\) company can use the following TMF APIs to create orders:

-   TMF622: Product Ordering API
-   TMF641: Service Ordering API

**Note:** You need a Telecommunications Service Management subscription to create orders using TMF APIs.

## Order creation using Service Exchange

Your ServiceNow instances can be integrated with the instances of your customers by using Service Bridge. With this integration, you can create and publish product offerings to your customer's instances. Enterprise customers can then submit requests for products or services, which you can then fulfill using Order Management. For detailed benefits on using the Service Bridge applications, see Exploring Service Exchange.

## Order creation by B2B customers

Business-to-Business \(B2B\) customers can leverage self-service capabilities provided through the Business Portal to browse products and submit orders. These orders are then processed by the order and fulfillment agents. For more information, see [Create orders from the Business Portal](../task/order-mgt-create-an-order-using-customer-portal.md).

## Post-capture order record generation

When you capture or directly enter a customer or service order, the corresponding order record is generated in the ServiceNow AI Platform. The order record has one or more associated order line items that describe the product or service and the action \(Add, Change, Disconnect\) to perform any required service for the item. The order line also contains the following elements:

-   The details of the product or service being added, updated, or deleted.
-   For Add type orders, the order line item holds the details of the product specification, with its required characteristics and characteristic values.
-   For Change and Disconnect type orders, the order line holds the details of the product inventory that you're updating or disconnecting.
-   The order line item can have a location and related information such as customer contacts detail.

**Related topics**  


[Creating orders in Order Management](creating-orders-som.md)

[Convert quotes into orders](../task/quote-management-customer-orders-tab.md)

