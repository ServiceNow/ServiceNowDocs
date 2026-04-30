---
title: List of Discovery probes
description: A wide variety of probes exist for the Discovery application to detect elements on your network.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# List of Discovery probes

A wide variety of probes exist for the Discovery application to detect elements on your network.

These probes are included with the Discovery application.

The PPP script designation in the table indicates whether the probe includes a probe post-processing \(PPP\) script that runs on the MID Server. The PPP script transforms probe results into a JSON string and returns the string to the ServiceNow instance for sensor processing.

To view probes and their descriptions, navigate to **Discovery Definition** &gt; **Probes**.

-   **[CIM probe](r_CIMProbe.md#)**  
The CIM probe uses WBEM protocols to query a particular CIM server, the CIM Object Manager, for a set of data objects and properties.
-   **[DNS probe](dns-discovery-probe.md)**  
DNS probes determine the DNS names for configuration items \(CI\).
-   **[Horizontal Pattern probe](r-HorizontalPatternProbe.md)**  
Discovery uses the Horizontal Pattern probe to launch patterns for horizontal discovery.
-   **[PowerShell probe](../concept/c_PowershellProbe.md)**  
The PowerShell Probe executes PowerShell V2 scripts on the MID Server host.
-   **[SCPRelay probe](r_SCPRelayProbe.md)**  
The SCP Relay Probe copies a single file or the contents of a directory from one host to another, using the MID Server as a relay.
-   **[SNMP probes](../concept/c_SNMPProbe.md)**  
The SNMP probes use the SNMP protocol to query a particular device for a list of OIDs, which are then traversed and the results passed back to the sensors. MID Servers support all SNMP protocol versions by default. You can set a MID Server to only support specific versions of SNMP.
-   **[SSHCommand probe](../concept/c_SSHCommandProbe.md)**  
A probe using the ECC queue topic name SSHCommand executes a shell command on the target host, and returns the resulting output to the sensor.
-   **[vCenter probes and probe parameters](vcenter-probes.md#)**  
vCenter probes scan virtual machines using VMware's vSphere product suite. Each probe scans for different kinds of data, such as networks, NICs, and tags. The VMware - vCenter probe that discovered all vCenter objects in previous releases is deprecated in the Istanbul release and replaced by multiple probes.
-   **[Windows probes and permissions](r_DiscoWinProbesAndPermissions.md)**  
Discovery accesses devices and software by executing commands as a specific user on Windows computers.
-   **[WMIRunner probe](r_WMIRunnerProbe.md)**  
WMI Runner is a probe type that fetches data from Windows operating systems via the Windows Management Instrumentation \(WMI\) interface. IPv6 supports WMI Runner.
-   **[Port probes](r_PortProbes.md)**  
Port probes are used in Discovery by the Shazzam probe to detect protocol activity on open ports on devices it encounters.

**Parent Topic:**[Discovery probes and sensors](../concept/c_DiscoveryProbesAndSensors.md)

