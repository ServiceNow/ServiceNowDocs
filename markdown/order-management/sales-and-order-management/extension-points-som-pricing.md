---
title: Use extension points in Pricing Management
description: Use extension points to call custom scripts from external sources that control pricing logic used in the Pricing Management feature of the Sales and Order Management \(SOM\) applications.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Use extension points in Pricing Management

Use extension points to call custom scripts from external sources that control pricing logic used in the Pricing Management feature of the Sales and Order Management \(SOM\) applications.

To access the available extension points, navigate to **All** &gt; **Scripted Extension Points** and in the Extension Points list, select the desired extension point to view it.

<table id="table_kyr_lyr_c1c"><thead><tr><th>

Extension point

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_csm\_pricing.DefaultCostBookExtensionPoint

</td><td>

Customize the logic for determining the default cost book used by the calling application, such as Quote Management. This extension point changes the default cost book logic for both the header and line of the calling application.

</td></tr><tr><td>

sn\_csm\_pricing.DefaultPriceListExtensionPoint

</td><td>

Customize the default price list logic used by the calling SOM applications such as Quote Management or Order Management. This extension point changes the default logic for both the header and line of the calling application.**Note:** If you want to create additional context variables, use the Price List defaulting matrix to manage the price list default at the header level. Use this extension point only for use cases that can’t use the Price List defaulting matrix. In this case, the request contains values for all the context variables, in addition to the default context variables.

</td></tr><tr><td>

sn\_csm\_pricing.ListPriceExtensionPoint

</td><td>

Customize the logic for determining a base list price. Enables you to extend the pricing engine logic and not rely on a price list and price list line to fetch the base list price.

</td></tr><tr><td>

sn\_csm\_pricing.AttributeAdjustmentExtensionPoint

</td><td>

Customize the logic that determines the attribute adjustments for a product offering. You can extend the pricing engine logic without using the Attribute Adjustment table to fetch the adjustment values.

</td></tr><tr><td>

sn\_csm\_pricing.PricingAdjustmentsExtensionPoint

</td><td>

Customize the logic that determines price adjustments for a product offering. Enables administrators \(partner implementers\) to extend the pricing engine logic by not relying on the Standard and Component Configuration Rule matrix to fetch the adjustment values.

</td></tr></tbody>
</table>