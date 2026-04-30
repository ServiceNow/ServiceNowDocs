---
title: Configure daily schedules for Walk-up Experience appointment booking
description: Define hours of operation and daily schedules for booking an appointment at your Walk-up Experience location.
locale: en-US
release: zurich
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Walk-up Experience appointment booking, Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# Configure daily schedules for Walk-up Experience appointment booking

Define hours of operation and daily schedules for booking an appointment at your Walk-up Experience location.

## Before you begin

Role required: appointment\_booking\_admin or admin

## About this task

Create a unique appointment booking schedule for each day of the week or for specific days of the week. For example, you can set the appointment booking availability schedule to run from 9:00am to 5:00pm, Monday, Wednesday, and Friday. The Tuesday and Thursday appointment availability schedule can run from 9:00am to 12:00pm. You can completely remove appointment booking for a specific day of the week, for example, Friday.

**Note:** To specify unique daily booking schedules, while using your associated appointment booking configuration, create new Schedule Entries to exclude the hours appointment booking is not available.

## Procedure

1.  Navigate to **All** &gt; **Walk-up Experience** &gt; **Administration** &gt; **Schedules**.

2.  Select the schedule you use, for example, the **8-5 weekdays excluding holidays** schedule.

3.  In the Schedule Entries related list, select **New**.

4.  Name the new record **Excludes** and fill in the form to create a unique daily booking schedule for Tuesday and Thursday appointments.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the record. For example, name the record **Excludes** to indicate the hours excluded from appointment booking.|
    |Type|Choose **Excluded** as the type.|
    |Show as|Choose **Busy** as the reason for the exclusion.|
    |When|Indicate the date to begin using this booking availability schedule. Also indicate the time to exclude booking availability for this date. For example, the hours of 12:00pm through 5:00pm.|
    |Repeats|Indicate the recurrence for this availability schedule. For example, **Weekly on Tue and Thu**.|
    |Repeat until|Specify how long you want this availability schedule to run by selecting an end date.|

    ![Schedule Entry Excludes form](../image/TuesdayThursdayExcluded.png)

5.  Select **Submit**.

6.  To verify that Tuesday and Thursday appointment booking is only available from 9:00am to 12:00am, navigate to your online Walk-up Check-in application.

    If configured for view, You can access the online Walk-up Check-in application from the **Service Portal Home** page or under **Self-Service** in the left navigation bar.

7.  Select the walk-up location for which you are verifying the schedule.

8.  Select **Schedule an appointment** and select a reason for the visit.

9.  Select a date for the appointment.

    The **Select Appointment** window displays the first available appointment, by week and day.

10. Determine that appointments are only available on Tuesdays and Thursdays from 9:00am to 12:00pm.

    ![Appointment selection choices](../image/SelectAnAppointment.png)


**Parent Topic:**[Configure Walk-up Experience appointment booking](../concept/walkup-appointment-booking-config.md)

