---
title: SNMPGatherDocParts - Global
description: The SNMPGatherDocParts script include provides methods to handle the gathering of parts of an SNMP response document for JavaScript SNMP sensors.Returns the given XML document with any data gathered by prior SNMP probes.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SNMPGatherDocParts- Global

The SNMPGatherDocParts script include provides methods to handle the gathering of parts of an SNMP response document for JavaScript SNMP sensors.

Use this script include in a discovery script when you need to gather the parts of an SNMP response document.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SNMPGatherDocParts - gather\(String doc, Object probe\)

Returns the given XML document with any data gathered by prior SNMP probes.

|Name|Type|Description|
|----|----|-----------|
|doc|String|The XML document for this sensor|
|probe|Object|The probe instance|

|Type|Description|
|----|-----------|
|String|The XML document with the gathered data.|

