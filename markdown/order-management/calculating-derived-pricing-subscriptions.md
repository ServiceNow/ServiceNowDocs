---
title: Calculating derived pricing for subscription products
description: The pricing engine calculates a derived product's price from the combined monthly recurring price of active source subscription products during each date segment. The derived price changes automatically when source products are added, reduced, or renewed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/calculating-derived-pricing-subscriptions.html
release: brazil
topic_type: concept
last_updated: "2026-09-21"
reading_time_minutes: 7
keywords: [derived pricing, Percentage Price, Monthly Recurring Price, subscription pricing]
breadcrumb: [Configuring derived pricing, Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Calculating derived pricing for subscription products

The pricing engine calculates a derived product's price from the combined monthly recurring price of active source subscription products during each date segment. The derived price changes automatically when source products are added, reduced, or renewed.

## How the pricing engine calculates a derived price

When a Derived Pricing Matrix rule uses the sum aggregate formula with Monthly Recurring Price as the price point, the pricing engine calculates the derived product's price from the combined monthly recurring price of the active source subscription products during each date segment. To configure these fields, see [Create rules for derived product pricing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/create-derived-pricing-source.md).

For each segment, the pricing engine does the following:

1.  Calculates the net price of each source product.

    Net Price = List Price × \(1 − Manual Discount %\)

2.  Calculates the monthly recurring price \(MRP\) of each source product.

    Monthly Recurring Price \(MRP\) = Qty × Net Price

3.  Calculates the segment net price.

    Segment Net Price = MRP × Number of Months in Segment

4.  Sums the MRP of every source product that's active during the segment to get the cumulative net price for that segment.

    Cumulative Net Price = Sum of \(Segment Net Price\) for all active sources

5.  Applies the rule's Percentage Price to the cumulative net price to get the derived product's price for that segment.

    Target Product Price \(pre-discount\) = Cumulative Net Price × Percentage Price %

6.  If a manual discount is entered on the derived product line, applies that discount to get the final price.

    Final target product price = Target Product Price × \(1 − Manual Discount % on target product\)


## Example: Quote with multiple source subscriptions

Boxeo buys three source subscription products on a one-year contract, each in a different bundle, with different start and end dates and a negotiated discount. The Derived Pricing Matrix rule for this example uses Account as its Scope, so the pricing engine totals every active source across Boxeo's account regardless of which bundle it's in, as listed in the following table.

|Source product|Quantity|Start date|End date|List price|Manual discount|Net price|Monthly recurring price|Bundle|
|--------------|--------|----------|--------|----------|---------------|---------|-----------------------|------|
|ITSM|100|January 1|December 31|$10|15%|$8.50|$850|Bundle 1|
|CSM|50|April 1|September 30|$20|10%|$18|$900|Bundle 1|
|HRSD|20|July 1|December 31|$15|20%|$12|$240|Standalone|

Because the sources start and end on different dates, the pricing engine creates four segments and calculates the derived product's price for each from the sources active during that segment, including HRSD even though it's in a different bundle from ITSM and CSM. This rule uses a Percentage Price of 10%, with no discount on the derived product line, as shown in the following table.

|Segment|Active source products|Combined monthly recurring price|Months in segment|Cumulative net price|Derived price \(10%\)|
|-------|----------------------|--------------------------------|-----------------|--------------------|---------------------|
|January 1 - March 31|ITSM|$850|3|$2,550|$255|
|April 1 - June 30|ITSM, CSM|$1,750|3|$5,250|$525|
|July 1 - September 30|ITSM, CSM, HRSD|$1,990|3|$5,970|$597|
|October 1 - December 31|ITSM, HRSD|$1,090|3|$3,270|$327|

## Example: Upsell adds a source subscription mid-term

On July 1, the customer adds a fourth source subscription product, SecOps, effective from July 1 through December 31: quantity 10, $25 list price, 5% discount, giving a monthly recurring price of $237.50.

The SecOps start date falls inside the existing July 1 - September 30 and October 1 - December 31 segments, so the pricing engine adds the SecOps monthly recurring price to the cumulative net price of both segments and recalculates the derived price for each. The January 1 - March 31 and April 1 - June 30 segments are unaffected because SecOps isn't active during them, as shown in the following table.

|Segment|Active source products|Combined monthly recurring price|Months in segment|Cumulative net price|Derived price \(10%\)|
|-------|----------------------|--------------------------------|-----------------|--------------------|---------------------|
|July 1 - September 30|ITSM, CSM, HRSD, SecOps|$2,227.50|3|$6,682.50|$668.25|
|October 1 - December 31|ITSM, HRSD, SecOps|$1,327.50|3|$3,982.50|$398.25|

## Example: Downsell reduces a source subscription mid-segment

On October 15, the customer reduces the ITSM quantity from 100 to 50, cutting its monthly recurring price from $850 to $425. Because the change takes effect partway through the October 1 - December 31 segment, the pricing engine splits that segment at the change date and prorates each part by the number of days it covers, as shown in the following table.

|Segment|Active source products|Combined monthly recurring price|Months in segment|Cumulative net price|Derived price \(10%\)|
|-------|----------------------|--------------------------------|-----------------|--------------------|---------------------|
|October 1 - October 14|ITSM \(qty 100\), HRSD, SecOps|$1,327.50|0.47|$623.93|$62.39|
|October 15 - December 31|ITSM \(qty 50\), HRSD, SecOps|$902.50|2.53|$2,283.33|$228.33|

If the seller also enters a manual discount on the derived product line, that discount applies only to the price for the segment created by the change, not to segments that came before it. For example, a 5% discount on the October 15 - December 31 segment reduces its derived price from $228.33 to $216.92.

## Example: Renewal with updated list prices and source products

A one-year contract renews with a new source product mix and updated list prices. Because both source products span the full renewal term, the pricing engine creates a single segment for the derived product, as listed in the following table.

|Source product|Quantity|Start date|End date|List price|Manual discount|Net price|Monthly recurring price|
|--------------|--------|----------|--------|----------|---------------|---------|-----------------------|
|ITSM|100|January 1|December 31|$12|10%|$10.80|$1,080|
|Platform|50|January 1|December 31|$50|5%|$47.50|$2,375|

The pricing engine sums the monthly recurring prices \($1,080 plus $2,375 equals $3,455 a month\), multiplies by the 12-month term to get a cumulative net price of $41,460, then applies the 10% Percentage Price to get a derived price of $4,146 for the renewal term. This is higher than the prior term's derived price of $1,020, which reflected only ITSM at its previous list price.

## Example: Sources on more than one contract

Boxeo has two active contracts. ITSM and CSM are sold on Contract 1; HRSD is sold on Contract 2. All three are source products for the same derived product, and the rule's Scope is Account, so the pricing engine totals every active source across Boxeo's account regardless of which contract it's on, as listed in the following table.

|Source product|Quantity|List price|Manual discount|Net price|Monthly recurring price|Term|Contract|
|--------------|--------|----------|---------------|---------|-----------------------|----|--------|
|ITSM|250|$10|10%|$9|$2,250|January 1 - December 31|Contract 1|
|CSM|300|$8|10%|$7.20|$2,160|January 1 - December 31|Contract 1|
|HRSD|400|$5|10%|$4.50|$1,800|January 1 - December 31|Contract 2|

Because all three sources run for the same term, the pricing engine creates a single derived line spanning January 1 through December 31, with a combined monthly recurring price of $6,210. Over the 12-month term that gives a cumulative net price of $74,520, and a Percentage Price of 10% makes the annual derived price $7,452.

On July 1, Boxeo upsells ITSM on Contract 1 by adding 50 more licenses, effective through the end of the term. The pricing engine splits the derived line at July 1: the January 1 - June 30 segment keeps its original dependent source products and price, and the pricing engine creates a new July 1 - December 31 segment whose dependent source products include the upsell line in addition to ITSM, CSM, and HRSD, as shown in the following table.

|Segment|Dependent source products|Combined monthly recurring price|Months in segment|Cumulative net price|Derived price \(10%\)|
|-------|-------------------------|--------------------------------|-----------------|--------------------|---------------------|
|January 1 - June 30|ITSM \(Contract 1\), CSM \(Contract 1\), HRSD \(Contract 2\)|$6,210|6|$37,260|$3,726|
|July 1 - December 31|ITSM \(Contract 1\), CSM \(Contract 1\), HRSD \(Contract 2\), ITSM upsell \(Contract 1\)|$6,660|6|$39,960|$3,996|

**Note:** The derived line and its segments belong to the account, not to either contributing contract. Amending one contract's source products doesn't require you to also amend the other contract, and the derived line continues to reflect every active source across the account.

