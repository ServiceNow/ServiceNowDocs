---
title: RoundingInterval - Global
description: The RoundingInterval script include provides methods that handle all the details of rounding intervals for CPU speed and RAM size.Creates an instance of the RoundingInterval class.Returns the value after applying the rounding interval.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RoundingInterval- Global

The RoundingInterval script include provides methods that handle all the details of rounding intervals for CPU speed and RAM size.

Use in any server-side Discovery script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RoundingInterval - RoundingInterval\(String type\)

Creates an instance of the RoundingInterval class.

|Name|Type|Description|
|----|----|-----------|
|type|String|Can be either CPU or RAM.|

## RoundingInterval - getRoundedValue\(Number value\)

Returns the value after applying the rounding interval.

|Name|Type|Description|
|----|----|-----------|
|value|Number|The value to round off|

|Type|Description|
|----|-----------|
|Number|The value after rounding|

