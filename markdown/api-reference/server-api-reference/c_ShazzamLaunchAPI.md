---
title: ShazzamLaunch - Global
description: The ShazzamLaunch script include provides methods to handle the details of launching a Shazzam probe for a given discovery.Creates an instance of the Shazzamlaunch class.Adds a single port probe to our MID services collection.Adds the specified range and this discovery's port probes to scan \(as defined by behavior\) to the collection of MID servers and port probes that need to be probed.Fires a Shazzam probe for the MID server and services in the given hash map.Launches Shazzam probes as necessary, depending on the current phase of each behavior used.Makes an XML port probe spec for the given port probe hashmap.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ShazzamLaunch- Global

The ShazzamLaunch script include provides methods to handle the details of launching a Shazzam probe for a given discovery.

Use this script include to launch a Shazzam probe during the discovery scanning phase.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ShazzamLaunch - ShazzamLaunch\(DiscoveryStatus status, DiscoverySchedule schedule\)

Creates an instance of the Shazzamlaunch class.

|Name|Type|Description|
|----|----|-----------|
|status|DiscoveryStatus|The DiscoveryStatus instance for this discovery.|
|schedule|DiscoverySchedule|The DiscoverySchedule instance for this discovery.|

|Type|Description|
|----|-----------|
|void| |

## ShazzamLaunch - addPortProbe\(String midPPs, String portProbes, IPIncludeExcluldeCollection ipiec\)

Adds a single port probe to our MID services collection.

<table id="table_cmr_fjp_tt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

midPPs

</td><td>

String

</td><td>

A hashmap with two properties. -   midServer: a MIDServer instance
-   portProbes: a hashmap \(by port probe name\) of DiscoveryPortProbe instances.

</td></tr><tr><td>

portProbes

</td><td>

String

</td><td>

A hashmap \(byMIDServer name\) that contains these properties. -   range: An IPMetaCollection containing the ranges to be probed.
-   midserver: A MIDServer instance for the MID server to be probed.
-   portProbes: a hashmap \(by port probe name\) of DiscoveryPortProbe instances to be probed.

</td></tr><tr><td>

ipiec

</td><td>

IPIncludeExcludeCollection

</td><td>

The range to be probed.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## ShazzamLaunch - addRange\(IPCollection ipc, String portProbes, Boolean samePhase\)

Adds the specified range and this discovery's port probes to scan \(as defined by behavior\) to the collection of MID servers and port probes that need to be probed.

<table id="table_ptp_j3p_tt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ipc

</td><td>

IPCollection

</td><td>

The range to be discovered

</td></tr><tr><td>

portProbes

</td><td>

String

</td><td>

A hashmap \(by MID server name\) of hashmaps containing these properties. -   range: an IPMetaCollection containing the ranges to be probed.
-   midServer: a Mid server instance for the MID server to be probed.
-   portProbes: a hashmap \(by port probe name\) of DiscoveryPortProbe instances to be probed.

</td></tr><tr><td>

samePhase

</td><td>

Boolean

</td><td>

True if this should use the same phase as is currently running.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## ShazzamLaunch - fireShazzamProbe\(String portProbe, String ip, String sensor\)

Fires a Shazzam probe for the MID server and services in the given hash map.

<table id="table_fnj_jkp_tt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

portProbe

</td><td>

String

</td><td>

A hashmap containing these properties.-   range: an IPMetaCollection containing the ranges to be probed.
-   midServer: a MIDServer instance for the MID server to be probed.

</td></tr><tr><td>

ip

</td><td>

String

</td><td>

A comma-separated list of IPs to fire probes for.

</td></tr><tr><td>

sensor

</td><td>

String

</td><td>

The sys\_id of the sensor that launched this probe \(network discovery only\).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

## ShazzamLaunch - launch\(String ip, Boolean samePhase, String sensor\)

Launches Shazzam probes as necessary, depending on the current phase of each behavior used.

|Name|Type|Description|
|----|----|-----------|
|ip|String|A comma-separated list of IPs to fire probes for.|
|samePhase|Boolean|True if this launch should use the same phase as is currently running.|
|sensor|String|The sys\_id of the sensor that launched this \(only in network discovery\).|

|Type|Description|
|----|-----------|
|Boolean|True if any probes are launched.|

## ShazzamLaunch - makeProbeSpec\(String portProbe\)

Makes an XML port probe spec for the given port probe hashmap.

<table id="table_cnc_nlp_tt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

portProbe

</td><td>

String

</td><td>

A hashmap containing these properties.-   range: an IPMetaCollection containing the ranges to be probed.
-   midServer: a MIDServer instance for the MID server to be probed.
-   portProbes: a hashmap \(by port probe name\) of DiscoveryPortProbe instances to be probed.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|An XML port probe specification|

