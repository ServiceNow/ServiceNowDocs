---
title: ProbeHandlerCim - Global
description: The ProbeHandlerCim script include provides methods to configures a Common Information Model \(CIM\) probe.Returns a string containing the CIM fields to fetchReturns the CIM name space.Returns a hash map of the parameters added by this probe handler.Runs the probe.Sets the probe parameters.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ProbeHandlerCim- Global

The ProbeHandlerCim script include provides methods to configures a Common Information Model \(CIM\) probe.

You can use this script include in any server-side script where you need to configure a CIM probe.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ProbeHandlerCim - getCimQueries\(\)

Returns a string containing the CIM fields to fetch

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The CIM fields to fetch|

## ProbeHandlerCim - getNamespace\(\)

Returns the CIM name space.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The name space|

## ProbeHandlerCim - getParameters\(\)

Returns a hash map of the parameters added by this probe handler.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A hash map of the parameters|

## ProbeHandlerCim - run\(\)

Runs the probe.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerCim - setProbeParameters\(Object params\)

Sets the probe parameters.

|Name|Type|Description|
|----|----|-----------|
|params|Object|The parameters to add|

|Type|Description|
|----|-----------|
|void| |

