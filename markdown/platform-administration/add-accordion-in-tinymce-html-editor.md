---
title: Configure accordion in TinyMCE HTML editor
description: You can enable the accordion on the TinyMCE HTML editor in both CoreUI and workspaces. When enabled, the accordion button appears on the HTML editor and can be used to expand/collapse content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/add-accordion-in-tinymce-html-editor.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Extended functions in HTML field editor, Configure the HTML toolbar, Configure a field editor for the HTML field, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Configure accordion in TinyMCE HTML editor

You can enable the accordion on the TinyMCE HTML editor in both CoreUI and workspaces. When enabled, the accordion button appears on the HTML editor and can be used to expand/collapse content.

## Before you begin

Role required: admin

## Procedure

1.  Add an accordion to the TinyMCE HTML editor.

    1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

    2.  Locate the system property, **glide.ui.html.editor.toolbar**.

    3.  Add an accordion as an option in the **value** field.

    4.  Select **save**.

2.  Use accordion in TinyMCE HTML editor.

    1.  Verify you have the role necessary to update the record that contains the HTML field.

        For example, any user with a role can create a knowledge article and embed an image in it.

    2.  Open the form that contains the HTML field.

    3.  Select the accordion button on the toolbar.

    4.  Add the accordion summary and body.

        \[Omitted image "TinyMCEV6-accordion-summary.png"\] Alt text: TinyMCE v6.8.3 Accordion summary and body

    5.  Select the accordion to expand and collapse the content.

        \[Omitted image "TinyMCEV6-accordion\_icon.png"\] Alt text: TinyMCE v6.8.3 Accordion icon


