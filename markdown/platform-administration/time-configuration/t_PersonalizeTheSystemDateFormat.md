---
title: Personalize the system date format
description: You can personalize the format in which date values appear in your instance.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Global date and time field format, Date and Date/Time fields, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Personalize the system date format

You can personalize the format in which date values appear in your instance.

## About this task

Personalizing the date format does not change global settings or impact the way other users see date values.

**Note:** It is recommended that you use a `yyyy` format-based date. For example, use `mm-dd-yyyy`, `yyyy-mm-dd`, or `dd-mm-yyyy`.

-   If your system date format is set to use the `yy` year format, the system considers dates 20 years later or 80 years earlier from the current date as a date in the past or future leading to an unexpected behavior.
-   For example, if you set the year as `51` for 2051, the system considers the year as 1951. Similarly, if you set the year as `37` for 1937, the system considers the year as 2037.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Profile**.

2.  In the **Date format** field, select an option.

3.  Click **Update**.


**Parent Topic:**[Global date and time field format](../reference/r_FormatDateAndTimeFields.md)

**Related topics**  


[Personalize the system time format](t_PersonalizeTheSystemTimeFormat.md)

