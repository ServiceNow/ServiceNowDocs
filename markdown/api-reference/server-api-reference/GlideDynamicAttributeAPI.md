---
title: GlideDynamicAttribute - Global
description: The GlideDynamicAttribute API provides access to dynamic attribute metadata.Gets the value of the group name property of a dynamic attribute object.Gets the value of the name property of a dynamic attribute object.Gets the name of a dynamic attribute within its namespace.Gets the name of a dynamic attribute namespace.Gets the value of the path property of a dynamic attribute object.Gets the value of the type property of a dynamic attribute object.Returns whether an object is a transient dynamic attribute.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDynamicAttribute- Global

The GlideDynamicAttribute API provides access to dynamic attribute metadata.

This API provides methods that enable you to get dynamic schema values defined in the Dynamic Attribute \[dynamic\_attribute\] table. Dynamic attributes have a defined data type and a sys\_id. For more details on dynamic attributes, see [Dynamic schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

To use this API to create dynamic attributes you must have the dynamic\_schema\_writer role. To read dynamic data using this API you must have the dynamic\_schema\_reader role.

[GlideAggregate - Global](../../GlideAggregate/concept/c_GlideAggregateAPI.md#) methods usable with dynamic schema:

-   addAggregate\(\)
-   addHaving\(\)
-   getDynamicAttributeValue\(\)
-   getDynamicAttributeDisplayValue\(\)
-   getValue\(\)
-   groupBy\(\)
-   orderBy\(\)
-   orderByAggregate\(\)

[GlideRecord - Global](../../GlideRecord/concept/c_GlideRecordAPI.md#) methods usable with dynamic schema:

-   addQuery\(\)
-   getDisplayValue\(\)
-   getDynamicAttribute\(\)
-   getDynamicAttributeDisplayValue\(\)
-   getDynamicAttributeValue\(\)
-   getValue\(\)
-   orderBy\(\)
-   orderByDesc\(\)
-   setDisplayValue\(\)
-   setDynamicAttributeDisplayValue\(\)
-   setDynamicAttributeValue\(\)
-   setDynamicAttributeValues\(\)
-   setValue\(\)

See also:

-   [GlideDynamicAttributeStore - Global](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)
-   [GlideDynamicNamespace - Global](../../GlideDynamicNamespace/concept/GlideDynamicNamespaceAPI.md#)
-   [GlideElement - Global](../../GlideElement_global/concept/c_GlideElementAPI.md#)
-   [GlideElementDynamicAttributeStore - Global](../../GlideElementDynamicAttributeStore/concept/GlideElementDynamicAttStoreAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDynamicAttribute - getGroupName\(\)

Gets the value of the group name property of a dynamic attribute object.

As of the Zurich release, dynamic groups have been removed from dynamic schema. For dynamic attributes defined with an associated dynamic attribute group before the Zurich release, this method continues to work for backwards compatibility. Customers are urged to migrate to the current Dynamic Attribute definitions to take advantage of future improvements in features and functionality.

For migration details, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

**Note:** This method returns null for migrated attributes and newly created attributes.

You can use dynamic attributes in dynamic categories to simplify administration and improve the dynamic schema user experience. For more information, see [Working with Dynamic Schema](https://www.servicenow.com/docs/access?context=working-with-dynamic-schema&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the dynamic attribute's group name property.|

In the following example, the value of the dynamic attribute object group name is displayed as `a`.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue('a->b', 5);    // transient (adding here)
das.setDynamicAttributeValue('a->c', 10);   // defined in dynamic_attribute table

var attributes = das.getDynamicAttributes();
gs.info(attributes);

for (var i = 0; i < attributes.length; i++) {
    var attr = attributes[i];
	
    gs.info("");
    gs.info("[" + i + "].getPath()      = " + attr.getPath());
    gs.info("[" + i + "].getName()      = " + attr.getName());
    gs.info("[" + i + "].getGroupName() = " + attr.getGroupName());
    gs.info("[" + i + "].isTransient()  = " + attr.isTransient());
    gs.info("[" + i + "].getType()      = " + attr.getType());
}
```

Output:

```
*** Script: a->c,a->b
*** Script: 
*** Script: [0].getPath()      = a->c
*** Script: [0].getName()      = c
*** Script: [0].getGroupName() = a
*** Script: [0].isTransient()  = false
*** Script: [0].getType()      = integer
*** Script: 
*** Script: [1].getPath()      = a->b
*** Script: [1].getName()      = b
*** Script: [1].getGroupName() = a
*** Script: [1].isTransient()  = true
*** Script: [1].getType()      = string
```

## GlideDynamicAttribute - getName\(\)

Gets the value of the name property of a dynamic attribute object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the dynamic attribute's name property.|

The following example shows how to return the value of the dynamic attribute object name.

```
var used_car = new GlideDynamicAttributeStore('u_product/u_car_inventory');
used_car.setDynamicAttributeValue('mfg_year', 2014);       // transient (adding here)
used_car.setDynamicAttributeValue('u_total_miles', 53246); // defined in dynamic_attribute table

var attributes = used_car.getDynamicAttributes();
gs.info(attributes);

for (var i = 0; i < attributes.length; i++) {
    var attr = attributes[i];
    gs.info("");
    gs.info("[" + i + "].getPath()           = " + attr.getPath());
    gs.info("[" + i + "].getName()           = " + attr.getName());
    gs.info("[" + i + "].getNamespaceName()  = " + attr.getNamespaceName());
    gs.info("[" + i + "].getNamespacedName() = " + attr.getNamespacedName());
    gs.info("[" + i + "].isTransient()       = " + attr.isTransient());
    gs.info("[" + i + "].getType()           = " + attr.getType());
}
```

Output:

```
*** Script: mfg_year,u_total_miles
*** Script: 
*** Script: [0].getPath()           = mfg_year
*** Script: [0].getName()           = mfg_year
*** Script: [0].getNamespaceName()  = u_product/u_car_inventory
*** Script: [0].getNamespacedName() = u_product/u_car_inventory/mfg_year
*** Script: [0].isTransient()       = true
*** Script: [0].getType()           = string
*** Script: 
*** Script: [1].getPath()           = u_total_miles
*** Script: [1].getName()           = u_total_miles
*** Script: [1].getNamespaceName()  = u_product/u_car_inventory
*** Script: [1].getNamespacedName() = u_product/u_car_inventory/u_total_miles
*** Script: [1].isTransient()       = false
*** Script: [1].getType()           = integer
```

## GlideDynamicAttribute - getNamespacedName\(\)

Gets the name of a dynamic attribute within its namespace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_o5y_sln_b2c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Name of the dynamic attribute within its namespace.Format: `namespace_name/attribute_name`

</td></tr></tbody>
</table>The following example shows how to return the dynamic attribute name within a namespace called `u_product/u_car_inventory`.

```
var used_car = new GlideDynamicAttributeStore('u_product/u_car_inventory');
used_car.setDynamicAttributeValue('mfg_year', 2014);       // transient (adding here)
used_car.setDynamicAttributeValue('u_total_miles', 53246); // defined in dynamic_attribute table

var attributes = used_car.getDynamicAttributes();
gs.info(attributes);

for (var i = 0; i < attributes.length; i++) {
    var attr = attributes[i];
    gs.info("");
    gs.info("[" + i + "].getPath()           = " + attr.getPath());
    gs.info("[" + i + "].getName()           = " + attr.getName());
    gs.info("[" + i + "].getNamespaceName()  = " + attr.getNamespaceName());
    gs.info("[" + i + "].getNamespacedName() = " + attr.getNamespacedName());
    gs.info("[" + i + "].isTransient()       = " + attr.isTransient());
    gs.info("[" + i + "].getType()           = " + attr.getType());
}
```

Output:

```
*** Script: mfg_year,u_total_miles
*** Script: 
*** Script: [0].getPath()           = mfg_year
*** Script: [0].getName()           = mfg_year
*** Script: [0].getNamespaceName()  = u_product/u_car_inventory
*** Script: [0].getNamespacedName() = u_product/u_car_inventory/mfg_year
*** Script: [0].isTransient()       = true
*** Script: [0].getType()           = string
*** Script: 
*** Script: [1].getPath()           = u_total_miles
*** Script: [1].getName()           = u_total_miles
*** Script: [1].getNamespaceName()  = u_product/u_car_inventory
*** Script: [1].getNamespacedName() = u_product/u_car_inventory/u_total_miles
*** Script: [1].isTransient()       = false
*** Script: [1].getType()           = integer
```

## GlideDynamicAttribute - getNamespaceName\(\)

Gets the name of a dynamic attribute namespace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the dynamic attribute namespace.|

The following example shows how to return the dynamic attribute namespace, `u_product/u_car_inventory`.

```
var used_car = new GlideDynamicAttributeStore('u_product/u_car_inventory');
used_car.setDynamicAttributeValue('mfg_year', 2014);       // transient (adding here)
used_car.setDynamicAttributeValue('u_total_miles', 53246); // defined in dynamic_attribute table

var attributes = used_car.getDynamicAttributes();
gs.info(attributes);

for (var i = 0; i < attributes.length; i++) {
    var attr = attributes[i];
    gs.info("");
    gs.info("[" + i + "].getPath()           = " + attr.getPath());
    gs.info("[" + i + "].getName()           = " + attr.getName());
    gs.info("[" + i + "].getNamespaceName()  = " + attr.getNamespaceName());
    gs.info("[" + i + "].getNamespacedName() = " + attr.getNamespacedName());
    gs.info("[" + i + "].isTransient()       = " + attr.isTransient());
    gs.info("[" + i + "].getType()           = " + attr.getType());
}
```

Output:

```
*** Script: mfg_year,u_total_miles
*** Script: 
*** Script: [0].getPath()           = mfg_year
*** Script: [0].getName()           = mfg_year
*** Script: [0].getNamespaceName()  = u_product/u_car_inventory
*** Script: [0].getNamespacedName() = u_product/u_car_inventory/mfg_year
*** Script: [0].isTransient()       = true
*** Script: [0].getType()           = string
*** Script: 
*** Script: [1].getPath()           = u_total_miles
*** Script: [1].getName()           = u_total_miles
*** Script: [1].getNamespaceName()  = u_product/u_car_inventory
*** Script: [1].getNamespacedName() = u_product/u_car_inventory/u_total_miles
*** Script: [1].isTransient()       = false
*** Script: [1].getType()           = integer
```

## GlideDynamicAttribute - getPath\(\)

Gets the value of the path property of a dynamic attribute object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the dynamic attribute's path.|

The following example shows how to return the value of the dynamic attribute object path.

```
var used_car = new GlideDynamicAttributeStore('u_product/u_car_inventory');
used_car.setDynamicAttributeValue('mfg_year', 2014);       // transient (adding here)
used_car.setDynamicAttributeValue('u_total_miles', 53246); // defined in dynamic_attribute table

var attributes = used_car.getDynamicAttributes();
gs.info(attributes);

for (var i = 0; i < attributes.length; i++) {
    var attr = attributes[i];
    gs.info("");
    gs.info("[" + i + "].getPath()           = " + attr.getPath());
    gs.info("[" + i + "].getName()           = " + attr.getName());
    gs.info("[" + i + "].getNamespaceName()  = " + attr.getNamespaceName());
    gs.info("[" + i + "].getNamespacedName() = " + attr.getNamespacedName());
    gs.info("[" + i + "].isTransient()       = " + attr.isTransient());
    gs.info("[" + i + "].getType()           = " + attr.getType());
}
```

Output:

```
*** Script: mfg_year,u_total_miles
*** Script: 
*** Script: [0].getPath()           = mfg_year
*** Script: [0].getName()           = mfg_year
*** Script: [0].getNamespaceName()  = u_product/u_car_inventory
*** Script: [0].getNamespacedName() = u_product/u_car_inventory/mfg_year
*** Script: [0].isTransient()       = true
*** Script: [0].getType()           = string
*** Script: 
*** Script: [1].getPath()           = u_total_miles
*** Script: [1].getName()           = u_total_miles
*** Script: [1].getNamespaceName()  = u_product/u_car_inventory
*** Script: [1].getNamespacedName() = u_product/u_car_inventory/u_total_miles
*** Script: [1].isTransient()       = false
*** Script: [1].getType()           = integer
```

## GlideDynamicAttribute - getType\(\)

Gets the value of the type property of a dynamic attribute object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the dynamic attribute's data type.|

In the following example, the value of the dynamic attribute object type is displayed as `string` for the transient attribute and `integer` for the non-transient attribute.

```
var used_car = new GlideDynamicAttributeStore('u_product/u_car_inventory');
used_car.setDynamicAttributeValue('mfg_year', 2014);       // transient (adding here)
used_car.setDynamicAttributeValue('u_total_miles', 53246); // defined in dynamic_attribute table

var attributes = used_car.getDynamicAttributes();
gs.info(attributes);

for (var i = 0; i < attributes.length; i++) {
    var attr = attributes[i];
    gs.info("");
    gs.info("[" + i + "].getPath()           = " + attr.getPath());
    gs.info("[" + i + "].getName()           = " + attr.getName());
    gs.info("[" + i + "].getNamespaceName()  = " + attr.getNamespaceName());
    gs.info("[" + i + "].getNamespacedName() = " + attr.getNamespacedName());
    gs.info("[" + i + "].isTransient()       = " + attr.isTransient());
    gs.info("[" + i + "].getType()           = " + attr.getType());
}
```

Output:

```
*** Script: mfg_year,u_total_miles
*** Script: 
*** Script: [0].getPath()           = mfg_year
*** Script: [0].getName()           = mfg_year
*** Script: [0].getNamespaceName()  = u_product/u_car_inventory
*** Script: [0].getNamespacedName() = u_product/u_car_inventory/mfg_year
*** Script: [0].isTransient()       = true
*** Script: [0].getType()           = string
*** Script: 
*** Script: [1].getPath()           = u_total_miles
*** Script: [1].getName()           = u_total_miles
*** Script: [1].getNamespaceName()  = u_product/u_car_inventory
*** Script: [1].getNamespacedName() = u_product/u_car_inventory/u_total_miles
*** Script: [1].isTransient()       = false
*** Script: [1].getType()           = integer
```

## GlideDynamicAttribute - isTransient\(\)

Returns whether an object is a transient dynamic attribute.

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

Flag that indicates if a dynamic attribute is transient.Valid values:

-   true: The dynamic attribute is transient. Dynamic attributes are defined in the Dynamic Attribute \[dynamic\_attribute\] table with a data type and a sys\_id. See [GlideDynamicAttribute](GlideDynamicAttributeAPI.md#).
-   false: The dynamic attribute is not transient. Transient dynamic attributes are dynamic attributes that have been added to a DynamicAttributeStore field without a definition in the Dynamic Attribute \[dynamic\_attribute\] table. Transient dynamic attributes are handled as strings and have no sys\_id.

</td></tr></tbody>
</table>In the following example, the isTransient\(\) method returns `false` for the non-transient object.

```
var used_car = new GlideDynamicAttributeStore('u_product/u_car_inventory');
used_car.setDynamicAttributeValue('mfg_year', 2014);       // transient (adding here)
used_car.setDynamicAttributeValue('u_total_miles', 53246); // defined in dynamic_attribute table

var attributes = used_car.getDynamicAttributes();
gs.info(attributes);

for (var i = 0; i < attributes.length; i++) {
    var attr = attributes[i];
    gs.info("");
    gs.info("[" + i + "].getPath()           = " + attr.getPath());
    gs.info("[" + i + "].getName()           = " + attr.getName());
    gs.info("[" + i + "].getNamespaceName()  = " + attr.getNamespaceName());
    gs.info("[" + i + "].getNamespacedName() = " + attr.getNamespacedName());
    gs.info("[" + i + "].isTransient()       = " + attr.isTransient());
    gs.info("[" + i + "].getType()           = " + attr.getType());
}
```

Output:

```
*** Script: mfg_year,u_total_miles
*** Script: 
*** Script: [0].getPath()           = mfg_year
*** Script: [0].getName()           = mfg_year
*** Script: [0].getNamespaceName()  = u_product/u_car_inventory
*** Script: [0].getNamespacedName() = u_product/u_car_inventory/mfg_year
*** Script: [0].isTransient()       = true
*** Script: [0].getType()           = string
*** Script: 
*** Script: [1].getPath()           = u_total_miles
*** Script: [1].getName()           = u_total_miles
*** Script: [1].getNamespaceName()  = u_product/u_car_inventory
*** Script: [1].getNamespacedName() = u_product/u_car_inventory/u_total_miles
*** Script: [1].isTransient()       = false
*** Script: [1].getType()           = integer
```

