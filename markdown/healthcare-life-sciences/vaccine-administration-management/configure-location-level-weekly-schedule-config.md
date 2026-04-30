---
title: Configure advanced appointment scheduling for a center
description: Configure advanced appointment scheduling for a center. Advanced appointment scheduling enables you to configure different vaccination schedules, weekly, daily, and more, and the capacity to meet the changing needs of different location centers and programs.
locale: en-US
release: zurich
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure advanced appointment scheduling for a center

Configure advanced appointment scheduling for a center. Advanced appointment scheduling enables you to configure different vaccination schedules, weekly, daily, and more, and the capacity to meet the changing needs of different location centers and programs.

## Before you begin

Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Properties**, and make sure that the **Enable Vaccine Administration Management location specific Appointment Configuration** property \(**sn\_vaccine\_sm.enable\_vam\_appointment\_config**\) is selected.

**Warning:** Once you have enabled the property and your advanced appointment scheduling configurations are live, avoid disabling the property to help prevent any data inconsistencies.

Role required: sn\_vaccine\_sm.admin

## About this task

Configure advanced appointment scheduling for a center. You can create appointment configurations for use at a specific location or for reuse across multiple location centers and programs.

For each appointment configuration, you can create one or more vaccination schedules to configure the daily start and end time. You can configure the days that appointments can be booked, the inclusion of a daily break, and more. Appointment configurations apply for both self-scheduled and mass-booked appointments.

**Important:** When you enable this feature, it replaces the default appointment scheduling configuration that is applied across all centers. For further information about the default configuration, see [Configure vaccine appointment scheduling](vaccine-appt-booking.md).

## Procedure

1.  Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Programs**.

2.  Open a program record.

3.  In the Center related list, click the preview icon \(![Preview icon.](../image/preview-icon.png)\) to open the program center record.

4.  In the **Appointment configuration** field, click the lookup icon \(![Lookup icon.](../image/lookup-icon.png)\).

5.  Click **New**.

6.  On the form, fill in the fields.

<table id="table_yys_1kf_v4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the appointment configuration.

</td></tr><tr><td>

Description

</td><td>

Description of the appointment configuration.

</td></tr><tr><td>

Holiday schedule

</td><td>

Holiday schedule to associate with the appointment configuration.

</td></tr><tr><td>

Appointment duration

</td><td>

Appointment duration for the appointment configuration, which can range from 10 minutes to 8 hours.

</td></tr><tr><td>

Lead time

</td><td>

Time after which the first available appointment slot is shown to the user. For example, say that the lead time is four hours. If the current time is 7 AM, then the next available slot that the user would see would be for 11 AM.

</td></tr><tr><td>

Future bookable max days

</td><td>

Range of days that the user can view available slots to book their appointment. For example, say that the value is 14 days. When the user is scheduling the appointment, the user sees available slots for the next 14 days.

</td></tr><tr><td>

Reschedule/Cancel by time

</td><td>

Time until the user can reschedule or cancel the appointment. For example, say that the value is six hours. If the appointment is scheduled for Monday at 3 PM, then the user must reschedule or cancel the appointment by 9 AM that same day.

</td></tr><tr><td>

Active

</td><td>

Option to activate the appointment configuration for use. If enabled, then the appointment configuration applies for both self-scheduled and mass booked appointments.

 **Note:** Only one appointment configuration can be active at a time.

</td></tr></tbody>
</table>7.  Select and hold \(or right-click\) the form header and click **Save**.

8.  In the Vaccination Schedules related list, create one or more vaccination schedules for the appointment configuration.

    1.  Click **New**.

    2.  On the form, fill in the fields.

<table id="table_et1_gyf_v4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the vaccination schedule.

</td></tr><tr><td>

Start date

</td><td>

Start date for the schedule.

</td></tr><tr><td>

Appointments according to window

</td><td>

Number of appointments according to window.

</td></tr><tr><td>

Daily start time

</td><td>

Daily start time for the schedule.

</td></tr><tr><td>

Bookable days

</td><td>

Days that appointments can be booked.

</td></tr><tr><td>

Include daily break

</td><td>

Option to include a daily break. If enabled, you can specify the start and end time of the daily break.

</td></tr><tr><td>

Appointment configuration

</td><td>

This field is automatically set to the associated appointment configuration record.

</td></tr><tr><td>

End date

</td><td>

End date of the schedule.

</td></tr><tr><td>

Appointment duration

</td><td>

This field is automatically set to the appointment duration that was set in the associated appointment configuration record.

</td></tr><tr><td>

Daily end time

</td><td>

Daily end time of the schedule.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Preview of the vaccination schedule.

</td></tr></tbody>
</table>    3.  Click **Submit**.

    4.  Repeat the procedure to create vaccination schedules, as needed.


## What to do next

Once the configuration is finalized, changing some of the configuration values can have undesired side effects on both existing and future appointment scheduling. For details on how to handle advanced appointment scheduling configurations for a center, see [Guidance for configuring advanced appointment scheduling for a vaccination center](../reference/recommendation-on-vaccination-appointment-configuration.md).

-   **[Guidance for configuring advanced appointment scheduling for a vaccination center](../reference/recommendation-on-vaccination-appointment-configuration.md)**  
Advanced appointment scheduling configuration enables administrators to configure appointment durations, daily schedule, holiday schedule, and so on. The configuration is used to identify the available slots as well as a location’s capacity for a given day. The configuration enables users to select appointment slots based on the parameters that you configure.

**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

