---
title: Exclude a table from cloning \(legacy\)
description: Exclude a table to create an empty but usable table on the target instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add exclusion, Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Exclude a table from cloning \(legacy\)

Exclude a table to create an empty but usable table on the target instance.

## Before you begin

Role required: clone\_admin

For information on excluding a table from cloning, see [General guidelines for excluding a table from cloning](../reference/clone-exclusions-guidelines.md).

## About this task

Data is removed during the exclusion substage before the node repoint. The data is removed before the instance becomes available to users.

## Procedure

1.  Navigate to **All** &gt; **Instance Clone** &gt; **Clone Definitions** &gt; **Exclude Tables**.

2.  Select **New**.

3.  Enter the table **Name**.

    **Note:** Entering a parent table results in the clone process also excluding its child tables. For example, excluding the task table would also exclude the Change, Incident, and Problem tables.

4.  Select **Submit**.


