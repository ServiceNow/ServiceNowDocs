---
title: Configuring derived pricing
description: Automatically set the pricing for a product by deriving its pricing from other products or pricing sources such as transactional values in quotes or orders.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Configuring derived pricing

Automatically set the pricing for a product by deriving its pricing from other products or pricing sources such as transactional values in quotes or orders.

## Derived pricing overview

As a pricing admin or manager, you can define rules for deriving product pricing dynamically, relative to other products or transactional values such as the total contract value \(TCV\) or annual contract value \(ACV\). When products with derived pricing are added to a transaction, such as a quote or order, the derived pricing is applied automatically. Derived pricing can be used in various scenarios. Example use cases include the following:

|Pricing scenario|Industry use case|
|----------------|-----------------|
|Price accessories relative to related base equipment|Manufacturing: Sell an extended warranty that is 10% of the price of a high-end industrial machine.|
|Price add-ons that are based on Product X and Y total|Telecom: Sell 24x7 support as an add-on that is 10% of all the subscription products in a quote.|
|Price add-ons based on a percentage of all products purchased|SaaS: Sell product support service as an add-on that is 15% of subscription fees for all software products purchased.|

Derived pricing for a product involves the following items, which you manage through the Derived Pricing Matrix:

<table id="table_nlg_5yh_mhc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target product offering

</td><td>

Product offering for which pricing is derived.

</td></tr><tr><td>

Source product offering

</td><td>

One or more product offerings whose pricing is the basis for the target offering.

</td></tr><tr><td>

Transaction header value \(context variable\)

</td><td>

Field from the header for a transaction, such as quote, that is used as the pricing basis to calculate the derived price, such as the annual contract value \(ACV\).

</td></tr><tr><td>

Scope

</td><td>

Level from which the context variable is used:-   Bundle
-   Cart
-   Account

</td></tr><tr><td>

Formula calculation

</td><td>

Percentage used to calculate the derived pricing

</td></tr><tr><td>

Price point

</td><td>

Price at which the product is sold: -   Unit list price
-   Unit net price
-   Cumulative net price
-   Monthly recurring price
-   Annual recurring price

</td></tr><tr><td>

Aggregate

</td><td>

Formulas \(SUM, MIN, MAX, AVG\) used to determine a single derived product price when pricing is derived from more than one source product. Percentages and price floor and ceiling amounts are then applied as pricing adjustments to calculate the final derived product price.

</td></tr></tbody>
</table>## Limitations for derived pricing

Derived pricing is not supported for quotes of type sales agreements.

## Setting up derived pricing

To implement derived pricing, follow these tasks:

<table id="table_wj5_chs_lhc"><thead><tr><th>

Task

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

[Enable related \(derived\) pricing for a price list line](../task/som-create-price-list-line.md)

</td><td>

When creating a price list line, select the Derive price option.You can also set the **Floor price** and **Ceiling price** for a price list line.

</td><td>

Pricing admin or manager

</td></tr><tr><td>

[Create rules for derived product pricing](../task/create-derived-pricing-source.md)

</td><td>

Use the Derived Pricing Matrix to define the product relationships and calculations used when deriving product pricing.

</td><td>

Pricing admin or manager

</td></tr></tbody>
</table>