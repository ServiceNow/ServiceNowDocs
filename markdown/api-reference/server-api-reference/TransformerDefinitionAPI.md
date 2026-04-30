---
title: TransformerDefinition - Scoped, Global
description: The TransformerDefinition API provides methods to instantiate and manage the TransformerDefinition object, which associates a transformation rules list and a record path.Instantiates a TransformerDefinition object.Instantiates a TransformerDefinition object using an existing transformer definition.If set when the TransformerDefinition object was instantiated, returns the record path for the source data file associated with the TransformerDefinition object.Validates whether a valid TransformerRuleList is associated with the TransformerDefintion object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TransformerDefinition - Scoped, Global

The TransformerDefinition API provides methods to instantiate and manage the TransformerDefinition object, which associates a transformation rules list and a record path.

This API works along with the Transformer and TransformerRuleList APIs. Together, these APIs transform XML nodes or any entity in a structured JSON document into an output of name-value pairs. Supported JSON entities including objects and elements within an array, such as strings, numbers, and other arrays.

-   The TransformerRuleList API enables you to create transformation rule lists that define what data in the source document to include in the output and how to transform the source data.

-   The TransformerDefinition API associates a transformation rule list with a JSON/XML record path to define reusable transform definition objects. You can use a transform definition object to transform one or more source documents.


In addition, this object provides methods that enable you to obtain the record path of the TransformerDefinition object. It can also validate whether the definition has a valid TransformerRuleList associated with it.

The Transformer API performs the actual data transformation, one data entity at a time, using the specified transformation rule list to create the desired output data.

You can use the TransformerDefinition class in both scoped and global server scripts. When using this class, use the `sn_tfrm` namespace identifier. Also, before this API is available in an instance, you must activate the Transformation Service plugin \(com.glide.transform\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TransformerDefinition - TransformerDefinition\(Object transformerRuleList, String recordPath\)

Instantiates a TransformerDefinition object.

<table id="table_sf4_rby_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

transformerRuleList

</td><td>

Object

</td><td>

TransformerRuleList to associate with this transformer definition.

</td></tr><tr><td>

recordPath

</td><td>

String

</td><td>

Optional. The path \(JSONPath for JSON, XPath for XML\) that identifies the container \(parent\) of nodes to parse as records in the source document.

 For JSON documents, these nodes can be any object, array, or JSON primitive \(string, number, boolean\). For XML documents, these nodes are the child elements of the container.

 If **recordPath** is unspecified, the entire document is inferred as a single record. For JSON documents, if the top node is an array and **recordPath** is unspecified, then the top array is the record's container, and each of its entries is a record.

</td></tr></tbody>
</table>```
var stockAPI = new sn_ws.RESTMessageV2('Stock Details', 'Default GET'); 
var response = stockAPI.execute(); 
var responseBody = response.getBody(); 

var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .addSymbol('ticker', 'quote.symbol') 
  .addSymbol('change_percentage', 'quote.change_change') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addSymbol('close_price', 'quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addSymbol('summary') 
  .thenConcat('Shares of ') 
  .thenConcatSymbol('ticker') 
  .thenConcat(' closed at ') 
  .thenConcatSymbol('close'); 

 
var path = '$.*'; // Transform all objects in the JSON document
var transformerDefinition = new sn_tfrm.TransformerDefinition(transformerRuleList, recordPath); 
var transformer = new sn_tfrm.Transformer(transformerDefinition, responseBody); 

var results = []; 
while (transformer.transform()) { 
  results.push(transformer.getRow());
}
```

## TransformerDefinition - TransformerDefinition\(String transformerDefinitionSysId\)

Instantiates a TransformerDefinition object using an existing transformer definition.

<table id="table_cfj_yr5_qxb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

transformerDefinitionSysId

</td><td>

String

</td><td>

Sys\_id of a transformer definition. Table: Record Transformer \[sys\_record\_transformer\]

</td></tr></tbody>
</table>This example instantiates a TransformerDefinition object based on the provided sys\_id.

```
var transformerDefinition = new sn_tfrm.TransformerDefinition("7208b59743542110d4dc2c78c9b8f2e2");
```

## TransformerDefinition - recordPath\(\)

If set when the TransformerDefinition object was instantiated, returns the record path for the source data file associated with the TransformerDefinition object.

A record path \(JSONPath for JSON, XPath for XML\) identifies the container \(parent\) of nodes to parse as records in the source document.

For JSON documents, these nodes can be any object, array, or JSON primitive \(string, number, boolean\). For XML documents, these nodes are the child elements of the container.

If **recordPath** is unspecified, the entire document is inferred as a single record. For JSON documents, if the top node is an array and **recordPath** is unspecified, then the top array is the record's container, and each of its entries is a record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|If set, the record path associated with the transformer definition. If not set, returns null.|

```
var path = '$.records'; 
var transformerDefinition = new sn_tfrm.TransformerDefinition(transformerRuleList, recordPath); 
var transformer = new sn_tfrm.Transformer(transformerDefinition, responseBody);  
.
.
.

var recordPath = transformerDefinition.recordfPath();

var results = []; 
while (transformer.transform()) { 
  results.push(transformer.getRow());
}
```

## TransformerDefinition - validate\(\)

Validates whether a valid TransformerRuleList is associated with the TransformerDefintion object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_klv_hgy_qhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether a valid TransformerRuleList is associated with the specified TransformerDefintion object.Valid values:

 -   true: Valid TransformerRuleList associated
-   false: Invalid or no TransformerRulList associated

</td></tr></tbody>
</table>```
var transformerDefinition = new sn_tfrm.TransformerDefinition(transformerRuleList, recordPath);
var transformer = new sn_tfrm.Transformer(transformerDefinition, responseBody); 
.
.
.

if (transformerDefinition.validate()) {

  var results = []; 
  while (transformer.transform()) { 
    results.push(transformer.getRow());
  }
}
```

