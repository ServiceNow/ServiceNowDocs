---
title: Change how messages are displayed to the end user
description: Control how messages appear in CPQ.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Change how messages are displayed to the end user

Control how messages appear in CPQ.

You can show messages to the end user in different formats.

By default, the messages shown for fields on a layout when messaging rules are fired are shown below the field.

![Field showing the default message style](../images/cpq-messages-below.png)

However, you can override this behavior, such as to show an icon which can be hovered over to display the message \("tooltip"\).

![Field showing the tooltip message style](../images/cpq-messages-tooltip.png)

In the layout editor, add `{“messageDisplayType”: “<type>”}` to the raw value in the field properties \(the gear icon\) of the element where you want to add the custom message display type.

Accepted type values are `above`, `below`, `popup`, and `tooltip`.

The following image shows a popup message \(`{“messageDisplayType”: “popup”}`\).

![Field showing the popup message style](../images/cpq-messages-popup.png)

