---
title: SNMP trap collector extension
description: The SNMP trap collector is a MID Server extension that listens for SNMP traps from the devices on your network.For the SNMP trap collector extension to receive traps from network devices, each device must designate the MID Server that runs the SNMP trap collector extension as a recipient of the trap.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# SNMP trap collector extension

The SNMP trap collector is a MID Server extension that listens for SNMP traps from the devices on your network.

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>Upon receiving a trap, the MID Server sends the trap to the instance for further processing by Event Management. If Event Management is not active, traps are not processed and are discarded by the instance.

For the SNMP trap collector extension to receive traps from network devices, each device must designate the MID Server that runs the SNMP trap collector extension as a recipient of the trap. See the documentation for the network device to configure your hardware to do this. Generally, the SNMP trap collector extension should run on only one MID Server per VLAN. Multiple MID Server recipients on the same VLAN causes duplicate data in the CMDB. If network devices are separated by VLANs, multiple MID Servers may have trap collectors installed.

To configure multiple SNMP trap collector extensions, configure each in a separate record, with a unique name, and a designated MID Server.

## Configure the SNMP Trap Collector Extension

For the SNMP trap collector extension to receive traps from network devices, each device must designate the MID Server that runs the SNMP trap collector extension as a recipient of the trap.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Extensions.** &gt; **MID SNMP Trap Listener**

2.  Click **New** or open an existing extension.

3.  Fill in the fields from the table, as appropriate.

4.  Click **Submit** or **Update**.

    ![SNMP trap collector](../image/SNMPTrapCollectorExtension.png)

<table id="table_j3g_vrs_zq"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for this SNMP trap collector extension for easy identification.

</td></tr><tr><td>

Short description

</td><td>

A description of the MID Server extension, if more description than the **Name** is necessary.

</td></tr><tr><td>

Extension

</td><td>

\[Read-Only\] The extension type is automatically set to **TrapExtension**.

</td></tr><tr><td>

UDP port

</td><td>

The port number that your network hardware uses when sending a trap to the designated MID Server. Port numbers 1024 and above are recommended. Port numbers 1023 and lower may be system reserved and can result in access violations for MID Servers that are not running with administrative credentials.

</td></tr><tr><td>

Status

</td><td>

\[Read-Only\] The status of the trap collector extension. This field is blank until the extension is run. After it is run, the value may be:

 -   **Started:** The extension is running.
-   **Stopped:** The extension is not running.
-   **Offline:** The MID Server is down.
-   **Error:** The extension failed with an error.


</td></tr><tr><td>

Execute on

</td><td>

The location for running this extension: a **Specific MID Server** or a **Specific MID Server Cluster**. The recommended setting is **Specific MID Server**. Network hardware typically has to be configured to send to a specific IP address. If the listener moved to a different MID Server in the cluster, the trap would not be received.

</td></tr><tr><td>

MID Server

</td><td>

The name of the designated MID Server if you selected **Specific MID Server** in the **Execute on** field. The name of the designated MID Server cluster if you selected **Specific MID Server Cluster** in the **Execute on** field. If you selected **Specific MID Server Cluster**, a ServiceNow algorithm determines which server in the cluster runs the extension.

</td></tr><tr><td>

Executing on

</td><td>

\[Read-Only\] The name of the MID Server on which the extension is running. This field shows the name of the MID Server even if the MID Server is down. If the extension is stopped by the user, this field is empty.

</td></tr></tbody>
</table>5.  In **Related Links**, run any of the following actions against the SNMP trap collector extension:

    |Related Link|Description|
    |------------|-----------|
    |Start|Starts the extension if it is currently not running. The extension is started on the configured MID Server and port number.|
    |Stop|Stops the running extension on the configured MID Server. No action is taken if the extension is not running.|
    |Restart|Stops, then starts the extension on the configured MID Server and port number.|
    |Test|Verifies that the configured MID Server can run the SNMP trap collector extension on the specified port. Running a test does not affect any extensions that are currently running.|
    |Update parameters|If you make changes to the extension configuration, use this option to update the parameters of the currently running extension. First, the parameters are tested for validity. If the parameters are valid, the extension disconnects and reconnects with the new parameters.|


