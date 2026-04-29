---
title: ProbeHandlerWMI - Global
description: The ProbeHandlerWMI script include is the discovery probe handler for Windows Management Instrumentation \(WMI\) probes.Returns the parameters added by this probe handler.Generates a string containing the WMI fields to fetch.Runs the probe.Sets the probe parameters.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ProbeHandlerWMI- Global

The ProbeHandlerWMI script include is the discovery probe handler for Windows Management Instrumentation \(WMI\) probes.

You can use this script include in any server-side script where you need to configure an WMI probe.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ProbeHandlerWMI - getParameters\(\)

Returns the parameters added by this probe handler.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A hash map of the parameters added by this probe|

## ProbeHandlerWMI - getWMIFields\(\)

Generates a string containing the WMI fields to fetch.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The WMI fields to fetch.|

## ProbeHandlerWMI - run\(\)

Runs the probe.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerWMI - setProbeParameters\(Object params\)

Sets the probe parameters.

|Name|Type|Description|
|----|----|-----------|
|params|Object|The probe parameters|

|Type|Description|
|----|-----------|
|void| |

