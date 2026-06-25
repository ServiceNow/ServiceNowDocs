---
title: Export data into Microsoft Excel and update the file
description: Export event task records to an Microsoft Excel file, edit the data offline, and re-import the updated file to apply changes in bulk. Use this task for updating multiple event task records simultaneously outside the ServiceNow interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/export-import-event-tasks-using-excel.html
release: australia
topic_type: task
last_updated: "2025-04-27"
reading_time_minutes: 5
keywords: [BCM, import, export, Excel, event task, bulk update]
breadcrumb: [Importing and exporting event tasks in Microsoft Excel, Structured workflows for Exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Export data into Microsoft Excel and update the file

Export event task records to an Microsoft Excel file, edit the data offline, and re-import the updated file to apply changes in bulk. Use this task for updating multiple event task records simultaneously outside the ServiceNow interface.

## Before you begin

Role required: sn\_bcm.core\_viewer

## About this task

The export and import feature is available from the Event tasks related list on any event record in the Business Continuity Workspace. It includes exercise events and crisis events. The Export and Import actions are grouped together in the related list action bar. Use this procedure when you want to reassign event tasks to different owners in bulk. Use it when you have to update dates and states across many event tasks in a single edit.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending** and select the exercise event.

2.  Open the event record that contains the event tasks you want to update.

3.  Locate the **Event tasks** tab on the event record form.

4.  In the action bar, select **Export to Excel**.

    An export dialog opens. The dialog displays the number and short description of the parent event record for context, and includes a **File name** field pre-populated based on those values.

    \[Omitted image "export-modal.png"\] Alt text: The Export Excel dialog showing the pre-populated file name and Download button.

    The default value is derived from the number and short description. You can change this to any name that identifies the export. A confirmation banner is displayed in the workspace indicating that the download has completed.

5.  Select **Download**.

    The Microsoft Excel file downloads to your machine.

6.  Select and open the downloaded Microsoft Excel sheet.

    All child records matching the current parent are exported \(for example, all Event tasks under the event\). Fields display human-readable values — names instead of sys\_ids and labels instead of internal codes. Drop-down lists are included for fields like **Status**, **Assigned to**, and **Assignment group**.

    \[Omitted image "instructions-sheet.png"\] Alt text: The Instructions sheet in the exported Excel file showing per-column guidance, valid values, and examples.

    The workbook contains three sheets:

    -   Instructions — Describes each column: whether it is mandatory or read-only, valid values, required date formats, and an example. Review this sheet before editing.
    -   Event Details — A read-only reference sheet showing the properties of the parent event. Do not edit this sheet.
    -   Event Tasks — The main data sheet. Row 1 is hidden and contains technical field names. Row 2 displays column labels. Data begins at row 3. Drop-down lists and field validation are pre-configured.
    **Note:** If no event task records exist, the file downloads as an empty template with headers and drop-down lists only. You can use this template to understand the expected format before any data exists.

7.  Open the downloaded Microsoft Excel file and edit the event task records as needed.

    Observe the following constraints when editing:

    -   Edit only the white, unlocked cells. Grey, locked cells are protected read-only fields and any edit to them is ignored at import time.
    -   Use the drop-down lists when they are available. Drop-downs confirm that you enter valid data and that the value can be resolved during import.
    -   Fields with drop-down lists must use a value from the provided list. Entering a value outside the list produces a validation error.
    -   The **Number**, **Short description**, and **Activated plan** fields are read-only for existing records. You cannot modify these values for rows that were included in the export.
    -   The Assigned to drop-down shows all users. Select users in user\_name format \(for example, abel.tuter\). The user\_name is unique while display name might not be. Use the exact format shown in the drop-down list when editing.
    -   The Activated plan drop-down shows only plans linked to the current event record.
    -   The **Additional assignees list** field accepts comma-separated username values. Enter each username exactly as it appears in the drop-down list. The same username cannot be entered more than once in the same cell.
    -   The **Dependencies** field has no drop-down validation. You can enter comma-separated task numbers \(for example, EVNTSK0010001, EVNTSK0010002\).
    -   The values in the **Date** and **Time** fields must use the date format specified in the **Instructions** sheet of the Microsoft Excel file.
    -   The **Short description**, **Activated plan**, **Number**, and **State** fields are required. Only **State** is editable.
    -   WIP and all close states \(Closed Complete, Closed Incomplete, Closed Skipped, Closed Failed, Closed Duplicate\) need the Actual start date. Closed Complete needs the Actual end date. \(Actual end must be after Actual start.\) Import rejects rows that don't meet these criteria.
    -   The **Phase** field is a drop-down. Select a value from the available drop-down.
    -   Do not delete rows. Deleting a row does not delete the corresponding record in ServiceNow. The row is simply skipped and the record remains unchanged.
    -   Do not add new rows to the Event Tasks sheet. New rows are not processed during import and no new records are created.
    -   Do not rearrange columns, rename sheets, or change the file format. The import reads columns by position and expects the sheet name to match the exported tab name. Save the file as ".xlsx" only; ".xls" and ".csv" files are rejected.
    -   Do not remove sheet protection. Sheet protection prevents accidental edits to key fields such as the number. Removing protection does not unlock protected fields at import time; protected field values continue to be ignored or rejected during import.
    Duplicate numbers entered in the file are highlighted in red using conditional formatting. Resolve any duplicates before saving and uploading the file.

    \[Omitted image "event-tasks-data-sheet.png"\] Alt text: The Event tasks data sheet showing protected gray columns, a drop-down arrow on the State column, and a duplicate number highlighted in red.

8.  Save the Microsoft Excel file after completing your edits.


**Parent Topic:**[Importing and exporting event tasks in Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-export-import-feature-event-tasks.md)

**Related topics**  


[Import data from Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/import-data-from-excel.md)

