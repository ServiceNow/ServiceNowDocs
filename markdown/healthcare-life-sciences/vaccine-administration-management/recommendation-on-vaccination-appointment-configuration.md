---
title: Guidance for configuring advanced appointment scheduling for a vaccination center
description: Advanced appointment scheduling configuration enables administrators to configure appointment durations, daily schedule, holiday schedule, and so on. The configuration is used to identify the available slots as well as a location’s capacity for a given day. The configuration enables users to select appointment slots based on the parameters that you configure.
locale: en-US
release: yokohama
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configuring Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Guidance for configuring advanced appointment scheduling for a vaccination center

Advanced appointment scheduling configuration enables administrators to configure appointment durations, daily schedule, holiday schedule, and so on. The configuration is used to identify the available slots as well as a location’s capacity for a given day. The configuration enables users to select appointment slots based on the parameters that you configure.

Be mindful that changing some of the configuration values for a finalized vaccination center configuration can have undesired side effects on both existing and future appointments.

The following forms and tables provide some helpful guidance for handling advanced appointment scheduling configurations for a vaccination center. They also provide some of the impacts of making certain changes. However, this guidance doesn’t address an exhaustive list of all possible side effects.

![Vaccination Appointment Configuration form with various fields to fill. For information on the fields available on the form, see the Vaccination Appointment Configuration form section that follows.](../image/vaccination-appointment-configuration.png "Vaccination Appointment Configuration form")

<table id="table_oxx_5nf_v4b"><thead><tr><th>

Field

</th><th>

Recommendation and Impact

</th></tr></thead><tbody><tr><td>

Name

</td><td>

You can change the name field without causing undesired side effects.

</td></tr><tr><td>

Description

</td><td>

You can change the description field without causing undesired side effects.

</td></tr><tr><td>

Holiday schedule

</td><td>

Don’t add a new holiday schedule when there are existing appointments in the current location. It invalidates existing appointments. Don’t add more holidays to the existing holiday schedule. New holidays may already contain booked appointments.

</td></tr><tr><td>

Appointment duration

</td><td>

-   Don’t modify the appointment duration when appointments have already been created in the current location.
-   Impact: Changing the total capacity of a location causes overlapping slots that result in overbooked appointments.
-   For example:
    1.  In your old configuration, if the appointment window was 5 minutes, the daily schedule would have looked like: 9:00 to 9:05, 9:05 to 9:10, 9:10 to 9:15, and 9:15 to 9:20. In this configuration, you have appointments booked from 9:00 to 9:05 and from 9:05 to 9:10, and appointments available from 9:10 to 9:15 and from 9:15 to 9:20.
    2.  If you create a new configuration with an appointment window of 10 minutes, then your daily schedule would look like: 9 to 9:10, 9:10 to 9:20 with available slots from 9:10 to 9:20, and actual slots are displayed in the same 10-minute increments.
    3.  The configuration change causes an overbooking in the 9:00 to 9:10 slot, because it was booked for two appointments in the previous configuration.

</td></tr><tr><td>

Lead time

</td><td>

You can change the lead time value without impacting any existing appointments.

</td></tr><tr><td>

Future bookable max days

</td><td>

-   Don’t decrease the value because appointments may have been booked on the last day in the current location. Decreasing the value invalidates appointments booked on the last day.
-   You can increase the value without impacting any existing appointments.

</td></tr><tr><td>

Reschedule or cancel by time

</td><td>

-   You can conditionally change the value.
-   If there’s any workflow that impacts existing appointments or users, it isn’t safe to change the value.

</td></tr><tr><td>

Active

</td><td>

-   Don’t deactivate the configuration when there are existing appointments. It invalidates existing appointments.
-   You can activate the previously inactive configuration without impacting any appointments.

</td></tr></tbody>
</table>![Vaccination Schedule form with various fields to fill. For information on the fields available here, see the Vaccination Appointment Configuration form section that follows.](../image/vacciation-schedule.png "Vaccination Schedule form")

<table id="table_pwn_hkm_fpb"><thead><tr><th>

Field

</th><th>

Recommendation and Impact

</th></tr></thead><tbody><tr><td>

Name

</td><td>

You can change the name field without causing undesired side effects.

</td></tr><tr><td>

Start date

</td><td>

-   Don’t increase the value because appointments may be booked between the old start date and the new start date. Increasing the value invalidates appointments booked between the old start date and the new start date.
-   You can decrease the value only when there are no overlapped slots configured in the other schedule under the same appointment configuration.
-   For example:
    1.  Say that your old schedule has a start date of April 8, 2021 and bookable days from Monday to Friday from 09:00 to 18:00.
    2.  Suppose that you created another schedule under the same appointment configuration which has a start and end date of March 1, 2021 to March 31, 2021.
    3.  Now, if you change the schedule start date to March 31, 2021, it creates an overlapped bookable slot with the existing schedule on March 31, 2021 and the system will create an error.

</td></tr><tr><td>

End date

</td><td>

-   Don’t decrease the value because appointments may be booked between the new end date and the old end date. Increasing the value invalidates appointments booked between the new end date and the old end date.
-   You can increase the value only when there are no overlapped slots configured in the other schedule under the same appointment configuration.

</td></tr><tr><td>

Appointments per window

</td><td>

-   Don’t set the number of appointments per window to 0.
-   Increase the number of appointments per window.
-   Don’t decrease the number of appointments per window for a service configuration when appointments have already been created.
-   Note the impact: Reducing the total number of appointments per window results in overbooked appointments per slot for the appointments that were created before the change.
-   For example:
    1.  Old configuration: You had 4 appointments per window. If the total number of windows = 2, then your total capacity is 2\*4, or 8. If you had 4 appointments created per slot, the total capacity used is 4\*2, or 8.
    2.  New configuration: You have 2 appointments per window. If you have two total windows, then your new total capacity is 2\*2, or 4. But if you had 4 appointments already created per slot \(based on a past configuration\), then your total capacity is 4\*2, or 8.
    3.  With this configuration, the total capacity, 8, exceeds the new total capacity of 4, causing overbooked appointments.

</td></tr><tr><td>

Daily start time

</td><td>

Don’t modify the daily start time when appointments are already present. Modification creates overbooked slots and invalidates previous appointments.

</td></tr><tr><td>

Daily end time

</td><td>

-   You can increase the daily end time. The increase is only valid when the appointment duration and daily start values aren’t changed.
-   Don’t make the daily end time earlier when appointments are already present. Doing so creates overbooked slots and invalidates previous appointments.

</td></tr><tr><td>

Bookable days

</td><td>

-   Adding days without impacting existing appointments.
-   Removing the bookable days when appointments have already been created invalidates past appointments.
-   For example:
    1.  In your old configuration, suppose that Saturday is bookable and appointments are booked on Saturday.
    2.  If you create a new configuration in which Saturday isn’t bookable, any appointments previously booked for Saturday are no longer valid.

</td></tr><tr><td>

Include daily break

</td><td>

-   Don’t change the value of the **Include daily break** check box.
-   Don’t add the daily break time if this check box is cleared.
-   Don’t change the duration of the break.
-   Don’t set the break start time and end time to be the same as the daily start time and daily end time because it won’t generate bookable slots.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

