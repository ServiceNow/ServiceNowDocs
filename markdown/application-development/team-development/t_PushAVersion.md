---
title: Push a version
description: Pushing promotes changes from the development instance to the parent instance and commits the current version of a customized record on the development instance as the current version on the parent instance.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Team Development, Planning your application, Building applications]
---

# Push a version

Pushing promotes changes from the development instance to the parent instance and commits the current version of a customized record on the development instance as the current version on the parent instance.

## Before you begin

Role required: none

## About this task

Pushing adds only the current development version to the parent, not all the development versions.

**Note:** Updates to records from different applications cannot be pushed/pulled in the same push/pull. To resolve the error in the case that updates to other applications are mixed in: De-queue the updates to other applications. Push for one application. Re-queue the updates to one application. Push and then repeat as needed.

Pushing creates a local Update Set on the parent that is marked as complete. Pushed changes are also tracked as local changes on the parent. Therefore, you can promote changes through your development and test hierarchy by transferring the Update Set or by pushing the local changes. Each push is recorded in the Push or Pull table on the development instance.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  [Queue the local changes](t_QueueALocalChangeForAPush.md) that are ready to push.

3.  [Pull versions](t_PullAVersion.md) from the parent instance and [resolve any collisions](t_ResolveACollision.md).

    You cannot push changes to the parent instance if collisions are detected.

4.  In the control panel, click **Push**.

    The Push Changes page opens.

5.  Provide a Name for the changes.

6.  Review the list of changes to ensure that the correct changes are included.

<table id="choicetable_qtn_cmc_bq"><tbody><tr><td id="d150006e150">

**To remove changes that you do not want to push**

</td><td>

Select the check boxes beside the rows and select **Do Not Push** from the Actions choice list

</td></tr><tr><td id="d150006e165">

**To add changes**

</td><td>

Click **Cancel** and repeat the procedure from [step 2](t_PushAVersion.md#step-2-queue-local-changes)

</td></tr></tbody>
</table>    ![Push versions](../image/PushVersions.png)

7.  Edit the name.

    The name identifies the push record on the development instance and the local Update Set record on the parent instance.

8.  Enter comments.

    The comments are added to the push record on the development instance and the local Update Set record on the parent instance.

9.  Click **Push Changes**.

    The system initiates a pull to ensure that there are no collisions before the push proceeds.

    -   If collisions are detected, the push is automatically canceled and you must repeat the procedure from [step 3](t_PushAVersion.md#step-3-pull-versions).
    -   If no collisions are detected, the changes are staged on the parent instance. On the parent, each version is validated and then committed in the correct order to maintain dependencies between records. For example, a new table is committed before a field on that table to ensure the field is properly created.
    **Note:** You cannot push if there is a version conflict between instances or the pushing instance has changes in the Awaiting Code Review stage.

10. On the completion page, click **Show Results**.

11. Review the push record for any errors or skipped changes.

    -   Changes with a state of Pushed were committed on the parent instance.
    -   Changes with a state of Skipped were not committed on the parent instance and remain queued as local changes on the development instance.
12. For each skipped change, review the log message to determine why the change was skipped.

    Develop any changes that are necessary to commit the desired version on the parent instance, and then push them. Some examples of why a change may be skipped include:

    -   A table does not exist on the parent because it was created when you activated a plugin on the development instance. Ensure the plugin is activated on the parent and push the change again.
    -   An error occurred during the push. Try to push again.
    -   The current version is invalid. Revert to a previous version and make the change again to ensure the version is valid
    -   An error occurred on the parent during the push. The Log field on the push record contains the exception message. Review the system logs on the parent instance and troubleshoot any problems with the instance.
    ![Push history](../image/PushHistory.png)


