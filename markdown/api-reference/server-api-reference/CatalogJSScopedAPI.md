---
title: CatalogJS - Scoped
description: The CatalogJS API provides methods to check and retrieve catalog-specific properties.Creates an instance of the catalog class for the specified glide record object.Creates an instance of the Catalog class with the specified sys\_id.Determines whether a user can view the current category on a mobile device or desktop.Returns the available active catalog.Returns the catalog background color.Returns the number of catalogs active in the catalog table.Returns the categories for the current catalog.Specifies the sys\_ids of the categories in the current catalog.Returns the description of the current catalog.Returns the catalog desktop image file name.Returns the current catalog's GlideRecord.Returns the current catalog's header icon.Returns the sys\_id of the current catalog.Returns the title of the current catalog.Specifies if the current catalog has categories.Specifies if the current catalog has catalog items.Specifies if the wish list is enabled for the current catalog.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatalogJS- Scoped

The CatalogJS API provides methods to check and retrieve catalog-specific properties.

To use this class in a scoped application, use the `sn_sc` namespace identifier. The Service Catalog Scoped API plugin \(com.glideapp.servicecatalog.scoped.api\) that is enabled by default is required to access the CatalogJS API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CatalogJS - Catalog\(GlideRecord now\_GR\)

Creates an instance of the catalog class for the specified glide record object.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|Object|Glide Record pointing to the sc\_catalog table.|

This example shows how to create a new instance of the catalog class.

```
var now_GR = new GlideRecord('sc_catalog');
 now_GR.addQuery('sys_id','e0d08b13c3330100c8b837659bba8fb4');
 now_GR.query();
 var catalog = new sn_sc.Catalog(now_GR);
```

## CatalogJS - Catalog\(String sys\_id\)

Creates an instance of the Catalog class with the specified sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|Sys\_id of the catalog.|

This example shows how to create an instance of the Catalog class wit the specified syst\_id.

```
new sn_sc.Catalog(catalog_sys_id);
var catalog = new sn_sc.Catalog("31bea3d53790200044e0bfc8bcbe5dec");
```

## CatalogJS - canView\(Boolean mobile, String userId\)

Determines whether a user can view the current category on a mobile device or desktop.

<table id="table_mnl_2lz_sbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mobile

</td><td>

Boolean

</td><td>

Flag that indicates whether to check if the user can view the current catalog on a mobile view or desktop view.

 Valid values:

-   true: Mobile view
-   false: Desktop view

</td></tr><tr><td>

userId

</td><td>

String

</td><td>

Optional. Sys\_id of the user to check if they can view the catalog.Default: Current user

</td></tr></tbody>
</table><table id="table_nnl_2lz_sbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the catalog is viewable by the user.

 Valid values:

-   true: Catalog is viewable by the user.
-   false: Catalog is not viewable by the user.

</td></tr></tbody>
</table>Example:

```
var catalog = new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
gs.info(catalog.canView(true));
```

Output:

```
true
```

## CatalogJS - getAvailableCatalog\(\)

Returns the available active catalog.

If only one active catalog exists, then the method returns that catalog. Otherwise, it returns the earliest catalog created from the list of the catalogs that the user can view. If no catalog is available, the method returns null.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object pointing to the earliest catalog that the user can view, or null if no catalog is available.|

This example returns the catalog that is available to the current user.

```
var catalog = sn_sc.Catalog.getAvailableCatalog()
```

## CatalogJS - getBackgroundColor\(\)

Returns the catalog background color.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Background color of the catalog.|

This example returns the background color for the associated catalog.

```
var catalog = new sn_sc.Catalog("0f910a2ac3112200b12d9f2974d3ae3c");
gs.info("Catalog background: " + catalog.getBackgroundColor());
```

Output:

```
Catalog background: white
```

## CatalogJS - getCatalogCount\(\)

Returns the number of catalogs active in the catalog table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Integer|Number of catalogs available in the catalog table.|

Example:

```
console.log(sn_sc.Catalog.getCatalogCount());
```

Output:

```
3
```

## CatalogJS - getCategories\(\)

Returns the categories for the current catalog.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ArrayList|Returns the categories for the current catalog.|

This example returns the categories available in the current catalog object.

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
console.log(catalog.getCategories());
```

Output:

```
0 : {header_image: "", sys_id: "e15706fc0a0a0aa7007fc21e1ab70c2f", description: "Your IT gateway. Report issues and submit requests.", title: "Can We Help You?"} 
1 : {header_image: "", sys_id: "95fc11615f1211001c9b2572f2b477c6", description: "Services offered by different departments in the organization", title: "Departmental Services"} 
2 : {header_image: "", sys_id: "900682363731300054b6a3549dbe5d5f", description: "Desktop computers for your work area.", title: "Desktops"} 
3 : {header_image: "", sys_id: "d2f716fcc611227a015a142fa0b262c1", description: "Order new furniture, and fixtures, or request for cubicle modifications can also be ordered here.", title: "Furniture and Decor"} 
4 : {header_image: "", sys_id: "d258b953c611227a0146101fb1be7c31", description: "Order from a variety of hardware to meet your business needs, including phones, tablets and laptops.", title: "Hardware"} 
```

## CatalogJS - getCategoryIds\(\)

Specifies the sys\_ids of the categories in the current catalog.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ArrayList|Returns the sys\_ids of the categories in the current catalog.|

This example returns the sys\_ids of the categories available in the current catalog.

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
console.log(catalog.getCategoryIds());
```

Output:

```
0:"e15706fc0a0a0aa7007fc21e1ab70c2f"
1 : "95fc11615f1211001c9b2572f2b477c6"
2 : "900682363731300054b6a3549dbe5d5f"
3 : "d2f716fcc611227a015a142fa0b262c1"
```

## CatalogJS - getDescription\(\)

Returns the description of the current catalog.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Catalog description.|

This example returns the name of the current catalog.

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
console.log(catalog.getDescription());
```

Output:

```
Service Catalog - IT Now
```

## CatalogJS - getDesktopImageSRC\(\)

Returns the catalog desktop image file name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Catalog desktop image file name.|

This example returns the current catalog desktop image file name.

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
console.log(catalog.getDesktopImageSRC());
```

Output:

```
adbcc271475211002ee987e8dee49001.iix
```

## CatalogJS - getGr\(\)

Returns the current catalog's GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord of the current catalog.|

This example returns the GlideRecord for the specified catalog.

```
var catalog = new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
data.history = catalog.getGr();
```

## CatalogJS - getHeaderIconSRC\(\)

Returns the current catalog's header icon.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Catalog header icon.|

This example shows how to obtain the name of the catalog header icon.

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
gs.info(catalog.getHeaderIconSRC());
```

Output:

```
service_catalog_header.png
```

## CatalogJS - getID\(\)

Returns the sys\_id of the current catalog.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the current catalog.|

This example returns the sys\_id of the current catalog.

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
console.log(catalog.getId());
```

Output:

```
e0d08b13c3330100c8b837659bba8fb4
```

## CatalogJS - getTitle\(\)

Returns the title of the current catalog.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Title of the current catalog.|

This example returns the title of the current catalog.

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
gs.info(catalog.getTitle());
```

Output:

```
Service Catalog
```

## CatalogJS - hasCategories\(\)

Specifies if the current catalog has categories.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_lwh_lsz_sbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current catalog has categories.

 Valid values:

-   true: Catalog has categories.
-   false: Catalog does not have categories.

</td></tr></tbody>
</table>This examples shows how to determine if the current catalog contains categories.

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
gs.info(catalog.hasCategories());
```

Output:

```
false
```

## CatalogJS - hasItems\(\)

Specifies if the current catalog has catalog items.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_bbg_5wz_sbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current catalog has catalog items.

 Valid values:

-   true: Catalog has catalog items.
-   false: Catalog does not have catalog items.

</td></tr></tbody>
</table>Example:

```
var catalog=new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
gs.info(catalog.hasItems());
```

Output:

```
true
```

## CatalogJS - isWishlistEnabled\(\)

Specifies if the wish list is enabled for the current catalog.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_fmb_xk2_sbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current catalog supports wish lists.

 Valid values:

-   true: Catalog supports wish lists.
-   false: Catalog does not support wish lists.

</td></tr></tbody>
</table>This example shows how to check if a wish lists are enabled for the current catalog.

```
var catalog = new sn_sc.Catalog("e0d08b13c3330100c8b837659bba8fb4");
gs.info(catalog.isWishlistEnabled());

```

Output:

```
true
```

