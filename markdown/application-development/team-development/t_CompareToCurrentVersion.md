---
title: Compare to the current version
description: Compare a version to the current version for any customizable object that is modified, such as a form layout or business rule. Team Development can be used to compare the local and current pulled version of an object.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Working with version records, Team Development, Planning your application, Building applications]
---

# Compare to the current version

Compare a version to the current version for any customizable object that is modified, such as a form layout or business rule. Team Development can be used to compare the local and current pulled version of an object.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Open the Compare to Current page using one of the options in the table.

    |Option|Action|
    |------|------|
    |**From [a Versions list](../concept/c_NavigatingVersionRecords.md)**|Navigate to **All** &gt; **Team Development** &gt; **Versions**. Select and hold \(or right-click\) the version and select **Compare to Current**.|
    |**From the Update Versions form**|Select the **Compare to Current** related link.|

2.  Review any differences in the fields.

<table id="choicetable_er4_v12_5s"><thead><tr><th align="left" id="d130104e145">

Option

</th><th align="left" id="d130104e148">

Action

</th></tr></thead><tbody><tr><td id="d130104e154">

**To resolve the differences by choosing the previous version**

</td><td>

-   Team Development: Select **Revert to Selected Version**.
-   Object version: Select **Use Local Version** to maintain the local record as the current version. The pulled version is added to the version history for the record.


</td></tr><tr><td id="d130104e180">

**To resolve the differences by modifying the current version and saving the merged changes**

</td><td>

You can either update the setting in the current record or move a setting from the selected version to the current version. To move a change, select the **&gt;** button for the field in the diff/merge tool. To work with scripts and text fields, select in the field and modify the text as needed. When the records meet your needs, select:-   Team Development: Select **Save Merge** to save the changes to the current version.
-   Team Development: Select **Use Pulled Version** or **Use Local Version** option to accept or reject all changes, as appropriate.
-   Upgrade history: Select **Revert to Base System**
 **Note:** Some types of record don’t support this method. See [Limitations on updating records](../reference/r_LimitationsOnResolvingCollisions.md) for more information.

</td></tr></tbody>
</table>3.  For more information on how to compare see [Merge tool](../concept/diff-merge-tool.md).


-   **[Merge tool](../concept/diff-merge-tool.md)**  
The Diff Merge tool enables you to compare differences between two versions of a record.

**Parent Topic:**[Working with version records](../concept/c_Versions.md)

