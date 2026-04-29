---
title: Configure daily schedules for Walk-up Experience service appointment booking
description: Specify different daily hours of operation for your Walk-up Experience location appointment booking.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Appointment booking configuration, Walk-up Experience appointment booking, Configure Walk-up Experience for Customer Service Management, Set up self-service, Configure, Customer Service Management]
---

# Configure daily schedules for Walk-up Experience service appointment booking

Specify different daily hours of operation for your Walk-up Experience location appointment booking.

## Before you begin

Role required: sn\_apptmnt\_booking.appointment\_booking\_admin

## About this task

Create a unique appointment booking schedule for each day of the week or for specific days of the week. For example, you can set the appointment booking availability schedule to run all day, from 9:00am to 5:00pm, Monday, Wednesday, and Friday. Tuesday and Thursday appointment availability schedule can run from 9:00am to 12:00pm. You can completely remove appointment booking for a specific day of the week, for example, Friday.

**Note:** To specify unique daily booking schedules, while using your associated appointment booking configuration, create new Schedule Entries to exclude the hours appointment booking is not available.

## Procedure

1.  To configure, for example, Tuesday and Thursday appointment availability schedule from 9:00am to 12:00pm, navigate to **Walk-up Experience** &gt; **Schedules**.

2.  Select the schedule you use, for example, the **8-5 weekdays excluding holidays** schedule.

3.  In the Schedule Entries related list, click **New** to display the Schedule Entry New record form.

4.  Name the new record **Excludes** and fill in the form to create a unique daily booking schedule for Tuesday and Thursday appointments.

    |Field|Description|
    |-----|-----------|
    |Name|Name the record. For example, name the record **Excludes** to indicate the hours excluded from appointment booking.|
    |Type|Choose **Excluded** as the type.|
    |Show as|Choose **Busy** as the reason for the exclusion.|
    |When|Indicate the date to begin using this booking availability schedule. Also indicate the time to exclude booking availability for this date. For example, the hours of 12:00pm through 5:00pm.|
    |Repeats|Indicate the recurrence for this availability schedule. For example, **Weekly on Tue and Thu**.|
    |Repeat until|Specify how long you want this availability schedule to run by selecting an end date.|

    ![Schedule Entry record displaying different configuration fields to create a schedule entry that occurs weekly on Tuesdays and Thursdays.](../image/TuesdayThursdayExcluded.png)

5.  Click **Submit**.

6.  To verify that Tuesday and Thursday appointment booking is only available from 9:00am to 12:00am, navigate to your online Walk-up Check-in application.

    If configured for view, You can access the online Walk-up Check-in application from the **Service Portal Home** page or under **Self-Service** in the left navigation bar.

7.  Select the walk-up location for which you are verifying the schedule.

8.  Click **Schedule an appointment** and select a reason for the visit.

9.  Select a date for the appointment.

    The **Select Appointment** window displays the first available appointment, by week and day.

10. Determine that appointments are only available on Tuesdays and Thursdays from 9:00am to 12:00pm.

    ![Appointment page displaying a calendar with available slots to schedule a service appointment.](../image/SelectAnAppointment.png)


