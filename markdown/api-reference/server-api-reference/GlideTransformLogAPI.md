---
title: GlideTransformLog - Scoped, Global
description: The GlideTransformLog API provides methods to create a GlideTransformLog object to log messages to localhost logs.Instantiates an GlideTransformLog object.Logs a message of type Error to localhost logs.Logs a message of type Info to localhost logs.Logs a message of type Warn to localhost logs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/server-api-reference/GlideTransformLogAPI.html
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideTransformLog - Scoped, Global

The GlideTransformLog API provides methods to create a GlideTransformLog object to log messages to localhost logs.

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/api-server.md)

**Related topics**  


[GlideImportLog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GlideImportLogAPI.md)

[GlideImportSetRun](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GlideImportSetRunAPI.md)

[GlideImportSetTable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GlideImportSetTableAPI.md)

[GlideImportSetTransformer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GlideImportSetTransformerAPI.md)

[GlideImportSetTransformMap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/GlideImportSetTransformMapAPI.md)

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

