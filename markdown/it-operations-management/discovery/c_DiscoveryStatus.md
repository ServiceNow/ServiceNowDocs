---
title: Discovery status
description: The Discovery status provides a summary of a Discovery launched from a schedule. You can also cancel a Discovery that is in progress from the status form.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery status

The Discovery status provides a summary of a Discovery launched from a schedule. You can also cancel a Discovery that is in progress from the status form.

**Note:** Discovery schedules that have no status updates for a over a defined number of minutes are analyzed automatically by the Discovery Status Monitor job. By default, this job applies to Discovery schedules that discover configuration items. For more information, see the [Discovery Status Monitoring Job](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=c2a6f4bf935a1ed0f538fb2d6cba10be) article in the Now Support Knowledge Base.

To access the Discovery Status form, navigate to **Discovery** &gt; **Status** and open the status record for a Discovery.

Each record in the Status list represents the execution of a Discovery by a schedule and displays such high-level information as the date of the Discovery, the mode, the number of probe messages sent to devices, and the number of sensor records that were processed. A status record contains data that can help you troubleshoot a failed discovery. Use this data to troubleshoot the behavior of individual probes and sensors or even run those elements separately. Use the status controls to enter probe/sensor threads at any point for a specific Discovery, and then follow the process in either direction. You can also clearly see which classification probe ran and discovered a particular device by viewing the classification probe column in the device list.

-   **Refresh**: Refreshes the related tabs, including the **Discovery Log** and **ECC Queue** for discoveries still in progress.
-   **Discovery timeline**: The Discovery timeline is a graphical display of a discovery, including information about each probe and sensor that was used.
-   **Discovery log entries**: The Discovery Log shows information such as classification failures, Configuration Management Database \(CMDB\) updates, and authentication failures. A Discovery Log record is created for each action associated with a discovery status.
-   **ECC queue entries**: Entries in the ECC queue provide you with a connected flow of probe and sensor activity, as well as the actual XML payload that is sent to or from an instance.
-   **Device history**: The device history provides a summary of all the devices scanned during discovery, and what action sensors took on the CMDB.

**Note:** By default, only 30 days of Discovery records are displayed in the status list at a time.

The following Discovery status record shows the discovery of a load balancer using a pattern.

![Example Discovery status record](../image/discovery-status.png "Example Discovery status record")

<table id="table_nl1_yv5_lz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

An auto-generated number for the record.

</td></tr><tr><td>

Description

</td><td>

How this discovery was run. Typically, the description is Scheduled, but if you ran discovery manually from a Schedule, the record would show Discover Now in the Description field.

</td></tr><tr><td>

Schedule

</td><td>

The name of the Discovery schedule.

</td></tr><tr><td>

State

</td><td>

The state of the discovery: -   **Starting**
-   **Active**
-   **Completed**
-   **Canceled**

</td></tr><tr><td>

Started and Completed

</td><td>

The number of probes started and completed during discovery.

</td></tr><tr><td>

Source

</td><td>

Optional read-only field that shows the source of the discovery, such as **Schedule Discovery**, or **Quick Discovery**. If the source of the Discovery was from an API call, the source is **DiscoveryAPI**.

</td></tr><tr><td colspan="2">

**From Schedule \(Read-only schedule data\)**

</td></tr><tr><td>

Discover

</td><td>

Shows the Discovery type. The possible types are: **Configuration items**, **IP addresses**, **Networks**, or **Processes/Connections** \(ADM\).

</td></tr><tr><td>

Max Run Time

</td><td>

Displays the maximum amount of time Discovery was permitted to run on this schedule.

</td></tr><tr><td>

Log state changes

</td><td>

Indicates that state changes were logged during this Discovery. These states can be seen in the Last and Current fields in the**Discovery Devices** list in this form.

</td></tr></tbody>
</table>-   **[Cancel a Discovery from a Discovery Status](../task/t_CancelDiscoveryStatus.md)**  
You can manually cancel a discovery while it is in progress from the Discovery Status record.
-   **[Discovery timelines](c_DiscoveryStatusTimelines.md#)**  
A Discovery timeline generates a graphical display of a Discovery Status record, including information about each probe and sensor that was used in the discovery.
-   **[The ECC queue for Discovery](../reference/r_DiscoveryStatusECCQueue.md)**  
The External Communication Channel \(ECC\) Queue is a connection point between your ServiceNow instance and other systems that integrate with it, most commonly a MID Server.
-   **[Discovery device history](../reference/r_DiscoveryStatusDevices.md)**  
The **Devices** Related list in the Discovery Status form provides a summary list of all the devices scanned.

**Parent Topic:**[Configuring Discovery](c_DiscoveryConfiguration.md)

**Related topics**  


[Schedule a horizontal discovery](../task/t_CreateADiscoverySchedule.md#)

