---
title: GlidePluginManager - Scoped
description: The scoped GlidePluginManager API provides a method for determining if a plugin has been activated.Determines if the specified plugin has been activated.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlidePluginManager- Scoped

The scoped GlidePluginManager API provides a method for determining if a plugin has been activated.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlidePluginManager - isActive\(String pluginID\)

Determines if the specified plugin has been activated.

|Name|Type|Description|
|----|----|-----------|
|pluginID|String|Unique plugin identifier.|

<table id="table_wrc_dwv_ht" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if the plugin is active.

 Valid values:

-   true: Plugin is active.
-   false: Plugin is inactive.

</td></tr></tbody>
</table>```
var now_GR = new GlideRecord('sys_plugins');
var queryString = "active=0^ORactive=1";
now_GR.addEncodedQuery(queryString);
now_GR.query();
var pMgr = new GlidePluginManager();
 
while (now_GR.next()) {
   var name = now_GR.getValue('name');
   var pID = now_GR.getValue('source');
   var isActive = pMgr.isActive(pID);
   if (isActive) 
       gs.info('The plugin ' + name + ' is active');
}
```

Output:

```
The plugin Country Lookup Data is active
The plugin Database Replication is active
The plugin REST API Provider is active
The plugin Ten Cool Things is active
```

