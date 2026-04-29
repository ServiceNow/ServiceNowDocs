---
title: Define a relative duration
description: Define relative durations to calculate duration time for SLAs based on business schedules and specific time requirements.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Use, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a relative duration

Define relative durations to calculate duration time for SLAs based on business schedules and specific time requirements.

## Before you begin

Role required: admin

## About this task

Relative durations calculate time periods based on business schedules. You can customize existing relative durations or create new ones to meet specific SLA requirements.

## Procedure

1.  Navigate to **System Scheduler** &gt; **Relative Durations**.

    Four base relative durations are available:

    -   Two business days by 4pm
    -   Three business days by 4pm
    -   Next business day by 4pm
    -   End of next business day
    **Note:** The business schedule you use defines business day durations. If you define no schedule, durations default to 24 x 7.

2.  Select a relative duration to view or modify its configuration.

3.  Customize the script variables and logic as needed for your requirements.


## Example

The **End of next business day** relative duration shows how to configure a basic calculation. The *days* variable is set to one because the result should land one day in the future. You can customize the end time \(currently set to 5pm\) in the script.

![End of Next Business Day Relative Duration](../image/EndOfNextBusDay.png)

The **2 business days by 4pm** relative duration demonstrates conditional logic. The script includes an if-statement that checks whether the calculated time is after 10am. If it is, an extra day is added to the calculation. Therefore, the description reads `2 business days by 4pm if before 10am`.

![2 Business Days by 4 pm Relative Duration](../image/TwoBusDays.png)

The end time of 17:00 is hard-coded into the relative duration script and is not related to the associated schedule. To change the end time from 5pm, modify the script directly.

**Parent Topic:**[Using time configuration](../using-time-configuration.md)

