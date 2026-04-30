---
title: SNMPNetworkInterfaces - Global
description: The SNMPNetworkInterfaces script include provides methods to create network interfaces for JavaScript SNMP sensors.Analyzes the SNMP data and reconciles the discovered NICs to the CMDB's NICs.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SNMPNetworkInterfaces- Global

The SNMPNetworkInterfaces script include provides methods to create network interfaces for JavaScript SNMP sensors.

Use this script include in discovery scripts when you need to create network interfaces for JavaScript SNMP sensors.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SNMPNetworkInterfaces - process\(String cmdb\_ci, String doc, Boolean isComputer, String agentName, String ecc\_sys\_id\)

Analyzes the SNMP data and reconciles the discovered NICs to the CMDB's NICs.

|Name|Type|Description|
|----|----|-----------|
|cmdb\_ci|String|The sys\_id of the CI|
|doc|String|The SNMP data in XML form|
|isComputer|Boolean|If true, this is a computer; otherwise, false.|
|agentName|String|Name of the MID server|
|ecc\_sys\_id|String|The sys\_id of the ECC queue record with the input.|

|Type|Description|
|----|-----------|
|void| |

