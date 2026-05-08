---
title: Export data from a record
description: Export a record to PDF or XML.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Export data from a record

Export a record to PDF or XML.

## Before you begin

Role required: none for exporting to PDF. Exporting to XML requires the admin role.

## About this task

When exporting to PDF, any field hidden by UI scripts \(UI policies, UI actions, client scripts\) and any fields visible from the current view are exported. When exporting to XML, all fields are exported, regardless of the view.

A PDF is generated only if the form has been submitted. An unsubmitted form generates an empty page.

## Procedure

1.  Navigate to the record that you want to export.

2.  Select the Additional actions menu \(![Additional actions menu.](../../../common/image/Form_MenuIcon.png)\).

3.  Select an export option.

    **Note:** For export to PDF, when the accessibility property is enabled, users will get a pop up when they export to PDF where they can specify whether to create an accessible PDF or not. For more information, see PDF generation and accessibility.

    -   To export the form data to PDF in portrait mode, select **Export** &gt; **PDF** &gt; **Portrait**, select **Export**.
    -   To export the form data to PDF in landscape mode, select **Export** &gt; **PDF** &gt; **Landscape**, select **Export**.
    -   To export all fields in the record to XML, select **Export** &gt; **XML \(This Record\)**.
    When exporting to XML, the system prompts you to save the file, or the browser automatically saves the file to the downloads folder specified in the browser preferences.


