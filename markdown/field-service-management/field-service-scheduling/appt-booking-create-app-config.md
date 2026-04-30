---
title: Create or modify an appointment booking application configuration
description: Create or modify an appointment booking configuration for an application. The information stored in this configuration applies to all the services within that application.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create or modify an appointment booking application configuration

Create or modify an appointment booking configuration for an application. The information stored in this configuration applies to all the services within that application.

## Before you begin

Role required: admin

## About this task

Application configurations enable booking appointments directly for work orders and work order tasks.

Application configurations apply to the entire application and all its services. Field Service Management provides default application-level configurations, known as the **Field Service Order Configuration** and **Field Service Task Configuration**. You can modify these default configurations or use them as templates to create new configurations.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  To create a new configuration, click **New**.

    To modify a configuration, click the configuration name.

3.  In the Appointment Booking Configuration form, fill in or modify the following fields as needed.

<table id="table_vst_5nf_2r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the application configuration.

</td></tr><tr><td>

Task Table

</td><td>

Appointments are created for the tasks in the selected table.

</td></tr><tr><td>

Availability Method

</td><td>

Use one of the methods to determine appointment availability. The selection depends on the Field Service Management configuration setting in the **Assignment method for tasks** field: -   **Number of appointments per slot**: Define a specific number of appointments per time slot. Use this availability method if the task assignment method is set to **manually**.
-   **Scripted**: Use the Field Service Management configuration setting to determine availability if the task assignment method is set to **using auto assignment** or **dynamic scheduling**. This is the default setting.
-   **Based on capacity**: Determine appointments based on the capacity defined in the capacity management settings. For more information, see [Create a capacity assignment](../concept/assign-work-based-on-the-defined-capacity-.md)

This option is available when the Task Table is selected as work\_order and Field Service Capacity and Reservations Management plugin is installed.

</td></tr><tr><td>

Advanced Calendar view for Portal

</td><td>

Option to display advanced calendar view for available appointments in the [Select Appointment window](../reference/appt-booking-select-appt-window.md) on your portal. This view displays appointments categorized in different time slots of the day, such as Morning, Afternoon, and Evening.

</td></tr><tr><td>

Active

</td><td>

Activates the application configuration and enables appointment booking.

</td></tr><tr><td>

Auto acceptance

</td><td>

If the Field Service Management configuration setting for **Process lifecycle** is set to **task-driven**, an agent must accept or reject an assigned task. Enable the **Auto acceptance** check box to override this configuration setting for appointment booking.

</td></tr><tr><td>

Calendar View

</td><td>

Display available appointments in the [Select Appointment window](../reference/appt-booking-select-appt-window.md) on the Customer or Consumer Service Portal for a single day or for a week.

</td></tr><tr><td>

Script

</td><td>

The script used to determine the number of available appointments.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The application configuration is created or modified.

## What to do next

Create service configurations for each of the services available to the customers. For more information, see, [Create or modify an appointment booking service configuration](appt-booking-create-service-config.md).

**Parent Topic:**[Configuring Appointment Booking](../concept/appointment-booking-administer.md)

