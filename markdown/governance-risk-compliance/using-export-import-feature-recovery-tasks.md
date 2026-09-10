---
title: Importing and exporting recovery tasks from Microsoft Excel
description: Export recovery tasks to a Microsoft Excel file, edit offline, and import the file to create or update multiple tasks at once.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/using-export-import-feature-recovery-tasks.html
release: zurich
topic_type: concept
last_updated: "2026-08-19"
reading_time_minutes: 8
keywords: [BCM, import, export, Excel, recovery task]
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Importing and exporting recovery tasks from Microsoft Excel

Export recovery tasks to a Microsoft Excel file, edit offline, and import the file to create or update multiple tasks at once.

The **Export to Excel** and **Import from Excel** actions are available in the **Recovery tasks** related list on a business continuity plan. Use these actions to create or update many recovery tasks in bulk outside the ServiceNow interface.

## Exported workbook

The exported workbook exports 24 columns of recovery task data across three sheets:

-   Instructions sheet: Describes each column, including whether it's mandatory or read-only, the valid values for choice and reference fields, and an example. Review this sheet before you edit the file, especially the valid values for reference fields such as Owner, Configuration item, and Related plan.
-   Plan details sheet: A read-only reference sheet that shows the properties of the parent plan. Don't edit this sheet.
-   Recovery task sheet: The data sheet that you edit, with one row per recovery task.

The following table shows how Microsoft Excel columns map to recovery task fields and their validation rules. The **Task ID** and **Short description** columns are mandatory. Dependencies are exported as comma-separated task IDs because the short description isn't unique.

|Column|Description|
|------|-----------|
|Task ID|Unique identifier for the task, unique within the plan but not necessarily unique across other plans. Read-only for existing tasks. Use a temporary N-prefixed identifier to create a task. See the "Import processing" section on this page.|
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

The import performs row-level validation against the following field-handling rules.

|Column|Rule|
|------|----|
|Owner|Uses a drop-down list of all users in the system. If the user table contains more than 10,000 records, the drop-down list is disabled and the field becomes a plain text field. In this case, enter the exact user name as it's defined in the system.|
|Additional assignees|Accepts comma-separated user names. The import validates entries against the user name field, not the display name. If two users share the same display name, the import always selects the first matching record, which can cause an incorrect assignment. Enter exact user names to avoid ambiguity. If you enter a user that doesn't exist, the import returns an error.|
|Dependencies|Accepts comma-separated task IDs, including the temporary N-prefixed IDs of tasks that this import creates. See the "Import processing" section on this page.|
|Configuration item|Enter the configuration item name exactly as it's defined in the system. If the name matches more than one configuration item, the import logs a warning on the plan's **Import log** tab and continues.|
|Task classification and Activate a related plan|These fields are mutually exclusive. An automated task can't also activate a related plan. On the form, setting **Task classification** to **Automated** hides the **Recovery team** and **Additional assignees** fields, but import doesn't automatically clear those fields. If you populate **Recovery team** or **Additional assignees** for an automated task, the import might fail during validation or return a business rule error.|
|Related plan|Applies only when **Activate a related plan** is **true**. The chosen plan must already be added as a related plan on the current plan, and can't create a cyclic plan dependency. Combined upstream and downstream plan nesting can't exceed 10 levels. On the form, setting **Activate a related plan** to **true** hides the **Assignment group**, **Loss scenario**, **Documentation**, and **Recovery strategy** fields, but import doesn't clear or enforce those fields.|
|Documentation, Loss scenario, and Recovery strategy|**Documentation** and **Recovery strategy** are mutually exclusive. Set **Loss scenario** before **Recovery strategy**. The **Recovery strategy** choices are limited to strategies that belong to the selected loss scenario.|
|Tag assets and Asset scope|**Asset scope** applies only when **Tag assets** is **Specific assets**. Setting **Tag assets** to **All assets from loss scenario** or **All assets from recovery strategy** requires the matching **Loss scenario** or **Recovery strategy** column to be populated on the same row. The import fails a row that's missing this required value.|
|Planned duration|Free text that combines one or more units: days, hours, minutes, or seconds. Use the full unit name with standard spacing, and don't use abbreviations, for example, `2 Days 4 Hours`, `1 Day 30 Minutes`, `5 Days`, `12 Hours`, or `30 Minutes`.|

For reference fields that match records by display name, such as **Configuration item**, **Documentation**, and **Related plan**, more than one record can share the same display name. If more than one **Configuration item** record uses the same name, the import matches the first record found and logs a warning on the **Import log** tab. If more than one **Documentation** section on the plan uses the same name, the import links the first matching section, which might not be the one you intended. If more than one **Related plan** record uses the same name, the import might select the incorrect plan. The row fails if the selected plan would exceed the plan-nesting depth limit described in this table. To avoid this issue, use unique display names for these records, or review the **Import log** tab and manually correct any mismatched records after import.

**Tip:** The **Additional assignees** and **Dependencies** columns are glide list fields that accept multiple comma-separated values. Microsoft Excel doesn't support multi-select drop-down lists, so the import validates each value only at import time, not while you edit the file. Review the Instructions sheet in the exported file for the valid values for these fields before you import.

## Import processing

When you import the file, the records are staged in a recovery-task import table. A scheduled job checks for pending imports every 60 seconds and processes all staged records into recovery tasks in a single run, in batches of 500.

Each row either updates an existing recovery task or creates one, based on the **Task ID** column:

-   To update an existing task, keep its numeric task ID. Don't change this value, or the update fails.
-   To create a task, enter a temporary N-prefixed identifier, for example, `N1` or `N2`. The system assigns the task a real task ID after import. Reference an N-prefixed identifier in the **Dependencies** column of any row in the file, including another new row, to set up dependencies between tasks that don't exist yet. For example, task `N5` can depend on existing tasks 1, 2, and 3. Task `N7` can depend on a combination of new and existing tasks, such as `N5`, `N6`, 1, and 2. Task `N6` can depend on task `N7`, creating a dependency chain between new tasks. The import job resolves all dependencies during processing, regardless of the row order in the file.

## Checking import results

After you start an import, select **View import progress** in the plan header to reopen the progress tracker. When the import finishes, review the following for traceability of the import run:

-   **Import log** tab: Review warnings and errors about specific rows, for example, a Configuration item value that matches more than one configuration item.
-   **Transform history** tab: View a summary of the most recent import run, including rows that were inserted, updated, or skipped, and any row-level errors.

**Important:** If a row's **Dependencies** value references a task ID that doesn't exist, including an invalid N-prefixed identifier, the import silently skips that dependency without affecting the rest of the row. The task is still created or updated with all other valid fields and valid dependencies. Review the **Import log** and **Transform history** tabs to identify rows with partially applied dependencies, and manually add any missing dependencies after import.

## Recovery task import and export procedure

For the procedure, see [Export and import recovery tasks from Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/export-import-recovery-tasks-using-excel.md).

-   **[Export and import recovery tasks from Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/export-import-recovery-tasks-using-excel.md)**  
Export recovery task records to a Microsoft Excel file, edit the data offline, and import the updated file to create or update many recovery tasks at once.

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

