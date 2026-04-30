---
title: Export to PDF
description: Export an individual record or list of records into a PDF format that supports accessibility. When this feature is enabled, accessibility tags are available in the PDF tag tree to help users who rely on-screen readers to navigate, understand, and interact with the generated PDF documents.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [PDF generation and accessibility, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Export to PDF

Export an individual record or list of records into a PDF format that supports accessibility. When this feature is enabled, accessibility tags are available in the PDF tag tree to help users who rely on-screen readers to navigate, understand, and interact with the generated PDF documents.

## Export to PDF for list of records

Export a list of records in a variety of formats. The **Export** option is available in the column heading context menu in List v2. In List v3, it’s available in the list title menu.

PDF export orientation includes:

-   Portrait
-   Landscape
-   Detailed Portrait \(exports the list and the associated form for each record\).
-   Detailed Landscape \(exports the list and the associated form for each record\).

When the accessibility property is enabled, you get a pop-up when they export to PDF where they can specify whether to create an accessible PDF or not.

![Check box to enable accessible PDF](../image/accessible-pdf.png "Export to PDF")

To enable accessibility, select the **Accessible PDF** check box.

**Note:** Adding accessibility tags to a PDF increases the file size.

To export a PDF list, see [Export data from a list](https://www.servicenow.com/docs/access?context=export-list-data&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Export to PDF for a single record

To export an individual record from a form, select and hold \(or right-click\) a form header bar and select the export type.

PDF export orientations include:

-   Portrait
-   Landscape

When the accessibility property is enabled, you get a pop-up when they export to PDF where they can specify whether to create an accessible PDF or not.

To enable accessibility, select the **Accessible PDF** check box.

**Note:** Adding accessibility tags to a PDF increases the file size.

To generate a single PDF record, see [Export data from a record](https://www.servicenow.com/docs/access?context=export-form-data&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[PDF generation and accessibility](pdf-generation-accessibility.md)

