---
title: General guidelines for excluding a table from cloning
description: A reference topic that includes general guidelines to exclude a table from cloning.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Clone, Configure core features, Administer]
---

# General guidelines for excluding a table from cloning

A reference topic that includes general guidelines to exclude a table from cloning.

-   **Workflow context data**

    Excluded workflow context data includes records stored in the wf\_context table, and in related tables with names starting with a prefix of wf\_. If workflow contexts were included, this process helps to prevent the occurrence of workflow timer syncing issues. Issues can occur due to the length of the cloning process.

-   **Excluding child tables of the task table**

    When excluding child tables of the task table, which use the [table per hierarchy extension model](../../platform-performance/concept/c_TaskTableFlattening.md), child tables are excluded. You don’t need to exclude the parent Task table together with the child table.

-   **Using wildcards**

    You can use wildcards to exclude several tables from cloning with one entry. For example, sys\_script.\* excludes all tables starting with sys\_script.

    **Note:** The wildcard has to include the dot '.' before the asterisk.

-   **Excluding or preserving related tables**

    To preserve or exclude related tables, you must preserve and exclude the following tables. If any of the tables are missed, the customer may not be able to log in to the instance after a clone.

    -   sys\_user
    -   sys\_user\_role
    -   sys\_user\_group
    -   sys\_user\_grmember
    -   sys\_group\_has\_role
    -   sys\_user\_role\_contains
    -   customer\_contact \(if the Customer Service Management plugin is active\)
-   **Tables that can't be excluded**

    sys\_db\_object and sys\_db\_object.\* can’t be added to the exclusions.


**Parent Topic:**[Instance Clone reference](instance-clone-reference.md)

