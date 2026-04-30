---
title: GlideImportLog - Scoped, Global
description: The GlideImportLog API provides methods to write log entries directly to the Import Log \[import\_log\] table.Instantiates a GlideImportLog object.Logs a message of type Error to the Import Log \[import\_log\] table.Returns a sys\_id of the Import Run record associated with this Import Log.Logs a message of type Info to the Import Log \[import\_log\] table.Associates the GlideImportLog object with a specific Import Set Run record.Logs a message of type Warn to the Import Log \[import\_log\] table.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideImportLog - Scoped, Global

The GlideImportLog API provides methods to write log entries directly to the Import Log \[import\_log\] table.

A GlideImportLog object is consumable by the GlideImportSetTransformer API. This object is not required for the GlideImportSetTransformer API, it enables you to associate import logs with a specific Import Set transformation.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[GlideImportSetRun](../../GlideImportSetRun/concept/GlideImportSetRunAPI.md#)

[GlideImportSetTable](../../GlideImportSetTable/concept/GlideImportSetTableAPI.md#)

[GlideImportSetTransformer](../../GlideImportSetTransformer/concept/GlideImportSetTransformerAPI.md#)

[GlideImportSetTransformMap](../../GlideImportSetTransformMap/concept/GlideImportSetTransformMapAPI.md#)

[GlideTransformLog](../../GlideTransformLog/concept/GlideTransformLogAPI.md#)

## GlideImportLog - GlideImportLog\(GlideImportSetRun importSetRun, String source\)

Instantiates a GlideImportLog object.

|Name|Type|Description|
|----|----|-----------|
|importSetRun|GlideImportSetRun|Optional. Import Set Run record on which all logs are to be associated with.|
|source|String|Optional. Source field value attached to the Import Log record that defines where in the Import Set process this message was logged from. For example, Loading could represent loading step, Cleanup could represent during the cleanup after the transform, and so on.|

Example without optional source parameter.

```
var importSetRun = new GlideImportSetRun();
var importLog = new GlideImportLog(importSetRun);

```

Example using optional source parameter.

```
var importSetRun = new GlideImportSetRun();
var importLog = new GlideImportLog(importSetRun, 'Scripted ImportSetTransformer');

```

## GlideImportLog - error\(String message, String source\)

Logs a message of type Error to the Import Log \[import\_log\] table.

### GlideImportLog

|Name|Type|Description|
|----|----|-----------|
|message|String|Log message. Maximum length 4000 characters.|
|source|String|Optional. Source field value attached to the Import Log record that defines where in the Import Set process this message was logged from. For example, Loading could represent loading step, Cleanup could represent during the cleanup after the transform, and so on.|

|Type|Description|
|----|-----------|
|None| |

```
var importLog = new GlideImportLog();
importLog.error('Error executing transform');

```

## GlideImportLog - getImportRunHistory\(\)

Returns a sys\_id of the Import Run record associated with this Import Log.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of an Import Set Run record from the Transform History \[sys\_import\_set\_run\] table.|

```
var importSet = new GlideRecord('sys_import_set');
importSet.name = 'Scripted Import Set';
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var importLog = new GlideImportLog();
var transformer = new GlideImportSetTransformer();
transformer.setLogger(importLog);
transformer.transformAllMaps(importSet);
var importRunSysId = importLog.getImportRunHistory();

```

## GlideImportLog - info\(String message, String source\)

Logs a message of type Info to the Import Log \[import\_log\] table.

### GlideImportLog

|Name|Type|Description|
|----|----|-----------|
|message|String|Log message. Maximum length 4000 characters.|
|source|String|Optional. Source field value attached to the Import Log record that defines where in the Import Set process this message was logged from. For example, Loading could represent loading step, Cleanup could represent during the cleanup after the transform, and so on.|

|Type|Description|
|----|-----------|
|None| |

```
var importLog = new GlideImportLog();
importLog.info('Successfully executed transform');

```

## GlideImportLog - setImportRunHistory\(String importRunHistory\)

Associates the GlideImportLog object with a specific Import Set Run record.

|Name|Type|Description|
|----|----|-----------|
|importRunHistory|String|The sys\_id of a record from the Transform History \[sys\_import\_set\_run\] table.|

|Type|Description|
|----|-----------|
|void| |

```
var importRunSysId = '4aa3a8d55ba10010953330ad5981c79f';
var importLog = new GlideImportLog();
importLog.setImportRunHistory(importRunSysId);

```

## GlideImportLog - warn\(String message, String source\)

Logs a message of type Warn to the Import Log \[import\_log\] table.

### GlideImportLog

|Name|Type|Description|
|----|----|-----------|
|message|String|Log message. Maximum length 4000 characters.|
|source|String|Optional. Source field value attached to the Import Log record that defines where in the Import Set process this message was logged from. For example, Loading could represent loading step, Cleanup could represent during the cleanup after the transform, and so on.|

|Type|Description|
|----|-----------|
|None| |

```
var importLog = new GlideImportLog();
importLog.warn('Transform taking longer than expected.');

```

