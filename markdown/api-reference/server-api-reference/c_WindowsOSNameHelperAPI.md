---
title: WindowsOSNameHelper - Global
description: The WindowsOSNameHelper script include provides methods to handle the formatting of Windows OS names.Formats the given Windows OS name.Ensures that the OS choice is valid.Cleans up the specified Windows OS name by stripping out incorrect characters, incorrect capitalization, extra spaces, or trailing spaces.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# WindowsOSNameHelper- Global

The WindowsOSNameHelper script include provides methods to handle the formatting of Windows OS names.

Use in any server-side discovery scripts where you need to format OS names.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## WindowsOSNameHelper - formatWindowsOSName\(String name\)

Formats the given Windows OS name.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name to format|

|Type|Description|
|----|-----------|
|String|The formatted name|

## WindowsOSNameHelper - makeOSChoiceValid\(String value\)

Ensures that the OS choice is valid.

**Note:** Deprecated. Use OSChoice.reconcile\(\)

|Name|Type|Description|
|----|----|-----------|
|value|String|The value to validate|

|Type|Description|
|----|-----------|
|void| |

## WindowsOSNameHelper - osCleanupName\(String name\)

Cleans up the specified Windows OS name by stripping out incorrect characters, incorrect capitalization, extra spaces, or trailing spaces.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name to clean up.|

|Type|Description|
|----|-----------|
|String|The cleaned up name|

