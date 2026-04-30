---
title: Team Development overview
description: Team Development allows developers to work on separate development instances while sharing code and resolving collisions throughout the development process.
locale: en-US
release: xanadu
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Team Development, Planning your application, Building applications]
---

# Team Development overview

Team Development allows developers to work on separate development instances while sharing code and resolving collisions throughout the development process.

After setting up the instance hierarchy, you can develop changes on your local development instance. Use the team dashboard to manage Team Development activities, such as:

-   Tracking local changes and determining which changes to promote to the parent development instance.
-   Pulling changes from the parent instance and resolving any collisions with local changes.
-   Comparing your instance with other development instances and resolving any collisions with other development projects.
-   Pushing changes when a feature is tested and ready to promote to the parent development instance.

Developers with admin access to their development instance and the parent instance can use team development. For alternative access settings, see [Granting access rights to developers](../reference/r_GrantingAccessRightsToDevelopers.md).

-   **[When to use Team Development](../reference/r_WhenToUseTeamDevelopment.md)**  
Team Development allows multiple developers to work on applications.
-   **[Local changes](c_LocalChanges.md)**  
The Local Changes table tracks which customized records have current versions that exist on the development instance but not on the parent instance.
-   **[Local change lists](c_NavigatingLocalChangeLists.md)**  
On the team dashboard, the Local Changes list shows the local changes that have not been queued for the next push or ignored for all pushes.
-   **[Pull exceptions](../reference/r_PullExceptions.md)**  
Pulling ignores versions when certain conditions occur.
-   **[Team dashboard](../reference/r_TeamDashboard.md)**  
The team dashboard provides a central place to manage all Team Development activities on your development instance.
-   **[Approve or reject a push](../task/t_ApproveOrRejectAPush.md)**  
Code reviewers must approve or reject a push from the Team Development application.
-   **[Back out a local change](../task/t_BackOutALocalChange.md)**  
Back out all local changes and restore the last version reconciled with the parent instance.
-   **[Cancel a code review request](../task/t_CancelACodeReviewRequest.md)**  
Developers can cancel any push they submitted that is in the Awaiting Code Review stage.
-   **[Change the parent instance](../task/t_ChangeTheParentInstance.md)**  
If it becomes necessary to modify the instance hierarchy, you can change the parent for a development instance.
-   **[Check the review status of a pushed change](../task/t_CheckReviewStatusOfAPushedChange.md)**  
If the parent instance requires pushed changes to undergo code review, changes are placed in the Awaiting Code Review stage.
-   **[Compare a pushed version to a local version](../task/t_ComparePushedVerLocalVer.md)**  
Code reviewers can compare the pushed versions to the local versions to see the potential effect of incoming changes.
-   **[Compare to peer instances](../task/t_CompareToAPeerInstance.md)**  
You can compare the local instance to any other remote instance and commit any current versions from the remote instance on your development instance.
-   **[Ignore a local change](../task/t_IgnoreALocalChange.md)**  
Ignoring a local change prevents updates to a record from generating new versions in the Local Changes list.
-   **[Pull a version](../task/t_PullAVersion.md)**  
Pulling retrieves versions of customized records from the parent instance and adds them on the development instance. Pulling does not retrieve any versions for changes made by system upgrades, but it retrieves all versions for changes made by users, not just the current version.
-   **[Push a version](../task/t_PushAVersion.md)**  
Pushing promotes changes from the development instance to the parent instance and commits the current version of a customized record on the development instance as the current version on the parent instance.
-   **[Back out a push](../task/t_BackOutAPush.md)**  
Application developers can back out a push to remove unwanted changes.
-   **[Queue a local change for a push](../task/t_QueueALocalChangeForAPush.md)**  
Application developers can queue a local change for a push to ensure the changes are available to other developers.
-   **[Reconcile changes](../task/t_Reconcile.md)**  
Reconciling first compares the local instance to the parent, and then generates the list of local changes and calculates the number of changes that are ready to pull from the parent.
-   **[Resolve a collision in Team Development](../task/t_ResolveACollision.md)**  
A collision is detected when the pulled version and the current local version are modifications of a different version, indicating that someone else has modified the same record that you have modified. The team dashboard displays the number of collisions between the local and the parent instance.
-   **[Limitations on updating records](../reference/r_LimitationsOnResolvingCollisions.md)**  
There are some types of records that you cannot merge while resolving differences on the Compare to Current and Resolve Collision pages.
-   **[Resolve multiple collisions](../task/t_ResolveMultipleCollisions.md)**  
You can resolve multiple collisions without reviewing the differences between the local and pulled versions.

**Parent Topic:**[Team Development](c_TeamDevelopment.md)

**Related topics**  


[Set up an instance hierarchy](../task/t_SetUpAnInstanceHierarchy.md)

