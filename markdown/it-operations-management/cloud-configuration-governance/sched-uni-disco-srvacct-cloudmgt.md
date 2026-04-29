---
title: Schedule discovery of all resources in a service account
description: Add a custom schedule for Discovery to discover all resources in each datacenter in a service account and then update the CMDB with the new information.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Additional Cloud Provisioning and Governance setup on day 2, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Schedule discovery of all resources in a service account

Add a custom schedule for Discovery to discover all resources in each datacenter in a service account and then update the CMDB with the new information.

## Before you begin

-   A cloud account must exist with service accounts and associated datacenters. You must run on-demand Discovery to discover datacenters before you can schedule Discovery.
-   Use the Cloud Discovery Workspace, and at least version 1.15 of Discovery and Service Mapping Patterns from the ServiceNow Store.

Role required: sn\_cmp.cloud\_admin

## About this task

-   Scheduled [Cloud Discovery](../../discovery/concept/cloud-discovery-wizard.md) discovers only datacenters that are part of the service account when the schedule is created. If datacenters have been added since the time you created the schedule, Discovery does not discover those datacenters. Delete the old schedule and create a schedule every time the datacenters in a service account change.
-   Discovery populates the CMDB with the discovered resources and updates the resource information on the **Resources** tab. You can view Discovery results on the **Discovery Log** tab.

**Important:** Use the Cloud Discovery Workspace to run the discovery schedule. The discover datacenter UI action is legacy and the preferred approach is to setup schedules from CDW.

## Procedure

1.  In the **Cloud Admin Portal** navigate to **Manage** &gt; **Discovery Schedules**.

2.  Select **Add Cloud Schedule**.

3.  On the Add Account page, select the cloud **Provider** and enter a unique, descriptive **Name** for the schedule.

4.  In the **Service Account** section, select **Select Account**, specify the service account, and then click **Next**.

    **Note:** To create a service account, select **Add Account** and then fill in the form. For details, see the process of setting up a service account in the Day 1 setup guide.

5.  On the Select Datacenters page, specify which of the datacenters in the service account to discover by moving the datacenters to discover into the **Selected** list or by selecting **Discover all datacenters listed below** to move all datacenters to the **Selected** list.

6.  Click **Next**.

7.  On the Create Schedule page, you specify the time and frequency of discovery.

    **Note:** **Run time** setting uses the system time zone.

<table id="table_qtt_rtf_br"><thead><tr><th>

Frequency

</th><th>

Description

</th></tr></thead><tbody><tr><td>

On Demand

</td><td>

Doesn’t run on a schedule. Select **Discover now** to run Discovery. This is the default option.

</td></tr><tr><td>

Daily

</td><td>

Runs every day. Use the **Start time** field to specify the time of day.

</td></tr><tr><td>

Weekly

</td><td>

Runs on one designated day of each week. Use the **Start time** field to specify the time of day.

</td></tr><tr><td>

Monthly

</td><td>

Runs on one designated day of each month. Use the **Day** field to select the day of the month. Use the **Start time** field to specify the time of day. If the designated day doesn’t occur in the month, the schedule doesn’t run that month. For example, if you designate day 30, the schedule doesn’t run in February.

</td></tr><tr><td>

Periodically

</td><td>

Runs every designated time. Use the **Repeat Interval** field to define the time in days, hours, minutes, and seconds. The first Discovery runs at the point in time defined in the **Starting** field. The subsequent discoveries run after each **Repeat Interval** period passes.

</td></tr><tr><td>

Once

</td><td>

Run one time as designated by the date and time defined in the **Starting** field.

</td></tr><tr><td>

Weekdays

</td><td>

Runs every Monday, Tuesday, Wednesday, Thursday, and Friday. Use the **Start time** field to select the time of day.

</td></tr><tr><td>

Weekends

</td><td>

Runs every Saturday and Sunday. Use the **Start time** field to select the time of day.

</td></tr><tr><td>

Month Last Day

</td><td>

Run the last day of every month. Use the **Start time** field to select the time of day.

</td></tr><tr><td>

Calendar Quarter End

</td><td>

Runs on March 31, June 30, September 30, and December 31. Use the **Start time** field to select the time of day. To change the dates, modify the DiscoveryScheduleRunType script include.

</td></tr><tr><td>

After Discovery

</td><td>

Allows you to sequentially stagger the schedule. Use this option to run this schedule after the Discovery designated in the **Run after** field finishes. Select the **Even if canceled** check box to designate that this discovery should run even if the **Run after** Discovery is canceled before it finishes.

 -   This option isn’t valid when the Discovery is started via DiscoverNow, or when using the Discover CI feature.
-   You can’t designate an inactive Discovery schedule.
-   You can’t create a loop by designating the run after Discovery to be the same Discovery.
-   This Discovery doesn’t run if the **Run after** Discovery doesn’t finish, with the exception that the **Even if canceled** check box is selected and the Discovery is canceled.


</td></tr><tr><td>

Cancel Discovery if longer than

</td><td>

Time limit for running the Discovery. When the specified time elapses, the remaining tasks for the Discovery are canceled even if the Discovery isn’t finished. If the check box isn’t selected, the Discovery runs until finished. This setting constrains system load to a desirable time window.

</td></tr></tbody>
</table>8.  Select **Finish** and **Run Now**.


## Result

Discovery runs immediately. Discovery runs at the specified times and adds discovered datacenters to the Logical Datacenters related list.

If you configured a Discovery schedule, it appears in the Discovery Config - Logical Datacenters related list. To run Discovery on a single datacenter, add the datacenter to the Discovery schedule in the related list, then run Discovery again.

Open a datacenter record to see the relationships between the datacenter and the resources in the datacenter.

![Resources in an AWS datacenter](../../cloud-management-v2/image/discovered-datacenter-example.png "Resources in an AWS datacenter")

**Note:** By default, Discovery stores the discovered VM hardware types in the Hardware Type \[cmdb\_ci\_compute\_template\] table. If you notice an unusually large number of records in this table, use the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table to store the discovered VM hardware types. For more information, see [Enable the Cloud Hardware Type class extension](../../discovery/task/enable-hardware-type-class-extension.md). All Cloud Provisioning and Governance features, such as provisioning, quotas, and so on continue to work as is after you switch to the Cloud Hardware Type table.

## What to do next

-   To view discovery status, discovery logs, discovered devices, and the ECC queue, click **Advanced View**.
-   If Discovery fails, check the Cloud Discovery results on the [Discovery Home page](../../discovery/concept/discovery-home-page.md#).

