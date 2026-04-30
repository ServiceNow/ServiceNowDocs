---
title: TransformerRuleList - Scoped, Global
description: The TransformerRuleList API enables you to create a list of rules for transforming various types of JSON and XML data into name-value pair output.Creates an entry in the associated transformation rules list which defines a field to create in the output.Defines a name for the associated TransformerRuleList object for logging purposes.Adds an adapter to the current rule that ties the specified currency code to the output field defined in the associated addRule\(\) call.Adds an adapter to the current rule that converts the source field from one unit of measure to another, such as from minutes to seconds or weeks to days.Adds an adapter to the current rule that adds the passed in value to the source field.Adds an adapter to the current rule that searches the associated source field for a list of strings and replaces them in the output with the specified replacement values.Adds an adapter to the current rule that matches a specified regex pattern to content in the source field and then replaces/reformats that content with a second regex pattern and stores that value in the output.Adds an action to the current rule to round the source field up at the decimal position specified by the passed in value.Adds an adapter to the current rule that concatenates the passed in string to the output field.Adds an adapter to the current rule that concatenates the value of a field previously defined in the rules list to the current output field.Adds an adapter to the current rule that divides the source field by the passed in value.Adds an adapter to the current rule that divides the passed in value by the source field.Adds an adapter to the current rule that rounds the source field down at the decimal position specified by the passed in value and stores it in the output.Adds an adapter to the current rule that reformats the content in the source field that matches the specified match pattern, with the specified output pattern.Adds an adapter to the current rule that compares the passed in value against the source field and copies the greater of the two values to the output field.Adds an adapter to the current rule that compares the passed in value against the source field and copies the lower of the two values to the output field.Adds an adapter to the current rule that multiplies the source field by the passed in value.Adds an adapter to the current rule that finds all text within the source field that matches a specified string and replaces it with an updated string.Adds an adapter to the current rule that rounds the source field down at the decimal position specified by the passed in value.Adds an adapter to the current rule that rounds the source data element up at the decimal position specified by the passed in value.Adds an adapter to the current rule that splits, reorganizes, and replaces strings within the source field and saves them in the output field.Adds an adapter to the current rule that subtracts the passed in value from the source field and stores it in the output field.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 20
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TransformerRuleList - Scoped, Global

The TransformerRuleList API enables you to create a list of rules for transforming various types of JSON and XML data into name-value pair output.

This API works along with the Transformer and TransformerDefinition APIs. Together, these APIs transform XML nodes or any entity in a structured JSON document into an output of name-value pairs. Supported JSON entities including objects and elements within an array, such as strings, numbers, and other arrays.

-   The TransformerRuleList API enables you to create transformation rule lists that define what data in the source document to include in the output and how to transform the source data.

-   The TransformerDefinition API associates a transformation rule list with a JSON/XML record path to define reusable transform definition objects. You can use a transform definition object to transform one or more source documents.

-   The Transformer API performs the actual data transformation, one data entity at a time, using the specified transformation rule list to create the desired output data.


When you instantiate the TransformRuleList object, you must define whether it describes a JSON or XML source document using the .fromJSON\(\) or .fromXML\(\) methods. For example:

`var trl = sn_tfrm.TransformerRuleList().fromJSON();` or `var trl = sn_tfrm.TransformerRuleList().fromXML();`

Then use the addRule\(\) method to define a transformation rule for each element in the source document that you want to include as a name-value pair in the output.

Use "adapter methods", such as setName\(\) or thenAdd\(\), to define how to manipulate data elements when the transformation is performed. Adapter methods work along with the addRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns. You can apply one or more adapter methods to each data transformation. Adapter methods enable you to do things such as:

-   Concatenate text.
-   Perform mathematical functions, such as add, subtract, divide, and multiply.
-   Round values up or down \(round up/down, ceiling/floor\).
-   Define whether to use the minimum or maximum value when comparing a source data element to a specified value.
-   Apply a currency code.
-   Convert between different units of measure.
-   Format data elements.
-   Apply patterns.
-   Replace specified data elements with a specified value.
-   Split and rearrange strings.

You can use the TransformerRuleList class in both scoped and global server scripts. When using this class in a scoped application, use the `sn_tfrm` namespace identifier. Also, before this API is available in an instance, you must activate the Transformation Service plugin \(com.glide.transform\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TransformerRuleList - addRule\(String rule, String path\)

Creates an entry in the associated transformation rules list which defines a field to create in the output.

You can create rules for any element in a source document. For example, `.addRule('ticker', '$.quote.symbol')` creates the field "ticker" in the output and copies over the value in quote.symbol of the source.

Once you define a rule using addRule\(\), you then use adaptor methods, such as thenAdd\(\), thenReplace\(\), and thenFloor\(\) to manipulate the rule's output data. You can define as many adaptor methods as needed for a single rule. All adapter methods directly after an addRule\(\) call, until the next addRule\(\) call, apply to that rule. Adapter methods are cumulative with the result of all adapter methods being the final value saved in the output field.

For example, in the following code snippet, thenMultiply\(\) and thenRoundDown\(\) apply to addRule\('change\_percentage', '$.quote.changePercent'\); addRule\('close\_price', '$.quote.close'\) starts a new rule. If the value in **$.quote.changePercent** is .011, then the final output value is "1" \( .011 \* 100 rounded down to the ones position\).

```

  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
```

The addRule\(\) method also supports the parameter **summary**; `.addRule('summary')`. This implementation creates the name field "summary:" in the output, but does not correlate it to any field in the source. You can then use the adaptor methods thenConcat\(\) and thenConcatSymbol\(\) to modify the contents of the summary field.

<table id="table_hwn_wrb_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

rule

</td><td>

String

</td><td>

Name of the element in the destination output.

</td></tr><tr><td>

path

</td><td>

String

</td><td>

Optional. JSONPath or XPath to the data element in the source document.The adapter methods thenConcat\(\) and thenConcatSymbol\(\) do not require you to define this parameter if no other adapter methods are defined for the rule. All other adapter methods require this parameter.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('summary') 
  .thenConcat('Shares of ') 
  .thenConcatSymbol('ticker') 
  .thenConcat(' closed at ') 
  .thenConcatSymbol('close_price'); 

```

## TransformerRuleList - setName\(String name\)

Defines a name for the associated TransformerRuleList object for logging purposes.

<table id="table_z2l_5hw_phb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name to use to identify the associated TransformerRuleList object. Although the API does not force this name to be unique, it is helpful if they are unique within an instance.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('summary') 
  .thenConcat('Shares of ') 
  .thenConcatSymbol('ticker') 
  .thenConcat(' closed at ') 
  .thenConcatSymbol('close_price'); 

```

## TransformerRuleList - thenAdaptCurrency\(String currencyCode, Boolean outputNumericCurrencyValue\)

Adds an adapter to the current rule that ties the specified currency code to the output field defined in the associated addRule\(\) call.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_akh_43w_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

currencyCode

</td><td>

String

</td><td>

Currency code to tie to the destination data element, such as USD, EUR, and GBP.

</td></tr><tr><td>

outputNumericCurrencyValue

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to display the currency code.Valid values:

 -   true: do not display the country code; numeric value only
-   false: display the country code

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('summary') 
  .thenConcat('Shares of ') 
  .thenConcatSymbol('ticker') 
  .thenConcat(' closed at ') 
  .thenConcatSymbol('close_price'); 

```

## TransformerRuleList - thenAdaptDuration\(String inputDuration, String outputDuration\)

Adds an adapter to the current rule that converts the source field from one unit of measure to another, such as from minutes to seconds or weeks to days.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_x4x_1nw_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inputDuration

</td><td>

String

</td><td>

Current unit of measure of the source field.Valid values:

 -   NANOSECOND
-   MICROSECOND
-   MILLISECOND
-   SECOND
-   MINUTE
-   HOUR
-   DAY
-   WEEK

</td></tr><tr><td>

outputDuration

</td><td>

String

</td><td>

Unit of measure to convert the source field to in the output.Valid values:

 -   NANOSECOND
-   MICROSECOND
-   MILLISECOND
-   SECOND
-   MINUTE
-   HOUR
-   DAY
-   WEEK

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('daily', '$.quote.weekly') 
  .thenAdaptDuration('WEEK', 'DAY'); 

```

## TransformerRuleList - thenAdd\(Number operand\)

Adds an adapter to the current rule that adds the passed in value to the source field.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|operand|Number|Value to add to the source field.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList.fromJSON()
  .setName('Stock Report 05182019 JSON')
  .addSymbol('ticker', '$.symbol') 
  .addSymbol('change_percentage', '$.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addSymbol('trade_price', '$.current_price')
  .thenAdaptCurrency('USD', false) 
  .addMultiply('$.trade_quantity')
  .thenAdd('4.5'); 

```

## TransformerRuleList - thenApplyMap\(Object map\)

Adds an adapter to the current rule that searches the associated source field for a list of strings and replaces them in the output with the specified replacement values.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_azh_c3x_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

map

</td><td>

Object

</td><td>

Name/value pairs.-   name: text to locate in the source data element
-   value: text to replace it with in the output

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

In this example, the thenApplyMap\(\) call searches the source text in the company\_info field for Inc. and St. and replaces them with Incorporated and Street in the company\_info field in the output.

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('company_info', '$.quote.company_info') 
  .thenApplyMap({'Inc.': 'Incorporated', 'St.': 'Street'});

```

## TransformerRuleList - thenApplyPattern\(String matchPattern, String outputPattern

Adds an adapter to the current rule that matches a specified regex pattern to content in the source field and then replaces/reformats that content with a second regex pattern and stores that value in the output.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|matchPattern|String|Regex pattern to use to locate the text to replace/reformat.|
|outputPattern|String|Regex pattern to use to update the located text.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

In this example, any company name that ends with "Inc." is transformed to "Incorporated", such as Company Inc. to Company Incorporated.

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('company', '$.quote.company') 
  .thenApplyPattern('(.+)(\\w{3}\\.)', '$1Incorporated');

```

## TransformerRuleList - thenCeiling\(Number operand\)

Adds an action to the current rule to round the source field up at the decimal position specified by the passed in value.

Unlike straight rounding where the number is rounded based on the value of the digit in the specified decimal position \(0-4 round down, 5-9 round up\), ceiling always rounds up. For example, the ceiling value for 2.156 and 2.152 is always 2.16 for the passed in decimal position of 2; whereas for straight rounding the values would be 2.16 and 2.15 respectively. For negative numbers, the ceiling operation makes the number more positive, as in the ceiling value of -2.156 is -2.15; whereas the same number rounded up makes the value more negative, -2.16.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_jfb_5fd_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operand

</td><td>

Number

</td><td>

Decimal position to the right of the decimal point at which to round the number up \(apply ceiling\). For example, if this value is 2 and the source data element is 6.421, the resulting value is 6.43.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Mortgage Rates 05022019 JSON')
  .addRule('interest_rate', '$.quote.interest_rate') 
  .thenCeiling('2') // Always round the interest rate up to the hundredths place 
  .addRule('monthly_payment', '$.quote.total_loan_amount') 
  .thenDivideBy('180'); 

```

## TransformerRuleList - thenConcat\(String value\)

Adds an adapter to the current rule that concatenates the passed in string to the output field.

Unlike other adapter methods, this method does not have to be applied to a source field. You can use this method to create completely new data strings in the output.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|value|String|Text to concatenate to the end of the current data element.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('summary') 
  .thenConcat('Shares of ') 
  .thenConcatSymbol('ticker') 
  .thenConcat(' closed at ') 
  .thenConcatSymbol('close_price'); 

```

## TransformerRuleList - thenConcatSymbol\(String symbol\)

Adds an adapter to the current rule that concatenates the value of a field previously defined in the rules list to the current output field.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|symbol|String|Name of the rules list element to append to the output field.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('summary') 
  .thenConcat('Shares of ') 
  .thenConcatSymbol('ticker') 
  .thenConcat(' closed at ') 
  .thenConcatSymbol('close_price'); 

```

## TransformerRuleList - thenDivideBy\(Number operand\)

Adds an adapter to the current rule that divides the source field by the passed in value.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|operand|Number|Value by which to divide the source field.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('dividend_per_share', '$.quote.total_dividend') 
  .thenDivideBy('$.quote.total_shares'); 

```

## TransformerRuleList - thenDivideInto\(Number operand\)

Adds an adapter to the current rule that divides the passed in value by the source field.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|operand|Number|Value into which to divide the source field.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('dividend_per_share', '$.quote.total_shares') 
  .thenDivideInto('$.quote.total_dividends'); 

```

## TransformerRuleList - thenFloor\(Number operand\)

Adds an adapter to the current rule that rounds the source field down at the decimal position specified by the passed in value and stores it in the output.

Unlike straight rounding where the number is rounded based on the value of the digit in the specified decimal position \(0-4 round down, 5-9 round up\), floor always rounds down. For example, the floor value for 2.156 and 2.152 is always 2.15 for the passed in decimal position of 2; whereas for straight rounding the values would be 2.16 and 2.15 respectively. For negative numbers, the floor operation makes the number more negative, as in the floor value of -2.156 is -2.16; whereas the same number rounded down makes the value more positive, -2.15.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_zpl_tzc_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operand

</td><td>

Number

</td><td>

Decimal position to the right of the decimal point at which to round the number down \(apply floor\). For example, if this value is 2 and the source data element is 6.427, the resulting value is 6.42.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Mortgage Rates 05022019 JSON')
  .addRule('interest_rate', '$.quote.interest_rate') 
  .thenFloor('2') // Always round the interest rate down to the hundreths place 
  .addRule('monthly_payment', '$.quote.total_loan_amount') 
  .thenDivideBy('180'); 

```

## TransformerRuleList - thenFormat\(String matchPattern, String outputPattern\)

Adds an adapter to the current rule that reformats the content in the source field that matches the specified match pattern, with the specified output pattern.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_uv3_qsw_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

matchPattern

</td><td>

String

</td><td>

Pattern to match against the source field.Valid values:

 -   @: any character
-   \#: decimal digit
-   \\: literal escape \(\\@ for the @ symbol\)

</td></tr><tr><td>

outputPattern

</td><td>

String

</td><td>

Pattern to replace the content with in the output.Valid values:

 -   @: any character
-   \#: decimal digit
-   \\: literal escape \(\\@ for the @ symbol\)

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

This example reformats the quote date from YYYY/MM/DD to YYYY MM-DD.

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('date', '$.quote.date') 
  .thenFormat('####/##/##', '#### ##-##'); 

```

## TransformerRuleList - thenMax\(Number operand\)

Adds an adapter to the current rule that compares the passed in value against the source field and copies the greater of the two values to the output field.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|operand|Number|Value to compare to the source field.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Mortgage Rates 05022019 JSON')
  .addRule('lowest_interest_rate', '$.quote.interest_rate') 
  .thenMax('3.5') // Interest rate cannot be less than 3.5%
  .addRule('dividend_per_share', '$.quote.total_shares') 
  .thenDivideInto('$.quote.total_dividends'); 

```

## TransformerRuleList - thenMin\(Number operand\)

Adds an adapter to the current rule that compares the passed in value against the source field and copies the lower of the two values to the output field.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|operand|Number|Value to compare to the source field.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addSymbol('broker_fee_percentage', '$.quote.broker_fee') 
  .thenMin('10') // Maximum of 10% broker fee
  .addSymbol('dividend_per_share', '$.quote.total_shares') 
  .thenDivideInto('$.quote.total_dividends'); 

```

## TransformerRuleList - thenMultiply\(Number operand\)

Adds an adapter to the current rule that multiplies the source field by the passed in value.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|operand|Number|Value by which to multiply the source field.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('summary') 
  .thenConcat('Shares of ') 
  .thenConcatSymbol('ticker') 
  .thenConcat(' closed at ') 
  .thenConcatSymbol('close_price'); 

```

## TransformerRuleList - thenReplace\(String matchString, String replaceString\)

Adds an adapter to the current rule that finds all text within the source field that matches a specified string and replaces it with an updated string.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|matchString|String|String to match against the source field to identify the text to replace.|
|replaceString|String|String with which to replace the matching text.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

In this example, any company name that ends with "Inc." is transformed to "Incorporated", such as Company Inc. to Company Incorporated.

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('company', '$.quote.company') 
  .thenReplace('Inc.', 'Incorporated');

```

## TransformerRuleList - thenRoundDown\(Number operand\)

Adds an adapter to the current rule that rounds the source field down at the decimal position specified by the passed in value.

For negative numbers, the thenRoundDown\(\) method makes the number more positive; the round down value of -2.156 is -2.15. The thenFloor\(\) method makes the same number more negative, -2.16.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_kf4_thd_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operand

</td><td>

Number

</td><td>

Decimal position to the right of the decimal point at which to round the number down. For example, if this value is 2 and the source data element is 6.427, the resulting value is 6.42.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList90
  .fromJSON()
  .setName('Mortgage Rates 05022019 JSON')
  .addRule('interest_rate', '$.quote.interest_rate') 
  .thenRoundDown('2') // Always round the interest rate down to the hundredths place 
  .addRule('monthly_payment', '$.quote.total_loan_amount') 
  .thenDivideBy('180'); 

```

## TransformerRuleList - thenRoundUp\(Number operand\)

Adds an adapter to the current rule that rounds the source data element up at the decimal position specified by the passed in value.

For negative numbers, the thenRoundUp\(\) method makes the number more negative; the round up value of -2.156 is -2.16. The thenCeiling\(\) method makes the same number more positive, -2.15.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_qbw_fjd_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operand

</td><td>

Number

</td><td>

Decimal position to the right of the decimal point at which to round the number up. For example, if this value is 2 and the source data element is 6.422, the resulting value is 6.43.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Mortgage Rates 05022019 JSON')
  .addRule('interest_rate', '$.quote.interest_rate') 
  .thenRoundUp('2') // Always round the interest rate up to the hundredths place 
  .addRule('monthly_payment', '$.quote.total_loan_amount') 
  .thenDivideBy('180'); 

```

## TransformerRuleList - thenSplit\(String splitPattern, String replaceString\)

Adds an adapter to the current rule that splits, reorganizes, and replaces strings within the source field and saves them in the output field.

The **splitPattern** parameter denotes how to divide the source text string into segments. This parameter can be a typical word separator such as a space \(' '\), comma \(','\), or semicolon \(';'\), and can also be any string, such as 'name'. For example, if the source text is "Smith John Michael" and the **splitPattern** is a space, then the available segments are "Smith", "John", and "Michael". To reference a segment, use $\#, where \# is the number of the order of the segment in the source text string. For example, if the method call is `thenSplit(' ', '$2 $3 $1')`, then the output is "John Michael Smith". In addition, you can add constants within the output pattern, such as `thenSplit(' ', 'First name: $2 Middle name: $3 Last name: $1')`.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

<table id="table_w4h_kfx_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

splitPattern

</td><td>

String

</td><td>

String that denotes how to split the text into segments.

</td></tr><tr><td>

replaceString

</td><td>

String

</td><td>

String that defines the output string, including segment references and constants. Not all segments need to be referenced. Reference the segments defined by the **splitPattern** using $\#, where \# is the number of the order of the segment in the source data element. Reference the entire source data element using $0.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

In this example, the CEO name is last name, first name in the source data and in the output it will be transformed to first name last name.

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock Report 05022019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('CEO', '$.quote.CEO') 
  .thenSplit(',', '$2 $1');

```

## TransformerRuleList - thenSubtract\(Number operand\)

Adds an adapter to the current rule that subtracts the passed in value from the source field and stores it in the output field.

**Note:** This is an adapter method and cannot be used on its own. Adapter methods work in conjunction with theaddRule\(\) method. They define adaptations to apply to the output field defined by the addRule\(\) method such as formatting, rounding, and applying patterns.

|Name|Type|Description|
|----|----|-----------|
|operand|Number|Value to subtract from the source data element.|

|Type|Description|
|----|-----------|
|Object|Current TransformerRuleList object.|

```
var transformerRuleList = new sn_tfrm.TransformerRuleList()
  .fromJSON()
  .setName('Stock 05182019 JSON')
  .addRule('ticker', '$.quote.symbol') 
  .addRule('change_percentage', '$.quote.changePercent') 
  .thenMultiply('100') 
  .thenRoundDown('0') 
  .addRule('close_price', '$.quote.close') 
  .thenAdaptCurrency('USD', false) 
  .addRule('trade_price', '$.quote.current_price') 
  .addMultiply('$.quote.trade_quantity')
  .thenSubtract('$.quote.discount_dollars'); 

```

