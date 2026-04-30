---
title: Updating arrival schedules at the workplace
description: Define building time zones, change the capacity of an arrival schedule, and set the schedule to active or inactive.
locale: en-US
release: xanadu
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting and tracking arrivals at the workplace, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Updating arrival schedules at the workplace

Define building time zones, change the capacity of an arrival schedule, and set the schedule to active or inactive.

## Before you begin

-   [Add your workplace data](../../workplace-service-delivery/concept/providing-your-workplace-data-wsd.md).
-   Ensure that you have the data for the arrival schedules of your workplace locations.
-   Ensure that your time zone is set to the time zone of the building that is used for the arrival.

    **Important:** Starting with Workplace Core version 2.3, time zones are introduced in the application. All the arrival schedules that were created on Workplace Core version 2.2 and earlier are deactivated after the upgrade. Both existing customers and new customers must perform the following actions on existing arrival schedules to set them to active:

    1.  Set the time zone of the building where you are creating or updating the arrival schedule.

        **Note:** If you are creating or updating the arrival schedule for a floor, area or a space, then select the building where it is located.

        1.  If you are updating the arrival schedule, do the following:
            1.  Select the workplace location info icon \(![Workplace location info icon.](../../wsd-reservation-management/image/info-icon.png)\) that is next to the **Workplace location** field.
            2.  In the dialog box, select **Open record**.
            3.  If the value of **Workplace location** is a floor, area or a space, then select the workplace location info icon \(![Workplace location info icon.](../../wsd-reservation-management/image/info-icon.png)\) that is next to the **Building** field.
        2.  On the Buildings form, set the time zone in the **Time zone** field.
        3.  Select **Update**.

            **Note:** All the active arrival schedules that were created on this building and on associated floors, areas, or spaces will be deactivated. Any future arrival requests that are related to this schedule will be canceled.

        4.  Select **Ok** on the warning that appears.
    2.  Change your session's time zone to the building's time zone.

        **Note:** Ensure that the sn\_wsd\_core.workplace\_manager role is included in the **glide.timezone\_changer.roles** property. If it is not included, ask your system administrator to include the role so that you can change your time zone.

        1.  Select the settings icon \(![Settings icon.](../images/system-settings-icon.png)\) on your instance header.
        2.  Set the **Time zone** field to the time zone of the building where you are creating or updating the arrival schedule.

Role required: sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Safety Management** &gt; **Workplace Arrival Scheduling**.

2.  Select **Arrival Schedules**.

3.  Select the arrival schedule that you want to update.

    **Note:** You cannot update the **Workplace location** or **Arrival schedule time** fields of an arrival schedule if there are any arrival requests associated with it. You must create a new arrival schedule for the changed **Workplace location** or **Arrival schedule time** fields.

4.  To activate the schedule, select the **Active** option.

5.  To change the capacity, edit the **Capacity** field.

6.  Select **Update**.


## Result

The arrival schedule is updated.

**Parent Topic:**[Setting and tracking arrivals at the workplace](../concept/scheduling-employees-arrival-to-the-workplace.md)

