---
title: Compare to peer instances
description: You can compare the local instance to any other remote instance and commit any current versions from the remote instance on your development instance.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Working with version records, Team Development, Planning your application, Building applications]
---

# Compare to peer instances

You can compare the local instance to any other remote instance and commit any current versions from the remote instance on your development instance.

## Before you begin

Role required: admin

## About this task

Comparing enables you to share code between instances without pushing to a common parent instance. Comparing instances doesn’t automatically commit any versions on the local instance. Instead a full comparison of all changes on the remote instance and on the local instance. A report is generated of customized records that have different current versions.

You can selectively commit a version from the remote instance or compare it with the version on your local instance. You can delete the instance comparison record when you finish evaluating the differences.

## Procedure

1.  Confirm that the peer instance is [defined as a remote instance](t_DefineARemoteInstance.md).

2.  Navigate to **Team Development** &gt; **Team Dashboard**.

3.  In the control panel, select **Compare to**.

4.  Select the peer instance that you want to compare to the local instance and select **Compare**.

5.  On the completion page, select **Show Results**.

    The instance comparison record opens.

6.  Review the On Remote and not Local related list, which shows the customized records where the current version on the peer instance isn’t on the local instance.

    For each customized record, you can:

    -   Compare the current remote version to the current local version by select and hold \(or right-click\) a row and selecting **Compare to Current**.
    -   Load the current remote version as the current local version by select and hold \(or right-click\) a row and selecting **Load This Change**.

**Parent Topic:**[Working with version records](../concept/c_Versions.md)

