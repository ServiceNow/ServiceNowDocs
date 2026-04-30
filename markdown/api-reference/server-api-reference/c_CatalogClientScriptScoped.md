---
title: CatalogClientScript - Scoped
description: The CatalogClientScript API provides methods that enable you to create, modify, or delete catalog client script records.Creates an instance of the CatalogClientScript class.Adds a script to the catalog client script.Specifies if the catalog client script runs on a catalog item.Specifies if the catalog client script runs on a catalog task.Specifies if the catalog client script runs on a requested item.Specifies if the catalog client script runs on a requested item.Inserts the defined catalog client script in the catalog\_script\_client table.Deletes the defined catalog client script.Defines attribute values for the catalog client script.Associates a catalog item with the catalog client script.Runs the catalog client script when a variable value is updated.Associates a variable set with the catalog client script.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatalogClientScript- Scoped

The CatalogClientScript API provides methods that enable you to create, modify, or delete catalog client script records.

To use this class in a scoped application, use the `sn_sc` namespace identifier. The Service Catalog Scoped API plugin \(ID: com.glideapp.servicecatalog.scoped.api\) that is enabled by default is required to access the CatalogClientScript API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CatalogClientScript - CatalogClientScript\(\)

Creates an instance of the CatalogClientScript class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var catalogClientScript = new sn_sc.CatalogClientScript();
```

## CatalogClientScript - addScript\(String script\)

Adds a script to the catalog client script.

|Name|Type|Description|
|----|----|-----------|
|script|String|Script to be added to the catalog client script.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call this method.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.addScript("function onLoad(){Enter the script}");
```

## CatalogClientScript - appliesToCatalogItem\(Boolean flag\)

Specifies if the catalog client script runs on a catalog item.

|Name|Type|Description|
|----|----|-----------|
|flag|Boolean|If true, the catalog client script runs on the catalog item. If false, the catalog client script does not run on the catalog item.|

|Type|Description|
|----|-----------|
|void| |

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.appliesToCatalogItem(true);
```

## CatalogClientScript - appliesToCatalogTask\(Boolean flag\)

Specifies if the catalog client script runs on a catalog task.

|Name|Type|Description|
|----|----|-----------|
|flag|Boolean|If true, the catalog client script runs on the catalog task. If false, the catalog client script does not run on the catalog task.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call this method.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.appliesToCatalogTask(true);
```

## CatalogClientScript - appliesToRequestedItem\(Boolean flag\)

Specifies if the catalog client script runs on a requested item.

|Name|Type|Description|
|----|----|-----------|
|flag|Boolean|If true, the catalog client script runs on the requested item. If false, the catalog client script does not run on the requested item.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.appliesToRequestedItem(true);
```

## CatalogClientScript - appliesToTargetRecord\(Boolean flag\)

Specifies if the catalog client script runs on a requested item.

|Name|Type|Description|
|----|----|-----------|
|flag|Boolean|If true, the catalog client script runs on the target record. If false, the catalog client script does not run on the target record.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.appliesToTargetRecord(true);
```

## CatalogClientScript - create\(Boolean standardUpdate\)

Inserts the defined catalog client script in the catalog\_script\_client table.

<table id="table_kj1_xbs_kx" class="parameters"><thead><tr><th>

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
|String|Sys\_id of the catalog client script.|

This example shows how to call the method.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.setAttributes({"name": "My Catalog Item", "applies_to": "item", "ui_type": "desktop", "type": "onLoad"});
catalogClientScript.appliesToCatalogItem(true);
catalogClientScript.appliesToRequestedItem(true);
catalogClientScript.appliesToCatalogTask(true);
catalogClientScript.appliesToTargetRecord(true);
var catalogClientScriptId = catalogClientScript.create();
gs.info(catalogClientScriptId);
```

Output:

```
039c516237b1300054b6a3549dbe5dfc
```

## CatalogClientScript - deleteRecord\(String sys\_id, Boolean standardUpdate\)

Deletes the defined catalog client script.

<table id="table_jdv_hsz_qy" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

String

</td><td>

Sys\_id of the catalog client script.

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

The following example shows how to delete a catalog client script.

```
var sys_id = "039c516237b1300054b6a3549dbe5dfc"; 
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.deleteRecord("039c516237b1300054b6a3549dbe5dfc");
```

## CatalogClientScript - setAttributes\(Map attributes\)

Defines attribute values for the catalog client script.

|Name|Type|Description|
|----|----|-----------|
|attributes|Map|A JSON object that has mapping for the field and value pairs.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.setAttributes({"name": "My Catalog Item", "applies_to": "catalog_item", "ui_type": "desktop", "type": "onLoad"});
```

## CatalogClientScript - setCatalogItem\(String sys\_id\)

Associates a catalog item with the catalog client script.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the catalog item.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to associate a catalog item with the current catalog client script.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.setCatalogItem("039c516237b1300054b6a3549dbe5dfc");
```

## CatalogClientScript - setOnChangeVariable\(String sys\_id\)

Runs the catalog client script when a variable value is updated.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the variable.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.setOnChangeVariable("039c516237b1300054b6a3549dbe5dfc");
```

## CatalogClientScript - setVariableSet\(String sys\_id\)

Associates a variable set with the catalog client script.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the variable set.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to call the method.

```
var catalogClientScript = new sn_sc.CatalogClientScript();
catalogClientScript.setVariableSet("039c516237b1300054b6a3549dbe5dfc");
```

