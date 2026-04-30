---
title: Change how messages are displayed to the end user
description: Control how messages appear in ServiceNow CPQ.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Change how messages are displayed to the end user

Control how messages appear in ServiceNow CPQ.

You can show messages to the end user in different formats.

By default, the messages shown for fields on a layout when messaging rules are fired are shown below the field.

However, you can override this behavior, such as to show an icon which can be hovered over to display the message \("tooltip"\). In the layout editor, add `{“messageDisplayType”: “<type>”}` to the raw value in the field properties \(the gear icon\) of the element where you want to add the custom message display type.

Accepted type values are `above`, `below`, `popup`, and `tooltip`.

The following image shows a popup message \(`{“messageDisplayType”: “popup”}`\).

![Message](../images/cpq-messages-default.png)

