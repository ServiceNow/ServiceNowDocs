---
title: Knowing about History sets
description: The system automatically generates History Set records as needed from the Audit table when a user either creates a record or views its history.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Auditing]
---

# Knowing about History sets

The system automatically generates History Set records as needed from the Audit table when a user either creates a record or views its history.

If a record is in an audited table, its history set is generated when the record is inserted or when a user views the record.

**Note:** Don’t use history sets to generate reports.

Several fields of information are captured in the History Set record, displayed in the list view.

|Field|Input Value|
|-----|-----------|
|ID|Document ID for the record whose history is being recorded.|
|Table|Audited table for the record whose history is being recorded.|
|Load Time|Amount of time it took to generate the history set.|

<table id="table_yym_ryd_wq"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Label

</td><td>

The label of the field that was changed.

</td></tr><tr><td>

Old

</td><td>

Value before the change.

</td></tr><tr><td>

New

</td><td>

Value after the change.

</td></tr><tr><td>

Type

</td><td>

Indicates if the entry is for a normal field, an email record, or a relationship change record.

</td></tr><tr><td>

Update Number

</td><td>

The number of times this field has been changed. A value of -1 indicates when the record was created or deleted.

</td></tr><tr><td>

Update Time

</td><td>

Date and time of the change.**Note:** The Update time for auto-generated history lines doesn’t match the Created or the Updated time for a record in a specific processing situation. When you view a history set of a record for the first time, an initial set of history line records is auto-generated. Since file changes in an upgrade aren’t audited, this date mismatch occurs when:

-   You view a history set after a change is made to a record, but
-   Before another change is made to it in a future upgrade.

</td></tr><tr><td>

User Name

</td><td>

Name of the user who created the change.

</td></tr></tbody>
</table>## History Sets in a Calendar View

After History Sets are active, the History context menu choice populates using information from the history set, rather than from the `sys_audit` table. From the user's perspective, the same historical data is available in the same user interface, but how the information is stored is different.

Since the History view includes a calendar view, but doesn’t use the normal list interface to filter and interact with the history records, it enables:

-   Searching and filtering historic data.
-   Exporting historic data.

## Viewing history sets

There are two ways of viewing the history set, accessible through the Context Menu action **History**.

