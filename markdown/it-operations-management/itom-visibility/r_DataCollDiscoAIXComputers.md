---
title: AIX server discovery
description: Discovery identifies and classifies information about AIX servers.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# AIX server discovery

Discovery identifies and classifies information about AIX servers.

## Credentials

Configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

Use OpenSSH version 7.5.102 and above for AIX machines since lower versions of OpenSSH can impact the discovered devices that are encountered with Discovery.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Classifier, probes, and pattern

<table id="table_vdg_xb1_nbb"><thead><tr><th>

Classifier

</th><th>

Probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

AIX \(UNIX Classification\)

</td><td>

-   Horizontal discovery probe: launches patterns
-   AIX - Installed Software^
-   AIX - ADM^
-   AIX - Identity\*
-   AIX - CPU\*
-   AIX - Hardware Model\*
-   AIX - Memory\*
-   AIX - OS Patches\*
-   AIX - OS Release\*
-   AIX - OS Revision\*
-   UNIX - Find FQDN
-   UNIX - OS Filesystems
-   UNIX - OS Uptime

</td><td>

AIX server

</td></tr></tbody>
</table>\*These probes aren't active on the classifier, as Discovery uses patterns by default for these discoveries.

^These probes remain active by default, even when Discovery uses pattern discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Operating System|cmdb\_ci\_computer|os|uname|
|OS version|cmdb\_ci\_computer|os\_version|oslevel|
|OS service pack|cmdb\_ci\_computer|os\_service\_pack|oslevel|
|Short description|cmdb\_ci\_aix\_server|short\_description|uname|
|Name|cmdb\_ci\_aix\_server|name|DNS, NBT|
|Hostname|cmdb\_ci\_aix\_server|host\_name|DNS, NBT|
|DNS domain|cmdb\_ci\_aix\_server|dns\_domain|DNS|
|Start date|cmdb\_ci\_aix\_server|start\_date|uptime|
|CPU type|cmdb\_ci\_computer|cpu\_type|lsdev, lsattr|
|CPU speed \(MHz\)|cmdb\_ci\_computer|cpu\_speed|lsdev, lsattr|
|CPU count|cmdb\_ci\_computer|cpu\_count|lsdev, lsattr|
|Manufacturer|cmdb\_ci\_aix\_server|manufacturer|lsattr|
|Model ID|cmdb\_ci\_aix\_server|model\_id|lsattr|
|RAM \(MB\)|cmdb\_ci\_computer|ram|lsdev, lsattr|
|Name|cmdb\_ci\_file\_system|name|df|
|Capacity \(MB\)|cmdb\_ci\_file\_system|capacity|df|
|Available Space \(MB\)|cmdb\_ci\_file\_system|available\_space|df|
|Mount point|cmdb\_ci\_file\_system|mount\_point|df|
|Name|cmdb\_ci\_patches|name|instfix|
|Name|cmdb\_running\_process|name|ps|
|Command|cmdb\_running\_process|command|ps|
|Connects to|cmdb\_running\_process|connects\_to|lsof|
|Listening on|cmdb\_running\_process|listening\_on|lsof|
|Type|cmdb\_running\_process|type|ps|
|PID|cmdb\_running\_process|pid|ps|
|Parameters|cmdb\_running\_process|parameters|ps|
|Name|cmdb\_ci\_network\_adapter|name|ifconfig, netstat|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|ifconfig, netstat|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|ifconfig, netstat|
|Netmask|cmdb\_ci\_network\_adapter|netmask|ifconfig, netstat|

**Parent Topic:**[Operating systems discovery](../concept/c_Computers.md)

