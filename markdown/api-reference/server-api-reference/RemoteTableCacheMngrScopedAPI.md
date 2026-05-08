---
title: RemoteTableCacheManager - Scoped
description: The RemoteTableCacheManager API provides a method to flush the cache for a specified remote table.Flushes the cache for a specified remote table.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RemoteTableCacheManager- Scoped

The RemoteTableCacheManager API provides a method to flush the cache for a specified remote table.

Remote tables often cache query results for performance reasons, but when the data at the source changes the cached results become outdated. Scoped applications can invoke this API to flush the remote table cache so that subsequent queries fetch the latest data from the source system. Use this API to automate cache flushing based on custom logic, workflows, or triggers in scoped applications.

The RemoteTableCacheManager API requires the Remote Tables plugin \(com.glide.script.vtable\) and is provided within the `sn_vtable` namespace. For more information, see Remote tables.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RemoteTableCacheManager - flushCache\(String tableName\)

Flushes the cache for a specified remote table.

Flushing the cache ensures that subsequent queries against the remote table fetch fresh data from the source system.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the remote table. Must be a valid remote table within the current scope.|

|Type|Description|
|----|-----------|
|None| |

A message containing details about the result is written to the system log.

Success message:

-   \[RemoteTableCacheManager\] - Flushed cache for Remote Table: &lt;tableName&gt;.

Error messages:

-   \[RemoteTableCacheManager\] - tableName cannot be null.
-   \[RemoteTableCacheManager\] - No remote table found with name: &lt;tableName&gt;.
-   \[RemoteTableCacheManager\] - Table scope is null.
-   \[RemoteTableCacheManager\] - Current scope is null.
-   \[RemoteTableCacheManager\] - Current scope: &lt;currentScope&gt; is not same as table scope: &lt;tableScope&gt;.

This example flushes the cache for the remote table x\_app\_my\_remote\_table.

```
sn_vtable.RemoteTableCacheManager.flushCache("x_app_my_remote_table");
```

Output:

```
[RemoteTableCacheManager] - Flushed cache for Remote Table: x_app_my_remote_table
```

