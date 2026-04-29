---
title: Configure automatic resizing
description: Configure fields to display multiple lines of content automatically without scrolling.Configure system properties for automatic resizing to display fields with multiple lines of content automatically without scrolling.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure automatic resizing

Configure fields to display multiple lines of content automatically without scrolling.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Use system properties to enable automatic resizing and set a line limit.


## System properties for automatic resizing

Configure system properties for automatic resizing to display fields with multiple lines of content automatically without scrolling.

-   **__glide.ui.textarea.autoresize\_line\_limit__**

    Determines the line number after which the scroll bar should appear for the text area component in all text area fields.

    Enter a maximum value for text area fields to automatically resize.

-   **__glide.ui.journal.use\_html__**

    Converts all journal fields with a text area subtype to HTML editor fields.

    Set the Value field to **true**.

-   **__glide.ui.journal.html.editor.autoresize__**

    Activates the autoresize plugin in all journal fields with the HTML subtype.

    Set the Value field to **true**.

-   **__glide.ui.journal.html.editor.autoresize\_line\_limit__**

    Determines the line number after which the scroll bar should appear for the HTML editor component in all journal fields with the HTML subtype.

    Effective if **glide.ui.journal.html.editor.autoresize** is set to true. Enter a maximum value for journal fields to automatically resize.

-   **__glide.ui.html.editor.autoresize\_line\_limit__**

    Determines the line number after which the scroll bar should appear for the HTML editor component in all HTML fields.

    Effective if automatic resizing is added to **glide.ui.html.editor.v5.enabled\_plugins**. Enter a maximum value for HTML fields to resize automatically.

-   **__glide.ui.html.editor.v5.enabled\_plugins__**

    Determines the line number after which the scroll bar should appear for the text area component in all Activity stream textarea fields.

    Enter a maximum value for text area fields to resize automatically.

-   **__glide.activity.compose.html.autoresize\_line\_limit__**

    Determines the line number after which the scroll bar should appear for the HTML editor component in all Activity stream journal fields with the HTML subtype.

    Effective if **glide.activity.compose.html.autoresize** is set to true. Enter a maximum value for journal fields to resize automatically.

-   **__glide.activity.compose.html.autoresize__**

    Activates the automatic resizing plugin in all Activity stream journal fields with the HTML subtype.

    Set the Value field to **true**.


