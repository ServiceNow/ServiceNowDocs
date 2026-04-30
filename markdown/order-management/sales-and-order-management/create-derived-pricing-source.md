---
title: Create rules for derived product pricing
description: Define product pricing rules for deriving the price of a product dynamically based on the pricing of related products or a pricing source.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 3
breadcrumb: [Derived product pricing, Pricing Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create rules for derived product pricing

Define product pricing rules for deriving the price of a product dynamically based on the pricing of related products or a pricing source.

## Before you begin

Role required: sn\_csm\_pricing\_pricelist\_administrator or sn\_csm\_pricing\_pricelist\_manager

## About this task

Use the Derived Price Matrix to define the rules for deriving the pricing of a product offering relative to other product offerings or a price source based on a transactional headers, such as quote

**Note:** Once a matrix is published, you can't make further changes to it. If you have changes, create another version of the matrix with your updates and publish the new version. However, your admin can allow changes to a published matrix by using the **allow\_edit\_on\_published\_matrices** system property. To learn more, see [Allow changes to published pricing and product eligiblity matrices](edit-published-matrices.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Pricing** &gt; **Pricing Matrices**.

4.  In the Pricing Matrices list, select the **Derived Pricing Matrix**.

5.  If you have a large number of rows in the decision table and you want to optimize rule matrix performance, in **Query optimization variables**, select the search icon and one or more context variables that the system uses to filter the derived pricing decision rows that are evaluated.

6.  In **Rule selection criteria**, select the option that indicates whether single or multiple rules are applied in the Derived Pricing Matrix.

    If multiple rules are applied, all applicable pricing rules are applied when evaluating relationships for derived pricing. If the option is Single, the first rule based on rank is applied for the relationship.

7.  Select **Edit Rule**.

    The Decision Table for the Derived Pricing Matrix opens in Workflow Studio and displays the following:

    -   Inputs: Lists the default inputs \(**Target Product Offering**,**Product Offering** \(the source product offering\), **Transaction Date**, and **Active**\).

        **Note:** If you have a custom context variable that represents a pricing value to be used as a pricing source, you can add a custom context variable as an input. Context variables are a reference to the Context Variable \[sn\_csm\_ctxrul\_mgt\_context\_variable\] table.

    -   Decision table: The conditions that you specify to derive the pricing for a target product from one or more source products, and the items used to generate the results.
8.  In the Decision table, enter the derived pricing conditions:

    1.  In the Conditions section, select **Add new decision row**.

    2.  In the **Target Product Offering** column, enter the conditions for the target offering and the source **Product Offerings** if applicable.

    3.  Set other mandatory inputs as needed.

9.  In the results section, specify the following:

    1.  In the **Scope** column, select one of the following:

        -   Bundle: All instances of the source product offerings in the bundle hierarchy are considered and their prices are totaled.
        -   Cart: All instances of the source product offerings in the transaction are considered and their prices are totaled.
    2.  In the **Percentage Price** column, enter the percentage of the source product price to be applied.

    3.  Select the **Price Point** used to calculate the derived price:

        -   Unit List Price: Product price that is based on a single unit of measure.
        -   Unit Net Price: Product price after all adjustments such as discounts or reductions are applied.
        -   Cumulative Net Price: Product price over a specific period, which considers discounts or price adjustments applied on the total quantity purchased.
    4.  In the **Header Variable** column, enter the header variable for a quote order to be used as the pricing source, for example Total annual recurring price.

    5.  Review the **Validation Status** and **Validation Message** columns to verify that the results are valid.

    6.  **Save**.

10. In the Details tab for the matrix, select **Publish**.

    The derived pricing for the target product is available when the product is used in a transaction line.


## Result

When sales or order agents add a product with derived pricing, the derived pricing for the product is automatically applied based on the conditions and the values set in the Derived Pricing Matrix. Agents can review the line item for the target product and see how the derived price was calculated, for example, by checking the scope \(Unit list price, Unit net price, or Cumulative net price\).

