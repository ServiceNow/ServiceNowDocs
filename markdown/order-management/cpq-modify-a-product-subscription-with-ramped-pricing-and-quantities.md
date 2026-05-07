---
title: Modify a product subscription with ramped pricing and quantities
description: Add pricing or quantity ramps to quote line items to set incremental changes during the life of a contract.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-10"
reading_time_minutes: 2
breadcrumb: [Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Modify a product subscription with ramped pricing and quantities

Add pricing or quantity ramps to quote line items to set incremental changes during the life of a contract.

In the CPQ configurator, you can modify the configuration of a product subscription so that prices and quantities change during the term of the subscription. This is called ramped pricing because the price or quantity increases or decreases during the term of the contract.

To enable the ramped pricing feature, select the **Enable Ramps** check box on the **Pricing** tab of the product offering configuration page.

When you create a quote for a configurable product, you can set ramped pricing for offerings within the product. Select a quote line item, and then select **Ramps**. A **Price ramps for \[product offering\]** dialog appears that contains the following fields:

-   Start date
-   End date
-   Term \(months\)
-   Ramp type
-   Segments
-   Annual % increase

If the start date, the end date, and the term are not already specified in the quote line, exit the price ramps dialog, enter them there, and save the quote line. You can modify them later when you set up a ramp. In the price ramps dialog, for the ramp type, select **Yearly** to change the pricing each year, **Quarterly** to change the pricing each quarter, or **Custom** to specify another period \(ramp segment\) at which prices are to be adjusted. Ramp segments are created according to the term of the contract and the ramp type. For example, if the term of the contract is 36 months \(three years\), and you select **Yearly** as the ramp type, three segments are created: one for each year of the contract.

In the **Annual % increase** box, enter the increase to go into effect each year. If you enter 10, the unit price will increase by 10% each year.

Click **Create**, and the segments display with price changes according to the figure that you entered.

In each segment, the **Quantity** field is editable. For example, to specify a contract during which 1 unit is purchased the first year, 2 units are purchased the second year, and 4 units are purchased the third year, set the quantities accordingly in the three annual segments. To set a quantity ramp with no change to pricing during the term of the contract, enter 0 in the **Annual % increase** box and modify only the quantity in each ramp segment.

**Note:** By default, ramps are hidden in a product’s list of line items. To display the ramps in the line items view, set the hierarchy toggle at the top of the list. Then, select **conditions** and remove the default conditions for the view.

**Parent Topic:**[Using CPQ](cpq-using.md)

**Related topics**  


[Configurable products](configurable-products-explore.md)

