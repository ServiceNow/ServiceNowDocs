---
title: Enable Markdown in text fields
description: Markdown lets you format rich text using an easy-to-remember plain text syntax.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/enable-markdown-in-text-fields.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure fields, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Enable Markdown in text fields

Markdown lets you format rich text using an easy-to-remember plain text syntax.

## Before you begin

Role required: Admin

## About this task

CPQ text fields support Markdown, a widely used, lightweight markup language for formatting text using plain-text syntax.

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


[Markdown syntax](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Markdown options for read-only text](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/layout_readonlytext_markdown_options.md)

