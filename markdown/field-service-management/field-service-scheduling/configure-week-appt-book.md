---
title: Change the day of the week that the appointment booking calendar starts on
description: You can make the appointment booking calendar start on a day other than Sunday, the default. If the start day of the week was changed, you can also change the start of the week back to Sunday.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Change the day of the week that the appointment booking calendar starts on

You can make the appointment booking calendar start on a day other than Sunday, the default. If the start day of the week was changed, you can also change the start of the week back to Sunday.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and search for `sys_properties.list`.

2.  Search for the property `glide.ui.date_picker.first_day_of_week`.

3.  Choose one of the following:

    -   If the property exists, select it.
    -   If the property doesn't exist, select **New**, for name enter `glide.ui.date_picker.first_day_of_week`, and for **Type** select **Integer**.
4.  Enter in the **Value** field the integer that corresponds to the day of the week you want the calendar to start on.

    |Value|Corresponding day|
    |-----|-----------------|
    |1|Sunday|
    |2|Monday|
    |3|Tuesday|
    |4|Wednesday|
    |5|Thursday|
    |6|Friday|
    |7|Saturday|

5.  Select **Submit**.


**Parent Topic:**[Configuring Appointment Booking](../concept/appointment-booking-administer.md)

