---
title: Default update set
description: Only one update set can be the default set for any application scope.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, System update sets, Deploying applications, Building applications]
---

# Default update set

Only one update set can be the default set for any application scope.

To set an update set to be the default set, you set the **Default set** field to true. When you set Default set = true, the following actions occur:

-   The update set becomes the default update set for its scope.
-   The system sets Default set = false for all other update sets with the same scope. This ensures that there is only one default update set for each scope.

## Global default set

Use the global default update set to make changes to an instance without adding the changes to any user-created update sets. The global default update set is the set where Default set = true and application scope is global. The global default set \(regardless of the Name of the set\) provides system functionality and should not be changed, deleted, or moved between systems. Use this update set to make changes to an instance without adding the changes to any user-created update sets.

## Auto-generated default set

At all times, to ensure that no updates to an instance are lost, the system ensures that there is a default set for the user’s current scope. If the system finds that a default update set does not exist \(or is marked **Ignored** or **Completed**\) for the current scope, then the system auto-generates an update set and sets **Default set = true**.

These are some common cases where the system auto-generates a default update set.

-   The very first time that an admin logs in, the system sets the system’s global default update set as the administrator’s update set. In addition, the application picker sets the administrator’s application scope to global.

    If a global default update set does not exist \(or is marked **Ignored** or **Completed**\), the system creates a new update set for the global application scope and performs the following actions:

    -   The system sets Default set = true for the new set.
    -   The system sets the name of the new set to start with the name of the former default set and appends the next numeral \(in the sequence SetName, SetName 1, SetName 2, …, SetName n\).
    -   The system sets the newly created set as the administrator’s update set.
-   When a user marks the default set for a scope as **Ignored** or **Completed** \(not a recommended practice\), the system immediately auto-generates a new default set for the scope.
-   The system auto-generates a new default update set for a scope when all the following conditions occur:
    -   You change application scope.
    -   Your preferred update set is **Complete** or **Ignored**.
    -   There is no In-Progress default update set for the new scope.

