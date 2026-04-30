---
title: Select the parent instance
description: An instance can have multiple peer instances but only one parent instance.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-09-23"
reading_time_minutes: 1
breadcrumb: [Building an instance hierarchy, Configure, Team Development, Planning your application, Building applications]
---

# Select the parent instance

An instance can have multiple peer instances but only one parent instance.

## Before you begin

Role required: admin

## About this task

The parent instance is the only instance that you can pull changes from and push changes to.

The parent instance must be on the same release family as the local instance. If you select a parent from a different release family, the Team Development dashboard displays an error message and helps to prevent you from pulling changes and reconciling. If you select a parent from a different patch release, the dashboard displays a warning message but enables you to pull changes and reconcile.

Don’t use Team Development with production or test instances. When you back out a change on a Team Development instance, the work on the source instance is also undone. This behavior can cause major problems on test and production instances.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, select the appropriate link:

    |Option|Description|
    |------|-----------|
    |Use &lt;instance name and URL&gt;|Selects the most recently defined remote instance as the parent instance.|
    |Select a different instance|Opens a dialog box where you can select another remote instance or define a new remote instance.|
    |Register a new instance or List all remote instances|Opens the remote instance form or list, where you can define a new remote instance. These options are available when no remote instances are defined.|

3.  If you defined a new remote instance in step 2, repeat the steps and select the remote instance you defined.

    The system initiates a reconcile, which compares the local instance to the parent. It then generates the list of local changes and calculates the number of changes that are ready to pull from the parent. The reconcile also validates the instance versions.

4.  Pull all changes from the parent instance if both instances are in the same release family.

    **Note:** The parent instance is saved in the glide.apps.hub.current system property.


**Parent Topic:**[Building an instance hierarchy](../concept/c_InstanceHierarchies.md)

