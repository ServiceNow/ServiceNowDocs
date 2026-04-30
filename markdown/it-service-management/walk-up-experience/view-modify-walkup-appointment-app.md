---
title: View or modify a Walk-up Experience appointment booking configuration
description: View the base system default appointment booking application configuration to determine if the criteria meets your walk-up appointment booking needs. You can modify the application configuration to uniquely manage appointment booking for your experience. The information stored in the Walk-up Experience appointment booking application configuration applies to all the services within the application.
locale: en-US
release: yokohama
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Walk-up Experience appointment booking, Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# View or modify a Walk-up Experience appointment booking configuration

View the base system default appointment booking application configuration to determine if the criteria meets your walk-up appointment booking needs. You can modify the application configuration to uniquely manage appointment booking for your experience. The information stored in the Walk-up Experience appointment booking application configuration applies to all the services within the application.

## Before you begin

Role required: sn\_walkup.walkup\_admin or admin

## About this task

The **Walk-up Experience** configuration is provided with the **Appointment Booking** feature.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Booking Configuration**.

2.  To view the **Walk-up Experience** configuration, select the configuration name.

3.  In the Appointment Booking Configuration form, view or modify the following fields as needed.

<table id="table_ltp_w1g_wfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the application configuration.

</td></tr><tr><td>

Task Table

</td><td>

Table where appointments are created for the tasks. The field is automatically populated with Walk-up Appointment \[wu\_appointment\] table for configuring **Walk-up Experience**.

</td></tr><tr><td>

Availability Method

</td><td>

Option to determine the appointment availability. -   **Number of appointments per slot**: Define a specific number of appointments per time slot. Use this availability method if the task assignment method is set to **manually**. This is the default setting.
-   **Scripted**: Use this configuration setting to determine availability if the task assignment method is set to **using auto assignment** or **dynamic scheduling**.


</td></tr><tr><td>

Advanced Calendar view for Portal

</td><td>

Option to display advanced view of the calendar for booking an appointment.

</td></tr><tr><td>

Active

</td><td>

Option to activate the application configuration and enable appointment booking.

</td></tr><tr><td>

Auto acceptance

</td><td>

If the application configuration setting for **Process lifecycle** is set to **task-driven**, an agent must accept or reject an assigned task. Enable the **Auto acceptance** check box to override this configuration setting for appointment booking.

</td></tr><tr><td>

Portal View

</td><td>

Displays available appointments for a single day or for a week on the online **Self Service Walk-up Check-in** portal or from the **Service Portal** if the walk-up icon is configured there.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Configure Walk-up Experience appointment booking](../concept/walkup-appointment-booking-config.md)

