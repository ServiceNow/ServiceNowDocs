---
title: Pricing Management properties
description: System properties available with Pricing Management that enable you to control the precision applied to non-currency pricing values, tune how multiline pricing requests are processed, and set the level of detail captured for pricing engine troubleshooting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/pricing-management-properties.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Pricing Management reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Pricing Management properties

System properties available with Pricing Management that enable you to control the precision applied to non-currency pricing values, tune how multiline pricing requests are processed, and set the level of detail captured for pricing engine troubleshooting.

These properties are available for Pricing Management.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_pricing-management-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_csm\_pricing.db\_batch\_size

</td><td>

Number of transaction lines included in each batch when a multiline pricing request is read from the database. Pricing splits large requests into batches so that each database call stays within the number of items allowed in an IN clause.

 -   Type: Integer
-   Default value: 500

</td></tr><tr><td>

sn\_csm\_pricing.derived\_price\_cache\_enabled

</td><td>

Option to cache derived price rule matrix results for each source and target product offering pair.

 -   Type: Boolean
-   Default value: true
-   Role required: Price List Administrator \(sn\_csm\_pricing.pricelist\_administrator\)

</td></tr><tr><td>

sn\_csm\_pricing.derived\_price\_cache\_ttl\_hours

</td><td>

Number of hours a cached derived price rule result is kept before it expires.

 -   Type: Integer
-   Default value: 72
-   Role required: Price List Administrator \(sn\_csm\_pricing.pricelist\_administrator\)

</td></tr><tr><td>

sn\_csm\_pricing.enable\_perf\_stats

</td><td>

Option to include performance statistics, such as total and per-step timings, in the pricing engine response. Use these statistics to investigate how long a pricing request takes to process.

 -   Type: Boolean
-   Default value: false

</td></tr><tr><td>

sn\_csm\_pricing.log.verbosity

</td><td>

Level of detail captured in the Pricing Management code execution log. Each level includes the levels above it, so selecting Debug captures debug, info, warning, and error entries.

 -   Type: Choice list
-   Default value: Error \(3\)
-   Other possible values:
    -   Debug \(0\): Information that's useful when you debug the application.
    -   Info \(1\): Status information about pricing processing.
    -   Warning \(2\): Conditions that don't stop processing but may need attention.

</td></tr><tr><td>

sn\_csm\_pricing.rounding.non\_currency\_max\_precision\_digits

</td><td>

Number of decimal digits used when rounding non-currency pricing fields, such as margin percentage. This property doesn't apply to currency fields, which are rounded to the number of decimal digits defined for their currency.

 -   Type: Integer
-   Default value: 4

</td></tr></tbody>
</table>**Parent Topic:**[Pricing Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/price-management-reference.md)

