---
title: CatalogItemVariable - Scoped
description: The CatalogItemVariable API provides methods that enable you to create and modify service catalog item variables using scripts.Inserts the specified catalog item variable.Deletes the defined catalog item variable.Returns a mapping of catalog item variable attribute values.Defines attribute values for this catalog item variable.Updates current catalog item variable with set values.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatalogItemVariable- Scoped

The CatalogItemVariable API provides methods that enable you to create and modify service catalog item variables using scripts.

This API runs in the `sn_sc` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CatalogItemVariable - create\(Boolean standardUpdate\)

Inserts the specified catalog item variable.

<table id="table_s3d_zrd_ns" class="parameters"><thead><tr><th>

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
|String|Return the sys\_id of the inserted variable record.|

## CatalogItemVariable - deleteRecord\(Boolean standardUpdate\)

Deletes the defined catalog item variable.

<table id="table_p1l_4sd_ns" class="parameters"><thead><tr><th>

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

## CatalogItemVariable - read\(Object columns, Boolean standardUpdate\)

Returns a mapping of catalog item variable attribute values.

<table id="table_j5k_5sd_ns" class="parameters"><thead><tr><th>

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

Set of columns for which to return values.

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

## CatalogItemVariable - setAttributes\(Object attributes\)

Defines attribute values for this catalog item variable.

|Name|Type|Description|
|----|----|-----------|
|attributes|Object|An object mapping column names to values.|

|Type|Description|
|----|-----------|
|void| |

## CatalogItemVariable - update\(Object columnValues, Boolean standardUpdate\)

Updates current catalog item variable with set values.

<table id="table_jxv_4td_ns" class="parameters"><thead><tr><th>

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

