---
title: Configure Markdown toolbar using dictionary attributes
description: Configure the toolbar options for a specific Markdown field using a dictionary attribute.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/configure-markdown-toolbar-dictionary-attribute.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Markdown field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Markdown toolbar using dictionary attributes

Configure the toolbar options for a specific Markdown field using a dictionary attribute.

## Before you begin

Role required: admin

## About this task

You can customize the toolbar options for a specific Markdown field without affecting other Markdown fields in the platform.

## Procedure

1.  Navigate to the dictionary configuration screen for the Markdown field.

2.  Select **Advanced view**.

3.  In the Attributes field, add the dictionary attribute **markdown\_toolbar** and specify the toolbar options.

    Available toolbar options: `heading`, `bold`, `italic`, `strike`, `highlight`, `subscript`, `superscript`, `code`, `ul`, `ol`, `tasklist`, `link`, `table`, `codeblock`, `quote`, `hr`, `download`, `fullscreen`.

    Use the pipe character \(\|\) to separate groups of options.

    Example: `markdown_toolbar=heading | bold italic | link`

4.  Select **Update**.


**Related topics**  


[Configure Markdown toolbar using system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/configure-markdown-toolbar-system-property.md)

[Markdown toolbar options and syntax](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/markdown-toolbar-options-reference.md)

