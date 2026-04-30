---
title: Cancel clone schedules \(legacy\)
description: Scheduled clones aren't able to be modified, you must cancel scheduled clones and make a new clone schedule.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Schedule recurring clones \(legacy\), Manage, Instance Clone, Configure core features, Administer]
---

# Cancel clone schedules \(legacy\)

Scheduled clones aren't able to be modified, you must cancel scheduled clones and make a new clone schedule.

## Before you begin

Role required: clone\_admin

## About this task

This topic assumes that you have a [Schedule recurring clones \(legacy\)](schedule-cloning.md) that you want to modify.

## Procedure

1.  Select **Instance Clone** &gt; **Active Clones** &gt; **&lt;one-of-your-clones&gt;**.

2.  In the **Related Links**, select **Cancel Clone**.

    Clones can only be canceled up to Node Repoint stage. The clone can be rolled back once it completes.

    The system stops any current cloning activities and sets the **State** to **Canceled**.


**Parent Topic:**[Schedule recurring clones \(legacy\)](schedule-cloning.md)

