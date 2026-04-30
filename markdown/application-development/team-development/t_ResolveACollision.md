---
title: Resolve a collision in Team Development
description: A collision is detected when the pulled version and the current local version are modifications of a different version, indicating that someone else has modified the same record that you have modified. The team dashboard displays the number of collisions between the local and the parent instance.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Team Development, Exploring Team Development, Team Development, Planning your application, Building applications]
---

# Resolve a collision in Team Development

A collision is detected when the pulled version and the current local version are modifications of a different version, indicating that someone else has modified the same record that you have modified. The team dashboard displays the number of collisions between the local and the parent instance.

## About this task

To ensure that your changes do not conflict with other development efforts, you should resolve collisions as soon as they are identified. You must resolve all collisions before you can pull or push.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, click **Collisions** or click the count of collisions.

    A list of collisions opens.

3.  Right-click a row and select **Resolve Collision**.

    Alternatively, open the record and click the **Resolve Collision** related link.

    The Resolve Collision page displays a comparison between the version that was pulled from the parent and your local record. The page highlights the differences.

4.  Review the differences and perform an action.

    |Option|Action|
    |------|------|
    |**To maintain the local record as the current version**|Click **Use Local Version**. The pulled version is added to the version history for the record.|
    |**To load the version pulled from the parent as the current version**|Click **Use Pulled Version**.|
    |**To move a setting from the selected version to update the current version__Note:__ Some types of record do not support this method. See [Limitations on updating records](../reference/r_LimitationsOnResolvingCollisions.md) for more information.

**|To move a change, click the **&gt;** \(Move Right\) button for the field. To work with scripts and text fields, click in the field and modify the text as needed. When the records meet your needs, click **Save Merge and Resolve Collision**.|

    The system performs that action and also clears the collision for future push/pulls.

5.  Repeat the process for every remaining collision.


## Result

The system saves the merged changes and resolves the collision.

**Parent Topic:**[Team Development](../concept/c_TeamDevelopment.md)

**Related topics**  


[Compare to the current version](t_CompareToCurrentVersion.md)

[Compare a pushed version to a local version](t_ComparePushedVerLocalVer.md)

[Compare two versions of an article](https://www.servicenow.com/docs/access?context=compare-two-article-versions&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Resolve conflicts for an individual record](https://www.servicenow.com/docs/access?context=um-resolve-conflict&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Revert a change](t_RevertAChange.md)

[View customizations and compare with current version](../../system-update-sets/task/view-customer-update-records.md)

