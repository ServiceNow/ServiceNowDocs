---
title: Adding a field with an extended picklist to the layout
description: Add an extended picklist field to a CPQ layout by placing it in a column set and defining each extension column in the layout CSV. Make sure that the picklist extension is marked “Available in layout” so its data appears correctly in the user interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/layout\_extended\_picklist.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure picklist extensions, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Adding a field with an extended picklist to the layout

Add an extended picklist field to a CPQ layout by placing it in a column set and defining each extension column in the layout CSV. Make sure that the picklist extension is marked “Available in layout” so its data appears correctly in the user interface.

Adding a field with an extended picklist to the layout is similar to how a field is added to a layout. First the field has to be added to a Columnset in a Tier. After that, each column of the extended picklist must be added to the layout with the field added at the end of the path. In the following example, row 16 adds the field “dogBreed” to the layout. The path in rows 17- 24 all have “dogBreed” at the end of the path. They also have the value, fieldExtension, in the type column \(column A\).

\[Omitted image "cpq-layout-extended-picklist-csv.png"\] Alt text: Extended picklist to the layout

It is also important to make sure that any extension that will be added to the layout is selected on the picklist extension menu by checking the “Available in layout” box.

\[Omitted image "cpq-layout-extended-picklist-available-in-layout.png"\] Alt text: Extended picklist to the layout

The setup above images would result in the following layout:

\[Omitted image "cpq-layout-extended-picklist-select-your-doggo.png"\] Alt text: Extended picklist to the layout

**Related topics**  


[Displaying a picklist extension on a layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/csv_layouts_how_do_i_display_a_picklist_extension.md)

