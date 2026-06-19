---
title: Reconcile changes
description: Reconciling first compares the local instance to the parent, and then generates the list of local changes and calculates the number of changes that are ready to pull from the parent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/team-development/t\_Reconcile.html
release: australia
product: Team Development
classification: team-development
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Team Development, Planning your application, Building applications]
---

# Reconcile changes

Reconciling first compares the local instance to the parent, and then generates the list of local changes and calculates the number of changes that are ready to pull from the parent.

## Before you begin

Role required: none.

## About this task

A reconcile occurs automatically whenever you select a parent instance. You may need to manually reconcile after an external disruptive event on the parent instance, such as a clone or failover.

**Note:** This process may take a while to complete depending on the size and age of the instance.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, click **Reconcile**.

3.  In the confirmation dialog box, click **OK**.

    The list of local changes that have not been queued or ignored is recreated. If you had previously queued or ignored a local change, that designation is maintained.

4.  On the completion page, click **Show Results**.

    Review the instance comparison record.

    -   The On Remote and not Local related list shows the versions that are ready to pull from the parent.
    -   The On Local and not on Remote related list shows the local versions that are ready to queue or ignore.
    \[Omitted image "Reconcile.png"\] Alt text: Reconcile

5.  Click **Team Dashboard**.

6.  [Pull versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/team-development/t_PullAVersion.md) from the parent instance and then [resolve any collisions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/team-development/t_ResolveACollision.md).

7.  Review the local changes list and [queue or ignore changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/team-development/t_QueueALocalChangeForAPush.md), as appropriate.


