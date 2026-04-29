---
title: GlideImportSetTransformMap - Scoped, Global
description: The GlideImportSetTransformMap API provides methods to create transform maps and transform entries.Instantiates a GlideImportSetTransformMap object.Add a GlideDateTime transform entry to a transform map.Adds a string transform entry to a transform map.Creates a new transform map.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideImportSetTransformMap - Scoped, Global

The GlideImportSetTransformMap API provides methods to create transform maps and transform entries.

You can use the GlideImportSetTransformMap methods in global and scoped scripts. Use the `sn_impex` namespace identifier to create a GlideImportSetTransformMap object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[GlideImportLog](../../GlideImportLog/concept/GlideImportLogAPI.md#)

[GlideImportSetRun](../../GlideImportSetRun/concept/GlideImportSetRunAPI.md#)

[GlideImportSetTable](../../GlideImportSetTable/concept/GlideImportSetTableAPI.md#)

[GlideImportSetTransformer](../../GlideImportSetTransformer/concept/GlideImportSetTransformerAPI.md#)

[GlideTransformLog](../../GlideTransformLog/concept/GlideTransformLogAPI.md#)

## GlideImportSetTransformMap - GlideImportSetTransformMap\(String transformMapName, String importSetTableName, String targetTableName\)

Instantiates a GlideImportSetTransformMap object.

|Name|Type|Description|
|----|----|-----------|
|transformMapName|String|Name of the map.|
|importSetTableName|String|Name of the Import Set table.|
|targetTableName|String|Name of the target table.|

```
var transformMap = new sn_impex.GlideImportSetTransformMap("temp user map name", importSetTableName, targetTableName);
```

## GlideImportSetTransformMap - addDateTimeTransformEntry\(String sourceColumn, String targetColumn, Boolean coalesce, String dateTimeFormat\)

Add a GlideDateTime transform entry to a transform map.

<table id="table_mrr_n1f_vjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

targetColumn

</td><td>

String

</td><td>

Target column from target table to transform to.

</td></tr><tr><td>

coalesce

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to insert the record into the target table

-   true: If true and target table contains a record with the same value in this field, the record is updated, that is, not inserted.
-   false: Default. Record is inserted into the target table.

</td></tr><tr><td>

sourceColumn

</td><td>

String

</td><td>

Source column from Import Set table to transform from.

</td></tr><tr><td>

dateTimeFormat

</td><td>

String

</td><td>

Optional. GlideDateTime format of the transform, for example, yyyy-MM-dd HH:mm:ss. If empty, the default value is the system date time format.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var transformMap = new sn_impex.GlideImportSetTransformMap("temp user map name", importSetTableName, targetTableName,);
transformMap.addDateTimeTransformEntry("u_start date", "first day", true, "yyyy-MM-dd HH:mm:ss");
var transformMapId = transformMap.create();
```

## GlideImportSetTransformMap - addTransformEntry\(String sourceColumn, String targetColumn, Boolean coalesce\)

Adds a string transform entry to a transform map.

<table id="table_mrr_n1f_vjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

targetColumn

</td><td>

String

</td><td>

Source column from Import Set table to transform from.

</td></tr><tr><td>

coalesce

</td><td>

String

</td><td>

Target column from target table to transform to.

</td></tr><tr><td>

sourceColumn

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to insert the record into the target table

-   true: If true and target table contains a record with the same value in this field, the record is updated, that is, not inserted.
-   false: Default. Record is inserted into the target table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var transformMap = new sn_impex.GlideImportSetTransformMap("temp user map name", importSetTableName, targetTableName); 
transformMap.addTransformEntry("first_name", "first_name", true);
transformMap.addTransformEntry("last_name", "last_name", false);
transformMap.addTransformEntry("age", "age", false); 
var transformMapId = transformMap.create();

```

## GlideImportSetTransformMap - create\(\)

Creates a new transform map.

**Note:** To create a transform map you must have defined at least one transform entry using either addDateTimeTransformEntry\(\) or addTransformEntry\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The sys\_id of the created transform map.|

```
var transformMap = new sn_impex.GlideImportSetTransformMap("temp user map name", importSetTableName, targetTableName);
transformMap.addTransformEntry("u_first_name", "first_name");
var transformMapId = transformMap.create();

```

