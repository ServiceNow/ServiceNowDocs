---
title: Revert a change
description: You can undo changes to a customized record by reverting to an older version.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Versions, Administer, Team Development, Planning your application, Building applications]
---

# Revert a change

You can undo changes to a customized record by reverting to an older version.

## Before you begin

Role required: none

## Procedure

1.  View a list of version records for an object.

2.  Compare the current version to the older version to ensure that you are reverting the desired changes.

3.  Right-click the older version and select **Revert to this version**.

    A confirmation dialog box appears.

    If reverting to this version results in data loss due to a database schema change, a warning message appears in the dialog box.

4.  Click **OK** to confirm the action.

    -   The current version is marked as a previous version.
    -   A new version record is added that duplicates the version that you selected in the preceding step. This new version is marked as the current version.
    **Note:** You can revert to the most recent baseline version. You cannot revert to an older baseline version.


**Parent Topic:**[Versions](../concept/c_Versions.md)

**Related topics**  


[Merge tool](../concept/diff-merge-tool.md)

[Compare to the current version](t_CompareToCurrentVersion.md)

[bundle-platcap.compare-two-article-versions]

[Compare a pushed version to a local version](t_ComparePushedVerLocalVer.md)

[Resolve a collision in Team Development](t_ResolveACollision.md)

[bundle-platadm.um-resolve-conflict]

[View customizations and compare with current version](../../system-update-sets/task/view-customer-update-records.md)

