---
title: Exclude a table from cloning \(legacy\)
description: Exclude a table on the target instance from being overwritten from the source instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-30"
reading_time_minutes: 1
breadcrumb: [Add exclusion, Configure, Instance Clone, Configure core features, Administer]
---

# Exclude a table from cloning \(legacy\)

Exclude a table on the target instance from being overwritten from the source instance.

## Before you begin

Role required: clone\_admin

For information on excluding a table from cloning, see [General guidelines for excluding a table from cloning](../reference/clone-exclusions-guidelines.md).

## About this task

## Procedure

1.  On the source instance, navigate to **Instance Clone** &gt; **Clone Definitions** &gt; **Exclude Tables**.

2.  Select **New**.

3.  Enter the table **Name**.

    **Note:** Entering a parent table results in the clone process also excluding its child tables. For example, excluding the task table would also exclude the Change, Incident, and Problem tables.

4.  Select **Submit**.


