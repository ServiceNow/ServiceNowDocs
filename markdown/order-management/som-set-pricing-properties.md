---
title: Set properties to control pricing processing
description: Activate or deactivate system properties that control how pricing features are processed in Sales Customer Relationship Management applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/som-set-pricing-properties.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set properties to control pricing processing

Activate or deactivate system properties that control how pricing features are processed in Sales Customer Relationship Management applications.

## Before you begin

Role required: admin

## About this task

You can control the following pricing features using pricing system properties:

-   Logging of pricing engine requests for debugging.
-   Multiplier term used when calculating uplifts for contract renewals.
-   Ramp segment and term basis used when calculating renewal adjustments for products with ramps.

## Procedure

1.  Navigate to **All** &gt; **Pricing** &gt; **Administration** &gt; **Properties**.

2.  Set the following properties:

<table id="table_vn2_m5m_l1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logging Pricing Requests\(sn\_csm\_pricing.log\_pricingengine\_request\)

</td><td>

Control the logging of pricing engine requests for debugging. Select **Yes** to activate logging or **No** to turn off the pricing request log.

</td></tr><tr><td>

Renewal Uplift Term\(sn\_csm\_pricing.renewal\_uplift\_term\)

</td><td>

Set the multiplier term for contract renewal uplifts, either per year or per term.

</td></tr><tr><td>

Ramp Renewal Pricing-   Set the ramp segment used as the price basis for calculating a renewal adjustment.

\(sn\_csm\_pricing.ramp\_renewal\_price\_segment\)

-   Set the term basis used when calculating renewal adjustments for ramp lines.

\(sn\_csm\_pricing.ramp\_renewal\_term\_basis\)

</td><td>

Set properties to control how pricing for ramp renewals is calculated.-   The ramp renewal price segment property is set to **Last Segment** by default, which uses the price from the final ramp segment as the price basis.

Select **First Segment** to use the price from the initial ramp segment as the price basis.

-   The ramp renewal term basis property is set to **Segment** by default, to apply the adjustment to the term of the segment identified in the ramp renewal price segment property \(sn\_csm\_pricing.ramp\_renewal\_price\_segment\).

Select **Total Ramp ** to apply the renewal adjustment across the full ramp duration.

</td></tr><tr><td>

Pricing Session Cache\(sn\_csm\_pricing.enable\_pricing\_session\_cache\)

</td><td>

For testing purposes only. Turn on \(select **Yes**\) or turn off \(select **No**\) the cache for pricing sessions.**Note:** don't set this property to **No** except for testing, as it may negatively impact pricing engine performance.

</td></tr></tbody>
</table>3.  Select **Save**.


