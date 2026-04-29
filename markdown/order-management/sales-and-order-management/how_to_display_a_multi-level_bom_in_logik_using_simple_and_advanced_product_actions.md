---
title: How to display a multi-level BOM in CPQ using simple and advanced product actions
description: Two ways to display a bill of materials that includes hierarchical relationships.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# How to display a multi-level BOM in CPQ using simple and advanced product actions

Two ways to display a bill of materials that includes hierarchical relationships.

When a bill of materials \(BOM\) is represented with hierarchy \(such as a parent-child relationship\), some businesses prefer to display the sum of the prices of the children on the parent line.

For example, when you are building a laptop pricing configurator, you might want to display a parent product, with supplemental products listed as part of a grouped nested menu. Each of these components has an additional price and must be grouped together to arrive at the Total Price of the full BOM.

In the example screenshots below, the Laptop category can be expanded or folded to either display or hide the sub-products in the final price configuration of the laptop.

Image 1: Multi-BOM of laptop hiding sub-products:

![Complete BOM](../images/cpq-multilevel-bom-sub-products-hidden.png)

Image 2: Multi-BOM expanded to display all sub-products in the BOM:

![Complete BOM](../images/cpq-multilevel-bom-sub-products-shown.png)

## Configuration

To begin building a bill of materials, navigate to the Rules section of your CPQ interface and build a new rule. In your rule, add a new product action. From here, add the products as you normally would when building a product action.

1.  Add a simple product action rule.
2.  Add your product list in order, as you would for a basic BOM.

    ![Basic BOM](../images/cpq-multilevel-bom-config-1.png)

3.  Set a unique identifier for the chosen parent field. This provides the capability to assign a parent ID and create nested products. In the above example, we have set the Laptop product.
4.  For each child product, add the unique identifier for the parent product to the Parent Product field. For example, `LAP_sc_parent` is the unique identifier for our Laptop parent product. We would add `LAP_sc_parent` to the Parent Product field for our child products.

    ![Simple selection](../images/cpq-multilevel-bom-config-2.png)


## Advanced

When you have many products that require scripted configuration, you can use the CPQ Advanced Function layer to create a multi-BOM. For this, follow the same instructions as above until you begin building your list of products. If you have multiple SKUs and you need the hierarchy to be correct for each SKU on the BOM, use an Advanced Function to better scale your configuration.

![Product action](../images/cpq-multilevel-bom-advanced-1.png)

1.  Instead of choosing a simple product action, select the Advanced option and click **Create Advanced Function**.
2.  In the Help bar, you can find a ProductList.parentProduct option on the right of the page. Click **Insert Example** to begin building your script. This lets you dynamically generate a unique identifier field for your parent products by leveraging the Set Index field.

![Advanced function](../images/cpq-multilevel-bom-advanced-2.png)

