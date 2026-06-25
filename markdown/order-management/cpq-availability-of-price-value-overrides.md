---
title: Availability of price value overrides
description: See which component types accept price-value overrides for zero-priced and null-priced items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-availability-of-price-value-overrides.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up pricing display, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Availability of price value overrides

See which component types accept price-value overrides for zero-priced and null-priced items.

<table id="table_bm2_ckr_jhc"><thead><tr><th>

Component type

</th><th>

Zero-price override

</th><th>

Null-price override

</th></tr></thead><tbody><tr><td>

Number field with ReadOnlyCurrency display type

</td><td>

Yes

</td><td>

\(Cannot be set to null\)

</td></tr><tr><td>

Picklist extension - static &amp; dynamic pricing

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Product Picker - price fields

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

ProductList.price

</td><td>

Yes

</td><td>

See note

</td></tr><tr><td>

ProductList.extended.&lt;currency field&gt;

</td><td>

Yes

</td><td>

Yes

</td></tr></tbody>
</table>**Note:**

To set a null-price override on a currency field, the administrator can set `ProductList.extended.<numericField> = ""` in an advanced product action or by using the OnBom enrichment. In the layout, define this numeric field to display as currency in the column properties of the product list, and follow the instructions in [Set a custom message for zero-priced and null-priced items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown) regarding override strings in the product list properties.

**Related topics**  


[Set a custom message for zero-priced and null-priced items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Override the shopping cart total when a null-priced item is included](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

