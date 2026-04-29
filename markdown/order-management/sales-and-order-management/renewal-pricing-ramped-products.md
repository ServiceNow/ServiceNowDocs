---
title: Renewal pricing for products with price and quantity ramps
description: You can control how renewal uplift pricing for product offerings with price and quantity ramps is calculated by the pricing engine. A renewal uplift is a price increase applied to a product when a contract is renewed.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-04-07"
reading_time_minutes: 4
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Renewal pricing for products with price and quantity ramps

You can control how renewal uplift pricing for product offerings with price and quantity ramps is calculated by the pricing engine. A renewal uplift is a price increase applied to a product when a contract is renewed.

## Overview of renewal pricing for products with ramps

When a product offering with ramps is up for renewal, determining the renewal unit price for the offering can be complex because a ramp may have multiple segments with different prices and quantities.

Ramp deals may also have standard \(yearly or quarterly\) and custom segment durations, making it difficult to choose which segment price to use as the price basis and the term for determining the renewal unit price used in uplift calculations. For non-ramped products, the uplift is calculated by taking the unit price and applying the uplift percentage over the renewal term.

-   **Price basis for calculating renewal unit prices**

    The renewal unit price is the starting price for a contract renewal line. The pricing engine supports two ways to calculate the renewal unit price using the segment and term. By default, the pricing engine uses the unit price basis from the last segment and the duration of the last segment for the term.

    However, the pricing engine can use the first segment as the price basis and apply the uplift across the entire ramp term \(total ramp duration\). You can set the first segment as the price basis and entire ramp term by using the pricing system properties **sn\_csm\_pricing.ramp\_renewal\_price\_segment** and **sn\_csm\_pricing.ramp\_renewal\_term\_basis**. You set these properties by using the Customization Properties for Pricing form \(navigate to **All** &gt; **Pricing** &gt; **Administration** &gt; **Properties**\).

    ![System properties for pricing, including properties for setting renewal uplift term and renewal pricing for products with price and quantity ramps](../image/customization-properties-pricing.png "Customization Properties for pricing")

    The following table shows the price basis and terms that you can control.

    |Basis option|Price|Term|
    |------------|-----|----|
    |Last segment \(Default used by pricing engine\)|Unit price from the last ramp segment|Duration of the last segment only.|
    |First segment|Unit price from the first ramp segment|Total ramp duration \(all segments combined; apply the uplift across the entire ramp term\)|

-   **Example of uplift calculations**

    The following example shows how the pricing engine uses the different price basis and term values to calculate the unit price:

    |Price basis and term|Calculation|
    |--------------------|-----------|
    |Last segment + Segment term|Last segment price: $220. Last segment = 1 year. Effective uplift = 10%. Renewal price = $220 + $22 = $242|
    |First segment + Full term|First segment price: $240. Full ramp = 3 years. Effective uplift = 10% x 3 = 30%. Renewal price = $240 + $72 = $312|

    **Note:** Quantity is always sourced from the last segment regardless of which price basis method is selected. The price basis configuration affects only the unit price and term for the uplift calculation.

-   **Non-standard segment durations**

    When a ramp has non-standard segment lengths \(for example, a segment that spans 18 months rather than 12\), the pricing engine rounds up the segment duration to the nearest full year before computing the renewal price. This provides consistent year-over-year uplift behavior even when segment lengths do not align with calendar years.


## Overriding default renewal uplift calculations

You can override the default renewal uplift calculations for ramped products made by the pricing engine by using the `sn_csm_pricing.RampRenewalUpliftCalculationExtensionPoint`. You can use this extension point to customize the logic for calculating renewal uplift pricing. Your inputs can include segment data, unit price, and term for each ramp segment.

For example, you might want the pricing engine to calculater the price basis and term for both the last and first segments to determine which price basis provides the maximum uplift amount. You could have the pricing engine choose the higher value of the two calculated renewal prices to use as the renewal price.

Using the uplift calculation example from the previous section, the pricing engine determines that the first segment price and full ramp term amount \($312\) is higher than the last segment and segment term price \($242\).

|Price basis and term|Calculation|
|--------------------|-----------|
|Last segment + Segment term|Last segment price: $220. Last segment = 1 year. Effective uplift = 10%. Renewal price = $220 + $22 = $242|
|First segment + Full term|First segment price: $240. Full ramp = 3 years. Effective uplift = 10% x 3 = 30%. Renewal price = $240 + $72 = $312|
|Value selected by pricing engine|Max \($312, $242\) = $312. The pricing engine uses the First segment price basis and Segment term to calculate the renewal price.|

## Controlling renewal uplift pricing for ramped products

Manage how the pricing engine calculates renewal uplift pricing for ramped products by using the following properties and extension point:

-   Uplift renewal multiplier: To set the uplift renewal multiplier, use the `renewal_uplift_term` system property. For more information, see [Set properties to control pricing processing](../task/som-set-pricing-properties.md).
-   Segment basis and term used by the pricing engine: Use the system properties `sn_csm_pricing.ramp_renewal_price_segment` and `sn_csm_pricing.ramp_renewal_term_basis`. To learn more, see [Set properties to control pricing processing](../task/som-set-pricing-properties.md).
-   Override the default renewal uplift calculations for ramped products: Use the `RampRenewalUpliftCalculationExtensionPoint` to customize the uplift calculation logic. Access the extension point by navigating to **All** &gt; **Pricing** &gt; **Administration** &gt; **Scripted Extension Points** and in the Extension Points list, select`sn_csm_pricing.RampRenewalUpliftCalculationExtensionPoint`. Your inputs can include data such as the unit price and term for each ramp segment.

