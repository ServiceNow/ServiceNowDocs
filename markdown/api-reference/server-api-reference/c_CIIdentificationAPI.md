---
title: CIIdentification - Global
description: The CIIdentification script include provides methods for discovery of configuration item \(CI\) identification.Creates an instance of the CIIdentification class.Logs a message to the CI Identification log if debug logging is turned on.Identifies the CI. This is the entry point for the entire CI Identification process.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CIIdentification- Global

The CIIdentification script include provides methods for discovery of configuration item \(CI\) identification.

Use this script include with any server-side discovery script for CI identification.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CIIdentification - CIIdentification\(String ciData, String logger\)

Creates an instance of the CIIdentification class.

|Name|Type|Description|
|----|----|-----------|
|ciData|String|The CI data to identify|
|logger|String|The discovery logger|

## CIIdentification - debug\(String msg\)

Logs a message to the CI Identification log if debug logging is turned on.

|Name|Type|Description|
|----|----|-----------|
|msg|String|The message to log|

|Type|Description|
|----|-----------|
|void| |

## CIIdentification - process\(\)

Identifies the CI. This is the entry point for the entire CI Identification process.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|IDResult|The result returned by the identifier|

