---
title: GlideFilter - Scoped, Global
description: The GlideFilter API enables filtering queries to determine if one or more records meet a specified set of requirements.Instantiates a GlideFilter object.Compares a specified filter to the contents of a specified GlideRecord.Evaluates a filter against a specified GlideRecord.Enables or disables case-sensitive filter results.Enables or disables sandboxed evaluation of the filter string.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideFilter - Scoped, Global

The GlideFilter API enables filtering queries to determine if one or more records meet a specified set of requirements.

Methods for this API are accessible using the GlideFilter global object.

## Case sensitivity

The GlideFilter API is case-sensitive by default. Use the [setCaseSensitive\(\)](c_GlideFilterScopedAPI.md#) method to enable or disable case sensitivity. [GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) queries are case-insensitive.

The following example shows how a GlideRecord query is case-insensitive and results in the same user record with upper or lower case.

```
var gr_Query = new GlideRecord('sys_user');
gr_Query.addQuery('first_name', 'Abel');
gr_Query.query();
while (gr_Query.next())
  gs.info("Upper case query: " + gr_Query.getDisplayValue());

var gr_Query = new GlideRecord('sys_user');
gr_Query.addQuery('first_name', 'abel');
gr_Query.query();
while (gr_Query.next())       
  gs.info("Lower case query: " + gr_Query.getDisplayValue());
```

GlideRecord.query\(\)output shows the same results display regardless of case.

```
Upper case query: Abel Tuter
Lower case query: Abel Tuter
```

The following example shows how GlideFilter only retrieves the matched value of the record for the upper case condition. The lower case condition does not provide a match.

```
// Matches the 'Abel Tuter' user record
var gr_Query = new GlideRecord('sys_user');
gr_Query.query();
var condition = 'first_name=Abel';
var glideFilter = new GlideFilter(condition, 'filterCondition');
while (gr_Query.next()) {
   if (glideFilter.match(gr_Query, true))
        gs.info("Upper case condition: " + gr_Query.getDisplayValue());
}

// The following code does not match 'Abel Tuter' user record
var gr_Query = new GlideRecord('sys_user');
gr_Query.query();
var condition = 'first_name=abel';
var glideFilter = new GlideFilter(condition, 'filterCondition');
while (gr_Query.next()) {
   if (glideFilter.match(gr_Query, true))
        gs.info("Lower case condition: " + gr_Query.getDisplayValue());
}
```

The output reveals that the filter only returns upper case results with default case-sensitivity:

```
Upper case condition: Abel Tuter
```

The following example shows how to disable GlideFilter case-sensitivity with the setCaseSensitive\(\) method. The filter matches the condition even though the case does not match the field value.

```
// Matches the 'Abel Tuter' user record
var gr_Query = new GlideRecord('sys_user');
gr_Query.query();
var condition = 'first_name=Abel';
var glideFilter = new GlideFilter(condition, 'filterCondition');
while (gr_Query.next()) {
   if (glideFilter.match(gr_Query, true))
     gs.info("Upper case condition: " + gr_Query.getDisplayValue());
}

// The following code disables case sensitivity and matches the same record
var gr_Query = new GlideRecord('sys_user');
gr_Query.query();

var condition = 'first_name=abel';
var glideFilter = new GlideFilter(condition, 'filterCondition');
glideFilter.setCaseSensitive(false);

while (gr_Query.next()) {
  if (glideFilter.match(gr_Query, true))
    gs.info("Lower case condition: " + gr_Query.getDisplayValue());
}
```

The output reveals GlideFilter case-insensitive results:

```
Upper case condition: Abel Tuter
Lower case condition: Abel Tuter
```

## Filter null values

To exclude null values from GlideFilter query results, add `ISNOTEMPTY` to the query condition. The following example shows how using the same encoded query with GlideRecord and GlideFilter produces different results.

```
var insertRecordsGr = new GlideRecord('u_test_table');
insertRecordsGr.deleteMultiple();
var dates = ['', '2021-01-29', '2021-01-30', '2021-01-31'];
dates.forEach(function(val) {
  insertRecordsGr.initialize();
  insertRecordsGr.u_date_field = val;
  insertRecordsGr.insert();
});

var now_GR = new GlideRecord('u_test_table');
now_GR.addEncodedQuery('u_date_field<javascript:gs.beginningOfToday()');
now_GR.query();

// Encoded query includes null values with GlideFilter, which might cause unexpected results
var condition = 'u_date_field<javascript:gs.beginningOfToday()';

var grWithGlideFilter = new GlideRecord('u_test_table');
grWithGlideFilter.query();
var filter = new GlideFilter(condition, 'filterCondition');
  
var countWithGlideFilter = 0;
while (grWithGlideFilter.next()) {
  if (GlideFilter.checkRecord(grWithGlideFilter, condition))
     countWithGlideFilter++;
}

gs.info('Record RowCount: ' + now_GR.getRowCount() + ' - Filter Count: ' + countWithGlideFilter);
```

The output shows that GlideRecord returns three records, skipping empty date values. The GlideFilter query counts the empty date value and returns a count of four records.

```
Record RowCount: 3 - Filter Count: 4
```

To exclude null values from the GlideFilter results, add an `AND` condition `ISNOTEMPTY` to the queried field.

```
// Encoded query includes null values with GlideFilter
var condition = 'u_date_field<=javascript:gs.beginningOfToday()^u_date_fieldISNOTEMPTY';
```

Output shows that the GlideFilter encoded query skips the null date value and counts three results.

```
Record RowCount: 3 - Filter Count: 3
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideFilter – GlideFilter\(String filter, String title\)

Instantiates a GlideFilter object.

<table id="table_vqm_5z1_ppb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

String

</td><td>

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US). Results are case-sensitive, unless disabled using the [setCaseSensitive\(\)](c_GlideFilterScopedAPI.md#) method.To exclude null values from GlideFilter query results, add ISNOTEMPTY to the query condition.

</td></tr><tr><td>

title

</td><td>

String

</td><td>

Descriptive title for the filter.

</td></tr></tbody>
</table>The following example shows how to filter the number of users named Rebekah.

```
var now_GR = new GlideRecord('sys_user');
now_GR.query();
var condition = 'first_name=rebekah';
var filter = new GlideFilter(condition, 'filterCondition');
filter.setCaseSensitive(false);
  
var countResults = 0;
while (now_GR.next()) {
  if (filter.match(now_GR, true))
     countResults++;
}

gs.info('Number of users named Rebekah: ' + countResults);
```

Output:

```
Number of users named Rebekah: 2
```

## GlideFilter - checkRecord\(GlideRecord now\_GR, String filter, Boolean match\)

Compares a specified filter to the contents of a specified GlideRecord.

If the specified filter contains one condition, the method returns true if the record meets the condition.

Filters support multiple conditions, for example `"active=true^number=abc^category=request"`. You can use the **match** parameter to define whether all conditions must be met to determine a match or just a single condition.

<table id="table_m2x_bc5_qr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

now\_GR

</td><td>

[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)

</td><td>

GlideRecord to evaluate.

</td></tr><tr><td>

filter

</td><td>

String

</td><td>

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US). To exclude null values from GlideFilter query results, add ISNOTEMPTY to the query condition.

 **Note:** The **filter** values are case-sensitive. In addition, you cannot use [setCaseSensitive\(false\)](c_GlideFilterScopedAPI.md#) to change the change the case-sensitive value.

</td></tr><tr><td>

match

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether all conditions must be met if the **filter** parameter contains multiple conditions. Valid values:

 -   true: All conditions must be met for the method to return true.
-   false: Only one of the conditions must be met for the method to return true.

 Default: true

</td></tr></tbody>
</table><table id="table_n2x_bc5_qr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Results of the filter comparison.-   true: Filter conditions were met.
-   false: Filter conditions were not met.

</td></tr></tbody>
</table>The following example shows how to display true for each record in the Incident table that meets the filter condition. False otherwise.

```
var rec = new GlideRecord('incident');
rec.query();

var bool = true;
 
while(rec.next())
{
   bool = GlideFilter.checkRecord(rec, "active=true");
   gs.info("number "+ rec.number + " is " + bool);
}
```

Output:

```
number INC0000060 is false
number INC0009002 is false
number INC0000009 is false
...
number INC0000015 is true
number INC0000016 is true
number INC0000017 is true
...
```

## GlideFilter - match\(GlideRecord now\_GR, Boolean match\)

Evaluates a filter against a specified GlideRecord.

<table id="table_m2x_bc5_qr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

now\_GR

</td><td>

[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)

</td><td>

GlideRecord to evaluate.

</td></tr><tr><td>

match

</td><td>

Boolean

</td><td>

Flag that indicates whether all filter conditions must match.

 Valid values:

-   true: All filter conditions must match.
-   false: Filter condition match is not required.

 Default: false

</td></tr></tbody>
</table><table id="table_n2x_bc5_qr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Results of the match check.-   true: Filter conditions were met.
-   false: Filter conditions were not met.

</td></tr></tbody>
</table>The following example shows how to ensure the filter conditions match against the GlideRecord provided.

```
var now_GR = new GlideRecord('sys_user');
now_GR.query();
var condition = 'first_name=rebekah';
var filter = new GlideFilter(condition, 'filterCondition');
filter.setCaseSensitive(false);
  
var countResults = 0;
while (now_GR.next()) {
  if (filter.match(now_GR, true))
     countResults++;
}

gs.info('Number of users named Rebekah: ' + countResults);
```

Output:

```
Number of users named Rebekah: 2
```

## GlideFilter - setCaseSensitive\(Boolean caseSensitive\)

Enables or disables case-sensitive filter results.

<table id="table_wd3_3hb_ppb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

caseSensitive

</td><td>

Boolean

</td><td>

Flag that indicates whether the filter is case-sensitive.Valid values:

-   true: The filter is case-sensitive.
-   false: The filter is case-insensitive.

 Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to disable case-sensitive results.

```
var now_GR = new GlideRecord('sys_user');
now_GR.query();

var condition = 'first_name=rebekah';
var filter = new GlideFilter(condition, 'filterCondition');

// Disable case-sensitive filtering
filter.setCaseSensitive(false);

while (now_GR.next()) {
  if (filter.match(now_GR, true))
     gs.info(now_GR.getDisplayValue());
}
```

Output shows that the filter retrieves upper case results with a lower case condition.

```
Rebekah Padley
Rebekah Lindboe
```

## GlideFilter - setEnforceSecurity\(Boolean enforceSecurity\)

Enables or disables sandboxed evaluation of the filter string.

<table id="table_ylz_2ch_v1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

enforceSecurity

</td><td>

Boolean

</td><td>

Flag that indicates whether to evaluate the filter in the sandbox.

 Valid values:

-   true: Evaluate the filter in the sandbox.
-   false: Don't evaluate the filter in the sandbox.

 Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
var now_GR = new GlideRecord('sys_user');
now_GR.query();
var condition = 'first_name=rebekah';
var filter = new GlideFilter(condition, 'filterCondition');
filter.setEnforceSecurity(true);
  
var countResults = 0;
while (now_GR.next()) {
  if (filter.match(now_GR, true))
     countResults++;
}

gs.info('Number of users named Rebekah: ' + countResults);

```

Output:

```
Number of users named Rebekah: 2
```

