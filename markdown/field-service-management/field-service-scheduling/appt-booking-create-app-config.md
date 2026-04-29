---
title: Create or modify an application configuration for Appointment Booking
description: Set up an application configuration to manage appointment booking settings across all services within your application. You can either create a new configuration or modify an existing one provided by Field Service Management.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create or modify an application configuration for Appointment Booking

Set up an application configuration to manage appointment booking settings across all services within your application. You can either create a new configuration or modify an existing one provided by Field Service Management.

## Before you begin

Role required: appointment\_booking\_admin

## About this task

Field Service Management provides default application-level configurations:

-   **Field Service Order Configuration** \(for work orders\)
-   **Field Service Task Configuration** \(for work order tasks\)

For example, if you create application configuration for the table Work Order \[wm\_order\], these appointment booking configurations are applied to all the work orders. You can modify these default configurations or use them as templates to create new configurations.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  Perform one of the following actions:

    -   Select **New** to create a new configuration.

    -   Click the name of an existing configuration to modify it.

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

The settings are applied and appointments are created for the tasks in the selected table. The Work Order \[wm\_order\] table is the default table for the Field Service Order Configuration.

</td></tr><tr><td>

Availability Method

</td><td>

Use one of the methods to determine appointment availability at the application-level. You can choose the availability method depending on the Field Service Management configuration setting in the **Assignment method for tasks** field of [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md). The available methods are:-   **Number of appointments per slot**: Sets a fixed number of available appointments per time slot. Recommended if task assignment is manual.
-   **Scripted**: Dynamically calculates availability of technicians using customized scripts. Recommended if auto-assignment or dynamic scheduling is used. This is the default setting.
-   **Based on capacity**: Calculates availability based on the capacity defined in the capacity management settings. For more information, see [Create a capacity assignment](../concept/assign-work-based-on-the-defined-capacity-.md)

This option is available when the Task Table is selected as work\_order and Field Service Capacity and Reservations Management plugin is installed.

For more information on appointment availability methods, see [Learn about appointment availability settings](../reference/appt-booking-task-assignment.md).

</td></tr><tr><td>

Advanced Calendar view for Portal

</td><td>

Select to activate the configuration and enable appointment booking.

</td></tr><tr><td>

Active

</td><td>

Activates the application configuration and enables appointment booking.

</td></tr><tr><td>

Auto acceptance

</td><td>

Automatically accepts tasks assigned through appointment booking, overriding the manual accept/reject requirement of the task-driven process lifecycle. If the Field Service Management configuration setting for **Process lifecycle** is set to **task-driven**, an agent must accept or reject an assigned task. Enable the **Auto acceptance** check box to override this configuration setting for appointment booking.

</td></tr><tr><td>

Calendar View

</td><td>

Display available appointments in the [Select Appointment window](../reference/appt-booking-select-appt-window.md) on the Customer or Consumer Service Portal for a single day or for a week. The available options are:-   Day: Displays the available appointments for the day.
-   Week: Displays the available appointments for the entire week.


</td></tr><tr><td>

Script

</td><td>

The script used to determine the number of available appointments.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The application configuration is created or modified. Appointment booking settings defined apply to all services associated with the selected task table.

## What to do next

Create service configurations for each of the services available to the customers. For more information, see [Create or modify an application configuration for Appointment Booking](appt-booking-create-app-config.md).

