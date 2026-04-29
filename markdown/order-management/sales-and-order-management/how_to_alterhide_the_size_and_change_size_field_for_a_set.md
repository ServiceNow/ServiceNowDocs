---
title: Modifying the Size and Change Size fields for a set
description: You can change the appearance of the size fields for a set, or hide them altogether.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure sets, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Modifying the Size and Change Size fields for a set

You can change the appearance of the size fields for a set, or hide them altogether.

![User interface](../images/cpq-sets-size-and-change-size-fields.png)

You can hide these fields by making an adjustment in the layout of the blueprint. In the layout editor, click the gear icon next to the set:

![Layout screen](../images/cpq-layout-editor-edit-set-layout.png)

In the size settings, you can choose to show or hide the set size field, as well as the appearance, location, and behavior of the field:

![Layout screen](../images/cpq-layout-editor-size-settings.png)

An admin can also hide the size field by modifying the Set type value column in the layout CSV file. Enter the following:

```
{ "sizeControl": { "visible": false } }
```

For more information about how to control the size and behavior of sets, see [Using sets in layouts](layouts-sets.md).

**Related topics**  


[Example: Use a custom field to dynamically control set size](example-use-a-custom-field-to-dynamically-control-set-size.md)

[Configure sets](sets.md)

