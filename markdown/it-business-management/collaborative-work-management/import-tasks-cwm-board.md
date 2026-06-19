---
title: Import existing tasks into a CWM Board
description: Bring existing work from a spreadsheet or document into a CWM Board. Column mapping is generated automatically. Review the mapping, preview the result, and confirm the import.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/import-tasks-cwm-board.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 2
breadcrumb: [Import tasks using Now Assist, Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Import existing tasks into a CWM Board

Bring existing work from a spreadsheet or document into a CWM Board. Column mapping is generated automatically. Review the mapping, preview the result, and confirm the import.

## Before you begin

-   Prepare a source file that meets these conditions:
    -   One of these file types: .doc, .docx, .pdf, .xls, .xlsx, .png, .jpg, or .jpeg
    -   10 MB or less
    -   A maximum of 100 rows and 50 columns
    -   Includes a column that contains a task title or name, used as the short description during import.
    -   For Excel files \(.xls or .xlsx\): place the column names in the first row. The AI always treats the first row as the header row.
    -   If your file contains dates, the dates must match the format set in the `glide.sys.date_format` system property. Dates in other formats are silently left blank after import.
-   Verify that Now Assist for CWM is active on your instance.
-   Role required: sn\_cwm\_ai.cwm\_ai\_user or lens\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a Space, select a Board to import tasks into.

3.  From the Board header, select **Import**.

    \[Omitted image "cwm-import-board-header.png"\] Alt text: Board header showing the Import button.

    The import wizard opens with three steps: **Upload file**, **Field mapping**, and **Preview board**.

4.  From the **Work item type** list, select the type of record to import tasks as.

    You can choose **CWM Tasks** or **Stories**. The source to CWM column mapping in the next step depends on this choice.

5.  Upload your file by dragging it onto the upload area or by selecting **Select file**.

    The file is processed and the wizard advances to the **Field mapping** step automatically.

    \[Omitted image "cwm-import-upload-file.png"\] Alt text: Upload file step with AI scanning the uploaded file.

6.  On the **Field mapping** step, review the proposed mapping.

    For each source column, a target column on your Board is suggested. Adjust the mapping in any of these ways:

    -   To map a source column to a different existing column, select a value from the target list.
    -   To add a new custom column on your Board, select **Add as new custom column**, and then choose the column type.
    -   To return to the original column mapping, select **Reset to Now Assist mapping**.
    The Short description column is required. Each source column must map to a different target column.

    \[Omitted image "cwm-import-ai-column-mapping.png"\] Alt text: Field mapping step showing AI column mapping recommendation.

7.  Select **Preview tasks**.

8.  On the **Preview board** step, review the tasks to import.

    Select all tasks at once or select the tasks to import.

    \[Omitted image "cwm-import-preview-tasks.png"\] Alt text: Preview board step showing tasks to be imported.

9.  Select **Confirm and Import**.

10. If you added any custom columns during the import, enable their display on the Board using the Personalize side panel and save the view.

    For more information on personalizing columns, see [Personalize List, Gantt and Kanban display for CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/personalize-cwm-board-views.md).


## Result

The wizard closes and the import runs in the background. A workspace notification confirms the outcome:

-   If all tasks import successfully, the notification shows the count of records added to your Board.
-   If some tasks import, the notification shows the count of records imported and indicates that some items were not processed.

## What to do next

Open the Board to verify the imported records. Edit individual records from the side panel or by inline editing in the grid.

