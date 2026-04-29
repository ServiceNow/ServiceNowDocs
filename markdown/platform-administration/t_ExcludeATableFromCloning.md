---
title: Exclude a table from cloning
description: Exclude a table to create an empty but usable table on the target instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Exclude a table from cloning

Exclude a table to create an empty but usable table on the target instance.

## Before you begin

Role required: clone\_admin

For information on excluding a table from cloning, see [General guidelines for excluding a table from cloning](../reference/clone-exclusions-guidelines.md).

## About this task

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Select the **Definitions** tab.

3.  Select **Exclusions**.

4.  Select **New**.

5.  Enter the table **Name**.

    **Note:** Entering a parent table results in the clone process also excluding its child tables. For example, excluding the task table would also exclude the Change, Incident, and Problem tables.

6.  Select **Save**.


