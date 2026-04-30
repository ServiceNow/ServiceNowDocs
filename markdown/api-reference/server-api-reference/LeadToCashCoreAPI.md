---
title: LeadtoCashCore - Scoped
description: The LeadtoCashCore script include provides methods to orchestrate a lead-to-cash workflow in the Lead to Cash Core life cycle.Triggers the PrimitiveUtil\(\) utility method.Returns the data of one or more given entities with a JSON object containing various details such as header, lines, child lines, characteristics, and their attributes.Compares the source and modified source JSON objects of a lead to cash entity and returns a JSON object that describes any changes made to the source JSON, such as any additions, deletions, or modifications.Transforms and applies the source JSON structure of a given entity to the target JSON of another entity. You can then commit the changed entity to the database using the commitInstance\(\) method.Commits the JSON of a given lead to cash entity to the instance, returns a status message with updated information, and updates the Lead to Cash Core Entity table as a result.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 42
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# LeadtoCashCore- Scoped

The LeadtoCashCore script include provides methods to orchestrate a lead-to-cash workflow in the Lead to Cash Core life cycle.

The Lead to Cash Core \(com.snc.l2c.core\) plugin must be activated for LeadtoCashCore script includes to be available in an instance. This plugin can be accessed via the Lead to Cash Core \(com.snc.l2c\_core\) application in the ServiceNow Store. This script include belongs to the sn\_l2c\_core namespace and requires the admin role.

In a lead to cash workflow, you map a source entity to a target entity. An entity is defined as a collection of tables. Source-to-target mapping allows you to transform the structure or content of the source entity to fit the structure or content needed in the target entity. The functionality provided by this script include represents the entity mapping feature available in the Lead to Cash feature. See [Lead to Cash Core](https://www.servicenow.com/docs/access?context=lead-to-cash&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

To complete a workflow using the LeadtoCash script include, you pass return parameters from one method to the next. Typically, you call these methods in the following order:

1.  [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#) - Contains a utility for retrieving the extension point used to invoke scripts. Must be provided with every method call. See the 'Prequisites' section in this topic for more information.
2.  [LeadtoCashCore - createInstance\(String headerSysIDs, String lineSysIDs, Boolean isTarget, Object additionalParams\)](LeadToCashCoreAPI.md#) - Fetches the data of a given entity. For example, customer order-related information including line items and their related data.

    Use the **context** parameter to declare one or more header or line IDs in the script, referred to as "multi-select". Pass the **context.entityConfigId** parameter to invoke the script without any defined mapping. For such multi-select use cases, the output JSON contains a key items array where each entry represents a single entity.

3.  [LeadtoCashCore - delta\(Object sourceJSON, Object dirtyJSON, Object additionalParams\)](LeadToCashCoreAPI.md#) - Compares two JSON inputs and identifies any changes that occurred between them. For example, when something is added, deleted, or modified in an entity.
4.  [LeadtoCashCore - effect\(Object sourceJSON, Object targetJSON, Object additionalParams\)](LeadToCashCoreAPI.md#) - Transforms the source JSON object into a target object.
5.  [LeadtoCashCore - commitInstance\(Object targetJSON, Object additionalParams\)](LeadToCashCoreAPI.md#) - Commits the transformation made in the effect\(\) script include to the database.

**Note:** If necessary, delta\(\) may be skipped in this workflow. However, calling these methods out of order results in an unsuccessful workflow \(for example, when calling commitInstance\(\) and then effect\(\)\).

## Prerequisites

Each of these methods are bundled with an extension point, sn\_l2c\_core.LeadToCashServiceEP. PrimitiveUtil\(\) is a utility which provides methods to get the extension point service and invokes the script includes according to their available parameters. You must first provide PrimitiveUtil\(\) with the getPrimitivesEPService\(\) method, which specifies the table to get source and target information from. For more information, see [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#). Once PrimitiveUtil\(\) and getPrimitivesEPService\(\) are provided in the script, you can then call any of the createInstance\(\), delta\(\), effect\(\), or commitInstance\(\) script includes as needed for your use case.

## Example Lead to Cash Core workflow script

Though each of the available Lead to Cash Core script includes are documented individually, you can reference the following example to see how you can use these methods together to produce a lead to cash work flow.

```
var util = new sn_l2c_core.PrimitiveUtil(); 

// Set the context.isMultiSelect parameter as true to enable multi-select use cases
// Set the context.entityConfigId parameter to the config id of the source entity (sold prodcut) to trigger createInstance with only configId 
var context = {"isMultiSelect": false, "entityConfigId": “sn_l2c_cust_flows_sold_product”}; 

//Flow: Creation of an order from a sold product 
var service = util.getPrimitivesEPService('sn_l2c_cust_flows_sp_to_order', context);  
  
//CREATE INSTANCE to get the data of sold product with sys_id '06670ba3c3adbd501caee74bb0013166' 
var SPInstance = service.createInstance(null, '06670ba3c3adbd501caee74bb0013166');  
gs.info("SPInstance: "+JSON.stringify(SPInstance));  
  
// DELTA  
// construct the dirtyJSON as required  
var deltaOutput = service.delta(SPInstance, dirtyJSON);/  
gs.info("deltaOutput: "+JSON.stringify(deltaOutput));  
  
// EFFECT  
var effectOutput = service.effect(deltaOutput);  
gs.info("effectOutput: " + JSON.stringify(effectOutput));  
  
// COMMIT INSTANCE 
var commitOutput = service.commitInstance(effectOutput);  
gs.info("commitOutput: " + JSON.stringify(commitOutput));
```

In our example, a customer purchased a sold product but now requests a modification on the existing sold product. The required modifications are provided in the form of a dirtyJSON. To apply these modifications, we call the Lead to Cash Core methods in the following order:

1.  The first call gets the existing sold product information using the createInstance\(\) method.
2.  We then compare this source JSON with the dirty JSON using the delta\(\) method, which returns a delta JSON.
3.  The **delta\(\)** JSON is then transformed into a JSON of type order using the effect\(\) method.
4.  The order JSON is committed to the database using the commitInstance\(\) method.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)

Triggers the PrimitiveUtil\(\) utility method.

To use any of the available methods in the LeadtoCashCore script include, you must first always call the scripted extension point PrimitiveUtil\(\) in your script with the getPrimitivesEPService\(\) utility method to trigger the implementation.

<table id="table_nzs_qbn_d1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

context

</td><td>

Object

</td><td>

Optional. Additional parameter options for displaying attribute values and for invoking more than one instance at a time.```
"context": {
  "entityConfigId": "String",
  "isMultiSelect": "Boolean",
  "loadDisplayValue": "Boolean"
}
```

</td></tr><tr><td>

context.entityConfigId

</td><td>

String

</td><td>

Optional. Configuration ID of the entity. If both **entityConfigId** and **sourceToTargetConﬁgID** are provided, priority is given to **entityConfigId**.Table: Lead To Cash Entity \[sn\_l2c\_core\_entity\]

Data type: String

</td></tr><tr><td>

context.isMultiSelect

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to pass multiple entities as input to create the instance. Valid values:

-   true: Enables the passing of multiple entities as input. When true, you can pass multiple line items in a comma-separated list.
-   false: Doesn't enable the passing of multiple entities as input. Only one input may be passed in the API script.

Default: false

</td></tr><tr><td>

context.loadDisplayValue

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to load the display value for each attribute.Valid values:

-   true: Enables the loading of an attribute's display value.
-   false: Doesn't enable the loading of an attribute's display value.

Default: false

</td></tr><tr><td>

sourceToTargetConfigID

</td><td>

String

</td><td>

Mapping configuration ID for the source-to-target mapping. Table: Lead To Cash Entity Mapping \[sn\_l2c\_core\_entity\_mapping\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example invokes PrimitiveUtil\(\) and picks an implementation based on sn\_l2c\_cust\_flows\_sp\_to\_order, which is a Mapping Config ID in the Lead To Cash Entity Mapping \[sn\_l2c\_core\_entity\_mapping\] table.

```
//Utility to invoke createInstance API  
var util = new sn_l2c_core.PrimitiveUtil(); 
var context = {"isMultiSelect": true}; // Set the context.isMultiSelect parameter as true to enable multi-select use cases.

//Invokes the extension point and specifies an implementation based on sourceToTargetConfigID of a L2C flow.  
var service = util.getPrimitivesEPService('sn_l2c_cust_flows_sp_to_order’, context)
```

The following example invokes PrimitiveUtil\(\) and picks an implementation based on the configId, `l2c_order`, in the Lead To Cash Entity \[sn\_l2c\_core\_entity\] table.

```
//Utility to invoke createInstance API   
var util = new sn_l2c_core.PrimitiveUtil();  
var context = {"isMultiSelect": true, “entityConfigId”: “l2c_order”};  
// Set the context.isMultiSelect parameter as true to enable multi-select use cases. 
// Set the context.entityConfigId parameter if createInstance needs to be invoked with only configId. 
 
//Invokes the extension point and uses default implementation based on entityConfigId of a L2C flow.   
var service = util.getPrimitivesEPService('’, context); 
```

## LeadtoCashCore - createInstance\(String headerSysIDs, String lineSysIDs, Boolean isTarget, Object additionalParams\)

Returns the data of one or more given entities with a JSON object containing various details such as header, lines, child lines, characteristics, and their attributes.

Use the output JSON of the createInstance\(\) method in subsequent methods of the Lead to Cash Core workflow such as delta\(\), effect\(\), and commitInstance\(\).

### Requirements

The LeadtoCashCore script include requires you to first call the script utility method PrimitiveUtil\(\) with the [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#) utility method to trigger the implementation before calling createInstance\(\) in your script. Per each flow, get the service only once and use the same service for all LeadtoCashCore methods.

### Considerations

-   To enable createInstance\(\) to pass multiple, comma-separated headerIDs or lineIDs at a time, set the getPrimitivesEPService\(\) boolean parameter **context.isMultiSelect** to true. Otherwise, you can only pass one ID at a time. The single headerID use case with multiple lineIDs is supported without setting **context.isMultiSelect** to true.

-   To enable createInstance\(\) to be invoked with only the configuration ID of the entity, set the getPrimitivesEPService\(\) String parameter, **context.entityConfigId**. If both entityConfigId and sourceToTargetConfigID are passed, entityConfigId is prioritized to execute createInstance\(\).

    For more information about this functionality, see [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#).

-   To partially update a Related Party, set a type in the **allowedContextTypes** parameter.

<table id="table_rn1_yzl_d1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

additionalParams

</td><td>

Object

</td><td>

Optional. Additional parameters to use.

</td></tr><tr><td>

additionalParams.skipLines

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to fetch line items for the specified entity.Valid values:

-   true: Skip returning line items information for the entity.
-   false: Return line items information for the entity.

Default: false

</td></tr><tr><td>

additionalParams.allowedContextTypes

</td><td>

Array of Strings

</td><td>

Optional. Object used to populate and process only the selected types and avoid unrelated sections \(like line items\) when updating Related Parties \(for example, partners, business organizations, contacts\).

-   For header-based partial sync, `header` must be passed in **allowedContextTypes**. Without it, the createInstance\(\) method can't build the root structure.
-   For non-header partial sync, `lineItems` must be passed in **allowedContextTypes**. Without it, the createInstance\(\) method can't build a valid structure for processing child data.

 ```
allowedContextTypes: ["header","headerRelatedParty"]  }; 
```

</td></tr><tr><td>

headerSysIDs

</td><td>

String

</td><td>

Header sys\_id\(s\) of an entity to retrieve data from. Required if you don't provide the **lineSysIDs** parameter. Pass `null` if you aren't passing any header sys\_ids.To designate one or more header sys\_ids in your script, set `context.isMultiSelect = true` in the getPrimitivesEPService\(\) utility method. For more details, see the Parameters table in [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#).

**Note:** At least one **headerSysID** or **lineSysIDs** parameter is required.

</td></tr><tr><td>

isTarget

</td><td>

Boolean

</td><td>

Optional. Flag that determines whether to fetch target entity data.Valid values:

-   true: Fetch data of the target entity.
-   false: Don't fetch data of the target entity.

Default: false

</td></tr><tr><td>

lineSysIDs

</td><td>

String

</td><td>

Line item sys\_id\(s\) of an entity to retrieve entity data from. Required if you don't provide **headerSysIDs** and if the entity structure starts with line items such as sold product. To designate one or more line item sys\_ids in your script, set `context.isMultiSelect = true` in the getPrimitivesEPService\(\) utility method. For more details, see the Parameters table in [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#).

**Note:** At least one **headerSysID** or **lineSysIDs** parameter is required. If passing multiple **lineSysIDs**, all records must belong to the same **headerSysID**.

</td></tr></tbody>
</table><table id="id_hfh_p13_h1c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON Object

</td><td>

A JSON containing details of the entity record.Data type: Array of objects

```
{
"items": [
  {
  "attributes": {Object},
  "sys_id": {Object},
  "table": "String",
  "lineItems": [
    {
     "attributes": {Object},
     "sys_id": {Object},
     "table": "String",
     "characteristics": [Array],
     "lineItems": [Array]
     }
    ],
  "characteristics": [Array],
  "_state": "String"
  }
 ]
}
```

</td></tr><tr><td>

\_state

</td><td>

Activity state of the entity.Possible values:

-   active: The entity is active.
-   inactive: The entity is inactive.

Default: active

Data type: String

</td></tr><tr><td>

characteristics

</td><td>

List of entity characteristics. Characteristics may vary between entities.Data type: Array of objects

```
"characteristics": [  
        {  
          "attributes": {Object},
          "sys_id": {Object},  
          "table": "String"
        }  
      ]
```

</td></tr><tr><td>

characteristics.attributes

</td><td>

One or more objects that contain information about attributes associated with the characteristic record. The &lt;attribute type&gt; can be different values based on the records/functionality associated with the characteristic. For example, this object could contain references to the attributes record's sys\_id, associated characteristic records, characteristic option records, or sold product information.Data type: Object

```
"attributes": {
  "<attribute_type>": {Object}
}
```

</td></tr><tr><td>

characteristics.attributes.&lt;attribute\_type&gt;

</td><td>

Information about the key name of the item attribute.```
"<key_name>": { 
  "value": "String" 
}
```

Data type: Object

</td></tr><tr><td>

characteristics.attributes.&lt;attribute\_type&gt;.value

</td><td>

Typically the sys\_id of the of the associate attribute record, but can be any meaningful text string that describes the associated attribute type.Data type: String

</td></tr><tr><td>

characteristics.sys\_id

</td><td>

Object containing the sys\_id of the associated characteristic record.Data type: Object

```
"sys_id": { 
  "value": "String" 
 }
```

</td></tr><tr><td>

characteristics.sys\_id.value

</td><td>

Sys\_id of the associated characteristic record.Data type: String

</td></tr><tr><td>

characteristics.table

</td><td>

Name of the table that contains the characteristic record of the lead to cash entity.Data type: String

</td></tr><tr><td>

items

</td><td>

Contains an array of selected objects when **context.isMultiSelect** is set to true.Data type: Array of Objects

```
"items": [
{ 
  "attributes": {Object}, 
  "sys_id": {Object}, 
  "table": "String",
  "lineItems": [Array]
 }, 
]
```

</td></tr><tr><td>

items.attributes

</td><td>

Attributes of the item record. Attributes may vary between entities.```
"attributes": {
  "account": {Object},
  "name": {Object}
}
```

Data type: Object

</td></tr><tr><td>

items.attributes.account

</td><td>

Information about the account associated with the item attribute.```
"account": { 
  "value": "String" 
}
```

</td></tr><tr><td>

items.attributes.account.value

</td><td>

Attributes of the item. Attributes may vary between entities.```
"attributes": {
  "account": {Object},
  "<key_name>": {Object}
}
```

Data type: Object

</td></tr><tr><td>

items.attributes.&lt;key\_name&gt;

</td><td>

Information about the key name of the item attribute.```
"<key_name>": { 
  "value": "String" 
}
```

Data type: Object

</td></tr><tr><td>

items.attributes.&lt;key\_name&gt;.value

</td><td>

Value of the key name attribute.Data type: String

</td></tr><tr><td>

items.sys\_id

</td><td>

Object containing sys\_id information about the entity item. Values vary between entities.Data type: Object

```
"sys_id": {
  "value": "String"
}
```

</td></tr><tr><td>

items.sys\_id.value

</td><td>

Sys\_id of an associated item.Data type: String

</td></tr><tr><td>

items.table

</td><td>

Name of the table that contains line item record associated with the lead to cash entity.Data type: String

</td></tr><tr><td>

items.lineItems

</td><td>

JSON object that contains the line item details of the entity record. Data type: Array of objects

```
"lineItems": [ 
  { 
    "attributes": {Object},
    "characteristics": [Array],
    "lineItems": [Array],
    "_state": "String",
    "sys_id": {Object},
    "table": "String"
  }
]
```

</td></tr><tr><td>

items.lineItems.\_state

</td><td>

Activity state of the line item entity.Possible values:

-   active: The entity is active.
-   inactive: The entity is inactive.

Default: active

Data type: String

</td></tr><tr><td>

items.lineItems.attributes

</td><td>

Attributes of the line item record. Attributes may vary between entities.```
"attributes": {
  "account": {Object},
  "<key_name>": {Object}
}
```

Data type: Object

</td></tr><tr><td>

items.lineItems.attributes.&lt;key\_name&gt;

</td><td>

Information about the key name of the line item attribute.```
"<key_name>": { 
  "value": "String" 
}
```

Data type: Object

</td></tr><tr><td>

items.lineItems.attributes.&lt;key\_name&gt;.value

</td><td>

Value of the key name attribute.Data type: String

</td></tr><tr><td>

items.lineItems.attributes.account

</td><td>

Information about the account associated with the line item attribute.```
"account": { 
  "value": "String" 
}
```

</td></tr><tr><td>

items.lineItems.attributes.account.value

</td><td>

Sys\_id of the account associated with the line item attribute.Data type: String

</td></tr><tr><td>

items.lineItems.characteristics

</td><td>

List of characteristics associated with the line item. Characteristics may vary between entities.Data type: Array of objects

```
"characteristics": [  
        {  
          "attributes": {Object},
          "sys_id": {Object},  
          "table": "String"
        }  
      ]
```

</td></tr><tr><td>

items.lineItems.characteristics.attributes

</td><td>

One or more objects that contain information about attributes associated with the characteristic record. The &lt;attribute type&gt; can be different values based on the records/functionality associated with the characteristic. For example, this object could contain references to the attributes record's sys\_id, associated characteristic records, characteristic option records, or sold product information.Data type: Object

```
"attributes": {
  "<attribute_type>": {Object}
}
```

</td></tr><tr><td>

items.lineItems.characteristics.attributes.&lt;attribute\_type&gt;.value

</td><td>

Typically the sys\_id of the of the associate attribute record, but can be any meaningful text string that describes the associated attribute type.Data type: String

</td></tr><tr><td>

items.lineItems.characteristics.sys\_id

</td><td>

Object containing the sys\_id of the associated characteristic record.Data type: Object

```
"sys_id": { 
  "value": "String" 
 }
```

</td></tr><tr><td>

items.lineItems.characteristics.sys\_id.value

</td><td>

Sys\_id of the associated characteristic record.Data type: String

</td></tr><tr><td>

items.lineItems.characteristics.table

</td><td>

Name of the table that contains the characteristic record of the lead to cash entity.Data type: String

</td></tr><tr><td>

items.lineItems.lineItems

</td><td>

Child line items of a parent line item. This object has the same format as the **lineItems** parameter.Data type: Object

```
"lineItems": [
  { 
    "attributes": {Object},
    "characteristics": [Array],
    "lineItems": [Array],
    "_state": {Object},
    "sys_id": {Object},
    "table": "String"
  }
] 
```

</td></tr><tr><td>

items.lineItems.sys\_id

</td><td>

Object containing sys\_id information about the associated line item record.Data type: Object

```
"sys_id": {
  "value": "String"
}
```

</td></tr><tr><td>

items.lineItems.sys\_id.value

</td><td>

Sys\_id of an associated line item record.Data type: String

</td></tr><tr><td>

items.lineItems.table

</td><td>

Name of the table that contains the line item record associated with the lead to cash entity.Data type: String

</td></tr></tbody>
</table>The example script below invokes the createInstance\(\) method to load the data of a sold product, its entire hierarchy, and its characteristics.

```
//Utility to invoke createInstance API 
var util = new sn_l2c_core.PrimitiveUtil();  
 
//Invoke extension point, picks an implementation based on sourceToTargetConfigID of a L2C flow, the Mapping Config ID  in "sn_l2c_core_entity_mapping" table. 
var service = util.getPrimitivesEPService('sn_l2c_cust_flows_sp_to_order'); 
 
//Invoke createInstance API with required params 
var SPInstance = service.createInstance(null, '4e03cda2ec873110f87727ef5883a2cf'); 
 
//Print the returned JSON 
gs.info("SPInstance: "+JSON.stringify(SPInstance));  
 
//The returned JSON can be used for subsequent methods of the flow such as delta(), effect() and commitInstance()
```

Output:

```
{ 
  "lineItems": [ 
    { 
      "table": "sn_install_base_sold_product", 
      "sys_id": { 
        "value": "4e03cda2ec873110f87727ef5883a2cf" 
      }, 
      "attributes": { 
        "name": { 
          "value": "Quadplay Home Tech Hub Bundle" 
        }, 
        "account": { 
          "value": "9e2fd2ee11b43110f877366201dea674" 
        } 
      }, 
      "lineItems": [ 
        { 
          "table": "sn_install_base_sold_product", 
          "sys_id": { 
            "value": "9e0301e2ec873110f87727ef5883a23a" 
          }, 
          "attributes": { 
            "name": { 
              "value": "Internet and OTT Bundle" 
            }, 
          "_state": "active",
          "account": { 
              "value": "9e2fd2ee11b43110f877366201dea674" 
            } 
          }, 
          "lineItems": [ 
          ], 
          "characteristics": [] 
        } 
      ], 
      "characteristics": [ 
        { 
          "table": "sn_prd_pm_product_characteristics", 
          "sys_id": { 
            "value": "8d669b6665ebf110f877d71ec56bf75c" 
          }, 
          "attributes": { 
            "sys_id": { 
              "value": "8d669b6665ebf110f87d71ec56bf75c" 
            },
          "_state": "active", 
          "characteristic_value": { 
              "value": "" 
            }, 
          "characteristic": { 
              "value": "4f31999fd0a63110f8770dbf976be178" 
            }, 
          "characteristic_option": { 
              "value": "4f31999fd0a63110f8770dbf976be179" 
            }, 
          "sold_product": { 
              "value": "4e03cda2ec873110f87727ef5883a2cf" 
            } 
          } 
        } 
      ] 
    } 
  ] 
}
```

### Multi-select

The following script demonstrates how to use **isMultiSelect** to invoke the createInstance\(\) method and load the data of two sold products with their entire hierarchy and characteristics.

```
//Utility to invoke createInstance API  
var util = new sn_l2c_core.PrimitiveUtil();   

//Set context variable isMultiSelect true to enable multi-select 
var context = {"isMultiSelect": true}; 
//Invoke extension point, picks an implementation based on sourceToTargetConfigID of a L2C flow, the Mapping Config ID  in “sn_l2c_core_entity_mapping” table.  
var service = util.getPrimitivesEPService('sn_l2c_cust_flows_sp_to_order’, context);  
  
//Multiple sold products selected  
var selectedLineitems = '4e03cda2ec873110f87727ef5883a2cf,036a2349284d0210f877b68370fb2e93'; 

//Invoke createInstance API with required params  
var SPInstance = service.createInstance(null, selectedLineitems);  
  
//Print the returned JSON  
gs.info("SPInstance: "+JSON.stringify(SPInstance));   
  
//The returned JSON can be used for subsequent APIs of the flow such as Delta, Effect and Commit Instance 
```

Response:

```
{  
  "items": [ 
    { 
      "lineItems": [ 
        { 
          "table": "sn_install_base_sold_product", 
          "sys_id": { 
            "value": "4e03cda2ec873110f87727ef5883a2cf" 
          }, 
          "attributes": { 
            "name": { 
              "value": "Quadplay Home Tech Hub Bundle" 
            }, 
            "account": { 
              "value": "9e2fd2ee11b43110f877366201dea674" 
            } 
          }, 
          "lineItems": [ 
            { 
              "table": "sn_install_base_sold_product", 
              "sys_id": { 
                "value": "9e0301e2ec873110f87727ef5883a23a" 
              }, 
              "attributes": { 
                "name": { 
                  "value": "Internet and OTT Bundle" 
                }, 
                "account": { 
                  "value": "9e2fd2ee11b43110f877366201dea674" 
                } 
              }, 
              "lineItems": [], 
              "characteristics": [] 
            } 
          ] 
        } 
      ] 
    }, 
    { 
      "lineItems": [ 
        { 
          "table": "sn_install_base_sold_product", 
          "sys_id": { 
            "value": "036a2349284d0210f877b68370fb2e93" 
          }, 
          "attributes": { 
            "name": { 
              "value": "Quadplay Home Tech Hub Bundle" 
            }, 
            "account": { 
              "value": "9e2fd2ee11b43110f877366201dea674" 
            } 
          }, 
          "lineItems": [ 
            { 
              "table": "sn_install_base_sold_product", 
              "sys_id": { 
                "value": "4b6a2349284d0210f877b68370fb2e9c" 
              }, 
              "attributes": { 
                "name": { 
                  "value": "Internet and OTT Bundle" 
                }, 
                "account": { 
                  "value": "9e2fd2ee11b43110f877366201dea674" 
                } 
              }, 
              "lineItems": [], 
              "characteristics": [] 
            } 
          ], 
          "characteristics": [],
          "_state": "active" 
        } 
      ] 
    } 
  ] 
}
```

### Invoke createInstance\(\) with entityConfigId

The example script below invokes the createInstance\(\) method to load the data of an order, its entire hierarchy, and its characteristics. The example demonstrates in an sp to order flow, we want to fetch the sales agreement data attached to the sold product.

```
// Utility to invoke createInstance API
var util = new sn_l2c_core.PrimitiveUtil();

var quoteToSA = "sn_l2c_quote_to_sales_agreement_pricing";

var context = {
  "entityConfigId": "sn_l2c_sales_agreement"
};

var spToOrder = "sn_l2c_cust_flows_sp_to_order";

var service = util.getPrimitivesEPService(spToOrder, context);

var createInstanceOutput = service.createInstance("c8e1e678432242105eba72eb3ab8f261");

gs.info("Sales Agreement JSON " + JSON.stringify(createInstanceOutput));

// The returned JSON can be used for subsequent methods of the flow such as delta(), effect() and commitInstance()
```

Output:

```
{
  "table": "sn_sales_agmt_core_sales_agreement",
  "sys_id": {
    "value": "c8e1e678432242105eba72eb3ab8f261"
  },
  "attributes": {
    "account": {
      "value": "051f62b0d7300200e5982cf65e610333"
    },
    "short_description": {
      "value": "1 year sales agreement for Spark Technologies"
    }
  },
  "lineItems": [
    {
      "table": "sn_sales_agmt_core_sales_agreement_line",
      "sys_id": {
        "value": "4104369034641210f877af77d9dd31bb"
      },
      "attributes": {
        "sales_agreement": {
          "value": "c8e1e678432242105eba72eb3ab8f261"
        },
        "short_description": {
          "value": "Home Automation Bundle"
        }
      },
      "lineItems": [
        {
          "table": "sn_sales_agmt_core_sales_agreement_line",
          "sys_id": {
            "value": "45e6fa4a436a02105eba72eb3ab8f247"
          },
          "attributes": {
            "sales_agreement": {
              "value": "c8e1e678432242105eba72eb3ab8f261"
            },
            "short_description": {
              "value": "Outdoor Camera"
            }
          },
          "lineItems": [],
          "characteristics": [],
          "pricingAdjustments": []
        },
        {
          "table": "sn_sales_agmt_core_sales_agreement_line",
          "sys_id": {
            "value": "73e6fa4a436a02105eba72eb3ab8f25a"
          },
          "attributes": {
            "sales_agreement": {
              "value": "c8e1e678432242105eba72eb3ab8f261"
            },
            "short_description": {
              "value": "Indoor Camera"
            }
          },
          "lineItems": [],
          "characteristics": [],
          "pricingAdjustments": []
        }
      ],
      "characteristics": [],
      "pricingAdjustments": []
    }
  ]
}
```

### Partial sync of Related Parties using allowedContextTypes

The following createInstance\(\) script sets **allowedContextTypes** with "`header`" and "`ramp`" to output only those two populated sections in the sn\_l2c\_quote\_to\_order table.

```
var util = new sn_l2c_core.PrimitiveUtil();
var service = util.getPrimitivesEPService('sn_l2c_quote_to_order'); // WITH HEADER FLOW
var quoteId = '0b0f5cc8f11f3110f8777d7194f16610';
var additionalParams = {
  allowedContextTypes: ["header","ramp"]
};

var quoteInstance = service.createInstance(quoteId, null, false, additionalParams);
```

Output. The output contains only those two populated sections defined in the **allowedContextTypes**. All other contexts \(lines, childLines, characteristics, etc.\) are empty or omitted, allowing partial sync.

```

{
  "table": "sn_quote_mgmt_core_quote",
  "sys_id": {
    "value": "0b0f5cc8f11f3110f8777d7194f16610"
  },
  "attributes": {
    "renewal_adjustment_value": { "value": "" },
    "contract_start_date": { "value": "2024-01-01" },
    "total_net_new_amount": { "value": "USD;0" },
    "agreement_start_date": { "value": "" },
    "total_one_time_price": { "value": "USD;0" },
    "consumer": { "value": "" },
    "billing_location": { "value": "" },
    "document_template": { "value": "" },
    "pricelist": { "value": "19d29513d0e63110f8770dbf976be122" },
    "assignment_group": { "value": "a4b31c0cf1db3110f8777d7194f166e9" },
    "partner_contact": { "value": "" },
    "auto_generated_for_renewal": { "value": "false" },
    "contract_end_date": { "value": "2025-12-31" },
    "active": { "value": "true" },
    "billing_state": { "value": "" },
    "external_system": { "value": "" },
    "renewal_adjustment_type": { "value": "" },
    "source_opportunity": { "value": "" },
    "total_annual_recurring_price_v2": { "value": "USD;4100" },
    "internal_signer": { "value": "" },
    "costbook": { "value": "a3042cdce405c210f8773750028d6f72" },
    "payment_terms": { "value": "" },
    "shipping_location": { "value": "" },
    "seller_organization": { "value": "" },
    "contact": { "value": "4d147a386f0331003b3c498f5d3ee437" },
    "external_id": { "value": "" },
    "transaction_date": { "value": "2023-12-18 23:56:14" },
    "version": { "value": "1" },
    "billing_zip": { "value": "" },
    "previous_quote": { "value": "" },
    "assigned_to": { "value": "31cbccccf19b3110f8777d7194f166ce" },
    "total_monthly_recurring_price_v2": { "value": "USD;341.6666" },
    "agreement_end_date": { "value": "" },
    "contract_type": { "value": "" },
    "renewal_adjustment_basis": { "value": "" },
    "header_api": { "value": "" },
    "channel": { "value": "agent_assist" },
    "existing_contract": { "value": "" },
    "state": { "value": "draft" },
    "header_id": { "value": "0b0f5cc8f11f3110f8777d7194f16610" },
    "account": { "value": "86837a386f0331003b3c498f5d3ee4ca" },
    "quote_type": { "value": "add" },
    "billing_street": { "value": "" },
    "same_as_shipping_address": { "value": "false" },
    "work_notes": { "value": "" },
    "comments": { "value": "" },
    "short_description": { "value": "B2B - Elevator Platinum Maintenance Plan" },
    "partner": { "value": "" },
    "rfq": { "value": "" },
    "sales_agreement": { "value": "" },
    "total_renewal_amount": { "value": "USD;0" },
    "sa_quote": { "value": "false" },
    "external_signer": { "value": "" },
    "shipping_city": { "value": "" },
    "discount_percentage": { "value": "" },
    "expiration_date": { "value": "" },
    "billing_city": { "value": "" },
    "currency": { "value": "USD" },
    "shipping_country": { "value": "" },
    "billing_country": { "value": "" },
    "record_number": { "value": "QT0000002" },
    "shipping_state": { "value": "" },
    "initial_quote": { "value": "0b0f5cc8f11f3110f8777d7194f16610" },
    "shipping_street": { "value": "" },
    "shipping_zip": { "value": "" },
    "total_amount": { "value": "USD;3710.0258" },
    "term_month": { "value": "24" },
    "total_upsell_downsell_amount": { "value": "USD;0" },
    "auto_renew": { "value": "false" }
  },
  "ramp": [
    {
      "table": "sn_quote_mgmt_core_quote_line_ramp",
      "sys_id": { "value": "603703c170d6b210f8772b33c4167462" },
      "attributes": {
        "quote": { "value": "0b0f5cc8f11f3110f8777d7194f16610" },
        "ramp_type": { "value": "yearly" },
        "start_date": { "value": "" },
        "end_date": { "value": "" },
        "term_month": { "value": "" },
        "name": { "value": "" },
        "annual_percentage_increase": { "value": "" },
        "sys_id": { "value": "603703c170d6b210f8772b33c4167462" },
        "ramp_key": { "value": "" }
      }
    },
    {
      "table": "sn_quote_mgmt_core_quote_line_ramp",
      "sys_id": { "value": "c6b7c70570d6b210f8772b33c41674e8" },
      "attributes": {
        "quote": { "value": "0b0f5cc8f11f3110f8777d7194f16610" },
        "ramp_type": { "value": "yearly" },
        "start_date": { "value": "" },
        "end_date": { "value": "" },
        "term_month": { "value": "" },
        "name": { "value": "" },
        "annual_percentage_increase": { "value": "" },
        "sys_id": { "value": "c6b7c70570d6b210f8772b33c41674e8" },
        "ramp_key": { "value": "" }
      }
    }
  ],
  "lineItems": [],
  "headerRelatedParty": []
}
```

## LeadtoCashCore - delta\(Object sourceJSON, Object dirtyJSON, Object additionalParams\)

Compares the source and modified source JSON objects of a lead to cash entity and returns a JSON object that describes any changes made to the source JSON, such as any additions, deletions, or modifications.

**Note:** The LeadtoCashCore script include requires you to first call the scripted extension point PrimitiveUtil\(\) with the [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#) utility method to trigger the implementation before calling delta\(\) in your script. Per each flow, get the service only once and use the same service for all LeadtoCashCore methods.

To enable delta\(\) to be invoked with only the configuration ID of the entity, set the getPrimitivesEPService\(\) string parameter, **context.entityConfigId**. If both **entityConfigId** and **sourceToTargetConfigID** are passed, **entityConfigId** is prioritized to execute delta\(\).

<table id="table_hvh_twm_d1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sourceJSON

</td><td>

Object

</td><td>

JSON object of the source lead to cash entity. **Note:** Use the [LeadtoCashCore - createInstance\(String headerSysIDs, String lineSysIDs, Boolean isTarget, Object additionalParams\)](LeadToCashCoreAPI.md#) method to retrieve the source JSON of an entity.

</td></tr><tr><td>

dirtyJSON

</td><td>

Object

</td><td>

Modified source JSON of the lead to cash entity.

</td></tr><tr><td>

additionalParams

</td><td>

Object

</td><td>

Optional. Additional parameters to use.

</td></tr><tr><td>

additionalParams.delta\_ignore\_attributes

</td><td>

Object

</td><td>

Table attributes to ignore during comparison between the source and dirtyJSON. Enables support of reconfiguration  use cases.```
{  
“<table_name>”: [<attribute_name1>, attribute_name2>] 
}
```

</td></tr><tr><td>

additionalParams.delta\_ignore\_attributes.&lt;table\_name&gt;

</td><td>

String

</td><td>

The name of the table and its associated attributes to ignore.For example:

```
{  
“sn_install_base_sold_product”: [“state”,”unit_price”]  
}
```

</td></tr><tr><td>

additionalParams.loadDisplayValue

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to load the display value for each attribute.Valid values:

-   true: Enables the loading of an attribute's display value.
-   false: Doesn't enable the loading of an attribute's display value.

Default: false

</td></tr></tbody>
</table><table id="leadtocore-return-parameters" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON Object

</td><td>

An object containing details of the entity record with any changes that occurred between the sourceJSON and dirtyJSON.Data type: Object

```
{
"lineItems": [Array] 
}
```

</td></tr><tr><td>

lineItems

</td><td>

JSON object that contains the line item details of the entity record. For example, order line items or quote line items. Data type: Array of objects

```
"lineItems": [ 
 {
  "_action": "String",
  "attributes": {Object}
  "characteristics": [Array]
  "lineItems": [Array],
  "sys_id": {Object},
  "table": "String"
 } 
]
```

</td></tr><tr><td>

lineItems.\_action

</td><td id="l2c-returns-lineItems._action-entry">

Change action applied to the line item of the source JSON. Possible values:

-   add: Information was added to the source JSON.
-   change: Information was updated in the source JSON.
-   disconnect: Information was disconnected from the source JSON.
-   nochange: No change occurred on the source JSON.

Data type: String

</td></tr><tr><td>

lineItems.attributes

</td><td id="l2c-returns-lineItems.attributes-returns">

Attributes of the line item. For example, the attribute's name and value. May contain varying fields based on the entity.Data type: Object

```
"attributes": { 
  "<attribute_name>": {Object}
}
```

</td></tr><tr><td>

lineitems.attributes.&lt;attribute\_name&gt;

</td><td id="l2c-returns-lineItems.attributes.attribute_name-returns">

Name of the line item attribute. For example, the name of an account or contact. May contain varying fields of the entity.Data type: Object

```
"attributes": { 
 "<attribute_name>": { 
   "value": "String"
 }
}
```

</td></tr><tr><td>

lineitems.attributes.&lt;attribute\_name&gt;.value

</td><td id="l2c-returns-lineItems.attributes.attribute_name.value-returns">

Value of the line item attribute. Data type: String

</td></tr><tr><td>

lineItems.attributes.account

</td><td id="l2c-returns-lineItems-attributes.account-returns">

Information about the account associated with the item attribute.Data type: Object

```
"account": { 
  "value": "String" 
}
```

</td></tr><tr><td>

lineItems.attributes.account.value

</td><td id="l2c-returns-lineItems.attributes.account.value-returns">

Sys\_id of the account associated with the line item attribute.Data type: String

</td></tr><tr><td>

lineItems.characteristics

</td><td>

Characteristics of the line item. May contain varying fields based on the entity.Data type: Array of Objects

```
"characteristics": [  
 {  
  "attributes": {Object},
  "sys_id": {Object},  
  "table": "String"
  }  
]
```

</td></tr><tr><td>

lineItems.characteristics.attributes

</td><td>

Attributes of the header record characteristics. For example, the attribute's name and value. May contain varying fields based on the entity.Data type: Object

```
"attributes": { 
 "<field_name>": { 
 "value": "String"
}
```

</td></tr><tr><td>

lineitems.characteristics.attributes.&lt;field\_name&gt;

</td><td id="l2c-returns-lineItems.attributes.field_name-returns">

Attribute name of the characteristic record associated with the line item.Data type: Object

```
"<field_name>": { 
  "value": "String" 
}
```

</td></tr><tr><td>

lineitems.characteristics.attributes.&lt;field\_name&gt;.value

</td><td id="l2c-returns-lineItems.attributes.name.field_name.value-returns">

Value of the attribute belonging to the characteristic record of an entity.Data type: String

</td></tr><tr><td>

lineItems.characteristics.sys\_id

</td><td>

Sys\_id object of the characteristic record.Data type: Object

```
"sys_id": { 
  "value": "String" 
}
```

</td></tr><tr><td>

lineItems.characteristics.sys\_id.value

</td><td id="l2c-returns-lineItems.-characteristics.sys_id.value-returns">

Sys\_id of the associated characteristic record. The updated table may vary between entities. For example, Order \[sn\_ind\_tmt\_orm\_order\].Data type: String

</td></tr><tr><td>

lineItems.characteristics.table

</td><td id="l2c-returns-lineItems.characteristics.table-returns">

Name of the table containing the characteristic record.Data type: String

</td></tr><tr><td>

lineItems.lineItems

</td><td id="l2c-returns-lineItems.lineitems-returns">

Child line items of a parent line item. This object has the same format as the **lineItems** parameter.Data type: Array of Objects

```
"lineItems": [  
 {  
  "_glide_action": "String",
  "attributes": {Object},
  "characteristics": [Array],
  "lineItems": [Array],
  "sys_id": {Object},
  "table": "String"
 } 
]
```

</td></tr><tr><td>

lineItems.sys\_id

</td><td id="l2c-returns-lineItems.sys_id-returns">

Sys\_id of the associated item record.Data type: Object

```
"sys_id": {
  "value": "String"
}
```

</td></tr><tr><td>

lineItems.sys\_id.value

</td><td id="l2c-returns-lineItems.sys_id.value-returns">

Sys\_id of an associated item record. The updated table may vary between entities, like Order or Specification. For example, Order \[sn\_ind\_tmt\_orm\_order\]. Data type: String

</td></tr><tr><td>

lineItems.table

</td><td id="l2c-returns-lineItems.table-returns">

Name of the table that contains the item record associated with the lead to cash entity. Data type: String

</td></tr></tbody>
</table>The following example demonstrates how to call the delta\(\) method by first calling the PrimitiveUtil utility method and getPrimitiesEPService\(\), and then providing the source and target JSON objects.

```
//Utility to invoke Delta API 
var util = new sn_l2c_core.PrimitiveUtil();  
 
//Invoke extension point, picks an implementation based on sourceToTargetConfigID of a L2C flow, the Mapping Config ID  in “sn_l2c_core_entity_mapping” table. 
var service = util.getPrimitivesEPService('sp_order_macd'); 
 
//Invoke delta API with required params 
// sourceJSON can be the output of createInstance or null 
//dirtyJSON is the modified sourceJSON 
var deltaOutput= service.delta(sourceJSON, dirtyJSON);  
 
//Print the returned JSON 
gs.info(" deltaOutput: "+JSON.stringify(deltaOutput));  
 
//The returned JSON can be used for subsequent APIs of the flow such as Effect and Commit Instance
```

The output JSON shows that several line items were added to the sold base product:

```
{ 
  "lineItems": [ 
    { 
      "table": "sn_install_base_sold_product", 
      "sys_id": { 
        "value": "-1" 
      }, 
      "attributes": { 
        "name": { 
          "value": "Quadplay Home Tech Hub Bundle" 
        }, 
        "account": { 
          "value": "9e2fd2ee11b43110f877366201dea674" 
        } 
      }, 
      "lineItems": [ 
        { 
          "table": "sn_install_base_sold_product", 
          "sys_id": { 
            "value": "-1" 
          }, 
          "attributes": { 
            "name": { 
              "value": "Internet and OTT Bundle" 
            }, 
            "account": { 
              "value": "9e2fd2ee11b43110f877366201dea674" 
            } 
          }, 
          "lineItems": [ 
            { 
              "table": "sn_install_base_sold_product", 
              "sys_id": { 
                "value": "-1" 
              }, 
              "attributes": { 
                "name": { 
                  "value": "Solana Sports streaming channel" 
                }, 
                "account": { 
                  "value": "9e2fd2ee11b43110f877366201dea674" 
                } 
              }, 
              "lineItems": [], 
              "characteristics": [], 
              "_action": "add" 
            } 
          ], 
          "characteristics": [], 
          "_action": "add" 
        } 
      ], 
      "characteristics": [ 
        { 
          "table": "sn_prd_pm_product_characteristics", 
          "sys_id": { 
            "value": "-1" 
          }, 
          "attributes": { 
            "characteristic_value": { 
              "value": "" 
            }, 
            "characteristic": { 
              "value": "4f31999fd0a63110f8770dbf976be178" 
            }, 
            "characteristic_option": { 
              "value": "4f31999fd0a63110f8770dbf976be179" 
            }, 
            "sold_product": { 
              "value": "4e03cda2ec873110f87727ef5883a2cf" 
            }, 
            "action": { 
              "value": "add" 
            } 
          }, 
          "_action": "add" 
        } 
      ], 
      "_action": "add" 
    } 
  ] 
} 
```

### Multi-select

The following example shows how to form the multi-select delta\(\) method by first calling PrimitiveUtil and getPrimitivesEPService and then providing the source and target JSON objects for multiple line or header IDs. Per each flow, get the service only once and use the same service for all the LeadtoCashCore methods.

```
/Utility to invoke Delta API  
var util = new sn_l2c_core.PrimitiveUtil();   

//Set context variable isMultiSelect true to enable multi-select 
var context = {"isMultiSelect": true}; 
 
//Invoke extension point, picks an implementation based on sourceToTargetConfigID of a L2C flow, the Mapping Config ID  in “sn_l2c_core_entity_mapping” table.  
var service = util.getPrimitivesEPService(‘sn_l2c_cust_flows_sp_to_order’, context);  
  
//Invoke delta API with required params  
// sourceJSON can be the output of createInstance for multiple lineIDs or headerIDs or null  
//dirtyJSON is the modified sourceJSON  
var deltaOutput= service.delta(sourceJSON, dirtyJSON);   
  
//Print the returned JSON  
gs.info(" deltaOutput: "+JSON.stringify(deltaOutput));   
  
//The returned JSON can be used for subsequent APIs of the flow such as Effect and Commit Instance
```

The output JSON shows that several line items were added to the sold base product:

```
{ 
  "items": [ 
    { 
      "lineItems": [ 
        { 
          "table": "sn_install_base_sold_product", 
          "sys_id": { 
            "value": "4e03cda2ec873110f87727ef5883a2cf" 
          }, 
          "attributes": { 
            "name": { 
              "value": "Quadplay Home Tech Hub Bundle" 
            }, 
            "account": { 
              "value": "9e2fd2ee11b43110f877366201dea674" 
            } 
          }, 
          "lineItems": [ 
            { 
              "table": "sn_install_base_sold_product", 
              "sys_id": { 
                "value": "9e0301e2ec873110f87727ef5883a23a" 
              }, 
              "attributes": { 
                "name": { 
                  "value": "Internet and OTT Bundle" 
                }, 
                "account": { 
                  "value": "9e2fd2ee11b43110f877366201dea674" 
                } 
              }, 
              "lineItems": [], 
              "characteristics": [], 
              "_action": "disconnect" 
            } 
          ], 
          "characteristics": [], 
          "_action": "disconnect" 
        } 
      ] 
    }, 
    { 
      "lineItems": [
        { 
          "table": "sn_install_base_sold_product", 
          "sys_id": { 
            "value": "036a2349284d0210f877b68370fb2e93" 
          }, 
          "attributes": { 
            "name": { 
              "value": "Quadplay Home Tech Hub Bundle" 
            }, 
            "account": { 
              "value": "9e2fd2ee11b43110f877366201dea674" 
            } 
          }, 
          "lineItems": [ 
            { 
              "table": "sn_install_base_sold_product", 
              "sys_id": { 
                "value": "4b6a2349284d0210f877b68370fb2e9c" 
              },
              "attributes": { 
                "name": { 
                  "value": "Internet and OTT Bundle" 
                }, 
                "account": { 
                  "value": "9e2fd2ee11b43110f877366201dea674" 
                } 
              }, 
              "lineItems": [], 
              "characteristics": [], 
              "_action": "disconnect" 
            } 
          ], 
          "characteristics": [], 
          "_action": "disconnect" 
        } 
      ] 
    } 
  ] 
}
```

## LeadtoCashCore - effect\(Object sourceJSON, Object targetJSON, Object additionalParams\)

Transforms and applies the source JSON structure of a given entity to the target JSON of another entity. You can then commit the changed entity to the database using the commitInstance\(\) method.

You can use the output JSON of the delta\(\) method in the effect\(\) request. Then, commit any effect\(\) JSON output to the database using the commitInstance\(\) to complete the lead to cash workflow.

**Note:** The LeadtoCashCore script include requires you to first call the scripted extension point PrimitiveUtil\(\) with the [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#) utility method to trigger the implementation before calling effect\(\) in your script. Per each flow, get the service only once and use the same service for all LeadtoCashCore methods.

<table id="table_sjw_1ym_d1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sourceJSON

</td><td>

Object

</td><td>

JSON containing details of the source entity.**Note:** Use the [LeadtoCashCore - createInstance\(String headerSysIDs, String lineSysIDs, Boolean isTarget, Object additionalParams\)](LeadToCashCoreAPI.md#) to retrieve the source JSON of an entity.

</td></tr><tr><td>

targetJSON

</td><td>

Object

</td><td>

JSON containing details of the target entity.

</td></tr><tr><td>

additionalParams

</td><td>

Object

</td><td>

Optional. Additional parameters to use.

</td></tr><tr><td>

additionalParams.is\_future\_state

</td><td>

Boolean

</td><td>

Optional. Use this to support reconfiguration  use cases. Accepted values:

-   true: Provides context variable keys instead of dictionary field names. This allows you to provide all the attributes from the target entity instead of mapping attributes from source to target.
-   false: Provides dictionary field names.

Default: false

</td></tr></tbody>
</table><table id="id_hfh_p13_h1c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON Object

</td><td>

Change that occurred and was applied from the source to target entity JSON objects at each of the header of the lead to cash entity.Data type: Object

```
{
  "_glide_action": "String",
  "_records_count: {Object},
  "_source_object": {Object},
  "lineItems": [Array],
  "sys_id": "String", 
  "table": "String"
}
```

</td></tr><tr><td>

\_glide\_action

</td><td>

Indicates the change that occurred at the item level between the source and target JSON.Possible values \(case-sensitive\):

-   DELETE: Information was removed between the source and target JSON structures.
-   INSERT: Information was added between the source and target JSON structures.
-   NO\_CHANGE: No change occurred between the source and target JSON structures.
-   UPDATE: Information was modified between the source and JSON structures.

Data type: String

</td></tr><tr><td>

\_records\_count

</td><td>

Details of new records inserted for each table.Data type: Object

```
"_records_count": {
"tableName": {Object}
}
```

</td></tr><tr><td>

\_records\_count.tableName

</td><td>

Name of the table in which new records are inserted.Data type: Object

```
"tableName": {
      "insert": Number}
}
```

</td></tr><tr><td>

\_records\_count.tableName.insert

</td><td>

Number of new records inserted in the table.Data type: Number

</td></tr><tr><td>

\_source\_object

</td><td>

Source JSON object to which changes were applied. The object structure may vary between entities.Data type: Object

```
"_source_object": { 
  "sys_id": "String",
  "table": "String" 
}
```

</td></tr><tr id="l2c-returns-lineItems._source_object.sys_id"><td>

\_source\_object.sys\_id

</td><td>

Sys\_id of the source entity record that was updated. Data type: String

</td></tr><tr id="l2c-returns-lineItems._source_object.table"><td>

\_source\_object.table

</td><td>

Table location of the source entity record that was updated. This value may vary between entities.Data type: String

</td></tr><tr><td>

lineItems.\_glide\_action

</td><td id="l2c-returns-lineItems._glide_action-entry">

Change action that occurred on the line item.Possible values:

-   DELETE: Information was removed between the source and target JSON structures.
-   INSERT: Information was added between the source and target JSON structures.
-   NO\_CHANGE: No change occurred between the source and target JSON structures.
-   UPDATE: Information was modified between the source and JSON structures.

Data type: String

</td></tr><tr><td>

lineItems.\_source\_object

</td><td id="l2c-returns-lineItems._source_object-entry">

Source entity record details to which the \_glide\_action was applied. This object may vary between entities.Data type: Object

```
"_source_object": { 
  "sys_id": "String",
  "table": "String" 
}
```

</td></tr><tr><td>

lineItems.\_source\_object.sys\_id

</td><td>

Sys\_id of the source entity record that was updated. Data type: String

</td></tr><tr><td>

lineItems.\_source\_object.table

</td><td>

Table location of the source entity record that was updated. This value may vary between entities.Data type: String

</td></tr><tr><td>

lineItems.\_state

</td><td id="l2c-returns-lineItems._state-entry">

State of the entity.Data type: Object

```
"_state": {  
 "value": "String" 
} 
```

</td></tr><tr><td>

lineItems.\_state.value

</td><td id="l2c-returns-lineItems._state.value-returns">

The current state of the entity.Possible values:

-   active: The entity object is in an active state.
-   inactive: The entity object isn't in an active state.

Data type: String

</td></tr><tr><td>

lineItems.attributes

</td><td id="l2c-returns-lineItems.attributes-returns">

Attributes of the line item. For example, the attribute's name and value. May contain varying fields based on the entity.Data type: Object

```
"attributes": { 
  "<attribute_name>": {Object}
}
```

</td></tr><tr><td>

lineitems.attributes.&lt;attribute\_name&gt;

</td><td id="l2c-returns-lineItems.attributes.attribute_name-returns">

Name of the line item attribute. For example, the name of an account or contact. May contain varying fields of the entity.Data type: Object

```
"attributes": { 
 "<attribute_name>": { 
   "value": "String"
 }
}
```

</td></tr><tr><td>

lineitems.attributes.&lt;attribute\_name&gt;.value

</td><td id="l2c-returns-lineItems.attributes.attribute_name.value-returns">

Value of the line item attribute. Data type: String

</td></tr><tr><td>

lineItems.attributes.account

</td><td id="l2c-returns-lineItems-attributes.account-returns">

Information about the account associated with the item attribute.Data type: Object

```
"account": { 
  "value": "String" 
}
```

</td></tr><tr><td>

lineItems.attributes.account.value

</td><td id="l2c-returns-lineItems.attributes.account.value-returns">

Sys\_id of the account associated with the line item attribute.Data type: String

</td></tr><tr><td>

lineItems.attributes.short\_description

</td><td>

Brief description of the line item attribute.Data type: String

</td></tr><tr><td>

lineItems.characteristics

</td><td id="l2c-returns-lineItems.characteristics-returns">

List of characteristics associated with the line item. Characteristics may vary between entities.Data type: Array of Objects

```
"characteristics": [  
 {
  "_glide_action: "String",
  "attributes": {Object},
  "sys_id": {Object},  
  "table": "String"
 }  
]
```

</td></tr><tr><td>

lineItems.characteristics.\_glide\_action

</td><td>

Change action that occurred on the line item.Possible values:

-   DELETE: Information was removed between the source and target JSON structures.
-   INSERT: Information was added between the source and target JSON structures.
-   NO\_CHANGE: No change occurred between the source and target JSON structures.
-   UPDATE: Information was modified between the source and JSON structures.

Data type: String

</td></tr><tr><td>

lineItems.characteristics.attributes

</td><td id="l2c-returns-lineItems.characteristics.attributes-entry">

One or more objects that contain information about attributes associated with the characteristic record.For example, this object could contain references to the attributes record's sys\_id, associated characteristic records, accounts or contacts, characteristic option records, or sold product information.

Data type: Object

```
"attributes": {
  "<attribute_type>": {Object}
}
```

</td></tr><tr><td>

lineItems.characteristics.attributes.&lt;attribute\_type&gt;

</td><td>

Type of attribute. This value can contain different values based on the records or functionality associated with the characteristic.Data type: Object

```
"<attribute_type>": {
  "value": "String"
}
```

</td></tr><tr><td>

lineItems.characteristics.attributes.&lt;attribute\_type&gt;.value

</td><td id="l2c-returns-lineItems.characteristics.attributes.attribute_type-returns">

Value of the line item attribute.Data type: String

</td></tr><tr><td>

lineitems.characteristics.attributes.&lt;field\_name&gt;

</td><td id="l2c-returns-lineItems.attributes.field_name-returns">

Attribute name of the characteristic record associated with the line item.Data type: Object

```
"<field_name>": { 
  "value": "String" 
}
```

</td></tr><tr><td>

lineitems.characteristics.attributes.&lt;field\_name&gt;.value

</td><td id="l2c-returns-lineItems.attributes.name.field_name.value-returns">

Value of the attribute belonging to the characteristic record of an entity.Data type: String

</td></tr><tr><td>

lineItems.characteristics.sys\_id

</td><td id="l2c-returns-lineItems-characteristics.sys_id-returns">

Sys\_id of the associated characteristic record.Data type: Object

```
"sys_id": { 
  "value": "String" 
 }
```

</td></tr><tr><td>

lineItems.characteristics.sys\_id.value

</td><td id="l2c-returns-lineItems.-characteristics.sys_id.value-returns">

Sys\_id of the associated characteristic record. The updated table may vary between entities. For example, Order \[sn\_ind\_tmt\_orm\_order\].Data type: String

</td></tr><tr><td>

lineItems.characteristics.table

</td><td id="l2c-returns-lineItems.characteristics.table-returns">

Name of the table containing the characteristic record.Data type: String

</td></tr><tr><td>

lineItems.lineItems

</td><td id="l2c-returns-lineItems.lineitems-returns">

Child line items of a parent line item. This object has the same format as the **lineItems** parameter.Data type: Array of Objects

```
"lineItems": [  
 {  
  "_glide_action": "String",
  "attributes": {Object},
  "characteristics": [Array],
  "lineItems": [Array],
  "sys_id": {Object},
  "table": "String"
 } 
]
```

</td></tr><tr><td>

lineItems.sys\_id

</td><td id="l2c-returns-lineItems.sys_id-returns">

Sys\_id of the associated item record.Data type: Object

```
"sys_id": {
  "value": "String"
}
```

</td></tr><tr><td>

lineItems.sys\_id.value

</td><td id="l2c-returns-lineItems.sys_id.value-returns">

Sys\_id of an associated item record. The updated table may vary between entities, like Order or Specification. For example, Order \[sn\_ind\_tmt\_orm\_order\]. Data type: String

</td></tr><tr><td>

lineItems.table

</td><td id="l2c-returns-lineItems.table-returns">

Name of the table that contains the item record associated with the lead to cash entity. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the entity.Data type: String

</td></tr><tr><td>

table

</td><td>

Name of the table in which the entity is found.Data type: String

</td></tr></tbody>
</table>The following example shows how to apply transformation logic using the output of the delta\(\) method:

**Note:** The same script is applicable for both single select and multi-select use cases, as just the source JSON format changes and the output remains the same for both. For multi-select use cases, a single header is created with all the line items added to the same header.

```
//Utility to invoke effect API 
var util = new sn_l2c_core.PrimitiveUtil();  
 
//Invoke extension point, picks an implementation based on sourceToTargetConfigID of a L2C flow, the Mapping Config ID  in “sn_l2c_core_entity_mapping” table. 
var service = util.getPrimitivesEPService('sp_order_macd'); 
 
//Invoke effect API with required params 
var effectOutput = service.effect(deltaOutput, null); 
 
//Print the returned JSON 
gs.info("effectOutput: " + JSON.stringify(effectOutput)); 
 
//The returned JSON can be used in the subsequent commitInstance() method.
```

Output:

```
{ 
  "sys_id": "-1", 
  "table": "sn_ind_tmt_orm_order", 
  "_glide_action": "INSERT", 
  "_source_object": {}, 
  "lineItems": [ 
    { 
      "sys_id": "-1", 
      "table": "sn_ind_tmt_orm_order_line_item", 
      "attributes": { 
        "account": { 
          "value": "9e2fd2ee11b43110f877366201dea674" 
        }, 
        "short_description": { 
          "value": "Quadplay Home Tech Hub Bundle" 
        } 
      }, 
      "_glide_action": "INSERT", 
      "_source_object": { 
        "sys_id": "-1", 
        "table": "sn_install_base_sold_product" 
      }, 
      "lineItems": [ 
        { 
          "sys_id": "-1", 
          "table": "sn_ind_tmt_orm_order_line_item", 
          "attributes": { 
            "account": { 
              "value": "9e2fd2ee11b43110f877366201dea674" 
            }, 
            "short_description": { 
              "value": "Internet and OTT Bundle" 
            } 
          }, 
          "_glide_action": "INSERT", 
          "_source_object": { 
            "sys_id": "-1", 
            "table": "sn_install_base_sold_product" 
          }, 
          "lineItems": [ 
            { 
              "sys_id": "-1", 
              "table": "sn_ind_tmt_orm_order_line_item", 
              "attributes": { 
                "account": { 
                  "value": "9e2fd2ee11b43110f877366201dea674" 
                }, 
                "short_description": { 
                  "value": "Solana Sports streaming channel" 
                } 
              }, 
              "_glide_action": "INSERT", 
              "_source_object": { 
                "sys_id": "-1", 
                "table": "sn_install_base_sold_product" 
              }, 
              "lineItems": [], 
              "characteristics": [] 
            } 
          ], 
          "characteristics": [] 
        } 
      ], 
      "characteristics": [ 
        { 
          "sys_id": "-1", 
          "table": "sn_ind_tmt_orm_order_characteristic_value", 
          "attributes": { 
            "characteristic_option": { 
              "value": "4f31999fd0a63110f8770dbf976be179" 
            }, 
            "characteristic": { 
              "value": "4f31999fd0a63110f8770dbf976be178" 
            }, 
            "characteristic_option_value": { 
              "value": "" 
            } 
          }, 
          "_glide_action": "INSERT", 
          "_source_object": { 
            "sys_id": "-1", 
            "table": "sn_prd_pm_product_characteristics" 
          } 
        } 
      ] 
    }, 
  "_state": {
      "value": "active"
}
   ],
  "_records_count":
    {
        "sn_ind_tmt_orm_order":
        {
            "insert": 1
        },
        "sn_ind_tmt_orm_order_line_item":
        {
            "insert": 3
        },
        "sn_ind_tmt_orm_order_characteristic_value":
        {
            "insert": 1
        }
    }
}
```

## LeadtoCashCore - commitInstance\(Object targetJSON, Object additionalParams\)

Commits the JSON of a given lead to cash entity to the instance, returns a status message with updated information, and updates the Lead to Cash Core Entity table as a result.

**Note:** The LeadtoCashCore script include requires you to first call the scripted extension point PrimitiveUtil\(\) with the [LeadtoCashCore - getPrimitivesEPService\(String sourceToTargetConfigID, Object context\)](LeadToCashCoreAPI.md#) utility method to trigger the implementation before calling commitInstance\(\) in your script. Per each flow, get the service only once and use the same service for all LeadtoCashCore methods.

<table id="table_lmb_zym_d1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

targetJSON

</td><td>

Object

</td><td>

JSON object containing the ‘glide\_action’ of a target entity to commit. You can pass the output of the [effect\(\)](LeadToCashCoreAPI.md#) method here. **Note:** ‘glide\_action’ identifies the change action that occurred between the source and target JSON of a lead to cash entity.

</td></tr><tr><td>

additionalParams

</td><td>

Object

</td><td>

Optional. Additional parameters to use.

</td></tr><tr><td>

additionalParams.useNumberGenerator

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to generate sys\_numbers in bulk. Valid values:

-   true: Generate the sys\_numbers in bulk to be utilized during the record insertion process. Reduces the need for additional queries to fetch numbers and decreases insertion time.
-   false: Generate the sys\_number individually at the time of insertion for each record.

Default: false

</td></tr></tbody>
</table><table id="table_mmb_zym_d1c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON Object

</td><td>

Details about the target entity record.Data type: Object

```
{
  "dataObject": {Object},
  "displayMessage": "String",
  "error": "String",
  "headerID": "String",
  "message": "String",
  "rootLineIDs": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

dataObject

</td><td>

JSON object that contains detailed data on the commit operations performed at each level.Data type: Object

```
"dataObject": {
  "_commitObjectInfo": {Object},
  "_glide_action": "String",
  "_source_object": {Object},
  "lineItems": [Array],
  "sys_id": "String",
  "table": "String"
}
```

</td></tr><tr><td>

dataObject.\_commitObjectInfo

</td><td>

Commit status and sys\_id if the line item change is an INSERT action.Data type: Object

```
"_commitObjectInfo": {
  "status": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

dataObject.\_commitObjectInfo.status

</td><td>

Status of the commit operation performed on the particular entity. Possible values:

-   success: The entity commit operation was successful.
-   failure: The entity commit operation wasn't successful.

Data type: String

</td></tr><tr><td>

dataObject.\_commitObjectInfo.sys\_id

</td><td>

Sys\_id of the inserted record. The method returns this parameter only if the **dataObject.\_glide\_action** is `INSERT`. The updated table may vary between entities. For example, Order \[sn\_ind\_tmt\_orm\_order\].Data type: String

</td></tr><tr><td>

dataObject.\_glide\_action

</td><td>

Change action that occurred on the line item. Possible values:

-   DELETE: Information was removed between the source and target JSON structures.
-   INSERT: Information was added between the source and target JSON structures.
-   NO\_CHANGE: No change occurred between the source and target JSON structures.
-   UPDATE: Information was modified between the source and target structures.

Data type: String

</td></tr><tr><td>

dataObject.\_source\_object

</td><td>

Source JSON object to which changes were applied. The object structure may vary between entities.Data type: Object

```
"_source_object": {
  "sys_id": "String", 
  "table": "String” 
}
```

</td></tr><tr><td>

dataObject.\_source\_object.sys\_id

</td><td>

Sys\_id of the source entity record to which the \_glide\_action was applied. The updated table may vary between entities. For example, Order \[sn\_ind\_tmt\_orm\_order\].Data type: String

</td></tr><tr><td>

dataObject.\_source\_object.table

</td><td>

Name of the table that contains the source entity record to which the \_glide\_action was applied. This may vary between entities.Data type: String

</td></tr><tr><td>

dataObject.lineItems

</td><td>

Line item details of the entity record. For example, order line items or quote line items.Data type: Array of Objects

```
"lineItems": [ 
{ 
  "_action": "String",
  "_commitObjectInfo": {Object},
  "_glide_action": "String",
  "_source_object": {Object},
  "_state": "String",
  "attributes": {Object},
  "characteristics": [Array],
  "lineItems": [Array],
  "sys_id": {Object},
  "table": "String",
}
]
```

</td></tr><tr><td>

dataObject.lineItems.\_action

</td><td>

Change action applied to the line item of the source JSON. Possible values:

-   add: Information was added to the source JSON.
-   change: Information was updated in the source JSON.
-   disconnect: Information was disconnected from the source JSON.
-   nochange: No change occurred on the source JSON.

Data type: String

</td></tr><tr><td>

dataObject.lineItems.\_commitObjectInfo

</td><td>

Returned if the line item change is an `INSERT` action. Contains the object’s commit status and sys\_id.Data type: Object

```
"_commitObjectInfo": { 
  "status": "String", 
  "sys_id": "String" 
}
```

</td></tr><tr><td>

dataObject.lineItems.\_commitObjectInfo.status

</td><td>

Status of the commit operation performed on the particular entity. Possible values:

-   success: The entity commit operation was successful.
-   failure: The entity commit operation wasn't successful.

Data type: String

</td></tr><tr><td>

dataObject.lineItems.\_commitObjectInfo.sys\_id

</td><td>

Sys\_id of the inserted record. The updated table may vary between entities. For example, Order \[sn\_ind\_tmt\_orm\_order\].Data type: String

</td></tr><tr><td>

dataObject.lineItems.\_glide\_action

</td><td>

Change action that occurred on the line item.Possible values:

-   DELETE: Information was removed between the source and target JSON structures.
-   INSERT: Information was added between the source and target JSON structures.
-   NO\_CHANGE: No change occurred between the source and target JSON structures.
-   UPDATE: Information was modified between the source and JSON structures.

Data type: String

</td></tr><tr><td>

dataObject.lineItems.\_source\_object

</td><td>

Source entity record details to which the \_glide\_action was applied. This object may vary between entities.Data type: Object

```
"_source_object": { 
  "sys_id": "String",
  "table": "String" 
}
```

</td></tr><tr><td>

dataObject.lineItems.\_source\_object.sys\_id

</td><td>

Sys\_id of the source entity record to which the \_glide\_action was applied. Data type: String

</td></tr><tr><td>

dataObject.lineItems.\_source\_object.table

</td><td>

Table name of the source entity record to which the \_glide\_action was applied.Data type: String

</td></tr><tr><td>

dataObject.lineItems.\_state

</td><td>

State of the object.Possible values:

-   active: The entity object is in an active state.
-   inactive: The entity object isn't in an active state.

Data type: String

</td></tr><tr><td>

dataObject.lineItems.attributes

</td><td>

Attributes of the line item. For example, the attribute's name and value. May contain varying fields based on the entity.Data type: Object

```
"attributes": { 
  "<attribute_name>": {Object}
}
```

</td></tr><tr><td>

dataObject.lineItems.attributes.&lt;attribute\_name&gt;

</td><td>

Name of the line item attribute. For example, the name of an account or contact. May contain varying fields of the entity.Data type: Object

```
"attributes": { 
 "<attribute_name>": { 
   "value": "String"
 }
}
```

</td></tr><tr><td>

dataObject.lineItems.attributes.&lt;attribute\_name&gt;.value

</td><td>

Value of the line item attribute. Data type: String

</td></tr><tr><td>

dataObject.lineItems.characteristics

</td><td>

List of characteristics associated with the line item. Characteristics may vary between entities.Data type: Array of Objects

```
"characteristics": [  
 {
  "_glide_action: "String",
  "attributes": {Object},
  "sys_id": {Object},  
  "table": "String"
 }  
]
```

</td></tr><tr><td>

dataObject.lineItems.characteristics.\_glide\_action

</td><td>

Change action that occurred on the line item.Possible values:

-   DELETE: Information was removed between the source and target JSON structures.
-   INSERT: Information was added between the source and target JSON structures.
-   NO\_CHANGE: No change occurred between the source and target JSON structures.
-   UPDATE: Information was modified between the source and JSON structures.

Data type: String

</td></tr><tr><td>

dataObject.lineItems.characteristics.attributes

</td><td>

One or more objects that contain information about attributes associated with the characteristic record.For example, this object could contain references to the attributes record's sys\_id, associated characteristic records, accounts or contacts, characteristic option records, or sold product information.

Data type: Object

```
"attributes": {
  "<attribute_type>": {Object}
}
```

</td></tr><tr><td>

dataObject.lineItems.characteristics.attributes.&lt;attribute\_type&gt;

</td><td>

Name of the characteristic attribute. May contain varying fields of the entity.Data type: Object

```
"<attributes_type>": { 
 "<attribute_name>": {Object}
}
```

</td></tr><tr><td>

dataObject.lineItems.characteristics.attributes.&lt;attribute\_type&gt;.&lt;attribute\_name&gt;

</td><td>

Name of the characteristic attribute.Data type: Object

```
"<attribute_name>": { 
 "value": "String"
}
```

</td></tr><tr><td>

dataObject.lineItems.characteristics.attributes.&lt;attribute\_type&gt;.&lt;attribute\_name&gt;.value

</td><td>

Value of the line item attribute.Data type: String

</td></tr><tr><td>

dataObject.lineItems\[0\].characteristics.sys\_id

</td><td>

Sys\_id of the associated characteristic record.Data type: Object

```
"sys_id": { 
  "value": "String" 
 }
```

</td></tr><tr><td>

dataObject.lineItems\[0\].characteristics.sys\_id.value

</td><td>

Sys\_id of the associated characteristic record. The updated table may vary between entities. For example, Order \[sn\_ind\_tmt\_orm\_order\].Data type: String

</td></tr><tr><td>

dataObject.lineItems\[0\].characteristics.table

</td><td>

Name of the table containing the characteristic record.Data type: String

</td></tr><tr><td>

dataObject.lineItems\[0\].lineItems

</td><td>

Child line items of a parent line item. This object has the same format as the **lineItems** parameter.Data type: Array of Objects

```
"lineItems": [  
 {  
  "_glide_action": "String",
  "attributes": {Object},
  "characteristics": [Array],
  "lineItems": [Array],
  "sys_id": {Object},
  "table": "String"
 } 
]
```

</td></tr><tr><td>

dataObject.lineItems\[0\].sys\_id

</td><td>

Sys\_id of the associated item record.Data type: Object

```
"sys_id": {
  "value": "String"
}
```

</td></tr><tr><td>

dataObject.lineItems\[0\].sys\_id.value

</td><td>

Sys\_id of an associated item record. The updated table may vary between entities, like Order or Specification. For example, Order \[sn\_ind\_tmt\_orm\_order\]. Data type: String

</td></tr><tr><td>

dataObject.lineItems\[0\].table

</td><td>

Name of the table that contains the item record associated with the lead to cash entity. Data type: String

</td></tr><tr><td>

dataObject.sys\_id

</td><td>

Sys\_id of the associated line item record. The updated table may vary between entities. For example, Order \[sn\_ind\_tmt\_orm\_order\]. Data type: String

</td></tr><tr><td>

dataObject.table

</td><td>

Name of the table that contains the record of the lead to cash entity.Data type: String

</td></tr><tr><td>

displayMessage

</td><td>

Message that is displayed to the user in the UI. The display message is identical to the **message** string value.Data type: String

</td></tr><tr><td>

error

</td><td>

Error message that describes the failure of the commitInstance method. If the request is successful, this parameter returns an empty string.Data type: String

</td></tr><tr><td>

headerID

</td><td>

Sys\_id of the target entity record created or updated by the commitInstance method. Stored in: The related table depending on the entity type, like sold product, order, etc.

Data type: String

</td></tr><tr><td>

message

</td><td>

Message describing the success, error, or partially\_success scenarios. This message is the same as the **displayMessage** string value and can be used by other application calls to the API.Data type: String

</td></tr><tr><td>

rootLineIDs

</td><td>

Comma-separated list of sys\_ids of the target entity records inserted, updated, or deleted by the commitInstance method. Stored in: The related table depending on the entity type, like sold product, order, etc.

Data type: Array of Strings

</td></tr><tr><td>

status

</td><td>

Status message confirming the success of the commit. Possible values:

-   success: The commit was successful.
-   failure: The root line or header glide operation failed. Retrigger the Lead to Cash Core API flow.
-   partial\_success: There were failures while processing the entire JSON. Refer to processing logs to troubleshoot specific errors.

Data type: String

</td></tr></tbody>
</table>The following example shows how to use each LeadtoCashCore method to retrieve, apply, and commit the details of a source-to-target entity. In this example, the commitInstance\(\) method is used to commit the changed JSON to a lead to cash entity on the instance.

```
//Utility to invoke commitInstance API 
var util = new sn_l2c_core.PrimitiveUtil();  
 
//Invokes the PrimitiveUtil extension point, picks an implementation based on sourceToTargetConfigID of a Lead to Cash (L2C) flow. The Mapping Config ID  in “sn_l2c_core_entity_mapping” table. 
var service = util.getPrimitivesEPService('sp_order_macd'); 
 
//Invoke commitInstance API with the required params 
var commitOutput = service.commitInstance(effectOutput); 
 
//Print the returned JSON 
gs.info("commitOutput: "+JSON.stringify(commitOutput));  

```

Output:

```
{
  "status": "success",
  "error": "",
  "message": "Commit operation successfully processed.",
  "displayMessage": "Commit operation successfully processed.",
  "dataObject": {
    "sys_id": "-1",
    "table": "sn_ind_tmt_orm_order",
    "_glide_action": "INSERT",
    "_source_object": {},
    "lineItems": [
      {
        "sys_id": "-1",
        "table": "sn_ind_tmt_orm_order_line_item",
        "attributes": {
          "account": {
            "value": "86837a386f0331003b3c498f5d3ee4ca"
          },
          "sold_product": {
            "value": "e4bbf902b7343300ece839a6ee11a937"
          },
          "short_description": {
            "value": "Network Monitoring"
          }
        },
        "_glide_action": "INSERT",
        "_source_object": {
          "sys_id": "e4bbf902b7343300ece839a6ee11a937",
          "table": "sn_install_base_sold_product"
        },
        "lineItems": [
          {
            "sys_id": "-1",
            "table": "sn_ind_tmt_orm_order_line_item",
            "attributes": {
              "account": {
                "value": "86837a386f0331003b3c498f5d3ee4ca"
              },
              "sold_product": {
                "value": "23dbbd02b7343300ece839a6ee11a98e"
              },
              "short_description": {
                "value": "Remote Monitoring"
              }
            },
            "_glide_action": "INSERT",
            "_source_object": {
              "sys_id": "23dbbd02b7343300ece839a6ee11a98e",
              "table": "sn_install_base_sold_product"
            },
            "lineItems": [],
            "characteristics": [],
            "coveredProducts": [],
            "_commitObjectInfo": {
              "sys_id": "d2d5b868488d5610f877a23d5db8922f",
              "status": "success"
            }
          }
        ],
        "characteristics": [],
        "coveredProducts": [],
        "_commitObjectInfo": {
          "sys_id": "92d5b868488d5610f877a23d5db89229",
          "status": "success"
        }
      }
    ],
    "_commitObjectInfo": {
      "sys_id": "46d5b0a4488d5610f877a23d5db892ef",
      "status": "success"
    }
  },
  "headerID": "46d5b0a4488d5610f877a23d5db892ef",
  "rootLineIDs": [
    "92d5b868488d5610f877a23d5db89229"
  ]
}
```

