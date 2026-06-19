---
title: Import data from Microsoft Excel
description: Import data such as event task records from Microsoft Excel to apply changes in bulk. Use this task for updating multiple event task records simultaneously outside the ServiceNow interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/import-data-from-excel.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 3
breadcrumb: [Importing and exporting event tasks in Microsoft Excel, Structured workflows for Exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Import data from Microsoft Excel

Import data such as event task records from Microsoft Excel to apply changes in bulk. Use this task for updating multiple event task records simultaneously outside the ServiceNow interface.

## Before you begin

Role required: sn\_bcm.core\_viewer

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending** and select the parent record \(the same one you exported from\).

2.  Open the same event record from where you had exported the Microsoft Excel sheet.

    You can attach your edited  .xlsx  file to the same record as shown in the next steps.

3.  Select **Import from Excel** from the **Event tasks** related list action bar.

    A modal opens for file selection where you can attach the file.

4.  Select your saved Microsoft Excel file in the import modal using the file picker.

    The modal shows the **Attach file** option where you can upload the saved Microsoft Excel file.

    \[Omitted image "import-excel-dialog.png"\] Alt text: Import excel modal.

5.  Select **Save** in the modal.

    The import queue starts automatically. The progress tracker status 'Import queued, waiting to process' is displayed and the import runs in the background.

    \[Omitted image "import-progress-tracker.png"\] Alt text: The Event tasks related-list action bar showing the View import progress button and the inline status indicator while an import is running.

    The attachment field is cleared automatically after the import completes, whether it succeeds or fails, so you can re-upload and re-import a corrected file without manual cleanup.

    **Important:** Only rows that were part of the original export are updated. Adding new rows to the file is not supported; new rows are not processed during import. You cannot start a new import while one is already in progress.

6.  Monitor and validate that the event queue is triggered and in-progress.

    The example shows that the event queue is being processed.

    \[Omitted image "import-progress-events.png"\] Alt text: Event queue.

7.  Monitor the import progress using the inline progress tracker on the event record.

    Import processing occurs in batches. Processing time depends on the number of records in the file. For information on the progress states shown in the tracker, see the Import progress states table in [Importing and exporting event tasks in Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-export-import-feature-event-tasks.md).

    The system reads the Microsoft Excel file, matches each row to an existing record using the **Number** field, and updates only the changed fields. Reference fields such as **Assigned to** are resolved automatically — the system converts display values back to the correct internal records.

8.  Verify that data is populated in the import table and state is processed.

    Example shows that data is populated in the import table and state is processed.

    \[Omitted image "data-popu-in-import-table-st-processed.png"\] Alt text: Data is populated in the import table and state is processed.

9.  Confirm that the event task shows the additional configuration details.

    Example shows an event task the additional assignee details.

    \[Omitted image "event-task-addi-assignee-list.png"\] Alt text: Additional assignee details.

10. Review the error details on the event record, if the progress tracker shows that some records failed.

    The progress bar in the example shows that some records failed the import.

    \[Omitted image "progress-tracker-import-failed-few-records.png"\] Alt text: Few records that failed the import.

    You can scroll to the Import Log related list to see which rows were rejected and the reason for each failure. The Transaction History related list shows the full processing history for the import run.

11. Correct the affected rows in the file.

    The full re-import steps are in the Instructions sheet of the Excel file: Unlock the data sheet, delete successful rows, keep only failed rows, and re-import. Save the file and repeat the import steps to reprocess the corrected data.


**Parent Topic:**[Importing and exporting event tasks in Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-export-import-feature-event-tasks.md)

