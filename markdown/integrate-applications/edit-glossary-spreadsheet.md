---
title: Edit glossary spreadsheet
description: Edit the downloaded glossary spreadsheet to add or update glossary terms before importing them back into the Data Catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/edit-glossary-spreadsheet.html
release: australia
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 2
keywords: [glossary spreadsheet edit bulk operations data catalog XLSX Excel]
breadcrumb: [Managing glossary terms, Data Catalog, Workflow Data Fabric]
---

# Edit glossary spreadsheet

Edit the downloaded glossary spreadsheet to add or update glossary terms before importing them back into the Data Catalog.

## Before you begin

Export glossary terms to generate the XLSX template file.

Role required: Data Steward \(df\_data\_steward\)

## About this task

You can obtain the glossary spreadsheet by [exporting existing glossary terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/bulk-export-glossary-terms.md) or downloading an empty template. The exported spreadsheet contains two sheets: Instructions and Export Template \(glossary terms\). The Instructions sheet provides detailed guidance on column formatting, field requirements, and editing rules.

## Procedure

1.  Open the downloaded XLSX file in Microsoft Excel or Apple Numbers.

    **Warning:** If you use Apple Numbers, you must export the file to Excel format \(.xlsx\) before importing it back into the Data Catalog. The import process accepts only XLSX files.

2.  Review the Instructions sheet to understand the column color coding and field requirements.

    -   Gray columns are read-only: **Sys ID**, **IRI**, **Parent Term**
    -   Yellow columns are required for new terms: **Title**
    -   Blue columns are editable: **Short Description**, **Domain**, **Owner**, **Status**, **Tags**
3.  Navigate to the Glossary terms sheet to edit glossary terms.

4.  Edit existing glossary terms or add new terms based on your needs.

    1.  To update an existing term, edit the values in the blue columns for that row.

        Leave a cell empty to leave that field unchanged.

    2.  To add a new term, insert a new row and enter values in the required and editable columns.

        The **Title** field is required for new terms. Leave the Sys ID, IRI, and Parent Term columns empty for new terms.

5.  Format multi-select fields using comma-separated values.

    For fields that accept multiple values \(such as Tags and Domain\), separate each value with a comma. For example: Customer,Finance,Sales

6.  Verify that user account fields contain valid usernames from your ServiceNow instance.

    Fields such as **Owner** must reference existing user accounts. Invalid usernames cause import errors.

7.  Verify that Status values match the options listed in the Status values sheet.

    Valid status values are: draft, in\_review, approved, deprecated, rejected

8.  Save the file in XLSX format.

    **Warning:** Do not change the file structure, sheet names, or column headers. Changes to the template structure cause import failures.


## Result

The edited spreadsheet is ready to import back into the Data Catalog. [Import the glossary terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/bulk-import-glossary-terms.md) to add or update them in the Data Catalog.

**Parent Topic:**[Managing glossary terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/managing-glossary-terms.md)

