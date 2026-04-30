---
title: GlideElementDynamicAttributeStore - Global
description: The GlideElementDynamicAttributeStore API provides convenient script methods for managing dynamic attributes in the current glide record. Use these methods in conjunction with the GlideRecord API to get and set defined dynamic attribute values.Returns a GlideElementDynamicAttribute object representing the dynamic attribute located at the specified dynamic attribute path.Returns the set of dynamic attribute definitions that are present and stored in a field.Returns the set of dynamic attribute definitions that are pointed to in the schema.Returns the display value of the dynamic attribute located at a specified attribute path within a dynamic attribute store. If a display value is not available, it returns the internal value.Returns the internal value of the dynamic attribute pointed to by a passed-in attribute path within a dynamic attribute store.Sets the attribute pointed to by a specified attribute path in a dynamic attribute store to a specified value.Sets the values specified in the passed GlideElementDynamicAttrbuteStore object in the dynamic attribute store of the current GlideRecord element. The current element's data type must be set to Dynamic Attribute Store.Sets the display value of the dynamic attribute located at a specified path within the dynamic attribute store of the current GlideRecord element.Sets the display values specified in the passed GlideDynamicAttrbuteStore object in the dynamic attributes of the current GlideRecord element. The current element's data type must be set to Dynamic Attribute Store in the associated table.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideElementDynamicAttributeStore- Global

The GlideElementDynamicAttributeStore API provides convenient script methods for managing dynamic attributes in the current glide record. Use these methods in conjunction with the GlideRecord API to get and set defined dynamic attribute values.

To use this API to create dynamic attributes you must have the dynamic\_schema\_writer role. To read dynamic data using this API you must have the dynamic\_schema\_reader role.

This API extends the [GlideElement - Global](../../GlideElement_global/concept/c_GlideElementAPI.md#) API.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

See also:

-   [GlideDynamicAttribute - Global](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#)
-   [GlideDynamicAttributeStore - Global](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)
-   [GlideTransientDynamicAttribute - Global](../../GlideTransientDynamicAttribute/concept/GlideTransientDynamicAttributeAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideElementDynamicAttributeStore - getDynamicAttribute\(String attributePath\)

Returns a GlideElementDynamicAttribute object representing the dynamic attribute located at the specified dynamic attribute path.

<table id="table_gzs_jld_bbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributePath

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
</table><table id="table_hzs_jld_bbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GlideElementDynamicAttribute

</td><td>

Object that contains the specified dynamic attributes. If the **attributePath** parameter contains invalid information, returns a null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
//Gets all the values of the make attribute from the u_inc_dynamic_schema dynamic attribute store column on the incident table
var gr_Inc = new GlideRecord('incident');
gr_Inc.query();
while(gr_Inc.next()) {
    var attr = gr.getDynamicAttribute('inc_dynamic_schema->cars->make');
    gs.info(attr.getValue());
}

//You can also use if(gr_Inc.next()) if you don't want all the values
var gr_Inc = new GlideRecord('incident');
gr_Inc.query();
if(gr_Inc.next()) {
    var attr = gr_Inc.getDynamicAttribute('inc_dynamic_schema->cars->make');
    gs.info(attr.getValue());
}
```

## GlideElementDynamicAttributeStore - getDynamicAttributesInStore\(\)

Returns the set of dynamic attribute definitions that are present and stored in a field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Array of [GlideDynamicAttribute](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#) or [GlideTransientDynamicAttribute](../../GlideTransientDynamicAttribute/concept/GlideTransientDynamicAttributeAPI.md#) objects.|

The following example shows how to retrieve the contents of a stored dynamic attribute, list the attributes it stored, and the attributes in its schema.

```
var record = new GlideRecord('cool_thing');
record.get('number', 'COOL0000005');

gs.info("Store Contents:\n" + JSON.stringify(JSON.parse(record.store1), null, 2) + "\n");
gs.info("Attributes in Store:\n" + record.store1.getDynamicAttributesInStore() + "\n");
gs.info("Attributes in Schema:\n" + record.store1.getDynamicAttributesInSchema() + "\n");
```

Output:

```
*** Script: Store Contents:
{
  "_a": {
    "b": "hello world"
  },
  "_group1": {
    "integer1": "5"
  },
  "_group2": {
    "integer1": "10",
    "string1": "hello"
  }
}

*** Script: Attributes in Store:
a->b,group1->integer1,group2->integer1,group2->string1

*** Script: Attributes in Schema:
group1->integer1,group1->string1,group2->integer1
```

## GlideElementDynamicAttributeStore - getDynamicAttributesInSchema\(\)

Returns the set of dynamic attribute definitions that are pointed to in the schema.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Array of [GlideDynamicAttribute](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#) or [GlideTransientDynamicAttribute](../../GlideTransientDynamicAttribute/concept/GlideTransientDynamicAttributeAPI.md#) objects.|

The following example shows how to retrieve the contents of a stored dynamic attribute, list the attributes it stored, and the attributes in its schema.

```
var record = new GlideRecord('cool_thing');
record.get('number', 'COOL0000005');

gs.info("Store Contents:\n" + JSON.stringify(JSON.parse(record.store1), null, 2) + "\n");
gs.info("Attributes in Store:\n" + record.store1.getDynamicAttributesInStore() + "\n");
gs.info("Attributes in Schema:\n" + record.store1.getDynamicAttributesInSchema() + "\n");
```

Output:

```
*** Script: Store Contents:
{
  "_a": {
    "b": "hello world"
  },
  "_group1": {
    "integer1": "5"
  },
  "_group2": {
    "integer1": "10",
    "string1": "hello"
  }
}

*** Script: Attributes in Store:
a->b,group1->integer1,group2->integer1,group2->string1

*** Script: Attributes in Schema:
group1->integer1,group1->string1,group2->integer1
```

## GlideElementDynamicAttributeStore - getDynamicAttributeDisplayValue\(String attributePath\)

Returns the display value of the dynamic attribute located at a specified attribute path within a dynamic attribute store. If a display value is not available, it returns the internal value.

<table id="table_zn3_1md_bbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributePath

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
</table><table id="table_a43_1md_bbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Value for the associated dynamic attribute in human-readable format.If the **attributePath** parameter contains invalid information, returns a null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
//Gets all the display values of the luxury attribute from the inc_dynamic_schema dynamic attribute store column on the incident table
var gr_Inc = new GlideRecord('incident');
gr_Inc.query();
while(gr_Inc.next()) {
    var attr = gr_Inc.getDynamicAttributeDisplayValue('inc_dynamic_schema->cars->luxury');
    gs.info(attr);
}

//You can also use if(gr.next()) if you don't want all the values
var gr_Inc = new GlideRecord('incident');
gr_Inc.query();

if(gr_Inc.next()) {
    var attr = gr_Inc.getDynamicAttributeDisplayValue('inc_dynamic_schema->cars->luxury');
    gs.info(attr);
}
```

## GlideElementDynamicAttributeStore - getDynamicAttributeValue\(String attributePath\)

Returns the internal value of the dynamic attribute pointed to by a passed-in attribute path within a dynamic attribute store.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_tnp_rld_bbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributePath

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
</table><table id="table_unp_rld_bbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Value of the dynamic attribute pointed to by the passed attribute path.If the **attributePath** parameter contains invalid information, returns a null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.query();

while(gr_Inc.next()) {
    var attr = gr_Inc.getDynamicAttributeValue('inc_dynamic_schema->cars->luxury');
    gs.info(attr);
}
```

Output:

```

*** Script: 1
```

## GlideElementDynamicAttributeStore - setDynamicAttributeValue\(String attributePath, Object value\)

Sets the attribute pointed to by a specified attribute path in a dynamic attribute store to a specified value.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_aj2_vmd_bbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributePath

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

</td><td id="DynS-value-entry">

Value to set in the specified attribute.**Note:** For dynamic attributes, only the following data types are supported:

-   Boolean \(True/False\)
-   Decimal
-   Floating Point Number
-   GlideDate
-   GlideDateTime
-   Integer
-   String

</td></tr></tbody>
</table><table id="table_bj2_vmd_bbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GlideElementDynamicAttributeStore

</td><td>

Returns a GlideElementDynamicAttributeStore object containing the specified value.If the **groupAttributePath** parameter contains invalid information, the attribute is not updated.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
//This simple example inserts a make attribute on the inc_dynamic_schema column where the value of the make attribute is Ford.
var gr_Inc = new GlideRecord('incident');
gr_Inc.setDynamicAttributeValue('inc_dynamic_schema->cars->make', 'Ford');
gr_Inc.insert();
```

## GlideElementDynamicAttributeStore - setDynamicAttributeValues\(GlideDynamicAttributeStore values\)

Sets the values specified in the passed GlideElementDynamicAttrbuteStore object in the dynamic attribute store of the current GlideRecord element. The current element's data type must be set to **Dynamic Attribute Store**.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|values|[GlideDynamicAttributeStore](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)|Object that contains the values to set in the current element's dynamic schema. Values not specified in this object are not updated.|

|Type|Description|
|----|-----------|
|GlideElementDynamicAttributeStore|Updated GlideElementDynamicAttributeStore object.|

The following code example shows how to call this method.

```
var gr_Inc = new GlideRecord('incident');
var das = new GlideDynamicAttributeStore();
das.setDynamicAttributeValue("cars->color", "black");
das.setDynamicAttributeValue("cars->make","Honda");
das.setDynamicAttributeValue("cars->model","CRV");
gr_Inc.setDynamicAttributeValues('inc_dynamic_schema', das);
gr_Inc.insert();
```

This code example inserts the following in the u\_inc\_dynamic\_schema column:

```
{
  "cars" : {
    "color" : "black",
    "make" : "Honda",
    "model" : "CRV"
  }
}
```

## GlideElementDynamicAttributeStore - setDynamicAttributeDisplayValue\(String attributePath\)

Sets the display value of the dynamic attribute located at a specified path within the dynamic attribute store of the current GlideRecord element.

<table id="table_bfg_2nd_bbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributePath

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

Value to set in the current dynamic attribute element.The passed value must be of one of the following data types:

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
|GlideElementDynamicAttributeStore|Object that contains the updated glide element.|

The following code example shows how to call this method.

```
var grFleet = new GlideRecord('u_car_fleet');
grFleet.setDynamicAttributeValue('u_dyn_attr_store', 'car->color', 'Yellow');
grFleet.setDynamicAttributeValue('u_dyn_attr_store', 'car->make', 'Ford');
var sysId = grFleet.insert();
gs.info("Inserted: " + grFleet.u_dyn_attr_store);

var daStore = new GlideDynamicAttributeStore();
daStore.setDynamicAttributeValue('car->color', 'Green');
daStore.setDynamicAttributeValue('car->model', 'Bronco');

var geDynAttrStore = grFleet.getElement('u_dyn_attr_store');
geDynAttrStore.setDynamicAttributeDisplayValues(daStore);
grFleet.update();
gs.info("Updated:  " + grFleet.u_dyn_attr_store);
```

Output:

```
*** Script: Inserted: {"car":{"color":"Yellow","make":"Ford"}}
*** Script: Updated:  {"car":{"color":"Green","make":"Ford","model":"Bronco"}}
```

The following code example shows how a Boolean display value is stored as "1" but is passed back as "true".

```
 var gr_Inc = new GlideRecord('incident');
gr_Inc.setDynamicAttributeDisplayValue('u_inc_dynamic_schema->u_cars->u_luxury', '1');
gr_Inc.insert()
```

Returned value:

```
{
  "u_cars" : {
    "u_luxury" : "true"
  }
}
```

## GlideElementDynamicAttributeStore - setDynamicAttributeDisplayValues\(GlideDynamicAttributeStore values\)

Sets the display values specified in the passed GlideDynamicAttrbuteStore object in the dynamic attributes of the current GlideRecord element. The current element's data type must be set to **Dynamic Attribute Store** in the associated table.

<table id="table_o32_b4d_bbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

values

</td><td>

[GlideDynamicAttributeStore](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)

</td><td>

Object that contains the display values to set in the current element's dynamic attribute store. Display values not specified in this object are not updated. This object must contain both the attribute path and the display value for each attribute to store.For example:

```
{
  "car":{
    "color":"Blue",
    "make":"Ford",
    "model":"Mustang"
  }
}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideElementDynamicAttributeStore|Object that contains the updated glide element.|

The following code example shows how to call this method.

```
var daStore = new GlideDynamicAttributeStore();
daStore.setDynamicAttributeValue('car->make', 'Ford');
daStore.setDynamicAttributeValue('car->model', 'Mustang');
daStore.setDynamicAttributeValue('car->color', 'Blue');
gs.info("daStore: " + daStore);

var gr_Car = new GlideRecord('u_car_fleet');
gr_Car.query();
while(gr_Car.next()) {
  var glideElement = gr_Car.getElement('u_dyn_attr_store');
  glideElement.setDynamicAttributeValues(daStore);
  gr_Car.update();
}
```

