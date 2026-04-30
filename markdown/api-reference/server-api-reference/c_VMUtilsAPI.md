---
title: VMUtils - Global
description: The VMUtils script include provides methods for discovery and provisioning of virtual machines.Converts a correlation ID into a UUID for a virtual machine in the ServiceNow system.Converts a WMware universal unique identifier \(UUID\) to a format that matches the original format in the ServiceNow system.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# VMUtils- Global

The VMUtils script include provides methods for discovery and provisioning of virtual machines.

This script include is available in server-side scripts to convert between UUID and Correlation ID formats.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## VMUtils - turnCorrelationIdToUuid\(String correlationId\)

Converts a correlation ID into a UUID for a virtual machine in the ServiceNow system.

|Name|Type|Description|
|----|----|-----------|
|correlationId|String|The correlation ID to convert|

|Type|Description|
|----|-----------|
|String|The UUID, or an empty string if invalid.|

```
gs.info(VMUtils.turnCorrelationIdToUuid('42 10 82 82 62 35 ca 68-b5 1c 1e f8 5c 0a 0d 5b'));
```

Output:

```
42108282-6235-ca68-b51c-1ef85c0a0d5b
```

## VMUtils - turnUuidToCorrelationId\(String uuid\)

Converts a WMware universal unique identifier \(UUID\) to a format that matches the original format in the ServiceNow system.

vCenter works with UUIDs where the ESXi Linux console worked with this format.

|Name|Type|Description|
|----|----|-----------|
|uuid|String|The UUID to convert.|

|Type|Description|
|----|-----------|
|String|The identifier converted to the ServiceNow format.|

```
gs.info(VMUtils.turnUuidToCorrelationId('13eb78d0-d504-11e1-9b23-0800200c9a66'));
```

Output:

```
13 eb 78 d0 d5 04 11 e1-9b 23 08 00 20 0c 9a 66
```

