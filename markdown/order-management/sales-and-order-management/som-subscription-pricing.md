---
title: Subscription revenue metrics
description: Subscription pricing is a pricing model where customers pay a recurring fee for products or services, usually at regular intervals such as monthly or annually. In Sales Customer Relationship Management, various subscription revenue amounts are calculated automatically for opportunities and quotes.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Subscription revenue metrics

Subscription pricing is a pricing model where customers pay a recurring fee for products or services, usually at regular intervals such as monthly or annually. In Sales Customer Relationship Management, various subscription revenue amounts are calculated automatically for opportunities and quotes.

Subscription revenue amounts are metrics that help sales agents and sales managers track and analyze the revenue impact of sales deals. Sales agents and managers can view these system-calculated revenue amounts in the pricing details for opportunities and quotes, both at the header and line levels. These revenue amounts, such as monthly recurring revenue \(MRR\) or annual recurring revenue \(ARR\), are useful for monitoring sales performance, forecasting subscription revenue, and providing relevant subscription amounts when agents engage with customers.

![Opportunity line and Opportunity header records that display system-calculated subscription revenue values described in the opportunity subscription tables that follow](../image/opportunity-subscription-revenue.png "Example opportunity subscription revenue details")

## Subscription pricing metrics

In subscription pricing, common metrics for assessing subscription-based revenue include the following values and items:

-   **Monthly Recurring Revenue \(MRR\)**

    The total revenue generated from recurring subscriptions or contracts on a monthly basis. It helps sales agents and managers assess the stability and growth of subscription-based revenue streams.

-   **Annual Recurring Revenue \(ARR\)**

    The annual revenue generated from recurring subscriptions or contracts. It provides insights into the predictable revenue stream that can be expected from existing customers over a year.

-   **Annual Contract Value \(ACV\)**

    The total value of a contract on an annual basis. It highlights the annual revenue impact of a deal and facilitates comparison with other contracts or revenue streams.

-   **Total Contract Value \(TCV\)**

    The total value of a contract over its entire duration, including recurring and one-time charges. It provides visibility into the overall value of a deal and its impact on the organization's financial performance.

-   **Term**

    The duration or period of a subscription or contract, in months, such as 10 months or 24 months. In Opportunity Management, agents can enter a Term value before adding line items. In Quote Management, when agents enter a Term value and the contract start date, the system uses the term value and start date to auto-calculate the contract end date. If an agent changes the contract end date, the system recalculates the Term value.

    For products with monthly periodicity, the per-day price \(pro-rate multiplier\) is based on the Unit list price/number of days in the month. For a product with annual periodicity, the per-day price \(prp-rate multiplier\) that is multiplied against the decimal fields is the Unit price/365 days or 366 days if the year is a leap year.


## How subscription pricing revenues are calculated

Product offers for products and services contain basic pricing information, such as list price and pricing method \(either one-time or recurring periodicity\). When agents add product lines to opportunities and quotes, the system uses basic pricing information and product line details to auto-calculate the various revenue subscription values. These values are calculated and displayed in both the header pricing details and line pricing details.

For example, when an agent adds an opportunity line, the system calculates the Cumulative Monthly Recurring Revenue \(MRR\) amount using the unit net price and quantity of the product. The system then sums up the cumulative revenue to the parent line in the opportunity and displays the cumulative MRR in the pricing details of the opportunity header.

When agents use the configuration UI to add customizable products to quotes, the configurator interface displays the calculated subtotal values such as the Cumulative Monthly Recurring price for the root product offer of the line item.

The following tables describe the subscription pricing revenue amounts for opportunities and quotes and how they're calculated.

<table id="table_fmj_l32_1dc"><thead><tr><th>

Opportunity line subscription metric

</th><th>

Description

</th><th>

Calculation

</th></tr></thead><tbody><tr><td>

Unit net price

</td><td>

Price of a single unit.

</td><td>

Unit list price - pre adjustments

</td></tr><tr><td>

Cumulative one-time price

</td><td>

One-time price of the opportunity line and any child lines.

</td><td>

Unit net price \* Quantity

</td></tr><tr><td>

Cumulative MRR

</td><td>

Cumulative monthly recurring revenue of the opportunity line and any child lines. Not calculated for one-time products.

</td><td>

-   If the periodicity is monthly: Cumulative MRR = Unit net price \* Quantity
-   If the periodicity is annual: Cumulative MMR = \(Unit net price/12 months\) \* Quantity

</td></tr><tr><td>

Cumulative ARR

</td><td>

Cumulative annual recurring revenue of the opportunity line and any child lines. Not calculated for one-time products.

</td><td>

Cumulative MRR \* 12 months

</td></tr><tr><td>

Cumulative ACV

</td><td>

Cumulative annual contract value of the opportunity and any child lines.

</td><td>

Cumulative One-time price + Cumulative ARR

</td></tr><tr><td>

Cumulative TCV

</td><td>

Cumulative total contract value of the opportunity and any child lines.

</td><td>

Cumulative One-time price + \(Cumulative MRR \* Term months\)

</td></tr></tbody>
</table>|Opportunity header subscription metric|Description|Calculation|
|--------------------------------------|-----------|-----------|
|Amount|The total contract value.|Total contract value if there are opportunity line items. If no line items exist, this amount is copied from the Estimated Deal Size.|
|Weighted amount|Value that represents the potential size of a deal.|Amount \* Probability|
|Total One-Time Price|Sum of all the cumulative one-time prices of the opportunity line items.|Cumulative one-time price of the top-level parent|
|Total MRR|Total monthly recurring revenue.|Sum of the Cumulative MRR values of the top-level parent.|
|Total ARR|Total annual recurring revenue.|Sum of the Cumulative ARR of the top-level parent.|
|Total ACV|Total annual contract value.|Sum of the Cumulative ACV of the top-level parent.|
|Total TCV|Total contract value.|Sum of the Cumulative TCV of the top-level parent.|

<table id="table_sdq_tcy_1dc"><thead><tr><th>

Quote line subscription metric

</th><th>

Calculation

</th></tr></thead><tbody><tr><td>

Monthly recurring price

</td><td>

-   If periodicity is monthly: Monthly recurring price = Unit net price \* Quantity
-   If periodicity is annual: Monthly recurring price = \(Unit net price/12\) \* Quantity

</td></tr><tr><td>

Annual recurring price

</td><td>

Monthly recurring price \* 12 months

</td></tr><tr><td>

Cumulative net price

</td><td>

Unit List Price - Total adjustment

</td></tr><tr><td>

Cumulative one time price

</td><td>

One-time price for the line item + \(if parent line item\) One-time price for all child line items

</td></tr><tr><td>

One-time price

</td><td>

One-time price for the line item.

</td></tr></tbody>
</table>|Quote header subscription metric|Calculation|
|--------------------------------|-----------|
|Term|The duration in months for subscription or contract. If an opportunity exists, the value comes from the opportunity. Otherwise, the default term is 12 months.|
|Total one-time price|Sum of all parent lines.|
|Total monthly recurring price|Sum of the Cumulative monthly recurring price of all root parent lines.|
|Total annual recurring price|Sum of the Cumulative annual recurring price of all root parent lines.|
|Total amount|Sum of the Cumulative net price of root parent lines.|

<table id="table_kk2_h1w_vfc"><thead><tr><th>

Order line subscription metric

</th><th>

Calculation

</th></tr></thead><tbody><tr><td>

Term

</td><td>

Contract end date - Contract start date

</td></tr><tr><td>

Contract start date

</td><td>

The start date of having access to the service or product

</td></tr><tr><td>

Contract end date

</td><td>

The end date of having access to the service or product

</td></tr><tr><td>

Unit adjustment

</td><td>

Total adjustment/Quantity

</td></tr><tr><td>

Monthly recurring price

</td><td>

-   If periodicity is monthly: Monthly recurring price = Unit net price \* Quantity
-   If periodicity is annual: Monthly recurring price = \(Unit net price/12\) \* Quantity

</td></tr><tr><td>

Annual recurring price

</td><td>

If pricing method is recurring: Monthly recurring price \* 12 months

</td></tr><tr><td>

Cumulative monthly price

</td><td>

Monthly recurring price for the line + \(if parent line item\) sum of all monthly recurring price of immediate child lines

</td></tr><tr><td>

Cumulative annual price

</td><td>

Cumulative monthly recurring price \* 12

</td></tr><tr><td>

Cumulative Net Price

</td><td>

\[One time price + \(Monthly recurring price \* Term\)\]+\(if parent line item\) sum of all Cumulative net price for immediate child lines

</td></tr></tbody>
</table>|Order header subscription metric|Calculation|
|--------------------------------|-----------|

To learn more about the revenue metrics in opportunity details, see [Add and view the details of an opportunity](opportunity-management-details-tab.md) and [Add line items to an opportunity](opportunity-management-line-items-tab.md).

To learn more about the revenue metrics in quote details, see [Add and view details of a quote](../task/quote-management-details-tab.md).

