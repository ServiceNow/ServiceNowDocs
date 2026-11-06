---
title: Formatting manual price adjustment values
description: Dynamic field formatting keeps manual price adjustment values clear and consistent for sellers. The adjustment value field automatically displays as a currency amount or a percentage based on the adjustment type, reducing entry errors and making quotes easier to review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/dynamic\_formatting\_price\_adjustments.html
release: australia
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Pricing in the ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Formatting manual price adjustment values

Dynamic field formatting keeps manual price adjustment values clear and consistent for sellers. The adjustment value field automatically displays as a currency amount or a percentage based on the adjustment type, reducing entry errors and making quotes easier to review.

To apply a manual price adjustment to a transaction line in productized pricing, the seller selects an adjustment type and enters an adjustment value. A discount reason is optional. The adjustment is stored in the **Price Adjustments** JSON field.

The adjustment types are:

|Label|Value|Description|
|-----|-----|-----------|
|Markdown %|`MARKDOWN_PER`|Deducts a percentage from the unit list price.|
|Markdown Amount|`MARKDOWN_AMT`|Deducts a fixed currency amount from the unit list price.|
|Price Override|`PRICE_OVERRIDE`|Sets the net price to the entered value.|

The adjustment value means something different for each type, so its display format depends on the type. Markdown Amount and Price Override values display with a currency symbol. Markdown % values display with a % suffix.

The format is set with dynamic field formatting in the transaction layout. For the steps, see [Configure dynamic formatting for the adjustment value field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/configure_dynamic_formatting_price_adjustments.md).

**Warning:** The adjustment value is sent to pricing as the number that was entered. To display a percentage without changing that number, use the `unit` format type with `unit: percent`. Do not use the `percent` format type. It formats the underlying value as a percentage, so 0.25 displays as 25%, but the underlying value is sent to pricing as-is, and the adjusted values are off by a factor of 2.

