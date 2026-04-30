---
title: Customer Service Management for Orders
description: The Customer Service Management for Orders feature adds support for orders and order line items to the Customer Service Management application.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Extend capabilities, Configuring Customer Service Management, Customer Service Management]
---

# Customer Service Management for Orders

The Customer Service Management for Orders feature adds support for orders and order line items to the Customer Service Management application.

**Note:** Starting with the Utah release, the Customer Service Management for Orders feature has been deprecated. It is no longer supported, enhanced, nor available for activation. For details, see the  [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

The [Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US) application replaces the Customer Service Management for Orders feature. For information on moving to Order Management for Customer Service Management, see the [Fix Script to Support Script-Based Data Migration to New Order Management Application](https://www.servicenow.com/community/csm-articles/fix-script-to-support-script-based-data-migration-to-new-order/ta-p/2297073) article in ServiceNow Community.

Customer Service Management for Orders enables customers and consumers to do the following through a self-service portal:

-   View orders
-   View and create cases for orders
-   Contact a customer service agent to report an issue

Customer service agents can respond to customer and consumer requests and create cases for orders.

## Plugins

To add support for orders to the Customer Service Management application, activate the Customer Service Management for Orders plugin \(com.snc.csm.order\). This plugin requires the Customer Service plugin \(com.sn\_customerservice\).

This plugin adds the following modules to the Customer Service menu:

-   **Orders**: displays a list of customer orders. Click an order to display the Order form.
-   **Order Line Items**: displays a list of the individual items within each order in the Orders list. Click an item to display the Order Line Item form.

## Creating a case for an order

When creating a case from the Customer or Consumer Service Portals, the end user can select the type of case to create. Based on the selection, the Create Case form includes fields specific to the selected case type.

-   **Create Product Case**: includes the **Asset** and **Product** fields.
-   **Create Order Case**: includes the **Order** field.

When creating a case from the Customer Service Management application, the customer service agent can select the type of case to create:

-   **Product**: opens a new Case form for a product that includes the **Product** and **Asset** fields.
-   **Order**: opens a new Case form for an order that includes the **Order** field.

## Tables installed with Customer Service Management for Orders

Customer Service Management for Orders adds the following tables.

<table id="table_udf_cmc_kt"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Orders\[csm\_order\]

</td><td>

Stores the orders associated with an account and contact or with a consumer.

</td></tr><tr><td>

Order Line Items\[csm\_order\_line\_item\]

</td><td>

Stores the individual line items within orders.

</td></tr><tr><td>

Order Cases\[csm\_order\_case\]

</td><td>

Stores information about customer service cases related to orders.

</td></tr><tr><td>

Order Case Line\[csm\_order\_case\_line\]

</td><td>

Stores information about customer services cases related to orders and order line items.

</td></tr></tbody>
</table>**Parent Topic:**[Customer Service Management](c_CustomerServiceManagement.md)

