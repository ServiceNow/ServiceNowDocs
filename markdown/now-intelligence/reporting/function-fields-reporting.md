---
title: Report on function fields
description: While regular fields store a value in the database, a function field displays the results of a database query. The function field generates the value based on computations of other fields and constants. You can use these fields in reports and data visualizations as you would other fields.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report on function fields

While regular fields store a value in the database, a function field displays the results of a database query. The function field generates the value based on computations of other fields and constants. You can use these fields in reports and data visualizations as you would other fields.

The responsibility for creating, editing, and deactivating function fields belongs to the user with the role function\_field\_admin. On upgrade, no user has this role. An admin must give this role to a non-admin user. See [Create a role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateARole.md).

Learn about function fields here: [Function field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/platform-support-functions.md).

## Function field operations

Function fields can perform the following operations using the glidefunction:&lt;operation&gt; syntax.

**Note:** Specify constants in single or double quotes. The examples for the concat\(\), dayofweek\(\), position\(\), and substring\(\) operations show the use of constants in function fields.

<table id="table_mdb_1zs_dbb"><thead><tr><th>

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

subtract\(\)

</td><td id="sub-func-desc">

Takes two number fields as input, subtracts the second from the first, and returns the result as a field value. This function also takes numerical values for either input. Place numerical values in single or double quotation marks.

</td><td id="sub-func-ex">

glidefunction:subtract\(u\_num1, u\_num2\) Returns 2 if num1 = 8 and num\_2 = 6.

Possible return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

</td></tr><tr><td>

multiply\(\)

</td><td id="mult-func-desc">

Takes two number fields as input, performs the multiplication, and returns the results as a field value.This function also takes numerical values for either input. Place numerical values in single or double quotation marks.

</td><td id="mult-func-ex">

glidefunction:multiply\(u\_num1, u\_num2\) Returns 48 if num1 = 8 and num\_2 = 6.

Possible return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

</td></tr><tr><td>

divide\(\)

</td><td id="div-func-desc">

Takes two number fields as input, divides the first by the second, and returns the result as a field value. This function also takes numerical values for either input. Place numerical values in single or double quotation marks.

</td><td id="div-func-ex">

glidefunction:divide\(u\_num2,u\_num1\) Returns 5 if num2 = 10 and num1 = 2.

Possible return types: Decimal, Floating Point Number, Large Whole Number, Whole Number

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

length\(\)

</td><td id="length-func-desc">

Takes a string field as input, calculates the field length in characters, and returns the results as a field value.

</td><td id="length-func-ex">

glidefunction:length\(short\_description\) Returns 37 if short\_description = "This application is performing a test".

Return type: Whole number

</td></tr><tr><td>

coalesce\(\)

</td><td id="coal-func-desc">

Takes any number of comma-separated fields as input and returns the first non-empty value.

</td><td id="coal-func-ex">

glidefunction:coalesce\(closed\_at, resolved\_at, sys\_updated\_on\) If the value of closed\_at is empty, the function returns the value of resolved\_at. If the value of resolved\_at is also empty, the function returns the value of sys\_updated\_on.

Return type: Text

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

</td></tr></tbody>
</table>-   **[Configuring function fields](../task/configure-function-fields.md)**  
You can configure up to 20 active function fields per table using the Report Designer. When you configure a function field on a table, you can group or stack by the results of the function calculation.
-   **[Create a function field](../task/create-function-field.md)**  
Create a function field to be able to group and stack a report by the results of the field's calculation.
-   **[Edit a function field](../task/edit-function-field.md)**  
The user who created a function field or a user with the admin or function\_field\_admin role can edit the definition of a saved function field. It isn’t possible to edit the label or the return type of a saved function field.
-   **[Deactivate a function field](../task/delete-function-field.md)**  
The user who created a function field or a user with the admin role can deactivate it. If a table already has 20 function fields, you must deactivate one or more existing fields before creating another.
-   **[Delete a function field](../task/delete-a-function-field-fg.md)**  
A user with the admin role can delete a function field from its table. Deleting a function field is useful if you want to create a function field with the same name as one that exists on that table.
-   **[Disable function field creation](../task/disable-function-field-creation.md)**  
Configure a system property to remove the ability to create function fields in the Report Designer.

**Parent Topic:**[Advanced Core UI reporting topics](c_AdvancedReporting.md)

