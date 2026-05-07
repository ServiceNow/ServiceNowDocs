---
title: Override the shopping cart total when a null-priced item is included
description: To avoid displaying an incorrect total price, show a custom string when a bill of materials includes an item with a null price.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up pricing display, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Override the shopping cart total when a null-priced item is included

To avoid displaying an incorrect total price, show a custom string when a bill of materials includes an item with a null price.

## Before you begin

Role required: Admin

## About this task

When a BOM contains null-priced items, the total price may be incorrect. When this is the case, the administrator can define a string to display in place of the BOM total.

## Procedure

1.  In the layout editor, open the product list properties.

    ![Product list](../images/cpq-layout-custom-message-gear-icon.png)

2.  In the properties dialog, set **Override display of Total for incomplete pricing** to true, and enter the string to display in the total's place.

    ![Product list properties](../images/cpq-layout-custom-message-override-display.png)

3.  Click **Save**.


**Related topics**  


[Set a custom message for zero-priced and null-priced items](cpq-set-a-custom-message-for-zero-priced-and-null-priced-items.md)

[Availability of price value overrides](cpq-availability-of-price-value-overrides.md)

