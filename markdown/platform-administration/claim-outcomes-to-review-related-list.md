---
title: Claim Outcomes to Review related list
description: During system upgrades, the Claim Status tab displays outcomes to review and resolve. See the Claim Status field in the table below.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Upgrade History module: Track every upgrade, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Claim Outcomes to Review related list

During system upgrades, the Claim Status tab displays outcomes to review and resolve. See the Claim Status field in the table below.

By default, the list is filtered by Disposition Skipped Error, Disposition Skipped Manual Merge, Disposition Skipped, or Disposition Skipped \(second pass\), and the resolution status is either empty or not reviewed.

Navigate to **System Diagnostics** &gt; **Upgrade History** to view the Claimed Outcomes to Review related list.

<table id="table_b1j_fzg_sbb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

File name

</td><td>

Name of skipped Upgrade Detail record.

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
-   No conflict: The installing application loaded the file without any conflicts; however, there may be one or more applications loading the same file so it is still recommended to review the outcomes.
-   Lost conflict: The file was not loaded because another application has a better claim on the file. Recommendation: Review the two versions of the file to see which should be loaded \(or if they should be merged\).

</td></tr><tr><td>

Priority

</td><td>

Relative importance of the conflict that caused the skip based on the following criteria:-   1: UI pages, UI macros, and more
-   2: Business rules, security ACLs, and more
-   3: Reports and more
-   4: Form sections, choice sets, and more
-   5 Everything else

</td></tr><tr><td>

Resolution

</td><td>

-   Not reviewed: Records which have not been reviewed
-   Reviewed: Records which have been reviewed
-   Reviewed and Merged: Records which have been reviewed and have both the old and new changes
-   Reviewed and Retained: Records which have been reviewed and have retained the updates from the latest upgrade
-   Reviewed and Reverted: Records which have been reviewed and have reverted changes to the base system

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

</td></tr></tbody>
</table>**Parent Topic:**[Upgrade History module: Track every upgrade](c_UpgradeHistory.md)

