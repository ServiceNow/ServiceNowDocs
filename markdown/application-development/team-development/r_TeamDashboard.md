---
title: Team dashboard
description: The team dashboard provides a central place to manage all Team Development activities on your development instance.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-09-23"
reading_time_minutes: 4
breadcrumb: [Explore, Team Development, Planning your application, Building applications]
---

# Team dashboard

The team dashboard provides a central place to manage all Team Development activities on your development instance.

You can track local changes, pull, and push changes between the local and parent instances, compare the local instance to other development instances, and resolve any collisions. You can also reconcile with the current parent instance or change the parent instance.

To access the dashboard, navigate to **Team Development** &gt; **Team Dashboard.**![Team Development dashboard](../image/team-dashboard-new.png)

## Control panel

**Note:** The control panel only displays once a remote instance is selected.

The control panel provides status indicators for Team Development actions.

|Status|Description|
|------|-----------|
|Parent|Indicates the status of the connection to the parent instance. If a problem or warning is detected, hover over the indicator to view the error messages, or select the indicator to open the remote instance record.|
|Change|Changes the parent instance. See [Changing the Parent Instance](../task/t_ChangeTheParentInstance.md).|
|Reconcile|Compares the development instance to the parent instance. See [Reconciling](../task/t_Reconcile.md).|
|Ready to Pull|Indicates the number of changes on the parent that haven’t been pulled to the local instance.|
|Pull|Initiates a pull. See [Pulling Versions](../task/t_PullAVersion.md).|
|Push|Opens a page that enables you to review the changes before a push. See [Pushing Versions](../task/t_PushAVersion.md).|
|Refresh|Updates the status indicators on the control panel. The dashboard updates only when you reload or refresh the page.|
|Local|Indicates the status of the most recent comparison with another instance. If collisions are detected, select the indicator to open the list and resolve the collisions. See [Resolve a collision in Team Development](../task/t_ResolveACollision.md).|
|Collisions|Appears only if any local changes collide with versions pulled from the parent and indicates the number of collisions. Select the indicator to open the list and resolve the collisions. See [Resolve a collision in Team Development](../task/t_ResolveACollision.md).|
|Compare to|Enables you to select another development instance to compare with the local instance. See [Comparing to Peer Instances](../task/t_CompareToAPeerInstance.md).|
|Ready to Push|Indicates the number of local changes that are queued for the next push. See [Queuing and Ignoring Local Changes](../task/t_QueueALocalChangeForAPush.md).|
|Local changes|Indicates the number of local changes that haven’t been queued or ignored. Select the indicator to open a list of these changes.|
|Ignored|Appears only if any local changes are ignored and indicates the number of ignored changes. Select the indicator to open a list of these changes.|

## Dashboard

The team dashboard includes lists for tracking local changes and viewing the history of Team Development activities.

|List|Description|
|----|-----------|
|Local changes|Lists the local changes that haven’t been queued or ignored. See [Local change lists](c_NavigatingLocalChangeLists.md).|
|Pushes and Pulls|Provides a history of pushes and pulls. Expand a row to see the customized records for which versions were transferred as part of the push or pull. See [Pulling changes](c_PullsAndPushes.md) and [Pushing changes](pushing-changes.md).|
|Instance Comparisons|Provides a history of comparisons with other development instances. See [Compare to peer instances](../task/t_CompareToAPeerInstance.md).|
|Collisions|Lists the collisions that must be resolved before the next pull or push. You can select and hold \(or right-click\) a row and select **Resolve Collision**. See [Resolving Collisions](../task/t_ResolveACollision.md).|
|Ready to Push|Lists the local changes that have been queued for the next push. See [Queue a local change for a push](../task/t_QueueALocalChangeForAPush.md).|
|Ignored|Lists the local changes that are ignored for all pushes. See [Ignore a local change](../task/t_IgnoreALocalChange.md).|

