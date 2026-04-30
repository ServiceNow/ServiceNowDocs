---
title: Change the parent instance
description: Change the parent for a development instance to modify the instance hierarchy.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-09-23"
reading_time_minutes: 1
breadcrumb: [Building an instance hierarchy, Configure, Team Development, Planning your application, Building applications]
---

# Change the parent instance

Change the parent for a development instance to modify the instance hierarchy.

## Before you begin

Role required: admin

## About this task

Changing the parent initiates a complete comparison between the development instance and the new parent instance. Confirm that the new parent instance was cloned recently from an appropriate instance. Verification optimizes comparison speed and reduces the number of collisions and local changes that need review after. Before you change the parent instance, confirm that the change doesn’t conflict with your change management process or other development efforts.

## Procedure

1.  On the development instance, navigate to **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, select **Change**.

3.  Select the remote instance that you want to use as the parent and select **Select**.

    Alternatively, select the link to [define a new remote instance](t_DefineARemoteInstance.md). Then, repeat steps 1–3 and select the remote instance you defined.

    The system initiates a reconcile, which compares the local instance to the parent. A list of local changes is generated and the number of changes are calculated that are ready to pull from the parent.

4.  On the completion page, select **Team Dashboard**.

5.  [Pull versions](t_PullAVersion.md) from the parent instance and [resolve any collisions](t_ResolveACollision.md).

6.  Review the local changes list and [queue or ignore changes](t_QueueALocalChangeForAPush.md), as appropriate.


**Parent Topic:**[Building an instance hierarchy](../concept/c_InstanceHierarchies.md)

