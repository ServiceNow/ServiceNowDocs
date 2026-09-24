---
title: Override the shopping cart total
description: To avoid displaying an incorrect total price, show a custom string when a bill of materials includes an item with a null price.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-override-the-shopping-cart-total-when-a-null-priced-item-is-included.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [shopping cart, bill of materials, null price, custom message]
breadcrumb: [Set up pricing display, CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Override the shopping cart total

To avoid displaying an incorrect total price, show a custom string when a bill of materials includes an item with a null price.

## Before you begin

Role required: admin

## About this task

When a BOM contains null-priced items, the total price may be incorrect. You can define a custom string to display instead of the BOM total.

## Procedure

1.  In the layout editor, open the product list properties.

    \[Omitted image "cpq-layout-custom-message-gear-icon.png"\] Alt text: Product list

2.  In the properties dialog, set **Override display of Total for incomplete pricing** to true, and enter the string to display instead of the total's place.

    \[Omitted image "cpq-layout-custom-message-override-display.png"\] Alt text: Product list properties

3.  Select **Save**.


**Related topics**  


[Set a custom message for zero-priced and null-priced items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-set-a-custom-message-for-zero-priced-and-null-priced-items.md)

[Availability of price value overrides](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cpq-availability-of-price-value-overrides.md)

