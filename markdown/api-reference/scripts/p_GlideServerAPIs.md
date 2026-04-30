---
title: Glide Server APIs
description: ServiceNow provides APIs for the Glide Server.The GlideAggregate class is an extension of GlideRecord and allows database aggregation \(COUNT, SUM, MIN, MAX, AVG\) queries to be done. This can be helpful in creating customized reports or in calculations for calculated fields.GlideAggregate is an extension of GlideRecord and its use is probably best shown through a series of examples.GlideRecord is a special Java class \(GlideRecord.java\) that can be used in JavaScript exactly as if it was a native JavaScript class.GlideRecordSecure is a class inherited from GlideRecord that performs the same functions as GlideRecord, and also enforces ACLs.The GlideSystem API provides methods for retrieving information.The GlideDateTime class provides methods for performing operations on GlideDateTime objects, such as instantiating GlideDateTime objects or working with glide\_date\_time fields.The GlideDate and GlideDateTime APIs are used to manipulate date and time values.Examples of JavaScript that can be used to set the value of a duration field.You can specify a date format with a sequence of specific date and time pattern strings. A pattern string consists of one or more uppercase and lowercase letters from A to Z. Any text within quotation marks is ignored and is instead copied into the date output.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Glide Server APIs

ServiceNow provides APIs for the Glide Server.

**Parent Topic:**[Server-side scripting](../../server-scripting/concept/c_ServerScripting.md)

## GlideAggregate

The GlideAggregate class is an extension of GlideRecord and allows database aggregation \(COUNT, SUM, MIN, MAX, AVG\) queries to be done. This can be helpful in creating customized reports or in calculations for calculated fields.

**Note:** This functionality requires a knowledge of JavaScript.

For additional information, refer to [GlideAggregate](../../../app-store/dev_portal/API_reference/glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#) API.

### GlideAggregate examples

GlideAggregate is an extension of GlideRecord and its use is probably best shown through a series of examples.

**Note:** This functionality requires a knowledge of JavaScript.

Here is an example that simply gets a count of the number of records in a table:

```
var count = new GlideAggregate('incident');
count.addAggregate('COUNT');
count.query();
var incidents = 0;
if(count.next()) 
   incidents = count.getAggregate('COUNT');
```

There is no query associated with the preceding example. If you want to get a count of the incidents that were open, simply add a query as is done with GlideRecord. Here is an example to get a count of the number of active incidents.

```
var count = new GlideAggregate('incident');
count.addQuery('active','true');
count.addAggregate('COUNT');
count.query();
var incidents = 0;
if(count.next()) 
   incidents = count.getAggregate('COUNT');
```

To get a count of all the open incidents by category the code is:

```
var count = new GlideAggregate('incident');
count.addQuery('active','true');
count.addAggregate('COUNT','category');
count.query();
while(count.next()){
  var category = count.category;
  var categoryCount = count.getAggregate('COUNT','category');
  gs.log("The are currently "+ categoryCount +" incidents with a category of "+ category);}
```

The output is:

```
 *** Script: The are currently 1.0 incidents with a category of Data  
       *** Script: The are currently 11.0 incidents with a category of Enhancement
       *** Script: The are currently 1.0 incidents with a category of Implementation
       *** Script: The are currently 197.0 incidents with a category of inquiry
       *** Script: The are currently 13.0 incidents with a category of Issue
       *** Script: The are currently 1.0 incidents with a category of 
       *** Script: The are currently 47.0 incidents with a category of request
```

The following is an example that uses multiple aggregations to see how many times records have been modified using the *MIN*, *MAX*, and *AVG* values.

```
var count = new GlideAggregate('incident');
count.addAggregate('MIN','sys_mod_count');
count.addAggregate('MAX','sys_mod_count');
count.addAggregate('AVG','sys_mod_count');
count.groupBy('category');
count.query();
while(count.next()){
  var min = count.getAggregate('MIN','sys_mod_count');
  var max = count.getAggregate('MAX','sys_mod_count');
  var avg = count.getAggregate('AVG','sys_mod_count');
  var category = count.category.getDisplayValue();
  gs.log(category +" Update counts: MIN = "+ min +" MAX = "+ max +" AVG = "+ avg);}
```

The output is:

```
       *** Script: Data Import Update counts: MIN = 4.0 MAX = 21.0 AVG = 9.3333
       *** Script: Enhancement Update counts: MIN = 1.0 MAX = 44.0 AVG = 9.6711
       *** Script: Implementation Update counts: MIN = 4.0 MAX = 8.0 AVG = 6.0
       *** Script: inquiry Update counts: MIN = 0.0 MAX = 60.0 AVG = 5.9715
       *** Script: Inquiry / Help Update counts: MIN = 1.0 MAX = 3.0 AVG = 2.0
       *** Script: Issue Update counts: MIN = 0.0 MAX = 63.0 AVG = 14.9459
       *** Script: Monitor Update counts: MIN = 0.0 MAX = 63.0 AVG = 3.6561
       *** Script: request Update counts: MIN = 0.0 MAX = 53.0 AVG = 5.0987
```

The following is a more complex example that shows how to compare activity from one month to the next.

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count','category'); 
agg.orderByAggregate('count','category'); 
agg.orderBy('category'); 
agg.addQuery('opened_at','>=','javascript:gs.monthsAgoStart(2)'); 
agg.addQuery('opened_at','<=','javascript:gs.monthsAgoEnd(2)'); 
agg.query();
while(agg.next()){
  var category = agg.category;
  var count = agg.getAggregate('count','category');
  var query = agg.getQuery();
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count','category');
  agg2.orderByAggregate('count','category');
  agg2.orderBy('category');
  agg2.addQuery('opened_at','>=','javascript:gs.monthsAgoStart(3)');
  agg2.addQuery('opened_at','<=','javascript:gs.monthsAgoEnd(3)');
  agg2.addEncodedQuery(query);
  agg2.query();
  var last ="";
  while(agg2.next()){
     last = agg2.getAggregate('count','category');}
  gs.log(category +": Last month:"+ count +" Previous Month:"+ last);
 
}
```

The output is:

```
 *** Script: Monitor: Last month:6866.0 Previous Month:4468.0
 *** Script: inquiry: Last month:142.0 Previous Month:177.0
 *** Script: request: Last month:105.0 Previous Month:26.0
 *** Script: Issue: Last month:8.0 Previous Month:7.0
 *** Script: Enhancement: Last month:5.0 Previous Month:5.0
 *** Script: Implementation: Last month:1.0 Previous Month:0
```

The following is an example to obtain distinct count of a field on a group query.

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count');
agg.addAggregate('count(distinct','category');
agg.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(2)');
agg.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(2)');
//
agg.groupBy('priority');
agg.query();
while (agg.next()) {
// Expected count of incidents and count of categories within each priority value (group)
  gs.info('Incidents in priority ' + agg.priority + ' = ' + agg.getAggregate('count') + 
            ' (' + agg.getAggregate('count(distinct','category') + ' categories)');
}
```

The output is:

```
*** Script: Incidents in priority 1 = 13 (3 categories)
*** Script: Incidents in priority 2 = 10 (5 categories)
*** Script: Incidents in priority 3 = 5 (3 categories)
*** Script: Incidents in priority 4 = 22 (6 categories)
```

You can implement the SUM aggregate with or without the use of the groupBy\(\) method. If you do not use the groupBy\(\) method, the result of the SUM is the cumulative value for each different value of the field for which you request the SUM. For example, if you SUM the total\_cost field in the Fixed Asset table, and the Fixed Asset table contains 12 total records:

-   Three records with a total\_cost of $12
-   Four records with a total\_cost of $10
-   Five records with a total\_cost of $5

When you SUM the record set, the getAggregate\(\) method returns three different sums: $36, $40, and $25.

The following code illustrates implementing the SUM aggregate without using the groupBy\(\) method:

```
var totalCostSum = new GlideAggregate('fixed_asset');
totalCostSum.addAggregate('SUM', 'total_cost');
totalCostSum.query();
 
while (totalCostSum.next()) {
  var allTotalCost = 0;
  allTotalCost = totalCostSum.getAggregate('SUM', 'total_cost');
  aTotalCost = totalCostSum.getValue('total_cost');
  gs.print('Unique field value: ' + aTotalCost + ', SUM = ' + allTotalCost + ', ' + allTotalCost/aTotalCost + ' records');
}
```

The output for this example is:

```
*** Script: Unique field value: 12, SUM = 36, 3 records
*** Script: Unique field value: 10, SUM = 40, 4 records
*** Script: Unique field value: 5, SUM = 25, 5 records
```

Using the same data points as the prior example, if you use the groupBy\(\) method, the SUM aggregate returns the sum of all values for the specified field.

The following example illustrates implementing the SUM aggregate using the groupBy\(\) method:

```
var totalCostSum = new GlideAggregate('fixed_asset');
totalCostSum.addAggregate('SUM', 'total_cost');
totalCostSum.groupBy('total_cost');
totalCostSum.query();
if(totalCostSum.next()){  // in case there is no result
   var allTotalCost = 0;
   allTotalCost = totalCostSum.getAggregate('SUM', 'total_cost');
   gs.print('SUM of total_cost: = ' + allTotalCost);
}
```

The output for this example is:

```
*** Script: SUM of total_cost: 101
```

## GlideRecord

GlideRecord is a special Java class \(GlideRecord.java\) that can be used in JavaScript exactly as if it was a native JavaScript class.

GlideRecord:

-   is used for database operations instead of writing SQL queries.
-   is an object that contains zero or more records from one table. Another way to say this is that a GlideRecord is an ordered list.

A GlideRecord contains both records \(rows\) and fields \(columns\). The field names are the same as the underlying database column names. For additional information, refer to [GlideRecord - Scoped](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

**Note:** Use of `gs.sql())` scripting syntax was discontinued in Geneva. Use standard GlideRecord syntax in its place.

## Using GlideRecordSecure

GlideRecordSecure is a class inherited from GlideRecord that performs the same functions as GlideRecord, and also enforces ACLs.

By default, GlideRecordSecure doesn't enforce query ACLs. While it enforces standard read-write ACLs automatically, query ACLs require explicit opt-in by developers. For more information, see [Enforcing query ACLs](p_GlideServerAPIs.md#enforcing_query_ACLs).

### Non-writable fields

When using GlideRecordSecure, non-writable fields are set to NULL when trying to write to the database. By default, the canCreate\(\) method on the column is replaced with canWrite\(\) on the column. If the canWrite\(\) method returns false, the column value is set to NULL.

### Getting the object type

You can check if an object type is ScopedGlideRecordSecure by calling the toString\(\) method.

-   **Checking the returned GlideRecord real type**

    The current object can be passed as ScopedGlideRecordSecure. In most cases, you can call current.toString\(\) to return the current object type.

    The following line returns `[object ScopedGlideRecordSecure]` for a ScopedGlideRecordSecure object:

    `gs.info(current.toString());`

-   **If the returned object type is different than expected**

    Calling a scoped function that returns a GlideRecord object as its type returns different results depending on the scope it’s called from.

    -   Calling the scoped function within application scope returns the expected object type of `GlideRecord` or `GlideRecordSecure`.
    -   Calling the scoped function within global scope returns the object type is `ScopedGlideRecord` or `ScopedGlideRecordSecure`.

### Checking for NULL values

If an element cannot be read because an ACL restricts access, a NULL value is created in memory for that record. With GlideRecord, you must explicitly check for any ACLs that might restrict read access to the record. To do so, an `if`statement such as the following is required to check if the record can be read:

```
if (!now_GRScanRead())
   continue;
```

With GlideRecordSecure, it's unnecessary to explicitly check for read access using canRead\(\). Instead, you can use next\(\) by itself to move to the next record. The following example provides a comparison between GlideRecord and GlideRecordSecure.

```
var count = 0;
var now_GR = new GlideRecord('mytable');
now_GR.query(); 
while (now_GR.next()) { 
    if (!now_GR.canRead()) continue; 
    if (!now_GR.canWrite()) continue; 
    if (!now_GR.val.canRead() || !now_GR.val.canWrite())
        now_GR.val = null;
    else
        now_GR.val = "val-" + now_GR.id; 
    if (now_GR.update())
        count ++; 
}
```

```
var count = 0;
var now_GRS = new GlideRecordSecure('mytable');
now_GRS.query(); 
while (now_GRS.next()) {
    now_GRS.val = "val-" + now_GRS.id; 
    if (now_GRS.update())
        count ++; 
}
```

### Enforcing query ACLs

By default, GlideRecordSecure doesn't enforce query ACLs. Query ACL enforcement requires explicit opt-in.

Enforcing query ACLs is a security approach that ensures users can only query fields and records they're authorized to access. This strategy provides defense-in-depth by applying access controls at the query level, not just at the data retrieval level. Explicit query ACL enforcement represents a more secure design pattern for applications handling user input.

To explicitly specify query ACL enforcement behavior, use GlideRecordSecure.addEncodedQuery\(\). Update the basic addEncodedQuery\(query\) usage without explicit ACL specification. Use one of the following secure options.

-   **Option 1: Convenience methods \(recommended\)**

    Use the [addUserEncodedQuery\(\)](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) method for the following use cases:

    -   Queries built from user input in which query ACLs apply
    -   Build dynamic filters based on user selections
    -   Handle untrusted data
    Use the [addSystemEncodedQuery\(\)](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) method for the following use cases:

    -   Hard-coded query conditions
    -   Back end or system-only logic with no user input
    -   Safe, predefined query conditions
    Mix both methods as needed. Different parts of your query can use different enforcement levels based on their source.

    ```
    // Queries built from user input
    nowGRS_ACL.addUserEncodedQuery(userInput);
    
    // Hard-coded system queries
    nowGRS.addSystemEncodedQuery("active=true");
    ```

-   **Option 2: Boolean parameter**

    The following example shows how to use the [addEncodedQuery\(\)](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#) method for ACL enforcement.

    ```
    // Explicitly enforce query ACLs
    var now_GRS_true = new GlideRecordSecure(<table_name>); 
    nowGRS_true.addEncodedQuery(query, true);
    
    // Explicitly skip query ACL enforcement (use cautiously) 
    var nowGRS_false = new GlideRecordSecure(<table_name>); 
    nowGRS_false.addEncodedQuery(query, false);
    ```


### Examples

These are two simple examples using GlideRecordSecure.

```
var att = new GlideRecordSecure('sys_attachment');
att.get('$[sys_attachment.sys_id]'); 
var sm = GlideSecurityManager.get(); 
var checkMe = 'record/sys_attachment/delete'; 
var canDelete = sm.hasRightsTo(checkMe, att);
gs.log('canDelete: ' + canDelete);
canDelete;
```

```
var now_GRS = new GlideRecordSecure('task_ci');
now_GRS.addSystemQuery();
now_GRS.query(); 
var count = now_GRS.getRowCount(); 
if (count > 0 ) { 
    var allocation = parseInt(10000/count) / 100;
    while (now_GRS.next()) {
      now_GRS.u_allocation = allocation;
      now_GRS.update();
    }
}
```

## GlideSystem

The GlideSystem API provides methods for retrieving information.

The GlideSystem \(referred to by the variable name '*gs*' in business rules\) provides a number of convenient methods to get information about the system, the current logged in user, etc. For example, the method addInfoMessage\(\) permits communication with the user.

```
 gs.addInfoMessage('Email address added for notification');
```

Many of the GlideSystem methods facilitate the easy inclusion of dates in query ranges and are most often used in filters and reporting.

For additional information, see [GlideSystem](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#).

## GlideDateTime

The GlideDateTime class provides methods for performing operations on GlideDateTime objects, such as instantiating GlideDateTime objects or working with *glide\_date\_time* fields.

In addition to the instantiation methods described below, a GlideDateTime object can be instantiated from a *glide\_date\_time* field using the getGlideObject\(\) method \(for example, `var gdt = gr.my_datetime_field.getGlideObject();`\).

Some methods use the Java Virtual Machine time zone when retrieving or modifying a date and time value. Using these methods may result in unexpected behavior. Use equivalent local time and UTC methods whenever possible.

### GlideDate and GlideDateTime examples

The GlideDate and GlideDateTime APIs are used to manipulate date and time values.

**Note:** This functionality requires a knowledge of JavaScript.

For additional information, refer to [GlideDate](../../../app-store/dev_portal/API_reference/glideDateScoped/concept/c_GlideDateScopedAPI.md#) API and [GlideDateTime](../../../app-store/dev_portal/API_reference/glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#) API.

You can create a GlideDateTime object from a GlideDate object by passing in the GlideDate object as a parameter to the GlideDateTime constructor. By default, the GlideDateTime object is expressed in the internal format, yyyy-MM-dd HH:mm:ss and the system time zone UTC.

```
var gDate = new GlideDate();
gDate.setValue('2015-01-01');
gs.info(gDate);
 
var gDT = new GlideDateTime(gDate);
gs.info(gDT);
```

Output:

```
2015-01-01
2015-01-01 00:00:00
```

See also [Modify a GlideDateTime field value](../../useful-scripts/concept/useful-server-side-scripts.md#).

### Set a duration field value in script

Examples of JavaScript that can be used to set the value of a duration field.

**Note:** Negative duration values are not supported.

#### Using the GlideDateTime.subtract\(\) method

The subtract\(GlideDateTime start, GlideDateTime end\) method in [GlideDateTime](../../../app-store/dev_portal/API_reference/glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#) enables you to set the duration value using a given start date/time and end date/time. An example on how to set the duration for the time a task was opened is:

```
var duration = GlideDateTime.subtract(start, end);
```

If you want to work with the value returned as a number to use in date or duration arithmetic, convert the return to milliseconds:

```
var time = GlideDateTime.subtract(start,end).getNumericValue();

```

If you want to set a duration to the amount of time between some event and the current date/time:

```
<duration_field> = GlideDateTime.subtract(new GlideDateTime(<start_time>.getValue()),gs.nowDateTime());
```

The time values presented to GlideDateTime.subtract are expected to be in the user's time zone and in the user's format.

#### Setting a default value of a duration field

Setting the default value for a duration field is similar to the method used in the previous topic.

#### Setting the duration field value in a client script

This script sets a *duration\_field* value in a client script. Replace *duration\_field* with the field name from your instance.

```
g_form.setValue('<duration_field>','11 01:02:03');
```

#### Calculating and setting a duration using a client script

Here is an example of how to return a value and populate it using a client script.

Create an `onChange` client script that includes the following code. You can modify this script if you need the calculation to happen in an `onLoad` script or some other way.

```
function onChange(control, oldValue, newValue, isLoading){
var strt = g_form.getValue('<start_field>');
var end = g_form.getValue('<end_field>');
var ajax = new GlideAjax('AjaxDurCalc');
  ajax.addParam('sysparm_name','durCalc');
  ajax.addParam('sysparm_strt',strt);
  ajax.addParam('sysparm_end',end);
  ajax.getXMLWait();
  var answer = ajax.getAnswer();
  g_form.setValue('<duration_field>', answer);}
```

Create a system script include file called *AjaxDurCalc* that handles the request. It may be reused for other functions as well.

```
var AjaxDurCalc = Class.create();
AjaxDurCalc.prototype = Object.extendsObject(AbstractAjaxProcessor,{
 durCalc:function(){return GlideDuration.subtract(this.getParameter('sysparm_strt'),this.getParameter('sysparm_end'));}});
```

#### Changing the duration field value

If you manipulate a duration value with addition/subtraction of some amount of time, use the functions that allow you to get and set the numeric value of the duration. A unit of measure for a duration numeric value is milliseconds. The following is an example that adds 11 seconds to the *duration* field in the current record.

```
var timems = current.duration.dateNumericValue();
timems = timems + 11*1000; 
current.duration.setDateNumericValue(timems);
```

#### Formatting the Resolve Time

To format the **Resolve Time** or the **Business Resolve Time** fields as durations, which displays them as a duration instead of a large integer, add the following attribute to those fields:

```
format=glide_duration
```

Modify the dictionary entry for the field and add the attribute. If there is an existing attribute, separate multiple attributes with commas.

#### Setting the maximum unit of measurement

The *max\_unit* dictionary attribute defines the maximum unit of time used in a duration. For example, if `max_unit=minutes`, a duration of 3 hours 5 minutes 15 seconds appears as 185 minutes 15 seconds. To set the maximum unit of duration measurement, add the following dictionary attribute to the *duration* field:

```
max_unit=<unit>
```

### Date and time format guidelines

You can specify a date format with a sequence of specific date and time pattern strings. A pattern string consists of one or more uppercase and lowercase letters from A to Z. Any text within quotation marks is ignored and is instead copied into the date output.

|String|Description|Output Format|Example|
|------|-----------|-------------|-------|
|G|Era designator|Text|AD|
|y|Year|Year|2019; 19|
|Y|Week in year|Year|2019; 19|
|M|Month in year \(within date\)|Month|July; Jul; 07|
|L|Month in year \(standalone value\)|Month|July; Jul; 07|
|w|Week in year|Number|52|
|W|Week in month|Number|1|
|D|Day in year|Number|365|
|d|Day in month|Number|2|
|F|Day of week in month|Number|3|
|E|Day name in week|Text|Wednesday; Wed|
|u|Day number of week|Number|3|
|a|a.m. or p.m.|Text|p.m.|
|H|Hour in day from 0 through 23|Number|0|
|k|Hour in day from 1 through 24|Number|24|
|K|Hour in a.m. or p.m. from 0 through 11|Number|0|
|h|Hour in a.m. or p.m. from 1 through 12|Number|12|
|m|Minute in hour|Number|59|
|s|Second in minute|Number|1|
|S|Millisecond|Number|500|
|z|Time zone in default format|Time zone in default format|Pacific Standard Time; PST|
|Z|Time zone in RFC 822 format|Time zone in RFC 822 format|-0800|
|X|Time zone in ISO 8601 format|Time zone in ISO 8601 format|-08; -0800; -08:00|

