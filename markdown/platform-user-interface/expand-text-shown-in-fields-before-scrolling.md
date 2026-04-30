---
title: Set up automatic resizing for fields
description: Enable multi-line text, HTML, and journal fields to display longer content automatically without requiring agents to scroll.Configure autoresize system properties that enable users to automatically adjust the size of multi-line text, HTML, and journal fields.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering forms for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Set up automatic resizing for fields

Enable multi-line text, HTML, and journal fields to display longer content automatically without requiring agents to scroll.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Select **Name** for the search value, and enter `autoresize` into the search bar.

    ![Search for autoresize](../image/autoresize-search.png)

3.  Select an autoresize system property to enable autoresize and set a line limit.


## Autoresize system properties

Configure autoresize system properties that enable users to automatically adjust the size of multi-line text, HTML, and journal fields.

|System property name|Function|Configuration|
|--------------------|--------|-------------|
|glide.ui.textarea.autoresize\_line\_limit|Determines the line number after which the scroll bar should appear for the text area component in all text area fields.|Enter a maximum value for text area fields to automatically resize.|
|glide.ui.journal.use\_html|Converts all journal fields with a text area subtype to HTML editor fields.|Set the Value field to **true**.|
|glide.ui.journal.html.editor.autoresize|Activates the autoresize plugin in all journal fields with the HTML subtype.|Set the Value field to **true**.|
|glide.ui.journal.html.editor.autoresize\_line\_limit|Determines the line number after which the scroll bar should appear for the HTML editor component in all journal fields with the HTML subtype.|Effective if glide.ui.journal.html.editor.autoresize is set to true. Enter a maximum value for journal fields to automatically resize.|
|glide.ui.html.editor.autoresize\_line\_limit|Determines the line number after which the scroll bar should appear for the HTML editor component in all HTML fields.|Effective if autoresize is added to glide.ui.html.editor.v5.enabled\_plugins. Enter a maximum value for HTML fields to automatically resize.|
|glide.ui.html.editor.v5.enabled\_plugins|Controls the availability of specific features in the HTML editor with specified plugins.|Add the autoresize plugin.|
|glide.activity.compose.textarea.autoresize\_line\_limit|Determines the line number after which the scroll bar should appear for the text area component in all Activity stream textarea fields.|Enter a maximum value for text area fields to automatically resize.|
|glide.activity.compose.html.autoresize\_line\_limit|Determines the line number after which the scroll bar should appear for the HTML editor component in all Activity stream journal fields with the HTML subtype.|Effective if glide.activity.compose.html.autoresize is set to true. Enter a maximum value for journal fields to automatically resize.|
|glide.activity.compose.html.autoresize|Activates the autoresize plugin in all Activity stream journal fields with the HTML subtype.|Set the Value field to **true**.|

