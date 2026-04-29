---
title: DynamicSchemaAPI - Global
description: The DynamicSchemaAPI provides methods to clear the various caches used by the dynamic schema implementation.Clears the entire dynamic category cache \(DynamicCategoryCache\).Clears the entire dynamic choice set cache \(DynamicChoiceSets\).Clears the DynamicAttributeGroups and DynamicAttributes caches.Clears the specified dynamic attribute group from the DynamicAttributeGroup cache.Clears a specified dynamic schema category from the DynamicCategoryCache.Clears a specified dynamic schema choice set from the DynamicChoiceSets cache.Returns the DynamicSchemaAPI singleton.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DynamicSchemaAPI- Global

The DynamicSchemaAPI provides methods to clear the various caches used by the dynamic schema implementation.

You must have the dynamic\_schema\_writer role to execute any of the clear\(\) methods.

**Note:** You shouldn't need to call the clear\(\) methods in a production environment. Use these methods when you are troubleshooting your implementation if you think there is a possible caching problem causing stale data.

See also [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DynamicSchemaAPI - clearDynamicCategoryCache\(\)

Clears the entire dynamic category cache \(DynamicCategoryCache\).

DynamicCategoryCache is the internal in-memory cache of all dynamic categories. If you observe issues with stale category data, use this method to clear the cache.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var api = DynamicSchemaAPI.get();
api.clearDynamicCategoryCache();
```

## DynamicSchemaAPI - clearDynamicChoiceSetCache\(\)

Clears the entire dynamic choice set cache \(DynamicChoiceSets\).

DynamicChoiceSets is the internal in-memory cache of all dynamic choice sets. If you observe issues with stale choice sets data, use this method to clear the cache.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var api = DynamicSchemaAPI.get(); 
api.clearDynamicChoiceSetCache();
```

## DynamicSchemaAPI - clearDynamicAttributeGroupCache\(\)

Clears the DynamicAttributeGroups and DynamicAttributes caches.

These are internal in-memory caches that contain the attribute and attribute group data. If you observe issues with stale attribute or group data, use this method to clear the cache.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var api = DynamicSchemaAPI.get(); 
api.clearDynamicAttributeGroupCache();
```

## DynamicSchemaAPI - clearDynamicAttributeGroupCacheItem\(String sysId\)

Clears the specified dynamic attribute group from the DynamicAttributeGroup cache.

If you observe issues with stale data for a specific attribute group, use this method to clear the group's cache.

<table id="table_okl_zlw_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysId

</td><td>

String

</td><td>

Sys\_id of the attribute group to clear from the cache.Table: Dynamic Attribute Group \[dynamic\_attribute\_group\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var api = DynamicSchemaAPI.get(); 
api.clearDynamicAttributeGroupCacheItem(sysId);
```

## DynamicSchemaAPI - clearDynamicCategoryCacheItem\(String sysId\)

Clears a specified dynamic schema category from the DynamicCategoryCache.

DynamicCategoryCache is the internal in-memory cache of all dynamic categories. If you observe issues with stale category data for a specific category, use this method to clear that category's cache.

<table id="table_mjl_nmw_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysId

</td><td>

String

</td><td>

Sys\_id of the category to clear from the cache.Table: Dynamic Category \[dynamic\_category\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var api = DynamicSchemaAPI.get(); 
api.clearDynamicCategoryCacheItem(sysId);
```

## DynamicSchemaAPI - clearDynamicChoiceSetItem\(String sysId\)

Clears a specified dynamic schema choice set from the DynamicChoiceSets cache.

DynamicChoiceSets is the internal in-memory cache for all dynamic choice sets. If you observe an issue with stale data for a specific choice set, use this method to clear that choice set's cache.

<table id="table_axs_cnw_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysId

</td><td>

String

</td><td>

Sys\_id of the choice set to clear from the cache.Table: Dynamic Choice Set \[dynamic\_choice\_set\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var api = DynamicSchemaAPI.get(); 
api.clearDynamicChoiceSetItem(sysId); 
```

## DynamicSchemaAPI - get\(\)

Returns the DynamicSchemaAPI singleton.

You must call this method prior to calling any other DynamicSchemaAPI method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var api = DynamicSchemaAPI.get();
```

