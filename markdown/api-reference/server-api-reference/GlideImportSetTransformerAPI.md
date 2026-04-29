---
title: GlideImportSetTransformer - Scoped, Global
description: The GlideImportSetTransformer API provides methods to create an Import Set Transformer object used to execute an Import Set Transform.Instantiates a GlideImportSetTransformer object.Gets the Import Set Run object associated with a GlideImportSetTransformer object.Returns a Boolean value specifying whether or not there was an error during a transformation.Associates an Import Set record with a specific GlideImportSetTransformer object.Associates an Import Set Run object with a specific GlideImportSetTransformer object.Associates a GlideImportLog object with a specific GlideImportSetTransformer object.Associates a Transform Map with a specific GlideImportSetTransformer object.Enables running synchronous transformations.Executes the Import Set transformation.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideImportSetTransformer - Scoped, Global

The GlideImportSetTransformer API provides methods to create an Import Set Transformer object used to execute an Import Set Transform.

To execute an Import Set transform:

1.  Create an Import Set table using the GlideImportSetTable API.
2.  Create a Transform Map using the GlideImportSetTransformMap API.
3.  Create or use an existing Import Set using the GlideRecord API.
4.  Execute an Import Set Transform using the GlideImportSetTransformer API.

Once you have created the Import Set record it must be consumed by the GlideImportSetTransformerAPI in order to trigger the transform.

```
var transformer = new GlideImportSetTransformer();
transformer.transformAllMaps(importSetGr); 
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[GlideImportLog](../../GlideImportLog/concept/GlideImportLogAPI.md#)

[GlideImportSetRun](../../GlideImportSetRun/concept/GlideImportSetRunAPI.md#)

[GlideImportSetTable](../../GlideImportSetTable/concept/GlideImportSetTableAPI.md#)

[GlideImportSetTransformMap](../../GlideImportSetTransformMap/concept/GlideImportSetTransformMapAPI.md#)

[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)

[GlideTransformLog](../../GlideTransformLog/concept/GlideTransformLogAPI.md#)

## GlideImportSetTransformer - GlideImportSetTransformer\(\)

Instantiates a GlideImportSetTransformer object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var transformer = new GlideImportSetTransformer();
```

## GlideImportSetTransformer - getImportSetRun\(\)

Gets the Import Set Run object associated with a GlideImportSetTransformer object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideImportSetRun|GlideImportSetRun object created by running a transformation or the argument supplied to the setImportSetRun\(\) method.|

```
var importSet = new GlideRecord('sys_import_set');
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var transformer = new GlideImportSetTransformer();
transformer.transformAllMaps(importSet);
var importSetRun = transformer.getImportSetRun();

```

## GlideImportSetTransformer - isError\(\)

Returns a Boolean value specifying whether or not there was an error during a transformation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_jnr_wvq_xjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there is an error.-   true: Error.
-   false: Success.

</td></tr></tbody>
</table>```
var importSet = new GlideRecord('sys_import_set');
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var transformer = new GlideImportSetTransformer();
transformer.transformAllMaps(importSet);
if(transformer.isError()) {
	gs.error('Error executing the transform');
}
```

## GlideImportSetTransformer - setImportSetID\(String id\)

Associates an Import Set record with a specific GlideImportSetTransformer object.

|Name|Type|Description|
|----|----|-----------|
|id|String|The sys\_id of an Import Set record from the Import Sets \[sys\_import\_set\] table.|

|Type|Description|
|----|-----------|
|void| |

```
var importSet = new GlideRecord('sys_import_set');
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var transformer = new GlideImportSetTransformer();
transformer.setImportSetID(importSetID);
transformer.transformAllMaps(importSet);

```

## GlideImportSetTransformer - setImportSetRun\(GlideImportSetRun importSetRun\)

Associates an Import Set Run object with a specific GlideImportSetTransformer object.

|Name|Type|Description|
|----|----|-----------|
|importSetRun|GlideImportSetRun|GlideImportSetRun object representing the ImportSetRun record to track the transformation history.|

|Type|Description|
|----|-----------|
|void| |

```
var importSet = new GlideRecord('sys_import_set');
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var importSetRun = new GlideImportSetRun(importSetID);
var transformer = new GlideImportSetTransformer();
transformer.setImportSetRun(importSetRun);
transformer.transformAllMaps(importSet);

```

## GlideImportSetTransformer - setLogger\(GlideImportLog log\)

Associates a GlideImportLog object with a specific GlideImportSetTransformer object.

If this method is not called prior to calling the transformAllMaps\(\) method, a GlideImportLog object is created internally on the server side.

|Name|Type|Description|
|----|----|-----------|
|log|GlideImportLog|GlideImportLog object to link to the Import Set history. Once set, any call from the GlideImportLog object is associated with the Import Set run history for that specific transform.|

|Type|Description|
|----|-----------|
|void| |

```
var importSet = new GlideRecord('sys_import_set');
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var importLog = new GlideImportLog();
var transformer = new GlideImportSetTransformer();
transformer.setLogger(importLog);
transformer.transformAllMaps(importSet);

```

## GlideImportSetTransformer - setMapID\(String mapID\)

Associates a Transform Map with a specific GlideImportSetTransformer object.

|Name|Type|Description|
|----|----|-----------|
|mapID|String|A sys\_id from the Table Transform Maps \[sys\_transform\_map\] table.|

|Type|Description|
|----|-----------|
|void| |

```
var importSet = new GlideRecord('sys_import_set');
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var transformMapId = '<sys id of transform map>';
var transformer = new GlideImportSetTransformer();
transformer.setMapID(transformMapId);
transformer.transformAllMaps(importSet);

```

## GlideImportSetTransformer - setSyncImport\(Boolean synchronous\)

Enables running synchronous transformations.

<table id="table_inr_wvq_xjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

synchronous

</td><td>

Boolean

</td><td>

Sets transformation mode. Valid values:

 -   true: Run transformation synchronously
-   false: Run transformation asynchronously

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```

var importSet = new GlideRecord('sys_import_set');
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var transformer = new GlideImportSetTransformer();
transformer.setSyncImport(true);
transformer.transformAllMaps(importSet);

```

## GlideImportSetTransformer - transformAllMaps\(GlideRecord importSet, String rowSysId\)

Executes the Import Set transformation.

<table id="table_inr_wvq_xjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

importSet

</td><td>

GlideRecord

</td><td>

GlideRecord of the import set to execute.

</td></tr><tr><td>

rowSysId

</td><td>

String

</td><td>

Optional. Restricts transformation to a single record by passing the sys\_id of a record from the Import Sets \[sys\_import\_set\] table. Default: Transform all rows

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var importSet = new GlideRecord('sys_import_set');
importSet.short_description = 'Import set from scripted rest api';
importSet.table_name = importSetTableName;
var importSetID = importSet.insert();
var transformer = new GlideImportSetTransformer();
transformer.transformAllMaps(importSet);
```

