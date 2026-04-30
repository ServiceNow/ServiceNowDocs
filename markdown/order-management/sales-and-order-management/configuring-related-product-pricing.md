---
title: Configuring derived pricing
description: Automatically set the pricing for a product by deriving its pricing from other products or pricing sources such as transactional values in quotes or orders.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-11"
reading_time_minutes: 2
breadcrumb: [Pricing Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configuring derived pricing

Automatically set the pricing for a product by deriving its pricing from other products or pricing sources such as transactional values in quotes or orders.

## Derived pricing overview

As a pricing admin or manager, you can define rules for deriving product pricing dynamically, relative to other products or transactional values such as the total contract value \(TCV\) or annual contract value \(ACV\). When products with derived pricing are added to a quote or order, the derived pricing is applied automatically. Derived pricing can be used in various scenarios:

<table id="table_gfn_hdg_mhc"><thead><tr><th>

Pricing scenario

</th><th>

Industry use case

</th><th>

Calculation

</th></tr></thead><tbody><tr><td>

Price accessories relative to related base equipment

</td><td>

Manufacturing: Sell an extended warranty that is 10% of the price of a high-end industrial machine

</td><td>

Define the warranty pricing as 10% of the referenced equipment:Product A price = 10% of Product B's price

</td></tr><tr><td>

Price add-ons that are based on Product X and Y total

</td><td>

Telecom: Sell 24x7 support as an add-on that is 10% of all the subscription products in a quote

</td><td>

Define 24x7 support add-on as 10% of the quote total: Product C price = 10% of the price for Product X and Y

</td></tr><tr><td>

Price add-ons based on a percentage of all products purchased

</td><td>

SaaS: Sell product support service as an add-on that is 15% of subscription fees for all software products purchased

</td><td>

Define the product support add-on as 15% of subscription fees for all software products: Product D price = 15% of all subscription fees

</td></tr></tbody>
</table>Derived pricing for a product involves the following items, which you manage through the Derived Pricing Matrix:

|Item|Description|
|----|-----------|
|Target product offering|Product offering for which pricing is derived.|
|Source product offering|One or more product offerings whose pricing is the basis for the target offering.|
|Transaction header value \(context variable\)|Quote-level header value used as the pricing basis to calculate the derived price, such as the annual contract value \(ACV\).|
|Scope|Level from which the context variable is used: bundle or cart|
|Formula calculation|Percentage used to calculate the derived pricing|
|Price point|Price at which the product is sold: Unit list price, Unit net price, and Cumulative net price.|

## Limitations for derived pricing

Related pricing are not supported for quotes of type sales agreements.

## Setting up derived pricing

To implement related pricing, follow these tasks:

|Task|Description|Role|
|----|-----------|----|
|[Enable related \(derived\) pricing for a price list line](../task/som-create-price-list-line.md)|When creating a price list line, select the Derive price option.|Pricing admin or manager|
|[Create rules for derived product pricing](../task/create-derived-pricing-source.md)|Use the Derived Pricing Matrix to define the product relationships and calculations used when deriving product pricing.|Pricing admin or manager|

