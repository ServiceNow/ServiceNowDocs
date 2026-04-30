---
title: CimIDSensor - Global
description: The CimIDSensor script include provides methods to perform identification for Common Information Model \(CIM\) probe results.Configures a triggered probe before it is launched.Gets the instance hash token.Prepares the probe results.Processes all CIM probe query results for a CIM ID sensor.Runs a multi-probe script against a probe result.Updates the device count.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CimIDSensor- Global

The CimIDSensor script include provides methods to perform identification for Common Information Model \(CIM\) probe results.

Use in any server-side script to perform identification of CIM probe results.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CimIDSensor - configureTriggeredProbe\(String probe\)

Configures a triggered probe before it is launched.

|Name|Type|Description|
|----|----|-----------|
|probe|String|An already configured probe that is ready to fire.|

|Type|Description|
|----|-----------|
|Boolean|True to fire this probe, false to skip it.|

## CimIDSensor - getInstanceHashToken\(\)

Gets the instance hash token.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The hash token|

## CimIDSensor - prepare\(\)

Prepares the probe results.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## CimIDSensor - process\(Object results, CimCIData cimData, CimIDSensor sensor\)

Processes all CIM probe query results for a CIM ID sensor.

|Name|Type|Description|
|----|----|-----------|
|results|Object|The query results|
|cimData|CimCIData|The CI data of the device being identified.|
|sensor|CimIDSensor|The wrapping sensor, extends CimIDSensor|

|Type|Description|
|----|-----------|
|void| |

## CimIDSensor - runMultiProbeScript\(String script, Object probeResult, String probeRecord\)

Runs a multi-probe script against a probe result.

|Name|Type|Description|
|----|----|-----------|
|script|String|The script|
|probeResult|Object|The probe result|
|probeRecord|String|The probe ID|

|Type|Description|
|----|-----------|
|void| |

## CimIDSensor - updateDeviceCount\(\)

Updates the device count.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

