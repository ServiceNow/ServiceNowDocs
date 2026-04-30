---
title: Pull a version
description: Pulling retrieves versions of customized records from the parent instance and adds them on the development instance. Pulling does not retrieve any versions for changes made by system upgrades, but it retrieves all versions for changes made by users, not just the current version.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Team Development, Exploring Team Development, Team Development, Planning your application, Building applications]
---

# Pull a version

Pulling retrieves versions of customized records from the parent instance and adds them on the development instance. Pulling does not retrieve any versions for changes made by system upgrades, but it retrieves all versions for changes made by users, not just the current version.

## About this task

Pulling retrieves all versions for changes made by users that have not already be pulled onto the development instance, and you cannot choose which versions to pull. The first time you pull from a parent instance, the pull retrieves all versions for changes made by users. Subsequent pulls retrieve the new versions since your last pull. Each pull is recorded in the Push or Pull `[sys_sync_history]` table on the development instance. Historical versions are saved with a state of History.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Team Dashboard**.

2.  In the control panel, click **Pull**.

3.  On the completion page, click **Show Results**.

    The Push and Pull Versions related list for the Push or Pull form shows the customized records for which versions were retrieved and indicates if any pull exceptions exist.

    ![Pull history](../image/PullHistory.png)

4.  Resolve any collisions.


**Parent Topic:**[Team Development](../concept/c_TeamDevelopment.md)

