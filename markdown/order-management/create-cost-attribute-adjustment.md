---
title: Create and publish a cost-based attribute adjustment
description: Set different product costs based on product attributes, such as model or size, by applying cost adjustments for a product offering by cost book or specified cost book line. The base cost is the cost at the cost book line. Product cost is the base cost plus attribute adjustments. These adjustments are used to display the profit margins in quotes and quote lines, which can be criteria for triggering quote approval rules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create and publish a cost-based attribute adjustment

Set different product costs based on product attributes, such as model or size, by applying cost adjustments for a product offering by cost book or specified cost book line. The base cost is the cost at the cost book line. Product cost is the base cost plus attribute adjustments. These adjustments are used to display the profit margins in quotes and quote lines, which can be criteria for triggering quote approval rules.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator or sn\_csm\_pricing.pricelist\_manager

## About this task

You select the characteristics of a product that affect the base product cost. Next, use a decision table to create an attribute adjustment rule that defines the conditions for applying the adjustments and the markup or markdown value, either a percentage or amount to be applied for specified characteristics. For more information on using decision tables, see Using decision tables.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

2.  Navigate to **Pricing** &gt; **Attribute Adjustments**.

3.  Select **New** and fill in the fields.

<table id="table_bdd_fmb_bgc"><thead><tr><th>

Field

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the cost-based attribute adjustment.

</td></tr><tr><td>

Code

</td><td>

System-generated alphanumeric value based on the attribute name.

</td></tr><tr><td>

Type

</td><td>

Type of adjustment, either Price or Cost.Select Cost.

</td></tr><tr><td>

Apply to all cost books

</td><td>

Option that applies this attribute adjustment to the product offering for all cost books.If this attribute adjustment applies only to a cost book line for a product offering, unselect this option.

</td></tr><tr><td>

Product offering

</td><td>

Product to which this adjustment applies. Select the field to display a list of products. The characteristics set for the product offering are displayed in the **Product Characteristics** field.

</td></tr><tr><td>

Number

</td><td>

System-generated alphanumeric value that identifies this cost-based attribute adjustment.

</td></tr><tr><td>

Cost book line

</td><td>

Option for selecting a cost book line to which the adjustment is applied. You can select this option if the **Apply to all cost books** option is unselected.

</td></tr><tr><td>

State

</td><td>

Status of the adjustment:-   Draft \(saved\)
-   Published
-   Retired
-   Archived


</td></tr><tr><td>

Start date

</td><td>

Date and time that this attribute adjustment begins.If you want to apply the adjustment to a cost book line, the **Start date** and **End date** must be the within the cost book line start and end dates.

</td></tr><tr><td>

End date

</td><td>

Date and time that this attribute adjustment ends, if applicable.

</td></tr><tr><td>

Product characteristics

</td><td>

Product attributes used to differentiate product costs.

</td></tr></tbody>
</table>4.  Select **Save**.

5.  In the Attribute Adjustment page, select **Create Rule**.

    The Decision Table for the adjustment opens in Workflow Studio.

6.  Set the attribute pricing rule:

    1.  In the Conditions section, select **Add new decision row**.

    2.  In the row, select an attribute column and select the appropriate value.

        For example, if an automation hub product has attribute columns labeled **4G** and **5G**, select each column and then select the appropriate value.

    3.  In the Results section, select the **Adjustment Type** column and choose the type of adjustment, for example Markdown % or Markdown amount.

    4.  In the **Adjustment Value** column, enter the adjustment amount.

    5.  Select **Save**.

        The adjustments are made to the cost book or the cost book line, depending on the options selected in step 3.

7.  Test your decision table.

    For information on testing your decision table before publishing it, see Test a decision table in Workflow Studio.

8.  If this is a product-based cost attribute adjustment, select **Publish** in the **Details** tab for the attribute adjustment to make the attribute adjustment available.

    The cost-based attribute adjustments for the product offering are applied when agents add the product offering to an opportunity, quote, or an order.


