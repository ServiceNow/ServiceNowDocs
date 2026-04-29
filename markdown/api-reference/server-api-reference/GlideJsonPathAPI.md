---
title: GlideJsonPath - Global
description: The GlideJsonPath API retrieves values from a JSON document using a query path string.Instantiates a GlideJsonPath scriptable object by parsing a JSON document.Retrieves values from a JSON document using a query path string.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideJsonPath- Global

The GlideJsonPath API retrieves values from a JSON document using a query path string.

This API is available by default.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideJsonPath - GlideJsonPath\(String jsonDocument\)

Instantiates a GlideJsonPath scriptable object by parsing a JSON document.

|Name|Type|Description|
|----|----|-----------|
|jsonDocument|String|JSON document to parse.|

This example instantiates a GlideJsonPath object by parsing a JSON document.

```
var v = new GlideJsonPath('{"lib":{"jsonpath":{"creator":{"name":"DevStudio","developers":["dev1","dev2","dev3"]}}}}');
```

## GlideJsonPath - read\(String jsonPath\)

Retrieves values from a JSON document using a query path string.

<table id="table_l4w_xhk_ywb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

jsonPath

</td><td>

String

</td><td>

Path to search for in the JSON document.All valid JSONPath expressions are supported. For more information, see [JSONPath](https://jsonpath.com/).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|JavaScript object\(s\) that match the specified path.|

This example searches a JSON document for all developers listed under the specified path.

```
var v = new GlideJsonPath('{"lib":{"jsonpath":{"creator":{"name":"DevStudio","developers":["dev1","dev2","dev3"]}}}}'); 
var l = v.read("$['lib']['jsonpath']['creator']['developers'][*]");
```

Output:

```
"dev1", "dev2", "dev3"
```

