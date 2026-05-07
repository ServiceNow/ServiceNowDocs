---
title: View or modify a Walk-up Experience appointment booking configuration
description: View the base system default appointment booking configuration to determine if the criteria meets your walk-up appointment booking requirement. You can modify the configuration to manage appointment booking. The information stored in the Walk-up Experience appointment booking configuration applies to all the services within the application.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Appointment booking configuration, Walk-up Experience appointment booking, Walk-up Experience for Customer Service Management, Set up self-service, Configure, Customer Service Management]
---

# View or modify a Walk-up Experience appointment booking configuration

View the base system default appointment booking configuration to determine if the criteria meets your walk-up appointment booking requirement. You can modify the configuration to manage appointment booking. The information stored in the Walk-up Experience appointment booking configuration applies to all the services within the application.

## Before you begin

Role required: sn\_csm\_walkup.walkup\_admin

## About this task

The **Walk-up Experience** configuration is provided with the **Appointment Booking** feature.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Appointment Configurations**.

2.  To view the **Walk-up Experience** configuration, click the configuration name.

3.  In the Appointment Booking Configuration form, view or modify the following fields as needed.

<table id="table_ltp_w1g_wfb"><thead><tr><th>

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

Appointments are created for the tasks in the selected table. The Walk-up Appointment \[wu\_appointment\] table is the default table for the **Walk-up Experience** configuration.

</td></tr><tr><td>

Availability Method

</td><td>

Use one of two methods to determine appointment availability. -   **Number of appointments per slot**: Define a specific number of appointments per time slot. Use this method if the task assignment is set to **manually** which is the default setting.
-   **Scripted**: Use this configuration setting to determine availability if the task assignment method is set to **using auto assignment** or **dynamic scheduling**.


</td></tr><tr><td>

Active

</td><td>

Activates the application configuration and enables appointment booking.

</td></tr><tr><td>

Auto acceptance

</td><td>

If the application configuration setting for **Process lifecycle** is set to **task-driven**, an agent must accept or reject an assigned task. Enable the **Auto acceptance** check box to override this configuration setting for appointment booking.

</td></tr><tr><td>

Portal View

</td><td>

Display available appointments for a single day or for a week on the online **Self Service Walk-up Check-in** portal or from the **Service Portal**.

</td></tr></tbody>
</table>4.  Click **Submit**.


