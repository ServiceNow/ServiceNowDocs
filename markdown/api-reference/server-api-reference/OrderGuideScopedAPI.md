---
title: OrderGuide - Scoped
description: The OrderGuide API enables you to initialize and view order guide details.Creates an instance of the OrderGuide class with the specified sys\_id.Returns the sys\_id of the order guide.Initialises the order guide with the specified catalog items and the variables, and returns the order guide.Specifies if the Show Include Toggle \(include\_items\) check box is selected for the specified order guide.Specifies if the two-step checkout is enabled.Specifies if a separate cart \(different from that for catalog items\) usage is enabled for a two-step order guide.Navigates to the catalog items of an order guide.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OrderGuide- Scoped

The OrderGuide API enables you to initialize and view order guide details.

To use this class in a scoped application, use the `sn_sc` namespace identifier. The Service Catalog Scoped API plugin \(com.glideapp.servicecatalog.scoped.api\) that is enabled by default is required to access the OrderGuide API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OrderGuide - OrderGuide\(String sys\_id\)

Creates an instance of the OrderGuide class with the specified sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|sys\_id of the OrderGuide.|

Example:

```
var cart=new sn_sc.OrderGuide("6690750f4f7b4200086eeed18110c761");
```

## OrderGuide - getID\(\)

Returns the sys\_id of the order guide.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|sys\_id of the order guide.|

Example:

```
var cart=new sn_sc.OrderGuide("6690750f4f7b4200086eeed18110c761");	
	console.log(cart.getID());

```

Output:

```
6690750f4f7b4200086eeed18110c761
```

## OrderGuide - init\(Map request\)

Initialises the order guide with the specified catalog items and the variables, and returns the order guide.

|Name|Type|Description|
|----|----|-----------|
|request|Map|A JSON object with the Catalog item and variable details.|

|Type|Description|
|----|-----------|
|Map|A JSON object with the initialised order guide details.|

Example:

```
var guide = new sn_sc.OrderGuide('6690750f4f7b4200086eeed18110c761');
 
var map = {};
map.variables = {};
//map.sysparm_id = '6690750f4f7b4200086eeed18110c761';
map.variables['IOce433d0f4f7b4200086eeed18110c74d'] = '221f3db5c6112284009f4becd3039cc9'; //Here ce433d0f4f7b4200086eeed18110c74d is the sys_id of the variable and 221f3db5c6112284009f4becd3039cc9 is its value
var includedItems = guide.init(map)
```

Output:

```
{
"cascade_variable_map":{
},
"items":[
{
"order":"-1",
"quantity":"1",
"show_quantity":false,
"sys_id":"a4022d7b87c20300e3010cf888cb0bb2"
},
{
"order":"300",
"quantity":"1",
"show_quantity":false,
"sys_id":"186d917a6fab7980575967ddbb3ee4f2"
},
{
"order":"600",
"quantity":"1",
"show_quantity":false,
"sys_id":"8b3ae7fedc1be1004ece5c08239e522b"
}
],
"variable_assignments":{
}
}
```

## OrderGuide - isIncludeItems\(\)

Specifies if the **Show Include Toggle** \(include\_items\) check box is selected for the specified order guide.

**Note:** The **Show Include Toggle** field does not appear on the Order guide form by default.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if the **Show Include Toggle** check box is selected for the specified order guide. Else, returns false.|

```
var orderGuide=new sn_sc.OrderGuide("6690750f4f7b4200086eeed18110c761");	
	console.log(orderGuide.isIncludeItems());
```

Output:

```
true
```

## OrderGuide - isTwoStep\(\)

Specifies if the two-step checkout is enabled.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if the two-step checkout is enabled. Else returns false.|

Example:

```
var orderGuide=new sn_sc.OrderGuide("6690750f4f7b4200086eeed18110c761");	
	console.log(orderGuide.isTwoStep());
```

Output:

```
false
```

## OrderGuide - isUseCustomCart\(\)

Specifies if a separate cart \(different from that for catalog items\) usage is enabled for a two-step order guide.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if a separate cart usage is enabled for a two-step order guide. Else, returns false.|

Example:

```
var orderGuide=new sn_sc.OrderGuide("6690750f4f7b4200086eeed18110c761");	
	console.log (orderGuide.isUseCustomCart());
```

Output:

```
false
```

## OrderGuide - navigateFromMap\(Map itemDetails\)

Navigates to the catalog items of an order guide.

|Name|Type|Description|
|----|----|-----------|
|itemDetails|Map|A JSON object with details of catalog items in the order guide.|

|Type|Description|
|----|-----------|
|void| |

Example:

```
var orderGuide=new sn_sc.OrderGuide.navigateFromMap(itemdetails);
```

