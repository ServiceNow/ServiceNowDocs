---
title: Mac \(OS/X\) discovery
description: Discovery identifies and classifies information about Mac \(OS/X\) computers.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Mac \(OS/X\) discovery

Discovery identifies and classifies information about Mac \(OS/X\) computers.

## Credentials

Configure SSH credentials.

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Data collected

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Operating System|cmdb\_ci\_computer|os|uname|
|OS Version|cmdb\_ci\_computer|os\_version|system\_profiler|
|OS Service pack|cmdb\_ci\_computer|os\_service\_pack|system\_profiler|
|Short description|cmdb\_ci\_computer|short\_description|uname|
|Name|cmdb\_ci\_computer|name|DNS, NBT|
|Hostname|cmdb\_ci\_computer|host\_name|DNS, NBT|
|DNS domain|cmdb\_ci\_computer|dns\_domain|DNS|
|Start date|cmdb\_ci\_computer|start\_date|uptime|
|Manufacturer|cmdb\_ci\_computer|manufacturer|Assumed to be Apple|
|Serial number|cmdb\_ci\_computer|serial\_number|system\_profiler|
|CPU type|cmdb\_ci\_computer|cpu\_type|system\_profiler|
|CPU speed \(MHz\)|cmdb\_ci\_computer|cpu\_speed|system\_profiler|
|CPU count|cmdb\_ci\_computer|cpu\_count|system\_profiler|
|Model ID|cmdb\_ci\_computer|model\_id|system\_profiler|
|RAM \(MB\)|cmdb\_ci\_computer|ram|system\_profiler|
|Disk space \(GB\)|cmdb\_ci\_computer|disk\_space|system\_profiler|
|Volume name|cmdb\_ci\_disk|volume\_name|system\_profiler|
|Volume serial number|cmdb\_ci\_disk|volume\_serial\_number|system\_profiler|
|Disk space \(GB\)|cmdb\_ci\_disk|disk\_space|system\_profiler|
|Name|cmdb\_ci\_disk|name|system\_profiler|
|Device ID|cmdb\_ci\_disk|device\_id|system\_profiler|
|Free space \(GB\)|cmdb\_ci\_disk|free\_space|system\_profiler|
|File system|cmdb\_ci\_disk|file\_system|system\_profiler|
|Name|cmdb\_running\_process|name|ps|
|Command|cmdb\_running\_process|command|ps|
|Connects to|cmdb\_running\_process|connects\_to|lsof|
|Listening on|cmdb\_running\_process|listening\_on|lsof|
|PID|cmdb\_running\_process|pid|ps|
|Parameters|cmdb\_running\_process|parameters|ps|
|Name|cmdb\_ci\_network\_adapter|name|system\_profiler|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|system\_profiler|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|system\_profiler|
|Netmask|cmdb\_ci\_network\_adapter|netmask|system\_profiler|
|MAC manufacturer|cmdb\_ci\_network\_adapter|mac\_mfr|Assumed to be Apple|
|DHCP enabled|cmdb\_ci\_network\_adapter|dhcp\_enabled|system\_profiler|

**Parent Topic:**[Operating systems discovery](../concept/c_Computers.md)

