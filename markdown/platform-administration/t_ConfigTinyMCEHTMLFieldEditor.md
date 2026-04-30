---
title: Configure a field editor for the HTML field
description: Configure HTML fields to use TinyMCE or the legacy htmlArea editor. The TinyMCE editor provides better stability and more editing functions than the legacy htmlArea editor.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a field editor for the HTML field

Configure HTML fields to use TinyMCE or the legacy htmlArea editor. The TinyMCE editor provides better stability and more editing functions than the legacy htmlArea editor.

## Before you begin

Role required: admin

## About this task

There are two options for HTML editors:

-   TinyMCE: A field that displays text as readers would see it on the screen. TinyMCE is the default editor.
-   htmlArea: The legacy editor, which offers a more basic interface as well as a mode that shows only HTML markup.

    **Note:** htmlArea only works in Core UI, not configurable workspace.


## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Locate the **HTML field editor to use** property \(**glide.ui.html.editor**\).

3.  Select **TinyMCE** or **htmlArea**.

4.  Select **Save**.


-   **[Configuring system properties for TinyMCE HTML editor](configuring-system-properties-for-tinymce-html-editor.md)**  
There are multiple system properties that are used to configure the behaviour of the HTML editor field type. Learn about the system properties available in the TinyMCE rich text editor.
-   **[Configuring plugins for the TinyMCE HTML editor](configuring-plugins-for-TinyMCE-HTML-editor.md#)**  
The TinyMCE HTML editor is a powerful, flexible, and customizable rich text editor. You can configure and extend the editor by using plugins.
-   **[Configure the HTML toolbar](t_ConfigureTheTinyMCEHTMLToolbar.md)**  
Configure which buttons are available on the HTML toolbar.
-   **[Configuring the TinyMCE toolbar via Dictionary attributes](../../workspace/concept/tinymce.md#)**  
 You can configure the TinyMCE HTML editor for a specific table by configuring the dictionary attributes.

**Parent Topic:**[Field types](../../reference-pages/reference/r_FieldTypes.md)

