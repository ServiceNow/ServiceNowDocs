---
title: Pause the MID Server
description: Pause the MID Server to temporarily prevent it from polling the ECC Queue for work or sending Discovery results back to the instance.The MID server can be put into a Paused state to temporarily prevent it from polling the ECC Queue for work or sending Discovery results back to the instance.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-07-31"
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

You can only pause [validated MID Servers](t_ValidateAMIDServer.md). You might want to pause the MID Server when your network infrastructure is undergoing changes. This prevents applications like Discovery from throwing errors during a particular maintenance window.

A paused MID Server continues processing commands that it had already retrieved before it was paused. When you resume the MID Server, the MID Server starts retrieving new commands to process.

**Note:** Discovery continues to assign jobs to MID Servers that are **Paused**. MID Servers that are **Down** are not assigned jobs.

## Procedure

1.  Open the MID Server record.

2.  Select a running MID Server that has been validated.

3.  On the MID Server form, select **Pause MID** under **Related Links**.

    The state of the MID Server changes to **Paused**.

    ![A paused MID Server](../image/MIDServerIcon.png "A paused MID Server")

4.  To resume MID Server processing, select **Resume MID** under **Related Links**.


**Parent Topic:**[MID Server reference](../concept/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](../reference/r_MIDServerSystemRequirements.md)

[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md)

[MID Server dashboard](../concept/c_MIDServerDashboard.md)

[MID Server properties](../reference/r_MIDServerProperties.md#)

[MID Server parameters](../reference/mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](../reference/mid-config-param-priority.md)

[MID Server File Cleaner](../concept/mid_file_cleaner.md)

[MID Server protected records and reserved characters](../reference/mid-server-reserved-characters.md)

[MID Server privileged commands](../concept/c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](../reference/r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](../reference/r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](t_MIDServerOptionalConfiguration.md)

## MID Server pause

The MID server can be put into a **Paused** state to temporarily prevent it from polling the ECC Queue for work or sending Discovery results back to the instance.

Unlike stopping the MID Server from the [Windows](../concept/mid-server-install-prereqs.md#) or [Linux](t_InstallAMIDServerOnLinux.md#) server command line on the MID Server machine, pausing the MID server is something that you can do from the instance. The MID Server pause feature is available starting with the Istanbul release.

**Note:** You can only pause [validated MID Servers](t_ValidateAMIDServer.md).

You can still perform these actions when the MID Server is paused:

-   [Access the MID Server logs](../concept/ecc-queue-mid-server.md#) and delete log entries.
-   View MID server statistics. While the MID Server is in the **Paused** state it stops generating statistics. But you can still view the statistics generated before you paused the MID Server.
-   Retrieve the MID Server thread dump.
-   Make and save [configuration changes](../concept/c_MIDServerConfiguration.md) and property changes to the server. The changes take effect after the MID Server is resumed.
-   Clear the ECC queue.

The [MID server heartbeat](../reference/r_MIDServerHeartbeat.md) continues to function while the MID Server is in the **Paused** state. If the MID Server is upgraded while it is in the **Paused** state, the MID Server state automatically changes to **Up** after successful upgrade. It does not return to the **Paused** state.

During [MID Server selection](../concept/c_MIDServerSelector.md), paused MID Servers can still be selected but are prioritized below MID Servers that are not paused.

### Events that occur during MID Server pause

The **vCenter** and **SNMP** event collectors, continue to run and process events when you pause the MID Server. These events are not part of the normal synchronous communication that the MID Server has with the instance that you see in the ECC queue. Events are still relayed to the instance and can even trigger actions on records in the instance, such as a CI update. For example, if vCenter detects that a virtual machine goes down or is deleted, a vCenter event makes a change to the status of the corresponding CI record for that virtual machine.

To prevent these events from being processed, stop the extensions from running. For more information, see:

-   [Configure and run the vCenter event collector extension](../concept/c_VCenterEventProcessorExtension.md#)
-   [Configure the SNMP Trap Collector Extension](../concept/c_SNMPTrapCollectorExtension.md#)

