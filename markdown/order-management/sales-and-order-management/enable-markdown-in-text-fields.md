---
title: Enable Markdown in text fields
description: Markdown lets you format rich text using an easy-to-remember plain text syntax.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Configure fields, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Enable Markdown in text fields

Markdown lets you format rich text using an easy-to-remember plain text syntax.

## Before you begin

Role required: Admin

## About this task

ServiceNow CPQ text fields support Markdown, a widely used, lightweight markup language for formatting text using plain-text syntax.

## Procedure

1.  In the layout editor, click the gear icon.

2.  Enter the following JSON text as the raw value for the field properties:

    ```
    {
      "enableMarkdown": true
    }
    ```

3.  Click **Edit Field Info**.

4.  Select ReadOnlyText as the display type for the field that will accept Markdown text.


**Related topics**  


[Markdown syntax](markdown-syntax-supported-in-servicenow-cpq.md)

[Markdown options for read-only text](layout_readonlytext_markdown_options.md)

