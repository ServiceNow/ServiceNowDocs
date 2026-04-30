---
title: Push a version
description: You can push a version from the development instance to the parent instance.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Pushing changes, Working with changes, Team Development, Planning your application, Building applications]
---

# Push a version

You can push a version from the development instance to the parent instance.

## Before you begin

Role required: admin

## About this task

Pushing adds only the current development version to the parent, not all the development versions. Updates to records from different applications can’t be pushed/pulled in the same push/pull.

You can resolve the error in the case that updates to other applications are mixed in:

1.  Stop the updates to other applications.
2.  Push for one application.
3.  Requeue the updates to one application.
4.  Push and then repeat as needed.

Pushing creates a local update set on the parent that is marked as complete. Pushed changes are also tracked as local changes on the parent. You can promote changes through your development and test hierarchy by transferring the Update Set. You can also push the local changes. Each push is recorded in the Push or Pull table on the development instance.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  [Queue the local changes](t_QueueALocalChangeForAPush.md) that are ready to push.

3.  [Pull versions](t_PullAVersion.md) from the parent instance and [resolve any collisions](t_ResolveACollision.md).

    If collisions are detected, you can’t push changes to the parent instance.

4.  In the control panel, select **Push**.

    The Push Changes page opens.

5.  Provide a Name for the changes.

6.  Review the list of changes to confirm that the correct changes are included.

    -   To remove changes.

        Select the changes and select **Do Not Push** from the Actions list.

    -   To add changes.

        Select **Cancel** and then select the changes to add.

7.  Enter comments.

    The comments are added to the push record on the development instance and the local Update Set record on the parent instance.

8.  Select **Push Changes**.

    The system initiates a pull to confirm that there are no collisions before the push proceeds.

    -   If collisions are detected, the push is automatically canceled and you must repeat the procedure from [step 3](t_PushAVersion.md#step-3-pull-versions).
    -   If no collisions are detected, the changes are staged on the parent instance. On the parent, each version is validated and then committed in the correct order to maintain dependencies between records. For example, a new table is committed before a field on that table to confirm the field is properly created.
    **Note:** You can’t push if there’s a version conflict between instances or the pushing instance has changes in the Awaiting Code Review stage.

9.  On the completion page, select **Show Results**.

10. Review the push record for any errors or skipped changes.

    -   Changes with a state of Pushed were committed on the parent instance.
    -   Changes with a state of Skipped weren’t committed on the parent instance and remain queued as local changes on the development instance.
11. For each skipped change, review the log message to determine why the change was skipped.

    Develop any changes that are necessary to commit the desired version on the parent instance, and then push them. Some examples of why a change is skipped include:

    -   A table doesn’t exist on the parent because it was created when you activated a plugin on the development instance. Confirm that the plugin is activated on the parent and push the change again.
    -   An error occurred during the push. Try to push again.
    -   The current version is invalid. Revert to a previous version and make the change again to confirm the version is valid
    -   An error occurred on the parent during the push. The Log field on the push record contains the exception message. Review the system logs in the parent instance and troubleshoot any problems with the instance.

**Parent Topic:**[Pushing changes](../concept/pushing-changes.md)

