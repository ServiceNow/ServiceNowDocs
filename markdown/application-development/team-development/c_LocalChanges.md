---
title: Local changes
description: The Local Changes table tracks customized records that have current versions on the development instance, but not on the parent instance.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Team Development, Planning your application, Building applications]
---

# Local changes

The Local Changes table tracks customized records that have current versions on the development instance, but not on the parent instance.

You can queue local changes in preparation for a push to the parent instance.

Each development instance maintains a single queue, regardless of who develops or queues the changes. You can ignore local changes that you don’t want to push. For example, you can ignore changes to the color scheme that visually distinguish a development instance from the production instance. You can remove a change from the queue or stop ignoring a change.

Changing the parent instance or reconciling recreates the list of local changes that haven’t been queued or ignored. If you had previously queued or ignored a local change, that designation is maintained.

|Action|Result|
|------|------|
|Ignore a record that has a version queued for push|The queued change is deleted|
|Ignore a record that has a version queued for code review|The queued change is deleted|
|Pull changes for an ignored record|Collision|
|Resolve a collision by taking the parent version|There’s no longer a local change to ignore|
|Resolve a collision by keeping the local version|The ignored change remains on the local instance|

-   **[Pulling changes](c_PullsAndPushes.md)**  
Developers synchronize their instances to the parent instance by pulling and pushing versions of customized records.
-   **[Pushing changes](pushing-changes.md)**  
You can push versions of customized records to synchronize your instance to the parent instance.
-   **[Back out a local change](../task/t_BackOutALocalChange.md)**  
Back out all local changes and restore the last version reconciled with the parent instance.
-   **[Ignore a local change](../task/t_IgnoreALocalChange.md)**  
Ignoring a local change helps to prevent a record from generating new versions in the Local Changes list.

**Parent Topic:**[Planning your application](../../custom-application/concept/planning-applications.md)

