---
title: GlideTransformLog - Scoped, Global
description: The GlideTransformLog API provides methods to create a GlideTransformLog object to log messages to localhost logs.Instantiates an GlideTransformLog object.Logs a message of type Error to localhost logs.Logs a message of type Info to localhost logs.Logs a message of type Warn to localhost logs.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideTransformLog - Scoped, Global

The GlideTransformLog API provides methods to create a GlideTransformLog object to log messages to localhost logs.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[GlideImportLog](../../GlideImportLog/concept/GlideImportLogAPI.md#)

[GlideImportSetRun](../../GlideImportSetRun/concept/GlideImportSetRunAPI.md#)

[GlideImportSetTable](../../GlideImportSetTable/concept/GlideImportSetTableAPI.md#)

[GlideImportSetTransformer](../../GlideImportSetTransformer/concept/GlideImportSetTransformerAPI.md#)

[GlideImportSetTransformMap](../../GlideImportSetTransformMap/concept/GlideImportSetTransformMapAPI.md#)

## GlideTransformLog - GlideTransformLog\(\)

Instantiates an GlideTransformLog object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var importLog = new GlideTransformLog();
```

## GlideTransformLog - error\(String message\)

Logs a message of type Error to localhost logs.

|Name|Type|Description|
|----|----|-----------|
|message|String|Transform log message.|

|Type|Description|
|----|-----------|
|None| |

```
var importLog = new GlideTransformLog();
importLog.error('Error executing transform');

```

## GlideTransformLog - info\(String message\)

Logs a message of type Info to localhost logs.

|Name|Type|Description|
|----|----|-----------|
|message|String|Transform log message.|

|Type|Description|
|----|-----------|
|None| |

```
var importLog = new GlideTransformLog();
importLog.info('Successfully executed the transform.');

```

## GlideTransformLog - warn\(String message\)

Logs a message of type Warn to localhost logs.

|Name|Type|Description|
|----|----|-----------|
|message|String|Transform log message.|

|Type|Description|
|----|-----------|
|None| |

```
var importLog = new GlideTransformLog();
importLog.warn('Transform taking longer than expected');

```

