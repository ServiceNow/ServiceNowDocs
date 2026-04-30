---
title: Add products or services to an order in Order Management
description: Add order lines for products or service orders using the product catalog and product configurator in Order Management.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-10-13"
reading_time_minutes: 2
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Add products or services to an order in Order Management

Add order lines for products or service orders using the product catalog and product configurator in Order Management.

## Before you begin

**Note:** Check your entitlements to see if the product configurator is available.

Role required: sn\_ind\_tmt\_orm.order\_agent, sn\_ind\_tmt\_orm.service\_agent

## About this task

The product catalog displays tiles that contain product information. Simple products have an **Add** button that adds the product with no options available to the order.

Products with options have a  **Customize**  button that opens the  product configurator, which lets you select product options.

![Product catalog used to add products and services to orders.](../image/som-om-order-catalog-2.png "Product Catalog used to add products to orders")

Products with options have a **Customize** button that opens the product configurator, which lets you select product options.

![Product configurator lets agents choose product options.](../image/som-om-configurator-callouts-2.png "Product configurator for selecting product options")

When the  product configurator opens you can select from the available options for the product or service.

The product configurator consists of three columns.

-   The product hierarchy displays product catalog items and child products associated with the product.
-   The option selection displays any available options for the product, service, order lines, and order tasks.
-   The Current Selection displays the selected products options and the pricing.

As you configure your product, use the following options:

<table id="table_pqy_fcs_tgc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reprice

</td><td>

Resets the pricing and updates the total price when you make changes.If cascading pricing is enabled, pricing information is cascaded from parent to child line items. See [Control cascading quantity values in child product offerings](som-activate-cascade-quantity.md) for more information.

</td></tr><tr><td>

Validate Related Items

</td><td>

Validates the product and prices when changes are made.

</td></tr><tr><td>

Add

</td><td>

Adds the product to the order after you've configured it.

</td></tr></tbody>
</table>**Note:** If you added a sales agreement while creating the order, only the products listed in the sales agreement are available for selection.

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All**.

4.  Select an order.

5.  In the **Catalog** tab, choose a catalog from the drop-down menu.

6.  Add products to your order.

    -   Select **Add** to add a simple product.
    -   Select **Customize** to add products with configurable options.
7.  Select the **Line items** tab to view products and services in your order.


**Related topics**  


[Filter product catalog by location](order-mgt-filter-catalog-by-location.md)

[Set up and review order lines](som-om-setup-product-order-lines.md)

