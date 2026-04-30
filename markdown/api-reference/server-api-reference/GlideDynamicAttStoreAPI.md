---
title: GlideDynamicAttributeStore - Global
description: Use the GlideDynamicAttributeStore API to create objects for working with dynamic attributes independently of a table or field.Clears all attributes and their values from the GlideDynamicAttributeStore object.Returns the JSON map representation of the values stored in the current GlideDynamicAttributeStore object.Returns the set of dynamic attribute definitions present in the store.Returns the value of the specified attribute within the dynamic attribute store element.Returns the dynamic namespace.Returns the compact string representation of the contents of the current GlideDynamicAttributeStore object.Clears the current GlideDynamicAttributeStore object and then stores the passed JSON map in the GlideDynamicAttributeStore object.Sets the value of the dynamic attribute located at a specified path within a dynamic attribute store element.Sets the dynamic attribute referenced by a specified attribute path to a specified value.Sets the internal JSON storage for the field to the String representation of the passed value. If the passed value is another instance of a GlideDynamicAttributeStore object, it copies the values from that object to the current object.Sets a dynamic namespace name.Clears the current GlideDynamicAttributeStore object and then stores the passed JSON map in that GlideDynamicAttributeStore object.Returns the content of the GlideDynamicAttributeStore object as a string.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDynamicAttributeStore- Global

Use the GlideDynamicAttributeStore API to create objects for working with dynamic attributes independently of a table or field.

This API provides methods that enable you to get and set dynamic schema attributes in a GlideDynamicAttributeStore object. For more details on dynamic attributes, see [Dynamic schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

To use this API to create dynamic attributes you must have the dynamic\_schema\_writer role. To read dynamic data using this API you must have the dynamic\_schema\_reader role.

There are methods in this API that have the same functionality as dynamic schema methods in the [GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#) API. Use this API if you want to set the same dynamic attributes on multiple records. Using this API, you can stage a GlideDynamicAttributeStore object with the intended attributes and then copy that object to records using the setDynamicAttributeValue\(\) or setDynamicAttributeValues\(\) method.

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

-   [GlideDynamicAttribute - Global](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#)
-   [GlideDynamicNamespace - Global](../../GlideDynamicNamespace/concept/GlideDynamicNamespaceAPI.md#)
-   [GlideElementDynamicAttributeStore - Global](../../GlideElementDynamicAttributeStore/concept/GlideElementDynamicAttStoreAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDynamicAttributeStore - clear\(\)

Clears all attributes and their values from the GlideDynamicAttributeStore object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("color","blue");
das.setDynamicAttributeValue("make","Toyota");
das.setDynamicAttributeValue("model","CRV");
das.setDynamicAttributeValue("luxury",true);
das.setDynamicAttributeValue("cost",12000.5);
das.setDynamicAttributeValue("avg_mpg",24.5234);
das.setDynamicAttributeValue("total_miles",5324);    
das.setDynamicAttributeValue("date_purchased",new GlideDateTime());
gs.info('das: ' + das.getDisplayValue());
das.clear();
gs.info('das: ' + das.getDisplayValue());
```

Output:

```
*** Script: das: {
  "avg_mpg" : "24.5234",
  "color" : "blue",
  "cost" : "12000.5",
  "date_purchased" : "2024-04-19 08:29:52",
  "luxury" : "true",
  "make" : "Toyota",
  "model" : "CRV",
  "total_miles" : "5324"
}
*** Script: das: null
```

## GlideDynamicAttributeStore - getDisplayValue\(\)

Returns the JSON map representation of the values stored in the current GlideDynamicAttributeStore object.

This method returns:

-   Boolean values as "true" and "false" instead of 1 and 0.
-   Date/time values in the user’s locale instead of UTC.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Human-readable JSON map of the values stored in the GlideDynamicAttributeStore object. The contents of this string depends on your dynamic schema definition.|

The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("color","blue");
das.setDynamicAttributeValue("make","Honda");
das.setDynamicAttributeValue("model","CRV");
das.setDynamicAttributeValue("luxury",false);
das.setDynamicAttributeValue("cost",12000.5);
das.setDynamicAttributeValue("avg_mpg", 24.5234);
das.setDynamicAttributeValue("total_miles", 5324);
das.setDynamicAttributeValue("date_purchased",new GlideDateTime());
gs.info('Value returned by getValue(): ' + das.getValue());
gs.info('Value returned by getDisplayValue(): ' + das.getDisplayValue());
```

Output:

```
*** Script: Value returned by getValue(): {"total_miles":5324,"color":"blue","model":"CRV","cost":12000.5,"luxury":1,"avg_mpg":24.5234,"make":"Toyota","date_purchased":"2024-04-19 15:33:23"}
*** Script: Value returned by getDisplayValue(): {
  "avg_mpg" : "24.5234",
  "color" : "blue",
  "cost" : "12000.5",
  "date_purchased" : "2024-04-19 08:33:23",
  "luxury" : "false",
  "make" : "Honda",
  "model" : "CRV",
  "total_miles" : "5324"
}
```

## GlideDynamicAttributeStore - getDynamicAttributes\(\)

Returns the set of dynamic attribute definitions present in the store.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qsl_m3q_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Array containing all transient and non-transient dynamic attributes present in the store.-   Dynamic attributes are defined in the Dynamic Attribute \[dynamic\_attribute\] table with a data type and a sys\_id. See [GlideDynamicAttribute](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#).
-   Transient dynamic attributes are dynamic attributes that have been added to a DynamicAttributeStore field without a definition in the Dynamic Attribute \[dynamic\_attribute\] table. Transient dynamic attributes are handled as strings and have no sys\_id.

</td></tr></tbody>
</table>The following example shows how to retrieve transient and non-transient dynamic attributes.

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
*** Script: [0].isTransient()       = true
*** Script: [0].getType()           = string
*** Script: 
*** Script: [1].getPath()           = u_total_miles
*** Script: [1].getName()           = u_total_miles
*** Script: [1].getNamespaceName()  = u_product/u_car_inventory
*** Script: [1].isTransient()       = false
*** Script: [1].getType()           = integer
```

## GlideDynamicAttributeStore - getDynamicAttributeValue\(String attrPath\)

Returns the value of the specified attribute within the dynamic attribute store element.

<table id="table_psl_m3q_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"attr_name"`

`attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr></tbody>
</table><table id="table_qsl_m3q_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Value of the dynamic schema attribute referenced by the passed group/attribute path.If the **attributePath** parameter contains invalid information, returns a null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("color","blue");
das.setDynamicAttributeValue("make","Toyota");
das.setDynamicAttributeValue("model","CRV");
das.setDynamicAttributeValue("luxury",true);
das.setDynamicAttributeValue("cost",12000.5);
das.setDynamicAttributeValue("avg_mpg", 24.5234);
das.setDynamicAttributeValue("total_miles", 5324);
das.setDynamicAttributeValue("date_purchased", new GlideDateTime());
gs.info('Value returned by getDynamicAttributeValue(): ' + das.getDynamicAttributeValue("color"));
gs.info('Value returned by getDynamicAttributeValue(): ' + das.getDynamicAttributeValue("luxury"));

```

Output:

```
*** Script: Value returned by getDynamicAttributeValue(): blue
*** Script: Value returned by getDynamicAttributeValue(): 1
```

## GlideDynamicAttributeStore - getDynamicNamespace\(\)

Returns the dynamic namespace.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Namespace object.|

The following example shows how to create a store using a dynamic namespace, and retrieve the name of the namespace.

```
gs.info("car_inventory = new GlideDynamicAttributeStore('u_product/u_car_inventory')");
var car_inventory = new GlideDynamicAttributeStore("u_product/u_car_inventory");
gs.info("car_inventory.getDynamicNamespace() : " + car_inventory.getDynamicNamespace());
var ns1 = car_inventory.getDynamicNamespace();
```

Output:

```
*** Script: new_cars = new GlideDynamicAttributeStore('u_product/u_car_inventory')
*** Script: new_cars.getDynamicNamespace() : u_product/u_car_inventory
```

## GlideDynamicAttributeStore - getValue\(\)

Returns the compact string representation of the contents of the current GlideDynamicAttributeStore object.

This method returns:

-   Boolean values as 1 and 0 instead of "true" and "false".
-   Date/time values in UTC instead of the user’s locale.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Compact string representation of the values stored in the GlideDynamicAttributeStore object. The contents of this string depends on your dynamic schema definition.|

The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("color","blue");
das.setDynamicAttributeValue("make","Honda");
das.setDynamicAttributeValue("model","CRV");
das.setDynamicAttributeValue("luxury",false);
das.setDynamicAttributeValue("cost",12000.5);
das.setDynamicAttributeValue("avg_mpg", 24.5234);
das.setDynamicAttributeValue("total_miles", 5324);
das.setDynamicAttributeValue("date_purchased",new GlideDateTime());
gs.info('Value returned by getValue(): ' + das.getValue());
gs.info('Value returned by getDisplayValue(): ' + das.getDisplayValue());
```

Output:

```
*** Script: Value returned by getValue(): {"total_miles":5324,"color":"blue","model":"CRV","cost":12000.5,"luxury":1,"avg_mpg":24.5234,"make":"Toyota","date_purchased":"2024-04-19 15:33:23"}
*** Script: Value returned by getDisplayValue(): {
  "avg_mpg" : "24.5234",
  "color" : "blue",
  "cost" : "12000.5",
  "date_purchased" : "2024-04-19 08:33:23",
  "luxury" : "false",
  "make" : "Honda",
  "model" : "CRV",
  "total_miles" : "5324"
}
```

## GlideDynamicAttributeStore - setDisplayValue\(Object value\)

Clears the current GlideDynamicAttributeStore object and then stores the passed JSON map in the GlideDynamicAttributeStore object.

This method is functionally the same as [GlideDynamicAttributeStore - setValue\(Object value\)](GlideDynamicAttStoreAPI.md#), except that it assumes that all date values are provided in the user's locale.

<table id="table_zpm_m2j_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

value

</td><td>

Object

</td><td>

Value to set in the current dynamic attribute store object.The passed value must be of one of the following data types:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("color","blue");
das.setDynamicAttributeValue("make","Honda");
das.setDynamicAttributeValue("model","CRV");
das.setDynamicAttributeValue("luxury",false);
das.setDynamicAttributeValue("cost",12000.5);
das.setDynamicAttributeValue("avg_mpg", 24.5234);
das.setDynamicAttributeValue("total_miles", 5324);    
das.setDynamicAttributeValue("date_purchased",new GlideDateTime());
gs.info('das: ' + das.getDisplayValue());
das.setDisplayValue('{"luxury":false}');
gs.info('das: ' + das.getDisplayValue());
```

Output:

```
*** Script: das: {
  "avg_mpg" : "24.5",
  "color" : "blue",
  "cost" : "12000.0",
  "date_purchased" : "2024-04-19 14:16:49",
  "luxury" : "false",
  "make" : "Honda",
  "model" : "CRV",
  "total_miles" : "5324.0"
}
*** Script: das: {
  "luxury" : "false"
}
```

## GlideDynamicAttributeStore - setDynamicAttributeDisplayValue\(String attrPath, Object value\)

Sets the value of the dynamic attribute located at a specified path within a dynamic attribute store element.

This method works the same as the [GlideDynamicAttributeStore - setDynamicAttributeValue\(String attrPath, Object value\)](GlideDynamicAttStoreAPI.md#) method except in its handling of Boolean and date/time values. This method assumes that all date/time values are provided in the user's locale.

<table id="table_zqq_cxp_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"attr_name"`

`attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to set in the specified attribute.**Note:** For dynamic attributes, only the following data types are supported:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table><table id="table_arq_cxp_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Updated GlideDynamicAttributeStore object.If the **attrPath** parameter isn't valid, the method throws an `IllegalArgumentException`.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeDisplayValue("color","blue");
das.setDynamicAttributeDisplayValue("make","Honda");
das.setDynamicAttributeDisplayValue("model","CRV");
das.setDynamicAttributeDisplayValue("luxury","false");
das.setDynamicAttributeDisplayValue("cost",12000.5);
das.setDynamicAttributeDisplayValue("avg_mpg", 24.5234);
das.setDynamicAttributeDisplayValue("total_miles", 5324);    
das.setDynamicAttributeDisplayValue("date_purchased",new GlideDateTime());
gs.info('das: ' + das.getDisplayValue());
das.setDisplayValue('{"luxury":"false"}');
gs.info('das: ' + das.getDisplayValue());
```

Output:

```
*** Script: das: {
  "avg_mpg" : "24.5234",
  "color" : "blue",
  "cost" : "12000.5",
  "date_purchased" : "2024-04-19 10:40:45",
  "luxury" : "false",
  "make" : "Honda",
  "model" : "CRV",
  "total_miles" : "5324"
}
*** Script: das: {
  "luxury" : "false"
}
```

## GlideDynamicAttributeStore - setDynamicAttributeValue\(String attrPath, Object value\)

Sets the dynamic attribute referenced by a specified attribute path to a specified value.

<table id="table_zgx_1np_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"attr_name"`

`attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to set in the specified attribute.**Note:** For dynamic attributes, only the following data types are supported:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table><table id="table_ahx_1np_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Updated GlideDynamicAttributeStore object.If the **attrPath** parameter isn't valid, the method throws an `IllegalArgumentException`.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("color","blue");
das.setDynamicAttributeValue("make","Honda");
das.setDynamicAttributeValue("model","CRV");
das.setDynamicAttributeValue("luxury",false);
das.setDynamicAttributeValue("cost",12000.5);
das.setDynamicAttributeValue("avg_mpg", 24.5234);
das.setDynamicAttributeValue("total_miles", 5324);
das.setDynamicAttributeValue("date_purchased",new GlideDateTime());
gs.info('Value returned by getValue(): ' + das.getValue());
gs.info('Value returned by getDisplayValue(): ' + das.getDisplayValue());
```

Output:

```
*** Script: Value returned by getValue(): {"total_miles":5324,"color":"blue","model":"CRV","cost":12000.5,"luxury":1,"avg_mpg":24.5234,"make":"Toyota","date_purchased":"2024-04-19 15:33:23"}
*** Script: Value returned by getDisplayValue(): {
  "avg_mpg" : "24.5234",
  "color" : "blue",
  "cost" : "12000.5",
  "date_purchased" : "2024-04-19 08:33:23",
  "luxury" : "false",
  "make" : "Honda",
  "model" : "CRV",
  "total_miles" : "5324"
}
```

## GlideDynamicAttributeStore - setDynamicAttributeValues\(Object value\)

Sets the internal JSON storage for the field to the String representation of the passed value. If the passed value is another instance of a GlideDynamicAttributeStore object, it copies the values from that object to the current object.

|Name|Type|Description|
|----|----|-----------|
|value|Object|JSON object to store as the value in the associated GlideRecord. The method ignores any invalid JSON values.|

|Type|Description|
|----|-----------|
|Object|Updated GlideDynamicAttributeStore object.|

The following example shows how to store attribute/value pairs in a GlideDynamicAttributeStore object and then copy those same values from one object to another.

```
var das = new GlideDynamicAttributeStore();
var otherValues = new GlideDynamicAttributeStore();
otherValues.setDynamicAttributeValue("position_x", 5);
otherValues.setDynamicAttributeValue("position_y", 6);

das.setDynamicAttributeValues(otherValues);
gs.info(das);
```

Output:

```
{"position_x":"5.0","position_y":"6.0"}
```

## GlideDynamicAttributeStore - setDynamicNamespace\(String namespaceName\)

Sets a dynamic namespace name.

|Name|Type|Description|
|----|----|-----------|
|namespaceName|String|Dynamic namespace name.|

|Type|Description|
|----|-----------|
|Object|Updated GlideDynamicAttributeStore object.|

The following example shows how to sets the name of a default namespace to `namespace1`.

```
gs.info("store1 = new GlideDynamicAttributeStore()");
var store1 = new GlideDynamicAttributeStore();
gs.info("store1.getDynamicNamespace() : " + store1.getDynamicNamespace());
gs.info("store1.setDynamicNamespace('namespace1')");
store1.setDynamicNamespace('namespace1');
gs.info("store1.getDynamicNamespace() : " + store1.getDynamicNamespace());
```

Output:

```
*** Script: store1 = new GlideDynamicAttributeStore()
*** Script: store1.getDynamicNamespace() : default
*** Script: store1.setDynamicNamespace('namespace1')
*** Script: store1.getDynamicNamespace() : namespace1
```

## GlideDynamicAttributeStore - setValue\(Object value\)

Clears the current GlideDynamicAttributeStore object and then stores the passed JSON map in that GlideDynamicAttributeStore object.

This method is functionally the same as [GlideDynamicAttributeStore - setDisplayValue\(Object value\)](GlideDynamicAttStoreAPI.md#) except that it assumes that all date values are in UTC.

<table id="table_uh2_2hj_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

value

</td><td>

Object

</td><td>

JSON map object to store in the GlideDynamicAttributeStore object. For example: `'{"cost":"12500"}'`

This method ignores any invalid JSON values.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("color","blue");
das.setDynamicAttributeValue("make","Toyota");
das.setDynamicAttributeValue("model","Rav4");
das.setDynamicAttributeValue("luxury",false);
das.setDynamicAttributeValue("cost",12000.5);
das.setDynamicAttributeValue("avg_mpg", 24.5234);
das.setDynamicAttributeValue("total_miles", 5324);    
das.setDynamicAttributeValue("date_purchased", new GlideDateTime());
gs.info('das: ' + das.getValue());
das.setValue('{"luxury":false}');
gs.info('das: ' + das.getValue());
```

Output:

```
*** Script: das: {"total_miles":5324,"color":"blue","model":"Rav4","cost":12000.5,"luxury":false,"avg_mpg":24.5234,"make":"Toyota","date_purchased":"2024-04-19 17:28:47"}
*** Script: das: {"luxury":false}
```

## GlideDynamicAttributeStore - toString\(\)

Returns the content of the GlideDynamicAttributeStore object as a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ggm_kgq_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

GlideDynamicAttribute object as a string.For example: `'{"attr2":"true","attr1":"42.0"}'`

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("color","blue");
das.setDynamicAttributeValue("make","Toyota");
das.setDynamicAttributeValue("model","CRV");
das.setDynamicAttributeValue("luxury",true);
das.setDynamicAttributeValue("cost",12000);
das.setDynamicAttributeValue("avg_mpg",24.5);
das.setDynamicAttributeValue("total_miles",5324);    
das.setDynamicAttributeValue("date_purchased",new GlideDateTime());
gs.info('das: ' + das.toString());
```

Output:

```
*** Script: das: {"cost":"12000.0","color":"blue","avg_mpg":"24.5","date_purchased":"2024-04-19 14:05:00","luxury":"true","model":"CRV","make":"Toyota","total_miles":"5324.123"}

```

