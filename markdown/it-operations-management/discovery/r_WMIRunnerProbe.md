---
title: WMIRunner probe
description: WMI Runner is a probe type that fetches data from Windows operating systems via the Windows Management Instrumentation \(WMI\) interface. IPv6 supports WMI Runner.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# WMIRunner probe

WMI Runner is a probe type that fetches data from Windows operating systems via the Windows Management Instrumentation \(WMI\) interface. IPv6 supports WMI Runner.

The probe handles multiple user-specified WMI Paths to be queried, using a basic form of native WMI query. Each field to be probed must be uniquely named \(within the domain of the probe\). The probe results returned to the sensor will provide the data found for each field queried, indexed by its name.

When creating a WMI probe, the probe type must be set to WMI Probe and the ECC Queue Topic must be set to WMIRunner.

For instructions on configuring probe parameters, see [Set probe parameters](../task/t_SetProbeParameters.md).

The following parameters may be passed to the WMI Probe:

|Parameter|Description|Default value|
|---------|-----------|-------------|
|source|Host to connect to.| |
|port|Port to connect to.| |
|debug|Enables debug logging.|false|
|wmi\_timeout|Timeout for the actual WMI probe, in seconds. Use this parameter to change the timeout interval for individual Windows probes. This value overrides the value in the windows\_probe\_timeout MID Server parameter, which sets a timeout for all probes launched by a specific MID Server. Windows - Installed Software probe is configured with a timeout value of 15 minutes.|300 \(seconds\)|
|process\_timeout|Timeout for the process running the script, in seconds. This parameter is for internal use only and is not supported.|wmi\_timeout + 10 \(seconds\)|
|credentials\_debug|Displays a &lt;credentials\_debug&gt; section in the ECC queue, which can help you troubleshoot credentials. If you set this property to true, credential troubleshooting information is output to the ECC queue, even if the credentials succeed. See Credentials troubleshooting for more information.|false|

**Note:** The default timeout for WMI/Powershell is 5 minutes, except for the Windows Installed Software probe, which has a default timeout value of 15 minutes. Adding **wmi\_timeout** to a probe parameter can change the default timeout of a Windows probe.

**Parent Topic:**[List of Discovery probes](r_ListOfDiscoveryProbes.md)

