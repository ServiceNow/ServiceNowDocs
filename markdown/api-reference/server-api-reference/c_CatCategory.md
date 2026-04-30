---
title: CatCategory - Scoped
description: The CatCategory API provides methods that enable you to create and modify service catalog categories using scripts.Adds the Available For user criteria to the current catalog category.Determines whether a specified user can view a specified category on a mobile device or desktop.Insert the defined category.Deletes the category record on which the CatCategory class was initially instantiated.Returns the sys\_id of the current category.Adds the Not Available For user criteria to a catalog category.Returns a mapping of the category.Defines the attribute values for this category.Defines the table name for this category.Updates the current category with the specified name-value pairs.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatCategory- Scoped

The CatCategory API provides methods that enable you to create and modify service catalog categories using scripts.

This API runs in the `sn_sc` namespace.

**Important:** This API is accessible; however, the recommended implementation is the [Service Catalog REST API](../../../../../integrate/inbound-rest/concept/c_ServiceCatalogAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CatCategory - availableForUserCriteria\(String action, Array criteriaIDs\)

Adds the **Available For** user criteria to the current catalog category.

<table id="table_oz2_pln_vz" class="parameters"><thead><tr><th>

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

```
var item = new sn_sc.CatCategory("31bea3d53790200044e0bfc8bcbe5dec");
item.availableForUserCriteria("add", ["0c441abbc6112275000025157c651c89"]);
```

## CatCategory - canView\(Boolean isMobile, String userSysId\)

Determines whether a specified user can view a specified category on a mobile device or desktop.

<table id="table_j5n_smk_chb" class="parameters"><thead><tr><th>

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

Flag that indicates whether to verify the user for access on a mobile device or desktop.-   true: Validate for mobile.
-   false: Validate for desktop.

</td></tr><tr><td>

userSysId

</td><td>

String

</td><td>

Sys\_id of the user to validate.

</td></tr></tbody>
</table><table id="table_k5n_smk_chb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user can view the associated category.-   true: User can view the category.
-   false: User cannot view the category.

</td></tr></tbody>
</table>```
var scopedCategoryObj = new sn_sc.CatCategory('7b1262b9530033007444ddeeff7b12ae');
scopedCategoryObj.canView(false, '62826bf03710200044e0bfc8bcbe5df1');
```

## CatCategory - create\(Boolean standardUpdate\)

Insert the defined category.

<table id="table_afn_1b2_ns" class="parameters"><thead><tr><th>

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

```
var categoryCreate = new sn_sc.CatCategory();
categoryCreate.setAttributes({"title" : "test a scoped category", "sc_catalog" : "e0d08b13c3330100c8b837659bba8fb4"});
var categorySysId = categoryCreate.create();
var isValidSysId = categorySysId.match(/^[0-9a-fA-F]{32}$/) == null ? false : true;
global.Assert.assertEquals(true, isValidSysId,"CategorySysId: ["+ categorySysId +"] is not valid", true, isValidSysId);
```

## CatCategory - deleteRecord\(Boolean standardUpdate\)

Deletes the category record on which the CatCategory class was initially instantiated.

<table id="table_xzp_4b2_ns" class="parameters"><thead><tr><th>

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

```
var categoryDelete = new sn_sc.CatCategory(categorySysId);
categoryDelete.deleteRecord();
var category = new sn_sc.CatCategory(categorySysId);
values = category.read({"title" : "", "sc_catalog":""}, false);
global.Assert.assertEquals("", values.title,"Category should title");
```

## CatCategory - getID\(\)

Returns the sys\_id of the current category.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current category.|

Example:

```
var cart = new sn_sc.CatCategory("2809952237b1300054b6a3549dbe5dd4");
var categoryID = cart.getID();
gs.info(categoryID);
```

Output:

```
2809952237b1300054b6a3549dbe5dd4
```

## CatCategory - notAvailableForUserCriteria\(String action, Array\[\] criteriaIDs\)

Adds the **Not Available For** user criteria to a catalog category.

<table id="table_yxb_1mn_vz" class="parameters"><thead><tr><th>

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

```
var item = new sn_sc.CatCategory("31bea3d53790200044e0bfc8bcbe5dec");
item. notAvailableForUserCriteria("add", ["0c441abbc6112275000025157c651c89"]);
```

## CatCategory - read\(Object columns, Boolean standardUpdate\)

Returns a mapping of the category.

<table id="table_p2h_5b2_ns" class="parameters"><thead><tr><th>

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
|Object|Mapping of column names to values.|

```
var category = new sn_sc.CatCategory("a96277509f300200b407b89a442e704e");
var values = category.read({"title" : ""}, true);
gs.log(values.title);
```

## CatCategory - setAttributes\(Object attributes\)

Defines the attribute values for this category.

|Name|Type|Description|
|----|----|-----------|
|attributes|Object|Attributes for the new field and value pairs.|

|Type|Description|
|----|-----------|
|void| |

```
var categoryCreate = new sn_sc.CatCategory();
categoryCreate.setAttributes({"title" : "test a scoped category", "sc_catalog" : "e0d08b13c3330100c8b837659bba8fb4"});
var categorySysId = categoryCreate.create();
var isValidSysId = categorySysId.match(/^[0-9a-fA-F]{32}$/) == null ? false : true;
global.Assert.assertEquals(true, isValidSysId,"CategorySysId: ["+ categorySysId +"] is not valid", true, isValidSysId);
```

## CatCategory - setTableName\(String tableName\)

Defines the table name for this category.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table that extends sc\_category.|

|Type|Description|
|----|-----------|
|void| |

```
var categoryRead = new sn_sc.CatCategory(categorySysId);
categoryRead.setTableName("test_category");
var values = categoryRead.read({"title" : "", "sc_catalog":"", "test": ""}, false);
gs.info(categorySysId);
gs.info(values.title);
gs.info(values.test);
global.Assert.assertEquals("testValue", values.test,"Category extends sc_category and stores its extended value");
```

## CatCategory - update\(Object columnValues, Boolean standardUpdate\)

Updates the current category with the specified name-value pairs.

<table id="table_dfz_fb2_ns" class="parameters"><thead><tr><th>

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

Mapping of column names to values.

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

```
var categoryUpdate = new sn_sc.CatCategory(categorySysId);
categoryUpdate.update({"title" : "test changed scoped category"}, true);
values = categoryUpdate.read({"title" : "", "sc_catalog":""}, false);
global.Assert.assertEquals("test changed scoped category", values.title,"Category should title");
```

