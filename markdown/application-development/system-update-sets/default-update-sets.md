---
title: Default update set
description: Only one update set can be the default set for any application scope.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, System update sets, Deploying applications, Building applications]
---

# Default update set

Only one update set can be the default set for any application scope.

## Global default set

Use the global default update set to change an instance without adding the changes to any user-created update sets. The global default update set is the set where the default set is `true` and the application scope is global. The global default set provides system functionality and shouldn’t be changed, deleted, or moved between systems. Use the global update set to change an instance without adding the changes to any user-created update sets.

**Note:** The system sets the default set to `false` for all other update sets with the same scope. This ensures that there’s only one default update set for each scope.

## Auto-generated default set

Common cases where the system auto-generates a default update set are as follows.

-   The first time that an admin logs in, the system sets the system’s global default update set as the administrator’s update set. In addition, the application picker sets the administrator’s application scope to global.

    If a global default update set is marked **Ignored** or **Completed**, the system creates an update set for the global application scope and performs the following actions:

    -   The system sets the default set to `true` for the new set.
    -   The system sets the name of the new set to start with the name of the former default set and appends the next numeral.
    -   The system sets the newly created set as the administrator’s update set.
-   When a user marks the default set for a scope as **Ignored** or **Completed**, the system immediately auto-generates a new default set for the scope.
-   The system auto-generates a new default update set for a scope when all the following conditions occur:
    -   You change the application scope.
    -   Your preferred update set is **Complete** or **Ignored**.
    -   There’s no In-Progress default update set for the new scope.

**Parent Topic:**[Update sets reference](update-sets-reference.md)

