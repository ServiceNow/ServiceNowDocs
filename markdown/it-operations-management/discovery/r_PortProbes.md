---
title: Port probes
description: Port probes are used in Discovery by the Shazzam probe to detect protocol activity on open ports on devices it encounters.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# Port probes

Port probes are used in Discovery by the Shazzam probe to detect protocol activity on open ports on devices it encounters.

When a port probe encounters a protocol in use, the Shazzam sensor checks the port probe record to determine which classification probe to launch. The common protocols WMI, SSH, SNMP, and HTTP in the base system have priority numbers that control the order in which they are launched.

The priority is as follows:

-   1 - WMI
-   2 - SSH
-   3 - SNMP
-   4 - HTTP

In the base system, the WMI probe is always launched first, and if it is successful on a device, no other port probes are launched for that device. If the WMI probe is not successful, then the SSH probe is launched to gather information on the device. If it is not successful, the SNMP probe is launched. This method allows Discovery to classify a device correctly if the device is running more than one protocol \(for example, SSH, SNMP, and HTTP\).

## Discovery Port Probe form

To access the Port Probe form, navigate to **Discovery Definition** &gt; **Port Probes**.

To add multiple classification probes to a port probe, create a link between the port probe and the actual classification probe itself. See the bottom of the form to add additional Trigger probes. That way, if one classification fails, it does not affect the others, thus Discovery performance may be enhanced.

![Discovery port probe form](../image/discovery_port_probe.png)

The Port Probe form provides the following fields:

<table id="table_zzx_q1w_dp"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Simple name for the port probe that reflects its function \(for example, SNMP\).

</td></tr><tr><td>

Description

</td><td>

Definition of the acronym for the protocol. \(For example, SSH is Secure Shell login\).

</td></tr><tr><td>

Scanner

</td><td>

Shazzam techniques for exploring a port. Some of these are protocol-specific, and others are generic. For example, a WMI port probe uses a Scanner value of Generic TCP, and the SNMP port probe uses a value of SNMP.

</td></tr><tr><td>

Active

</td><td>

Indicates whether this port probe is enabled or disabled.

</td></tr><tr><td>

CIs

</td><td>

Indicates whether this port probe is enabled or disabled for discovering Configuration Items.

</td></tr><tr><td>

IPs

</td><td>

Indicates whether this port probe is enabled or disabled for discovering IP addresses.

</td></tr><tr><td>

Triggered by services

</td><td>

Indicates which services define the port usage. Use this setting to define non-standard port usage and pair the port number with the protocol.

</td></tr><tr><td>

Use classification

</td><td>

Names the appropriate classification table, based on the protocol being explored.

</td></tr><tr><td>

Classification priority

</td><td>

Establishes the priority in which this port probe runs. If the first port probe fails, then the next probe runs on the device, and so forth, until the correct data is returned. This allows for the proper classification of a device that has two running protocols, such as SSH and SNMP. The default priorities for the Discovery protocols are:

 -   1 - WMI
-   2 - SSH
-   3 - SNMP
-   4 - HTTP

</td></tr><tr><td>

Supplementary

</td><td>

Launches supplementary classifications after a higher-priority identification succeeds, in order of priority.

</td></tr><tr><td>

Conditional

</td><td>

Runs this port probe if any one of the non-conditional probes returns an open port. The conditional port probes in the base system attempt to resolve the names of Windows devices and DNS names. These ports probes take additional resources and are not used unless activity is detected on open ports.

</td></tr><tr><td>

Script

</td><td>

Script to run.

</td></tr></tbody>
</table>-   **[Shazzam probe, port probes, and protocols](r_DiscoveryPortsAndProtocols.md)**  
Port scanning is the first step in the discovery process. The Shazzam probe performs port scanning, regardless of whether you use patterns for horizontal discovery. The following table lists the known ports and protocols used by Discovery.
-   **[Configure Shazzam probe](../task/t_ConfigureTheShazzamProbe.md#)**  
When you run Discovery, the Shazzam probe finds your active network devices by scanning specified ports on specified IP address ranges. If the list of IP ranges being scanned is large, you can configure the Shazzam payload for JSON encoding to reduce its size.

**Parent Topic:**[List of Discovery probes](r_ListOfDiscoveryProbes.md)

