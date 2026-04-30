---
title: Resolve a skipped update and set a resolution status
description: To prevent your customizations from being overwritten during system upgrades, the upgrade process skips \(does not apply the update to\) objects that have been customized. One of your responsibilities as the administrator is to resolve each skipped update after an upgrade.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Skipped Changes to Review related list, Upgrade History module: Track every upgrade, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Resolve a skipped update and set a resolution status

To prevent your customizations from being overwritten during system upgrades, the upgrade process skips \(does not apply the update to\) objects that have been customized. One of your responsibilities as the administrator is to resolve each skipped update after an upgrade.

## Before you begin

Role required: admin

## About this task

You resolve an update by either retaining the customization or \(when the software upgrade contains a feature that you would like to implement\) by merging or overwriting the customization with the base system update.

**Note:** Objects that are customized and that did not change in the base system since the last upgrade require no action on your part.

When an object is customized, the system adds a corresponding record to the Customer Updates \[sys\_update\_xml\] table and then maintains current version information for all customized objects. The upgrade process skips changes to objects that have a current version in the Customer Updates table. When you follow the procedure, you perform one of the following actions:

-   Retain \(keep\) a customization with no changes
-   Retain a customization by merging changes from the updated object
-   Revert a customized object to the updated version \(that is, overwrite the customization\)
-   Review the skip and perform no action on the object

## Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Upgrade History**.

2.  Select the desired software version.

3.  In the [Skipped Changes to Review related list](../concept/skipped-changes-to-review-related-list.md), select the update record to resolve.

    **Note:** By default, the list displays records with disposition of Skipped and resolution status of Not Reviewed.

4.  Review the list of changes.

    For text fields, you can click in the field to open the Diff/Merge tool. Review the differences. Click a text box to view and edit the detailed differences.

5.  Perform one of the following actions.

    You have the option to add a **Comment** to any record, for example, to explain the action to future reviewers.

<table id="choicetable_fg3_mmp_ps"><thead><tr><th align="left" id="d169382e146">

Action

</th><th align="left" id="d169382e149">

Description

</th></tr></thead><tbody><tr><td id="d169382e155">

**Retain the customized record as is and do not update it.**

</td><td>

After reviewing the changes, set **Resolution Status** to **Reviewed and Retained**.

 The record moves from the Skipped Changes to Review to [Skipped Changes Reviewed related list](../concept/skipped-changes-reviewed-related-list.md).

</td></tr><tr><td id="d169382e189">

**Retain the customization by merging changes from the updated object.**

</td><td>

1.  Click **Resolve Conflicts** to navigate to the [Resolve Conflicts form](../../administer/platform-upgrades/reference/upgrademon-resolve-conflicts-form.md).
2.  Review the differences.
3.  To merge a field:
    -   Click the right-arrow button for the field.
    -   Click a text box to view and edit the detailed differences.
    -   When you have merged all appropriate fields, click **Merge**.
 After merging the customization changes:

 -   The **Resolution Status** changes to **Reviewed and Merged**.
-   The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.


</td></tr><tr><td id="cho_OverwriteCustomization">

**Discard the customization and update the record to match the base system for this upgrade.**

</td><td>

After reviewing the changes, click **Revert to Base System**.-   The **Disposition** changes from **Skipped** to **Reverted**.
-   The **Resolution Status** changes to **Reviewed and Reverted**.
-   The system creates a Customer Update record.
-   The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.
 **Note:** At any time after you revert a customization, you can click **Reapply Changes** to reapply the customization \(undo the revert\).

</td></tr><tr><td id="d169382e300">

**Review the skip and perform no action on the object.

**

</td><td>

After reviewing the changes, set **Resolution Status** to **Reviewed**. The record moves from the Skipped Changes to Review to the Skipped Changes Reviewed related list.

</td></tr><tr><td id="d169382e322">

**Leave on the skipped list for a later decision, and note that you have not reviewed the record.**

</td><td>

From the **Resolution** list, choose **Not Reviewed** to defer the decision on how to handle this conflict. The record stays on the Skipped Changes to Review related list.

</td></tr></tbody>
</table>6.  Click **Update**.

7.  Repeat the process to resolve each update record in the list.


## Result

Only skipped updates with a **Resolution Status** of **Not Reviewed** or without a resolution set appear in the Skipped Changes to Review related list. Any action you take that changes the **Resolution Status** to a value other than **Not Reviewed** or **--None--** removes the skipped update from list and moves it to the Skipped Changes Reviewed related list.

**Parent Topic:**[Skipped Changes to Review related list](../concept/skipped-changes-to-review-related-list.md)

**Related topics**  


[Upgrade Details related list](../concept/c_UpgradeDetails.md)

[Skipped Changes to Review related list](../concept/skipped-changes-to-review-related-list.md)

[Skipped Changes Reviewed related list](../concept/skipped-changes-reviewed-related-list.md)

