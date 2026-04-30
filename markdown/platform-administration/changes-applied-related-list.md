---
title: Changes Applied related list
description: Changes Applied lists all changes that were applied in this upgrade.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Upgrade History module: Track every upgrade, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Changes Applied related list

Changes Applied lists all changes that were applied in this upgrade.

This list is ordered by priority and displays Upgrade Detail records for this upgrade that have a disposition of Updated, Updated \(second pass\), Inserted, Inserted \(second pass\), Deleted, Deleted \(second pass\), and for which the changed flag is true for all of the dispositions.

Navigate to **System Diagnostics** &gt; **Upgrade History** to view the Changes Applied related list.

<table id="table_b1j_fzg_sbb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Disposition

</td><td>

Action performed on this file during the selected upgrade:-   Inserted: The system inserted a new record.
-   Updated: The system updated this record.
-   Deleted: The system deleted this record.
-   Skipped: The system did not change this record in order to preserve customizations.
-   Reverted: This record was reverted to the base version.
-   Table not found: The system could not find the table that contains this record.
-   Unchanged: The system did not change this record because the baseline component has not changed since the last release.
-   Skipped Manual Merge: The system did not change this record because updating it requires manual intervention.
-   Skipped Apply Once: The system skipped this record because it had already applied an update from an xml file in the apply once folder.
-   Not Latest: The system applied a change, but this change was overwritten later during the same upgrade.

</td></tr><tr><td>

Priority

</td><td>

Relative importance of the conflict that caused the skip based on the following criteria:-   1 \(highest priority\): xml content
-   2: script or script\_plain
-   3: html content
-   4: sys\_ui\_form\_section, sys\_ui\_related\_list, or sys\_choice\_set
-   5 \(lowest priority\): other

</td></tr><tr><td>

Resolution

</td><td>

-   Reviewed
-   Retained
-   Reverted

</td></tr><tr><td>

Comment

</td><td>

During the process of resolving a skipped update, you have the option to add a **Comment** to any record. For example, the comment might explain the action that you took to future reviewers.

</td></tr><tr><td>

Target name

</td><td>

Name of the record corresponding to the current file.

</td></tr><tr><td>

Plugin

</td><td>

Plugin that contains the record.

</td></tr><tr><td>

Type

</td><td>

Current file type \(such as Business Rule or UI Policy\).

</td></tr><tr><td>

Table

</td><td>

Table that contains the record.

</td></tr><tr><td>

File name

</td><td>

Current upgrade file name.

</td></tr><tr><td>

File differences

</td><td>

Comparison of the file in the upgrade with the customized version.

</td></tr><tr><td>

Changed by vendor

</td><td>

Indicates whether the file has been changed by the vendor since the last upgrade.

</td></tr></tbody>
</table>**Parent Topic:**[Upgrade History module: Track every upgrade](c_UpgradeHistory.md)

