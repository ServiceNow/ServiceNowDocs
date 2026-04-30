---
title: Export data from a list
description: Export a list of records to a variety of file formats.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exporting data, Tables and data, Configure core features, Administer]
---

# Export data from a list

Export a list of records to a variety of file formats.

## Before you begin

Role required: none. Exporting to XML requires the admin role.

## About this task

Note the following important details:

-   Data exported from a list may be different from what a user sees in the list view. This generally happens when a table has ACLs that are dependent on the user's current session. To avoid blocking user activity on the browser, list export is executed from a background thread and doesn't have access to user session data.
-   To export records in an [embedded list](https://www.servicenow.com/docs/access?context=c_EmbeddedLists&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US), export the record containing the list. See [Export data from a record](export-form-data.md).
-   To control how line breaks appear in exported CSV data, use the glide.csv.export.line\_break system property. See [glide.csv.export.line\_break](../../reference-pages/reference/r_AvailableSystemProperties.md#).
-   To remove unwanted HTML tags from list data, see the blog [Rendering HTML in Exported Lists](https://community.servicenow.com/community?id=community_blog&sys_id=1cdc2665dbd0dbc01dcaf3231f961967&view_source=searchResult) by a ServiceNow employee in the ServiceNow Community.
-   The platform provides a default upper limit for data exports. See [Export limits](../concept/c_ExportLimits.md).

## Procedure

1.  Navigate to the list of records that you want to export.

2.  Select and hold \(or right-click\) any column header in the list.

3.  Select an export option.

    **Note:** For export to PDF, when the accessibility property is enabled, users will get a pop up when they export to PDF where they can specify whether to create an accessible PDF or not. For more information, see [PDF generation and accessibility](https://www.servicenow.com/docs/access?context=pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   To export the list to Excel, select **Export** &gt; **Excel \(.xlsx\)**.
    -   To export the list to CSV, select **Export** &gt; **CSV**.
    -   To export the list to XML, select **Export** &gt; **XML**
    -   To export the list to JSON, select **Export** &gt; **JSON**.
    -   To export the list to PDF in portrait mode, select **Export** &gt; **PDF** &gt; **Portrait** &gt; **Export**
    -   To export the list to PDF in landscape mode, select **Export** &gt; **PDF** &gt; **Landscape** &gt; **Export**
    -   To export the list and the associated form for each record in portrait mode, select **Export** &gt; **PDF** &gt; **Detailed Portrait****Export**.
    -   To export the list and the associated form for each record in landscape mode, select **Export** &gt; **PDF** &gt; **Details Landscape** &gt; **Export**.
    -   To export the list to a file using an export set, select **Export** &gt; **Export Set**.
    -   To export the list to a Google spreadsheet, select **Export** &gt; **Google Sheets**.
    For details on using export sets, see [Export sets](https://www.servicenow.com/docs/access?context=c_ExportSets&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

4.  When the export completes, select **Download**.


