---
title: Schedule recurring clones
description: Schedule recurring clones to keep your cloned instances up to date.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Schedule recurring clones

Schedule recurring clones to keep your cloned instances up to date.

## Before you begin

Role required: clone\_admin

## About this task

Instead of manually cloning instances, you can schedule cloning that happens automatically. You create a cloning schedule in the same interface that you use to [create a clone](t_StartAClone.md#).

**Note:** The system limits the number of future clones you can schedule at once. The following are the maximum allowed scheduled clones by frequency:

-   Every 4 weeks: 7 occurrences
-   Every 2 weeks: 13 occurrences
-   Weekly: 25 occurrences

## Procedure

1.  Select **Clone Admin Console** &gt; **Request Clone**.

2.  Select your source instance and target instance for the clone.

3.  Select a clone profile.

4.  Select the calendar icon \(![](../image/clone-calendar.png)\).

5.  Select a time slot for your instance to be cloned.![The clone start time calendar.](../image/clone-schedule-calendar.png)

6.  Select **Schedule**.

7.  In the clone frequency option, select the frequency for your clone.

8.  Enter the total number of clones to occur.

9.  Finish filling out the request form and select **Continue**.


