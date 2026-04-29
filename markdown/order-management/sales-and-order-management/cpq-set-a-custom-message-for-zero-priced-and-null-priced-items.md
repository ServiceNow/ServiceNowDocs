---
title: Set a custom message for zero-priced and null-priced items
description: Customize how zero-priced and null-priced items appear in CPQ layouts. Replace $0.00 or missing prices with custom messages—such as “Included,” “Pending,” or “Price TBD”—across product pickers, picklist extensions, and shopping cart components for clearer user communication.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up pricing display, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Set a custom message for zero-priced and null-priced items

Customize how zero-priced and null-priced items appear in CPQ layouts. Replace $0.00 or missing prices with custom messages—such as “Included,” “Pending,” or “Price TBD”—across product pickers, picklist extensions, and shopping cart components for clearer user communication.

## Before you begin

Role required: Admin

## About this task

Some configurations result in items that have a zero price or a null price. In these scenarios, the administrator may want to display a message in place of the zero or null price. Using the layout editor, you can define custom strings for null-priced or zero-priced items in product pickers, picklist extensions \(with dynamic pricing\), and the shopping cart.

Administrators frequently replace the $0.00 value with the display string "Included".

When the price is null, the solution may include components that require research or engineering before a price can be shared with the end user. When this is the case, the administrator may display strings such as "Pending" or "Price TBD". When a null-priced item is in the cart, the sum of cart items displayed in the total may be misleading. To alleviate this confusion, the administrator can define a string that overrides the cart total when null-priced items are present. For step by step instructions, see [Override the shopping cart total when a null-priced item is included](cpq-override-the-shopping-cart-total-when-a-null-priced-item-is-included.md).

For a list of components that support null-price and zero-price overrides, see [Availability of price value overrides](cpq-availability-of-price-value-overrides.md).

## Procedure

1.  In the layout editor, click the gear icon associated with the header.

2.  In the Layout Properties dialog, toggle the appropriate "Override format" switches, and enter the strings you would like to show in place of the price.

    ![Layout properties](../images/cpq-layout-custom-message-set-default.png)

3.  Save the layout properties, save the layout, and deploy.

    **Note:** If you want to apply distinct price display behaviors at the component level, this can be done in the layout properties of each read-only currency field, picklist extension, product picker, or product list element. When formatting is set at the element level, it overrides the format defined at the layout level.


**Related topics**  


[Override the shopping cart total when a null-priced item is included](cpq-override-the-shopping-cart-total-when-a-null-priced-item-is-included.md)

[Availability of price value overrides](cpq-availability-of-price-value-overrides.md)

