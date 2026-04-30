---
title: Exclude a table from cloning
description: Exclude a table to create an empty but usable table on the target instance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-09-10"
reading_time_minutes: 1
breadcrumb: [Request a clone, System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Exclude a table from cloning

Exclude a table to create an empty but usable table on the target instance.

## Before you begin

Role required: clone\_admin

## About this task

**Note:** When using Exclusions \(Exclude Tables\), the data is removed during the exclusion substage before the node repoint. The data is removed before the instance becomes available to users.

The **System Clone** &gt; **Exclude Tables** module lists the tables that aren’t copied during a system clone. On the clone request form, the option "Exclude tables specified in Exclusion List" is on by default. It verifies that the exclusions are processed during a clone. By default, the system excludes certain required tables such as logging, auditing, notifications, workflow contexts, and license usage.

**Note:** Excluded workflow context data includes records stored in the wf\_context table, and in related tables with names starting with a prefix of wf\_. This also includes the workflow scheduler table. This helps to prevent the occurrence of workflow timer syncing issues that might take place due to the length of the cloning process if workflow contexts were included.

`sys_db_object` and `sys_db_object.*` can’t be added to the exclusions.

When excluding child tables of the Task table, which use the [table per hierarchy extension model](../../platform-performance/concept/c_TaskTableFlattening.md), child tables are excluded. You don’t need to exclude the parent Task table together with the child table.

You can use wildcards to exclude several tables from cloning with one entry. For example, `sys_script.*` excludes all tables starting with sys\_script.

**Note:** The wildcard has to include the dot '.' before the asterisk.

To preserve the existing data on the target instance, see [Create a data preserver](../concept/data-preservation.md#). Data on tables that reference the table, such as business rules, isn’t excluded. To avoid unexpected results, we \(strongly\) advise against altering out-of-box preservers.

To preserve or exclude related tables, you must preserve and exclude all of the following tables. If any of the tables are missed, the customer may not be able to log in to the instance after a clone.

-   sys\_user
-   sys\_user\_role
-   sys\_user\_group
-   sys\_user\_grmember
-   sys\_group\_has\_role
-   sys\_user\_role\_contains
-   customer\_contact \(if the Customer Service Management plugin is active\)

## Procedure

1.  On the source instance, navigate to **System Clone** &gt; **Exclude Tables**.

2.  Select **New**.

3.  Enter the table **Name**.

4.  Select **Submit**.


