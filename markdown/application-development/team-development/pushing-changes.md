---
title: Pushing changes
description: You can push versions of customized records to synchronize your instance to the parent instance.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-09-11"
reading_time_minutes: 2
breadcrumb: [Working with changes, Team Development, Planning your application, Building applications]
---

# Pushing changes

You can push versions of customized records to synchronize your instance to the parent instance.

Developers should consider the following when preparing to push changes.

-   Push changes when a feature is tested and ready to promote to the parent development instance.
-   Pushing changes to the parent instance only adds the current development version. Changes to previous development versions aren't pushed.
-   Pushing changes creates a local update set on the parent instance that is marked as complete.
-   Transfer the update set or push to move the local changes through your development and test hierarchy.
-   Customize which changes to push to the parent instance.
-   Pushed versions are also tracked as local changes on the parent instances.

## Workflow when pushing changes

1.  [Queue a local change for a push](../task/t_QueueALocalChangeForAPush.md)

    Application developers can queue a local change for a push to confirm the changes are available to other developers.

2.  [Push a version](../task/t_PushAVersion.md)

    Pushing promotes changes from the development instance to the parent instance.

3.  [Code reviews](c_CodeReview.md)

    Team Development administrators can require that pushes undergo code review before accepting pushes.

4.  [Approve or reject a push](../task/t_ApproveOrRejectAPush.md)

    Code reviewers must approve or reject a push from the Team Development application.

5.  [Check the review status of a pushed change](../task/t_CheckReviewStatusOfAPushedChange.md)

    If the parent instance requires pushed changes to undergo code review, changes are placed in the Awaiting Code Review stage.

6.  [Compare a pushed version to a local version](../task/t_ComparePushedVerLocalVer.md)

    Code reviewers can compare the pushed versions to the local versions to see the potential effect of incoming changes.

7.  [Back out a push](../task/t_BackOutAPush.md)

    Application developers can back out a push to remove unwanted changes.


-   **[Queue a local change for a push](../task/t_QueueALocalChangeForAPush.md)**  
Application developers can queue a local change for a push to confirm that the changes are available to other developers.
-   **[Push a version](../task/t_PushAVersion.md)**  
You can push a version from the development instance to the parent instance.
-   **[Code reviews](c_CodeReview.md)**  
Team Development administrators can require that pushes undergo code review before accepting pushes.
-   **[Approve or reject a push](../task/t_ApproveOrRejectAPush.md)**  
Code reviewers must approve or reject a push from the Team Development application.
-   **[Check the review status of a pushed change](../task/t_CheckReviewStatusOfAPushedChange.md)**  
If the parent instance requires pushed changes to be sent to code review, changes are placed in the Awaiting Code Review stage.
-   **[Back out a push](../task/t_BackOutAPush.md)**  
Application developers can back out a push to remove unwanted changes.
-   **[Compare a pushed version to a local version](../task/t_ComparePushedVerLocalVer.md)**  
Code reviewers can compare the pushed versions to the local versions to see the potential effect of incoming changes.
-   **[Reconcile changes](../task/t_Reconcile.md)**  
Reconciling changes compares the local instance to the parent instance. A report is generated of local changes and calculates the number of changes that are ready to pull from the parent.

**Parent Topic:**[Local changes](c_LocalChanges.md)

