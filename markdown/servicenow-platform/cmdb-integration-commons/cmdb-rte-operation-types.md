---
title: RTE operation types included within the Integration Commons for CMDB app
description: The Robust Transform Engine \(RTE\) operation types are common operation methods for use in ETL without having to write your own complex data transformations.
locale: en-US
release: xanadu
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Integration Commons for CMDB, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# RTE operation types included within the Integration Commons for CMDB app

The Robust Transform Engine \(RTE\) operation types are common operation methods for use in ETL without having to write your own complex data transformations.

The following operation types are available in the Integration Commons for CMDB app.

## Concatenation

Combines the values from input fields into a single string, joining them on the optional **joining\_string** field.

<table id="table_bqc_ynv_qwb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Concatenation Operation \[sys\_rte\_eb\_concat\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_fields** Input is a set of fields and constants.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the combined value of the provided fields as a single string.

</td></tr><tr><td>

Additional fields

</td><td>

**joining\_string** \(optional\)

</td></tr></tbody>
</table>|Input|joining\_string|Result|
|-----|---------------|------|
|"input\_1", "input\_2", "input\_3"|", "|"input\_1, input\_2, input\_3"|

## Convert to Boolean

Converts the incoming value to a Boolean.

<table id="table_jfy_3k1_nkb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Convert to Boolean Operation \[sys\_rte\_eb\_to\_boolean\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field** Input is a string value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is `true` when input is `true` or `1`, otherwise output is `false`. \(case insensitive\)

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|input\_1|false|
|true|true|
|1|true|
|0|false|
|11|false|

## Convert to Date

Attempts to convert the incoming value to a GlideDateTime value by applying the date\_format to the incoming value.

<table id="table_ekx_zl1_nkb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Convert to Date Operation \[sys\_rte\_eb\_to\_date\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field** Input is a data timestamp value with date format.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the date timestamp in the specified date format. Attempts to directly convert using GlideDateTime if the date\_format is incorrect. Returns an empty value if unable to parse at all.

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|"2018/09/20 11:21:00 AM EST" with date\_format "yyyy/MM/dd hh:mm:ss a z"|"2018-09-20 16:21:00"|
|"2018/09/20 01:21:00 PM EST" with date\_format "yyyy/MM/dd hh:mm:ss a z"|"2018-09-20 18:21:00"|
|"09/20/18" with date\_format "yyyy/MM/dd hh:mm:ss a z"|""0018-09-20 00:00:0"|

## Convert to Numeric

Converts the incoming value to a number.

<table id="table_yrv_lxm_4yb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Convert to Numeric Operation \[sys\_rte\_eb\_to\_numeric\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field** Input is a value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is a numeric value. If the input value is non-numeric the output is empty.

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|input\_1|null|
|1.23|1.23|
|1.00|1|
|two|null|

## Copy

Copies the value of the source field to all the target fields.

<table id="table_qzx_km1_nkb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Copy Operation \[sys\_rte\_eb\_copy\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field** Input is a value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_fields** Output is the copied source field value.

</td></tr><tr><td>

Additional field

</td><td>

**overwrite\_existing\_value** \(optional, Boolean\): If `true`, then the values of the target fields are replaced. Otherwise, any non-empty value isn’t overwritten.

</td></tr></tbody>
</table>## Extract First Numeric

Sets the target field as the first numeric value found in the source field.

<table id="table_bnb_bn1_nkb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Extract Numeric Operation \[sys\_rte\_eb\_extract\_numeric\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field** Input is a value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the numeric value found in the input.

</td></tr><tr><td>

Additional fields

</td><td>

-   **decimal\_places** \(optional, number\) : Forces the output to have a specified number of decimal places.
-   **remainder\_target\_field** \(optional, reference to field\): Set to the trimmed remainder of the source field, after removing the first numeric value.

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|100 mb|100|
|100.123 mb|100.123|
|100.123 mb with **decimal\_places**=2|100.12|
|100 mb with **decimal\_places**=2|100.00|
|100 mb with **remainder\_target\_field**|mb|

## Glide Lookup Operation

Performs a lookup in the database on the target table specified in the **target\_table** field.

<table id="table_o5n_fl1_nkb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Glide Lookup Operation \[sys\_rte\_eb\_glide\_lookup\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_fields** The database table for lookup.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_fields**The resulting data based on the lookup operation.

</td></tr><tr><td>

Additional fields

</td><td>

-   **target\_table**
-   **glide\_matching\_fields** \(string\): Comma-separated list of column names in the target table. For each input field in source\_sys\_rte\_eb\_fields, there must be an equal number of values in glide\_matching\_fields.
-   **glide\_target\_fields** \(string\): Comma-separated list of column names in the target table. For each target field in target\_sys\_rte\_eb\_fields, there must be an equal number of values in glide\_target\_fields.

</td></tr></tbody>
</table><table id="table_vwc_g51_bmb"><thead><tr><th>

Input

</th><th>

Result

</th></tr></thead><tbody><tr><td>

-   Input Field 1: 100 South Charles Street, Baltimore
-   Input Field 2: MD
-   Target Table: Location \(cmn\_location\)
-   Glide Matching Fields: street,state
-   Glide Target Fields: sys\_id

</td><td>

Output Field 1: 25ab9c4d0a0a0bb300f7dabdc0ca7c1c

</td></tr></tbody>
</table>## Multiple Input Script 

Runs a script with multiple inputs setting the **target\_sys\_rte\_eb\_field** field as the output for that script.

<table id="table_hty_g2d_jmb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Multiple Input Script Operation \[sys\_rte\_eb\_multi\_in\_script\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_fields** Input is a script.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the result of the input script.

</td></tr><tr><td>

Additional Fields

</td><td>

-   **script** \(script\)
-   **use\_unique\_input\_sets**\(Boolean\): When `true`, only unique input values are included in the data batch for IRE processing. Otherwise, all input object’s field values are included.

</td></tr></tbody>
</table>Example for using **use\_unique\_input\_sets**, with a script function that takes `record_type` and `operating_system` as input and returns `record_with_os`:

|Record|record\_type|operating\_system|
|------|------------|-----------------|
|1|computer|Windows XP|
|2|computer|Linux|
|3|computer|Windows XP|

If use\_unique\_inputs\_sets is set to `true`, then the script processes only two values \(`computer` + `Windows XP` and `computer` + `Linux`\). If `use_unique_inputs_sets` is set to `false`, then each of the three values is individually processed \(`computer` + `Windows XP`, `computer` + `Linux`, and `computer` + `Windows XP`\).

Sample script:

```
(function(batch, output) { 
                for (var i = 0; i < batch.length; i++) { 
                        // batch[i] is the unique set of inputs/individual record 
                        // batch[i].<field> gives access to the field value 
                        var in0 = gs.nil(batch[i].record_type) ? '' : batch[i].record_type;
                        var in1 = gs.nil(batch[i].operating_system) ? '' : batch[i].operating_system;
                        // output[i] is the output for the specific combination of inputs/individual record 
                        output[i] = in0 + "_" + in1; 
                    } 
                } 
            })(batch, output);
```

## Multiple Input/Output Script

Runs a script with multiple inputs setting the target fields specified in the **target\_sys\_rte\_eb\_fields** field as the multiple outputs for that script.

<table id="table_tdl_gq1_d1c"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Multiple Input/Output Script Operation \[sys\_rte\_eb\_multiple\_input\_output\_script\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_fields** Input is a script.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_fields** Output is the result of the input script.

</td></tr><tr><td>

Additional Fields

</td><td>

**script** \(script\)

</td></tr></tbody>
</table>Sample script:

```
(function(batch, output) { 
                for (var i = 0; i < batch.length; i++) { 
                        var userId = (batch[i].user_id);
                        var userIdParts = userId.split(".");
                        output[i].first_name = userIdParts[0]; 
                        output[i].last_name = userIdParts[1];
                    } 
                } 
            })(batch, output);
```

## Regex Replace 

Replaces each substring of the input string that matches the regular expression pattern specified in the **match\_regex** field with the string specified in the **replacement\_regex** field.

<table id="table_pyv_h41_nkb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Regular Expression Replace Operation \[sys\_rte\_eb\_regex\_replace\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field** Input is a string value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the replaced string.

</td></tr><tr><td>

Additional fields

</td><td>

-   **match\_regex** \(string, regular expression\)
-   **replacement\_regex** \(string\) 

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|"String&amp;With\(Special\)$Characters" with match\_regex="\[^0-9a-zA-Z\]+" and replacement\_regex=" "|"String With Special Characters"|

## Replace 

Replaces each substring of the input string that matches the string specified in the **match\_string** field with the string specified in the **replacement\_string** field.

<table id="table_alq_54v_c1c"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Replace Operation \[sys\_rte\_eb\_replace\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field**Input is a string value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the replaced string.

</td></tr><tr><td>

Additional fields

</td><td>

-   **match\_string** \(string\)
-   **replacement\_string** \(string\)

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|"Original String" with match\_string = "Original" and replacement\_string= "Replacement"|"Replacement String"|

## Round Numeric

Rounds off the input numeric value to the nearest whole number.  Non-numbers are truncated.

<table id="table_fm5_fpv_c1c"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Round Numeric Operation \[sys\_rte\_eb\_round\_numeric\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field**Input is a numeric value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is a whole number.

</td></tr><tr><td>

Additional fields

</td><td>

-   **match\_string** \(string\)
-   **replacement\_string** \(string\)

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|"1.5"|"2"|
|"1.4"|"1"|
|"i’m a string"|"" |

## Script Operation

Runs a script with an input and sets the **target\_sys\_rte\_eb\_field** field as the output for that script.

**Note:** The Script operation type has been largely superseded by the Multi Input Script Operation and is included for backwards compatibility with the existing configurations. 

<table id="table_fdp_lpv_c1c"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Script Operation \[sys\_rte\_eb\_script\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field**Input is a script.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the result of the input script.

</td></tr><tr><td>

Additional fields

</td><td>

-   **script**\(script\)
-   **use\_unique\_input\_sets** \(Boolean\): When `true`, only unique input values are included in the data batch for IRE processing. Otherwise, all input object’s field values are included. For an example and for more details, see the Multiple Input Script transform.

</td></tr></tbody>
</table>The source field is included in the ‘batch’ variable as the JavaScript field ‘input’.

```
(function(batch, output) { 
                for (var i = 0; i < batch.length; i++) { 
                        // batch[i] is the unique set of inputs/individual record 
                        // batch[i].input gives access to the field value 
                        var in0 = gs.nil(batch[i].input) ? '' : batch[i].input; 
                        // output[i] is the output for the specific combination of inputs/individual record 
                        output[i] = in0 + " modified by script"; 
                    } 
                } 
            })(batch, output); 
```

Example:

```
/* Example Script
 (function(batch, output) {
     for (var i = 0; i < batch.length; i++) {
         //step1: access the input variables
         var a = batch[i].input; //Value of the source field.
 
         //step2: Your script/code goes here.
         var b = a + 1;
         //step3: set the output for each elements
         output[i] = b;
     }
 })(batch, output);
*/ 
```

## Set 

Sets the **target\_sys\_rte\_eb\_field** field value to the string provided in the **set\_value** field.

<table id="table_pcx_ypv_c1c"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Set Operation \[sys\_rte\_eb\_set\_operation\]

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the value associated with the **set\_value** field.

</td></tr><tr><td>

Additional fields

</td><td>

-   **set\_value** \(string\)
-   **overwrite\_existing\_value** \(optional, Boolean\) : When true, the current value of the target field is overwritten. Otherwise, a non-empty value isn't replaced.

</td></tr></tbody>
</table>## Set Min/Max

Sets the target field to either the maximum or minimum of the values from all input fields.

<table id="table_pzz_241_nkb"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Min/Max Operation \[sys\_rte\_eb\_min\_max\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_fields** Input is a set of values.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the maximum or minimum value based on the **min\_max** value.

</td></tr><tr><td>

Additional fields

</td><td>

-   **data\_type** \(choice list with values as STRING, NUMERIC, and DATE\)
-   **min\_max** \(choice list with values as MIN and MAX\) 

</td></tr></tbody>
</table>|Input|Output|
|-----|------|
|"2", "-1", "0"|2|
|"a", "b"|c|
|"2", "-1", "0"|-1|
|"a", "b"|a|

## Split 

Splits the string included in the **source\_sys\_rte\_eb\_field** input value at the separator specified in the **splitting\_string** field and assigns the resulting array of strings to the **target\_sys\_rte\_eb\_field** field, in order.

<table id="table_mlh_2qv_c1c"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Split Operation \[sys\_rte\_eb\_split\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field**Input is a string value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_fields** Output is list of substrings.

</td></tr><tr><td>

Additional fields

</td><td>

**splitting\_string** \(string\) 

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|"value1\|\|value2\|\|value3", splitting\_string:"\|\|" with target\_sys\_rte\_eb\_fields \{target1,target2,target3\}|target1 : value1, target2 : value2, target3 : value3  |
|"value1\|\|value2\|\|value3", splitting\_string:"\|\|" with target\_sys\_rte\_eb\_fields \{target1\}|target1 : value1 |
|"value1", splitting\_string:"\|\|" with target\_sys\_rte\_eb\_fields \{target1,target2,target3\}|target1 : value1, target2 : &lt;null&gt;, target3 : &lt;null&gt;|

## Trim 

Removes any whitespaces at the beginning and at the end of the string included in the **source\_sys\_rte\_eb\_field** input value and assigns the result to the **target\_sys\_rte\_eb\_field** field.  This transform is equivalent to the Java String trim\(\) Method.

<table id="table_csp_4qv_c1c"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Trim Operation \[sys\_rte\_eb\_trim\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field**Input is a string value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the input string value but without any leading and trailing spaces.

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|" value 1 "|"value 1"|

## Uppercase

Changes all characters of the **source\_sys\_rte\_eb\_field** input value to upper case and assigns the result to the **target\_sys\_rte\_eb\_field** field.

<table id="table_ewd_tqv_c1c"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Upper Case Operation \[sys\_rte\_eb\_upper\_case\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field**Input is a string value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the upper case string value.

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|"value1"|"VALUE1"|

## Uppercase Trim 

Combines both the Uppercase and the Trim transforms.

<table id="table_vkq_xqv_c1c"><thead><tr><th colspan="2" align="center">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

RTE Entity Upper Case Trim Operation \[sys\_rte\_eb\_upper\_case\_trim\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field**Input is a string value.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the upper case string value without any whitespaces at the beginning and end.

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|"      value1    "|"VALUE1"|

