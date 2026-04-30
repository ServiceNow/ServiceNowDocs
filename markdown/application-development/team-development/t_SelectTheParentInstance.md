---
title: Select the parent instance
description: An instance can have multiple peer instances but only one parent instance.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Team Development setup, Configuring Team Development, Team Development, Planning your application, Building applications]
---

# Select the parent instance

An instance can have multiple peer instances but only one parent instance.

## About this task

The parent instance is the only instance you can pull changes from and push changes to.

The parent instance must be on the same release family as the local instance. For example, a development instance on the Geneva release family must have a parent instance also on the Geneva release family. If you select a parent from a different release family, the Team Development dashboard displays an error message and prevents you from pulling changes and reconciling. If you select a parent from a different patch release, the dashboard displays a warning message but allows you to pull changes and reconcile.

Do not use Team Development with production or test instances.

-   Do not use a test or production instance as the parent instance in Team Development.
-   Do not make any instance the parent of a production instance.
-   Production instances should never have a parent.

When you back out a change on a Team Development instance, it backs out the change all the way back down the chain, including undoing the work on the source instance. This behavior can cause major problems on test and production instances.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, click the appropriate link:

    |Option|Description|
    |------|-----------|
    |Use &lt;instance name and URL&gt;|Selects the most recently defined remote instance as the parent instance.|
    |Select a different instance|Opens a dialog box where you can select another remote instance or define a new remote instance.|
    |Register a new instance or List all remote instances|Opens the remote instance form or list, where you can define a new remote instance. These options are available when no remote instances are defined.|

    ![Parent instance](../image/ParentInstance.png)

3.  If you defined a new remote instance in step 2, repeat [step 1](t_SelectTheParentInstance.md#step-1-navigate-team-dashboard) through [step 2](t_SelectTheParentInstance.md#step-2-click-link) and select the remote instance you defined.

    The system initiates a reconcile, which compares the local instance to the parent. It then generates the list of local changes and calculates the number of changes that are ready to pull from the parent. The reconcile also validates the instance versions.

4.  Pull all changes from the parent instance if both instances are in the same release family.

    **Note:** The parent instance is saved in theglide.apps.hub.current system property.


