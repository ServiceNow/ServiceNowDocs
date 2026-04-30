---
title: Team dashboard
description: The team dashboard provides a central place to manage all Team Development activities on your development instance.
locale: en-US
release: xanadu
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Team Development overview, Team Development, Planning your application, Building applications]
---

# Team dashboard

The team dashboard provides a central place to manage all Team Development activities on your development instance.

You can track local changes, pull and push changes between the local and parent instances, compare the local instance to other development instances, and resolve any collisions. You can also reconcile with the current parent instance or change the parent instance.

To access the dashboard, navigate to **Team Development** &gt; **Team Dashboard**.

![Team dashboard](../image/TeamDashboard.png "Team dashboard")

The control panel in the top left provides status indicators and Team Development actions.

-   Parent: indicates the status of the connection to the parent instance. If a problem or warning is detected, point to the indicator to view the error messages, or click the indicator to open the remote instance record.
-   **Change**: changes the parent instance. See [Changing the Parent Instance](../task/t_ChangeTheParentInstance.md).
-   **Reconcile**: compares the development instance to the parent instance. See [Reconciling](../task/t_Reconcile.md).
-   Ready to Pull: indicates the number of changes on the parent that have not been pulled to the local instance.
-   **Pull**: initiates a pull. See [Pulling Versions](../task/t_PullAVersion.md).
-   **Push**: opens a page that allows you to review the changes before a push. See [Pushing Versions](../task/t_PushAVersion.md).
-   **Refresh**: updates the status indicators on the control panel. The dashboard updates only when you reload or refresh the page.
-   Local: indicates the status of the most recent comparison with another instance. If collisions are detected, click the indicator to open the list and resolve the collisions. See [Resolve a collision in Team Development](../task/t_ResolveACollision.md).
-   Collisions: appears only if any local changes collide with versions pulled from the parent and indicates the number of collisions. Click the indicator to open the list and resolve the collisions. See [Resolve a collision in Team Development](../task/t_ResolveACollision.md).
-   **Compare to**: allows you to select another development instance to compare with the local instance. See [Comparing to Peer Instances](../task/t_CompareToAPeerInstance.md).
-   Ready to Push: indicates the number of local changes that are queued for the next push. See [Queuing and Ignoring Local Changes](../task/t_QueueALocalChangeForAPush.md).
-   Local changes: indicates the number of local changes that have not been queued or ignored. Click the indicator to open a list of these changes.
-   Ignored: appears only if any local changes are ignored and indicates the number of ignored changes. Click the indicator to open a list of these changes.

The team dashboard includes lists for tracking local changes and viewing the history of Team Development activities.

-   Local changes: lists the local changes that have not been queued or ignored.
-   Pushes and Pulls: provides a history of pushes and pulls. Expand a row to see the customized records for which versions were transferred as part of the push or pull.
-   Instance Comparisons: provides a history of comparisons with other development instances.
-   Collisions: lists the collisions that must be resolved before the next pull or push. You can right-click a row and select **Resolve Collision**. See [Resolving Collisions](../task/t_ResolveACollision.md).
-   Ready to Push: lists the local changes that have been queued for the next push.
-   Ignored: lists the local changes that are ignored for all pushes.

**Parent Topic:**[Team Development overview](../concept/c_UsingTeamDevelopment.md)

**Related topics**  


[Team Development overview](../concept/c_UsingTeamDevelopment.md)

[Pull a version](../task/t_PullAVersion.md)

[Pull exceptions](r_PullExceptions.md)

[Resolve a collision in Team Development](../task/t_ResolveACollision.md)

[Resolve multiple collisions](../task/t_ResolveMultipleCollisions.md)

[Local changes](../concept/c_LocalChanges.md)

[Local change lists](../concept/c_NavigatingLocalChangeLists.md)

[Queue a local change for a push](../task/t_QueueALocalChangeForAPush.md)

[Ignore a local change](../task/t_IgnoreALocalChange.md)

[Back out a local change](../task/t_BackOutALocalChange.md)

[Push a version](../task/t_PushAVersion.md)

[Approve or reject a push](../task/t_ApproveOrRejectAPush.md)

[Check the review status of a pushed change](../task/t_CheckReviewStatusOfAPushedChange.md)

[Cancel a code review request](../task/t_CancelACodeReviewRequest.md)

[Compare to peer instances](../task/t_CompareToAPeerInstance.md)

[Change the parent instance](../task/t_ChangeTheParentInstance.md)

[Reconcile changes](../task/t_Reconcile.md)

