---
title: GlideDynamicAttributeStore - Global
description: The GlideDynamicAttributeStore API provides access to a dynamic attribute store data type, similar to other data types such as string, date, or date/time.Clears all attributes and their values from the GlideDynamicAttributeStore object.Returns the JSON map representation of the values stored in the current GlideDynamicAttributeStore object.Returns the set of dynamic attribute definitions present in the store.Returns the value of the specified attribute within the dynamic attribute store element.Returns the compact string representation of the contents of the current GlideDynamicAttributeStore object.Clears the current GlideDynamicAttributeStore object and then stores the passed JSON map in the GlideDynamicAttributeStore object.Sets the value of the dynamic attribute located at a specified path within a dynamic attribute store element.Sets the dynamic attribute referenced by a specified group/attribute path to a specified value.Sets the internal JSON storage for the field to the String representation of the passed value. If the passed value is another instance of a GlideDynamicAttributeStore object, it copies the values from that object to the current object.Clears the current GlideDynamicAttributeStore object and then stores the passed JSON map in that GlideDynamicAttributeStore object.Returns the content of the GlideDynamicAttributeStore object as a string.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDynamicAttributeStore- Global

The GlideDynamicAttributeStore API provides access to a dynamic attribute store data type, similar to other data types such as string, date, or date/time.

This API provides methods that enable you to get and set dynamic schema attributes within a GlideDynamicAttribute object. These dynamic attributes enable each row in a table to contain different fields. The fields on which this data type is applied are shown as `dynamic_attribute_store` within the column data type description of the table. For more details on dynamic attributes, see [Dynamic schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

To use this API to create dynamic attributes you must have the dynamic\_schema\_writer role. To read dynamic data using this API you must have the dynamic\_schema\_reader role.

The following screenshot shows the dynamic attribute group and associated dynamic attributes that are used in the code examples for this API. The defined attributes provide an example of each of the data types that the dynamic schema implementation supports.

![Dynamic attribute group setup](../images/GDAS-UI_group_setup.png)

There are methods in this API that have the same functionality as dynamic schema methods in the [GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#) API. Use this API if you want to set the same group of dynamic attributes on multiple records. Using this API, you can stage a GlideDynamicAttributeStore object with the desired attributes and then copy that object to multiple GlideRecords using the various setDynamicAttributeValues\(\) methods. Using similar dynamic schema methods in the GlideRecord API performs the actions on a specified GlideRecord.

See also:

-   [GlideDynamicAttribute - Global](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#)
-   [GlideElementDynamicAttributeStore - Global](../../GlideElementDynamicAttributeStore/concept/GlideElementDynamicAttStoreAPI.md#)
-   [GlideTransientDynamicAttribute - Global](../../GlideTransientDynamicAttribute/concept/GlideTransientDynamicAttributeAPI.md#)

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
das.setDynamicAttributeValue("cars->color","blue");
das.setDynamicAttributeValue("cars->make","Toyota");
das.setDynamicAttributeValue("cars->model","CRV");
das.setDynamicAttributeValue("cars->luxury",true);
das.setDynamicAttributeValue("cars->cost",12000.5);
das.setDynamicAttributeValue("cars->avg_mpg",24.5234);
das.setDynamicAttributeValue("cars->total_miles",5324);    
das.setDynamicAttributeValue("cars->date_purchased",new GlideDateTime());
gs.info('das: ' + das.getDisplayValue());
das.clear();
gs.info('das: ' + das.getDisplayValue());
```

Output:

```
*** Script: das: {
  "cars" : {
    "avg_mpg" : "24.5234",
    "color" : "blue",
    "cost" : "12000.5",
    "date_purchased" : "2024-04-19 08:29:52",
    "luxury" : "true",
    "make" : "Toyota",
    "model" : "CRV",
    "total_miles" : "5324"
  }
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
das.setDynamicAttributeValue("cars->color","blue");
das.setDynamicAttributeValue("cars->make","Toyota");
das.setDynamicAttributeValue("cars->model","CRV");
das.setDynamicAttributeValue("cars->luxury",true);
das.setDynamicAttributeValue("cars->cost",12000.5);
das.setDynamicAttributeValue("cars->avg_mpg", 24.5234);
das.setDynamicAttributeValue("cars->total_miles", 5324);
das.setDynamicAttributeValue("cars->date_purchased",new GlideDateTime());
gs.info('Value returned by getValue(): ' + das.getValue());
gs.info('Value returned by getDisplayValue(): ' + das.getDisplayValue());
```

Output:

```
*** Script: Value returned by getValue(): {"cars":{"total_miles":5324,"color":"blue","model":"CRV","cost":12000.5,"luxury":1,"avg_mpg":24.5234,"make":"Toyota","date_purchased":"2024-04-19 15:33:23"}}
*** Script: Value returned by getDisplayValue(): {
  "cars" : {
    "avg_mpg" : "24.5234",
    "color" : "blue",
    "cost" : "12000.5",
    "date_purchased" : "2024-04-19 08:33:23",
    "luxury" : "true",
    "make" : "Toyota",
    "model" : "CRV",
    "total_miles" : "5324"
  }
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

Array containing all transient and non-transient dynamic attributes present in the store.-   [GlideDynamicAttribute](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#) object. Dynamic attributes are defined in the Dynamic Attribute \[dynamic\_attribute\] table with a data type and a sys\_id.
-   [GlideTransientDynamicAttribute](../../GlideTransientDynamicAttribute/concept/GlideTransientDynamicAttributeAPI.md#) object. Transient dynamic attributes are dynamic attributes that have been added to a DynamicAttributeStore field without a definition in the Dynamic Attribute \[dynamic\_attribute\] table. Transient dynamic attributes are handled as strings and have no sys\_id.

**Note:** The Dynamic Attribute \[dynamic\_attribute\] table is accessible by navigating to **All** &gt; **Dynamic Schema** &gt; **Dynamic Attribute Groups**, selecting a group, and selecting the **Dynamic Attributes** tab.

</td></tr></tbody>
</table>The following example shows how to retrieve transient and non-transient dynamic attributes.

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

## GlideDynamicAttributeStore - getDynamicAttributeValue\(String groupAttrPath\)

Returns the value of the specified attribute within the dynamic attribute store element.

<table id="table_psl_m3q_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with.

Table: In the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.

-   `attr_name`: Name of the dynamic attribute within the dynamic group.

Table: In the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.


For example: `"car->color"`

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
das.setDynamicAttributeValue("cars->color","blue");
das.setDynamicAttributeValue("cars->make","Toyota");
das.setDynamicAttributeValue("cars->model","CRV");
das.setDynamicAttributeValue("cars->luxury",true);
das.setDynamicAttributeValue("cars->cost",12000.5);
das.setDynamicAttributeValue("cars->avg_mpg", 24.5234);
das.setDynamicAttributeValue("cars->total_miles", 5324);
das.setDynamicAttributeValue("cars->date_purchased",new GlideDateTime());
gs.info('Value returned by getDynamicAttributeValue(): ' + das.getDynamicAttributeValue("cars->color"));
gs.info('Value returned by getDynamicAttributeValue(): ' + das.getDynamicAttributeValue("cars->luxury"));

```

Output:

```
*** Script: Value returned by getDynamicAttributeValue(): blue
*** Script: Value returned by getDynamicAttributeValue(): 1
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
das.setDynamicAttributeValue("cars->color","blue");
das.setDynamicAttributeValue("cars->make","Toyota");
das.setDynamicAttributeValue("cars->model","CRV");
das.setDynamicAttributeValue("cars->luxury",true);
das.setDynamicAttributeValue("cars->cost",12000.5);
das.setDynamicAttributeValue("cars->avg_mpg", 24.5234);
das.setDynamicAttributeValue("cars->total_miles", 5324);
das.setDynamicAttributeValue("cars->date_purchased",new GlideDateTime());
gs.info('Value returned by getValue(): ' + das.getValue());
gs.info('Value returned by getDisplayValue(): ' + das.getDisplayValue());
```

Output:

```
*** Script: Value returned by getValue(): {"cars":{"total_miles":5324,"color":"blue","model":"CRV","cost":12000.5,"luxury":1,"avg_mpg":24.5234,"make":"Toyota","date_purchased":"2024-04-19 15:33:23"}}
*** Script: Value returned by getDisplayValue(): {
  "cars" : {
    "avg_mpg" : "24.5234",
    "color" : "blue",
    "cost" : "12000.5",
    "date_purchased" : "2024-04-19 08:33:23",
    "luxury" : "true",
    "make" : "Toyota",
    "model" : "CRV",
    "total_miles" : "5324"
  }
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
das.setDynamicAttributeValue("cars->color","blue");
das.setDynamicAttributeValue("cars->make","Toyota");
das.setDynamicAttributeValue("cars->model","CRV");
das.setDynamicAttributeValue("cars->luxury",true);
das.setDynamicAttributeValue("cars->cost",12000.5);
das.setDynamicAttributeValue("cars->avg_mpg", 24.5234);
das.setDynamicAttributeValue("cars->total_miles", 5324);    
das.setDynamicAttributeValue("cars->date_purchased",new GlideDateTime());
gs.info('das: ' + das.getDisplayValue());
das.setDisplayValue('{"cars":{"luxury":false}}');
gs.info('das: ' + das.getDisplayValue());
```

Output:

```
*** Script: das: {
  "cars" : {
    "avg_mpg" : "24.5",
    "color" : "blue",
    "cost" : "12000.0",
    "date_purchased" : "2024-04-19 14:16:49",
    "luxury" : "true",
    "make" : "Toyota",
    "model" : "CRV",
    "total_miles" : "5324.0"
  }
}
*** Script: das: {
  "cars" : {
    "luxury" : "false"
  }
}
```

## GlideDynamicAttributeStore - setDynamicAttributeDisplayValue\(String groupAttrPath, Object value\)

Sets the value of the dynamic attribute located at a specified path within a dynamic attribute store element.

This method works the same as the [GlideDynamicAttributeStore - setDynamicAttributeValue\(String groupAttrPath, Object value\)](GlideDynamicAttStoreAPI.md#) method except in its handling of Boolean and date/time values. This method assumes that all date/time values are provided in the user's locale.

<table id="table_zqq_cxp_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with.

Table: In the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.

-   `attr_name`: Name of the dynamic attribute within the dynamic group.

Table: In the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.


For example: `"car->color"`

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

Updated GlideDynamicAttributeStore object.If the **groupAttrPath** parameter isn't valid, the method throws an `IllegalArgumentException`.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeDisplayValue("cars->color","blue");
das.setDynamicAttributeDisplayValue("cars->make","Toyota");
das.setDynamicAttributeDisplayValue("cars->model","CRV");
das.setDynamicAttributeDisplayValue("cars->luxury","true");
das.setDynamicAttributeDisplayValue("cars->cost",12000.5);
das.setDynamicAttributeDisplayValue("cars->avg_mpg", 24.5234);
das.setDynamicAttributeDisplayValue("cars->total_miles", 5324);    
das.setDynamicAttributeDisplayValue("cars->date_purchased",new GlideDateTime());
gs.info('das: ' + das.getDisplayValue());
das.setDisplayValue('{"cars":{"luxury":"false"}}');
gs.info('das: ' + das.getDisplayValue());
```

Output:

```
*** Script: das: {
  "cars" : {
    "avg_mpg" : "24.5234",
    "color" : "blue",
    "cost" : "12000.5",
    "date_purchased" : "2024-04-19 10:40:45",
    "luxury" : "true",
    "make" : "Toyota",
    "model" : "CRV",
    "total_miles" : "5324"
  }
}
*** Script: das: {
  "cars" : {
    "luxury" : "false"
  }
}
```

## GlideDynamicAttributeStore - setDynamicAttributeValue\(String groupAttrPath, Object value\)

Sets the dynamic attribute referenced by a specified group/attribute path to a specified value.

<table id="table_zgx_1np_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with.

Table: In the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.

-   `attr_name`: Name of the dynamic attribute within the dynamic group.

Table: In the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.


For example: `"car->color"`

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

Updated GlideDynamicAttributeStore object.If the **groupAttrPath** parameter isn't valid, the method throws an `IllegalArgumentException`.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("cars->color","blue");
das.setDynamicAttributeValue("cars->make","Toyota");
das.setDynamicAttributeValue("cars->model","CRV");
das.setDynamicAttributeValue("cars->luxury",true);
das.setDynamicAttributeValue("cars->cost",12000.5);
das.setDynamicAttributeValue("cars->avg_mpg", 24.5234);
das.setDynamicAttributeValue("cars->total_miles", 5324);
das.setDynamicAttributeValue("cars->date_purchased",new GlideDateTime());
gs.info('Value returned by getValue(): ' + das.getValue());
gs.info('Value returned by getDisplayValue(): ' + das.getDisplayValue());
```

Output:

```
*** Script: Value returned by getValue(): {"cars":{"total_miles":5324,"color":"blue","model":"CRV","cost":12000.5,"luxury":1,"avg_mpg":24.5234,"make":"Toyota","date_purchased":"2024-04-19 15:33:23"}}
*** Script: Value returned by getDisplayValue(): {
  "cars" : {
    "avg_mpg" : "24.5234",
    "color" : "blue",
    "cost" : "12000.5",
    "date_purchased" : "2024-04-19 08:33:23",
    "luxury" : "true",
    "make" : "Toyota",
    "model" : "CRV",
    "total_miles" : "5324"
  }
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
otherValues.setDynamicAttributeValue("position->x", 5);
otherValues.setDynamicAttributeValue("position->y", 6);

das.setDynamicAttributeValues(otherValues);
gs.info(das);
```

Output:

```
{"_position":{"x":"5.0","y":"6.0"}}
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

JSON map object to store in the GlideDynamicAttributeStore object. For example: `'{"cars":{"cost":"12500"}}'`

This method ignores any invalid JSON values.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("cars->color","blue");
das.setDynamicAttributeValue("cars->make","Toyota");
das.setDynamicAttributeValue("cars->model","CRV");
das.setDynamicAttributeValue("cars->luxury",true);
das.setDynamicAttributeValue("cars->cost",12000.5);
das.setDynamicAttributeValue("cars->avg_mpg", 24.5234);
das.setDynamicAttributeValue("cars->total_miles", 5324);    
das.setDynamicAttributeValue("cars->date_purchased", new GlideDateTime());
gs.info('das: ' + das.getValue());
das.setValue('{"cars":{"luxury":false}}');
gs.info('das: ' + das.getValue());
```

Output:

```
*** Script: das: {"cars":{"total_miles":5324,"color":"blue","model":"CRV","cost":12000.5,"luxury":true,"avg_mpg":24.5234,"make":"Toyota","date_purchased":"2024-04-19 17:28:47"}}
*** Script: das: {"cars":{"luxury":false}}
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

GlideDynamicAttribute object as a string.For example: '\{"group":\{"attr2":"true","attr1":"42.0"\}\}'

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("cars->color","blue");
das.setDynamicAttributeValue("cars->make","Toyota");
das.setDynamicAttributeValue("cars->model","CRV");
das.setDynamicAttributeValue("cars->luxury",true);
das.setDynamicAttributeValue("cars->cost",12000);
das.setDynamicAttributeValue("cars->avg_mpg",24.5);
das.setDynamicAttributeValue("cars->total_miles",5324);    
das.setDynamicAttributeValue("cars->date_purchased",new GlideDateTime());
gs.info('das: ' + das.toString());
```

Output:

```
*** Script: das: {"cars":{"cost":"12000.0","color":"blue","avg_mpg":"24.5","date_purchased":"2024-04-19 14:05:00","luxury":"true","model":"CRV","make":"Toyota","total_miles":"5324.123"}}

```

