---
title: Compare to the current version
description: You can compare a version to the current version for any customizable object that a user has modified, such as a form layout or business rule. You can also compare the local and current pulled version of an object in Team Development. Administrators can suppress versions for specific tables.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Versions, Administer, Team Development, Planning your application, Building applications]
---

# Compare to the current version

You can compare a version to the current version for any customizable object that a user has modified, such as a form layout or business rule. You can also compare the local and current pulled version of an object in Team Development. Administrators can suppress versions for specific tables.

## Before you begin

Role required: none

## About this task

To compare a version to the current version of an object:

## Procedure

1.  Open the Compare to Current page using one of the methods given in the below table.

    |Option|Action|
    |------|------|
    |**From [a Versions list](../concept/c_NavigatingVersionRecords.md)**|Right-click the version and select **Compare to Current**.|
    |**From the Update Versions form**|Click the **Compare to Current** related link.|

    ![The Compare to Current page includes a diff/merge tool that highlights the fields that differ.](../image/CompareToCurrentForm.png)

2.  On the Compare to Current page, review the fields that differ.

<table id="choicetable_er4_v12_5s"><thead><tr><th align="left" id="d140702e134">

Option

</th><th align="left" id="d140702e137">

Action

</th></tr></thead><tbody><tr><td id="d140702e143">

**To resolve the differences by choosing the previous version**

</td><td>

-   Team Development: Click **Revert to Selected Version**.
-   For a version of an object: Click **Use Local Version** to maintain the local record as the current version. The pulled version is added to the version history for the record.


</td></tr><tr><td id="d140702e167">

**To resolve the differences by modifying the current version and saving the merged changes__Note:__ Some types of record do not support this method. See [Limitations on updating records](../reference/r_LimitationsOnResolvingCollisions.md) for more information.

**

</td><td>

You can either update the setting in the current record or move a setting from the selected version to the current version. To move a change, click the **&gt;** \(Move Right\) button for the field in the diff/merge tool. To work with scripts and text fields, click in the field and modify the text as needed. When the records meet your needs, click:-   Team Development: Click **Save Merge** to save the changes to the current version.
-   Team Development: Click **Use Pulled Version** or **Use Local Version** option to accept or reject all changes, as appropriate.
-   On the upgrade history Compare to Current form, the only option is **Revert to Base System**


</td></tr></tbody>
</table>
**Parent Topic:**[Versions](../concept/c_Versions.md)

**Related topics**  


[Merge tool](../concept/diff-merge-tool.md)

[Compare to the current version](t_CompareToCurrentVersion.md)

[Compare a pushed version to a local version](t_ComparePushedVerLocalVer.md)

[Compare two versions of an article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/compare-two-article-versions.md)

[Resolve conflicts for an individual record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-resolve-conflict.md)

[Resolve a collision in Team Development](t_ResolveACollision.md)

[Revert a change](t_RevertAChange.md)

[View customizations and compare with current version](../../system-update-sets/task/view-customer-update-records.md)

