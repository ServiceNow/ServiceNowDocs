---
title: Set the starting day of the week on the appointment booking calendar
description: Customize the starting day of the week on your appointment booking calendar to match your organization's scheduling preferences. By default, the calendar week starts on Sunday, but you can easily set it to any day \(e.g., Monday\) or revert it if needed.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Set the starting day of the week on the appointment booking calendar

Customize the starting day of the week on your appointment booking calendar to match your organization's scheduling preferences. By default, the calendar week starts on Sunday, but you can easily set it to any day \(e.g., Monday\) or revert it if needed.

## Before you begin

Role required: appointment\_booking\_admin

## Procedure

1.  Navigate to **All** and search for `sys_properties.list`.

2.  Search for the property `glide.ui.date_picker.first_day_of_week`.

3.  Choose one of the following:

    -   If the property already exists, select it to edit.
    -   If the property doesn't exist, create it.

        1.  Select **New**.

        2.  Enter `glide.ui.date_picker.first_day_of_week` in the **Name** field.

        3.  Set **Type** to **Integer**.

4.  In the **Value** field, enter the integer that corresponds to your desired starting day.

    |Value|Day of the week|
    |-----|---------------|
    |1|Sunday|
    |2|Monday|
    |3|Tuesday|
    |4|Wednesday|
    |5|Thursday|
    |6|Friday|
    |7|Saturday|

    For example, to start your calendar week on Monday, enter 2.

5.  Select **Submit**.


## Result

The appointment booking calendar displays your selected starting day of the week.

