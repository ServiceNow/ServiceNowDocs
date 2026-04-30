---
title: GlideImportSetRun - Scoped, Global
description: The GlideImportSetRun API provides methods to creates an Import Set Run record which the GlideImportSetTransformer API can consume.Instantiates a GlideImportSetRun object.Gets the sys\_id of the Import Set Run associated with the transformation.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideImportSetRun - Scoped, Global

The GlideImportSetRun API provides methods to creates an Import Set Run record which the GlideImportSetTransformer API can consume.

See also:

-   [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)
-   [Import Set API](../../../../../integrate/inbound-rest/concept/c_ImportSetAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[GlideImportLog](../../GlideImportLog/concept/GlideImportLogAPI.md#)

[GlideImportSetTable](../../GlideImportSetTable/concept/GlideImportSetTableAPI.md#)

[GlideImportSetTransformer](../../GlideImportSetTransformer/concept/GlideImportSetTransformerAPI.md#)

[GlideImportSetTransformMap](../../GlideImportSetTransformMap/concept/GlideImportSetTransformMapAPI.md#)

[GlideTransformLog](../../GlideTransformLog/concept/GlideTransformLogAPI.md#)

## GlideImportSetRun - GlideImportSetRun\(String importSetID\)

Instantiates a GlideImportSetRun object.

|Name|Type|Description|
|----|----|-----------|
|importSetID|String|Optional. The sys\_id of the import set record listed in the Import Sets \[sys\_import\_set\] table. If not set, a new \[sys\_import\_set\] record is created and the GlideImportSetRun object represents this record.|

```
var importSetRun = new GlideImportSetRun();
```

## GlideImportSetRun - getImportSetRunSysID\(\)

Gets the sys\_id of the Import Set Run associated with the transformation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The sys\_id of the Transform Histories \[sys\_import\_set\_run\] record associated with the transform.|

```
var importSetRun = new GlideImportSetRun();
var importSetRunSysId = importSetRun.getImportSetRunSysID();

```

