---
title: Bulk export glossary terms
description: Download existing glossary terms to an XLSX file for offline review and editing, or download an empty template to create new glossary terms with properly formatted fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/bulk-export-glossary-terms.html
release: australia
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 1
keywords: [glossary export bulk operations data catalog XLSX]
breadcrumb: [Managing glossary terms, Data Catalog, Workflow Data Fabric]
---

# Bulk export glossary terms

Download existing glossary terms to an XLSX file for offline review and editing, or download an empty template to create new glossary terms with properly formatted fields.

## Before you begin

Role required: Data Steward \(df\_data\_steward\)

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the **Data Catalog** icon.

3.  Download a glossary terms template or export existing terms:

    1.  To download an empty template for creating new glossary terms:

        1.  Select the three-dot menu and select **Import glossary terms**.
        2.  Select **Download** to download the empty XLSX template. \[Omitted image "dc-glossary-export-template.png"\] Alt text: Export the template
        A blank glossary terms template is downloaded in XLSX format with properly formatted fields.

    2.  To export existing glossary terms for review or editing:

        1.  Select the three-dot menu and select **Bulk edit glossary terms**.
        2.  Select glossary terms to export. Use the **Add all** button to select all terms, or select **Add** next to each term to select them individually. Use the filters to narrow the list. You can select up to 2000 glossary terms.
        3.  Select **Done** to proceed to the summary screen.
        4.  Review the list of glossary terms. If needed, select **Add more** to return to the previous screen and adjust your selection.
        5.  Select **Export** to download the glossary terms. \[Omitted image "dc-glossary-export-existing.png"\] Alt text: Export existing terms
        The glossary terms are exported in an XLSX file.


## Result

The downloaded XLSX file has a set structure with all the sheets you need to add and edit the business glossary. Before editing the file, read the instructions in the Overview tab carefully. See [Edit glossary spreadsheet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/edit-glossary-spreadsheet.md) for detailed guidance on editing the spreadsheet.

**Parent Topic:**[Managing glossary terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-glossary-terms.md)

