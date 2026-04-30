---
title: Markdown options for read-only text
description: Enable markdown formatting for ReadOnlyText components in ServiceNow CPQ layouts to enhance text presentation. Use syntax for bold, italics, lists, links, images, and dynamic field values to create clear, engaging, and context-aware display text in configurations.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [Enable Markdown in text fields, Configure fields, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Markdown options for read-only text

Enable markdown formatting for ReadOnlyText components in ServiceNow CPQ layouts to enhance text presentation. Use syntax for bold, italics, lists, links, images, and dynamic field values to create clear, engaging, and context-aware display text in configurations.

This article describes the markdown syntax and behaviors available to administrators when a text field is defined on a native ServiceNow CPQ UI layout with component display type ReadOnlyText. For a broader discussion of layout options, see [CSV layout upload](csv_layout_upload.md).

To apply markdown formatting to a ReadOnlyText component:

1.  In the layout editor, open the field properties \(button with cog icon\)
2.  Add the following as the raw value: `{ "enableMarkdown": true }`
3.  Use the following markdown syntax in the text field value.

<table><thead><tr><th>

Formatting Option

</th><th>

Syntax

</th><th>

Output

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Bold

</td><td>

\*\*this will be bold\*\*

</td><td>

**bold text**

</td><td>

A double underscore instead of the double \* will also work

</td></tr><tr><td>

Italics

</td><td>

\*this will be italic\*

</td><td>

*italic text*

</td><td>

A single underscore instead of the single \* will also work

</td></tr><tr><td>

Unordered List

</td><td>

Item\\r- Item\\r- Item

</td><td>

-   Item
-   Item
-   Item

</td><td>

 

</td></tr><tr><td>

Ordered List

</td><td>

1.Item\\r2. Item\\r3. Item

</td><td>

1.  Item
2.  Item
3.  Item

</td><td>

 

</td></tr><tr><td>

Newline

</td><td>

\\n

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Link

</td><td>

\[link display text\] \(https://www.example.com\)

</td><td>

[link display text](https://www.example.com)

</td><td>

Any JavaScript entered will be sanitized

</td></tr><tr><td>

Image

</td><td>

!\[alt text\]\(image url, "title text"\)

</td><td>

N/A

</td><td>

 

</td></tr><tr><td>

Dynamic Text

</td><td>

\{\{fieldVariableName\}\}

</td><td>

 

</td><td>

Outputs the value of the selected field in the text

</td></tr><tr><td>

Dynamic Non- Field Text

</td><td>

\{\{txn\#rowNumber\}\}

</td><td>

 

</td><td>

Outputs the value of the dynamic text based on context

 Currently, only rowNumber in a txn line is supported

</td></tr></tbody>
</table>This markdown syntax is the same as that available for field help popups.

