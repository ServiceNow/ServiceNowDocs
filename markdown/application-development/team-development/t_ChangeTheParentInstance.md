---
title: Change the parent instance
description: If it becomes necessary to modify the instance hierarchy, you can change the parent for a development instance.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Team Development, Exploring Team Development, Team Development, Planning your application, Building applications]
---

# Change the parent instance

If it becomes necessary to modify the instance hierarchy, you can change the parent for a development instance.

## About this task

Changing the parent initiates a complete comparison between the development instance and the new parent instance. To optimize comparison speed and reduce the number of collisions and local changes that need review afterwards, ensure that the new parent instance was cloned recently from an appropriate instance \(for example, the production instance\). Before you change the parent instance, ensure that the change does not conflict with your change management process or other development efforts.

To change the parent for a development instance:

## Procedure

1.  On the development instance, navigate to **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, click **Change**.

3.  Select the remote instance you want to use as the parent and click **Select**.

    Alternatively, click the link to [define a new remote instance](t_DefineARemoteInstance.md). Then, repeat steps 1–3 and select the remote instance you defined.

    ![Parent instance](../image/ParentInstance.png)

    The system initiates a reconcile, which compares the local instance to the parent, and then generates the list of local changes and calculates the number of changes that are ready to pull from the parent.

4.  On the completion page, click **Team Dashboard**.

5.  [Pull versions](t_PullAVersion.md) from the parent instance and [resolve any collisions](t_ResolveACollision.md).

6.  Review the local changes list and [queue or ignore changes](t_QueueALocalChangeForAPush.md), as appropriate.


**Parent Topic:**[Team Development](../concept/c_TeamDevelopment.md)

