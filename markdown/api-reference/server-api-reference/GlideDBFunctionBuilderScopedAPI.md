---
title: GlideDBFunctionBuilder - Scoped, Global
description: The GlideDBFunctionBuilder API provides methods to build functions to perform SQL operations in the database.Instantiates a GlideDBFunctionBuilder object.Begins a new AND expression, which returns true only if all expressions provided to it as parameters are true. At least one boolean-valued expression must be provided as a parameter.Adds the values of two or more integer fields.Builds the database function defined by the GlideDBFunctionBuilder object.Takes any number of comma-separated fields as input and returns the first non-empty value.Begins a new COMPARE expression which performs a comparison between two expressions.Concatenates the values of two or more fields.Defines a constant value to use in the function. If used with the dayofweek\(\) method, the string defines whether to use Sunday or Monday as the first day of the week.Determines the duration using a given start date/time and end date/time.Returns an integer representing the day of the week for a given date.Divides the value of one integer field by another.Defines a field on which a SQL operation is performed.Determines the number of code units in a field.Multiplies the values of two integer fields.Begins a new OR expression which returns true if at least one of the expressions provided to it as a parameter is true.Returns the first occurrence of a specified string within a column of a table.Returns a substring from a specified column of a table starting at a specified location.Subtracts the value of one integer field from another.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDBFunctionBuilder - Scoped, Global

The GlideDBFunctionBuilder API provides methods to build functions to perform SQL operations in the database.

These methods provide a way to build Relational Database Management System \(RDBMS\) functions to perform SQL operations on record data. You can use these methods in both scoped and global server scripts.

To use platform functions:

-   Construct a function using the GlideDBFunctionBuilder constructor and associated methods.
-   After building a function, you apply the function to the current record using the addFunction\(\) method of the GlideRecord class.
-   Add the function to a query using the addQuery\(\) method of the GlideRecord class.
-   Retrieve the results of the function using the existing GlideRecord API methods such as getValue\(\) and getElement\(\).

For example:

```
var functionBuilder = new GlideDBFunctionBuilder();
var dbFunction = functionBuilder.position();
dbFunction = functionBuilder.constant('my'); // search_term: Text to search for in the specified table column.
dbFunction = functionBuilder.field('short_description');  // column: Name of the table column to search.
dbFunction = functionBuilder.build();

gs.log(dbFunction);

var gr_incident = new GlideRecord('incident'); // Table containing the column to search
gr_incident.addFunction(dbFunction);
gr_incident.addQuery("short_description", "CONTAINS", "my");
gr_incident.setLimit(20);
gr_incident.query();
while(gr_incident.next()) {
  gs.info(gr_incident.short_description + "\n position('my', short_description): " + gr_incident.getValue(dbFunction));
}
```

For additional information on Function fields, see [Function field](https://www.servicenow.com/docs/access?context=platform-support-functions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideDBFunctionBuilder - GlideDBFunctionBuilder\(\)

Instantiates a GlideDBFunctionBuilder object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var builder = new GlideDBFunctionBuilder();

```

## Scoped GlideDBFunctionBuilder - andFunc\(expr1, expr2, …\)

Begins a new AND expression, which returns true only if all expressions provided to it as parameters are true. At least one boolean-valued expression must be provided as a parameter.

|Name|Type|Description|
|----|----|-----------|
|expression|Boolean-valued GlideFunction Expression|At present, glide functions that meet this criteria include and\(\), or\(\), and compare\(\).|

|Type|Description|
|----|-----------|
|String|The resultant GlideFunction expression.|

The following example shows how to define and build a simple case statement.

```
var expr = new GlideDBFunctionBuilder() 
    .andFunc() 
        .compare().field('first_name').constant('=').constant('John').endfunc() 
        .compare().field('active').constant('=').constant(1).endfunc() 
    .endfunc() 
    .build(); 
gs.info("Expression: " + expr);
```

Output:

```
Expression: glidefunction:and(compare(first_name,'=','John'),compare(active,'=','1'))
```

## Scoped GlideDBFunctionBuilder - add\(\)

Adds the values of two or more integer fields.

Use the field\(String field\) method to define fields on which the operation is performed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myAddingFunction = functionBuilder.add();
myAddingFunction = functionBuilder.field('order');
myAddingFunction = functionBuilder.field('priority');
myAddingFunction = functionBuilder.build();
```

## Scoped GlideDBFunctionBuilder - build\(\)

Builds the database function defined by the GlideDBFunctionBuilder object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myAddingFunction = functionBuilder.add();
myAddingFunction = functionBuilder.field('order');
myAddingFunction = functionBuilder.field('priority');
myAddingFunction = functionBuilder.build();
gs.info(myAddingFunction);
```

Output:

```
*** Script: glidefunction:add(order,priority)
```

## Scoped GlideDBFunctionBuilder - coalesce\(\)

Takes any number of comma-separated fields as input and returns the first non-empty value.

|Name|Type|Description|
|----|----|-----------|
|argument|String|A list containing a constant value \(strings, objects, booleans\) or a field. Accepted format: `glidefunction:coalesce(<string, string, string, etc.>)`. An argument can have any number of parameters but must have at least one parameter defined.|

|Type|Description|
|----|-----------|
|String|The first value in the argument list that is non-null. If no values are non-null, null is returned. If no arguments are provided in the creation of the function object, "invalid function" is returned as a string.|

The following example request demonstrates how to form the coalesce guide function to return null values according to closed\_at, resolved\_at, and sys\_updated\_on fields.

```
var gr = new GlideRecord('incident');
var func = "glidefunction:coalesce(closed_at, resolved_at,sys_updated_on)";
gr.addFunction(func);
gr.query(); 
while(gr.next())
gs.info(gr.getValue(func));
```

The script returns the first non-null value from a field out of this list: \[closed\_at, resolved\_at, sys\_updated\_on\] for each incident record in the incident table and outputs them with `gs.info`.

```
2016-12-14 02:46:44
2018-01-09 22:55:16
2018-01-07 22:54:55
2018-01-13 23:02:54
2018-01-09 23:12:02
```

## Scoped GlideDBFunctionBuilder - compare\(exp1, op, exp2\)

Begins a new COMPARE expression which performs a comparison between two expressions.

<table id="table_a5r_px1_mxb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

exp1

</td><td>

String

</td><td>

Left comparison expression. Can be a constant, reference to a field, or another Glide function.

</td></tr><tr><td>

op

</td><td>

String

</td><td>

A comparison operator, surrounded with quotes. Accepted values:-   “’=’”
-   “’&lt;’”
-   “’&gt;’”
-   “’&lt;=’”
-   “’&gt;=’”

</td></tr><tr><td>

exp2

</td><td>

String

</td><td>

Right comparison expression. Can be a constant, reference to a field, or another Glide function.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The resultant GlideFunction expression.|

The following example shows how to build a glidefunction expression using the compare\(\) operation. After calling compare\(\), three additional calls must be made to specify each of the three required parameters, which is then completed by a single call to endfun\(\). Below, we create two separate compare\(\) expressions and provide them as parameters to the or\(\) expression.

```
var expr = new GlideDBFunctionBuilder() 
    .orFunc() 
        .compare().field('first_name').constant('=').constant('John').endfunc() 
        .compare().field('active').constant('=').constant(1).endfunc() 
    .endfunc() 
    .build();
```

Output:

```
Expression: glidefunction:or(compare(first_name,'=','John'),compare(active,'=','1'))
```

## Scoped GlideDBFunctionBuilder - concat\(\)

Concatenates the values of two or more fields.

Use the field\(String field\) method to define fields on which the operation is performed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myConcatFunction = functionBuilder.concat();
myConcatFunction = functionBuilder.field('short_description');
myConcatFunction = functionBuilder.field('caller_id.name');
myConcatFunction = functionBuilder.build();
```

## Scoped GlideDBFunctionBuilder - constant\(String constant\)

Defines a constant value to use in the function. If used with the dayofweek\(\) method, the string defines whether to use Sunday or Monday as the first day of the week.

<table id="table_lww_s2h_jbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

constant

</td><td>

String

</td><td>

A constant value used in a function. When used with the dayofweek\(\) method, the value defines whether the week starts on a Sunday or Monday.

 -   **1**: Week begins on Sunday.
-   **2**: Week begins on Monday.

 This definition enables the dayofweek\(\) method to return the correct day of the week from a given date. If a value other than 1 or 2 is provided, the dayofweek\(\) method uses Sunday as the first day of the week.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to call this method.

```
var functionBuilder = new GlideDBFunctionBuilder();
var dbFunction = functionBuilder.position();
dbFunction = functionBuilder.constant('my');
dbFunction = functionBuilder.field('short_description');
dbFunction = functionBuilder.build();

gs.log(dbFunction);

var g = new GlideRecord('incident');
g.addFunction(dbFunction);
g.addQuery("short_description", "CONTAINS", "my");
g.setLimit(20);
g.query();
while(g.next()) {
  gs.info(g.short_description + "\n position('my', short_description): " + g.getValue(dbFunction));
}
```

## Scoped GlideDBFunctionBuilder - datediff\(\)

Determines the duration using a given start date/time and end date/time.

Use the field\(String field\) method to define start and end date/time fields.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myDateDiffFunction = functionBuilder.datediff();
myDateDiffFunction = functionBuilder.field('sys_updated_on');
myDateDiffFunction = functionBuilder.field('opened_at');
myDateDiffFunction = functionBuilder.build();
```

## Scoped GlideDBFunctionBuilder - dayofweek\(\)

Returns an integer representing the day of the week for a given date.

Use the field\(String field\) method to define the given date/time. Use the constant\(String constant\) method to define whether the week starts on a Sunday or Monday.

This method can be used with MySQL, Oracle, and Microsoft SQL Server databases only. If using an Oracle database, the NLS\_TERRITORY setting must be set to a territory with Sunday as the first day of the week.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_pd2_dnh_jbb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integer

</td><td>

If the first day of the week is set to Sunday in the constant\(String constant\) method, return values are associated with the following days of the week:

 -   **1**: Sunday
-   **2**: Monday
-   **3**: Tuesday
-   **4**: Wednesday
-   **5**: Thursday
-   **6**: Friday
-   **7**: Saturday

 If the first day of the week is set to Monday:

 -   **1**: Monday
-   **2**: Tuesday
-   **3**: Wednesday
-   **4**: Thursday
-   **5**: Friday
-   **6**: Saturday
-   **7**: Sunday

 If a value other than 1 or 2 is provided in the constant\(String constant\) method, the dayofweek\(\) method uses Sunday as the first day of the week.

</td></tr></tbody>
</table>```
var functionBuilder = new GlideDBFunctionBuilder();
var dayOfWeekFunction = functionBuilder.dayofweek();
dayOfWeekFunction = functionBuilder.field('opened_at');
dayOfWeekFunction = functionBuilder.constant('2');
dayOfWeekFunction = functionBuilder.build();

var now_GR = new GlideRecord('incident');
now_GR.addFunction(dayOfWeekFunction);
now_GR.query();
while(now_GR.next())
gs.log(now_GR.getValue(dayOfWeekFunction));

```

## Scoped GlideDBFunctionBuilder - divide\(\)

Divides the value of one integer field by another.

Use the field\(String field\) method to define fields on which the operation is performed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myDivideFunction = functionBuilder.divide();
myDivideFunction = functionBuilder.field('order');
myDivideFunction = functionBuilder.field('priority');
myDivideFunction = functionBuilder.build();
```

## Scoped GlideDBFunctionBuilder - field\(String field\)

Defines a field on which a SQL operation is performed.

|Name|Type|Description|
|----|----|-----------|
|field|String|The field on which you are performing the SQL operation.|

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myAddingFunction = functionBuilder.add();
myAddingFunction = functionBuilder.field('order');
myAddingFunction = functionBuilder.field('priority');
myAddingFunction = functionBuilder.build();
```

## Scoped GlideDBFunctionBuilder - length\(\)

Determines the number of code units in a field.

Use the field\(String field\) method to define fields on which the operation is performed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myLengthFunction = functionBuilder.length();
myLengthFunction = functionBuilder.field('short_description');
myLengthFunction = functionBuilder.build();

```

## Scoped GlideDBFunctionBuilder - multiply\(\)

Multiplies the values of two integer fields.

Use the field\(String field\) method to define fields on which the operation is performed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var myMultiplyFunction = functionBuilder.multiply();
myMultiplyFunction = functionBuilder.field('order');
myMultiplyFunction = functionBuilder.field('priority');
myMultiplyFunction = functionBuilder.build();
```

## Scoped GlideDBFunctionBuilder - orFunc\(expression\)

Begins a new OR expression which returns true if at least one of the expressions provided to it as a parameter is true.

At least one boolean-valued expression must be provided as a parameter.

|Name|Type|Description|
|----|----|-----------|
|expression|Boolean-valued GlideFunction Expression|At Present, glide functions that meet this criteria include and\(\), or\(\), and compare\(\).|

|Type|Description|
|----|-----------|
|String|The resultant GlideFunction expression.|

The following example shows how to build a glidefunction expression using the or\(\) operation. The expression returns true if either the **first\_name** field is 'John" or the **active** field is true. The resulting expression string may then be used wherever glidefunction expressions are accepted.

```
var expr = new GlideDBFunctionBuilder() 
    .orFunc() 
        .compare().field('first_name').constant('=').constant('John').endfunc() 
        .compare().field('active').constant('=').constant(1).endfunc() 
    .endfunc() 
    .build(); 
gs.info("Expression: " + expr);
```

Output:

```
Expression: glidefunction:or(compare(first_name,'=','John'),compare(active,'=','1'))
```

## Scoped GlideDBFunctionBuilder - position\(\)

Returns the first occurrence of a specified string within a column of a table.

Optionally you can specify a location within the string to start the search. This method equates to the `LOCATE(substring, str, position)` in MySQL.

You can use this method to find interesting data points or custom reports by data analysts. Typically you will use this method for data warehousing or to extract, transform and load \(ETL\) data into less flexible systems.

To use this method in Dictionary records, use `glidefunction:position(<serarch_term>,<column>)`.

**Note:** The parameters specified in the following table are not passed with the method call, but rather are set in the GlideDBFunctionBuilder\(\) object.

<table id="table_h5j_hy1_rwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

search\_term

</td><td>

String

</td><td>

Text to search for in the specified table column.

</td></tr><tr><td>

column

</td><td>

String

</td><td>

Name of the table column to search. The table is specified in the associated GlideRecord object.

</td></tr><tr><td>

start\_position

</td><td>

Number

</td><td>

Optional. Location in the column text to start the search.Default: 1

</td></tr></tbody>
</table><table id="table_i5j_hy1_rwb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

Position of the first occurrence of the specified search term.Returns `0` if the search term is not found in the associated text. Returns `NULL` if any required argument is NULL.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var functionBuilder = new GlideDBFunctionBuilder();
var dbFunction = functionBuilder.position();
dbFunction = functionBuilder.constant('my'); // search_term: Text to search for in the specified table column.
dbFunction = functionBuilder.field('short_description');  // column: Name of the table column to search.
dbFunction = functionBuilder.build();

gs.log(dbFunction);

var gr_incident = new GlideRecord('incident'); // Table containing the column to search
gr_incident.addFunction(dbFunction);
gr_incident.addQuery("short_description", "CONTAINS", "my");
gr_incident.setLimit(20);
gr_incident.query();
while(gr_incident.next()) {
  gs.info(gr_incident.short_description + "\n position('my', short_description): " + gr_incident.getValue(dbFunction));
}
```

Output:

```
*** Script: glidefunction:position('my',short_description)
*** Script: Wireless access is down in my area
 position('my', short_description): 28
*** Script: Printer in my office is out of toner
 position('my', short_description): 12
*** Script: Reset my password
 position('my', short_description): 7
*** Script: I can't launch my VPN client since the last software update
 position('my', short_description): 16
*** Script: Missing my home directory
 position('my', short_description): 9
*** Script: Seem to have an issue with my hard drive...
 position('my', short_description): 28
*** Script: Please remove the latest hotfix from my PC
 position('my', short_description): 38
*** Script: I can't get my weather report
 position('my', short_description): 13
*** Script: Reset my password
 position('my', short_description): 7
*** Script: my PDF docs are all locked from editing
 position('my', short_description): 1
*** Script: My desk phone does not work
 position('my', short_description): 1
*** Script: Can't log into SAP from my laptop today
 position('my', short_description): 25
*** Script: My computer is not detecting the headphone device
 position('my', short_description): 1
*** Script: My disk is still having issues. Can't delete a file
 position('my', short_description): 1
*** Script: The USB port on my PC stopped working
 position('my', short_description): 17
```

## Scoped GlideDBFunctionBuilder - substring\(\)

Returns a substring from a specified column of a table starting at a specified location.

Optionally you can also specify a location within the string where to stop the text extraction. This method equates to the `LOCATE(substring, str, position)` in MySQL.

This method works similar to that of JavaScript, just at the database level. You can use this method to find interesting data points or custom reports for data analysts. Typically you will use this method for data warehousing or to extract, transform and load \(ETL\) data into less flexible systems.

To use this method in Dictionary records, use `glidefunction:substring(<field>,<start_position>,<end_position>)`

**Note:** The parameters specified in the following table are not passed with the method call, but rather are set in the GlideDBFunctionBuilder\(\) object.

<table id="table_oc5_hgb_rwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field

</td><td>

String

</td><td>

Name of the column in the table from which to obtain the text. The table is specified in the associated GlideRecord object.

</td></tr><tr><td>

start\_position

</td><td>

Number

</td><td>

Location in the column text to start extracting text.

</td></tr><tr><td>

end\_position

</td><td>

Number

</td><td>

Optional. Location in the column text to stop extracting text.Default: End of text in the specified column.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Text extracted from the specified table column.|

The following code example shows how to call this method.

```
var functionBuilder = new GlideDBFunctionBuilder();
var dbFunction = functionBuilder.substring();
dbFunction = functionBuilder.field('short_description');  // field: Column within the table to obtain the substring
dbFunction = functionBuilder.constant(0); // start_position: Location in the column text to start extracting text
dbFunction = functionBuilder.constant(20); // end_position: Location in the column text to stop extracting text.
dbFunction = functionBuilder.build();

gs.log(dbFunction);

var gr_incident = new GlideRecord('incident'); // Table containing the column from which to extract the text
gr_incident.addFunction(dbFunction);
gr_incident.addQuery("short_description", "CONTAINS", "my");
gr_incident.setLimit(20);
gr_incident.query();
while(gr_incident.next()) {
  gs.info(gr_incident.short_description + "\n substring(short_description, 0, 20): " + gr_incident.getValue(dbFunction));
}
```

Output:

```
*** Script: glidefunction:substring(short_description,'0','20')
*** Script: Wireless access is down in my area
 substring(short_description, 0, 20): Wireless access is 
*** Script: Printer in my office is out of toner
 substring(short_description, 0, 20): Printer in my offic
*** Script: Reset my password
 substring(short_description, 0, 20): Reset my password
*** Script: I can't launch my VPN client since the last software update
 substring(short_description, 0, 20): I can't launch my V
*** Script: Missing my home directory
 substring(short_description, 0, 20): Missing my home dir
*** Script: Seem to have an issue with my hard drive...
 substring(short_description, 0, 20): Seem to have an iss
*** Script: Please remove the latest hotfix from my PC
 substring(short_description, 0, 20): Please remove the l
*** Script: I can't get my weather report
 substring(short_description, 0, 20): I can't get my weat
*** Script: Reset my password
 substring(short_description, 0, 20): Reset my password
*** Script: my PDF docs are all locked from editing
 substring(short_description, 0, 20): my PDF docs are all
*** Script: My desk phone does not work
 substring(short_description, 0, 20): My desk phone does 
*** Script: Can't log into SAP from my laptop today
 substring(short_description, 0, 20): Can't log into SAP 
*** Script: My computer is not detecting the headphone device
 substring(short_description, 0, 20): My computer is not 
*** Script: My disk is still having issues. Can't delete a file
 substring(short_description, 0, 20): My disk is still ha
*** Script: The USB port on my PC stopped working
 substring(short_description, 0, 20): The USB port on my 
```

## Scoped GlideDBFunctionBuilder - subtract\(\)

Subtracts the value of one integer field from another.

Use the field\(String field\) method to define fields on which the operation is performed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var functionBuilder = new GlideDBFunctionBuilder();
var mySubtractFunction = functionBuilder.subtract();
mySubtractFunction = functionBuilder.field('order');
mySubtractFunction = functionBuilder.field('priority');
mySubtractFunction = functionBuilder.build();
```

