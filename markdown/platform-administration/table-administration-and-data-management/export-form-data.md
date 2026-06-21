---
title: Export data from a record
description: Export a record to PDF or XML.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/table-administration-and-data-management/export-form-data.html
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2024-08-01"
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

2.  Select the Additional actions menu \(\[Omitted image "Form\_MenuIcon.png"\] Alt text: Additional actions menu.\).

3.  Select an export option.

    -   To export the form data to PDF in portrait mode, select **Export** &gt; **PDF \(Portrait\)**.
    -   To export the form data to PDF in landscape mode, select **Export** &gt; **PDF \(Landscape\)**.
    -   To export all fields in the record to XML, select **Export** &gt; **XML \(This Record\)**.
    When exporting to XML, the system prompts you to save the file, or the browser automatically saves the file to the downloads folder specified in the browser preferences.


## Example

\[Omitted image "ExportFromForm.png"\] Alt text: Export data from form options.

