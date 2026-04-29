---
title: StartDiscovery - Global
description: The StartDiscovery script include provides methods to start discovery jobs.Adds an IP \(or comma-separated list of IPs\) to an existing discovery \(used by networks discovery\).Handles discovery of devices \(whether basic or advanced\) from a schedule.Returns the cancel script.If the schedule specifies a cancel time, if necessary, schedules a job to cancel the discovery.Starts a discovery for a single IP using the specified schedule to get information such as MID servers and behaviors.Invoked by the discovery script include to kick off a scheduled \(or discover now\) discovery.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# StartDiscovery- Global

The StartDiscovery script include provides methods to start discovery jobs.

Use this script include during the discovery scanning phase.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## StartDiscovery - addAdditionalIP\(String status, String ip, String sensor\)

Adds an IP \(or comma-separated list of IPs\) to an existing discovery \(used by networks discovery\).

|Name|Type|Description|
|----|----|-----------|
|status|String|The discovery status|
|ip|String|An IP address, or a comma-separated list of IP addresses.|
|sensor|String|The discovery sensor|

|Type|Description|
|----|-----------|
|void| |

## StartDiscovery - discoverFromSchedule\(String ip, Boolean samePhase, String sensor\)

Handles discovery of devices \(whether basic or advanced\) from a schedule.

|Name|Type|Description|
|----|----|-----------|
|ip|String|An IP address, or a comma-separated list of IP addresses.|
|samePhase|Boolean| |
|sensor|String|The discovery sensor|

|Type|Description|
|----|-----------|
|void| |

## StartDiscovery - getCancelScript\(\)

Returns the cancel script.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The cancel script|

## StartDiscovery - scheduleCancelJob\(\)

If the schedule specifies a cancel time, if necessary, schedules a job to cancel the discovery.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

The following example shows how to use the scheduleCancelJob\(\) method to cancel a current discovery job.

```
var discoveryScheduleGR = new GlideRecord('discovery_schedule'); // Create a discovery schedule Gliderecord
discoveryScheduleGR.get('name', 'Disco'); // Put the discovery schedule job name

var discoverySchedule = new DiscoverySchedule(discoveryScheduleGR); 
var discoveryStatusSysId = new StartDiscovery().startFromIP(discoverySchedule, '172.167.31.231'); // Initiate discovery
gs.info(discoveryStatusSysId); // Display the sys_id of the discovery status record

discoveryStatusSysId.scheduleCancelJob(); // Schedule a cancel job, located in the sys_trigger table

```

Output:

```
Operation	Table		Row Count
insert		discovery_result	1
update		discovery_status	1
insert		sys_trigger	     1
insert		discovery_status	1
*** Script: Fired started event for: undefined Disco
*** Script: Scheduling Discovery DIS0010023 for cancellation at 2022-02-13 16:42:44
*** Script: 1828b05f1b6d811070cb96c6b04bcb53
```

## StartDiscovery - startFromIP\(DiscoverySchedule schedule, String ip\)

Starts a discovery for a single IP using the specified schedule to get information such as MID servers and behaviors.

<table id="table_elc_1cv_tt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

schedule

</td><td>

DiscoverySchedule

</td><td>

DiscoverySchedule instance for the schedule to use.

</td></tr><tr><td>

ip

</td><td>

String

</td><td>

IP address to discover.Format: dot-formatted string

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the status record created.|

This example uses the startFromIP\(\) method to obtain the record that contains the discover information.

```
// Get a discovery schedule gliderecord
var discoveryScheduleGR = new GlideRecord('discovery_schedule'); 
discoveryScheduleGR.get('name', 'Discover Management Range 172.x.x.x');

// Create a DiscoverySchedule object to get information such as MID servers and behaviors
var discoverySchedule = new DiscoverySchedule(discoveryScheduleGR); 
var discoveryStatusSysId = new StartDiscovery().startFromIP(discoverySchedule, '172.1.1.10');
 
// Sys_id of the genterated status record
gs.info(discoveryStatusSysId);
```

Output:

```
9d3c1197c611228701cd1d94bc32d76d
```

## StartDiscovery - startFromSchedule\(GlideRecord schedule, GlideRecord job\)

Invoked by the discovery script include to kick off a scheduled \(or discover now\) discovery.

|Name|Type|Description|
|----|----|-----------|
|schedule|GlideRecord|The instance of discovery\_schedule that this discovery is based on.|
|job|GlideRecord|The instance of sys\_trigger that triggered this discovery.|

|Type|Description|
|----|-----------|
|void| |

