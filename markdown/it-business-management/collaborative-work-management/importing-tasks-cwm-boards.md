---
title: Task import into CWM Boards using Now Assist
description: Save time and effort by importing tasks or stories from a spreadsheet or document into a Collaborative Work Management Board. Now Assist proposes column mapping so you can bring existing work onto a Board without manually recreating each row.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/importing-tasks-cwm-boards.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-05-29"
reading_time_minutes: 3
keywords: [Import tasks, Now Assist, CWM, bulk import]
breadcrumb: [Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Task import into CWM Boards using Now Assist

Save time and effort by importing tasks or stories from a spreadsheet or document into a Collaborative Work Management Board. Now Assist proposes column mapping so you can bring existing work onto a Board without manually recreating each row.

Teams migrating to CWM from external task tracking tools often have months of structured work already documented in spreadsheets or documents. Recreating that work manually on a CWM Board is time-consuming and error-prone.

The import feature on a CWM Board lets you bring that existing work in from a file. Now Assist scans the file, identifies the tasks, and proposes how each source column maps to a column on your Board. You review and adjust the mapping, preview the tasks before they are created, and confirm to complete the import.

\[Omitted image "cwm-import-upload-file.png"\] Alt text: Upload file step with AI scanning the uploaded file

## Key capabilities

-   **AI-proposed column mapping**

    Now Assist analyzes your file and proposes a target Board column for each source column based on the data it detects. Because the mapping is AI-generated, review each proposal and adjust as needed before proceeding to the preview.

-   **Manual mapping adjustments**

    For any source column, you can select a different target column from the list of available Board columns. Each source column must map to a unique target column.

-   **Custom column creation**

    If a source column does not match any existing Board column, you can add it as a new custom column directly from the mapping step. You can choose the column type while adding.

-   **Reset to AI mapping**

    If you have adjusted mappings manually and need to start over, you can reset the entire mapping to the original Now Assist proposal.

-   **Preview before import**

    Before confirming, review the full list of tasks that will be created on the Board. You can deselect individual rows to exclude them from importing.

-   **Background processing with notification**

    The import runs in the background after you confirm. A workspace notification reports the number of records added to your Board and flags any rows that could not be processed.


## Record types

Each row of your file is imported as a record into CWM. Choose one of these record types in the upload step:

-   CWM task
-   Story

The available target columns in the mapping step depend on the record type that you choose.

## Considerations

-   **File limits**

    Each import accepts a single file with a maximum size of 10 MB, up to 100 rows, and up to 50 columns. Supported file types are .doc, .docx, .pdf, .xls, .xlsx, .png, .jpg, and .jpeg. For Excel files with multiple sheets, only the first sheet is imported.

-   **Excel column header row**

    For Excel files \(.xls or .xlsx\), the first row must contain the column names. The AI always treats the first row as the header row. This requirement does not apply to image files, where the AI reads the content directly without relying on a header row.

-   **Date format**

    Dates in the source file must match the format set in the `glide.sys.date_format` system property on your instance. Dates in any other format are silently left blank after import.

-   **Required mapping**

    The **Short Description** column must be mapped before you can proceed to the preview step.

-   **Access requirements**

    The **Import** button is visible only on Boards where Now Assist for CWM is active. You need the sn\_cwm\_ai.cwm\_ai\_user and lens\_user roles.

-   **Single file per import**

    Each import session accepts one file at a time. Upload a separate file for each set of tasks you want to bring in.

-   **CSV files aren't supported**

    CSV format is not a supported file type. To import tabular task data from a spreadsheet, use an .xls or .xlsx file instead.

-   **Tabular data required**

    The file must contain structured, tabular data with identifiable rows and columns. Files that contain only freeform or narrative text can't be processed, and the import fails if Now Assist can't detect any importable rows.

-   **Import can't be reversed**

    After you confirm the import, records are created in the background. There is no option to undo or reverse a completed import but to delete the imported records from the Board.

-   **Newly imported tasks aren't highlighted on the Board**

    After the import completes, the imported tasks appear on the Board but aren't visually highlighted or grouped as a set. Use filters or sort options to locate them.


## Get started

[Import existing tasks into a CWM Board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/import-tasks-cwm-board.md).

