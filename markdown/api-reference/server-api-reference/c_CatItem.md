---
title: CatItem - Scoped
description: The CatItem API provides methods that enable you to create and modify service catalog items using scripts.Adds the Available For user criteria to the current catalog item.Verifies whether the current catalog item is viewable in the selected domain \(domain selected in the domain picker\).Determines if the user has access to view the catalog item on global search.Inserts the defined catalog item.Deletes a catalog item.Returns the first category that the user can view in a catalog.Returns an array of users for whom the associated item cannot be delegated \(requested on behalf of\).Returns the class name for the current catalog item record.Verifies whether the specified delegated user has acquisition rights to the current service catalog item.Determines if the current catalog item is available in service portal.Adds the Not Available For user criteria to a catalog item.Returns a mapping of catalog item attribute values.Sets attributes for a catalog item.Defines the catalogs that this catalog item is associated with.Defines the categories that this catalog item is associated with.Adds an image to a catalog item.Defines the table name for this catalog item.Creates a record using a specified Service Catalog record producer.Updates the values for specified fields of a catalog item.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatItem- Scoped

The CatItem API provides methods that enable you to create and modify service catalog items using scripts.

This API runs in the `sn_sc` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CatItem - availableForUserCriteria\(String action, Array criteriaIDs\)

Adds the **Available For** user criteria to the current catalog item.

<table id="table_mbk_f5f_vz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

String

</td><td>

Action to perform.-   `add`: Adds the user criteria to the **Available For** list.
-   `delete`: Deletes the user criteria from the **Available For** list.

</td></tr><tr><td>

criteriaIDs

</td><td>

Array

</td><td>

Array of the user criteria sys\_ids.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to add the specified **Available For** user criteria.

```
var item = new sn_sc.CatItem("31bea3d53790200044e0bfc8bcbe5dec");
item.availableForUserCriteria("add", ["0c441abbc6112275000025157c651c89"]);
```

## CatItem - canViewInDomain\(\)

Verifies whether the current catalog item is viewable in the selected domain \(domain selected in the domain picker\).

Catalog items in the global domain are available across all domains.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hww_bbd_thb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that validates whether the current catalog item is viewable in the selected domain.Valid values:

 -   true: Catalog item is viewable in the domain
-   false: Catalog item is not viewable in the domain

</td></tr></tbody>
</table>This example shows how to verify whether a catalog item is viewable in the currently selected domain.

```
var catItem = new sn_sc.CatItem("060f3afa3731300054b6a3549dbe5d3e");
gs.info(catItem.canViewInDomain());
```

## CatItem - canViewOnSearch\(boolean isMobile\)

Determines if the user has access to view the catalog item on global search.

<table id="table_pqy_zl2_sbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isMobile

</td><td>

Boolean

</td><td>

Flag that indicates whether to perform the search for the mobile or desktop view.

 Valid values:

-   true: Perform the search for the mobile view.
-   false: Perform the search for the desktop view.

</td></tr></tbody>
</table><table id="table_qqy_zl2_sbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user has access to view the catalog item on global search.

 Valid values:

-   true: User has access to view the catalog item on global search.
-   false: User does not have access to view the catalog item on global search.

</td></tr></tbody>
</table>This code example shows how to check if the user has access to view the catalog item on global search in desktop view.

```
var catItem = new sn_sc.CatItem("04b7e94b4f7b4200086eeed18110c7fd");
var canView = catItem.canViewOnSearch('false');
gs.info("Can view on global search: " + canView);
```

Output:

```
Can view on global search: true
```

## CatItem - create\(Boolean standardUpdate\)

Inserts the defined catalog item.

<table id="table_uh4_31n_ms" class="parameters"><thead><tr><th>

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

-   true: Enable the running of engines and workflow.
-   false: Do not enable the running of engines and workflow. Note that the created and updated system date columns on the table are not updated.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the newly created catalog item.|

This example creates a new catalog item and adds a variable and variable set.

```
createCatalogItem('Catalog Item Name', 'Short Description', 'e0d08b13c3330100c8b837659bba8fb4', '109f0438c6112276003ae8ac13e7009d'); 

function createCatalogItem(name, short_desc, catalogId, categoryId) {
    var catalogItem = new sn_sc.CatItem();
    catalogItem.setAttributes({
        "name": name,
        "short_description": short_desc
    });
    catalogItem.setCatalogs(catalogId); // set catalog
    catalogItem.setCategories(categoryId); // set category

    var catItemSysId = catalogItem.create(); // create new catalog item
    gs.info('Catalog item created in table sc_cat_item with sys_id ' + catItemSysId);

    // add variables and variable set
    addDefaultVariables(catItemSysId);
    addDefaultVariableSet(catItemSysId);
}

// creates a new variable and adds it to the catalog item
function addDefaultVariables(catItemSysId) {
    var myVarAttrs = {
        "type": "6", // type 6 is single line text
        "cat_item": catItemSysId,
        "question_text": "First Name",
        "name": "first_name",
        'order': 50
    };
    var myVar = new sn_sc.CatalogItemVariable();
    myVar.setAttributes(myVarAttrs);
    var varRec = myVar.create(true);
    gs.info('Variable added to catalog item and record created in table item_option_new with sys_id ' + varRec);
}

// adds an existing variable set to the catalog item
function addDefaultVariableSet(catItemSysId) {
    var varset = new sn_sc.CatalogItemVariableSetM2M();
    // fields used in object are from table io_set_item 
    var attr = {
        'variable_set': 'e01cab1a4f334200086eeed18110c71f', // required
        'sc_cat_item': catItemSysId, // required
        'order': 100 // optional
    };
    varset.setAttributes(attr);
    var m2mRec = varset.create(true);
    gs.info('Variable set added to catalog item and M2M record created in table io_set_item with sys_id ' + m2mRec);
}
```

Output:

```
Catalog item created in table sc_cat_item with sys_id be5c771e876370103a730f2d0ebb3556
Variable added to catalog item and record created in table item_option_new with sys_id b65cb71e876370103a730f2d0ebb3535
Variable set added to catalog item and M2M record created in table io_set_item with sys_id 8b5cb71e876370103a730f2d0ebb354b
```

## CatItem - deleteRecord\(Boolean standardUpdate\)

Deletes a catalog item.

<table id="table_g1q_mfn_ms" class="parameters"><thead><tr><th>

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

-   true: Enable the running of engines and workflow.
-   false: Do not enable the running of engines and workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example deletes all inactive catalog items.

```
var catalogItem = new GlideRecord('sc_cat_item');
catalogItem.addQuery('active', 'false'); // get all inactive catalog items
catalogItem.query();
while (catalogItem.next()) {

    // before deleting a catalog item, delete its associated variable set M2M records
    var variableSetM2M = new GlideRecord('io_set_item'); // M2M table linking variable set and catalog item
    variableSetM2M.addQuery('sc_cat_item', catalogItem.getUniqueValue()); // get M2M records for the catalog item
    variableSetM2M.query();
    while (variableSetM2M.next()) {
        var varset = new sn_sc.CatalogItemVariableSetM2M(variableSetM2M.getUniqueValue()); // M2M record sys_id
        varset.deleteRecord(true); // delete M2M record
    }

    // then delete the catalog item
    var item = new sn_sc.CatItem(catalogItem.getUniqueValue()); 
    item.deleteRecord(true);
}
```

## CatItem - getFirstAccessibleCategoryForSearch\(String catalogId\)

Returns the first category that the user can view in a catalog.

|Name|Type|Description|
|----|----|-----------|
|catalogId|String|Sys\_id of the catalog.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the first category that the user can view in a catalog.|

Example:

```
var CatItem=new sn_sc.CatItem("04b7e94b4f7b4200086eeed18110c7fd");	
	console.log(CatItem.getFirstAccessibleCategoryForSearch("e0d08b13c3330100c8b837659bba8fb4"));
```

Output:

```
d258b953c611227a0146101fb1be7c31
```

## CatItem - getInvalidDelegatedUsers\(Array requestForUsers\)

Returns an array of users for whom the associated item cannot be delegated \(requested on behalf of\).

The method verifies each of the users passed in the array.

<table id="table_avj_5n3_nlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

requestForUsers

</td><td>

Object

</td><td>

Array of user sys\_ids to check whether the associated user can acquire the current item and that the item can be requested on behalf of them.Table: User \[sys\_user\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Array|List of user names \(Name column from Users \[sys\_user\] table\) for whom the item can't be requested for by a delegate.|

This example shows how to obtain a list of user names for whom the item can't be requested for by a delegate.

```
function getInvalidDelegatedUsers(itemId, userIds) {
var catItem = new sn_sc.CatItem(itemId);
var invalidUsers = catItem.getInvalidDelegatedUsers(userIds);
return invalidUsers;
}
```

Output:

```
[
  "Joe Smith",
  "Jenny Brown",
  "Fred Bennet",
  "Alice Jones"
]
```

## CatItem - getRecordClass\(\)

Returns the class name for the current catalog item record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Class name for the current catalog item record.|

Example:

```
var CatItem=new sn_sc.CatItem("04b7e94b4f7b4200086eeed18110c7fd");	
	console.log(CatItem.getRecordClass());
```

Output:

```
sc_cat_item
```

## CatItem - isDelegationAllowed\(String delegatedUser\)

Verifies whether the specified delegated user has acquisition rights to the current service catalog item.

<table id="table_spd_p3q_nlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

delegatedUser

</td><td>

String

</td><td>

Optional. Sys\_id of the user to request the service catalog item for \(delegate\). The method verifies whether the user has acquisition rights to the item.Default: Checks whether the calling user has acquisition rights to the item.

</td></tr></tbody>
</table><table id="table_tpd_p3q_nlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user has acquisition rights to the current service catalog item.Valid values:

-   true: User has acquisition rights to the item.
-   false: User does not have acquisition rights to the item.

</td></tr></tbody>
</table>This code example shows how to determine if delegation is allowed for the catalog item.

```
function canRequestFor(itemId, user) {
  var catItem = new sn_sc.CatItem(itemId);
  var result = catItem.isDelegationAllowed(user);
  return result;
}
```

Output: true

## CatItem - isVisibleServicePortal\(\)

Determines if the current catalog item is available in service portal.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_sdm_bn2_sbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the catalog item is available in the Service Portal.

 Valid values:

-   true: Available on Service Portal.
-   false: Not available on Service Portal.

</td></tr></tbody>
</table>Example:

```
var catItem = new sn_sc.CatItem("04b7e94b4f7b4200086eeed18110c7fd");
var catItemAvail = catItem.isVisibleServicePortal();
gs.info("Is item available on Service Portal: " + catItemAvail);
```

Output:

```
Is item available on Service Portal: true
```

## CatItem - notAvailableForUserCriteria\(String action, Array criteriaIDs\)

Adds the **Not Available For** user criteria to a catalog item.

<table id="table_wdk_tkn_vz" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

String

</td><td>

Action to perform.-   `add`: Adds the user criteria to the **Not Available For** list.
-   `delete`: Deletes the user criteria from the **Not Available For** list.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to add the specified **Not Available For** user criteria.

```
var item = new sn_sc.CatItem("31bea3d53790200044e0bfc8bcbe5dec");
item. notAvailableForUserCriteria("add", ["0c441abbc6112275000025157c651c89"]);
```

## CatItem - read\(Object columns, Boolean standardUpdate\)

Returns a mapping of catalog item attribute values.

<table id="table_hsf_kgn_ms" class="parameters"><thead><tr><th>

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

Name-value pairs of columns for which to return values.

</td></tr><tr><td>

standardUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable the running of engines and workflow.Valid values:

-   true: Enable the running of engines and workflow.
-   false: Do not enable the running of engines and workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Mapping of column names to values.|

This example reads the name and price fields of a catalog item.

```
var catItem = new sn_sc.CatItem("a96277509f300200b407b89a442e704e");
var values = catItem.read({"name" : "", "price" : ""}, true);
gs.info("Catalog item name: " + values.name);
gs.info("Catalog item price: " + values.price);
```

Output:

```
Catalog item name: Standard Laptop
Catalog item price: 1100
```

## CatItem - setAttributes\(Object attributes\)

Sets attributes for a catalog item.

|Name|Type|Description|
|----|----|-----------|
|attributes|Object|Name-value pairs of the columns for which to set.|

|Type|Description|
|----|-----------|
|void| |

This example sets attributes for a new catalog item.

```
createCatalogItem('Name of your Catalog Item', 'Short Description of your Catalog Item', 'e0d08b13c3330100c8b837659bba8fb4', '109f0438c6112276003ae8ac13e7009d'); 

function createCatalogItem(name, short_desc, catalogId, categoryId) {
    var catalogItem = new sn_sc.CatItem();
    // catalog item column values
    var attributes ={
        "name": name,
        "short_description": short_desc,
	 "description": "<p>This is a test catalog item.</p>",
	 "workflow":"0287f2c64a36232700820846b1f8bdce" // sys_id of workflow
    };
    catalogItem.setAttributes(attributes); // set catalog item attributes
    catalogItem.setCatalogs(catalogId); // set catalog
    catalogItem.setCategories(categoryId); // set category

    var catItemSysId = catalogItem.create(); // create new catalog item
    gs.info('Catalog item created in table sc_cat_item with sys_id ' + catItemSysId);
}
```

Output:

```
Catalog item created in table sc_cat_item with sys_id 706948a287e370103a730f2d0ebb351e
```

## CatItem - setCatalogs\(String catalogs\)

Defines the catalogs that this catalog item is associated with.

|Name|Type|Description|
|----|----|-----------|
|catalogs|String|Comma-separated list of sys\_ids of the catalogs to associate with the item the item.|

|Type|Description|
|----|-----------|
|void| |

This example associates a catalog item with two catalogs.

```
var short_desc = 'This is a short description of my catalog item.';
var catalogItem = new sn_sc.CatItem();
catalogItem.setAttributes({
    "name": 'My Catalog Item',
    "short_description": short_desc
});
catalogItem.setCatalogs('e0d08b13c3330100c8b837659bba8fb4,742ce428d7211100f2d224837e61036d'); // set Service Catalog and Technical Catalog

var catItemSysId = catalogItem.create(); // create new catalog item
gs.info('Catalog item created in table sc_cat_item with sys_id ' + catItemSysId);
```

Output:

```
Catalog item created in table sc_cat_item with sys_id d0c5dcaa872770103a730f2d0ebb35cb
```

## CatItem - setCategories\(String categories\)

Defines the categories that this catalog item is associated with.

|Name|Type|Description|
|----|----|-----------|
|categories|String|Comma-separated list of sys\_ids of the categories to associate with the item the item.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to associate two categories to an item.

```
var catItem = new sn_sc.CatItem("060f3afa3731300054b6a3549dbe5d3e");
catItem.setCatagories("af443cfa5f130100a9ad2572f2b47747", "d467125fd7500200d74460affd6103a1");
```

## CatItem - setImage\(String dbImageSysId, String type\)

Adds an image to a catalog item.

<table id="table_nwf_kjn_ms" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dbImageSysId

</td><td>

String

</td><td>

Sys\_id of the image from the Images table \[db\_image\].

</td></tr><tr><td>

type

</td><td>

String

</td><td>

Type of image. Valid values:

-   picture
-   icon

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example adds an image to a catalog item.

```
var catItem = new sn_sc.CatItem("1fc0bd968777301093d5ec6d0ebb3548"); // sys_id of catalog item to update
// update fields if needed
var attr = {
    'name': 'New Name of Catalog Item - 123',
    'description': '<p>This is an updated description.</p><p> My description new line 1</p><p>My description new line 2</p>',
    'short_description': 'New Short Description of Catalog Item' 
};
catItem.update(attr, true);
catItem.setImage('1b443cfa5f130100a9ad2572f2b47746', 'picture'); // sys_id of image from table db_image

```

## CatItem - setTableName\(String tableName\)

Defines the table name for this catalog item.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table that extends Catalog Item \[sc\_cat\_item\].|

|Type|Description|
|----|-----------|
|void| |

This example shows how to set the name of an extended table.

```
var catItem = new sn_sc.CatItem();
catItem.setTableName("New_catalog_table");
```

## CatItem - submitProducer\(Object values\)

Creates a record using a specified Service Catalog record producer.

<table id="table_gdj_y4n_crb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

values

</td><td>

Object

</td><td>

Contains the field values and record producer to use when creating the record.```
{
  "variables": {Object},
  "sysparm_id": "String"
}
```

</td></tr><tr><td>

values.variables

</td><td>

Object

</td><td>

The field values to set for the new record.```
{
   "field": "String",
   "field": "String"
}
```

</td></tr><tr><td>

values.sysparm\_id

</td><td>

String

</td><td>

Sys\_id of the record producer to use from the Record Producer \[sc\_cat\_item\_producer\] table.

</td></tr></tbody>
</table><table id="table_hdj_y4n_crb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Contains information about the record that was created.```
{
   "number": "String",
   "parent_id": "String",
   "parent_table": "String",
   "record": "String",
   "redirect_portal_url": "String",
   "redirect_to": "String",
   "redirect_url": "String",
   "sys_id": "String",
   "table": "String"	
}
```

</td></tr><tr><td>

&lt;Object&gt;.number

</td><td>

Value of the **Number** field of the created record.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.parent\_id

</td><td>

Sys\_id of the parent record.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.parent\_table

</td><td>

The parent table of the table that the record was created in.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.record

</td><td>

XML of the created record.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.redirect\_portal\_url

</td><td>

URL to which to redirect the Service Portal.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.redirect\_to

</td><td>

Redirect value.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.redirect\_url

</td><td>

URL of the created record.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.sys\_id

</td><td>

Sys\_id of the created record.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.table

</td><td>

The table the record was created in.Data type: String

</td></tr></tbody>
</table>This example creates an incident using the Create Incident record producer.

```
var catalogItem = new sn_sc.CatItem('3f1dd0320a0a0b99000a53f7604a2ef9');  //sys_id of the Create Incident record producer 
var values = {
   "variables": {"urgency" : "2", "comments" : "Laptop is in a brick state"},
   "sysparm_id": "3f1dd0320a0a0b99000a53f7604a2ef9"
}
var targetRecordDetails = catalogItem.submitProducer(values);
gs.info(JSON.stringify(targetRecordDetails, null, 3));
```

Output:

```
{
   "sys_id": "133b2ee1875f30103a730f2d0ebb35f9",
   "number": "INC0010002",
   "parent_id": null,
   "record": "api/now/table/incident/133b2ee1875f30103a730f2d0ebb35f9",
   "redirect_portal_url": "",
   "parent_table": "task",
   "redirect_url": "incident.do?sys_id=133b2ee1875f30103a730f2d0ebb35f9&sysparm_view=ess",
   "table": "incident",
   "redirect_to": "generated_record"
}
```

## CatItem - update\(Object columnValues, Boolean standardUpdate\)

Updates the values for specified fields of a catalog item.

<table id="table_uv3_npd_ns" class="parameters"><thead><tr><th>

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

Name-value pairs of the fields to update and their associated values.

</td></tr><tr><td>

standardUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable the running of engines and workflow.Valid values:

-   true: Enable the running of engines and workflow.
-   false: Do not enable the running of engines and workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example updates the name, short description, and price of an existing catalog item.

```
var catItem = new sn_sc.CatItem("1fc0bd968777301093d5ec6d0ebb3548"); // sys_id of catalog item to update
printCatalogItem(); // print current catalog item values
// object containing fields to update
var attr = {
    "name": "New Name of Catalog Item",
    "short_description": "New Short Description of Catalog Item", 
    "price": "450"
};
catItem.update(attr, true);
printCatalogItem(); // print new catalog item values

// prints the name, short description, and price of the catalog item
function printCatalogItem(){
    // object containing fields to read
    var readValues = {
        "name" : "", 
        "short_description" : "", 
        "price" : ""
    };
    var values = catItem.read(readValues, true); // read the field values
    gs.info("Catalog item name: " + values.name);
    gs.info("Catalog item short description: " + values.short_description);
    gs.info("Catalog item price: " + values.price);
}
```

Output:

```
Catalog item name: Example Catalog Item
Catalog item short description: Example Short Description
Catalog item price: 300
Catalog item name: New Name of Catalog Item
Catalog item short description: New Short Description of Catalog Item
Catalog item price: 450
```

