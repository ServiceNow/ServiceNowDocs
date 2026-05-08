---
title: Solaris discovery
description: Discovery identifies and classifies information about Solaris computers.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Solaris discovery

Discovery identifies and classifies information about Solaris computers.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Supported operating systems

-   Oracle Solaris 10
-   Oracle Solaris 11

## Prerequisites

Discovery stores data in the \[cmdb\_running\_process\] table with truncated command line parameters up to 80 characters. This can cause multiple applications to be merged into one CI. To get the full command line and prevent this issue, run `pargs -a` and parse the result.

For Discovery to use patterns to find Solaris computers, you must install [SNEEP](https://docs.oracle.com/cd/E35557_01/doc.81/e35226/ch3_sneep.htm#IGSTB131). Otherwise, Discovery cannot find the serial number.

If using Solaris zones, each zone should be configured to return a unique value for the serial number. Otherwise, each zone will return the same number causing issues with CI identification.

**Note:** Solaris discovery only supports local zones installed on the same host as the global zone. If the local zone is installed on a different host from the global zone, the `zoneadm list -cip` command won't retrieve the UUID for the local zone.

Solaris - ADM probe requires installing the LSOF command.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

## Credentials

Configure SSH credentials for the systems you want to discover.

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Classifier, probes, and pattern

<table id="table_g3w_4nf_nbb"><thead><tr><th>

Classifier

</th><th>

Probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Solaris\(UNIX Classification\)

</td><td>

-   Horizontal discovery probe: launches patterns
-   Solaris - Installed Software^
-   Solaris - Identity\*
-   Solaris - CPU\*
-   Solaris - Hardware Model\*
-   Solaris - Memory\*
-   Solaris - Network ARP Tables\*
-   Solaris - OS Patches\*
-   Solaris - Storage\*
-   Solaris - Zones\*
-   Solaris - Disks\*
-   DNS\*

</td><td>

Solaris Server

</td></tr></tbody>
</table>\*For new instances, these probes are inactive on the classifier. Discovery uses patterns for discovery.

^This probe remains active by default, even when Discovery uses pattern discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected

|Label|Table name|Field name|Source|
|-----|----------|----------|------|
|Operating System|cmdb\_ci\_computer|os|uname|
|Short description|cmdb\_ci\_solaris\_server|short\_description|uname|
|Name|cmdb\_ci\_solaris\_server|name|DNS, NBT|
|Hostname|cmdb\_ci\_solaris\_server|host\_name|DNS, NBT|
|DNS domain|cmdb\_ci\_solaris\_server|dns\_domain|DNS|
|Start date|cmdb\_ci\_solaris\_server|start\_date|uptime|
|CPU type|cmdb\_ci\_computer|cpu\_type|kstat|
|CPU speed \(MHz\)|cmdb\_ci\_computer|cpu\_speed|kstat|
|CPU count|cmdb\_ci\_computer|cpu\_count|kstat|
|CPU core count|cmdb\_ci\_computer|cpu\_core\_count|kstat|
|CPU core thread|cmdb\_ci\_computer|cpu\_core\_thread|kstat|
|Model number|cmdb\_ci\_solaris\_server|model\_number|suntype|
|Model ID|cmdb\_ci\_solaris\_server|model\_id|suntype|
|RAM \(MB\)|cmdb\_ci\_computer|ram|prtconf|
|Disk space \(GB\)|cmdb\_ci\_solaris\_server|disk\_space|iostat|
|Serial Number|cmdb\_ci\_solaris\_server|serial\_number|sneep \*|
|Manufacturer|cmdb\_ci\_disk|manufacturer|iostat|
|Model ID|cmdb\_ci\_disk|model\_id|iostat|
|Volume serial number|cmdb\_ci\_disk|volume\_serial\_number|iostat|
|Disk space \(GB\)|cmdb\_ci\_disk|disk\_space|iostat|
|Name|cmdb\_ci\_disk|name|iostat|
|Name|cmdb\_ci\_file\_system|name|df|
|Capacity \(MB\)|cmdb\_ci\_file\_system|capacity|df|
|Available Space \(MB\)|cmdb\_ci\_file\_system|available\_space|df|
|Mount point|cmdb\_ci\_file\_system|mount\_point|df|
|Name|cmdb\_ci\_patches|name|showrev|
|Name|cmdb\_running\_process|name|ps|
|Command|cmdb\_running\_process|command|ps|
|Connects to|cmdb\_running\_process|connects\_to|lsof|
|Listening on|cmdb\_running\_process|listening\_on|lsof|
|Type|cmdb\_running\_process|type|ps|
|PID|cmdb\_running\_process|pid|ps|
|Parameters|cmdb\_running\_process|parameters|ps|
|Name|cmdb\_ci\_network\_adapter|name|ifconfig|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|ifconfig|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|ifconfig|
|Netmask|cmdb\_ci\_network\_adapter|netmask|ifconfig|
|Default gateway|cmdb\_ci\_hardware|default\_gateway|netstat|

\* To discover Fujitsu PRIMEPOWER devices, you must install Oracle SNEEP and run Solaris discovery with root credentials.

## Solaris zone discovery

Discovery maps the relationships between global and local Solaris zones upon detection.

In the following example, a Solaris global zone contains two local zones: zone01 and zone02. Each local zone is represented by a physical Solaris CI record and a Virtual Machine Instance record. Each of the local zones is tied to a Zone Server, demonstrating how virtualization relates to the global zone \(mmp1\).

![Solaris zone relationship map](../image/SolarisZoneMap.png "Solaris zone relationship map")

The TCP connection and process information for local zone servers must be collected by running commands on their parent global zone. The relationship path between the local and global zone physical machines must be established before TCP connection and process information for local zone servers can be collected.

Case 1: Global zone discovered first.

-   The system creates the Solaris server CI for the global zone.
-   Discovery detects the local zones, creates a hypervisor zone server record, and creates a virtual machine instance record for each Solaris device in the local zone.
-   Discovery creates the relationship between the hypervisor record and the VM instance record.

Case 2: Local zone discovered first.

-   The system creates the Solaris server CI for the local zone.
-   Discovery sets the correlation ID, so that it can be reconciled during later global zone discoveries.

Case 3: Global zone discovered after creation of local zone Solaris server CIs.

-   Global zone Discovery detects local zones.
-   Discovery creates a hypervisor zone server record, and creates a virtual machine instance record for each Solaris device in the local zone.
-   Discovery creates the relationship between the hypervisor record and the VM instance record. In addition, it creates the relationship between the physical local zone VM and its virtual machine instance record.
-   The global zone runs the Solaris - ADM probe on itself, filtering by the local zone, and updates the physical local zone VMs with this data.

Case 4: The relationship path between physical local and global zone machines is established.

Subsequent discoveries of the global zone refresh the TCP connection and process information for the contained local zones.

When the system discovers a global zone, the Solaris - Zones &amp; ADM Launcher probe triggers the Solaris - ADM probe to explore the global zone and each local zone found. Because the Solaris - ADM probe must run on the global zone to detect TCP connection and process information from its local zones, you might see multiple ECC queue records that appear identical.

![ECC queue entries for a zone Discovery](../image/ZoneECCQueue.png "ECC queue entries for a zone Discovery")

Upon examining the payload, however, you will see that each probe is actually targeting a different zone CI to filter on and update.

![Local zone payload](../image/Zone01DiscoveryPayload.png "Local zone payload")

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Version|`cmdb_ci_vm_zones`|`version`|zoneadm, zonename|
|Correlation ID|`cmdb_ci_vm_zones`|`correlation_id`|zoneadm, zonename|
|Name|`cmdb_ci_solaris_instance`|`name`|zoneadm, zonename|
|Parent|`cmdb_ci_solaris_instance`|`parent`|Internal|
|CMDB CI|`cmdb_ci_solaris_instance`|`cmdb_ci`|Internal|
|Correlation ID|`cmdb_ci_solaris_instance`|`correlation_id`|zoneadm, zonename|

**Note:** cmdb\_ci\_solaris\_instance extends cmdb\_ci\_vm\_instance.

**Parent Topic:**[Operating systems discovery](../concept/c_Computers.md)

