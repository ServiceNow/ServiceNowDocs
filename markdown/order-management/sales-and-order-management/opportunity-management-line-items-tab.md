---
title: Add line items to an opportunity
description: Create a new product line item for your opportunity by entering the details, such as product offering and quantity.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Opportunity Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Add line items to an opportunity

Create a new product line item for your opportunity by entering the details, such as product offering and quantity.

## Before you begin

Role required: sales\_agent

## Procedure

1.  In the CSM Configurable Workspace, navigate to the **List** view ![list icon](../image/Lists.png) and select **Opportunity - All**.

2.  From the **Opportunity List** view, select the opportunity you want to work with and select the **Line Items** tab.

3.  Select **New** to start a new opportunity line item or select an existing opportunity line item to make changes.

4.  Fill in the fields in the Opportunity Line Item form.

<table id="table_mbp_gg5_c1c"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The system-generated number of the opportunity line item.

</td></tr><tr><td>

Opportunity

</td><td>

The system-generated id of your opportunity.

</td></tr><tr><td>

Product Offering

</td><td>

The product offering that is selected for the opportunity line item.

</td></tr><tr><td>

Unit of Measure

</td><td>

The measuring unit of the opportunity line item.

</td></tr><tr><td>

Unit Net Price

</td><td>

Price per unit after adjustments, if any.

</td></tr><tr><td>

Term \(months\)

</td><td>

Subscription period of the opportunity line item.The default term is 12 months only for recurring products.

</td></tr><tr><td>

Quantity

</td><td>

The quantity of the opportunity line item.

</td></tr><tr><td>

Service location

</td><td>

Service location to which the opportunity line item applies.

</td></tr><tr><td>

Price List

</td><td>

Default price list based on the opportunity created.

</td></tr><tr><td>

Periodicity

</td><td>

Periodicity is based on the pricing method selected for the product offering. -   If the pricing method is selected 'One time', the periodicity is set to 'None'.
-   If the pricing method is selected 'Recurring', the periodicity can be set to 'Monthly' or 'Annually'.


</td></tr><tr><td>

Unit List Price

</td><td>

Unit list price of the product offering included in the opportunity line item.**Note:** The **Unit Net price** and **Unit List Price** fields have the same values if the opportunity isn’t in sync with the quote.

</td></tr><tr><td>

Cumulative One-Time Price

</td><td>

One-time price of the opportunity and opportunity child line items.Cumulative One-Time Price = Quantity \* Unit Net Price.

</td></tr><tr><td>

Cumulative MRR

</td><td>

Cumulative monthly recurring revenue of the opportunity and any child lines.

 -   If periodicity is monthly, Cumulative MRR = Unit Net Price \* Quantity.
-   If periodicity is annual, Cumulative MRR = Unit Net Price/12 months \* Quantity.
 Customer can change this formula in case of they customize their own values for periodicity.

 This field is populated only if the periodicity of the opportunity is recurring in nature.

</td></tr><tr><td>

Cumulative ARR

</td><td>

This field is populated only if the periodicity of the opportunity is recurring in nature.

 Cumulative ARR = Cumulative MRR \* 12

</td></tr><tr><td>

Cumulative ACV

</td><td>

Total annual contract value \(ACV\), which is the yearly amount revenue for all products and services from a customer contract.Cumulative ACV = Cumulative One-Time Price + Cumulative ARR.

</td></tr><tr><td>

Cumulative TCV

</td><td>

Total contract value \(TCV\), which is the total amount of revenue from a customer contract expected over the lifetime of the contract.Cumulative TCV = Cumulative One-Time Price + Term \* Cumulative MRR.

</td></tr><tr><td>

Work Notes

</td><td>

Any additional information related to the opportunity line item.

</td></tr></tbody>
</table>5.  Select **Save**.

    The Opportunity Line Item is added to the main opportunity.


## What to do next

Add a task to your opportunity. To learn more, see [Add opportunity tasks](opportunity-management-tasks-tab.md).

