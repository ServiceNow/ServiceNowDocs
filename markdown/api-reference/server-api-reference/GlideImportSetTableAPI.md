---
title: GlideImportSetTable - Scoped, Global
description: The GlideImportSetTable API provides methods to create temporary Import Set tables.Instantiates a GlideImportSetTable object.Creates a GlideDateTime column.Creates a string column.Creates the Import Set table.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideImportSetTable - Scoped, Global

The GlideImportSetTable API provides methods to create temporary Import Set tables.

These methods create the Import Set table using a dynamic, standard naming convention. Tables must have at least one defined column. Modification and deletion of existing Import Set tables is not supported.

A scheduled job named Scripted Import Set Deleter runs every seven days by default. Scripted Import Set Deleter deletes all Import Sets, Transform Maps, Transform Entries, and drops the Import Set Tables associated with the tables created by this API.

You can use the GlideImportSetTable methods in global and scoped scripts. Use the `sn_impex` namespace identifier to create a GlideImportSetTable object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[GlideImportLog](../../GlideImportLog/concept/GlideImportLogAPI.md#)

[GlideImportSetRun](../../GlideImportSetRun/concept/GlideImportSetRunAPI.md#)

[GlideImportSetTransformer](../../GlideImportSetTransformer/concept/GlideImportSetTransformerAPI.md#)

[GlideImportSetTransformMap](../../GlideImportSetTransformMap/concept/GlideImportSetTransformMapAPI.md#)

[GlideTransformLog](../../GlideTransformLog/concept/GlideTransformLogAPI.md#)

## GlideImportSetTable - GlideImportSetTable\(String tableLabel\)

Instantiates a GlideImportSetTable object.

|Name|Type|Description|
|----|----|-----------|
|tableLabel|String|Label of the Import Set table created upon calling the create\(\) method.|

```
var importSetTable = new sn_impex.GlideImportSetTable("temp user table");
```

## GlideImportSetTable - addDateTimeColumn\(String columnLabel\)

Creates a GlideDateTime column.

|Name|Type|Description|
|----|----|-----------|
|columnLabel|String|Label of the GlideDateTime column to create in the Import Set table.|

|Type|Description|
|----|-----------|
|void| |

```
var importSetTable = new sn_impex.GlideImportSetTable("temp user table");
importSetTable.addDateTimeColumn('start date');
var tableStructure = importSetTable.create();

```

## GlideImportSetTable - addStringColumn\(String columnLabel, Number length\)

Creates a string column.

<table id="table_arm_vr2_vjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

columnLabel

</td><td>

String

</td><td>

Label of the string column to create in the Import Set table.

</td></tr><tr><td>

length

</td><td>

Number

</td><td>

Optional. Maximum column length. Default: 40 characters

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var importSetTable = new sn_impex.GlideImportSetTable("temp user table");
importSetTable.addStringColumn('first name', 50);
importSetTable.addStringColumn('last name', 50);
var tableStructure = importSetTable.create();

```

## GlideImportSetTable - create\(\)

Creates the Import Set table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_l5g_xs2_vjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON object in the following format:-   tableName: String. Database name of the table.
-   tableLabel: String. User-friendly label of the table \(rewriteable\).
-   columns: Object. Map of table column labels to column names provided by the addDateTimeColumn\(\) and addStringColumn\(\) methods.
    -   column\_label: String. Label of the string column in the Import Set table.
    -   column\_name: String. Name of the string column in the Import Set table.

 ```
{"tableName": "<table_name>", "tableLabel": "<table label>", "columns": StringMap(<column_label>: <column_name>)}
```

</td></tr></tbody>
</table>```
// Create Import Set table
var importSetTable = new sn_impex.GlideImportSetTable("temp user table");
importSetTable.addStringColumn('first name', 40);
importSetTable.addStringColumn('last name', 40);
importSetTable.addDateTimeColumn('start date');
var tableStructure = importSetTable.create();

/*
tableStructure = {
"tableName": "imp_staging_table_1417601730000",
"tableLabel": "temp user table",
"columns": {
		"first name": "u_first_name",
		"last name": "u_last_name",
		"start date": "u_start_date"
	}
}
*/

var importSetTableName = tableStructure["tableName"];
var columns = tableStructure["columns"];

```

