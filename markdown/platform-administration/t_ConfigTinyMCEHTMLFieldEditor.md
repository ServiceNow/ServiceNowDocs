---
title: Configure a field editor for the HTML field
description: Configure HTML fields to use TinyMCE or the legacy htmlArea editor. The TinyMCE editor provides better stability and more editing functions than the legacy htmlArea editor.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
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


