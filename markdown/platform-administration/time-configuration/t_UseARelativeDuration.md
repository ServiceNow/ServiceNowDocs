---
title: Use a relative duration
description: When you define an SLA, you can set the Duration type to be a relative duration.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Time configuration, Configure core features, Administer]
---

# Use a relative duration

When you define an SLA, you can set the **Duration type** to be a relative duration.

## Before you begin

Role required: admin

## About this task

When using relative durations, you can also use the **Relative duration works on** field. It calculates against the SLA record, or the task record that the SLA record is used for.

This example demonstrates how a relative duration of End of next business day works.

## Procedure

1.  Create an SLA that has a relative duration of **End of next business day**.

2.  Complete the rest of the fields of this SLA with the values as shown, also setting a Timezone if you want.

    ![Relative Duration in an SLA](../image/SLARelativeDuration.png)

3.  To show how this Relative Duration works, create a new incident.

    The SLA starts for this incident. In the **Task SLAs** related list, if you look at the **Business time left** and **Start time** fields, notice that the time left is until the next business day at 5pm.

    **Note:** Pause conditions are not compatible with Relative Durations.


**Parent Topic:**[Using time configuration](../using-time-configuration.md)

