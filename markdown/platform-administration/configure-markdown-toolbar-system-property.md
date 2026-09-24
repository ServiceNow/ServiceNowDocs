---
title: Configure Markdown toolbar using system properties
description: Configure the toolbar options for Markdown editors across all tables in the platform using a system property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/configure-markdown-toolbar-system-property.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Markdown field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Markdown toolbar using system properties

Configure the toolbar options for Markdown editors across all tables in the platform using a system property.

## Before you begin

Role required: admin

## About this task

The Markdown field type provides a default toolbar. You can customize the toolbar options globally for all Markdown editors in the platform.

## Procedure

1.  In the application navigator, enter `sys_properties.list` to navigate to the System Properties \[sys\_properties\] table.

2.  In the Name column, search for **glide.ui.markdown.editor.toolbar**.

3.  Select the **glide.ui.markdown.editor.toolbar** property.

4.  In the Value field, modify the toolbar options.

    The default value is: `heading | bold italic strike code | ul ol tasklist | link table codeblock | quote hr | download fullscreen`

    Available toolbar options: `heading`, `bold`, `italic`, `strike`, `highlight`, `subscript`, `superscript`, `code`, `ul`, `ol`, `tasklist`, `link`, `table`, `codeblock`, `quote`, `hr`, `download`, `fullscreen`.

    Use the pipe character \(\|\) to separate groups of options.

5.  Select **Update**.


**Related topics**  


[Configure Markdown toolbar using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/configure-markdown-toolbar-dictionary-attribute.md)

[Markdown toolbar options and syntax](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/markdown-toolbar-options-reference.md)

