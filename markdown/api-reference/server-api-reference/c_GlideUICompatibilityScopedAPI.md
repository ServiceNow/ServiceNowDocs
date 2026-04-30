---
title: GlideUICompatibility - Scoped
description: The GlideUICompatibility API provides the ability for scoped applications to define their own minimum browser versions. This is done by creating system properties for the scoped application.Creates a GlideUICompatibility object.Returns the terms "block" or "allow" based upon the browser version.Determines if the browser is not supported \(blocked\).
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideUICompatibility- Scoped

The GlideUICompatibility API provides the ability for scoped applications to define their own minimum browser versions. This is done by creating system properties for the scoped application.

You create the properties using the sys\_properties list and assign a version number. When you do this from the scoped application, the &lt;scope-name&gt; prefix is automatically added to the property name. The scoped application UI compatibility properties are:

-   &lt;scope-name&gt;.ui.ie\_minimum
-   &lt;scope-name&gt;.ui.chrome\_minimum
-   &lt;scope-name&gt;.ui.firefox\_minimum
-   &lt;scope-name&gt;.ui.safari\_major\_version\_minimum

You can then use the GlideUICompatibility class to determine if the current browser is supported.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideUICompatibility - GlideUICompatibility\(String scopeName\)

Creates a GlideUICompatibility object.

|Name|Type|Description|
|----|----|-----------|
|scopeName|String|Application's scope name.|

## GlideUICompatibility - getCompatibility\(\)

Returns the terms "block" or "allow" based upon the browser version.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Either `block`or `allow`.|

```
UICompatibility = new GlideUICompatibility(gs.getCurrentScopeName());
var blockOrAllow = UICompatibility.getCompatibility();
gs.info(blockOrAllow);
```

Output:

```
allow
```

## GlideUICompatibility - isBlocked\(\)

Determines if the browser is not supported \(blocked\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_nyv_kgq_wt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the browser is blocked.Possible values:

-   true: Browser is blocked.
-   false: Browser is valid and not blocked.

</td></tr></tbody>
</table>```
UICompatibility = new GlideUICompatibility(gs.getCurrentScopeName());
var blocked = UICompatibility.isBlocked();
gs.info(blocked);
```

Output:

```
false
```

