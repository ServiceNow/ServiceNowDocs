---
title: Resolve a skipped update and set a resolution status
description: Review the reason for each skipped record to resolve each skipped update after an upgrade.
locale: en-US
release: zurich
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reviewing upgrade history, Upgrade History tool in Upgrade Console, Upgrade Console tools, Use, Upgrade Console, Upgrade, Administer]
---

# Resolve a skipped update and set a resolution status

Review the reason for each skipped record to resolve each skipped update after an upgrade.

## Before you begin

Role required: admin

## About this task

You resolve an update by either retaining the customization or by merging or overwriting the customization with the base system update.

**Note:** Objects that are customized and that did not change in the base system since the last upgrade require no action on your part.

When an object is customized, the system adds a corresponding record to the Customer Updates \[sys\_update\_xml\] table and then maintains current version information for all customized objects. The upgrade process skips changes to objects that have a current version in the Customer Updates table. When you follow the procedure, you perform one of the following actions:

-   Retain a customization with no changes
-   Retain a customization by merging changes from the updated object
-   Revert a customized object to the updated version \(that is, overwrite the customization\)
-   Review the skip and perform no action on the object

## Procedure

1.  Navigate to Upgrade History using one of the following ways.

    |Option|Navigation|
    |------|----------|
    |Using left navigation|Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Management** &gt; **Upgrade History**.|
    |Using Admin tab option|Navigate to **Admin** &gt; **Upgrade Management** &gt; **Upgrade History**.|

    A list of upgrades is displayed.

2.  Select the desired software version.

3.  In the Skipped Changes to Review related list, select the update record to resolve.

    See [Review skipped records using related lists](um-access-rl.md#).

4.  Review the list of changes.

    For text fields, you can click in the field to open the Diff/Merge tool.

    To review the differences, Click a text box to view and edit the detailed differences.

5.  Perform one of the following actions.

    You have the option to add a **Comment** to any record, for example, to explain the action to future reviewers.

<table id="table_cqj_4jv_dlb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Retain the customized record as is and do not update it.

</td><td>

After reviewing the changes, set **Resolution Status** to **Reviewed and Retained**.The record moves from the Skipped Changes to Review to Skipped Changes Reviewed related list.

</td></tr><tr><td>

Retain the customization by merging changes from the updated object.

</td><td>

1.  Click**Resolve Conflicts** to navigate to the Resolve Conflicts form.
2.  Review the differences.
3.  To merge a field:
    -   Click the right-arrow button for the field.
    -   Click a text box to view and edit the detailed differences.
    -   When you have merged all appropriate fields, click **Merge**.
 After merging the customization changes:

-   The Resolution Status changes to Reviewed and Merged.
-   The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.


</td></tr><tr><td>

Discard the customization and update the record to match the base system for this upgrade.

</td><td>

After reviewing the changes, click **Revert to Base System**.-   **Disposition** changes from **Skipped** to **Reverted**.
-   **Resolution Status** changes to **Reviewed and Reverted**.
-   The system creates a Customer Update record.
-   The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.
 **Note:** At any time after you revert a customization, you can click **Reapply Changes** to reapply the customization.

</td></tr><tr><td>

Review the skip and perform no action on the object.

</td><td>

After reviewing the changes, set **Resolution Status** to **Reviewed**. The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.

</td></tr><tr><td>

Leave on the skipped list for a later decision, and note that you have not reviewed the record.

</td><td>

From the **Resolution** list, choose **Not Reviewed** to defer the decision on how to handle this conflict. The record stays on the Skipped Changes to Review related list.

</td></tr></tbody>
</table>6.  Click **Update**.

7.  Repeat the process to resolve each update record in the list.


## Result

Only skipped updates with a **Resolution Status** of **Not Reviewed** or without a resolution set appear in the Skipped Changes to Review related list. Any action you take that changes the **Resolution Status** to a value other than **Not Reviewed** or **--None--** removes the skipped update from list and moves it to the Skipped Changes Reviewed related list.

**Parent Topic:**[Reviewing upgrade history](../concept/um-review-history.md)

