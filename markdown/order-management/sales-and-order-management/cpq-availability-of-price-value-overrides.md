---
title: Availability of price value overrides
description: See which component types accept price-value overrides for zero-priced and null-priced items.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up pricing display, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
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

To set a null-price override on a currency field, the administrator can set `ProductList.extended.<numericField> = ""` in an advanced product action or by using the OnBom enrichment. In the layout, define this numeric field to display as currency in the column properties of the product list, and follow the instructions in [Set a custom message for zero-priced and null-priced items](cpq-set-a-custom-message-for-zero-priced-and-null-priced-items.md) regarding override strings in the product list properties.

**Related topics**  


[Set a custom message for zero-priced and null-priced items](cpq-set-a-custom-message-for-zero-priced-and-null-priced-items.md)

[Override the shopping cart total when a null-priced item is included](cpq-override-the-shopping-cart-total-when-a-null-priced-item-is-included.md)

