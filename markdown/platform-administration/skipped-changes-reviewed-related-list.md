---
title: Skipped Changes Reviewed related list
description: Skipped Changes Reviewed lists update records that previously appeared on the Skipped Changes to Review related list and have been reviewed. When you select a skipped record to review and set a Resolution Status to a value other than Not Reviewed, the update record moves to the Skipped Changes Reviewed related list.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Upgrade History module: Track every upgrade, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Skipped Changes Reviewed related list

Skipped Changes Reviewed lists update records that previously appeared on the **Skipped Changes to Review** related list and have been reviewed. When you select a skipped record to review and set a **Resolution Status** to a value other than Not Reviewed, the update record moves to the Skipped Changes Reviewed related list.

Navigate to **System Diagnostics** &gt; **Upgrade History** to view the Skipped Changes Reviewed related list.

<table id="table_b1j_fzg_sbb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

File name

</td><td>

Name of reviewed Upgrade Details record.

</td></tr><tr><td>

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

Claim Status

</td><td>

Outcomes:-   N/A: There are no claims on the record \(no need to review\)
-   Won conflict: The loading application loaded the file but is in conflict with the previously loaded file. Recommendation: Review the two versions of the file to confirm your intended outcome.
-   No conflict: There may be one or more applications loading but there is no conflict. However, it is still good to review the outcome to see if it's what you intended.
-   Lost conflict: The file was not loaded because another application has a better claim on the file. Recommendation: Review the two versions of the file to see which should be loaded \(or if they should be merged\).

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

