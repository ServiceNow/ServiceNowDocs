---
title: CimInstanceToken - Global
description: The CimInstanceToken script include provides methods to represent the unique query identity of a Common Information Model \(CIM\) instance.Parses the instance token.Parses the instance token.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CimInstanceToken- Global

The CimInstanceToken script include provides methods to represent the unique query identity of a Common Information Model \(CIM\) instance.

Use with any server-side discovery script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CimInstanceToken - getHashToken\(String cimomip\)

Parses the instance token.

|Name|Type|Description|
|----|----|-----------|
|cimomip|String| |

|Type|Description|
|----|-----------|
|String|The hash token|

## CimInstanceToken - parse\(XMLObj instance\)

Parses the instance token.

|Name|Type|Description|
|----|----|-----------|
|instance|XMLObj|The CIM instance|

|Type|Description|
|----|-----------|
|String|The parsed instance token, for example, CIM\_ClassName\{Key1='Value1',Key2='Value2'\}|

