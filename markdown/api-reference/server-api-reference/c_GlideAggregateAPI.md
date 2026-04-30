---
title: GlideAggregate - Global
description: The GlideAggregate API enables creating database aggregation queries.Adds an aggregate to a database query.Adds trending by a business calendar to the aggregate query. This method allows you to pick a date and time field in the corresponding GlideRecord and group records based on a specified business calendar time span.Adds an encoded query to the other queries that may have been set for this aggregate.Adds a "having" element to the aggregate, such as select category, count\(\*\) from incident group by category HAVING count\(\*\) &gt; 5.Adds a "having" element to the aggregate, such as select category, count\(\*\) from incident group by category HAVING count\(\*\) &gt; 5. This implementation of the method enables you to specify a specific field within a table or a dynamic attribute to act upon.Adds a trend for a field. Use a trend to show patterns over a period of time.Gets the value of an aggregate from the current record.Returns the value of the dynamic attribute located at a specified path.Returns the value of the dynamic attribute located at a specified field in the current table and a specified attribute path.Returns the display value of the dynamic attribute located at the specified path.Returns the display value of the dynamic attribute located in a specified table field and attribute path.Retrieves the query necessary to return the current aggregate.Retrieves the number of rows in the GlideAggregate object.Returns the number of records by summing an aggregate.Returns the value of a field or a dynamic attribute.Provides the name of a field, or an attribute within a dynamic attribute store, to use when grouping the aggregates.Orders the aggregates using the value of the specified field, dynamic attribute path, or glidefunction. The field is also added to the group-by list.Orders the aggregates based on the specified aggregate and field or dynamic attribute.Issues the query and gets the results.Limits the number of rows from the table to include in the aggregate query.Sets whether to group the results.Sets whether to group results by year for day-of-week trends. These trends are created using the addTrend\(\) method with the dayofweek time interval.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 28
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideAggregate- Global

The GlideAggregate API enables creating database aggregation queries.

The GlideAggregate class is an extension of the GlideRecord class and provides database aggregation \(AVG, COUNT, GROUP\_CONCAT, GROUP\_CONCAT\_DISTINCT, MAX, MIN, STDDEV, SUM\) queries. This functionality can be helpful when creating customized reports or in calculations for calculated fields.

When you use GlideAggregate methods on currency or price fields, you are working with the reference currency value. Be sure to convert the aggregate values to the user's session currency for display. Because the conversion rate between the currency or price value \(displayed value\) and its reference [currency](https://www.servicenow.com/docs/access?context=currency&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) value \(aggregation value\) might change, the result may not be what the user expects.

To use this API to create dynamic attributes you must have the dynamic\_schema\_writer role. To read dynamic data using this API you must have the dynamic\_schema\_reader role.

For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Note:** When using an on-premise system, the database server time zone must be set to GMT/UTC for this class to work properly.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideAggregate - addAggregate\(String agg, String name\)

Adds an aggregate to a database query.

<table id="id_zgs_fl2_4nb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agg

</td><td>

String

</td><td>

Name of an aggregate to use.Valid values:

-   AVG: Average value of the expression.
-   COUNT: Count of the number of non-null values.
-   GROUP\_CONCAT: Concatenates all non-null values of the group in ascending order, joins them with a comma \(','\), and returns the result as a string.
-   GROUP\_CONCAT\_DISTINCT: Concatenates all non-null values of the group in ascending order, removes duplicates, joins them with a comma \(','\), and returns the result as a string.
-   MAX: Largest, or maximum, value.
-   MIN: Minimum value.
-   STDDEV: Population standard deviation.
-   SUM: Sum of all values.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Optional for field name. Name of the field, or path to an attribute within a dynamic attribute store, to group the results of the aggregation by.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Default: Null

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to use GlideAggregate functions on the Incident \[incident\] table.

```
var incidentGA = new GlideAggregate('incident');
incidentGA.groupBy('category');
incidentGA.orderByAggregate('COUNT', 'sys_mod_count');

incidentGA.addAggregate('AVG', 'sys_mod_count');
incidentGA.addAggregate('COUNT', 'sys_mod_count');
incidentGA.addAggregate('GROUP_CONCAT', 'sys_mod_count');
incidentGA.addAggregate('GROUP_CONCAT_DISTINCT', 'sys_mod_count');
incidentGA.addAggregate('MAX', 'sys_mod_count');
incidentGA.addAggregate('MIN', 'sys_mod_count');
incidentGA.addAggregate('STDDEV', 'sys_mod_count');
incidentGA.addAggregate('SUM', 'sys_mod_count');

incidentGA.query();

while (incidentGA.next()) {
gs.info('CATEGORY: ' + incidentGA.getValue('category'));
gs.info('AVG: ' + incidentGA.getAggregate('AVG', 'sys_mod_count'));
gs.info('COUNT: ' + incidentGA.getAggregate('COUNT', 'sys_mod_count'));
gs.info('GROUP_CONCAT: ' + incidentGA.getAggregate('GROUP_CONCAT', 'sys_mod_count'));
gs.info('GROUP_CONCAT_DISTINCT: ' + incidentGA.getAggregate('GROUP_CONCAT_DISTINCT', 'sys_mod_count'));
gs.info('MAX: ' + incidentGA.getAggregate('MAX', 'sys_mod_count'));
gs.info('MIN: ' + incidentGA.getAggregate('MIN', 'sys_mod_count'));
gs.info('STDDEV: ' + incidentGA.getAggregate('STDDEV', 'sys_mod_count'));
gs.info('SUM: ' + incidentGA.getAggregate('SUM', 'sys_mod_count'));
gs.info(' ');
}
```

Output.

```
CATEGORY: inquiry
AVG: 8.42424242424242424242424242424242424242E00
COUNT: 33
GROUP_CONCAT: 0,0,0,0,1,2,2,4,4,4,5,5,5,6,6,6,6,6,6,6,6,7,8,8,8,8,9,15,15,19,32,33,36
GROUP_CONCAT_DISTINCT: 0,1,2,4,5,6,7,8,9,15,19,32,33,36
MAX: 36
MIN: 0
STDDEV: 9.15843294125113629932710147135171494439E00
SUM: 278
  
CATEGORY: software
AVG: 21
COUNT: 13
GROUP_CONCAT: 3,4,5,5,6,7,9,10,10,11,14,94,95
GROUP_CONCAT_DISTINCT: 3,4,5,6,7,9,10,11,14,94,95
MAX: 95
MIN: 3
STDDEV: 3.27693962918655755532970326989852794087E01
SUM: 273
  
CATEGORY: Hardware
AVG: 6.8
COUNT: 10
GROUP_CONCAT: 2,5,5,6,6,6,7,7,9,15
GROUP_CONCAT_DISTINCT: 2,5,6,7,9,15
MAX: 15
MIN: 2
STDDEV: 3.39280283999985933622820108982884699755E00
SUM: 68
  
CATEGORY: network
AVG: 18
COUNT: 5
GROUP_CONCAT: 3,12,17,21,37
GROUP_CONCAT_DISTINCT: 3,12,17,21,37
MAX: 37
MIN: 3
STDDEV: 1.25698050899765347157025586536136512302E01
SUM: 90
  
CATEGORY: 
AVG: 9.5
COUNT: 4
GROUP_CONCAT: 8,8,10,12
GROUP_CONCAT_DISTINCT: 8,10,12
MAX: 12
MIN: 8
STDDEV: 1.91485421551267621995020382273964310607E00
SUM: 38
  
CATEGORY: database
AVG: 29
COUNT: 2
GROUP_CONCAT: 8,50
GROUP_CONCAT_DISTINCT: 8,50
MAX: 50
MIN: 8
STDDEV: 2.969848480983499602483546320840365965E01
SUM: 58
```

The following example shows how to call this method using an attribute in a dynamic attribute store.

```
var ga_Inc = new GlideAggregate('incident');
ga_Inc.groupBy('inc_dynamic_schema->cars->make');
ga_Inc.addAggregate('AVG', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('MIN', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('MAX', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('SUM', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('COUNT', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('STDDEV', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('GROUP_CONCAT', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('GROUP_CONCAT_DISTINCT', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('COUNT(DISTINCT', 'inc_dynamic_schema->cars->cost');
ga_Inc.query();
while (ga_Inc.next()) {
    gs.info(gr_Inc.getValue('inc_dynamic_schema->cars->make'));
    gs.info('AVG: ' + ga_Inc.getAggregate('AVG', 'inc_dynamic_schema->cars->cost'));
    gs.info('MAX: ' + ga_Inc.getAggregate('MAX', 'inc_dynamic_schema->cars->cost'));
    gs.info('MIN: ' + ga_Inc.getAggregate('MIN', 'inc_dynamic_schema->cars->cost'));
    gs.info('SUM: ' + ga_Inc.getAggregate('SUM', 'inc_dynamic_schema->cars->cost'));
    gs.info('COUNT: ' + ga_Inc.getAggregate('COUNT', 'inc_dynamic_schema->cars->cost'));
    gs.info('STDDEV: ' + ga_Inc.getAggregate('STDDEV', 'inc_dynamic_schema->cars->cost'));
    gs.info('GROUP_CONCAT: ' + ga_Inc.getAggregate('GROUP_CONCAT', 'inc_dynamic_schema->cars->cost'));
    gs.info('GROUP_CONCAT_DISTINCT: ' + ga_Inc.getAggregate('GROUP_CONCAT_DISTINCT', 'inc_dynamic_schema->cars->cost'));
    gs.info('COUNT(DISTINCT: ' + ga_Inc.getAggregate('COUNT(DISTINCT', 'inc_dynamic_schema->cars->cost'));
    gs.info(' ');
}
```

Output:

```
*** Script: BMW
*** Script: AVG: 31852.066666666667
*** Script: MAX: 49182
*** Script: MIN: 16544
*** Script: SUM: 477781
*** Script: COUNT: 15
*** Script: STDDEV: 10376.50218706
*** Script: GROUP_CONCAT: 16544,18427,19083,22144,24126,27018,32353,34934,35691,35698,35799,36814,41257,48711,49182
*** Script: GROUP_CONCAT_DISTINCT: 16544,18427,19083,22144,24126,27018,32353,34934,35691,35698,35799,36814,41257,48711,49182
*** Script: COUNT(DISTINCT: 15
*** Script:  
*** Script: Ford
*** Script: AVG: 31520.090909090909
*** Script: MAX: 47408
*** Script: MIN: 16080
*** Script: SUM: 346721
*** Script: COUNT: 11
*** Script: STDDEV: 11355.75551388
*** Script: GROUP_CONCAT: 16080,16082,16996,27621,31662,33478,35201,36965,38085,47143,47408
*** Script: GROUP_CONCAT_DISTINCT: 16080,16082,16996,27621,31662,33478,35201,36965,38085,47143,47408
*** Script: COUNT(DISTINCT: 11
*** Script:  
*** Script: Honda
*** Script: AVG: 31972.750000000000
*** Script: MAX: 49187
*** Script: MIN: 15208
*** Script: SUM: 511564
*** Script: COUNT: 16
*** Script: STDDEV: 10240.67632207
*** Script: GROUP_CONCAT: 15208,17926,18365,20942,25557,28215,29090,34336,34857,34969,37144,38097,41541,41805,44325,49187
*** Script: GROUP_CONCAT_DISTINCT: 15208,17926,18365,20942,25557,28215,29090,34336,34857,34969,37144,38097,41541,41805,44325,49187
*** Script: COUNT(DISTINCT: 16
*** Script:  
*** Script: Lexus
*** Script: AVG: 29841.250000000000
*** Script: MAX: 48406
*** Script: MIN: 15517
*** Script: SUM: 238730
*** Script: COUNT: 8
*** Script: STDDEV: 12073.56647214
*** Script: GROUP_CONCAT: 15517,16964,22371,23900,32421,36620,42531,48406
*** Script: GROUP_CONCAT_DISTINCT: 15517,16964,22371,23900,32421,36620,42531,48406
*** Script: COUNT(DISTINCT: 8
*** Script:  
*** Script: Tesla
*** Script: AVG: 30790.000000000000
*** Script: MAX: 45032
*** Script: MIN: 16724
*** Script: SUM: 431060
*** Script: COUNT: 14
*** Script: STDDEV: 8510.068136760580
*** Script: GROUP_CONCAT: 16724,17173,21049,24837,28431,30594,31871,32549,32675,33778,36963,37946,41438,45032
*** Script: GROUP_CONCAT_DISTINCT: 16724,17173,21049,24837,28431,30594,31871,32549,32675,33778,36963,37946,41438,45032
*** Script: COUNT(DISTINCT: 14
*** Script:  
*** Script: Toyota
*** Script: AVG: 32115.444444444444
*** Script: MAX: 49418
*** Script: MIN: 15188
*** Script: SUM: 289039
*** Script: COUNT: 9
*** Script: STDDEV: 12120.76776767
*** Script: GROUP_CONCAT: 15188,16453,24596,28529,32863,34697,42790,44505,49418
*** Script: GROUP_CONCAT_DISTINCT: 15188,16453,24596,28529,32863,34697,42790,44505,49418
*** Script: COUNT(DISTINCT: 9
*** Script:
```

### Scoped equivalent

To use the addAggregate\(\) method in a scoped application, use the corresponding scoped method: [addAggregate\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - addBizCalendarTrend\(String fieldName, String bizCalendarSysId\)

Adds trending by a business calendar to the aggregate query. This method allows you to pick a date and time field in the corresponding GlideRecord and group records based on a specified business calendar time span.

**Note:** This method does not use the JOIN operator on the SQL queries.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Date and time field in the associated GlideRecord to use to determine in which group or calendar time span that the record will be included.|
|bizCalendarSysId|String|Sys\_id of the calendar record to use. This is the calendar that contains the desired time spans.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows the count of incident records grouped by the “Month” business calendar time spans.

```
var monthCal = "4d7ddda353f3001076bcddeeff7b12b1"
var ga = new GlideAggregate('incident');
ga.addAggregate('COUNT');
ga.addBizCalendarTrend('opened_at', monthCal);
ga.setGroup(false);
ga.query();
gs.print(ga.getRowCount());
while (ga.next()) {
  gs.info(ga.getValue('bizcalref') + ', ' + ga.getValue('bizcalrefend') + ', ' + ga.getAggregate('COUNT'));
}
```

Output:

```
13
2015-08-01 00:00:00, 2015-09-01 00:00:00, 2
2015-11-01 00:00:00, 2015-12-01 00:00:00, 2
2016-08-01 00:00:00, 2016-09-01 00:00:00, 3
2016-12-01 00:00:00, 2017-01-01 00:00:00, 1
2018-08-01 00:00:00, 2018-09-01 00:00:00, 3
2018-09-01 00:00:00, 2018-10-01 00:00:00, 3
2018-10-01 00:00:00, 2018-11-01 00:00:00, 2
2019-07-01 00:00:00, 2019-08-01 00:00:00, 2
2020-06-01 00:00:00, 2020-07-01 00:00:00, 1
2021-01-01 00:00:00, 2021-02-01 00:00:00, 1
2023-04-01 00:00:00, 2023-05-01 00:00:00, 15
2023-05-01 00:00:00, 2023-06-01 00:00:00, 23
2023-07-01 00:00:00, 2023-08-01 00:00:00, 9
```

## GlideAggregate - addEncodedQuery\(String query\)

Adds an encoded query to the other queries that may have been set for this aggregate.

|Name|Type|Description|
|----|----|-----------|
|query|String|Encoded query string to add to the aggregate.|

|Type|Description|
|----|-----------|
|None| |

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count','category'); 
agg.orderByAggregate('count', 'category'); 
agg.orderBy('category'); 
agg.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(2)'); 
agg.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(2)'); 
agg.query(); 
while (agg.next()) { 
  var category = agg.category;
  var count = agg.getAggregate('count','category');
  var query = agg.getQuery();  
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count','category');
  agg2.orderByAggregate('count', 'category');
  agg2.orderBy('category');
  agg2.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(3)');
  agg2.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(3)');
  agg2.addEncodedQuery(query);
  agg2.query();
  var last = "";
  while (agg2.next()) {
     last = agg2.getAggregate('count','category');      
  }
  gs.log(category + ": Last month:" + count + " Previous Month:" + last);
 
}
```

### Scoped equivalent

To use the addEncodedQuery\(\) method in a scoped application, use the corresponding scoped method: [addEncodedQuery\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - addHaving\(String name, String operator, String value\)

Adds a "having" element to the aggregate, such as select category, count\(\*\) from incident group by category HAVING count\(\*\) &gt; 5.

|Name|Type|Description|
|----|----|-----------|
|name|String|Aggregate to filter on. For example, COUNT.|
|operator|String|Operator symbol. For example &lt;, &gt;, =, !=.|
|value|String|Value to query on. For example, '5'.|

|Type|Description|
|----|-----------|
|None| |

```
var trend = new GlideAggregate('incident');
trend.addTrend ('opened_at','Month');
trend.addAggregate('COUNT');

//addHaving limits the results returned to those in which the aggregate COUNT is greater than 2
trend.addHaving('COUNT', '>', '2');
trend.setGroup(false);
trend.query();
while(trend.next()) {
  gs.print(('Incidents by month ' + trend.getValue('timeref') + ' where count is more than 2 count is: ' + trend.getAggregate('COUNT'));
}
```

Output:

```
Incidents by month 9/2018 where count is more than 2 count is: 3
Incidents by month 10/2018 where count is more than 2 count is: 8
Incidents by month 11/2018 where count is more than 2 count is: 14
```

## GlideAggregate - addHaving\(String aggName, String fieldName, String operator, String value\)

Adds a "having" element to the aggregate, such as select category, count\(\*\) from incident group by category HAVING count\(\*\) &gt; 5. This implementation of the method enables you to specify a specific field within a table or a dynamic attribute to act upon.

<table id="table_asq_nbk_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aggName

</td><td>

String

</td><td>

Aggregate to filter on. For example, COUNT.

</td></tr><tr><td>

fieldName

</td><td>

String

</td><td>

Field name or path to an attribute within a dynamic attribute store.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

operator

</td><td>

String

</td><td>

Operator symbol. For example &lt;, &gt;, =, !=.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Value to query on. For example, '5'.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to identify the duplicate serial numbers within the cmdb table using a field name in the addHaving\(\) method call.

```
function getDupes(tableName, dpField) { 
    var ga = new GlideAggregate(tableName);
    ga.addAggregate('COUNT', dpField); // Aggregate to count values in whatever field is passed as dpField
    ga.addHaving('COUNT', dpField, '>', '1'); // Returns only records having more than one active instance of dpField
    ga.query(); 
    var arDupes = new Array(); // Build array to push the results into
    while (ga.next()) { 
      arDupes.push(ga.getValue(dpField)); // Push the value of the dupe field to the array  
    }
    return arDupes;
}
 
var tableName = "cmdb";
var dpField = "serial_number";
 
gs.print(getDupes(tableName, dpField));
```

Output:

```
Incidents by month 9/2018 where count is more than 2 count is: 3
Incidents by month 10/2018 where count is more than 2 count is: 8
Incidents by month 11/2018 where count is more than 2 count is: 14
```

The following example shows to identify duplicates, but uses a dynamic attribute instead of a field in the addHaving\(\) method call.

```
function getDupes(tableName, dpField) { 
    var ga = new GlideAggregate(tablename);
    ga.addAggregate('COUNT', dpField); // Aggregate to count values in whatever dynamic attribute is passed as dpField
    ga.addHaving('COUNT', dpField, '>', '1'); // Returns only records having more than one active instance of dpField
    ga.query(); 
    var arDupes = new Array(); // Build array to push the results into
    while (ga.next()) { 
      arDupes.push(ga.getValue(dpField)); // Push the value of the dupe field to the array  
    }
    return arDupes;
}
 
var tableName = "cmdb";
var dpField = "dyn_att_field->group->attr";
 
gs.print(getDupes(tableName, dpField));
```

Output:

```
Incidents by month 9/2018 where count is more than 2 count is: 3
Incidents by month 10/2018 where count is more than 2 count is: 8
Incidents by month 11/2018 where count is more than 2 count is: 14
```

## GlideAggregate - addTrend\(String fieldName, String timeInterval, Number numUnits\)

Adds a trend for a field. Use a trend to show patterns over a period of time.

**Note:** To control whether to group **dayofweek** results by year, use [GlideAggregate - setIntervalYearIncluded\(Boolean b\)](c_GlideAggregateAPI.md#).

<table id="table_tlk_cdk_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

Name of the field for which trending should occur.

</td></tr><tr><td>

timeInterval

</td><td>

String

</td><td>

Time interval for the trend. Valid values:

-   date
-   dayofweek
-   hour
-   minute
-   quarter
-   value
-   week
-   year

</td></tr><tr><td>

numUnits

</td><td>

Number

</td><td>

Optional. Only valid when **timeInterval** = minute. Number of minutes to include in the trend.Default: 1

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var trend = new GlideAggregate('incident');  
trend.addTrend ('opened_at','month');  
trend.addAggregate('COUNT');  
trend.setGroup(false);  
trend.query();  
while(trend.next()) {  
   gs.print(trend.getValue('timeref') + ': ' + trend.getAggregate('COUNT'));  
}  
```

Output:

```
9/2018: 3
10/2018: 8
11/2018: 14
```

### Scoped equivalent

To use the addTrend\(\) method in a scoped application, use the corresponding scoped method: [addTrend\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - getAggregate\(String agg, String name\)

Gets the value of an aggregate from the current record.

<table id="table_udy_sdk_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agg

</td><td>

String

</td><td>

Type of the aggregate.Valid values:

-   AVG: Average value of the expression.
-   COUNT: Count of the number of non-null values.
-   GROUP\_CONCAT: Concatenates all non-null values of the group in ascending order, joins them with a comma \(','\), and returns the result as a string.
-   GROUP\_CONCAT\_DISTINCT: Concatenates all non-null values of the group in ascending order, removes duplicates, joins them with a comma \(','\), and returns the result as a string.
-   MAX: Largest, or maximum, value.
-   MIN: Minimum value.
-   STDDEV: Population standard deviation.
-   SUM: Sum of all values.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Name of the field, or path to an attribute within a dynamic schema, to get the aggregate from.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table><table id="table_vdy_sdk_ws" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Value of the aggregation.If the values being aggregated are FX Currency values, the returned value is in the format `<currency_code;currency_value>`, such as: `USD;134.980000`.

**Note:** If the specified field contains FX Currency values of mixed currency types, the method is not able to aggregate the values and returns a semicolon \(;\).

</td></tr></tbody>
</table>This example shows how to obtain the COUNT aggregate.

```
function doMyBusinessRule(assigned_to, number) {
  var agg = new GlideAggregate('incident');
  agg.addQuery('assigned_to', assigned_to);
  agg.addQuery('category', number);
  agg.addAggregate("COUNT");
  agg.query();
  var answer = 'false';
  if (agg.next()) {
    answer = agg.getAggregate("COUNT");
    if (answer > 0)
      answer = 'true';
    else
      answer = 'false';
  }
  return answer; 
}
```

This example shows the aggregation of an FX Currency field.

```
var ga = new GlideAggregate('laptop_tracker');
ga.addAggregate('SUM', 'cost');
ga.groupBy('name');
ga.query();
while (ga.next()) {
  gs.info('Aggregate results ' + ga.getValue('name') + ' => ' + ga.getAggregate('SUM', 'cost'));
}
```

Output:

```
*** Script: Aggregate results Apple MacBook Air => USD;1651.784280000000
*** Script: Aggregate results Apple MacBook Pro => USD;1651.784280000000
*** Script: Aggregate results Dell XPS => USD;470.852672000000
*** Script: Aggregate results LG => 
*** Script: Aggregate results Samsung Galaxy => USD;225.320000000000
*** Script: Aggregate results Surface3 => USD;2895.560369520000
*** Script: Aggregate results Toshiba => USD;9385.202875800000
```

The following example shows how to call this method using an attribute in a dynamic attribute store.

```
var ga_Inc = new GlideAggregate('incident');
ga_Inc.groupBy('inc_dynamic_schema->cars->make');
ga_Inc.addAggregate('AVG', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('MIN', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('MAX', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('SUM', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('COUNT', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('STDDEV', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('GROUP_CONCAT', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('GROUP_CONCAT_DISTINCT', 'inc_dynamic_schema->cars->cost');
ga_Inc.addAggregate('COUNT(DISTINCT', 'inc_dynamic_schema->cars->cost');
ga_Inc.query();
while (ga_Inc.next()) {
    gs.info(gr_Inc.getValue('inc_dynamic_schema->cars->make'));
    gs.info('AVG: ' + ga_Inc.getAggregate('AVG', 'inc_dynamic_schema->cars->cost'));
    gs.info('MAX: ' + ga_Inc.getAggregate('MAX', 'inc_dynamic_schema->cars->cost'));
    gs.info('MIN: ' + ga_Inc.getAggregate('MIN', 'inc_dynamic_schema->cars->cost'));
    gs.info('SUM: ' + ga_Inc.getAggregate('SUM', 'inc_dynamic_schema->cars->cost'));
    gs.info('COUNT: ' + ga_Inc.getAggregate('COUNT', 'inc_dynamic_schema->cars->cost'));
    gs.info('STDDEV: ' + ga_Inc.getAggregate('STDDEV', 'inc_dynamic_schema->cars->cost'));
    gs.info('GROUP_CONCAT: ' + ga_Inc.getAggregate('GROUP_CONCAT', 'inc_dynamic_schema->cars->cost'));
    gs.info('GROUP_CONCAT_DISTINCT: ' + ga_Inc.getAggregate('GROUP_CONCAT_DISTINCT', 'inc_dynamic_schema->cars->cost'));
    gs.info('COUNT(DISTINCT: ' + ga_Inc.getAggregate('COUNT(DISTINCT', 'inc_dynamic_schema->cars->cost'));
    gs.info(' ');
}
```

Output:

```
*** Script: BMW
*** Script: AVG: 31852.066666666667
*** Script: MAX: 49182
*** Script: MIN: 16544
*** Script: SUM: 477781
*** Script: COUNT: 15
*** Script: STDDEV: 10376.50218706
*** Script: GROUP_CONCAT: 16544,18427,19083,22144,24126,27018,32353,34934,35691,35698,35799,36814,41257,48711,49182
*** Script: GROUP_CONCAT_DISTINCT: 16544,18427,19083,22144,24126,27018,32353,34934,35691,35698,35799,36814,41257,48711,49182
*** Script: COUNT(DISTINCT: 15
*** Script:  
*** Script: Ford
*** Script: AVG: 31520.090909090909
*** Script: MAX: 47408
*** Script: MIN: 16080
*** Script: SUM: 346721
*** Script: COUNT: 11
*** Script: STDDEV: 11355.75551388
*** Script: GROUP_CONCAT: 16080,16082,16996,27621,31662,33478,35201,36965,38085,47143,47408
*** Script: GROUP_CONCAT_DISTINCT: 16080,16082,16996,27621,31662,33478,35201,36965,38085,47143,47408
*** Script: COUNT(DISTINCT: 11
*** Script:  
*** Script: Honda
*** Script: AVG: 31972.750000000000
*** Script: MAX: 49187
*** Script: MIN: 15208
*** Script: SUM: 511564
*** Script: COUNT: 16
*** Script: STDDEV: 10240.67632207
*** Script: GROUP_CONCAT: 15208,17926,18365,20942,25557,28215,29090,34336,34857,34969,37144,38097,41541,41805,44325,49187
*** Script: GROUP_CONCAT_DISTINCT: 15208,17926,18365,20942,25557,28215,29090,34336,34857,34969,37144,38097,41541,41805,44325,49187
*** Script: COUNT(DISTINCT: 16
*** Script:  
*** Script: Lexus
*** Script: AVG: 29841.250000000000
*** Script: MAX: 48406
*** Script: MIN: 15517
*** Script: SUM: 238730
*** Script: COUNT: 8
*** Script: STDDEV: 12073.56647214
*** Script: GROUP_CONCAT: 15517,16964,22371,23900,32421,36620,42531,48406
*** Script: GROUP_CONCAT_DISTINCT: 15517,16964,22371,23900,32421,36620,42531,48406
*** Script: COUNT(DISTINCT: 8
*** Script:  
*** Script: Tesla
*** Script: AVG: 30790.000000000000
*** Script: MAX: 45032
*** Script: MIN: 16724
*** Script: SUM: 431060
*** Script: COUNT: 14
*** Script: STDDEV: 8510.068136760580
*** Script: GROUP_CONCAT: 16724,17173,21049,24837,28431,30594,31871,32549,32675,33778,36963,37946,41438,45032
*** Script: GROUP_CONCAT_DISTINCT: 16724,17173,21049,24837,28431,30594,31871,32549,32675,33778,36963,37946,41438,45032
*** Script: COUNT(DISTINCT: 14
*** Script:  
*** Script: Toyota
*** Script: AVG: 32115.444444444444
*** Script: MAX: 49418
*** Script: MIN: 15188
*** Script: SUM: 289039
*** Script: COUNT: 9
*** Script: STDDEV: 12120.76776767
*** Script: GROUP_CONCAT: 15188,16453,24596,28529,32863,34697,42790,44505,49418
*** Script: GROUP_CONCAT_DISTINCT: 15188,16453,24596,28529,32863,34697,42790,44505,49418
*** Script: COUNT(DISTINCT: 9
*** Script:
```

### Scoped equivalent

To use the getAggregate\(\) method in a scoped application, use the corresponding scoped method: [getAggregate\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - getDynamicAttributeValue\(String fullPath\)

Returns the value of the dynamic attribute located at a specified path.

<table id="table_oh3_x1x_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fullPath

</td><td>

String

</td><td>

Path to use to locate the desired dynamic attribute. Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


</td></tr></tbody>
</table><table id="table_ph3_x1x_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Value of the dynamic attribute located at the specified path.If the **fullPath** parameter contains invalid data or the specified attribute value isn't one of the supported data types, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var ga_Tab = new GlideAggregate('u_mytable');
ga_Tab.groupBy('u_dyn_attr_store->paint->color');
ga_Tab.addAggregate('AVG', 'u_dyn_attr_store->paint->number');
ga_Tab.query();

while(ga_Tab.next()) {
    gs.info(
        "color: " + ga_Tab.getDynamicAttributeValue('u_dyn_attr_store->paint->color')
        + "  avg: " + ga_Tab.getAggregate('AVG', 'u_dyn_attr_store->paint->number'));
}
```

Output:

```
*** Script: color: blue  avg: 5.0000
*** Script: color: red  avg: 8.0000
*** Script: color: yellow  avg: 7.0000
```

## GlideAggregate - getDynamicAttributeValue\(String dynamicAttributeField, String groupAttrPath\)

Returns the value of the dynamic attribute located at a specified field in the current table and a specified attribute path.

<table id="table_n1f_fbx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dynamicAttributeField

</td><td>

String

</td><td id="DynS-dynamicAttributeField-entry">

Name of the field in the table that contains the dynamic attribute.

</td></tr><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with.

Table: In the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.

-   `attr_name`: Name of the dynamic attribute within the dynamic group.

Table: In the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.


For example: `"car->color"`

</td></tr></tbody>
</table><table id="table_o1f_fbx_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Value of the dynamic attribute located at the specified path.If either the **dynamicAttributeField** or **groupAttrPath** parameters are invalid, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var ga_Tab = new GlideAggregate('u_mytable');
ga_Tab.groupBy('u_dyn_attr_store->paint->color');
ga_Tab.addAggregate('AVG', 'u_dyn_attr_store->paint->number');
ga_Tab.query();

while(ga_Tab.next()) {
    gs.info(
        "color: " + ga_Tab.getDynamicAttributeValue('u_dyn_attr_store', 'paint->color')
        + "  avg: " + ga_Tab.getAggregate('AVG', 'u_dyn_attr_store->paint->number'));
}
```

Output:

```
*** Script: color: blue  avg: 5.0000
*** Script: color: red  avg: 8.0000
*** Script: color: yellow  avg: 7.0000
```

## GlideAggregate - getDynamicAttributeDisplayValue\(String fullPath\)

Returns the display value of the dynamic attribute located at the specified path.

<table id="table_nht_nbx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fullPath

</td><td>

String

</td><td>

Path to use to locate the desired dynamic attribute. Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


</td></tr></tbody>
</table><table id="table_oht_nbx_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Display value of the dynamic attribute located at the specified path.If the **fullPath** parameter is invalid, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var ga_Tab = new GlideAggregate('u_mytable');
ga_Tab.groupBy('u_dyn_attr_store->paint->color');
ga_Tab.addAggregate('AVG', 'u_dyn_attr_store->paint->number');
ga_Tab.query();

while(ga_Tab.next()) {
    gs.info(
        "color: " + ga_Tab.getDynamicAttributeDisplayValue('u_dyn_attr_store->paint->color')
        + "  avg: " + ga_Tab.getAggregate('AVG', 'u_dyn_attr_store->paint->number'));
}
```

Output:

```
*** Script: color: blue  avg: 5.0000
*** Script: color: red  avg: 8.0000
*** Script: color: yellow  avg: 7.0000
```

## GlideAggregate - getDynamicAttributeDisplayValue\(String dynamicAttributeField, String groupAttrPath\)

Returns the display value of the dynamic attribute located in a specified table field and attribute path.

<table id="table_vm3_wbx_1bc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dynamicAttributeField

</td><td>

String

</td><td id="DynS-dynamicAttributeField-entry">

Name of the field in the table that contains the dynamic attribute.

</td></tr><tr><td>

groupAttrPath

</td><td>

String

</td><td>

Attribute path to use to locate the associated dynamic schema attribute.Format: `"group_name->attr_name"`

-   `group_name`: Name of the group that the attribute is associated with.

Table: In the Name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table or the Group field of the Dynamic Attribute \[dynamic\_attribute\] table.

-   `attr_name`: Name of the dynamic attribute within the dynamic group.

Table: In the Name field of the Dynamic Attribute \[dynamic\_attribute\] table.


For example: `"car->color"`

</td></tr></tbody>
</table><table id="table_wm3_wbx_1bc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Display value of the dynamic attribute located at the specified path.If either the **dynamicAttributeField** or **groupAttrPath** parameters are invalid, returns null.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
var ga_Tab = new GlideAggregate('u_mytable');
ga_Tab.groupBy('u_dyn_attr_store->paint->color');
ga_Tab.addAggregate('AVG', 'u_dyn_attr_store->paint->number');
ga_Tab.query();

while(ga_Tab.next()) {
    gs.info(
        "color: " + ga_Tab.getDynamicAttributeDisplayValue('u_dyn_attr_store', 'paint->color')
        + "  avg: " + ga_Tab.getAggregate('AVG', 'u_dyn_attr_store->paint->number'));
}
```

Output:

```
*** Script: color: blue  avg: 5.0000
*** Script: color: red  avg: 8.0000
*** Script: color: yellow  avg: 7.0000
```

## GlideAggregate - getQuery\(\)

Retrieves the query necessary to return the current aggregate.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The query.|

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count','category'); 
agg.orderByAggregate('count', 'category'); 
agg.orderBy('category'); 
agg.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(2)'); 
agg.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(2)'); 
agg.query(); 
while (agg.next()) { 
  var category = agg.category;
  var count = agg.getAggregate('count','category');
  var query = agg.getQuery();  
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count','category');
  agg2.orderByAggregate('count', 'category');
  agg2.orderBy('category');
  agg2.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(3)');
  agg2.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(3)');
  agg2.addEncodedQuery(query);
  agg2.query();
  var last = "";
  while (agg2.next()) {
     last = agg2.getAggregate('count','category');      
  }
  gs.log(category + ": Last month:" + count + " Previous Month:" + last);
 
}
```

## GlideAggregate - getRowCount\(\)

Retrieves the number of rows in the GlideAggregate object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of rows in the GlideAggregate object.|

```
var count = new GlideAggregate('incident');
  count.addAggregate('MIN', 'sys_mod_count');
  count.addAggregate('MAX', 'sys_mod_count');
  count.addAggregate('AVG', 'sys_mod_count');
  count.groupBy('category');
  count.query();
  gs.info(count.getRowCount());
  while (count.next()) {  
     var min = count.getAggregate('MIN', 'sys_mod_count');
     var max = count.getAggregate('MAX', 'sys_mod_count');
     var avg = count.getAggregate('AVG', 'sys_mod_count');
     var category = count.category.getDisplayValue();
     gs.info(category + " Update counts: MIN = " + min + " MAX = " + max + " AVG = " + avg);
  }
```

Output:

```
6
Database Update counts: MIN = 8 MAX = 48 AVG = 28.0000
Hardware Update counts: MIN = 4 MAX = 14 AVG = 6.6250
Inquiry / Help Update counts: MIN = 0 MAX = 34 AVG = 6.5714
Network Update counts: MIN = 3 MAX = 37 AVG = 18.6000
Request Update counts: MIN = 5 MAX = 39 AVG = 13.4000
Software Update counts: MIN = 4 MAX = 98 AVG = 24.0000
```

### Scoped equivalent

To use the getRowCount\(\) method in a scoped application, use the corresponding scoped method: [Scoped GlideAggregate - getRowCount\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - getTotal\(String agg, String name\)

Returns the number of records by summing an aggregate.

<table id="table_kl5_v2k_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agg

</td><td>

String

</td><td>

Name of an aggregate to use.Valid values:

-   AVG: Average value of the expression.
-   COUNT: Count of the number of non-null values.
-   GROUP\_CONCAT: Concatenates all non-null values of the group in ascending order, joins them with a comma \(','\), and returns the result as a string.
-   GROUP\_CONCAT\_DISTINCT: Concatenates all non-null values of the group in ascending order, removes duplicates, joins them with a comma \(','\), and returns the result as a string.
-   MAX: Largest, or maximum, value.
-   MIN: Minimum value.
-   STDDEV: Population standard deviation.
-   SUM: Sum of all values.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Name of the field to aggregate.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Number|Number of records.|

```
var incidentGA = new GlideAggregate('incident');
incidentGA.addQuery('category', 'software'); 
incidentGA.addAggregate('COUNT');  
incidentGA.addTrend('opened_at','year'); // Counting number of incidents for software category per year
incidentGA.setGroup(false);
incidentGA.query();
while(incidentGA.next()){
  gs.info('Incidents opened on year - '+incidentGA.getValue('timeref')+' - '+incidentGA.getAggregate('COUNT'));
}
gs.info('Total Aggregate Value >> '+ incidentGA.getTotal('COUNT')); 
```

Output:

```
Incidents opened on year - 2015 - 1
Incidents opened on year - 2018 - 5
Incidents opened on year - 2020 - 10
Total Aggregate Value >> 16
```

## GlideAggregate - getValue\(String name\)

Returns the value of a field or a dynamic attribute.

<table id="table_odk_kfk_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Field name or path to an attribute within a dynamic attribute store.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Value of the specified field. Returns null if invalid \(not part of result set\).|

```
var trend = new GlideAggregate('incident');
trend.addTrend ('opened_at','Month');
trend.addAggregate('COUNT');

//addHaving limits the results returned to those in which the aggregate COUNT is greater than 2
trend.addHaving('COUNT', '>', '2');
trend.setGroup(false);
trend.query();
while(trend.next()) {
  gs.print(('Incidents by month ' + trend.getValue('timeref') + ' where count is more than 2 count is: ' + trend.getAggregate('COUNT'));
}
```

Output:

```
Incidents by month 9/2018 where count is more than 2 count is: 3
Incidents by month 10/2018 where count is more than 2 count is: 8
Incidents by month 11/2018 where count is more than 2 count is: 14
```

### Scoped equivalent

To use the getValue\(\) method in a scoped application, use the corresponding scoped method: [getValue\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - groupBy\(String name\)

Provides the name of a field, or an attribute within a dynamic attribute store, to use when grouping the aggregates.

May be called numerous times to set multiple group fields.

<table id="table_itp_2gk_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Field name or path to an attribute within a dynamic attribute store.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to call this method.

```
var count = new GlideAggregate('incident');
count.addAggregate('MIN', 'sys_mod_count');
count.addAggregate('MAX', 'sys_mod_count');
count.addAggregate('AVG', 'sys_mod_count');
count.groupBy('category');
count.query();   
while (count.next()) {  
  var min = count.getAggregate('MIN', 'sys_mod_count');
  var max = count.getAggregate('MAX', 'sys_mod_count');
  var avg = count.getAggregate('AVG', 'sys_mod_count');
  var category = count.category.getDisplayValue();
  gs.log(category + " Update counts: MIN = " + min + " MAX = " + max + " AVG = " + avg);
}
```

The following example shows how to call this method using an attribute in a dynamic attribute store.

```
var ga_AppTab = new GlideAggregate('application_table');
ga_AppTab.addGroupBy('dyn_att_field->group->attr');
ga_AppTab.addAggregate('AVG', 'dyn_att_field->group->attr1');
ga_AppTab.addHaving('SUM', 'dyn_att_field->group->attr2', '>=', 420);
ga.query();
```

### Scoped equivalent

To use the groupBy\(\) method in a scoped application, use the corresponding scoped method: [groupBy\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - orderBy\(String name\)

Orders the aggregates using the value of the specified field, dynamic attribute path, or glidefunction. The field is also added to the group-by list.

<table id="table_ft1_wgk_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Field name, path to an attribute within a dynamic attribute store, or glidefunction to use to order the aggregates.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

glidefunction format: `glidefunction:length(short_description)`. For more information about glidefunctions, see [glidefunction operations](https://www.servicenow.com/docs/access?context=platform-support-functions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count','category'); 
agg.orderByAggregate('count', 'category'); 
agg.orderBy('category'); 
agg.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(2)'); 
agg.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(2)'); 
agg.query(); 
while (agg.next()) { 
  var category = agg.category;
  var count = agg.getAggregate('count','category');
  var query = agg.getQuery();  
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count','category');
  agg2.orderByAggregate('count', 'category');
  agg2.orderBy('category');
  agg2.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(3)');
  agg2.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(3)');
  agg2.addEncodedQuery(query);
  agg2.query();
  var last = "";
  while (agg2.next()) {
     last = agg2.getAggregate('count','category');      
  }
  gs.log(category + ": Last month:" + count + " Previous Month:" + last);
}
```

### Scoped equivalent

To use the orderBy\(\) method in a scoped application, use the corresponding scoped method: [orderBy\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - orderByAggregate\(String agg, String fieldName\)

Orders the aggregates based on the specified aggregate and field or dynamic attribute.

<table id="table_ycv_lhk_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agg

</td><td>

String

</td><td>

Type of aggregation.Valid values:

-   AVG: Average value of the expression.
-   COUNT: Count of the number of non-null values.
-   GROUP\_CONCAT: Concatenates all non-null values of the group in ascending order, joins them with a comma \(','\), and returns the result as a string.
-   GROUP\_CONCAT\_DISTINCT: Concatenates all non-null values of the group in ascending order, removes duplicates, joins them with a comma \(','\), and returns the result as a string.
-   MAX: Largest, or maximum, value.
-   MIN: Minimum value.
-   STDDEV: Population standard deviation.
-   SUM: Sum of all values.

</td></tr><tr><td>

fieldName

</td><td>

String

</td><td>

Name of the field or path to an attribute within a dynamic attribute store to aggregate.Format of the dynamic path: `dyn_att_field->group_name->attribute_name`

-   `dyn_att_field`: Name of a dynamic attribute store field on the table.
-   `group_name`: Name of the group that the attribute is associated with.

Table: In the group\_name field of the Dynamic Attribute Group \[dynamic\_attribute\_group\] table.

-   `attr_name`: Name of the dynamic attribute.

Table: In the attribute field of the Dynamic Attribute \[dynamic\_attribute\] table.


For more information on dynamic attributes, see [Dynamic Schema](https://www.servicenow.com/docs/access?context=dynamic-schema&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count','category'); 
agg.orderByAggregate('count', 'category'); 
agg.orderBy('category'); 
agg.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(2)'); 
agg.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(2)'); 
agg.query(); 
while (agg.next()) { 
  var category = agg.category;
  var count = agg.getAggregate('count','category');
  var query = agg.getQuery();  
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count','category');
  agg2.orderByAggregate('count', 'category');
  agg2.orderBy('category');
  agg2.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(3)');
  agg2.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(3)');
  agg2.addEncodedQuery(query);
  agg2.query();
  var last = "";
  while (agg2.next()) {
     last = agg2.getAggregate('count','category');      
  }
  gs.log(category + ": Last month:" + count + " Previous Month:" + last);
 
}
```

### Scoped equivalent

To use the orderByAggregate\(\) method in a scoped application, use the corresponding scoped method: [orderByAggregate\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - query\(\)

Issues the query and gets the results.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count','category'); 
agg.orderByAggregate('count', 'category'); 
agg.orderBy('category'); 
agg.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(2)'); 
agg.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(2)'); 
agg.query(); 
while (agg.next()) { 
  var category = agg.category;
  var count = agg.getAggregate('count','category');
  var query = agg.getQuery();  
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count','category');
  agg2.orderByAggregate('count', 'category');
  agg2.orderBy('category');
  agg2.addQuery('opened_at', '>=', 'javascript:gs.monthsAgoStart(3)');
  agg2.addQuery('opened_at', '<=', 'javascript:gs.monthsAgoEnd(3)');
  agg2.addEncodedQuery(query);
  agg2.query();
  var last = "";
  while (agg2.next()) {
     last = agg2.getAggregate('count','category');      
  }
  gs.log(category + ": Last month:" + count + " Previous Month:" + last);
```

### Scoped equivalent

To use the query\(\) method in a scoped application, use the corresponding scoped method: [query\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - setAggregateWindow\(Number firstRow, Number lastRow\)

Limits the number of rows from the table to include in the aggregate query.

|Name|Type|Description|
|----|----|-----------|
|firstRow|Number|Zero-based index of the first row to include in the aggregate query, inclusive.|
|lastRow|Number|Zero-based index of the last row to include in the aggregate query, exclusive.|

|Type|Description|
|----|-----------|
|None| |

Prints the count of each category for the first ten records in the Incident \[incident\] table.

```js
var incidentGroup = new GlideAggregate('incident');
incidentGroup.addAggregate('COUNT', 'category');
incidentGroup.setAggregateWindow(0, 10);
incidentGroup.query();
while (incidentGroup.next()) {
   var incidentCount = incidentGroup.getAggregate('COUNT', 'category');
   gs.info('{0} count: {1}', [incidentGroup.getValue('category'), incidentCount]);
}
```

Output:

```js
database count: 1
Hardware count: 1
inquiry count: 7
software count: 1
```

### Scoped equivalent

To use the setAggregateWindow\(\) method in a scoped application, use the corresponding scoped method: [setAggregateWindow\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - setGroup\(Boolean b\)

Sets whether to group the results.

<table id="table_g3r_m3k_ws" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

b

</td><td>

Boolean

</td><td>

Flag that indicates whether to group the results.Valid values:

-   true: Group the results.
-   false: Do not group the results.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var ga = new GlideAggregate('incident');
ga.addAggregate('COUNT', 'category');
 
ga.setGroup(true);
```

### Scoped equivalent

To use the setGroup\(\) method in a scoped application, use the corresponding scoped method: [setGroup\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

## GlideAggregate - setIntervalYearIncluded\(Boolean b\)

Sets whether to group results by year for day-of-week trends. These trends are created using the addTrend\(\) method with the **dayofweek** time interval.

Dependency: [GlideAggregate - addTrend\('&lt;fieldName&gt;', 'dayofweek'\)](c_GlideAggregateAPI.md#).

<table class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

b

</td><td>

Boolean

</td><td>

Flag that indicates whether to include a year for a trend with a day-of-week time interval.Valid values:

-   true: Group day-of-week results by year.
-   false: Exclude the year from time interval results.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to count incidents created in the last six months. The incidents are separated by the day of the week, but not including the year. For example, the default results for Thursday would include the year, such as `Thursday/2023: 16`.

```
var incidentGroup = new GlideAggregate('incident');
incidentGroup.addEncodedQuery("sys_created_onRELATIVEGT@month@ago@6");
incidentGroup.addTrend('sys_created_on', 'dayofweek');
incidentGroup.addAggregate('COUNT');
incidentGroup.setIntervalYearIncluded(false);
incidentGroup.query();
while (incidentGroup.next()) {
    gs.info(incidentGroup.getValue('timeref') + ': ' + incidentGroup.getAggregate('COUNT'))};
```

Output:

```
Sunday: 1
Monday: 15
Tuesday: 1
Wednesday: 7
Thursday: 16
Saturday: 1
```

### Scoped equivalent

To use the setIntervalYearIncluded\(\) method in a scoped application, use the corresponding scoped method: [setIntervalYearIncluded\(\)](../../glideAggregateScoped/concept/c_GlideAggregateScopedAPI.md#).

