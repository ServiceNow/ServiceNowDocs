---
title: Show rollup pricing in the shopping cart
description: Configure the shopping cart to display the sum of the child items as the price of the parent item.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-21"
reading_time_minutes: 2
breadcrumb: [Set up pricing display, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Show rollup pricing in the shopping cart

Configure the shopping cart to display the sum of the child items as the price of the parent item.

## Before you begin

Role required: Admin

## About this task

When a bill of materials \(BOM\) is represented with hierarchy, such as a parent-child relationship, you may prefer to total the prices of the child items and display them on the parent line as a sum. ServiceNow CPQ rollup pricing totals direct child and parent extended list values. Rollup pricing delivers the sum of all child line prices to the shopping cart, including the price of the parent, and displays it at the parent line.

To view a script that illustrates how a hierarchical bill of materials might be generated, see [Adv Product Action with Product List](https://docs.google.com/document/d/1DmVwr1NTJyFLWM0RJB4wUWcA7fI-Jg4iikv9Cji3OVI/edit?usp=sharing).

The following example shows four child products rolling up to their related parent products.

![Display rollup pricing in the shopping cart](../images/cpq-rollup-pricing-1.png)

The next example shows a 2-tier roll-up, with a child product \(child1B and child 2B\) rolling up to a parent \(parent B\) and that parent rolling up to the parent product \(parent A\) in addition to the remaining child products \(child 1A and child 2A\).

![Display rollup pricing in the shopping cart](../images/cpq-rollup-pricing-2.png)

## Procedure

1.  In ServiceNow CPQ administration, create a rule by clicking **+ New**.

    ![Rules](../images/cpq-rollup-pricing-3.png)

2.  Name the rule, and click **Save**.

3.  Set your condition and create your product actions.

    -   Start with a parent product and set the parent product ID, quantity, price, type, BOM type, and unique identifier.

        For parent products, the type should be set to Component. For child products, the type should be set to Accessory.

    -   Add the unique identifier to the parent product field of any products that you want rolled up into the parent product.
    ![Product action](../images/cpq-rollup-pricing-4.png)

4.  To display the rolled-up price in your cart, add `rollUpPrice` to your shopping cart in the layout editor, or define the `productlistcolumn` type in your layout CSV with the variable name `rollUpPrice`.

    ![CSV file](../images/cpq-rollup-pricing-5.png)


**Related topics**  


[Customizing the currency display in the shopping cart](layout_how_do_i_customize_currency_display_in_shopping_cart.md)

[How price is displayed on a layout with multiple BOMs](how_does_pricing_on_multiple_boms_displayed_on_a_layout_behave.md)

[Set a custom message for zero-priced and null-priced items](cpq-set-a-custom-message-for-zero-priced-and-null-priced-items.md)

