---
title: Pull a version
description: Pulling retrieves versions of customized records from the parent instance and adds them on the development instance. Pulling doesn’t retrieve any versions for changes made by system upgrades.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Pulling changes, Working with changes, Team Development, Planning your application, Building applications]
---

# Pull a version

Pulling retrieves versions of customized records from the parent instance and adds them on the development instance. Pulling doesn’t retrieve any versions for changes made by system upgrades.

## Before you begin

Role required: developer

## About this task

The first time you pull from a parent instance, the pull retrieves all versions for changes made by developers. Additional pulls retrieve the newest version.

Each pull is recorded in the Push or Pull `[sys_sync_history]` table on the development instance. Historical versions are saved with a state of History.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, select **Pull**.

3.  On the completion page, select **Show Results**.

    The Push and Pull Versions related list for the Push or Pull form shows the customized records for which versions were retrieved. If any pull exceptions exist, they’re displayed.

4.  Resolve any collisions, see [Resolving collisions](../concept/resolving-collisions.md).

    Pulling ignores versions when certain conditions occur. See [Pull exceptions](../reference/r_PullExceptions.md) for a list of exceptions.


**Parent Topic:**[Pulling changes](../concept/c_PullsAndPushes.md)

