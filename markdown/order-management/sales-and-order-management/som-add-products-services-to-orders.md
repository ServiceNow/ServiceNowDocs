---
title: Add products or services to an order in Order Management
description: Once an order is started, add order lines for products or services using the product catalog and product configurator in Order Management.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-04-07"
reading_time_minutes: 2
breadcrumb: [Create an order in Order Management, Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Add products or services to an order in Order Management

Once an order is started, add order lines for products or services using the product catalog and product configurator in Order Management.

## Before you begin

**Note:** Check your entitlements to see if the product configurator is available.

Role required: sn\_ind\_tmt\_orm.order\_agent

## About this task

The product catalog shows tiles that contain product information. Simple products have an **Add** button that adds the product to the order with no options available.

![Product catalog used to add products and services to orders.](../image/som-om-order-catalog-2.png "Product Catalog used to add products to orders")

Products with options have a **Customize** button that opens the product configurator, which lets you select product options.



![Product configurator lets agents choose product options.](../image/som-om-configurator-callouts-2.png)

The product configurator consists of three columns. The Product Hierarchy column displays product catalog items and child products associated with the product. The Option Selection column shows any available options for the product or service and order lines and order tasks. The Current Selections column shows the products options selected and the pricing.

## Procedure

1.  In the **Configurable Workspace**, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Customer Orders** &gt; **All**.

3.  Select your order.

4.  Add products to your order.

    -   Select **Add** to add a simple product \(product with no options\) to your order.
    -   Select **Customize** to add products that have configurable options.

        The product configurator opens for choosing available options for the product or service. For details on the configurator interface, see [Using Sales Customer Relationship Management applications](../concept/som-using.md). As you are configuring your product, you use the following options:

<table id="table_ksy_whv_x2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reprice

</td><td>

Resets the pricing and updates the total price when changes are made.If cascading pricing is enabled, pricing information is cascaded from parent to child line items. See [Control cascading quantity values in child product offerings](som-activate-cascade-quantity.md) for more information.

</td></tr><tr><td>

Validate

</td><td>

Validates the product and prices when changes are made.

</td></tr><tr><td>

Add

</td><td>

Adds the product to the order after you've configured it.

</td></tr></tbody>
</table>    The product or service is added to the order as an order line item.

5.  Select the **Order Line Item** tab to view products and services in your order.


**Parent Topic:**[Create an order in Order Management](som-create-product-order.md)

**Related topics**  


[Set up and review product order lines in Order Management](som-om-setup-product-order-lines.md)

