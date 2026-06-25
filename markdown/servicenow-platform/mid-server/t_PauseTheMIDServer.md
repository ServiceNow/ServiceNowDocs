---
title: Pause the MID Server
description: Pause the MID Server to temporarily prevent it from polling the ECC Queue for work or sending Discovery results back to the instance.The MID server can be put into a Paused state to temporarily prevent it from polling the ECC Queue for work or sending Discovery results back to the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/t\_PauseTheMIDServer.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Pause the MID Server

Pause the MID Server to temporarily prevent it from polling the ECC Queue for work or sending Discovery results back to the instance.

## Before you begin

Role required: agent\_admin

<table id="table_uh4_bsf_khb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>## About this task

You can only pause [validated MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ValidateAMIDServer.md). You might want to pause the MID Server when your network infrastructure is undergoing changes. This prevents applications like Discovery from throwing errors during a particular maintenance window.

A paused MID Server continues processing commands that it had already retrieved before it was paused. When you resume the MID Server, the MID Server starts retrieving new commands to process.

**Note:** Discovery continues to assign jobs to MID Servers that are **Paused**. MID Servers that are **Down** are not assigned jobs.

## Procedure

1.  Open the MID Server record.

2.  Select a running MID Server that has been validated.

3.  On the MID Server form, select **Pause MID** under **Related Links**.

    The state of the MID Server changes to **Paused**.

    \[Omitted image "MIDServerIcon.png"\] Alt text: A paused MID Server

4.  To resume MID Server processing, select **Resume MID** under **Related Links**.


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

[MID Server heartbeat]()

[Set the MID Server JVM memory size]()

## MID Server pause

The MID server can be put into a **Paused** state to temporarily prevent it from polling the ECC Queue for work or sending Discovery results back to the instance.

Unlike stopping the MID Server from the [Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md) or [Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_InstallAMIDServerOnLinux.md) server command line on the MID Server machine, pausing the MID server is something that you can do from the instance. The MID Server pause feature is available starting with the Istanbul release.

**Note:** You can only pause [validated MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ValidateAMIDServer.md).

You can still perform these actions when the MID Server is paused:

-   [Access the MID Server logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/ecc-queue-mid-server.md) and delete log entries.
-   View MID server statistics. While the MID Server is in the **Paused** state it stops generating statistics. But you can still view the statistics generated before you paused the MID Server.
-   Retrieve the MID Server thread dump.
-   Make and save [configuration changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerConfiguration.md) and property changes to the server. The changes take effect after the MID Server is resumed.
-   Clear the ECC queue.

The [MID server heartbeat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerHeartbeat.md) continues to function while the MID Server is in the **Paused** state. If the MID Server is upgraded while it is in the **Paused** state, the MID Server state automatically changes to **Up** after successful upgrade. It does not return to the **Paused** state.

During [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md), paused MID Servers can still be selected but are prioritized below MID Servers that are not paused.

### Events that occur during MID Server pause

The **vCenter** and **SNMP** event collectors, continue to run and process events when you pause the MID Server. These events are not part of the normal synchronous communication that the MID Server has with the instance that you see in the ECC queue. Events are still relayed to the instance and can even trigger actions on records in the instance, such as a CI update. For example, if vCenter detects that a virtual machine goes down or is deleted, a vCenter event makes a change to the status of the corresponding CI record for that virtual machine.

To prevent these events from being processed, stop the extensions from running. For more information, see:

-   [Configure and run the vCenter event collector extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_VCenterEventProcessorExtension.md)
-   [Configure the SNMP Trap Collector Extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_SNMPTrapCollectorExtension.md)

