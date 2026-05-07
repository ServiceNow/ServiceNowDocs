---
title: Configure volume pricing
description: Set volume pricing rules by using the Standard Price Adjustment matrix.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure volume pricing

Set volume pricing rules by using the Standard Price Adjustment matrix.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator, sn\_csm\_pricing.pricelist\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

2.  Navigate to **Pricing** &gt; **Pricing Matrices**.

3.  In the Pricing Matrices list, select the Standard Price Adjustment matrix and [create a new matrix version](create-matrix-versions.md).

4.  In the Context variables section of the new matrix version, select the Search ![](../../tmt-telecom-network-inventory/image/search.png) icon and in the list of Context variables, select the Quantity variable.

    The Quantity variable is added to the Context variables section.

5.  Select **Create Rule**.

    The Standard Price Adjustment Matrix opens in Workflow Studio and displays the inputs available and the Decision table for entering the volume pricing conditions to be applied.

6.  In the Conditions section of the Decision table, do the following:

    1.  Select the item to which the volume pricing adjustment is to be applied, such as **Product Offering**.

        For example, if you're setting volume pricing for door sensors, select the Door Sensor product offering.

    2.  Make the condition active by selecting the **Active** field and set it to true.

    3.  Select a condition operator in the **Quantity** field and enter the quantity value to be applied.

        The following operators are available:

        -   is
        -   is not
        -   is empty
        -   is not empty
        -   less than
        -   greater than
        -   less than or is
        -   greater than or is
        -   between
        For example, selecting the operator **greater than or is** and specifying a quantity value 10 indicates that the pricing adjustment applies to a quantity that is equal to or greater than 10.

        If you select the operator **between**, you specify a quantity range by entering the **Min value** and **Max value** for the range. You must set both a minimum and maximum value so that the quantity pricing adjustment applies only to the quantity of product offerings in the specified range.

        ![Standard Price Adjustment Matrix conditions for Product Offering and Quantity range](../image/std-price-adj-matrix-example.png "Example quantity range for volume pricing")

        For example, the door sensor pricing adjustment applies only to quantities ranging from 1 through 10. The pricing adjustments are not applicable to other quantity values for door sensors.

7.  In the Results section, do the following:

    1.  Select the **Adjustment Type** field and choose the type of adjustment, for example Markdown % or Markdown amount.

    2.  In the **Adjustment Value** column, enter the adjustment amount.

    3.  In the **Adjustment Description** column, enter a brief description of the adjustment, for example, Quantity adjustment for door sensors.

    4.  Select **Save**.

8.  Return to the version of the Standard Price Adjustment Matrix that you created and select **Save** and then **Publish** to make the matrix version active.

    The volume pricing adjustment is available to sales or order agents as they work on quotes or orders. For example, a pricing adjustment has a quantity range for a particular product, such as 1 through 10 door sensors. When a sales agent adds five door sensors to a quote, the pricing adjustment is applied. The pricing adjustment doesn't apply to quantities outside this range.


