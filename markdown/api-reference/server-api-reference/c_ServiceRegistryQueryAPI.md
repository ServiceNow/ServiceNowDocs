---
title: ServiceRegistryQuery - Global
description: The ServiceRegistryQuery script include provides methods to map Shazzam service registry query results against a port probe. Child classes provide specifics on mapping.Creates an instance of the ServiceRegistryQuery class.Parses an array of IDs for the given port probe.Retrieves a registry service by id, regardless of child class.Returns the Shazzam! querier class name.Retrieves the port probe XML and creates a map.Creates XML output for Shazzam! port probes.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ServiceRegistryQuery- Global

The ServiceRegistryQuery script include provides methods to map Shazzam service registry query results against a port probe. Child classes provide specifics on mapping.

Use this script include during the discovery scanning phase.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ServiceRegistryQuery - ServiceRegistryQuery\(Object source\)

Creates an instance of the ServiceRegistryQuery class.

|Name|Type|Description|
|----|----|-----------|
|source|Object|A GlideRecord or sys\_id of the registry service.|

## ServiceRegistryQuery - findForPortProbe\(PortProbe portProbe\)

Parses an array of IDs for the given port probe.

|Name|Type|Description|
|----|----|-----------|
|portProbe|PortProbe|The port probe|

|Type|Description|
|----|-----------|
|void| |

## ServiceRegistryQuery - get\(Object source\)

Retrieves a registry service by id, regardless of child class.

|Name|Type|Description|
|----|----|-----------|
|source|Object|The registry service GlideRecord or sys\_id.|

|Type|Description|
|----|-----------|
|String|The registry service|

## ServiceRegistryQuery - getShazzamQuerierClassname\(\)

Returns the Shazzam! querier class name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The class name|

## ServiceRegistryQuery - toPortProbeMap\(\)

Retrieves the port probe XML and creates a map.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The port probe map|

## ServiceRegistryQuery - toPortProbeXml\(\)

Creates XML output for Shazzam! port probes.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The XML output for the probe.|

