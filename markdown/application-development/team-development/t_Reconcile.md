---
title: Reconcile changes
description: Reconciling changes compares the local instance to the parent instance. A report is generated of local changes and calculates the number of changes that are ready to pull from the parent.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Pushing changes, Working with changes, Team Development, Planning your application, Building applications]
---

# Reconcile changes

Reconciling changes compares the local instance to the parent instance. A report is generated of local changes and calculates the number of changes that are ready to pull from the parent.

## Before you begin

Role required: admin

## About this task

A reconcile occurs automatically whenever you select a parent instance. You can manually reconcile after an external disruptive event on the parent instance, such as a clone or failover.

**Note:** The duration of the process varies depending on the size and age of the instance.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, select **Reconcile**.

3.  In the confirmation dialog box, select **OK**.

    The list of local changes that haven’t been queued or ignored is recreated. If you had previously queued or ignored a local change, that designation is maintained.

4.  On the completion page, select **Show Results**.

    Review the instance comparison record.

    -   The On Remote and not Local related list shows the versions that are ready to pull from the parent.
    -   The On Local and not on Remote related list shows the local versions that are ready to queue or ignore.
5.  Select **Team Dashboard**.

6.  [Pull versions](t_PullAVersion.md) from the parent instance and then [resolve any collisions](t_ResolveACollision.md).

7.  Review the local changes list and [queue or ignore changes](t_QueueALocalChangeForAPush.md), as appropriate.


**Parent Topic:**[Pushing changes](../concept/pushing-changes.md)

