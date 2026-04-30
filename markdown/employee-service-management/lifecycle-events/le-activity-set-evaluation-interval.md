---
title: Change the evaluation interval default wait time
description: As an administrator, you can change the default time that an activity set waits before the activity set is evaluated.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Lifecycle Events evaluation interval, Configure a lifecycle event, Building a lifecycle event, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# Change the evaluation interval default wait time

As an administrator, you can change the default time that an activity set waits before the activity set is evaluated.

## Before you begin

Role required: admin

## About this task

Starting in the Utah family, the default evaluation interval can be changed.

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Manage Lifecycle Events**.

2.  Select a lifecycle event.

3.  Select the **Activity Sets** tab.

4.  Select the edit icon for an **Activity Set**.

    **Note:** In Journeys, stages are equivalent to activity sets.

5.  Select **Configure** &gt; **All** from the **Additional actions** list.

6.  Select the **Dictionary Entries** tab.

7.  Find **evaluation\_interval** **Column name**.

8.  Open the related **Dictionary Entry**.

    **Note:** To edit this record, you must be in the Human Resources: Lifecycle Enterprise application.

9.  Select the **Default Value** tab.

    **Default value** format `0 04:00:00` is equal to `d hh:mm:ss`:

    -   Days = d
    -   Hours = hh
    -   Minutes = mm
    -   Seconds = ss
10. Change the **Default value**.

11. Select **Update**.


**Parent Topic:**[Lifecycle Events evaluation interval](../concept/le-evaluation-interval1.md)

