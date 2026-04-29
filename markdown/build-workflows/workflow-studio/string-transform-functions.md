---
title: String transform functions
description: Use string transform functions to reformat or perform calculations on String data pills.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Transform functions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# String transform functions

Use string transform functions to reformat or perform calculations on String data pills.

String transform functions require a String input data pill. Make sure to use the correct input [data pill type](action-inputs-outputs.md) when applying string transform functions. If a string transform function is applied to an improper data type, the data is not transformed at runtime and the input value is returned instead. For more information on confirming your flow runtime values, see [Test a flow](../task/flow-test.md).

## Convert String to Number

Converts a string into a number.

|Input data pill|Output data pill|
|---------------|----------------|
|String|Number - Number converted from a string.|

-   Input: `“500”`
-   Output: `500`

## Contains

Returns **true** when the input string contains a given sequence of characters.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|String|Characters to search for.|Boolean indicating whether a sequence of characters exists in the input string|

-   Input: `Cheese Pizza`
-   Parameter: `Cheese`
-   Output: `true`

## Does not Contain

Returns **true** when the input string does not contain a given sequence of characters.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|String|Characters to search for.|Boolean indicating whether a sequence of characters does not exist in the input string|

-   Input: `Cheese Pizza`
-   Parameter: `Joey`
-   Output: `true`

## Ends With

Returns **true** when the input string ends with a given sequence of characters.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|String|Characters to search for.|Boolean indicating whether the input string ends with the given sequence of characters|

-   Input: `Cheese Pizza`
-   Parameter: `Pizza`
-   Output: `true`

## First Character

Returns the first character of the input String.

|Input data pill|Output data pill|
|---------------|----------------|
|String|String - Transformed String as the first character of the input String|

-   Input: `Madrid`
-   Output: `M`

In this example, the flow triggers when a User \[sys\_user\] record is created. The flow then updates the **City** field for the User \[sys\_user\] record with a code that is represented as the first character of the city's name.

![Update the city code for a user.](../images/first-character-transform-function-example.png)

## Last Character

Returns the last character of the input String.

|Input data pill|Output data pill|
|---------------|----------------|
|String|String - Transformed String as the last character of the input String|

-   Input: `Madrid`
-   Output: `d`

## Replace String

Returns a replaced string from the input string based on the provided regular expression \(regex\) and replacement string. Use the JavaScript regular expression format.

<table id="table_el5_3w4_mpb"><thead><tr><th>

Input data pill

</th><th>

Parameters

</th><th>

Output data pill

</th></tr></thead><tbody><tr><td>

String

</td><td>

-   **Regex** - Regular expression to be matched for replacement
-   **Replace String** - Replacement string

</td><td>

Resulting string after replacement with given parameters

</td></tr></tbody>
</table>-   Input: `"Example input string."`
-   Parameters:
    -   Regex: `\"`
    -   Replacement string: `\\\"`
-   Output: `\"Example input string.\"`

## Size

Returns the total number of characters in the input String.

|Input data pill|Output data pill|
|---------------|----------------|
|String|Integer|

-   Input: `Example input string.`
-   Output: `21`

## Split

Returns an Array.String based on a provided **Separator** that splits the input String. If the **Separator** field is left blank, the transformation is ignored and the system returns the input String. If entering any data type other than a String as the **Separator**, the system converts the provided value to a String.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|String|**Separator** - Enter a delimiter that specifies where the input String should be split. If left blank, the input String is not transformed at runtime.|Array.String - An array of substrings from the input String|

-   Input: `Example, input, string.`
-   Separator: `,`
-   Output: `["Example", "input", "string."]`

## Starts With

Returns **true** when the input string starts with a given sequence of characters.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|String|Characters to search for.|Boolean indicating whether the input string starts with the given sequence of characters|

-   Input: `Cheese Pizza`
-   Parameter: `Chees`
-   Output: `true`

## Substring

Returns a substring from the input String that is based on the provided **Start Index** and **End Index**. Input String index starts at 0.

<table id="table_orx_v1n_mkb"><thead><tr><th>

Input data pill

</th><th>

Parameters

</th><th>

Output data pill

</th></tr></thead><tbody><tr><td>

String

</td><td>

-   **Start Index** - Index of the first character to include in the returned substring
-   **End Index** - Index of the last character to include in the returned substring

</td><td>

String - Transformed String as a substring of the input String

</td></tr></tbody>
</table>**Note:** If the **Start Index** value is longer than the string's length, then the transform function returns the input string. This behavior is different from the JavaScript substring\(\) method, which instead returns an empty string.

-   Input: `Example input string`
-   Start Index: `3`
-   End Index: `6`
-   Output: `mple`

-   Input: `Example input string`
-   Start Index: `30`
-   End Index: `40`
-   Output: `Example input string`

## To Lower Case

Converts the input String to all lowercase characters.

|Input data pill|Output data pill|
|---------------|----------------|
|String|String in all lowercase characters|

-   Input: `ExamPle inpuT stRing`
-   Output: `example input string`

## To Proper Case

Changes the case of words in the input string. Capitalizes the first letter of each word and makes the remaining letters in the word lower case. A word is considered any string separated by a space, hyphen, backslash, or forward slash character. The transform function always evaluates words from left-to-right to determine the first letter.

|Input data pill|Output data pill|
|---------------|----------------|
|String|String in proper case|

-   Input: `exAMPle-input string/TEXT`
-   Output: `Example-Input String/Text`

## To Upper Case

Converts the input String to all uppercase characters.

|Input data pill|Output data pill|
|---------------|----------------|
|String|String in all uppercase characters|

-   Input: `ExamPle inpuT stRing`
-   Output: `EXAMPLE INPUT STRING`

## Trim

Removes white space from the beginning and end of the input String. Does not remove white space within the input String.

|Input data pill|Output data pill|
|---------------|----------------|
|String|String - Transformed String with trimmed white space|

-   Input: `SQL Server APAC 1`
-   Output: `SQL Server APAC 1`

In this example, the action makes a REST call to a third-party system and GETs a response body containing data about a server. Then, the Trim transform function removes any unwanted white space before adding the server's name to a new record in the Server \[cmdb\_ci\_server\] table.

![Trim white space from a server name before adding it to the CMDB.](../images/trim-transform-function-example.png)

**Parent Topic:**[Transform functions](../concept/transform-functions.md)

