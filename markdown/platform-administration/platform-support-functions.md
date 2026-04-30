---
title: Function field
description: Create function fields and scripts in the ServiceNow AI Platform to perform common database transformations and calculations.Create a field that displays the results of a database function, such as a mathematical operation, field length computation, or day of the week calculation. Test in a subproduction instance before deploying to a production instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Function field

Create function fields and scripts in the ServiceNow AI Platform to perform common database transformations and calculations.

Regular fields store a value in the database. Instead of storing data, a function field displays the results of a database query. Function fields do not have an associated database column. Instead, function fields generate a value based on simple computations of other fields and constants. They can be used like any other fields in the system: in forms, lists, query conditions, reports, data visualizations, and so on.

**Warning:** A function field that references another function field in the function will result in an error. Function fields don't hold data or evaluate in run-time.

## Use case

You want to identify all incidents with a probably useless short description of fewer than 10 characters.

Instead of querying all records to determine which record meets a given criteria, create a function field or function script that retrieves only the records that meet the criteria.

For a simple computation, it is better to use a function field or function script rather than store a computed value. The value is always calculated on retrieval. Another benefit of using function fields is that the database server performs the transformation rather than the application node.

## Function fields versus calculated fields

The values of the calculated fields are stored in the database. The values of function fields or function scripts are not stored in the database, but are calculated at the time of retrieval. Function field values are always up to date.

## Function fields versus business rules

Use function fields or scripts when business logic is based on a simple transformation of one or more existing fields. Function fields and scripts let you implement business logic without storing and maintaining the result of a transformation.

## Function fields versus filters, query strings, and Rhino

Rather than calling Rhino to perform string transformations, you can use a function field or function script to perform the transformations for you. Function fields and function scripts are more efficient and result in up-to-date values that do not have to be stored or maintained.

## Function field limitations

Because function field calculations are not stored in the database, some operations are not relevant.

-   Function fields cannot be directly audited or indexed.

    **Note:** To index a function field as if it were a regular field, make sure the individual fields used by the function are indexed. Or for best performance, make sure that there is a composite index including all fields that are used in the function.

-   Function fields cannot be encrypted, since a function field value is never stored in the database.
-   Function fields cannot be converted to regular fields or vice versa.
-   Function fields that you create in the Reporting UI do not support dot-walking. For more information, see [Configure function fields in Reporting](https://www.servicenow.com/docs/access?context=configure-function-fields&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).
-   Security is evaluated on the components of the function and on the calculated value of the field. When used in visualizations, sections that contain information that the user is not permitted to see are hidden from the user.
-   Field function names must be unique.

## Defining platform functions

Platform functions can be defined in two ways:

1.  Use the following application programming interfaces \(APIs\) to build and use functions in a script.

    |APIs|Description|
    |----|-----------|
    |[Scoped GlideDBFunctionBuilder](https://www.servicenow.com/docs/access?context=GlideDBFunctionBuilderScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|Construct the function to perform a SQL operation.|
    |[GlideRecord - addFunction\(Object function\)](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|Apply the function to a GlideRecord.|
    |[GlideDBFunctionCaseBuilder - Global](https://www.servicenow.com/docs/access?context=GlideDBFunctionCaseBuilderAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|Build case statements.|

2.  Create a field that holds the function definition, as shown in the following example.

    ![Function field definition](../image/platform-functions-dictionary-entry.png)

    Select the **Function field** check box on the Dictionary Entry \[sys\_dictionary\] form. This action specifies that the field runs a function rather than stores a value.


## glidefunction operations

Function fields can perform the following operations using the `glidefunction:<operation>` syntax. When providing a field as an argument, you can dot-walk to related fields. For example, `cmdb_ci.name`.

**Note:** The function field type must be compatible with the return type of the glide function. For example, integer, longint, string, and so on. If the returned type cannot be converted to the dictionary type, you get exceptions.

<table id="table_g33_2jx_2nb"><thead><tr><th>

Operation

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

add\(\)

</td><td id="add-func-desc">

Takes two number fields as input, adds them, and returns the results as a field value. This function also takes numerical values for either input. Place numerical values in single or double quotation marks.

</td><td id="add-func-ex">

glidefunction:add\(child\_incidents, parent\_incident\) Returns 6 if the incident has five child incidents and one parent incident.

Possible return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

</td></tr><tr><td>

coalesce\(\)

</td><td id="coal-func-desc">

Takes any number of comma-separated fields as input and returns the first non-empty value.

</td><td id="coal-func-ex">

glidefunction:coalesce\(closed\_at, resolved\_at, sys\_updated\_on\) If the value of closed\_at is empty, the function returns the value of resolved\_at. If the value of resolved\_at is also empty, the function returns the value of sys\_updated\_on.

Return type: Text

</td></tr><tr><td>

concat\(\)

</td><td id="concat-func-desc">

Takes any number of comma-separated fields and constants as input, concatenates the input, and returns a single string as a field value.

</td><td id="concat-func-ex">

glidefunction:concat\(incident\_number, '/', short\_description\) Returns "INC0001 / My client needs a new laptop." if the value of the number field is 'INC0001' and the short\_description is 'My client needs a new laptop'.

Return type: Text

</td></tr><tr><td>

datediff\(\)

</td><td id="datediff-func-desc">

Takes two date/time fields as input, calculates the difference between the dates in days, minutes, and seconds, and returns the results as a duration field value.

</td><td id="datediff-func-ex">

glidefunction:datediff\(closed\_at, sys\_created\_on\) Returns the duration of an incident from the creation date to the close date. Example result: 10 days, 8 hours 23 minutes 11 seconds

Return type: Duration

</td></tr><tr><td>

dayofweek\(\)

</td><td id="dayofweek-func-desc">

Takes two arguments: A date field and a constant of either '1' \(week starts on Sunday\) or '2' \(week starts on Monday\). Returns the results as an integer value that represents the day of the week.The `dayofweek()` function uses UTC dates, but adjusts comparison values based on the instance's time zone.

</td><td id="dayofweek-func-ex">

glidefunction:dayofweek\(resolved\_at, '1'\). If resolved\_at occurs on a Wednesday, returns 4 if the integer is 1 and returns 3 if the integer is 2.

Return type: Whole number

</td></tr><tr><td>

distance\_sphere\(\)

</td><td id="dist-sph-func-desc">

Takes two locations and returns the distance between them in meters.

</td><td id="dist-sph-func-ex">

-   glidefunction:distance\_sphere\('-0.189937', '51.473584', '80.206458', '25.767242'\)

Returns the distance between the two sets of longitude and latitude pairs.

-   glidefunction:distance\_sphere\(u\_location, '80.206458', '25.767242'\)

Returns the distance between the u\_location geo point field and the longitude and latitude coordinates.

-   glidefunction:distance\_sphere\(location1, location2\)

Returns the distance between the location1 and location2 geo point fields.

-   glidefunction:divide\(distance\_sphere\(location1, '-0.189937', '51.473584'\), '1000'\)

Returns the distance between the location1 geo point field and London in kilometers.


 Return type: Decimal

</td></tr><tr><td>

divide\(\)

</td><td id="div-func-desc">

Takes two number fields as input, divides the first by the second, and returns the result as a field value. This function also takes numerical values for either input. Place numerical values in single or double quotation marks.

</td><td id="div-func-ex">

glidefunction:divide\(u\_num2,u\_num1\) Returns 5 if num2 = 10 and num1 = 2.

Possible return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

</td></tr><tr><td>

get\_latitude\(\)

</td><td id="get-lat-func-desc">

Takes any geo point column or numeric field or numeric constant and converts it to a valid latitude value within the \[-90,90\] range.

</td><td id="get-lat-func-ex">

-   glidefunction:get\_latitude\(u\_geo\_point\_field\)Returns the latitude value in the u\_geo\_point\_field.
-   glidefunction:get\_latitude\(u\_numerical\_column\)Returns the latitude value in the u\_numerical\_column within \[-90,90\] range.
-   glidefunction:get\_latitude\('305.767242'\)Returns -54.232758 latitude value.

 Return type: Floating point number

</td></tr><tr><td>

get\_longitude\(\)

</td><td id="get-long-func-desc">

Takes any geo point column or numeric field or numeric constant and converts it to a valid longitude value within the \[-179,180\] range.

</td><td id="get-long-func-ex">

-   glidefunction:get\_longitude\(u\_geo\_point\_field\)Returns the longitude value in the u\_geo\_point\_field.
-   glidefunction:get\_ longitude\(u\_numerical\_column\)Returns the longitude value in the u\_numerical\_column within \[-179,180\] range.
-   glidefunction:get\_longitude\('380.206458'\)Returns 20.206458 longitude value.

 Return type: Floating point number

</td></tr><tr><td>

greatest\(\)

</td><td id="gr-func-desc">

Takes two or more values as input and returns the greatest value of the list of arguments.

</td><td id="gr-func-ex">

glidefunction:greatest\(10,100,1000\) Returns 1000

Possible numeric return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

This function also works with date and string fields.

</td></tr><tr><td>

least\(\)

</td><td id="least-func-desc">

Takes two or more values as input and returns the lowest value of the list of arguments.

</td><td id="least-func-ex">

glidefunction:least\(10,100,1000\) Returns 10

Possible numeric return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

This function also works with date and string fields.

</td></tr><tr><td>

length\(\)

</td><td id="length-func-desc">

Takes a string field as input, calculates the field length in characters, and returns the results as a field value.

</td><td id="length-func-ex">

glidefunction:length\(short\_description\) Returns 37 if short\_description = "This application is performing a test".

Return type: Whole number

</td></tr><tr><td>

multiply\(\)

</td><td id="mult-func-desc">

Takes two number fields as input, performs the multiplication, and returns the results as a field value.This function also takes numerical values for either input. Place numerical values in single or double quotation marks.

</td><td id="mult-func-ex">

glidefunction:multiply\(u\_num1, u\_num2\) Returns 48 if num1 = 8 and num\_2 = 6.

Possible return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

</td></tr><tr><td>

position\(\)

</td><td id="pos-func-desc">

Takes two text fields or two text fields and a whole number as input. One or both of the text fields can also be strings.1.  Returns the position of the first occurrence of the string of the first text field in the second.
2.  If a whole number is specified, this function returns the position of the second text field after the position of the whole number.

 Returns 0 if the first text field is not present in the second \(after the position of the whole number if specified\).

</td><td id="pos-func-ex">

-   glidefunction:position\('e',short\_description\)

If the value of the short\_description field is "This computer is performing an upgrade", returns 12.

-   glidefunction:position\('e',short\_description,'14'\)

If the value of the short\_description field is "This computer is performing an upgrade", returns 19.


 Return type: Whole number

</td></tr><tr><td>

substring\(\)

</td><td id="subs-func-desc">

Takes a text field and two whole numbers as input. Returns the first instance of a string that starts at the position of the first whole number and is the length of the second.

</td><td id="subs-func-ex">

glidefunction:substring\(short\_description, '7', '2'\) If the value of the short\_description field is 'We're going to the store', returns 'go'.

Return type: Text

</td></tr><tr><td>

subtract\(\)

</td><td id="sub-func-desc">

Takes two number fields as input, subtracts the second from the first, and returns the result as a field value. This function also takes numerical values for either input. Place numerical values in single or double quotation marks.

</td><td id="sub-func-ex">

glidefunction:subtract\(u\_num1, u\_num2\) Returns 2 if num1 = 8 and num\_2 = 6.

Possible return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

</td></tr><tr><td>

to\_geopoint\(\)

</td><td id="to-geo-func-desc">

Takes latitude and longitude columns or numerical values and converts them to a geo point column.

</td><td id="to-geo-func-ex">

-   glidefunction:to\_geopoint\(u\_long\_column, u\_lat\_column\)

Converts the latitude and longitude columns into a single geo\_point column.

-   glidefunction:to\_geopoint\('80.206458','25.767242'\)

Returns a geo\_point field with the coordinates “\(80.206458, 25.767242\)”.


 Return type: Geo point

</td></tr></tbody>
</table>**Parent Topic:**[Field types](../../../administer/reference-pages/reference/r_FieldTypes.md)

## Create a function field to perform database functions

Create a field that displays the results of a database function, such as a mathematical operation, field length computation, or day of the week calculation. Test in a subproduction instance before deploying to a production instance.

### Before you begin

Role required: personalize\_dictionary or admin.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Click **New**.

3.  Select **Function field**.

4.  Fill in these fields on the form.

<table id="table_k2c_wsz_y1b_2"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table to which the function field is added.

</td></tr><tr><td>

Type

</td><td>

Species the type of field: string, number, date, and so on.

</td></tr><tr><td>

Column label

</td><td>

Defines the label for the column.

</td></tr><tr><td>

Column name

</td><td>

Defines the name of the column. Created automatically based on **Column label**.

</td></tr><tr><td>

Max length

</td><td>

Defines the maximum length of the return value.

</td></tr><tr><td>

Function field

</td><td>

If selected, creates a field that displays the results of a database function, such as a mathematical operation, field length computation, or day of the week calculation.Once the new function record is saved, you cannot clear the check box to make the field a regular field.

</td></tr><tr><td>

Function definition

</td><td>

Defines the function that the field performs.Starts with `glidefunction:`, followed by the operation to be performed \(for example, `concat`\), followed by function parameters. Constants must be enclosed in single quotes.

For example, the following function definition creates a field that shows the short description, followed by a space, followed by the caller name:

`glidefunction:concat(short_description, ' ', caller_id.name)`

**Note:** Function parameters support dot-walking. See [Dot-walking to data in related tables](https://www.servicenow.com/docs/access?context=c_DotWalking&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>5.  Click **Submit**.

    You return to the Dictionary Entry \[sys\_dictionary\] table.

6.  Navigate to the table to which you added the function field.

7.  Add the function field to the list.

    See [Configure items on forms or in lists using a list collector](https://www.servicenow.com/docs/access?context=t_UseSlushbuckets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).


### Result

Use the function field like any other field. For example, add it to a form, use it in a filter, or use it in the condition builder.

If the function definition is invalid, instead of the expected value you receive the message **Invalid function** if the function field is a string type field, or an empty value for other field types.

