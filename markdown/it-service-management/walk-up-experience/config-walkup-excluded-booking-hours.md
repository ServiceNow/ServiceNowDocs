---
title: Configure excluded hours for Walk-up Experience appointment booking
description: Using the Appointment Booking application, you can specify excluded appointment hours in the schedule for your Walk-up Experience location.
locale: en-US
release: yokohama
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure Walk-up Experience appointment booking, Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# Configure excluded hours for Walk-up Experience appointment booking

Using the **Appointment Booking** application, you can specify excluded appointment hours in the schedule for your Walk-up Experience location.

## Before you begin

Role required: appointment\_booking\_admin or admin

## About this task

Configure your Walk-up Experience location to exclude certain hours of operation from users scheduling appointments. For example, you can set the appointment booking availability schedule to run from 8:00 a.m. to 5:00 p.m., Monday through Thursday. On Friday, you can schedule the appointment booking availability from 8:00 a.m. to 2:00 p.m. You can also completely remove appointment booking for a specific day of the week, for example, Mondays or Friday.

Reconfigure the **Holiday Schedule** field on the Appointment Booking Service Configuration form for your walk-up location to use a custom **Off hours schedule** instead of the default holidays schedule.

## Procedure

1.  To create a schedule to exclude your unavailable appointment booking hours, navigate to **Walk-up Experience** &gt; **Administration** &gt; **Schedules**.

2.  Select **New.**

3.  Provide a name for your schedule, for example, `Off hours schedule`.

4.  Add a description, if desired.

5.  Select **Submit**.

6.  In the **Schedules** list, search by **Name** for the new **Off hours schedule** record.

7.  Select **Off hours schedule** to open the record.

    Use the Schedule Entries related list to create two separate excluded hours schedule entries, one for **Friday off hours** and one for **Weekday off hours**.

    ![Off hours schedule](../image/OffHoursSchedule.png)

8.  Select **New** in the Schedule Entries related list to create **Friday off hours**.

    You will configure Fridays to exclude all appointments after 1:00 p.m.

    ![Friday off hours](../image/FridayOffHours.png)

9.  Select **Update** to save your changes.

10. Add the **U.S. Holidays** default off-hour schedule as a child schedule to the **Off hours schedule**.

    1.  Click the Child Schedules related list.

    2.  Click **Edit** and use the slush bucket to move the **U.S. Holidays** schedule into the **Child Schedules List** for the **Off hours schedule**.

        Adding the **U.S. Holidays** schedule as a child ensures that all holidays are excluded from appointment booking and overrides the **Off hours schedule** configurations for holidays.

        **Note:** The **U.S. Holidays** schedule is the default off-hours schedule for the United States. Default off-hours schedules will differ depending on your location.

    3.  Click **Save**.

11. Click **Update** to save the **Off hours schedule** record.

12. Next, to configure your walk-up location to use the **Off hours schedule**, navigate to **Appointment Booking** &gt; **Appointment Booking Configuration**.

13. Select **Walk-up Experience** and then the walk-up location you want to reconfigure, for example, San Diego Tech Lounge.

    ![Appointment Booking Configuration](../image/AppointmentBookingConfiguration.png)

14. In the **Holiday Schedule** field, change the default, base system schedule value to **Off hours schedule**, using the list search ![list search icon](../../../common/image/List_SearchIcon.png) icon.

15. Click the **Daily Schedule** tab to configure the daily start and end times for the walk-up location.

    For this location, the hours of operation begin at 8:00 a.m. and end at 5:00 p.m. \(17:00\), Monday through Friday.

    ![Configure location daily start and end times](../image/AppointmentBookingConfig.png)

16. Select **Update** to save your changes.

17. To verify the hours you want excluded from appointment booking are unavailable, navigate to **Self-Service** &gt; **Walk-up Check-in**.

18. Select the walk-up location with the excluded hours you want to verify.

    ![Welcome to the walk-up check-in](../image/WelcomeWalkupServicePortal.png)

19. Select **Schedule an appointment**.

20. Click the calendar ![calendar icon](../image/CalendarIcon.png) icon to view the available appointment times for the walk-up location.

    The appointment schedule reflects the excluded hours you configured by using the **Off hours schedule**. Scroll down in the **Select Appointment** window to view the end times.

    ![Available appointments with accurate off hours times](../image/AvailableAppointments.png)


**Parent Topic:**[Configure Walk-up Experience appointment booking](../concept/walkup-appointment-booking-config.md)

