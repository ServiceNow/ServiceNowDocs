---
title: CatalogSearch - Scoped
description: The CatalogSearch API provides methods that enable you to search catalog items.Creates an instance of the CatalogSearch class.Searches a catalog item based on a search term. The search can be narrowed down to a catalog category level.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CatalogSearch- Scoped

The CatalogSearch API provides methods that enable you to search catalog items.

To use this class in a scoped application, use the `sn_sc` namespace identifier. The Service Catalog Scoped API plugin \(ID: com.glideapp.servicecatalog.scoped.api\) that is enabled by default is required to access the CatalogSearch API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CatalogSearch - CatalogSearch\(\)

Creates an instance of the CatalogSearch class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var catSearchGR = new sn_sc.CatalogSearch().search('', '', 'Apple', false, true);
catSearchGR.query();
while(catSearchGR.next()) {
  gs.info(catSearchGR.getValue('name'));
}
```

## CatalogSearch - search \(String catalogID, String categoryID, String term, Boolean mobile, Boolean noDepthSearch\)

Searches a catalog item based on a search term. The search can be narrowed down to a catalog category level.

<table id="table_t55_3by_5z" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalogID

</td><td>

String

</td><td>

Identifier of the catalog to search.

</td></tr><tr><td>

categoryID

</td><td>

String

</td><td>

Identifier of the catalog category to search.

</td></tr><tr><td>

term

</td><td>

String

</td><td>

Search term.

</td></tr><tr><td>

mobile

</td><td>

Boolean

</td><td>

Flag that indicates whether catalog items exposed for mobile are searched.Valid values:

-   true: Search for mobile catalog items.
-   false: Do not search for mobile catalog items.

</td></tr><tr><td>

noDepthSearch

</td><td>

Boolean

</td><td>

Flag that indicates whether to search subcategories.Valid values:

-   true: Do not search subcategories.
-   false: Search subcategories.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideRecord|Returns the GlideRecord on sc\_cat\_item matching the search result.|

This example shows how to search all catalogs and all categories for term: ServiceNow.

```
var now_GR = new sn_sc.CatalogSearch().search('', '', 'ServiceNow', false, false);
now_GR.query();
while(now_GR.next()) {
  gs.log(now_GR.name);
}
```

Output:

```
ServiceNow T-shirt
```

