---
title: Utilities transform functions
description: Use utilities transform functions to return a Complex Object from an Array, or a value associated with a specific key.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Transform functions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Utilities transform functions

Use utilities transform functions to return a Complex Object from an Array, or a value associated with a specific key.

Utilities transform functions require an Array, Name-Value Pair, String, Integer, or Choice input data pill. Make sure to use the correct input [data pill type](action-inputs-outputs.md) when applying utilities transform functions. If a utility transform function is applied to an improper data type, the data is not transformed at runtime and the input value is returned instead. For more information on confirming your flow runtime values, see [Test a flow](../task/flow-test.md).

## Get First Item from Array

Returns the first item from the input array as a complex object.

|Input data pill|Output data pill|
|---------------|----------------|
|Array|**Complex Object** - First item found in the input array|

## Get Item from Array

Returns a Complex Object from the input Array. Enter a value for the **Nth Item** in the input Array that you want to return. The **Nth Item** represents the Array index, starting at 0.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Array|**Nth Item** - Enter the index of the target object in the input Array. The Array index starts at 0.|Complex Object|

## Get Item from Name/Values

Returns a value that is associated with a matching key from a map of Name-Value Pairs.

<table id="table_mjc_xdn_mkb"><thead><tr><th>

Input data pill

</th><th>

Parameters

</th><th>

Output data pill

</th></tr></thead><tbody><tr><td>

Name-Value Pairs

</td><td>

-   **Key** - Name of the key that is used to look up its corresponding value
-   **Default** - The value returned when there is no matching key

</td><td>

String associated with the matching key

</td></tr></tbody>
</table>**Note:** When applying the Get Item from Name/Values transform function, consider that the runtime value might be the system value, not the display value. For example, if mapping the **Priority** field in the Incident table to a similar field in a remote table, the returned runtime value might be 2, not 2 - High.

Example usage:

-   Input: `"username":"abel.tuter"`
-   Key: `username`
-   Default: `example.username`
-   Output: `abel.tuter`

In this example, an action makes a REST call to a third-party system and GETs ticket data as a map of Name-Value Pairs. A Ticket ID is provided as an output for this action. The Get Item from Name/Values transform function returns either the value that is associated with the `ticket_id` key or `Ticket ID not found`.

![Associated value for ticket_id key or "Ticket ID not found" returned as action output.](../images/value-map-transform-function-example.png)

## Get Last Item from Array

Returns the last item from the input array as a complex object.

|Input data pill|Output data pill|
|---------------|----------------|
|Array|**Complex Object** - Last item found in the input array|

## Is Blank

Returns **true** when the input is blank. A string input is blank when it is an empty string. An integer input is blank when it is zero. A Boolean input is blank when it is **false**.

**Note:** This transform function doesn't support reference inputs.

|Input data pill|Output|
|---------------|------|
|Any|Returns **true** or **false**|

Example usage:

-   Input: an integer data pill with `0`
-   Output: `true`

## Is False

Returns **true** when the input is false. A string is false when it is an empty string. An integer is false when it is zero. A Boolean input is false when it is **false**.

|Input data pill|Output data pill|
|---------------|----------------|
|Any|Returns **true** or **false**|

Example usage:

-   Input: an integer data pill with `13`
-   Output: `false`

## Is Not Blank

Returns **true** when the input is not blank. A string is not blank when it is not an empty string. An integer is not blank when it is anything but zero. A Boolean input is not blank when it is **true**.

**Note:** This transform function doesn't support reference inputs.

|Input data pill|Output data pill|
|---------------|----------------|
|Any|Returns **true** or **false**|

Example usage:

-   Input: an integer data pill with `13`
-   Output: `true`

## Is Null

Returns **true** when the input value is null. An input is null if it is not initialized, or if it is a null object or reference.

|Input data pill|Output|
|---------------|------|
|Any|Returns **true** or **false**|

Example usage:

-   Input: an integer data pill with `725`
-   Output: `false`

## Is True

Returns **true** when the input is true. A string is true when it is not an empty string. An integer is true when it is anything but zero. A Boolean input is true when it is **true**.

|Input data pill|Output data pill|
|---------------|----------------|
|Any|Returns **true** or **false**|

Example usage:

-   Input: an integer data pill with `13`
-   Output: `true`

## Key Value Map

Returns a value associated with a matching key, or a default value if there is not a match.

<table id="table_qqy_yqg_ykb"><thead><tr><th>

Input data pill

</th><th>

Parameters

</th><th>

Output data pill

</th></tr></thead><tbody><tr><td>

String or Integer

</td><td>

-   **Name** - The key that is used to find the corresponding value
-   **Value** - The value matched to a specific key
-   **Default** - The value returned when there is no matching name

</td><td>

String associated with the matching key

</td></tr></tbody>
</table>Example usage:

In this example, a log action stores a record's priority as a message. In the Name-Values section, each priority is mapped to a corresponding string value. When the flow runs, the record's priority number is transformed to a string, and the string is logged to a message.

![A Key-value map transforms a value from a number to a string.](../images/key-value-transform-function-example.png)

## Sort

Sorts the specified array in ascending or descending order.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Array.String, Array.Integer, Array.Boolean, or Array.Datetime. - Unsorted array|**Sort Order** - Ascending or descending|Array - Sorted array|

**Note:** Sort function is case-sensitive for array.strings.

Example usage:

-   Input: `[7, 2, 3, 1, 7, 9]`
-   Parameter: Ascending
-   Output: `[1, 2, 3, 7, 7, 9]`

## Unique

Removes the duplicate elements from the specified array.

|Input data pill|Output data pill|
|---------------|----------------|
|Array.String, Array.Integer, Array.Boolean, or Array.Datetime.|Array - After duplicated elements are removed|

Example usage:

-   Input: `[7, 2, 3, 2, 7, 9]`
-   Output: `[7, 2, 3, 9]`

## Join

Concatenates the individual elements of the specified array with the specified delimiter and returns the concatenated string.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Array.String, Array.Integer, Array.Boolean, or Array.Datetime.|Delimiter - Character that separates the individual elements after concatenation.|String - String after a delimiter is added.|

Example usage:

-   Input: `[1, 2, 3]`
-   Parameters: `<`
-   Output: `1<2<3`

**Parent Topic:**[Transform functions](../concept/transform-functions.md)

