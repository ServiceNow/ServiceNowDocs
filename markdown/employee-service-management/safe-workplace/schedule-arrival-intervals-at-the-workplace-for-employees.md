---
title: Define arrival schedules at the workplace for employees
description: Define arrival slot times in Workplace Core for different locations at your workplace and indicate the capacity for each slot. Establishing arrival schedules enables safe staggered entry of employees to these locations.
locale: en-US
release: yokohama
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Setting and tracking arrivals at the workplace, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Define arrival schedules at the workplace for employees

Define arrival slot times in Workplace Core for different locations at your workplace and indicate the capacity for each slot. Establishing arrival schedules enables safe staggered entry of employees to these locations.

## Before you begin

-   [Add your workplace data](../../workplace-service-delivery/concept/providing-your-workplace-data-wsd.md).
-   Ensure you have the data for arrival schedules of the locations of your workplace.
-   Ensure that your time zone is set to the time zone of the building that is used for the arrival.

    **Important:** Starting with Workplace Core version 2.3, time zones are introduced in the application. All the arrival schedules that were created on Workplace Core version 2.2 and earlier are deactivated after the upgrade. Both existing customers and new customers must perform the following actions on existing arrival schedules to set them to active:

    1.  Set the time zone of the building where you are creating or updating the arrival schedule.

        **Note:** If you are creating or updating the arrival schedule for a floor, area or a space, then select the building where it is located.

        1.  Go to **Workplace Safety Management** &gt; **Space Administration**.
        2.  Select **Buildings**, **Floors**, **Areas**, or **Spaces** based on where you are scheduling an arrival slot.
        3.  Select the building, floor, area, or the space for which you want to set the time zone.
        4.  Set the building time zone.
            -   If you selected a building, set the time zone in the **Time zone** field.
            -   If you selected a floor, area, or the space, on the form, select the preview icon \(![workplace location info icon](../../wsd-reservation-management/image/info-icon.png)\) that is next to the **Building** field.
                -   In dialog box, select **Open record**.
                -   On the Buildings form, set the time zone in the **Time zone** field.
        5.  Select **Update**.

            **Note:** All the active arrival schedules that were created on this building and on associated floors, areas, or spaces will be deactivated. Any future arrival requests that are related to this schedule will be canceled.

        6.  Select **Ok** on the warning that appears.
    2.  Change your session's time zone to the building's time zone.

        **Note:** Ensure that the sn\_wsd\_core.workplace\_manager role is included in the **glide.timezone\_changer.roles** property. If it is not included, ask your system administrator to include the role so that you can change your time zone.

        1.  Select the settings icon \(![Settings icon.](../images/system-settings-icon.png)\) on your instance header.
        2.  Set the **Time zone** field to the time zone of the building where you are creating or updating the arrival schedule.

Role required: sn\_wsd\_core.workplace\_manager

## About this task

## Procedure

1.  Navigate to **Workplace Safety Management** &gt; **Workplace Arrival Scheduling**.

2.  Select **Create Arrival Schedules**.

3.  On the form, fill in the fields.

<table id="table_dkj_gzq_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace location

</td><td>

Select a building, floor, area or space where you want to schedule the arrival times.

</td></tr><tr><td>

Arrival schedule time

</td><td>

Time \(in hours, minutes, and seconds\) at which employee arrivals can start at this location, for example, 12 30 00.

</td></tr><tr><td>

Active

</td><td>

Option for indicating whether this schedule time is active.If marked as active, this schedule time will appear every day in the list of available time slots.

</td></tr><tr><td>

Capacity

</td><td>

Maximum number of employees that can schedule their arrival to this location at this slot time.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

An arrival schedule is created for this workplace location for the indicated time and capacity. You can view arrival schedules by navigating to **Workplace Safety Management** &gt; **Workplace Arrival Scheduling** &gt; **Arrival Schedules**.

**Parent Topic:**[Setting and tracking arrivals at the workplace](../concept/scheduling-employees-arrival-to-the-workplace.md)

