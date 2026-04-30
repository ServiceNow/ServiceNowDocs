---
title: Compare to peer instances
description: You can compare the local instance to any other remote instance and commit any current versions from the remote instance on your development instance.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Team Development, Exploring Team Development, Team Development, Planning your application, Building applications]
---

# Compare to peer instances

You can compare the local instance to any other remote instance and commit any current versions from the remote instance on your development instance.

## About this task

Comparing allows you to share code between instances without pushing to a common parent.

Comparing instances does not automatically commit any versions on the local instance. It initiates a full comparison of all changes on the remote instance and all changes on the local instance, and then reports which customized records have different current versions. You can selectively commit a version from the remote instance or compare it with the version on your local instance. You can delete the instance comparison record when you finish evaluating the differences.

To compare the local instance to a peer instance:

## Procedure

1.  Ensure that the peer instance is [defined as a remote instance](t_DefineARemoteInstance.md).

2.  Navigate to **Team Development** &gt; **Team Dashboard**.

3.  In the control panel, click **Compare to**.

4.  Select the peer instance you want to compare to the local instance and click **Compare**.

5.  On the completion page, click **Show Results**.

    The instance comparison record opens.

    ![Compare instance](../image/CompareInstance.png)

6.  Review the On Remote and not Local related list, which shows the customized records where the current version on the peer instance is not on the local instance.

    For each customized record, you can:

    -   Compare the current remote version to the current local version by right-clicking a row and selecting **Compare to Current**.
    -   Load the current remote version as the current local version by right-clicking a row and selecting **Load This Change**.

**Parent Topic:**[Team Development](../concept/c_TeamDevelopment.md)

