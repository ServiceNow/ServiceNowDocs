---
title: Process the skipped records list
description: Process the skipped records list to resolve the differences between the upgraded and customized versions of a record. If you have customized or altered a record affected by this upgrade, such as a business rule or script, the upgrade generates a skip log record.
locale: en-US
release: zurich
product: Upgrade Center
classification: upgrade-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Scheduling and monitoring an upgrade, Use, Upgrade Center, Upgrade, Administer]
---

# Process the skipped records list

Process the skipped records list to resolve the differences between the upgraded and customized versions of a record. If you have customized or altered a record affected by this upgrade, such as a business rule or script, the upgrade generates a skip log record.

## Before you begin

Role required: admin

## About this task

Review the changes you made to baseline records, such as business rules and scripts, that appear on the skipped records list and revert to the baseline version if appropriate. Post-upgrade, thoroughly test all changes you made to these records.

## Procedure

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade Monitor**.

    If the upgrade is still in progress, the system displays the [Upgrade Progress](../reference/uc-monitor-progress.md) screen. When the upgrade finishes, the system displays the [Upgrade Summary Report](../reference/uc-complete-summary.md).

2.  After the system displays the Upgrade Summary Report, click the Review changes link in the Skipped box.

    The system displays the [System Upgrades form](../reference/uc-system-upgrades-form.md).

3.  Navigate to Review Skipped Records section and – if necessary – scroll to the Skipped Changes to Review related list.

    See [Review skipped records using related lists](uc-access-rl.md#) for more information.

4.  Click the row for the first record you want to reconcile.

    The system displays the [Upgrade details form](../reference/uc-upgrade-details-form.md) for that record.

5.  Evaluate how you want to resolve the conflict for this record and take the appropriate action:

<table id="table_znb_ggg_rlb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Retain the customized record as is and do not update it

</td><td>

After reviewing the changes, set **Resolution Status** to **Reviewed and Retained**.The record moves from the Skipped Changes to Review to Skipped Changes Reviewed related list. See [Review skipped records using related lists](uc-access-rl.md#).

</td></tr><tr><td>

Retain the customization by merging changes from the updated object

</td><td>

1.  Click **Resolve Conflicts** to navigate to the [Resolve Conflicts form](../reference/uc-resolve-conflicts-form.md).
2.  Review the differences.
3.  To merge a field:
    -   Click the right-arrow button for the field.
    -   Click a text box to view and edit the detailed differences.
    -   When you have merged all appropriate fields, click **Merge**.
 After merging the customization changes:

-   The **Resolution Status** changes to **Reviewed and Merged**.
-   The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.


</td></tr><tr><td>

Discard the customization and update the record to match the base system for this upgrade

</td><td>

After reviewing the changes, click **Revert to Base System**.-   The **Disposition** changes from **Skipped** to **Reverted**.
-   The **Resolution Status** changes to **Reviewed and Reverted**.
-   The system creates a Customer Update record.
-   The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.

**Note:** At any time after you revert a customization, you can click **Reapply Changes** to reapply the customization \(undo the revert\).

</td></tr><tr><td>

Review the skip and perform no action on the object

</td><td>

After reviewing the changes, set **Resolution Status** to **Reviewed**. The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.

</td></tr><tr><td>

Leave on the skipped list for a later decision, and note that you have not reviewed the record

</td><td>

From the **Resolution** list, choose **Not Reviewed** to defer the decision on how to handle this conflict. The record stays on the Skipped Changes to Review related list.

</td></tr></tbody>
</table>    **Note:** The system tracks changes to records in an update set so you can apply these changes to another instance later. However, the system does not migrate the upgrade details records from one instance to the next. These records apply to a specific upgrade of a specific instance. If you want to preserve the Comments, Resolutions, or other information from the skipped list, export it from this instance.

6.  In the **Comment** field, write the reasons for making your decision and other information you want to document.

7.  Click **Update**.

    Post-upgrade, thoroughly test all changes you made to the records on the skipped record list.


