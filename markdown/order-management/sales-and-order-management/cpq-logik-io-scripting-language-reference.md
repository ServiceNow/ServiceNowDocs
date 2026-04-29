---
title: CPQ scripting language reference
description: View the operators, objects, and keywords that CPQ supports, together with information about type conversion, type checking, alternative scripts for unsupported operations, and accessing object properties.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# CPQ scripting language reference

View the operators, objects, and keywords that CPQ supports, together with information about type conversion, type checking, alternative scripts for unsupported operations, and accessing object properties.

CPQ uses a JavaScript-like language to dynamically change the value of fields and BOM data via rules and enrichments. JavaScript is a complex language built over almost thirty years, and while we are unable to replicate every piece of functionality that a developer would normally expect while coding, CPQ scripting remains a powerful tool to assist in the dynamic configuration of products.

The capabilities of CPQ scripting are always expanding. Check back to see the most up-to-date features.

## Supported operators

Arithmetic operators:

-   **+**

    Addition

-   **-**

    Subtraction

-   **\***

    Multiplication

-   **/**

    Division

-   **%**

    Modulus

-   **++**

    Increment

-   **--**

    Decrement


String operators:

-   **+**

    Concatenation

-   **+=**

    Addition assignment


Assignment operators:

-   **=**

    Assignment

-   **+=**

    Addition assignment

-   **-=**

    Subtraction assignment


Comparison operators:

-   **==**

    Equal to

-   **===**

    Equal value and equal type

-   **!=**

    Not equal to

-   **!==**

    Not equal value nor equal type

-   **&gt;**

    Greater than

-   **&lt;**

    Less than

-   **&gt;=**

    Greater than or equal to

-   **&lt;=**

    Less than or equal to


Logical operators:

-   **&amp;&amp;**

    And

-   **\|\|**

    Or


## Supported objects

Each object supported can be declared with the following:

-   **\[ \]**

    Array

-   **" "**

    String

-   **\( \)**

    Number

-   **true \| false**

    Boolean

-   **\{ \}, new Map\( \)**

    Map

-   **new Date\( \)**

    Date


`undefined`, `NaN`, and `null` are unsupported.

**Note:** Date objects cannot be returned, but they can be referenced and manipulated with the Date APIs in the Help menu.

## Supported keywords

-   `var`
-   `let`
-   `const`
-   `new`
-   `if`
-   `else if`
-   `else`
-   `for`
-   `for/of`
-   `return`

We do not support `while` or unconditional `for` loops with `break`, because of the risk of infinite loops halting performance.

We do not support functions, as the script itself should be small enough to be considered one function. If your script is long with many conditions and variables, consider creating a managed table and using a table query. For more information about using managed tables and table queries, see [Matrix Loader: CSV table upload](../task/cpq-matrix-loader-csv-table-upload.md) and [Minimizing table queries](table_queries.md).

## Alternative scripts for unsupported operations

Assignment multiplication and division \(/= or \*=\): `number = number * otherNumber;`, `number = number / otherNumber;`

Exponentiation \(x\*\*y\): `Math.pow(x, y);`

## Type conversion

Convert arrays to strings: `Array.toString()`

Convert numbers to strings: `[number] + ""`

Convert numeric strings to numbers: `[string] - 0`

**Note:** Strings cannot be treated as arrays, but `.length` does work for strings.

## Type checking

The following returns a Boolean value indicating whether an input is a number: `LGK.isNumber(123)`

## Accessing object properties

You can access the properties of map objects such as `cfgRequest` in two ways.

```
objectName.propertyName
//or
objectName["propertyName"]
```

This is helpful in order to replace large amounts of repetitive code with results from a Table Lookup, since the “propertyName” text could instead be replaced by a variable.

For example, consider a blueprint with the following fields associated with it, and a managed table named shipstatebooleantest.

-   shipState
-   boolean1
-   boolean2
-   boolean3
-   quantity1
-   quantity2
-   quantity3

<table id="table_l5q_jr2_dhc"><tbody><tr><td>

id

</td><td>

shipState

</td><td>

trueBoolean

</td><td>

quantityTest

</td><td>

rowQuantity

</td></tr><tr><td>

1

</td><td>

Arizona

</td><td>

boolean1

</td><td>

quantity1

</td><td>

1

</td></tr><tr><td>

2

</td><td>

Maine

</td><td>

boolean2

</td><td>

quantity2

</td><td>

2

</td></tr><tr><td>

3

</td><td>

California

</td><td>

boolean3

</td><td>

quantity3

</td><td>

3

</td></tr></tbody>
</table>Instead of having an identical `if` statement check what `shipState` is and setting the Boolean values and quantities accordingly, you could instead replace it with only one `if` statement that sets the values based on the results of a table lookup.

In the following On Configure/Reconfigure script, if the `shipState` field has a value, the fields that are returned by the lookup function are set. If the `shipState` field is blank, then all Boolean and quantity fields are set.

```
if (cfgRequest.shipState.value != "" && cfgRequest.shipState.value != null){
	var fieldMapping = lookup("Select trueBoolean,quantityTest,rowQuantity from shipstatebooleantest where shipState = :value", { "value": cfgRequest.shipState.value });
	console.log(fieldMapping);
	if (fieldMapping != []){
		cfgRequest[fieldMapping[0].trueBoolean].set("value",true);
		cfgRequest[fieldMapping[0].quantityTest].set("value",fieldMapping[0].rowQuantity);
	}
}
else{
	var fieldMapping = lookup("Select trueBoolean,quantityTest,rowQuantity from shipstatebooleantest");
  console.log(fieldMapping);
  for (var row of fieldMapping) {
 		cfgRequest[row.trueBoolean].set("value",true);
 		cfgRequest[row.quantityTest].set("value",row.rowQuantity);
  }
} 
```

If your instance of CPQ needs functionality not described here, contact support@logik.io with your use case.

**Related topics**  


[Sample scripts](cpq-sample-scripts.md)

[Using comments and the console to debug scripts](rules-enrichments-comments-and-console_log.md)

[Scripting: Checking for first and subsequent configurations](enrichments_on_configurer_and_reconfigure_behavior.md)

