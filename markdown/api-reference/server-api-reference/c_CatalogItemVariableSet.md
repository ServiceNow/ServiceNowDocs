---
title: CatalogItemVariableSet - Scoped
description: The CatalogItemVariableSet API provides methods that enable you to create and modify service catalog item variable sets using scripts.Inserts the defined catalog item variable set.Deletes a variable set.Returns a mapping of catalog item variable set attribute values.Sets attributes for a variable set.Updates a variable set.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatalogItemVariableSet- Scoped

The CatalogItemVariableSet API provides methods that enable you to create and modify service catalog item variable sets using scripts.

This API runs in the `sn_sc` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CatalogItemVariableSet - create\(Boolean standardUpdate\)

Inserts the defined catalog item variable set.

<table id="table_dk2_55d_ns" class="parameters"><thead><tr><th>

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

Flag indicating whether to enable the running of engines and workflow.Valid values:

-   true: Enable the running of engines and workflow.
-   false: Do not enable the running of engines and workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the inserted variable record.|

```
// Given an existing catalog item
var catItemSysId = "e0d08b13c3330100c8b837659bba8fb4";
addVariableSets(catItemSysId);

function addVariableSets(catItemSysId) {
  // List of all variable sets to attach
  var myVarSets = [];

  // Create variable set
  var myVarSetAttrs = {"name": "Requester details", "order": "100"};
  var myVarSet = new sn_sc.CatalogItemVariableSet();
  myVarSet.setAttributes(myVarSetAttrs);
  var myVarSetId = myVarSet.create(true);
  myVarSets.push(myVarSetId);
}
```

## CatalogItemVariableSet - deleteRecord\(Boolean standardUpdate\)

Deletes a variable set.

<table id="table_rzk_z5d_ns" class="parameters"><thead><tr><th>

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

This example removes My Variable Set from all catalog items that use it, and then deletes My Variable Set.

```
// Get the sys_id of the variable set you want to delete
var vSet = new GlideRecord('item_option_new_set');
vSet.addEncodedQuery('title=My Variable Set'); // find My Variable Set
vSet.query();
if (vSet.next()) {

    // first remove the variable set from all catalog items
    var catItemVset = new GlideRecord('io_set_item'); // M2M table linking variable set and catalog item
    catItemVset.addQuery('variable_set', vSet.getUniqueValue); // find all catalog items using My Variable Set
    catItemVset.query();
    while (catItemVset.next()) {
        var vsetM2M = new sn_sc.CatalogItemVariableSetM2M(catItemVset.getUniqueValue()); // io_set_item M2M record sys_id
        vsetM2M.deleteRecord(true); // delete M2M record
    }

    // then delete the variable set record
    var varset = new sn_sc.CatalogItemVariableSet(vSet.getUniqueValue()); 
    varset.deleteRecord(true);
}

```

## CatalogItemVariableSet - read\(Object columns, Boolean standardUpdate\)

Returns a mapping of catalog item variable set attribute values.

<table id="table_k4p_dvd_ns" class="parameters"><thead><tr><th>

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

Specify the set of columns that you would like the values for.

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

## CatalogItemVariableSet - setAttributes\(Object attributes\)

Sets attributes for a variable set.

|Name|Type|Description|
|----|----|-----------|
|attributes|Object|An object mapping column names to values.|

|Type|Description|
|----|-----------|
|void| |

This example creates a variable set and then adds a variable to the new set.

```
createVariableSet('My Variable Set', 'This is my test variable set', '100', 'one_to_one');

function createVariableSet(name, description, order, type) {
    var myVarSet = new sn_sc.CatalogItemVariableSet();
    // fields used in object are from table item_option_new_set
    var myVarSetAttrs = {
        "name": name,
        "description": description,
        "order": order,
        "type": type
    }; 
    myVarSet.setAttributes(myVarSetAttrs);
    var myVarSetId = myVarSet.create(true); // returns the sys_id of the created variable set
    gs.info('Variable set created in table item_option_new_set with sys_id ' + myVarSetId);

    // add a variable to the newly created variable set
    var myVar = new sn_sc.CatalogItemVariable();
    var myVarAttrs = {
        "type": "6", // type 6 is single line text
        "variable_set": myVarSetId.toString(), 
        "question_text": "Example question",
        "name": "example_question",
        "order": 200
    };
    myVar.setAttributes(myVarAttrs);
    myVar.create(true);
}
```

Output:

```
Variable set created in table item_option_new_set with sys_id e21df65a1bff7c10593876a61a4bcbc4

```

## CatalogItemVariableSet - update\(Object columnValues, Boolean standardUpdate\)

Updates a variable set.

<table id="table_z35_5vd_ns" class="parameters"><thead><tr><th>

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

This example updates the description and order for the Standard Employee Questions variable set.

```
// Get the sys_id of the variable set you want to update
var vSet = new GlideRecord('item_option_new_set');
vSet.addEncodedQuery('title=Standard Employee Questions'); // find the Standard Employee Questions variable set
vSet.query();
if (vSet.next()) {
    var varset = new sn_sc.CatalogItemVariableSet(vSet.getUniqueValue()); 
    var attr = {
        'description': 'This should be used for all end user requests such as phones, tablets, etc. \n My description line',
        'order': '500' 
    };
    varset.update(attr, true);
}
```

