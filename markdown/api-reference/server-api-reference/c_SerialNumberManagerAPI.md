---
title: SerialNumberManager - Global
description: The SerialNumberManager script include provides methods to manage the serial numbers for discovery devices.Adds the specified serial number.Returns the serial number.Returns serial number information for CI Data, including the type, serial number, and validity.Checks if the number is a valid serial number.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SerialNumberManager- Global

The SerialNumberManager script include provides methods to manage the serial numbers for discovery devices.

You can use this script include with a discovery script where you need to manage serial numbers.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SerialNumberManager - add\(Number sType, Number value\)

Adds the specified serial number.

|Name|Type|Description|
|----|----|-----------|
|sType|Number|The serial number type|
|value|Number|The serial number|

|Type|Description|
|----|-----------|
|void| |

## SerialNumberManager - getSerialNumber\(\)

Returns the serial number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The serial number.|

## SerialNumberManager - getSerialsForCIData\(\)

Returns serial number information for CI Data, including the type, serial number, and validity.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array with the serial number information in the following order: serial number type, serial number, and validity flag.|

## SerialNumberManager - isValid\(Number value\)

Checks if the number is a valid serial number.

|Name|Type|Description|
|----|----|-----------|
|value|Number|The number to check|

|Type|Description|
|----|-----------|
|Boolean|True if the number is valid; otherwise, false.|

