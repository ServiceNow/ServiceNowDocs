---
title: Create or modify service configuration for Appointment Booking
description: Service-level appointment booking enables customers to easily schedule specific services like installation, AC repair, or configuring printers, by customizing appointment availability, lead times, notifications, and booking rules.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create or modify service configuration for Appointment Booking

Service-level appointment booking enables customers to easily schedule specific services like installation, AC repair, or configuring printers, by customizing appointment availability, lead times, notifications, and booking rules.

## Before you begin

Role required: appointment\_booking\_admin

Verify you have an active application configuration \(**Field Service Order Configuration or Field Service Task Configuration**\) set up. You can create multiple service-level configuration within an application-level configuration.

## About this task

To use the appointment booking feature, administrators must create a configuration for each service that is available to customers. In the service configuration, administrators can select a schedule from the **Schedules** list and set it as **Excluded** to exclude it from appointment availability.

**Note:**

Appointment Booking determines work and travel duration for appointment booking using the following hierarchy.

1.  **Appointment schedule override**: This takes the highest priority.

    The appointment schedule override lets you define work and travel duration for a specific territory, specific days, or specific date ranges.

2.  **Appointment schedule**: If no schedule override exists, the system uses the duration defined in Appointment schedule at a territory level.
3.  **Work order task**: If the **Use task duration** option is enabled and no appointment schedule defined, Appointment Booking uses the durations from the work order task.
4.  **Appointment service configuration**: If none of the above are defined, Appointment Booking uses the work duration and travel duration configured in the appointment service configuration.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  Select the desired configuration.

    -   To configure appointment booking service for work orders, select **Field Service Order Configuration**
    -   To configure appointment booking service for work order tasks, select **Field Service Task Configuration**
3.  In the Appointment Booking Service Configuration related list, click **New**.

4.  On the form, fill in the following fields as needed.

<table id="table_vst_5nf_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use appointment schedule

</td><td>

Option to configure schedule based on appointment window and service mapping configurations.When enabled, you can configure additional features like overlapping appointment window, allowing overbooking of slots. For more information, see [Create an Appointment schedule](create-appt-sched.md)

**Note:**

-   When **Use appointment schedule** is selected, the default service configuration is overridden and the appointments are configured based on the **Appointment Schedule** settings.
-   The Advanced Appointment Booking plugin is required to use appointment schedules. For more information, see [Activate Advanced Appointment Booking](activate-adv-appt-booking.md).

</td></tr><tr><td>

Enable advanced configuration

</td><td>

Option to configure different appointment schedule for specific days. Advanced appointment booking configurations settings and service configuration rules will be considered for calculating the appointment slots.You can choose to either enable **Use appointment schedule** or **Enabled advanced configuration** for a service configuration. Both the settings can't be enabled together.

For more information, see [Create appointment booking advanced configuration](appintment-booking-day-level-config.md) and [Create service configuration rules for a service configuration](create-appt-booking-service-config-rules.md).

</td></tr><tr><td>

Active

</td><td>

Activates appointment booking for the service. **Note:** If deactivated, customers cannot schedule appointments for the service but can still create work orders.

</td></tr><tr><td>

Ignore Default Notifications

</td><td>

Sends notifications to customers.-   FALSE \(default\): Notifications are sent to the customer whenever an appointment is scheduled, rescheduled, or canceled.
-   TRUE: No notifications are sent.


</td></tr><tr><td>

Availability Method

</td><td>

Use one of the methods to determine appointment availability for the service. You can choose the availability method depending on the Field Service Management configuration setting in the **Assignment method for tasks** field of [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md). **Note:** The availability method setting for the service overrides the availability method setting in the application configuration unless **Appointment configuration method** is selected.

The available methods are:-   **Number of appointments per slot**: Sets a fixed number of available appointments per time slot. Recommended if task assignment is manual.
-   **Scripted**: Dynamically calculates availability based on Field Service Management settings. Recommended if auto-assignment or dynamic scheduling is used. This is the default setting.
-   **Based on capacity**: Calculates availability based on the capacity defined in the capacity management settings. For more information, see [Create a capacity assignment](../concept/assign-work-based-on-the-defined-capacity-.md)

This option is available when the Task Table is selected as work\_order and Field Service Capacity and Reservations Management plugin is installed.

-   **Appointment configuration method**: This is the default option. It calculates availability based on the availability method setting in the appointment booking application configuration.
For more information on appointment availability methods, see [Learn about appointment availability settings](../reference/appt-booking-task-assignment.md).

</td></tr><tr><td class="sub-head" colspan="2">

General Information

</td></tr><tr><td>

Name

</td><td>

The name of the service configuration.

</td></tr><tr><td>

Configuration

</td><td>

The name of the appointment booking configuration to which this service belongs.

</td></tr><tr><td>

Availability table

</td><td>

The table that is used to calculate appointment availability. The default is the Work Order Task \[wm\_task\] table for Field Service Management. The availability table is considered when the tasks are auto-assigned or through dynamic scheduling and the availability method is set to **Scripted**.

</td></tr><tr><td>

Holiday Schedule

</td><td>

The holiday schedule to use when determining availability. Appointment booking evaluates the holiday schedule when determining the number of available appointments and excludes any day in the schedule that is set to **Exclude**. Click the lookup icon and select a schedule from the Schedules list. **Note:**

-   Holiday schedules are useful when the assignment method for tasks is set to **manually**, which does not consider agent schedules.
-   When **Use appointment schedule** is selected, the holiday schedule defined in the appointment schedule is considered and the holiday schedule defined in the service configuration is ignored.


</td></tr><tr><td class="sub-head" colspan="2">

Catalog Information

</td></tr><tr><td>

Catalog Item

</td><td>

Select the catalog item \(service\) for which this configuration applies.**Note:** The catalog item must exist in the service catalog.

Before configuring appointment booking with work orders, ensure you create a work order template. Similarly, if you are using appointment booking with work order tasks, create a work order task template first.

</td></tr><tr><td>

Location

</td><td>

Field from the record producer that specifies the appointment location. Ensure that this field not left blank and is filled with the appropriate location to avoid issues when rescheduling an appointment.

</td></tr><tr><td>

Appointment is mandatory

</td><td>

Enable this check box if it is mandatory that a customer create an appointment when requesting this service. -   If enabled, the **Appointment** field appears on the record producer and the user must select an available appointment on the [Select Appointment window](../reference/appt-booking-select-appt-window.md) before submitting the service request.
-   If disabled, the user can submit the service request without selecting an appointment.


</td></tr><tr><td>

User contact

</td><td>

The field on the record producer that determines the individual for whom the appointment is being created. This is a reference field that looks for a sys\_user variable and sets variable on the record producer, for example, **Contact**.Ensure that this field not left blank and is filled with the appropriate value to avoid issues when rescheduling an appointment.

</td></tr><tr><td>

Timezone

</td><td>

The timezone considered to display the appointment window. The available options are:-   **Appointment Location**: Determines the appointment availability based on the location of the appointment.
-   **User Contact Location**: Determines the appointment availability based on the user contact's location.


</td></tr><tr><td class="sub-head" colspan="2">

Booking

</td></tr><tr><td>

Appointments per window

</td><td>

Number of available appointments per time slot. Applies primarily for **manual assignment**. This setting does not apply for **auto-assignment or dynamic scheduling**, unless a location is not provided. Then, the configuration defaults to the number of appointments per window.

</td></tr><tr><td>

Lead time

</td><td>

Minimum time in hours or days required in advance for customers to book an appointment. Default time is 4 hours.

</td></tr><tr><td>

Future bookable max days

</td><td>

The maximum number of days into the future, starting from the current day, for which an appointment can be booked for this service. The default is 14 days.

</td></tr><tr><td>

Reschedule / Cancel by time

</td><td>

The number of hours or days prior to an appointment when cancellation or rescheduling is permitted. The **Cancel** button is not available if a user attempts to cancel or reschedule an appointment within this time. The default is 4 hours.

</td></tr><tr><td>

Ignore lead time on reschedule

</td><td>

Select to skip lead-time validation when rescheduling appointments.

</td></tr><tr><td>

Consider holidays for lead time calculation

</td><td>

Select to exclude holidays to calculate booking lead times when displaying available appointment booking slots. For example, if a holiday occurs during the lead time calculation period, the system skips the holiday and calculates the lead time using the next available working day.

</td></tr><tr><td class="sub-head" colspan="2">

Appointments

</td></tr><tr><td>

Appointment window

</td><td>

The length or duration of the appointment window. **Note:** Allow enough time for the work to be started and completed within this window.

The appointment window duration should be longer than both the work duration and travel duration when the appointment window is set as Complete by.

</td></tr><tr><td>

Use slot end time as

</td><td>

Select whether the agent should arrive by or complete the job before the window end time.

</td></tr><tr><td>

Work duration

</td><td>

Estimated time needed to complete all tasks created by the record producer. This duration is set for a task when it is created. Work duration is used to determine appointment availability.**Note:** When Use appointment schedule is selected, and **Use durations from the schedule** is enabled for the schedule, the work duration from the schedule is considered for determining appointment availability and the work duration set in the service configuration is overridden.

</td></tr><tr><td>

Use duration from template or task

</td><td>

Ignore the work duration configured in the service configuration and use the duration from the template or task.-   FALSE \(default\): Use the duration as set in the Work duration field.The sum of work and travel durations must be less than or equal to the appointment window to show available slots.
-   TRUE: Ignore manually configured work and travel durations. Instead, use values from templates or tasks.


</td></tr><tr><td>

Travel duration \(round trip\)

</td><td>

Average round-trip travel time to the appointment location. Travel duration is used to determine availability.**Note:** When Use appointment schedule is selected, and **Use durations from the schedule** is enabled for the schedule, the travel duration from the schedule is considered for determining appointment availability and the work duration set in the service configuration is overridden.

</td></tr><tr><td class="sub-head" colspan="2">

Daily Schedule

</td></tr><tr><td>

Bookable days

</td><td>

The days of the week for which appointments can be booked. The default is Monday through Friday.

</td></tr><tr><td>

Daily start time

</td><td>

The start of the work day and the earliest start time for an appointment window.

</td></tr><tr><td>

Daily end time

</td><td>

The end of the work day and the latest end time for an appointment window.

</td></tr><tr><td>

Include daily break

</td><td>

Enable this check box to schedule a break for each bookable day, then select the break start and end times. Can define one break which applies to all days.

</td></tr><tr><td>

Appointment booking preview

</td><td>

Provides a preview of the appointment windows and times based on the selected start and end times, break time, and appointment window.

</td></tr><tr><td class="sub-head" colspan="2">

Recommendation Configuration

</td></tr><tr><td>

Maximum slots to recommend

</td><td>

The maximum number of recommended slots.This field is available only if the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin is activated.

</td></tr><tr><td>

Recommendation score

</td><td>

Indicates the minimum score to recommend a slot. Enter a value between 0 and 1.This field is available only if the Advanced Appointment Booking \(com.snc.advanced\_appointment\_booking\) plugin is activated.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

The service-level appointment booking configuration is set up or updated. Users can book appointments based on these customized settings.

## What to do next

For further customization, you can create **service configuration rules** to define specific booking conditions or exceptions for individual locations or scenarios. For more information, see [Create service configuration rules for a service configuration](create-appt-booking-service-config-rules.md).

