---
title: Bulk import glossary terms
description: Import multiple glossary terms at once using an XLSX file to quickly populate your data catalog with business terminology and definitions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/bulk-import-glossary-terms.html
release: australia
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 1
keywords: [glossary terms, bulk import, data catalog, XLSX, import]
breadcrumb: [Managing glossary terms, Data Catalog, Workflow Data Fabric]
---

# Bulk import glossary terms

Import multiple glossary terms at once using an XLSX file to quickly populate your data catalog with business terminology and definitions.

## Before you begin

Role required: Data Steward \(df\_data\_steward\)

## About this task

Before importing, [export glossary terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/bulk-export-glossary-terms.md) to obtain the XLSX template, then [edit the spreadsheet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/edit-glossary-spreadsheet.md) to add or update glossary terms.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Data catalog icon in the left sidebar.

3.  Select the three-dot menu and select **Import glossary terms**.

4.  Select **Browse** and upload the XLSX file with glossary terms.

    Alternatively, drag the XLSX file into the **Import glossary terms** window.\[Omitted image "dc-glossary-import.png"\] Alt text: Import glossary terms

5.  Select **Preview**.

6.  Review all the terms selected for import in the Preview window.

    If there are any warnings or validation failures for the terms, they are tagged as such. To fix the errors, abort the import, make fixes in the file, and initiate the import again.

7.  Select **Import**.

    The import process begins and the system displays the status of the import. If any terms are not imported, you can download a file that includes the list of terms that aren't imported and the reason for failure. \[Omitted image "dc-glossary-import-preview.png"\] Alt text: Preview the changes

8.  Select **Done**.

    The glossary terms are imported in the data catalog.


## Result

After the import completes, the system displays one of the following status values:

-   `COMMITTED` — All rows imported successfully
-   `PARTIAL` — Some rows imported; others failed
-   `FAILED` — No rows imported

**Parent Topic:**[Managing glossary terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-glossary-terms.md)

**Related topics**  


[Glossary import error scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/glossary-import-error-scenarios.md)

