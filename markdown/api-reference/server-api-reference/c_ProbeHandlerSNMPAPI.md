---
title: ProbeHandlerSNMP - Global
description: The ProbeHandlerSNMP script include is a discovery probe handler for SNMP probes, invoked when an SNMP probe is about to be created.Adds a boolean value to the parameter map.Adds debugging to the probe handler.Adds a JavaScript handler.Adds OID automatic resolution.Adds OID specifications to the parameter map.Adds a sensor handler.Adds the stage to the parameter map.Adds timing specifications to the parameter map.Returns the parameters added by this probe handler.Runs the probe.Sets the value of a given XML parameter element.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ProbeHandlerSNMP- Global

The ProbeHandlerSNMP script include is a discovery probe handler for SNMP probes, invoked when an SNMP probe is about to be created.

You can use this script include in any server-side script where you need to configure an SNMP probe.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ProbeHandlerSNMP - addBoolean\(String dbName, String paramName, String paramMap\)

Adds a boolean value to the parameter map.

|Name|Type|Description|
|----|----|-----------|
|dbName|String|The database name|
|paramName|String|The parameter name|
|paramMap|String|The parameter map|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - addDebug\(String paramMap\)

Adds debugging to the probe handler.

|Name|Type|Description|
|----|----|-----------|
|paramMap|String|The parameter map|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - addJavascriptHandlers\(String paramMap\)

Adds a JavaScript handler.

|Name|Type|Description|
|----|----|-----------|
|paramMap|String|The parameter map|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - addOIDAutoResolve\(String paramMap\)

Adds OID automatic resolution.

|Name|Type|Description|
|----|----|-----------|
|paramMap|String|The parameter map|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - addOIDSpec\(String paramMap\)

Adds OID specifications to the parameter map.

|Name|Type|Description|
|----|----|-----------|
|paramMap|String|The parameter map|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - addSensorHandler\(String paramMap\)

Adds a sensor handler.

|Name|Type|Description|
|----|----|-----------|
|paramMap|String|The parameter map|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - addStage\(String paramMap\)

Adds the stage to the parameter map.

|Name|Type|Description|
|----|----|-----------|
|paramMap|String|The parameter map|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - addTimingSpecs\(String paramMap\)

Adds timing specifications to the parameter map.

|Name|Type|Description|
|----|----|-----------|
|paramMap|String|The parameter map|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - getParameters\(\)

Returns the parameters added by this probe handler.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A hash map of the parameters added by this probe handler.|

## ProbeHandlerSNMP - run\(\)

Runs the probe.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerSNMP - setProbeParameters\(String params\)

Sets the value of a given XML parameter element.

|Name|Type|Description|
|----|----|-----------|
|params|String|The probe's parameters|

|Type|Description|
|----|-----------|
|void| |

