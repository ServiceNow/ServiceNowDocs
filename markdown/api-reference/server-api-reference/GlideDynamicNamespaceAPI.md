---
title: GlideDynamicNamespace - Global
description: The GlideDynamicNamespace API provides access to dynamic namespace metadata.Gets name of the dynamic namespace.Returns whether an object is an active dynamic namespace.Returns whether an object is a transient dynamic namespace.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-09-10"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDynamicNamespace- Global

The GlideDynamicNamespace API provides access to dynamic namespace metadata.

This API provides methods that enable you to get dynamic schema values defined in the Dynamic Namespace \[dynamic\_namespace\] table. For more details on dynamic namespaces, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

See also:

-   [GlideDynamicAttribute - Global](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#) — getNamespaceName\(\)
-   [GlideDynamicAttributeStore - Global](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)
    -   getDynamicNamespace\(\)
    -   setDynamicNamespace\(\)
-   [GlideElement - Global](../../GlideElement_global/concept/c_GlideElementAPI.md#) — getDynamicNamespace\(\)
-   [GlideElementDynamicAttributeStore - Global](../../GlideElementDynamicAttributeStore/concept/GlideElementDynamicAttStoreAPI.md#) — getDynamicNamespace\(\)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDynamicNamespace - getName\(\)

Gets name of the dynamic namespace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the dynamic namespace's name property.|

The following example shows how to get the name of a dynamic namespace. In this example, the dynamic attribute store field associated with the namespace is `u_attributes`.

```
var gr = new GlideRecord('u_product');
gr.query();
gr.next();

gs.info("Dynamic namespace: " + gr.u_attributes.getDynamicNamespace().getName());
```

Output:

```
Dynamic namespace: u_product/u_attributes
```

## GlideDynamicNamespace - isActive\(\)

Returns whether an object is an active dynamic namespace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_o5y_sln_b2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if a dynamic namespace is active.Valid values:

-   true: The dynamic namespace is active.
-   false: The dynamic namespace is not active.

</td></tr></tbody>
</table>The following example shows how to determine if a dynamic namespace called `u_product/u_attributes` is active. In this example, the dynamic attribute store field associated with the namespace is `u_attributes`.

```
var gr = new GlideRecord('u_product');
gr.query();
gr.next();

gs.info("Dynamic namespace: " + gr.u_attributes.getDynamicNamespace().getName());
gs.info("Active true/false: " + gr.u_attributes.getDynamicNamespace().isActive());
```

Output:

```
Dynamic namespace: u_product/u_attributes
Active true/false: false
```

## GlideDynamicNamespace - isTransient\(\)

Returns whether an object is a transient dynamic namespace.

-   Dynamic namespaces are defined in the Dynamic Namespace \[dynamic\_namespace\] table with a data type and a sys\_id.
-   Transient dynamic namespaces are dynamic namespaces that have been added to a DynamicAttributeStore field without a definition in the Dynamic Namespace \[dynamic\_namespace\] table. Transient dynamic namespaces only contain transient attributes.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_o5y_sln_b2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if a dynamic namespace is transient.Valid values:

-   true: The dynamic namespace is not transient.
-   false: The dynamic namespace is transient.

</td></tr></tbody>
</table>The following example shows how to determine if a dynamic namespace called `u_product/u_attributes` is transient. In this example, the dynamic attribute store field associated with the namespace is `u_attributes`.

```
var gr = new GlideRecord('u_product');
gr.query();
gr.next();

gs.info("Dynamic namespace: " + gr.u_attributes.getDynamicNamespace().getName());
gs.info("Is transient? t/f: " + gr.u_attributes.getDynamicNamespace().isTransient());
```

Output:

```
Dynamic namespace: u_product/u_attributes
Is transient? t/f: false
```

