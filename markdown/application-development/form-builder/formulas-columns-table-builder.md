---
title: Formulas for column values in Table Builder
description: You can use a predefined function and create a formula to calculate the value of a column without writing a script. Use a predefined function or create a nested formula by using the existing predefined functions to calculate the column value type.Use simple math functions to perform basic mathematical calculations on numeric value columns.Use string functions to reformat or perform calculations on string column values.Use date and time functions to calculate or reformat the date and time column values.Use logical functions to perform logical operations on column values.
locale: en-US
release: yokohama
product: Form Builder
classification: form-builder
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Field configuration in Table Builder, Table Builder reference, Table Builder, Builder library, Developing your application, Building applications]
---

# Formulas for column values in Table Builder

You can use a predefined function and create a formula to calculate the value of a column without writing a script. Use a predefined function or create a nested formula by using the existing predefined functions to calculate the column value type.

## Supported operators

The following comparison operators are supported only for number type values.

-   = \(Equal to\)
-   &lt;&gt; \(Not equal to\)
-   &gt; \(Greater than\)
-   &lt; \(Less than\)
-   &gt;= \(Greater than or equal to\)
-   &lt;= \(Less than or equal to\)

**Parent Topic:**[Field configuration in Table Builder](field-parameters.md)

## Simple math functions

Use simple math functions to perform basic mathematical calculations on numeric value columns.

### AVERAGE

Returns the average value of the arguments.

|Syntax|Input|Output|
|------|-----|------|
|AVERAGE\(argument 1, argument 2, … argument n\)|Numeric value, function call, or variable|Numeric value|

Examples:

-   Function: AVERAGE\(1,2,3\)

    The result is 2.

-   Formula: AVERAGE\(LENGTH\(first\_name\), LENGTH\(last\_name\)\)

    The result is the average value of the number of characters in the first\_name column and last\_name column.


### DIVIDE

Returns the final quotient value after consecutively dividing the first argument with the next argument until the function reaches the last argument.

|Syntax|Input|Output|
|------|-----|------|
|DIVIDE\(argument 1, argument 2 … argument n\)|Numeric value, function call, or variable|Numeric value|

Examples:

-   Function: DIVIDE\(10,20, 0.25, 10\)

    The result is 0.2.

-   Formula: DIVIDE\(LENGTH\(full\_name\),2\)

    The result is the number of characters in the full\_name column divided by 2.


### INDEXMATCH

Retrieves the first not null value from the specified set of arguments.

<table id="table_lb3_qfn_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

INDEXMATCH\(argument 1, argument 2 , … argument n\)

</td><td>

String, numeric value, function call, or variable.

</td><td>

Numeric value

</td></tr></tbody>
</table>Example:

Function: INDEXMATCH\(""," ",2,"string"\)

The result is 2.

### MAX

Returns the highest value in the specified arguments.

|Syntax|Input|Output|
|------|-----|------|
|MAX\(argument 1, argument 2, … argument n\)|Numeric value, function call, or variable|Numeric value|

Examples:

-   Function: MAX\(1, -5, 20, 6\)

    The result is 20.

-   Formula: MAX\(LENGTH\(first\_name\), LENGTH\(last\_name\)\)

    The result is the number of characters in the first\_name column or last\_name column whichever is the highest.


### MIN

Returns the lowest value in the specified arguments.

|Syntax|Input|Output|
|------|-----|------|
|MIN\(argument 1, argument 2, … argument n\)|Numeric value, function call, or variable|Numeric value|

Examples:

-   Function: MIN\(1, -5, 20, 6\)

    The result is -5.

-   Formula: MIN\(LENGTH\(first\_name\), LENGTH\(last\_name\)\)

    The result is the number of characters in the first\_name column or last\_name column whichever is the lowest.


### MULTIPLY

Returns the total multiplied value of the arguments.

|Syntax|Input|Output|
|------|-----|------|
|MULTIPLY \(argument 1, argument 2, … argument n\)|Numeric value, function call, or variable|Numeric value|

Examples:

-   Function: MULTIPLY\(12, 4\)

    The result is 48.

-   Formula: MULTIPLY\(order, 2\)

    The result is the order column value multiplied by 2.


### POWER

Returns the result of the base value raised to the power of the exponent value.

<table id="table_e35_mkn_ytb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

POWER\(argument 1, argument 2\)

</td><td>

argument 1 is base and argument 2 is exponent.-   base: number or variable
-   exponent: number or variable

</td><td>

Number

</td></tr></tbody>
</table>Examples:

-   Function: POWER\(3,2\)

    The result is 9.

-   Formula: POWER\(LENGTH\(full\_name\),2\)

    The result is the number of characters in the full\_name column to the power of 2.


### SUBTRACT

Returns the result value after consecutively subtracting the next available argument from the earlier argument until the function reaches last argument.

|Syntax|Input|Output|
|------|-----|------|
|SUBTRACT\(argument 1, argument 2 … argument n\)|Numeric value, function call, or variable|Numeric value|

Examples:

-   Function: SUBTRACT\(1.15, 0.02, 0.45, -0.85\)

    The result is 1.53.

-   Formula: SUBTRACT\(LENGTH\(full\_name\), LENGTH\(first\_name\)\)

    The result is the number of characters from the full\_name column minus the number of characters from the first\_name column.


### SUM

Returns the sum of all the arguments.

|Syntax|Input|Output|
|------|-----|------|
|SUM\(argument 1,argument 2, ... argument n\)|Numeric value, function call, or variable|Numeric value|

Examples:

-   Function: SUM\(0.03, -0.02, 1\)

    The result is 1.01.

-   Formula: SUM\(LENGTH\(first\_name\), LENGTH\(last\_name\)\)

    The result is the total number of characters in the first\_name column plus the total number of characters in the last\_name column.


### COUNTIF

Returns the number of arguments that match the specified criteria within the specified set of arguments.

<table id="table_p1x_yd4_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

COUNTIF\(argument 1, argument 2, argument n-1, criteria\)

</td><td>

-   argument 1 … argument n: String, numeric value, function call, or variable.
-   criteria: Criteria that evaluates the specified set of arguments. String, numeric value, function call, or variable.

</td><td>

Numeric value

</td></tr></tbody>
</table>Example:

Function: COUNTIF\(2,3,2,"string",2\)

The result is 2.

### MODE

Returns the most frequently repeating value in the specified set of arguments.

|Syntax|Input|Output|
|------|-----|------|
|MODE\(argument 1,argument 2, ... argument n\)|Numeric value, function call, or variable|Numeric value|

Example:

Function: MODE\(1, 2, 2, 3, 3, 3\)

The result is 3.

## String functions

Use string functions to reformat or perform calculations on string column values.

### CONCATENATE

Joins one or more input strings into a single string.

|Syntax|Input|Output|
|------|-----|------|
|CONCATENATE\(string 1, string 2, … string n\)|String, function call, or variable|String|

Examples:

-   Function: CONCATENATE\(first\_name, ".", last\_name, "@", LOWERCASE\(example\), ".com"\)

    The result is the concatenated value &lt;first\_name\_value&gt;.&lt;last\_name\_value&gt;@example.com. In this example, &lt;first\_name\_value&gt; and &lt;last\_name\_value&gt; are placeholders.

-   Function: CONCATENATE\(first\_name, " ", last\_name\)

    The result is the concatenated string of first\_name column value and last\_name column value separated by a white space.


### ISBLANK

Finds white spaces or blank values in the string and returns true if there are any.

|Syntax|Input|Output|
|------|-----|------|
|ISBLANK\(argument\)|String or value|True or false|

Examples:

-   Function: ISBLANK\(“example\_string”\)

    The result is false.

-   Function: ISBLANK\(full\_name\)

    The result is true only when there are empty spaces in the full\_name column. Otherwise, the result is false.


### LENGTH

Returns the total number of characters in the input string.

|Syntax|Input|Output|
|------|-----|------|
|LENGTH\(argument\)|String value, function call, or variable|Numeric value|

Examples:

-   Function: LENGTH\("example\_string"\)

    The result is 14.

-   Function: LENGTH\(full\_name\)

    The result is the total number of characters in the full\_name column value.


### LOWERCASE

Converts the input string to all lowercase characters.

|Syntax|Input|Output|
|------|-----|------|
|LOWERCASE\(argument\)|String, function call, or variable|String in lowercase|

Examples:

-   Function: LOWERCASE\(“ExamPle inpuT stRing”\)

    The result is example input string.

-   Function: LOWERCASE\(sys\_created\_by\)

    The result is the lower case string of the sys\_created\_by column value.


### REPLACE

Replaces the characters in the source string with the characters in the target string.

<table id="table_efv_2hd_g5b"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

REPLACE\(source\_string, target\_string, replacement\_string\)

</td><td>

-   source\_string: String, function call, or variable
-   target\_string: String, function call, or variable
-   replacement\_string: String, function call, or variable

</td><td>

String

</td></tr></tbody>
</table>Examples:

-   Function: REPLACE\(“Pepperoni Pizza”, “Pepperoni”, “Cheese”\)

    The result string is Cheese Pizza.

-   Function: REPLACE\("abe.tuter@example.com", "example", company\_name\)

    The result string is abe.tuter@&lt;company\_name&gt;.com. In this example, &lt;company\_name&gt;is a place holder.


### TITLECASE

Converts the input string to all title case characters.

|Syntax|Input|Output|
|------|-----|------|
|TITLECASE\(argument\)|String, function call, or variable|String in title case|

Examples:

-   Function: TITLECASE\("example string"\)

    The result is Example String.

-   Function: TITLECASE\(full\_name\)

    The result is the full name column value in the title case.


### UPPERCASE

Converts the input string to all uppercase characters.

|Syntax|Input|Output|
|------|-----|------|
|UPPERCASE\(argument\)|String value, function call, or variable|String in uppercase|

Examples:

-   Function: UPPERCASE\("eXamPle sTring"\)

    The result is EXAMPLE STRING.

-   Function: UPPERCASE\(state\)

    The result is the State column value in upper case.


### FIND

Searches for the first occurrence of a substring within a string and returns the position of the first occurrence.

**Note:** This function is case sensitive.

<table id="table_vvp_1hn_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

FIND\(search\_string, source\_string, from\_index\)

</td><td>

-   search\_string: Substring, function call, or variable.
-   source\_string: Main string, function call, or variable.
-   from\_index: Index position in the main string from where the search should start. Numeric value, function call, or variable.

</td><td>

Numeric value \(integer\). When the substring does not exist in the main string, -1 is returned.

</td></tr></tbody>
</table>Example:

Function: FIND\("morning", "Good morning"\)

The result is 5.

### SEARCH

Searches for a substring within a string and returns the position of the first occurrence of the substring.

**Note:** This function is case insensitive.

<table id="table_udg_zc4_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

SEARCH\(search\_string, source\_string, from\_index\)

</td><td>

-   search\_string: Substring, function call, or variable.
-   source\_string: Main string, function call, or variable.
-   from\_index: Index position in the main string from where the search should start. Numeric value, function call, or variable.

</td><td>

Numeric value \(integer\). When the substring does not exist in the main string, -1 is returned.

</td></tr></tbody>
</table>Examples:

-   SEARCH\("Morning", "Good morning"\)

    The result is 5.

-   SEARCH\("World","Hello world!"\)

    The result is -1.


### SUBSTRING

Retrieves a substring from a string at the specified index position and for the specified length.

<table id="table_jjp_wb4_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

SUBSTRING\(source\_string, start\_index, length\)

</td><td>

-   source\_string: String, function call, or variable.
-   start\_index: Position in the string from where the substring is extracted. Numeric value, function call, or variable.
-   length: Length of the substring that should be extracted.

</td><td>

String

</td></tr></tbody>
</table>Example:

SUBSTRING\("Hello, Good Morning", 7, 4\)

The result substring is 'Good'.

## Date and time functions

Use date and time functions to calculate or reformat the date and time column values.

### NOW

Returns the current date and time of the instance in ISO format \(YYYY-MM-DD hh:mm:ss\).

|Syntax|Input|Output|
|------|-----|------|
|NOW\(\)|No arguments are required for this function|ISO format of current date and time|

Example:

Function: NOW\(\)

The result is the current date and time in ISO format.

### TODAY

Returns the current date with time offset to start of the day in ISO format in UTC time zone.

|Syntax|Input|Output|
|------|-----|------|
|TODAY\(\)|No arguments are required for this function|Current date with time offset to start of the day in ISO format.|

Example:

Function: TODAY\(\)

The result is the current date and start time of the day in ISO format.

### TIMEDIFF

Evaluates the time duration difference between two dates.

|Syntax|Input|Output|
|------|-----|------|
|TIMEDIFF\(argument1, argument2\)|Date in ISO format \(YYYY-MM-DD hh:mm:ss\) as string or variable|Duration|

Examples:

-   Function: TIMEDIFF\("2021-05-02 9:10:12", "2021-04-07 6:2:23"\)

    The result is 25 03:07:49.

-   Formula: TIMEDIFF\(sys\_created\_on, NOW\(\)\)

    The result is the time duration difference between the sys\_created\_on date and the current date of the system.


### DATEDIF

Evaluates the difference between the two dates in days, months, or years.

<table id="table_s4h_33n_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

DATEDIF\(start\_date, end\_date, date\_difference\_unit\)

</td><td>

-   start\_date: Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string or variable.
-   end\_date: Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string or variable.
-   date\_difference\_unit: Character String and either "Y","M", or "D" in lowercase or uppercase. Default is "D".

</td><td>

Numeric duration value based on the specified date difference unit.

</td></tr></tbody>
</table>Example:

Function: DATEDIF\("2021-05-02 9:10:12", "2021-05-05 6:2:23 ","d"\)

The result is 3.

### DATE

Creates a date from the specified individual year, month, and day values. The created date is in Coordinated Universal Time \(UTC\) time zone.

<table id="table_ek1_jdn_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

DATE\(year,month,day\)

</td><td>

-   year: Numeric value, variable or function.
-   month: Numeric value, variable or function.
-   day: Numeric value, variable or function.

</td><td>

Date in ISO format \(YYYY-MM-DD hh:mm:ss\)

</td></tr></tbody>
</table>Example:

Function: DATE\(2021,5,2\)

The result is 2021-05-02 00:00:00.

### DAY

Retrieves the numerical day component from the specified date.

|Syntax|Input|Output|
|------|-----|------|
|DAY\(date\)|Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string, variable, or function.|Numeric value \(integer\). The values range from 1 through 31.|

Examples:

-   Function: DAY\("2021-05-029:10:12"\)

    The result is 2.

-   Function: DAY\(NOW\(\)\)

    The result will be the day component of the current date and time.


### MONTH

Retrieves the numerical month component from the specified date.

|Syntax|Input|Output|
|------|-----|------|
|MONTH\(date\)|date: Date in ISO format \(YYYY-MM-DD or YYYY-MM- DD hh:mm:ss\) as string or variable.|Numeric value \(integer\). The values range from 1\(January\) through 12\(December\).|

Examples:

-   Function: MONTH\("2021-05-02 9:10:12"\)

    The result is 5.

-   Function: DAY\(NOW\(\)\)

    The result will be the month component of the current date and time.


### YEAR

Retrieves the year component from the specified date.

|Syntax|Input|Output|
|------|-----|------|
|YEAR\(date\)|Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string, variable, or function.|Numeric value \(integer\)|

Examples:

-   Function: YEAR\("2021-05-02 9:10:12"\)

    The result is 2021.

-   Function: YEAR\(NOW\(\)\)

    The result will be the year component of the current date and time.


### WEEKDAY

Returns the numerical day of the week for the specified date. The day range is 1 \(Sunday\) through 7 \(Saturday\).

|Syntax|Input|Output|
|------|-----|------|
|WEEKDAY\(date\)|date: Date in ISO format \(YYYY-MM-DD or YYYY-MM- DD hh:mm:ss\) as string or variable.|Numeric value \(integer\)|

Example:

Function: WEEKDAY\("2021-05-02 9:10:12"\)

The result is 1.

### TEXT

Retrieves the specific date components in a date in string format.

<table id="table_znr_d1n_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

TEXT\(date, format\_text\)

</td><td>

-   date: Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string, variable.
-   format\_text: Date components as string or variable that are to be extracted.

</td><td>

String

</td></tr></tbody>
</table>Example:

TEXT\("2022-08-17 9:10:12","yyyy-MM"\)

The result is 2022-08.

### DATEVALUE

Converts a date in text format into a date in ISO format.

<table id="table_opb_d44_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

DATEVALUE\(date\_text\)

</td><td>

date\_text: Date stored as text must be in YYYY-MM-DD format.

</td><td>

Date in ISO format \(YYYY-MM-DD hh:mm:ss\) as string.

</td></tr></tbody>
</table>Example:

Function: DATEVALUE\("2021-05-02"\)

The result is 2021-05-02 00:00:00.

### WORKDAY

Returns the nearest working day for the specified input date by excluding the specified holidays and weekends before or after the specified n number of days.

<table id="table_zyw_b2n_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

WORKDAY\(start\_date, days, holiday 1,holiday 2, ..., holiday n\)

</td><td>

-   start\_date: Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string or variable.
-   days: Number of days as a numeric value, string, or function.
-   holiday 1...holiday n \(Optional\): Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string or variable.

</td><td>

Date in ISO format \(YYYY-MM-DD hh:mm:ss\) as string.

</td></tr></tbody>
</table>Example:

Function: WORKDAY\("2022-08-17 9:10:12",2\)

The result is 2022-08-19 00:00:00.

### NETWORKDAYS

Calculates the number of working days between two dates by excluding weekends and specified holiday dates. Number of working days includes the start date and end date.

<table id="table_opy_qf4_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

NETWORKDAYS\(start\_date,end\_date,holiday 1,holiday 2, ... holiday n\)

</td><td>

-   start\_date: Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string or variable.
-   end\_date: Date in ISO format \(YYYY-MM-DD or YYYY-MM-DD hh:mm:ss\) as string or variable.
-   holiday 1,holiday 2, ... holiday n \(optional\) : List of holidays that should be excluded while calculating working days.

</td><td>

Numeric value \(integer\)

</td></tr></tbody>
</table>Example:

Function: NETWORKDAYS\("2022-08-17 20:10:12","2022-08-19 9: 10:12"\)

The result is 3.

## Logical functions

Use logical functions to perform logical operations on column values.

### AND

Performs a logical AND operation on the arguments.

|Syntax|Input|Output|
|------|-----|------|
|AND\(argument 1, argument 2\)|String, function call, or variable|True or false|

Examples:

-   Function: AND\(2&gt;3, 4&lt;5\)

    The result is false.

-   Formula: AND\(LENGTH\(sys\_created\_by\)&gt;25, LENGTH\(sys\_updated\_by\)&gt;25\)

    The result is true only when the number of characters in both the sys\_created\_by and sys\_updated\_by columns are greater than 25. Otherwise, the result is false.


### IF

Executes the specified statements based on the Boolean output of the conditional expression.

<table id="table_pt3_zgn_ytb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

IF\(&lt;conditional\_expression&gt;, &lt;do\_this\_when\_true&gt;, &lt;do this\_when\_false&gt;\)

</td><td>

-   conditional\_expression: Logical conditional expression, function call, or variable

**Note:** Logical comparison of strings is not supported in the conditional expression.

-   do\_this\_when\_true: String, numeric value, function call, or variable that is returned when the condition evaluates to true
-   do\_this\_when\_false: String, numeric value, function call, or variable that is returned when the condition evaluates to false

</td><td>

String, numeric value, function call, or variable based on the Boolean output of the conditional expression.

</td></tr></tbody>
</table>Examples:

-   Function: IF\(number\_of\_incidents &gt;= 5, "High", "Medium"\)

    If the number of incidents is greater than 5, the string ‘High’ is returned. In other cases, the string ‘Medium’ is returned.

-   Function: IF\(LENGTH\(full\_name\) &gt; 100, "Number of characters exceed the limit", "Number of characters within the limit"\)

    If the number of characters for the full\_name column is above 100, the string 'Number of characters exceed the limit' is returned. Otherwise, the string 'Number of characters within the limit' is returned.


### OR

Performs logical OR operation on the arguments.

|Syntax|Input|Output|
|------|-----|------|
|OR\(argument 1, argument 2\)|Conditional expression, function call, or variable|True or false|

Examples:

-   Function: OR\(2&gt;3,4&lt;5\)

    The result is true.

-   Formula: OR\(LENGTH\(first\_name\)&gt;25, LENGTH\(last\_name\)&lt;25\)

    The result is true when the number of characters in the first\_name column is greater than 25 or the number characters in the last\_name column is less than 25. Otherwise, the result is false.


### IFERROR

Evaluates expression 1 and returns the expression 1 value when there are no errors in the expression 1. When an error occurs while evaluating expression 1, expression 2 is evaluated and expression 2 value is returned.

<table id="table_wgl_rln_dwb"><thead><tr><th>

Syntax

</th><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

IFERROR\(expression 1, expression 2\)

</td><td>

-   expression 1: Arithmetic, Logical expression, function call, String, numeric value or variable.
-   expression 2: Arithmetic, Logical expression, function call, String, numeric value or variable.

</td><td>

Result of expression 1 when there are no errors in expression 1. Otherwise, result of expression 2.

</td></tr></tbody>
</table>Example:

Function: IFERROR\( MULTIPLY\(snr\_factor, signal\), MULTIPLY\( default\_factor, signal\)\)

If the snr\_factor value is a valid number, the multiplied value of snr\_factor with signal is returned. If the snr\_factor value is not a valid number, the multiplied value of default\_factor value with signal is returned.

