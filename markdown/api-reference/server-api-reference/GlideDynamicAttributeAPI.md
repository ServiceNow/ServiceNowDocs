---
title: GlideDynamicAttribute - Global
description: The GlideDynamicAttribute API provides access to dynamic attribute metadata.Gets the value of the group name property of a dynamic attribute object.Gets the value of the name property of a dynamic attribute object.Gets the value of the path property of a dynamic attribute object.Gets the sys\_id of a dynamic attribute object.Gets the value of the type property of a dynamic attribute object.Returns whether an object is a transient dynamic attribute.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDynamicAttribute- Global

The GlideDynamicAttribute API provides access to dynamic attribute metadata.

This API provides methods that enable you to get dynamic schema values defined in the Dynamic Attribute \[dynamic\_attribute\] table. Dynamic attributes have a defined data type and a sys\_id. For more details on dynamic attributes, see [Dynamic schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). The same methods are also available for transient dynamic attributes in the [GlideTransientDynamicAttribute - Global](../../GlideTransientDynamicAttribute/concept/GlideTransientDynamicAttributeAPI.md#) API.

To use this API to create dynamic attributes you must have the dynamic\_schema\_writer role. To read dynamic data using this API you must have the dynamic\_schema\_reader role.

See also:

-   [GlideDynamicAttributeStore - Global](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)
-   [GlideElementDynamicAttributeStore - Global](../../GlideElementDynamicAttributeStore/concept/GlideElementDynamicAttStoreAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDynamicAttribute - getGroupName\(\)

Gets the value of the group name property of a dynamic attribute object.

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

Value of the dynamic attribute's group name property.See also [Create a dynamic attribute group](https://www.servicenow.com/docs/access?context=create-dynamic-attribute-group&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>In the following example, the value of the dynamic attribute object group name is displayed as `a`.

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
    gs.info("[" + i + "].getSysId()     = " + attr.getSysId());
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
*** Script: [0].getSysId()     = 8bc411a94fc01210b8ddc0e552ce0b3c
*** Script: [0].isTransient()  = false
*** Script: [0].getType()      = integer
*** Script: 
*** Script: [1].getPath()      = a->b
*** Script: [1].getName()      = b
*** Script: [1].getGroupName() = a
*** Script: [1].getSysId()     = undefined
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

In the following example, the value of the dynamic attribute object name is displayed as `c`.

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
    gs.info("[" + i + "].getSysId()     = " + attr.getSysId());
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
*** Script: [0].getSysId()     = 8bc411a94fc01210b8ddc0e552ce0b3c
*** Script: [0].isTransient()  = false
*** Script: [0].getType()      = integer
*** Script: 
*** Script: [1].getPath()      = a->b
*** Script: [1].getName()      = b
*** Script: [1].getGroupName() = a
*** Script: [1].getSysId()     = undefined
*** Script: [1].isTransient()  = true
*** Script: [1].getType()      = string
```

## GlideDynamicAttribute - getPath\(\)

Gets the value of the path property of a dynamic attribute object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the dynamic attribute's path.|

In the following example, the value of the dynamic attribute object path is displayed as `a->c`.

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
    gs.info("[" + i + "].getSysId()     = " + attr.getSysId());
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
*** Script: [0].getSysId()     = 8bc411a94fc01210b8ddc0e552ce0b3c
*** Script: [0].isTransient()  = false
*** Script: [0].getType()      = integer
*** Script: 
*** Script: [1].getPath()      = a->b
*** Script: [1].getName()      = b
*** Script: [1].getGroupName() = a
*** Script: [1].getSysId()     = undefined
*** Script: [1].isTransient()  = true
*** Script: [1].getType()      = string
```

## GlideDynamicAttribute - getSysId\(\)

Gets the sys\_id of a dynamic attribute object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the dynamic attribute's sys\_id.|

In the following example, the value of the dynamic attribute object's sys\_id is displayed as `8bc411a94fc01210b8ddc0e552ce0b3c`.

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
    gs.info("[" + i + "].getSysId()     = " + attr.getSysId());
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
*** Script: [0].getSysId()     = 8bc411a94fc01210b8ddc0e552ce0b3c
*** Script: [0].isTransient()  = false
*** Script: [0].getType()      = integer
*** Script: 
*** Script: [1].getPath()      = a->b
*** Script: [1].getName()      = b
*** Script: [1].getGroupName() = a
*** Script: [1].getSysId()     = undefined
*** Script: [1].isTransient()  = true
*** Script: [1].getType()      = string
```

## GlideDynamicAttribute - getType\(\)

Gets the value of the type property of a dynamic attribute object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value of the dynamic attribute's data type.|

In the following example, the value of the dynamic attribute object type is displayed as `integer`.

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
    gs.info("[" + i + "].getSysId()     = " + attr.getSysId());
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
*** Script: [0].getSysId()     = 8bc411a94fc01210b8ddc0e552ce0b3c
*** Script: [0].isTransient()  = false
*** Script: [0].getType()      = integer
*** Script: 
*** Script: [1].getPath()      = a->b
*** Script: [1].getName()      = b
*** Script: [1].getGroupName() = a
*** Script: [1].getSysId()     = undefined
*** Script: [1].isTransient()  = true
*** Script: [1].getType()      = string
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

-   true: The dynamic attribute is transient. Dynamic attributes are defined in the Dynamic Attribute \[dynamic\_attribute\] table with a data type and a sys\_id.
-   false: The dynamic attribute is not transient. Transient dynamic attributes are dynamic attributes that have been added to a DynamicAttributeStore field without a definition in the Dynamic Attribute \[dynamic\_attribute\] table. Transient dynamic attributes are handled as strings and have no sys\_id.

**Note:** The Dynamic Attribute \[dynamic\_attribute\] table is accessible by navigating to **All** &gt; **Dynamic Schema** &gt; **Dynamic Attribute Groups**, selecting a group, and selecting the **Dynamic Attributes** tab.

</td></tr></tbody>
</table>In the following example, the isTransient\(\) method returns `false` for the non-transient object.

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
    gs.info("[" + i + "].getSysId()     = " + attr.getSysId());
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
*** Script: [0].getSysId()     = 8bc411a94fc01210b8ddc0e552ce0b3c
*** Script: [0].isTransient()  = false
*** Script: [0].getType()      = integer
*** Script: 
*** Script: [1].getPath()      = a->b
*** Script: [1].getName()      = b
*** Script: [1].getGroupName() = a
*** Script: [1].getSysId()     = undefined
*** Script: [1].isTransient()  = true
*** Script: [1].getType()      = string
```

