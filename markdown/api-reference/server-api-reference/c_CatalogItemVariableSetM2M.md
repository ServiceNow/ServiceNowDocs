---
title: CatalogItemVariableSetM2M - Scoped
description: The CatalogItemVariableSetM2M API provides methods that enable you to create and modify service catalog item variable set many-to-many \(M2Ms\) using scripts.Inserts the defined catalog item variable set M2M.Deletes the defined catalog item variable set M2M.Returns a mapping of catalog item variable set M2M attribute values.Defines attribute values for this catalog item variable set M2M.Updates current catalog item variable set M2M with set values.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatalogItemVariableSetM2M- Scoped

The CatalogItemVariableSetM2M API provides methods that enable you to create and modify service catalog item variable set many-to-many \(M2Ms\) using scripts.

This API runs in the `sn_sc` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CatalogItemVariableSetM2M - create\(Boolean standardUpdate\)

Inserts the defined catalog item variable set M2M.

<table id="table_rrn_wwd_ns" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

standardUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable the running of engines and workflow.Valid values:

-   true: Enable engines and workflow.
-   false: Do not enable engines and workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the inserted variable record.|

This example adds the Standard Employee Questions variable set to the iPhone 6s catalog item and creates a record linking them in the Catalog Variable Sets table \[io\_set\_item\].

```
var cat_item_sys_id = 'bd6fa75a4f334200086eeed18110c79e'; // catalog item - iPhone 6s
var variable_set_sys_id = 'e01cab1a4f334200086eeed18110c71f'; // variable set - Standard Employee Questions
var app_scope = 'global'; // sys_id id in case of scoped app
var varset = new sn_sc.CatalogItemVariableSetM2M();
var attr = {
    'variable_set': variable_set_sys_id, // required
    'sc_cat_item': cat_item_sys_id, // required
    'sys_scope': app_scope, // optional
    'order': 10 // optional
};
varset.setAttributes(attr);
var m2mRec = varset.create(true);
gs.info('Variable set added to catalog item and M2M record created in table io_set_item with sys_id ' + m2mRec);
```

Output:

```
Variable set added to catalog item and M2M record created in table io_set_item with sys_id c5c87af187eb30103a730f2d0ebb3578
```

## CatalogItemVariableSetM2M - deleteRecord\(Boolean standardUpdate\)

Deletes the defined catalog item variable set M2M.

<table id="table_v2c_1xd_ns" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

standardUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable the running of engines and workflow.Valid values:

-   true: Enable engines and workflow.
-   false: Do not enable engines and workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example removes the Standard Employee Questions variable set from the iPhone 6s catalog item and deletes the record linking them in the Catalog Variable Sets table \[io\_set\_item\].

```
var vset = new GlideRecord('io_set_item');
vset.addQuery('sc_cat_item', 'bd6fa75a4f334200086eeed18110c79e'); // catalog item - iPhone 6s
vset.addQuery('variable_set', 'e01cab1a4f334200086eeed18110c71f'); // variable set - Standard Employee Questions
vset.query();
if (vset.next()) {
    var varset = new sn_sc.CatalogItemVariableSetM2M(vset.getUniqueValue()); // pass sys_id of io_set_item record
    varset.deleteRecord(true);  
}
```

## CatalogItemVariableSetM2M - read\(Object columns, Boolean standardUpdate\)

Returns a mapping of catalog item variable set M2M attribute values.

<table id="table_uxc_fxd_ns" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

columns

</td><td>

Object

</td><td>

Set of columns that you would like the values for.

</td></tr><tr><td>

standardUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable the running of engines and workflow.Valid values:

-   true: Enable engines and workflow.
-   false: Do not enable engines and workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|An object mapping column names to values.|

This example reads all variable sets that are used by the iPhone 6s catalog item.

```
var vset = new GlideRecord('io_set_item');
vset.addQuery('sc_cat_item', 'bd6fa75a4f334200086eeed18110c79e'); // catalog item - iPhone 6s
vset.query();
while (vset.next()) {
    var varset = new sn_sc.CatalogItemVariableSetM2M(vset.getUniqueValue()); // pass sys_id of io_set_item record
    //add the fields you want to read from the record
    var attr = {
        'sys_name': '', // optional
        'sys_scope': '', // optional
        'order': '' // optional
    };
    var m2mRec = varset.read(attr, true);
    gs.info(JSON.stringify(m2mRec));
}
```

Output:

```
{"sys_name":"HTML Description.iPhone 6s","sys_scope":"global","order":"10"}
{"sys_name":"Standard Employee Questions.iPhone 6s","sys_scope":"global","order":"20"}

```

## CatalogItemVariableSetM2M - setAttributes\(Object attributes\)

Defines attribute values for this catalog item variable set M2M.

|Name|Type|Description|
|----|----|-----------|
|attributes|Object|An object mapping column names to values.|

|Type|Description|
|----|-----------|
|void| |

This example adds the Standard Employee Questions variable set to the iPhone 6s catalog item and creates a record in the Catalog Variable Sets table \[io\_set\_item\].

```
var cat_item_sys_id = 'bd6fa75a4f334200086eeed18110c79e'; // catalog item - iPhone 6s
var variable_set_sys_id = 'e01cab1a4f334200086eeed18110c71f'; // variable set - Standard Employee Questions
var app_scope = 'global'; // sys_id id in case of scoped app
var varset = new sn_sc.CatalogItemVariableSetM2M();
var attr = {
    'variable_set': variable_set_sys_id,
    'sc_cat_item': cat_item_sys_id,
    'sys_scope': app_scope,
    'order': 10
};
varset.setAttributes(attr);
var m2mRec = varset.create(true);
gs.info('Variable set added to catalog item and M2M record created in table io_set_item with sys_id ' + m2mRec);
```

Output:

```
Variable set added to catalog item and M2M record created in table io_set_item with sys_id c5c87af187eb30103a730f2d0ebb3578
```

## CatalogItemVariableSetM2M - update\(Object columnValues, Boolean standardUpdate\)

Updates current catalog item variable set M2M with set values.

<table id="table_dj1_cyd_ns" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

columnValues

</td><td>

Object

</td><td>

An object mapping column names to values.

</td></tr><tr><td>

standardUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable the running of engines and workflow.Valid values:

-   true: Enable engines and workflow.
-   false: Do not enable engines and workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example updates the order of the Standard Employee Questions variable set for the iPhone 6s catalog item.

```
var vset = new GlideRecord('io_set_item');
vset.addQuery('sc_cat_item', 'bd6fa75a4f334200086eeed18110c79e'); // catalog item - iPhone 6s
vset.addQuery('variable_set', 'e01cab1a4f334200086eeed18110c71f'); // variable set - Standard Employee Questions
vset.query();
if (vset.next()) {
    var varset = new sn_sc.CatalogItemVariableSetM2M(vset.getUniqueValue()); // pass sys_id of io_set_item record
    var attr = {
        'order': '30' // update order to 30
    };
    varset.update(attr, true);
    var readAttr = {
        'sys_name': '',
        'order': '' 
    };
    var m2mRec = varset.read(readAttr, true); // read the record to confirm the update 
    gs.info(JSON.stringify(m2mRec));
}
```

Output:

```
{"sys_name":"Standard Employee Questions.iPhone 6s","order":"30"}
```

