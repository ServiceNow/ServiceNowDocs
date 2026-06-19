---
title: Importing and exporting event tasks in Microsoft Excel
description: Use Export to download event task records into a structured Microsoft Excel file — complete with dropdowns, instructions, and field protection. Edit records offline, then use Import to upload the updated file and apply bulk changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/using-export-import-feature-event-tasks.html
release: australia
topic_type: concept
last_updated: "2025-04-27"
reading_time_minutes: 7
keywords: [import, export, Excel, event task, Record Transform Engine]
breadcrumb: [Structured workflows for Exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Importing and exporting event tasks in Microsoft Excel

Use Export to download event task records into a structured Microsoft Excel file — complete with dropdowns, instructions, and field protection. Edit records offline, then use Import to upload the updated file and apply bulk changes.

## Benefits of using import and export functionality

Starting with the Australia release of the BCM application, import and export of event tasks is supported. Import and export is useful when you want to update many records at once. For example, reassigning 50 event tasks to different owners or bulk-updating dates and statuses. You can bulk-update fields like **Assigned To**, **Status**, and **Dates** or download data to review offline.

You can download an empty template to see the expected format before any data exists. Import only  updates  existing records matched by the **Number** field— it does not create or delete records, or modify protected fields like **Number**, **Short description**, and **Activated plan**.

The feature consists of two independent systems. The export layer uses the Microsoft Excel JS library on the front-end to generate structured files; the import layer uses the Record Transform Engine \(RTE\), which processes display values only.

Because the two layers are decoupled, you can use either independently. The Microsoft Excel JS library runs only in the browser. Export performance scales with the user's available memory and CPU, and the Max export rows limit is enforced for this reason.

See the following points for reference:

-   Date format: YYYY-MM-DD HH:MM:SS
-   Dependencies: comma-separated EVNTSK numbers
-   State rules: WIP and all close states need Actual start, Closed Complete needs Actual end
-   Re-import: delete successful rows first, then re-upload

## Microsoft Excel sheet structure

The exported file follows a fixed row structure. It shows a single-column approach — one column per field with display values only.

The visible column shows the human-readable value, typically a dot-walked field such as user\_name. The dot-walk applies only to specifically configured fields.

The exported workbook contains three sheets:

1.  Instructions sheet — describes each column: whether it is mandatory or read-only, valid values, date format requirements for Actual Start and Actual End, and an example value. Review this sheet before editing.
2.  Event details sheet — a read-only reference sheet showing the parent event record properties. Not processed during import.
3.  Event task — the main data sheet, with one row per event task record beginning at Row 3. Records are sorted by number by default.

The following table describes the column types in the Event task data sheet and how each one behaves while you edit the file.

|Column type|Appearance|Editable|
|-----------|----------|--------|
|Protected \(for example Number, Short description\)|Grey, locked|No|
|Drop-down \(for example, State, Assigned to, Assignment group\)|Drop-down arrow|Yes - select from list|
|Free text \(for example, Date and Time fields\)|Plain white|Yes - type value|

## Drop-down and record-limit behavior

Drop-downs are populated using reference qualifiers defined in the system. When the number of records in a reference field exceeds the configured maximum, the drop-down is suppressed and the field displays plain text with no validation.

|UI component|Description|
|------------|-----------|
|Max export rows|Maximum number of records included in an export. Defaults to 10,000. Processing is bounded by the user's machine.|
|Max drop-down records|Threshold beyond which drop-downs are replaced with plain text and field validation is removed. Defaults to 10,000.|

## Protected fields and uniqueness enforcement

The **Number** field is protected by default. Duplicate numbers are flagged with a red highlight using conditional formatting but cannot be blocked in Microsoft Excel — they are rejected at import time.

## GlideList field handling in the Record Transform Engine

The Microsoft Excel JS library does not support multi-select drop-downs. GlideList fields such as Additional Assignees List render as plain text cells. Validation is still applied — the system verifies that each comma-separated value exists in the referenced table and rejects invalid records. The same value cannot appear more than once in the same cell.

The following table describes the import progress states.

<table id="table_k5h_3nr_cjc"><thead><tr><th>

State

</th><th>

Meaning

</th></tr></thead><tbody><tr><td>

Queued

</td><td>

Import is waiting to be processed.

</td></tr><tr><td>

Processing N rows

</td><td>

Records are actively being updated.

</td></tr><tr><td>

Successfully imported N records

</td><td>

All rows were processed without errors.

</td></tr><tr><td>

Import has failed for few records

</td><td>

Some rows had errors. Review the Import Log related list for details on which rows were rejected and the reason for each failure.

</td></tr><tr><td>

Error

</td><td>

Import failed entirely. Review system logs and the Import Log related list.

</td></tr></tbody>
</table>While an import is running, the **View import progress** button replaces the **Import** button in the related list action bar. After the tracker shows a completed or error state, the **Import** button is available again. Only one import can run at a time per event record.

## Duplicate display name handling

The Record Transform Engine does not support resolution of duplicate display names. If two users share the same display name, the system cannot guarantee the correct record is matched during import. Configure the dot-walk field to use a unique identifier such as user\_name or email for affected reference fields.

|UI Component|Description|
|------------|-----------|
|Display Name \(default\)|Default identifier for reference field drop-downs. Duplicate display names may produce incorrect matches.|
|user\_name|Recommended unique identifier for Assigned To and Additional Assignees List fields.|
|email|Alternative unique identifier configurable via the dot-walk field setting.|

## Import attachment flow and progress tracking

Import updates only existing records matched by the Number field. It does not create or delete records, or modify protected fields such as Number, Short description, and Activated plan, even if sheet protection is manually removed before upload. Rows omitted from the file are not processed; the corresponding records in ServiceNow remain unchanged.

When a user initiates an import, a modal opens for file selection. Only .xlsx files are accepted — .xls and .csv files are rejected. The uploaded file attaches to the event record and the import queue starts automatically on save. The progress tracker status is displayed.

The attachment field is cleared automatically after import completes, whether it succeeds or fails, so you can re-upload a corrected file without manual cleanup. Import status is displayed inline via a progress tracker. Errors and transaction history are surfaced via the Import log and Transaction history related lists on the event page.

The system reads the file, matches each row to an existing record by the Number field, and updates only changed fields. Reference fields such as Assigned To are resolved automatically — display values are converted back to the correct internal records.

## Limitations

The following table summarizes the limitations to consider when you use the import and export feature for event task.

|Limitation|Details|
|----------|-------|
|Update only|Import matches records by Number. Rows without a matching number are skipped. No new records are created.|
|.xlsx only|Only .xlsx files are accepted. Other formats are rejected.|
|Single file at a time|Only one import can run at a time per parent event record.|
|Column structure|The uploaded file must match the exported column structure exactly. Renaming sheets, rearranging columns, or changing the file format causes the import to fail.|
|Drop-down overflow|Fields exceeding the drop-down record limit are exported as plain text and must be entered manually in the exact expected format.|
|Protected fields|Protected fields like **Number**, **Short description**, and **Activated plan** are locked in Microsoft Excel. Even if sheet protection is removed, the import ignores or rejects edits to those fields.|

## Import and export integration reference

For information on Import and export integration reference, see [Import and export integration reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/installed-with-bcm.md).

-   **[Export data into Microsoft Excel and update the file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/export-import-event-tasks-using-excel.md)**  
Export event task records to an Microsoft Excel file, edit the data offline, and re-import the updated file to apply changes in bulk. Use this task for updating multiple event task records simultaneously outside the ServiceNow interface.
-   **[Import data from Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/import-data-from-excel.md)**  
Import data such as event task records from Microsoft Excel to apply changes in bulk. Use this task for updating multiple event task records simultaneously outside the ServiceNow interface.

**Parent Topic:**[Structured workflows for Exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/performing-tasks-to-manage-exercise-events.md)

