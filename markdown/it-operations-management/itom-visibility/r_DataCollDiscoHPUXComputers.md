---
title: HP-UX discovery
description: Discovery identifies and classifies information about HP-UX computers.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# HP-UX discovery

Discovery identifies and classifies information about HP-UX computers.

## Credentials

Configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Classifier, probes, and pattern

<table id="table_dnx_5lf_nbb"><thead><tr><th>

Classifier

</th><th>

Probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

HP-UX\(Unix classifier\)

</td><td>

-   Horizontal discovery probe: launches patterns
-   HP-UX - Installed Software^
-   HP-UX - ADM^
-   HP-UX - OS Patches\*
-   HP-UX - CPU Speed\*
-   HP-UX - Total Memory\*
-   HP-UX - Hardware Model\*
-   HP-UX - CPU Info\*
-   HP-UX - Identity\*
-   UNIX - Find FQDN\*
-   UNIX - OS Filesystems\*
-   UNIX - OS Uptime\*

</td><td>

HP-UX Server

</td></tr></tbody>
</table>\*These probes aren't active on the classifier, as Discovery uses patterns by default for these discoveries.

^These probes remain active by default, even when Discovery uses pattern discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Operating System|cmdb\_ci\_hpux\_server|os|uname|
|Short description|cmdb\_ci\_hpux\_server|short\_description|uname|
|Name|cmdb\_ci\_hpux\_server|name|DNS, NBT|
|Hostname|cmdb\_ci\_hpux\_server|host\_name|DNS, NBT|
|DNS domain|cmdb\_ci\_hpux\_server|dns\_domain|DNS|
|Start date|cmdb\_ci\_hpux\_server|start\_date|uptime|
|Manufacturer|cmdb\_ci\_computer|manufacturer|dmidecode|
|Serial number|cmdb\_ci\_hpux\_server|serial\_number|uname|
|CPU type|cmdb\_ci\_hpux\_server|cpu\_type|cpuinfo|
|CPU speed \(MHz\)|cmdb\_ci\_hpux\_server|cpu\_speed|adb|
|CPU count|cmdb\_ci\_hpux\_server|cpu\_count|cpuinfo|
|Model ID|cmdb\_ci\_hpux\_server|model\_id|model|
|RAM \(MB\)|cmdb\_ci\_hpux\_server|ram|adb|
|Name|cmdb\_ci\_file\_system|name|df|
|Capacity \(MB\)|cmdb\_ci\_file\_system|capacity|df|
|Available Space \(MB\)|cmdb\_ci\_file\_system|available\_space|df|
|Mount point|cmdb\_ci\_file\_system|mount\_point|df|
|Name|cmdb\_ci\_patches|name|swlist|
|Name|cmdb\_running\_process|name|ps|
|Command|cmdb\_running\_process|command|ps|
|Type|cmdb\_running\_process|type|ps|
|PID|cmdb\_running\_process|pid|ps|
|Parameters|cmdb\_running\_process|parameters|ps|
|Name|cmdb\_ci\_network\_adapter|name|hifconfig|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|hifconfig|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|hifconfig|
|Netmask|cmdb\_ci\_network\_adapter|netmask|hifconfig|

**Parent Topic:**[Operating systems discovery](../concept/c_Computers.md)

