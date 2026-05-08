---
title: Create a discovery behavior for Unix-based load balancers
description: If your network uses load balancers running on Linux hosts, create a discovery behavior to ensure that Service Mapping and Discovery discover them correctly.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Create a discovery behavior for Unix-based load balancers

If your network uses load balancers running on Linux hosts, create a discovery behavior to ensure that Service Mapping and Discovery discover them correctly.

## Before you begin

Make sure that Discovery is activated.

Role required: service\_mapping\_admin or admin

## About this task

The discovery and mapping process begins with Discovery identifying the host. After the host discovery is complete, Service Mapping starts discovering and mapping applications running on this host.

The default discovery process identifies a configuration item \(CI\) as a Linux server if it finds an SSH port in use. It may lead to incorrect discovery of load balancers running on Linux as Linux servers. Create a discovery behavior to first discover network devices using SNMP protocol. After Discovery has discovered Unix-based load balancers correctly and created the appropriate CIs for them, you can continue with discovering and mapping application services in Service Mapping.

Discovery performs discovery through a MID Server located in the enterprise private network. A behavior determines:

-   What MID Server Discovery is using.
-   What probes and patterns the chosen the MID Server is running.

## Procedure

1.  Create a new behavior for discovering Unix-based load balancers:

    1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Behavior**.

    2.  Click **New**.

    3.  Enter the name for this behavior.

    4.  Right-click on the header bar and click **Save**.

    5.  Click **New** on the **Discovery Functionality** tab.

    6.  Enter 1 in the **Phase** field.

    7.  Select **SNMP only** from the **Functionality definition** list.

    8.  Select the relevant MID Servers in the **MID Servers** area.

    9.  Check the **Active** check box.

    10. Click **Submit**.

2.  Create a discovery schedule for the newly defined behavior:

    1.  Navigate to **Discovery** &gt; **Discovery Schedules**.

    2.  Click **New**.

    3.  Fill in the fields as follows:

<table id="table_xnx_zrb_5p"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique, descriptive name for your schedule.

</td></tr><tr><td>

Discover

</td><td>

Select **Configuration items**.

</td></tr><tr><td>

MID Server selection method

</td><td>

Select **Use behavior**.

</td></tr><tr><td>

Behavior

</td><td>

Select the behavior you created in step [1](t_CreateDiscoBehavior4LB.md#step_createBehavior).

</td></tr><tr><td>

Active

</td><td>

Select the check box to enable this schedule. If you clear the check box, the schedule is disabled, but you can still run a discovery manually from this form, using the configured values.

</td></tr><tr><td>

Max run time

</td><td>

Set a time limit for running this schedule. When the configured time elapses, the remaining tasks for the discovery are canceled, even if the scan is not complete. Use this field to limit system load to a desirable time window. If no value is entered in this field, this schedule runs until complete.

</td></tr><tr><td>

Max Idle time

</td><td>

Set a time limit for inactivity during discovery to automatically cancel stalled processes and log the event. A discovery is only considered idle if no input records are processed and nothing remains in the processing state; idle time is measured from the most recent change to an ECC Queue record. The configured idle time is fixed at the start of the discovery and won’t reflect any edits until the next run. If no value is entered in this field, this schedule runs until complete or cancelled.**Note:** By default, the **Max Idle time** field doesn’t display in the Discovery Schedule form. To include this parameter, open the Discovery Schedules \[discovery\_schedule\] table, add the column, and configure the Max Idle time directly in the table. For information about customizing columns in tables, see Personalize a list.

</td></tr><tr><td>

Run and related fields

</td><td>

Determines the run schedule of the discovery. Configure the frequency in the **Run** field and the other fields that appear to specify an exact time.**Note:** The run time always uses the system time zone. If you add the optional **Run as tz** field, it has no effect on the actual runtime.

</td></tr></tbody>
</table>3.  Create an IP range for the discovery schedule:

    **Important:** The IP range for the schedule must correlate with the IP range of the MID Server that you assigned to the behavior. The MID Server must also have the appropriate application or the **ALL** application.

    1.  On the Discovery IP Ranges tab, click **New**.

    2.  Enter the name for this IP range.

    3.  Configure the IP range by entering IP addresses in the **Starting IP** and **Ending IP** fields.

4.  Click **Submit**.


**Related topics**  


[Pattern-based discovery in Service Mapping](../concept/pattern-based-discovery.md)

[bundle-platcap.mid-server-landing]

