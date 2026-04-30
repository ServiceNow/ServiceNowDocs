---
title: Resolve a collision in Team Development
description: A collision is detected when the pulled version and the current local version are modifications of a different version. Collisions indicate that the record has been modified multiple times.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resolving collisions, Team Development, Planning your application, Building applications]
---

# Resolve a collision in Team Development

A collision is detected when the pulled version and the current local version are modifications of a different version. Collisions indicate that the record has been modified multiple times.

## Before you begin

Role required: admin

## About this task

To confirm that your changes don’t conflict with other development efforts, you should resolve collisions as soon as they’re identified. You must resolve all collisions before you can pull or push.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, select **Collisions** or select the count of collisions.

    A list of collisions opens.

3.  Select and hold \(or right-click\) a row and select **Resolve Collision**.

    Alternatively, open the record and select the **Resolve Collision** related link.

    The Resolve Collision page displays a comparison between the version that was pulled from the parent and your local record. The page highlights the differences.

4.  Review the differences and perform an action.

<table id="choicetable_er4_v12_5s"><thead><tr><th align="left" id="d200613e137">

Option

</th><th align="left" id="d200613e140">

Action

</th></tr></thead><tbody><tr><td id="d200613e146">

**To maintain the local record as the current version**

</td><td>

Select **Use Local Version**. The pulled version is added to the version history for the record.

</td></tr><tr><td id="d200613e158">

**To load the version pulled from the parent as the current version**

</td><td>

Select **Use Pulled Version**.

</td></tr><tr><td id="d200613e170">

**To move a setting from the selected version to update the current version**

</td><td>

To move a change, select the **&gt;** button for the field. To work with scripts and text fields, select in the field and modify the text as needed. When the records meet your needs, select **Save Merge and Resolve Collision**.**Note:** Some types of record don’t support this method. See [Limitations on updating records](../reference/r_LimitationsOnResolvingCollisions.md) for more information.

</td></tr></tbody>
</table>    The system performs the selected action and also clears the collision for future push/pulls.

5.  Repeat the process for every remaining collision.


## Result

The system saves the merged changes and resolves the collision.

