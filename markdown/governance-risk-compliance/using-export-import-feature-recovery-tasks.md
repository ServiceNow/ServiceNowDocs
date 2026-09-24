---
title: Import and export recovery tasks
description: Export recovery tasks to a Microsoft Excel file, edit offline, and import the file to create, or update multiple tasks at once.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/using-export-import-feature-recovery-tasks.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 18
keywords: [BCM, import, export, Excel, recovery task]
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Import and export recovery tasks

Export recovery tasks to a Microsoft Excel file, edit offline, and import the file to create, or update multiple tasks at once.

The **Export to Excel** and **Import from Excel** actions are available in the **Recovery tasks** related list on a business continuity plan. Use these actions to create or update many recovery tasks in bulk outside the ServiceNow interface.

## Import architecture and data flow

When importing an Excel file, recovery task data flows through multiple processing stages before records are created or updated in the final recovery tasks table.

Import data flow:

1.  Upload: Attach the Excel file using the **Import from Excel** action. The file is validated for structure \(sheet names, column order, file format\).
2.  Staging: Valid file contents are loaded into a staging table \(`sn_bcp_import_staging`\) with one row per recovery task. The staging table temporarily holds the data while awaiting processing. Records remain in the staging table for up to 30 days or until manually purged.
3.  Post-processing: A scheduled import job \(running every 60 seconds\) retrieves pending staged records and processes them in batches of 500. See the Post-processing workflow section for details on how the system validates, transforms, and applies the data.
4.  Final table: After successful post-processing, records are created or updated in the recovery tasks table \(`sn_bcp_recovery_task`\), and staging records are marked as processed.

Staging table access and permissions The staging table is restricted by the following access control rules:

-   Read access is limited to users with one of these roles: sn\_bcp.plan\_owner, sn\_bcp.plan\_manager, sn\_bcp.plan\_admin, or admin.
-   Write access \(to create staged rows\) requires the sn\_bcm.core\_user role or higher.
-   The staging table schema mirrors the recovery task export schema, with additional metadata fields for import tracking \(import run ID, status, error messages\).

To monitor staged records in the UI, navigate to **Business Continuity Workspace** &gt; **Administration** &gt; **Import Staging**. This view shows pending imports grouped by plan and import run.

## Exported workbook

The exported workbook contains 24 columns of recovery task data across three sheets:

-   Instructions sheet: Shows each column, including whether it's mandatory or read-only, the valid values for choice and reference fields, and an example. Review this sheet before you edit the file, especially the valid values for reference fields such as Owner, Configuration item, and Related plan.
-   Plan details sheet: A read-only reference sheet that shows the properties of the parent plan. Do not edit this sheet.
-   Recovery task sheet: The data sheet to edit, with one row per recovery task.

This table shows how Microsoft Excel columns map to recovery task fields and their validation rules. The **Task ID** and **Short description** columns are mandatory. Dependencies are exported as comma-separated task IDs because the short description is not unique.

|Column|Description|
|------|-----------|
|Task ID|Unique identifier for the task, unique within the plan but not necessarily unique across other plans. Read-only for existing tasks. Use a temporary N-prefixed identifier to create a task. See the Import processing section on this page.|
|Short description|Short description of the task.|
|Tag|Tag for the task, used for filtering and reporting.|
|Dependencies|Comma-separated task IDs for the predecessor tasks that must complete before this task can start.|
|Configuration item|Configuration item associated with the task.|
|Phase|Phase for the task, used for filtering and reporting.|
|Asset recovery level|Asset recovery level that this task achieves on completion.|
|Include task in|Whether the task is included in actual events, exercises, or both.|
|Do not include this task in time calculation|Whether the task is excluded from time calculations.|
|Task classification|Whether the task is manual or automated.|
|Automated flow|Subflow that runs when the task executes. Applies only when **Task classification** is **Automated**.|
|Tag assets|Plan assets that this task applies to for recovery tracking.|
|Asset scope|Specific plan assets in scope for the task. Applies only when **Tag assets** is **Specific assets**.|
|Planned duration|Planned duration for the task.|
|Activate a related plan|Whether the task activates a related plan on completion.|
|Related plan|Related plan to activate. Applies only when **Activate a related plan** is **true**.|
|Owner|Owner of the task.|
|Assignment group|Group that owns the task.|
|Additional assignees|Additional users assigned to the task.|
|Recovery team|Recovery team assigned to the task.|
|Documentation|Documentation section of the plan that this task links to.|
|Loss scenario|Loss scenario associated with the task.|
|Recovery strategy|Recovery strategy associated with the task.|
|Description|Detailed description of the task.|

## Field handling

Several columns on the **Recovery task** sheet have dependencies on other columns, or behave differently on the form than they do at import time.

The import validates each row against these field-handling rules:

|Column|Rule|
|------|----|
|Owner|Displays a drop-down list of all users in the system. If the user table contains more than 10,000 records, the drop-down list is disabled and the field becomes a plain text field. In this case, enter the exact user name as it's defined in the system.|
|Additional assignees|Enter comma-separated user names. The import validates entries against the user name field, not the display name. If two users share the same display name, the import always selects the first matching record, which can cause an incorrect assignment. Enter exact user names to avoid ambiguity. If you enter a user that does not exist, the import returns an error.|
|Dependencies|Enter comma-separated task IDs, including the temporary N-prefixed IDs of tasks that this import creates. See the Import processing section on this page.|
|Configuration item|Enter the configuration item name exactly as it's defined in the system. If more than one configuration item has the same name, the import logs a warning on the plan's **Import log** tab and continues.|
|Task classification and Activate a related plan|These fields are mutually exclusive. An automated task cannot also activate a related plan. On the form, setting **Task classification** to **Automated** hides the **Recovery team** and **Additional assignees** fields, but the import does not automatically clear those fields. If you populate **Recovery team** or **Additional assignees** for an automated task, the import may fail during validation or return a business rule error.|
|Related plan|Applies only when **Activate a related plan** is **true**. The chosen plan must already be added as a related plan on the current plan, and cannot create a cyclic plan dependency. Combined upstream and downstream plan nesting cannot exceed 10 levels. On the form, setting **Activate a related plan** to **true** hides the **Assignment group**, **Loss scenario**, **Documentation**, and **Recovery strategy** fields, but the import does not clear or enforce those fields.|
|Documentation, Loss scenario, and Recovery strategy|**Documentation** and **Recovery strategy** are mutually exclusive. Set **Loss scenario** before **Recovery strategy**. The **Recovery strategy** choices are limited to strategies that belong to the selected loss scenario.|
|Tag assets and Asset scope|**Asset scope** applies only when **Tag assets** is **Specific assets**. Setting **Tag assets** to **All assets from loss scenario** or **All assets from recovery strategy** requires the matching **Loss scenario** or **Recovery strategy** column to be populated on the same row. The import fails a row that's missing this required value.|
|Planned duration|Free text that combines one or more units: days, hours, minutes, or seconds. Use the full unit name with standard spacing, and do not use abbreviations, for example, `2 Days 4 Hours`, `1 Day 30 Minutes`, `5 Days`, `12 Hours`, or `30 Minutes`.|

For reference fields that match records by display name, such as **Configuration item**, **Documentation**, and **Related plan**, more than one record can share the same display name. If more than one **Configuration item** record uses the same name, the import matches the first record found and logs a warning on the **Import log** tab. If more than one **Documentation** section on the plan uses the same name, the import links the first matching section, which might not be the one you intended. If more than one **Related plan** record uses the same name, the import might select the incorrect plan. The row fails if the selected plan would exceed the plan-nesting depth limit described in this table. To avoid this issue, use unique display names for these records, or review the **Import log** tab and manually correct any mismatched records after import.

**Tip:** The **Additional assignees** and **Dependencies** columns are glide list fields that accept multiple comma-separated values. Microsoft Excel does not support multi-select drop-down lists, so the import validates each value only at import time, not while you edit the file. Review the Instructions sheet in the exported file for the valid values for these fields before you import.

## Import validation rules and error reference

The import validates each row of data against a comprehensive set of rules before records are created or updated. Validation errors prevent rows from being processed until the issues are resolved.

Common validation errors and remedies:

|Error Message|Cause|How to Fix|
|-------------|-----|----------|
|Mandatory field missing: Task ID|The Task ID column is empty for a new or existing task.|For new tasks, enter a temporary N-prefixed identifier \(e.g., N1, N2\). For updates, keep the numeric task ID from the export.|
|Mandatory field missing: Short description|The Short description column is empty.|Enter a brief description for the task. This field is required for all rows.|
|Invalid date format in \[field name\]|A date field contains an unrecognized format \(if applicable to your tasks\).|Use standard date formatting consistent with your system locale, or refer to field-specific format rules in the Field handling section.|
|User not found: \[user name\]|The Owner, Additional assignees, or Recovery team field references a user that does not exist in the system.|Verify the exact user name as defined in the system. Use the Instructions sheet in the export to validate user names.|
|Configuration item not found or ambiguous: \[item name\]|The Configuration item field value does not exist or matches multiple items.|Check the exact name of the configuration item in the system. If multiple items share the same name, use a unique identifier or partial name to disambiguate.|
|Invalid dependency: Task ID \[ID\] does not exist|The Dependencies field references a task ID that does not exist \(and is not a valid N-prefixed identifier in this import\).|Verify the task ID exists on the plan, or check that N-prefixed references are spelled correctly \(e.g., N1, not N01\).|
|Mutually exclusive fields populated: Task classification and Activate related plan|Both Task classification \(set to Automated\) and Activate a related plan are populated on the same row.|An automated task cannot also activate a related plan. Remove one of these values.|
|Plan nesting depth exceeded|The Related plan field would create a nested plan structure exceeding 10 levels deep.|Reduce plan nesting depth or choose a different related plan that does not violate the nesting limit.|
|Business rule error: \[rule description\]|A business rule defined for recovery tasks has been violated \(e.g., field dependency not met\).|Review the error message for details. Common causes include missing required fields when certain other fields are set. See the Field handling section for field dependency rules.|

Date and duration format rules: The **Planned duration** field requires a specific format. Use full unit names with spacing \(no abbreviations\): `2 Days 4 Hours`, `1 Day 30 Minutes`, `5 Days`, `12 Hours`, or `30 Minutes`. If you receive an invalid format error, verify spacing and unit names match these examples exactly.

Re-importing after fixing errors: After resolving validation errors in your Excel file, save the changes, then re-upload the file using **Import from Excel**. Each import run is independent; the system creates a new import log for the re-import.

## Import processing

When you import the file, the records are staged in a recovery-task import table. A scheduled job retrieves pending imports every 60 seconds and processes all staged records into recovery tasks in a single run, in batches of 500.

Each row either updates an existing recovery task or creates one, based on the **Task ID** column

-   To update an existing task, keep its numeric task ID. Do not change this value, or the update fails.
-   To create a task, enter a temporary N-prefixed identifier, for example, `N1` or `N2`. The system assigns the task a real task ID after import. Reference an N-prefixed identifier in the **Dependencies** column of any row in the file, including another new row, to set up dependencies between tasks that do not exist yet. For example, task `N5` can depend on existing tasks 1, 2, and 3. Task `N7` can depend on a combination of new and existing tasks, such as `N5`, `N6`, 1, and 2. Task `N6` can depend on task `N7`, creating a dependency chain between new tasks. The import job resolves all dependencies during processing, regardless of the row order in the file.

## Post-processing: From staging to final tasks

After the import file is uploaded and staged, a background post-processing job executes automatically every 60 seconds to transform staged data into recovery tasks. Understanding this workflow helps you troubleshoot import issues and resolve dependencies correctly.

Post-processing workflow stages:

1.  Validation stage: The system validates each staged row against field-handling rules \(see the Field handling section\) and validation rules \(see Validation errors reference\). Rows with validation errors are flagged and not processed further.
2.  N-prefixed ID resolution stage: The system processes all rows in the batch for temporary N-prefixed identifiers \(N1, N2, N3, etc.\). It creates a mapping of these temporary IDs to their permanent task IDs. This happens before any rows are inserted, ensuring dependencies between new tasks can be resolved correctly.
3.  Dependency resolution stage: The system processes each row's Dependencies field, resolving all referenced task IDs. For dependencies on N-prefixed IDs, the system substitutes the temporary ID with the permanent task ID established in the previous stage. Dependencies that reference non-existent task IDs are silently skipped \(the task is still created, but without that dependency\).
4.  Insertion/update stage: The system inserts new rows or updates existing rows in the recovery tasks table. Dependencies, field values, and all other data are applied during this stage.
5.  Post-processing completion stage: Staged records are marked as processed, and an import log entry is created summarizing the batch \(rows inserted, updated, skipped, and errors\).

Timeline and visibility: Post-processing typically completes within 1-2 seconds per batch of 500 rows. Use **View import progress** in the plan header to monitor the status. Results appear in the **Import log** tab immediately after processing completes.

Cyclic dependency handling: If a row's dependencies would create a cycle \(Task A -&gt; Task B -&gt; Task A\), the post-processing job detects this and logs an error. The row is not inserted, and you must resolve the cycle manually before re-importing.

Plan-nesting depth validation: When a row sets **Activate a related plan** to **true**, the post-processing job verifies that the resulting plan nesting does not exceed 10 levels combined upstream and downstream. If the limit would be exceeded, the row fails and is logged in the Import log with an error.

## Checking import results

After starting an import, select **View import progress** in the plan header to reopen the progress tracker. When the import finishes, review the following for traceability of the import run:

-   **Import log** tab: Review warnings and errors about specific rows, for example, a Configuration item value that matches more than one configuration item.
-   **Transform history** tab: View a summary of the most recent import run, including rows that were inserted, updated, or skipped, and any row-level errors.

Transform history and Import log field reference After import completes, two tabs appear on the plan record to show detailed results. Use these tabs to verify successful imports and troubleshoot failures.

|Field Name|Type|Description|
|----------|----|-----------|
|Import Run|Reference|Link to the import set run that generated this transform history record. Groups results by individual import batch.|
|Plan|Reference|The business continuity plan that the tasks belong to \(for context and filtering\).|
|Status|Choice|Status of the row in this batch. Values: Inserted \(new task created\), Updated \(existing task modified\), Skipped \(row not processed due to error\), Error \(row processing failed\).|
|Rows Inserted|Integer|Count of new tasks created from this import batch.|
|Rows Updated|Integer|Count of existing tasks updated from this import batch.|
|Rows Skipped|Integer|Count of rows that were not processed \(usually due to validation errors or partial dependency failures\).|
|Rows with Errors|Integer|Count of rows that failed validation or business rule checks and were not inserted/updated.|
|Started|Date/Time|When the post-processing job began processing this batch.|
|Completed|Date/Time|When the post-processing job finished processing this batch.|

|Field Name|Type|Description|
|----------|----|-----------|
|Import Run|Reference|Link to the import set run that generated this log entry \(same as Transform history for the same batch\).|
|Row Number|Integer|The row number in the Excel file where this issue occurred \(useful for locating the problem in your source file\).|
|Message Type|Choice|Type of message: Warning \(issue resolved but worth noting\) or Error \(row could not be processed\).|
|Message|String|Detailed description of the warning or error. Examples: "Configuration item matched multiple records, selected first", "Task dependency N5 not found", "Mandatory field missing: Short description".|
|Task ID|String|The Task ID from the Excel row \(or N-prefixed identifier if the task is new\). Helps you locate which row in your file caused the issue.|
|Created|Date/Time|When this log entry was created \(timestamp of the import batch execution\).|

Using these tabs to troubleshoot:

-   Transform history tab: Review summary counts to confirm the import ran as expected. If "Rows with Errors" is greater than zero, check the Import log tab for specific error messages.
-   Import log tab: Filter by Message Type = **Error** to see all rows that failed. Use the Row Number and Task ID columns to locate the problematic rows in your original Excel file. Fix the issues and re-import.
-   Partial dependencies: If a row shows Status = **Updated** but has a warning like "Task dependency N5 not found", the task was created or updated. One or more dependencies were missing and skipped. Review the row and manually add the missing dependencies after import.

Access and retention: The Transform history and Import log tabs are visible only to users with roles sn\_bcp.plan\_owner, sn\_bcp.plan\_manager, sn\_bcp.plan\_admin, or admin. Records are retained for 90 days after import completion, then automatically purged.

**Important:** If a row's **Dependencies** value references a task ID that does not exist, including an invalid N-prefixed identifier, the import silently skips that dependency without affecting the rest of the row. The task is still created or updated with all other valid fields and valid dependencies. Review the **Import log** and **Transform history** tabs to identify rows with partially applied dependencies, and manually add any missing dependencies after import.

## Record Transformation Engine \(RTE\) and data mapping

The recovery task import process uses a Record Transformation Engine \(RTE\) to automatically transform Excel data into ServiceNow recovery tasks. Understanding the RTE helps you comprehend how the system applies your data and troubleshoot complex import scenarios.

Record Transformation Engine \(RTE\) overview: The RTE is a ServiceNow framework that defines how data flows from an external source \(Excel\) into ServiceNow tables. The RTE is configured with:

-   Entity: A definition of the source data structure. For recovery task imports, the Entity describes the columns in the Recovery task sheet \(Task ID, Short description, Dependencies, etc.\). The Entity specifies which columns are mandatory, which are optional, and their data types.
-   Mapping: A configuration that defines how each source column \(Entity field\) maps to a target ServiceNow field on the recovery task table. For example, the "Owner" column in Excel maps to the "Assigned to" field on the recovery task. The Mapping also applies business logic \(e.g., resolving user names to user records, handling N-prefixed IDs\).
-   ETL process: Extract-Transform-Load. The RTE extracts each row from the staged table and transforms the data according to the Mapping \(resolving references, applying defaults, validating values\). The RTE then loads the result into the recovery tasks table.

When RTE executes: The RTE processes staged rows asynchronously every 60 seconds. When the import job runs, it invokes the RTE for each batch of up to 500 staged rows. The RTE output is visible immediately after processing completes in the Transform history and Import log tabs.

RTE and field dependencies: The RTE validates field dependencies \(e.g., "Asset scope requires Tag assets to be set to 'Specific assets'"\). If your Excel data violates these dependencies, the RTE applies them as validation errors. See the Field handling section for a complete list of field dependencies.

Custom mapping for N-prefixed IDs: The RTE includes special handling for N-prefixed task IDs. During the N-prefixed ID resolution stage of post-processing, the RTE creates a temporary mapping of N1 -&gt; task 1001, N2 -&gt; task 1002, etc. This mapping is applied when the RTE resolves dependency references in subsequent rows.

## Recovery task import and export procedure

For the procedure, see [Import and export recovery tasks using Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/export-import-recovery-tasks-using-excel.md).

-   **[Import and export recovery tasks using Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/export-import-recovery-tasks-using-excel.md)**  
Export recovery task records to a Microsoft Excel file, edit the data offline, and import the updated file to create or update many recovery tasks at once.

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

