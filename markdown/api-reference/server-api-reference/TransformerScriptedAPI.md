---
title: Transformer - Scoped, Global
description: The Transformer API provides methods to parse and transform structured JSON or XML source content into structured key-value pair output, using a defined set of rules.Instantiates a Transformer object \(constructor\).Returns the row resulting from the last transformation \(or null if no row exists\).Transforms the next available row/node in the source document.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Transformer - Scoped, Global

The Transformer API provides methods to parse and transform structured JSON or XML source content into structured key-value pair output, using a defined set of rules.

This API works along with the TransformerDefinition and TransformerRuleList APIs. Together, these APIs transform XML nodes or any entity in a structured JSON document into an output of name-value pairs. Supported JSON entities including objects and elements within an array, such as strings, numbers, and other arrays.

-   The TransformerRuleList API enables you to create transformation rule lists that define what data in the source document to include in the output and how to transform the source data.

-   The TransformerDefinition API associates a transformation rule list with a JSON/XML record path to define reusable transform definition objects. You can use a transform definition object to transform one or more source documents.

-   The Transformer API performs the actual data transformation, one data entity at a time, using the specified transformation rule list to create the desired output data.


You can use the Transformer class in both scoped and global server scripts. When using this class, use the `sn_tfrm` namespace identifier. Before this API is available in an instance, you must activate the Transformation Service plugin \(com.glide.transform\).

The following example illustrates how to use the TransformerRuleList API to define the transformation rules, the TransformerDefinition API to define the transformation criteria, and the Transformer API to actually perform the transformation.

This code example retrieves an external JSON-based stock details document, creates rules for transforming that data into a tabular table, and then transforms the source document, one row at a time. The following is a snippet of the JSON source document being transformed:

```
{
  "NOW": {
    "quote": {
      "symbol": "NOW",
      "companyName": "ServiceNow Inc.",
      "primaryExchange": "New York Stock Exchange",
      "sector": "Technology",
      "open": 166.78,
      "openTime": 1522935000556,
      "close": 165.77,
      "changePercent": 0.00656,
       ...
     },
 ...}
```

```
var stockAPI = new sn_ws.RESTMessageV2('Stock Details', 'Default GET'); 
var response = stockAPI.execute(); 
var responseBody = response.getBody(); // obtain the source JSON document

/* Define the list of rules to use to transform the acquired JSON stock detail 
information into a tabular table */

var transformerRuleList = new sn_tfrm.TransformerRuleList() // instantiate the rule list object
  .fromJSON() // indicate that the source document is JSON
  .addRule('ticker', '$.quote.symbol') // add a rule to copy the value in the "symbol" field of the source document to the ticker field in the output document (no changes)
  .addRule('change_percentage', '$.quote.changePercent') // copy the "changePercent" field from source into the change_percentage field of output document
  .thenMultiply('100') // multiply the change_percentage value by 100
  .thenRoundDown('0') // addthen round it down to a whole number 
  .addRule('close_price', '$.quote.close') // copy the "close" field to the close_price field in the 21=-[';output
  .thenAdaptCurrency('USD', false) // attach the US dollar code to the close_price field, but do not display the symbol
  .addRule('summary') // add a blank "summary" field to the output (no corresponding source field)
  .thenConcat('Shares of ') // in the summary field concatenate the string "Shares of "
  .thenConcatSymbol('ticker') // then concatenate the "ticker" field from the source document
  .thenConcat(' closed at ') // then concatenate the string " closed at "
  .thenConcatSymbol('close_price'); // then concatenate the "close_price" field from the source document

// Create a transformer definition that associates the rule list to use and the record path of the set of records in the source document to transform.  
var path = '$.*'; 
var transformerDefinition = new sn_tfrm.TransformerDefinition(transformerRuleList, path);
 
// Instantiate the transformer object.
var transformer = new sn_tfrm.Transformer(transformerDefinition, responseBody); 

// Transform the source data, one row at a time, until all rows are processed.
var results = []; 
while (transformer.transform()) { 
  results.push(transformer.getRow());
} 
```

Output:

```
 {ticker: "Now", change_percentage: "0", close_price: "165.77 USD", summary: "Shares of Now closed at 165.77" }
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Transformer - Transformer\(Object transformerDefinition, String document\)

Instantiates a Transformer object \(constructor\).

<table id="table_uq2_glh_phb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

transformerDefinition

</td><td>

Object

</td><td>

Object that describes the content transformation; includes rule list and JSONPath/XPath record path. Use the TransformerRuleList\(\) and TransformerDefinition\(\) APIs to generate this object.

</td></tr><tr><td>

document

</td><td>

String

</td><td>

Source document to translate.

</td></tr></tbody>
</table>```
var stockAPI = new sn_ws.RESTMessageV2('Stock Details', 'Default GET'); 
var response = stockAPI.execute(); 
var responseBody = response.getBody(); 

var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .addRule('ticker', 'quote.symbol') 
  .addRule('change_percentage', 'quote.change') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', 'quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('summary') 
  .thenConcat('Shares of ') 
  .thenConcatSymbol('ticker') 
  .thenConcat(' closed at ') 
  .thenConcatSymbol('close') 

 
var path = '$.*'; 
var transformerDefinition = new sn_tfrm.TransformerDefinition(transformerRuleList, path); 
var transformer = new sn_tfrm.Transformer(transformerDefinition, responseBody); 

var results = []; 
while (transformer.transform()) { 
  results.push(transformer.getRow());
}
```

## Transformer - getRow\(\)

Returns the row resulting from the last transformation \(or null if no row exists\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object containing one transformed row/node of data.|

```
var results = []; 
while (transformer.transform()) { 
  results.push(transformer.getRow());

```

Output:

```
 {ticker: "Now", change_percentage: "0", close_price: "165.77 USD", summary: "Shares of Now closed at 165.77" }
```

## Transformer - transform\(\)

Transforms the next available row/node in the source document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ljw_tph_phb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there is a valid next row to transform.-   true: Valid next row
-   false: No additional rows

</td></tr></tbody>
</table>```
var results = []; 
while (transformer.transform()) { 
  results.push(transformer.getRow());

```

Output:

```
 {ticker: "Now", change_percentage: "0", close_price: "165.77 USD", summary: "Shares of Now closed at 165.77" }
```

