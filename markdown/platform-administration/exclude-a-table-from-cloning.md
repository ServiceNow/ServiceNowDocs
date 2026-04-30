---
title: Exclude a table from cloning
description: Exclude a table to create an empty but usable table on the target instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-30"
reading_time_minutes: 1
breadcrumb: [Configure, Instance Clone, Configure core features, Administer]
---

# Exclude a table from cloning

Exclude a table to create an empty but usable table on the target instance.

## Before you begin

Role required: clone\_admin

For information on excluding a table from cloning, see [General guidelines for excluding a table from cloning](../reference/clone-exclusions-guidelines.md).

## About this task

Data is removed during the exclusion substage before the node repoint. The data is removed before the instance becomes available to users.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Select the Definitions tab.

3.  Select Exclusions.

4.  Select **New**.

5.  Enter the table **Name**.

6.  Select **Save**.


