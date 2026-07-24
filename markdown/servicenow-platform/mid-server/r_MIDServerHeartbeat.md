---
title: MID Server heartbeat
description: The instance checks the MID Server for a response every 5 minutes, using a synthetic transaction monitoring system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/r\_MIDServerHeartbeat.html
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
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

**Note:** Make sure that your MID Server can communicate on **port 443**. See [Configure MID Server network connectivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerConnectionPrerequisites.md) and [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md) for more information.

## System events

When a MID Server transitions from one state to another, one of these events is triggered:

-   mid\_server.up: The MID Server goes from a status of **Down**, **Paused**, or **Upgrading** to a status of Up.
-   mid\_server.down: The MID Server goes from a status of Up to a status of Down.
-   mid\_server.paused: The MID Server is paused.
-   mid\_server.upgrading: The MID Server is being automatically upgraded because the instance is being upgraded.

You can use these events to send notifications or trigger actions that you specify in scripts.

## Scheduled job

To change the trigger interval for the Heartbeat probe, navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**. Open the **MID Server Monitor** record and edit the interval.

\[Omitted image "MIDServerMonitorInterval.png"\] Alt text: MID Server heartbeat trigger interval

**Parent Topic:**[MID Server reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements]()

[MID Server upgrades]()

[Resolving MID Server issues]()

[MID Server dashboard]()

[MID Server properties]()

[MID Server parameters]()

[MID Server Configuration Parameter settings and priority]()

[MID Server File Cleaner]()

[MID Server protected records and reserved characters]()

[MID Server privileged commands]()

[MIDSystem methods]()

[Manually start, stop, and restart a MID Server]()

[Set the MID Server JVM memory size]()

[Pause the MID Server]()

