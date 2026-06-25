---
title: Modifying the Size and Change Size fields for a set
description: You can change the appearance of the size fields for a set, or hide them altogether.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/how\_to\_alterhide\_the\_size\_and\_change\_size\_field\_for\_a\_set.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure sets, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Modifying the Size and Change Size fields for a set

You can change the appearance of the size fields for a set, or hide them altogether.

\[Omitted image "cpq-sets-size-and-change-size-fields.png"\] Alt text: User interface

You can hide these fields by making an adjustment in the layout of the blueprint. In the layout editor, click the gear icon next to the set:

\[Omitted image "cpq-layout-editor-edit-set-layout.png"\] Alt text: Layout screen

In the size settings, you can choose to show or hide the set size field, as well as the appearance, location, and behavior of the field:

\[Omitted image "cpq-layout-editor-size-settings.png"\] Alt text: Layout screen

An admin can also hide the size field by modifying the Set type value column in the layout CSV file. Enter the following:

```
{ "sizeControl": { "visible": false } }
```

For more information about how to control the size and behavior of sets, see [Using sets in layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/layouts-sets.md).

**Related topics**  


[Example: Use a custom field to dynamically control set size](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Configure sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sets.md)

