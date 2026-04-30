---
title: Domain separation and Order Management
description: Domain separation is supported for Order Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.OM revamp project - This topic was unhidden on Oct 30, 2025. Toby reviewed and approved it.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-30"
reading_time_minutes: 2
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Domain separation and Order Management

Domain separation is supported for Order Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Overview of domain separation in Order Management

The order fulfillment module in Order Management supports domain separation at an account level. All customer orders, order line items, and order tasks have account \(customer\) level separation.

## How domain separation works in Order Management

-   Ensure that the account is domain separated according to the domain separation guidelines in Customer Service Management. For more information, see [Domain separation and Customer Service Management](https://www.servicenow.com/docs/access?context=domain-separation-customer-service&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).
-   Customer orders, customer order line items, service orders, service order lines, and order tasks are domain separated using the account name.
-   If an administrator assigns fulfillment agents and managers to work on customer orders, service orders, and order tasks for a specific domain, they can work on these types of transactions across accounts.

## Domain separated tables

-   Customer Order
-   Customer Order Line Item
-   Customer Order Characteristic Value
-   Service Order
-   Service Order Line Item
-   Service Order Characteristic Value
-   Order Tasks
-   Product Order
-   Resource Order
-   Contract product offering

## Use cases

If customer or service orders have an account name, an administrator can identify and separate customer or service orders for different domains.

If fulfillment agents or managers are assigned to a domain, an administrator can assign them to work on customer orders, service orders, and order tasks for a specific domain \(account\).

**Parent Topic:**[Order Management reference](../reference/order-mgt-reference.md)

**Related topics**  


[Using Order Management](using-order-management.md)

[Configuring Order Management](order-mgt-configuring.md)

[Managing service orders](managing-service-orders.md)

