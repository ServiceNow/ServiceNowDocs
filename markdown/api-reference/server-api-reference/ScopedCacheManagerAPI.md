---
title: ScopedCacheManager - Scoped
description: The ScopedCacheManager API provides methods for retrieving, setting, and flushing cache data for scoped applications.Flushes an entire cache or a single entry from a cache.Gets a value from a cache.Gets cache entry details including byte size, object type, and entry value.Flushes all cache entries that have keys beginning with a specified prefix.Puts a value in a scoped cache for caches that are Table or Table Column pair types.Puts an entry into the cache and sets all records with the specified sys\_ids as a flush source for that entry. This method is intended for caches that are Table or Table Column pair types.Puts a value in a single row \(table\) of a cache. Use this method for caches that are Table Row or Table Row and Column pair types.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ScopedCacheManager- Scoped

The ScopedCacheManager API provides methods for retrieving, setting, and flushing cache data for scoped applications.

This API requires the Scoped Cache \(com.glide.scopedcache\) plugin and runs in the `sn_scoped_cache` namespace. The plugin is installed and activated by default.

These methods require one or more scoped caches and scoped cache pairs to be defined. For more information on creating scoped caches, see the [ScopedCacheManager API Developer Guide](../../../../../integrate/guides/scopedcachemgr/concept/scoped-caches.md#).

Using this API with scoped caches provides several advantages, including:

-   Caching strings in scoped applications that live in memory across transactions.
-   Caching scoped application data in memory and flushing this data based on changes in the underlying table.
-   Defining and use cache data outside the transaction life cycle.
-   Caching the output of expensive operations or calculations for quick access in the future.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ScopedCacheManager – flushScopedCache\(String catalog, String key\)

Flushes an entire cache or a single entry from a cache.

|Name|Type|Description|
|----|----|-----------|
|catalog|String|Name of the cache defined in the Scoped Caches \[sys\_scoped\_cache\] table.|
|key|String|Optional. Cache key. Set this parameter to flush a single entry from a cache.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to flush the "abc" key from a cache named myCache. To flush the entire cache, leave out the key parameter.

```
sn_scoped_cache.ScopedCacheManager.flushScopedCache("myCache", "abc");
```

## ScopedCacheManager – get\(String catalog, String key\)

Gets a value from a cache.

|Name|Type|Description|
|----|----|-----------|
|catalog|String|Name of the cache defined in the Scoped Caches \[sys\_scoped\_cache\] table.|
|key|String|Cache key.|

|Type|Description|
|----|-----------|
|String|Cache entry.|

The following example shows how to count the number of incident records having short descriptions with a number of characters greater than the key \(50\). In this case, there are 6 incident records with short descriptions longer than 50 characters. This value is stored in the cache as a reusable string, so you don't have to make a calculation each time you want to retrieve the value.

```
var cache2 = "Cache 2"; // column pair type

// Re-populate the column cache
for (var i = 0; i < 100; i+=10) {
    var inc = new GlideRecord('incident');
    inc.query();
    var counter = 0;
    while (inc.next()) {
        if (inc.getValue('short_description').length > i)
        counter++;
    }
    sn_scoped_cache.ScopedCacheManager.put(cache2, i.toString(), counter.toString());
}

// script to get values from column cache
gs.info(sn_scoped_cache.ScopedCacheManager.get(cache2, "50"));
```

Output:

```
scoped_app: 6
```

## ScopedCacheManager – getCacheEntryDetails\(String catalog, String key\)

Gets cache entry details including byte size, object type, and entry value.

<table id="table_b5d_z35_4tb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalog

</td><td>

String

</td><td>

Name of the cache defined in the Scoped Caches \[sys\_scoped\_cache\] table. The catalog name must be prefixed with the scope name and a caret character. For example, "test\_cache" in the global scope is prefixed as `"global^test_cache"`.

</td></tr><tr><td>

key

</td><td>

String

</td><td>

Cache key.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|String in the format `<ObjectType> (<EntrySize>): <Value.toString()>`.|

The following example shows how to display cache entry details for a scoped cache named `test_cache`.

```
sn_scoped_cache.ScopedCacheManager.put("test_cache", "key1", "val1");
gs.info(sn_scoped_cache.ScopedCacheManager.getCacheEntryDetails("global^test_cache", "key1"));
```

Output:

```
java.lang.String (48):
val1
```

## ScopedCacheManager – prefixFlush\(String catalog, String prefix\)

Flushes all cache entries that have keys beginning with a specified prefix.

|Name|Type|Description|
|----|----|-----------|
|catalog|String|Name of the cache defined in the Scoped Caches \[sys\_scoped\_cache\] table.|
|prefix|String|Prefix by which to search for keys when flushing the cache.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to flush cache values for keys with the prefix `a`.

```
sn_scoped_cache.ScopedCacheManager.put("test_cache", "aKey1", "val1");
sn_scoped_cache.ScopedCacheManager.put("test_cache", "aKey2", "val2");
sn_scoped_cache.ScopedCacheManager.put("test_cache", "bKey1", "val3");

sn_scoped_cache.ScopedCacheManager.prefixFlush("test_cache", "a");

gs.info(sn_scoped_cache.ScopedCacheManager.get("test_cache", "aKey1"));
gs.info(sn_scoped_cache.ScopedCacheManager.get("test_cache", "aKey2"));
gs.info(sn_scoped_cache.ScopedCacheManager.get("test_cache", "bKey1"));
```

Output:

```
*** Script: null
*** Script: null
*** Script: val3
```

## ScopedCacheManager – put\(String catalog, String key, String value\)

Puts a value in a scoped cache for caches that are **Table** or **Table Column** pair types.

|Name|Type|Description|
|----|----|-----------|
|catalog|String|Name of the cache defined in the Scoped Caches \[sys\_scoped\_cache\] table.|
|key|String|Cache key.|
|value|String|Cache entry.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to define and retrieve a key called "abc" to a cache named myCache. The cache is table-paired with the Incident \[incident\] table. The example also shows how the cache is flushed after updating the description field of an incident record.

```
//put value in cache for key "abc"
gs.info("put key 'abc' into cache with value 'value1'");
sn_scoped_cache.ScopedCacheManager.put("myCache", "abc", "value1");

// retrieve value from cache for key "abc"
gs.info("value of 'abc' in cache: ");
gs.info(sn_scoped_cache.ScopedCacheManager.get("myCache", "abc")+"\n");

//update an incident record (add string to the description field)
gs.info("Updating incident record.");
var gr = new GlideRecord("incident");
gr.get("<incident_sys_id>");
gr.description= "test12345";
if (gr.update()) {
    gs.info("Record updated successfully.\n");
};

//retrieve the value from cache for key "abc"
gs.info("Retrieving 'abc' from cache. Value should be null because a table pair was updated.");
gs.info(sn_scoped_cache.ScopedCacheManager.get("myCache", "abc"));
```

Output:

```
scoped_app: put key 'abc' into cache with value 'value1'
scoped_app: value of 'abc' in cache: 
scoped_app: value1

scoped_app: Updating incident record.
scoped_app: Record updated successfully.

scoped_app: Retrieving 'abc' from cache. Value should be null because a table pair was updated.
scoped_app: null
```

## ScopedCacheManager – putMultiRow\(String catalog, String key, String value, Array ids\)

Puts an entry into the cache and sets all records with the specified sys\_ids as a flush source for that entry. This method is intended for caches that are **Table** or **Table Column** pair types.

|Name|Type|Description|
|----|----|-----------|
|catalog|String|The catalog to be flushed. Name of the cache defined in the Scoped Caches \[sys\_scoped\_cache\] table.|
|key|String|Cache key for the new entry.|
|value|String|Value for new entry.|
|ids|Array|List of sys\_ids of the records to be used as flush sources for the entry. These records can be from different tables.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to use an incident and user record as flush points. The test\_cache key INC0000060 is flushed when either of the specified records is updated.

```
// This example requires a table-row pair for the "incident" and "sys_user" tables assigned to a cache named test_cache
var inc1ID = "1c741bd70b2322007518478d83673af3";
var userID = "681ccaf9c0a8016400b98a06818d57c7";

// update to email should invalidate the entry
gs.info("initial put");
putCacheEntry();
gs.info("cache value for INC0060: " + sn_scoped_cache.ScopedCacheManager.get("test_cache", "INC0000060"));
var gr = new GlideRecord("sys_user");
gr.get(userID);
gr.setValue("email", "a" + gr.getValue("email"));
gr.update();
gs.info("updated user email");
gs.info("cache value: " + sn_scoped_cache.ScopedCacheManager.get("test_cache", "INC0000060"));

// update to incident number should invalidate the entry.
gs.info("second put");
putCacheEntry();
gs.info("cache value: " + sn_scoped_cache.ScopedCacheManager.get("test_cache", "INC0000060"));
var gr = new GlideRecord("incident");
gr.get(inc1ID);
gr.setValue("number", gr.getValue("number") + "1");
gr.update();
gs.info("updated incident number");
gs.info("cache value: " + sn_scoped_cache.ScopedCacheManager.get("test_cache", "INC0000060"));

function putCacheEntry() {
    var incGr = new GlideRecord("incident");
    incGr.get(inc1ID);
    var userGr = new GlideRecord("sys_user");
    userGr.get(userID);
    // the cache stores that the incident is assigned to a specific user. So if the incident or user record changes, we should flush.
    sn_scoped_cache.ScopedCacheManager.putMultiRow("test_cache",incGr.getValue("number"), userGr.getValue("email"), [inc1ID, userID]);
}
```

Output:

```
*** Script: initial put
*** Script: cache value for INC0060: employee@example.com
*** Script: Updating Joe Employee's primary email device based on change to user record email address
*** Script: updated user email
*** Script: cache value: null
*** Script: second put
*** Script: cache value: aemployee@example.com
*** Script: updated incident number
*** Script: cache value: null
```

## ScopedCacheManager – putRow\(String catalog, String key, String value, String sysId\)

Puts a value in a single row \(table\) of a cache. Use this method for caches that are **Table Row** or **Table Row and Column** pair types.

|Name|Type|Description|
|----|----|-----------|
|catalog|String|Name of the cache defined in the Scoped Caches \[sys\_scoped\_cache\] table.|
|key|String|Cache key.|
|value|String|Cache entry.|
|sysId|String|Optional. Sys\_id of a row in a table, that is, the record being tracked.|

|Type|Description|
|----|-----------|
|None| |

The following example uses a table row pair cache type named incident\_cache. The cache adds the incident caller ID, and the cache entries associated with the changed record's sys\_id are cleared.

```
// build the cache:
var number = 'INC0009009';
var inc = new GlideRecord('incident');
inc.addQuery('number', number);
inc.query();
inc.next();
var entry = inc.caller_id.getDisplayValue();
sn_scoped_cache.ScopedCacheManager.putRow("incident_cache", inc.getValue('number'), entry, inc.getValue('sys_id'));
gs.info(sn_scoped_cache.ScopedCacheManager.get("incident_cache", number));

// when the incident is altered, the cache entry will be flushed.
inc = new GlideRecord('incident');
inc.addQuery('number', number);
inc.query();
inc.next();
inc.setValue('short_description', inc.getValue('short_description') + "a");
inc.update();
gs.info(sn_scoped_cache.ScopedCacheManager.get("incident_cache", number));
```

Output:

```
scoped_app: John Jones
scoped_app: null
```

