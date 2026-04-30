---
title: TCP connection discovery
description: Discovery identifies and classifies information about TCP connections using the ADM and ADME probes.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# TCP connection discovery

Discovery identifies and classifies information about TCP connections using the ADM and ADME probes.

Discovery populates this data in the TCP Connections \[cmdb\_tcp\] table.

<table id="table_DiscoverTCPConnections"><thead><tr><th>

Label

</th><th>

Table Name

</th><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Absent

</td><td>

cmdb\_tcp

</td><td>

absent

</td><td>

If the process is no longer running on this device. The first time the process is detected, the value is not selected \(meaning that it is not absent\). If Discovery runs again and does not detect the process, it is selected.

</td></tr><tr><td>

Computer

</td><td>

cmdb\_tcp

</td><td>

computer

</td><td>

The device that is connected to or is listening on the TCP port.

</td></tr><tr><td>

IP

</td><td>

cmdb\_tcp

</td><td>

ip

</td><td>

The IP address that this device or process is listening on or is connected to. If the IP address is 127.0.0.1, it is the host computer itself.

</td></tr><tr><td>

PID

</td><td>

cmdb\_tcp

</td><td>

pid

</td><td>

The ID of the process that is connecting to or listening on this device \(IP address\).

</td></tr><tr><td>

Port

</td><td>

cmdb\_tcp

</td><td>

port

</td><td>

The port number through which TCP traffic was detected.

</td></tr><tr><td>

Process

</td><td>

cmdb\_tcp

</td><td>

process

</td><td>

The process that is connecting to or listening on the port.

</td></tr><tr><td>

Type

</td><td>

cmdb\_tcp

</td><td>

type

</td><td>

-   **Listening on**: the process is listening to the device via TCP.
-   **Connecting to**: if the process is connected to this device via TCP.

</td></tr><tr><td>

count

</td><td>

cmdb\_tcp

</td><td>

count

</td><td>

The number of times that Discovery detects a specific TCP connection. This field is used by ADM enhanced probes.

</td></tr></tbody>
</table>Discovery populates this data in the Running Process \[cmdb\_running\_process\] table.

|Label|Field Name|Description|
|-----|----------|-----------|
|Name|name|The name of the running process.|
|Computer|computer|The device that the process is running on.|
|Parent|parent|The parent process of this process, if any.|
|Listening on|listening\_on|The ports that the processes is listening on.|
|Connected to|connected\_to|The ports that the processes is connected to.|
|Command|command|The command for this process, including the path.|
|PID|pid|The ID for the process.|
|PPID|ppid|The ID for the parent process.|
|Absent|absent|If the process is no longer running on this device. The first time the process is detected, the value is not selected \(meaning that it is not absent\). If Discovery runs again and does not detect the process, it is selected.|
|Classify|classify|If the running process should be classified.|
|Key parameters|key\_parameters|The key parameters for the command.|
|Parameters|parameters|The parameters for the command.|
|Count|count|The number of times that Discovery detects a specific TCP connection. This field is used by ADM enhanced probes.|

## Standard ADM probes

Discovery launches these probes with standard ADM discovery:

<table id="table_sw4_hmt_v4"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Includes these sub-probes

</th></tr></thead><tbody><tr><td>

AIX - ADM

</td><td>

Queries for information about active \(running\) AIX processes and active connections - the information required to perform application dependency mapping.

</td><td>

-   AIX - Active Connections
-   AIX - Active Processes

</td></tr><tr><td>

HP-UX - ADM

</td><td>

Queries for information about active \(running\) HP-UX processes and active connections - the information required to perform application dependency mapping.This probe requires that lsof be installed and the UNIX - Active Connections probe be activated, which is inactive by default.

</td><td>

-   UNIX - Active Connections
-   HP-UX - Active Processes

</td></tr><tr><td>

Solaris - ADM

</td><td>

Queries for information about active \(running\) Solaris processes and active connections - the information required to perform application dependency mapping. This probe is triggered by the Solaris Zones probe. The system triggers an ADM probe for each local zone contained in a global zone.This probe requires that lsof be installed on the global zone.

</td><td>

-   Solaris - Active Processes
-   Solaris - Active Connections

</td></tr><tr><td>

UNIX - ADM

</td><td>

Queries for information about active \(running\) UNIX processes and active connections - the information required to perform application dependency mapping.

</td><td>

-   UNIX - Active Connections
-   UNIX - Active Processes

</td></tr><tr><td>

Windows - ADM

</td><td>

Queries for information about active \(running\) Windows processes and active connections - the information required to perform application dependency mapping.

</td><td>

-   Windows - Active Connections
-   Windows - Active Processes

</td></tr><tr><td>

UNIX - ADM netstat

</td><td>

Performs the same functions as the UNIX ADM probe relying on netstat to support continuous TCP-based discovery. Service Mapping uses this probe for traffic-based discovery.

</td><td>

-   UNIX - Active Connections with Netstat. This probe retrieves TCP connections to populate the cmdb\_tcp and cmdb\_tcp\_connection tables.
-   UNIX - Active Processes. This probe retrieves TCP processes and populates the cmdb\_running\_process table.

</td></tr></tbody>
</table>## Enhanced ADM probes

Discovery launches these probes when enhanced ADM is activated:

|Probe|Description|
|-----|-----------|
|Windows - ADM Enhanced|Performs the same functions as the Windows ADM probe with additional parameters to control continuous TCP-based discovery. This probe is compatible with WinRM and non-WinRM supported MID Servers. Configure your MID Server using the `mid.windows.management_protocol` parameter. See [MID Server parameters](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for the values you can use for this parameter.|
|UNIX - ADM Enhanced|Performs the same functions as the UNIX ADM probe with additional parameters to control continuous TCP-based discovery.|

Use these probe parameters with the enhanced ADM probes:

<table id="table_ggg_cnp_x1b"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.adme.max\_result\_size

</td><td>

Control the size of the TCP tracking file.

</td></tr><tr><td>

max.adme\_result\_payload\_size

</td><td>

Controls the size of the result, including the payload.**Note:** If this is greater than the [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) mid.discovery.max\_payload\_size, a configuration error can occur.

</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Network device discovery](../concept/c_NetworkDevices.md)

**Related topics**  


[Application Dependency Mapping \(ADM\) for Discovery](r_ApplicationDependencyMapping.md#)

