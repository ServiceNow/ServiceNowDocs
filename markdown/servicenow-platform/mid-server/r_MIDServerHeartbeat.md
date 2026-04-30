---
title: MID Server heartbeat
description: The instance checks the MID Server for a response every 5 minutes, using a synthetic transaction monitoring system.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server heartbeat

The instance checks the MID Server for a response every 5 minutes, using a synthetic transaction monitoring system.

<table id="table_ljs_dsf_khb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>## Checking for a heartbeat

ServiceNow instances send a synthetic transaction via the Heartbeat probe to every MID Server every 5 minutes. The Heartbeat probe functions exactly as a normal probe does and is sent by writing an output record to the ECC queue. A MID Server retrieves the record when it queries the ECC queue for work. The MID Server processes the probe just as it would any other probe and responds back to the instance. If the instance does not detect a response from a MID Server, the instance marks that MID Server as **Down**. If the MID Server responds, the instance considers the MID Server to be functioning and communicating properly with the instance.

**Note:** Make sure that your MID Server can communicate on **port 443**. See [Configure MID Server network connectivity](../concept/c_MIDServerConnectionPrerequisites.md#) and [MID Server system requirements](r_MIDServerSystemRequirements.md) for more information.

## System events

When a MID Server transitions from one state to another, one of these events is triggered:

-   mid\_server.up: The MID Server goes from a status of **Down**, **Paused**, or **Upgrading** to a status of Up.
-   mid\_server.down: The MID Server goes from a status of Up to a status of Down.
-   mid\_server.paused: The MID Server is paused.
-   mid\_server.upgrading: The MID Server is being automatically upgraded because the instance is being upgraded.

You can use these events to send notifications or trigger actions that you specify in scripts.

## Scheduled job

To change the trigger interval for the Heartbeat probe, navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**. Open the **MID Server Monitor** record and edit the interval.

![MID Server heartbeat trigger interval](../image/MIDServerMonitorInterval.png "MID Server heartbeat trigger interval")

**Parent Topic:**[MID Server reference](../concept/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](r_MIDServerSystemRequirements.md)

[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

[MID Server dashboard](../concept/c_MIDServerDashboard.md)

[MID Server properties](r_MIDServerProperties.md#)

[MID Server parameters](mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](mid-config-param-priority.md)

[MID Server File Cleaner](../concept/mid_file_cleaner.md)

[MID Server protected records and reserved characters](mid-server-reserved-characters.md)

[MID Server privileged commands](../concept/c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)

