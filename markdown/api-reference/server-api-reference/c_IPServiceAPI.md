---
title: IPService - Global
description: The IPService script include provides methods that encapsulate an IP Service.Creates an instance of the IPService class.The table where this service creates entries.Description of the IPService.Returns an array of IPService instances specified by a Java ArrayList of sys\_ids.The TCP or UDP port used by the service.The protocol used by the service \("UDP", "TCP", or "TCP/UDP"\).A short name or handle for the IPService.A long, descriptive English name for the IPService.The sys\_id of this record.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# IPService- Global

The IPService script include provides methods that encapsulate an IP Service.

Use this class during the discovery scanning phase.

See also [AbstractDBObject - isValid\(\)](../../AbstractDBObject/concept/c_AbstractDBObject.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## IPService - IPService\(Object source\)

Creates an instance of the IPService class.

|Name|Type|Description|
|----|----|-----------|
|source|Object|Either a GlideRecord instance or a sys\_id string|

## IPService - creates

The table where this service creates entries.

|Name|Type|Description|
|----|----|-----------|
|creates|String|The table where this service creates entries.|

## IPService - description

Description of the IPService.

|Name|Type|Description|
|----|----|-----------|
|description|String|Description of the IPService.|

## IPService - getFromArrayList\(Array list\)

Returns an array of IPService instances specified by a Java ArrayList of sys\_ids.

|Name|Type|Description|
|----|----|-----------|
|list|Array|List of sys\_ids.|

|Type|Description|
|----|-----------|
|Array|IPService instances|

## IPService - port

The TCP or UDP port used by the service.

|Name|Type|Description|
|----|----|-----------|
|port|String|The TCP or UDP port used by the service.|

## IPService - protocol

The protocol used by the service \("UDP", "TCP", or "TCP/UDP"\).

|Name|Type|Description|
|----|----|-----------|
|protocol|String|The protocol used by the service \("UDP", "TCP", or "TCP/UDP"\).|

## IPService - name

A short name or handle for the IPService.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the IPService|

## IPService - serviceName

A long, descriptive English name for the IPService.

|Name|Type|Description|
|----|----|-----------|
|serviceName|String|A long, descriptive English name for the IPService.|

## IPService - sysID

The sys\_id of this record.

|Name|Type|Description|
|----|----|-----------|
|sysID|String|The sys\_id of this record.|

