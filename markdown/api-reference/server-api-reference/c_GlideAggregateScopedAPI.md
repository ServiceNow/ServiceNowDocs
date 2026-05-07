---
title: GlideAggregate - Scoped
description: The GlideAggregate API enables creating database aggregation queries.Creates a GlideAggregate object on the specified table.Adds an aggregate to a database query.Adds an encoded query to the other queries that may have been set for this aggregate.Adds a query to the aggregate.Adds a not null query to the aggregate.Adds a null query to the aggregate.Adds a trend for a specified field. Use a trend to show patterns over a period of time.Returns the value of an aggregate from the current record.Gets the query necessary to return the current aggregate.Retrieves the encoded query.Retrieves the number of rows in the GlideAggregate object.Retrieves the table name associated with this GlideAggregate object.Returns the value of the specified field.Provides the name of a field to use in grouping the aggregates.Determines if there are any more records in the GlideAggregate object.Moves to the next record in the GlideAggregate.Orders the aggregates using the value of the specified field. The field is also added to the group-by list.Orders the aggregates based on the specified aggregate and field.Sorts the aggregates in descending order based on the specified field. The field will also be added to the group-by list.Issues the query and gets the results.Limits the number of rows from the table to include in the aggregate query.Activates or deactivates the running of business rules for aggregate queries.Sets whether to group the return results.Sets whether to group results by year for day-of-week trends. These trends are created using the addTrend\(\) method with the dayofweek time interval.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideAggregate- Scoped

The GlideAggregate API enables creating database aggregation queries.

The GlideAggregate class is an extension of the GlideRecord class and provides database aggregation \(AVG, COUNT, GROUP\_CONCAT, GROUP\_CONCAT\_DISTINCT, MAX, MIN, STDDEV, SUM\) queries. This functionality can be helpful when creating customized reports or in calculations for calculated fields.

When you use GlideAggregate methods on currency or price fields, you are working with the reference currency value. Be sure to convert the aggregate values to the user's session currency for display. Because the conversion rate between the currency or price value \(displayed value\) and its reference [currency](https://www.servicenow.com/docs/access?context=currency&version=australia&pubname=australia-platform-administration&ft:locale=en-US) value \(aggregation value\) might change, the result may not be what the user expects.

**Note:** When using an on-premise system, the database server time zone must be set to GMT/UTC for this class to work properly.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideAggregate - GlideAggregate\(String tableName\)

Creates a GlideAggregate object on the specified table.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table.|

```
var count = new GlideAggregate('incident');
```

## Scoped GlideAggregate - addAggregate\(String agg, String name\)

Adds an aggregate to a database query.

<table id="id_zgs_fl2_4nb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="agg-GlideAgg-row"><td>

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

Optional. Name of the field to group the results of the aggregation by.Default: Null

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

## Scoped GlideAggregate - addEncodedQuery\(String query\)

Adds an encoded query to the other queries that may have been set for this aggregate.

|Name|Type|Description|
|----|----|-----------|
|query|String|An encoded query to add to the aggregate.|

|Type|Description|
|----|-----------|
|None| |

```
//Number of incidents varies depending on the current state
//of the incident table
var count = new GlideAggregate('incident');
count.addEncodedQuery('active=true');
count.addAggregate('COUNT');
count.query();
var incidents = 0;
if (count.next())
   incidents = count.getAggregate('COUNT');
gs.info(incidents);
```

## Scoped GlideAggregate - addQuery\(String name, String operator, String value\)

Adds a query to the aggregate.

|Name|Type|Description|
|----|----|-----------|
|name|String|Query to add.|
|operator|String|Operator for the query.|
|value|String|List of values to include in the query.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|Query condition.|

```
//Number of incidents varies depending on the current state
//of the incident table
var count = new GlideAggregate('incident');
count.addQuery('active', '=','true');
count.addAggregate('COUNT', 'category');
count.query();  
while (count.next()) {
   var category = count.category;
   var categoryCount = count.getAggregate('COUNT', 'category');
   gs.info("There are currently " + categoryCount + " incidents with a category of " + category);
}
```

Output:

```
There are currently 1 incidents with a category of database
There are currently 5 incidents with a category of hardware
There are currently 42 incidents with a category of inquiry
There are currently 4 incidents with a category of network
There are currently 4 incidents with a category of request
There are currently 7 incidents with a category of software
```

## Scoped GlideAggregate - addNotNullQuery\(String fieldName\)

Adds a not null query to the aggregate.

|Name|Type|Description|
|----|----|-----------|
|fieldname|String|Name of the field.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|Scoped query condition.|

```
var count = new GlideAggregate('incident');
  count.addNotNullQuery('short_description');
  count.query();   // Issue the query to the database to get all records
  while (count.next()) {   
     // add code here to process the aggregate
  }
```

## Scoped GlideAggregate - addNullQuery\(String fieldName\)

Adds a null query to the aggregate.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|Name of the field.|

|Type|Description|
|----|-----------|
|GlideQueryCondition|The scoped query condition.|

```
var count = new GlideAggregate('incident');
  count.addNullQuery('short_description');
  count.query();   // Issue the query to the database to get all records
  while (count.next()) {   
     // add code here to process the aggregate
  }
```

## Scoped GlideAggregate - addTrend\(String fieldName, String timeInterval, Number numUnits\)

Adds a trend for a specified field. Use a trend to show patterns over a period of time.

**Note:** To control whether to group **dayofweek** results by year, use [Scoped GlideAggregate - setIntervalYearIncluded\(Boolean b\)](c_GlideAggregateScopedAPI.md#).

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
|void| |

```
var ga = new GlideAggregate('incident');
ga.addAggregate('COUNT'); // Count all incidents opened each quarter
ga.addTrend('opened_at', 'quarter');
ga.query();
while(ga.next()) {
 gs.info([ga.getValue('timeref'), ga.getAggregate('COUNT')]);
}
```

Output:

```
3/2018, 9
4/2018, 2
1/2019, 38
2/2019, 310
```

## Scoped GlideAggregate - getAggregate\(String agg, String name\)

Returns the value of an aggregate from the current record.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

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

Name of the field on which to perform the aggregation.

</td></tr></tbody>
</table><table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The value of the aggregation.If the values being aggregated are FX Currency values, the returned value is in the format `<currency_code;currency_value>`, such as: `USD;134.980000`.

**Note:** If the specified field contains FX Currency values of mixed currency types, the method is not able to aggregate the values and returns a semicolon \(;\).

</td></tr></tbody>
</table>Shows an aggregation that returns the number of records in the Incident table.

```
var count = new GlideAggregate('incident');
count.addAggregate('COUNT');
count.query();
var incidents = 0;
if (count.next()) {
  incidents = count.getAggregate('COUNT');
}
//Number of incidents varies depending on the current state
//of the incident table
gs.info('Number of incidents: ' + incidents);
```

Output: Number of incidents: 63.

Shows the aggregation of an FX Currency field.

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

## Scoped GlideAggregate - getAggregateEncodedQuery\(\)

Gets the query necessary to return the current aggregate.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Encoded query to get the aggregate.|

```
var count = new GlideAggregate('incident');
count.addAggregate('MIN', 'sys_mod_count');
count.groupBy('category');
count.query();  
while (count.next()) {
    gs.info(count.getAggregateEncodedQuery());
}
```

Output:

```
category=database
category=hardware
category=inquiry
category=network
category=request
category=software
```

## Scoped GlideAggregate - getEncodedQuery\(\)

Retrieves the encoded query.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|Encoded query.|

```
var count = new GlideAggregate('incident');
count.addAggregate('MIN', 'sys_mod_count');
count.addAggregate('MAX', 'sys_mod_count');
count.addAggregate('AVG', 'sys_mod_count');
count.groupBy('category');
count.query();
gs.info(count.getEncodedQuery());
```

Output:

```
ORDERBYcategory^GROUPBYcategory
```

## Scoped GlideAggregate - getRowCount\(\)

Retrieves the number of rows in the GlideAggregate object.

|Name|Type|Description|
|----|----|-----------|
|none| | |

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

## Scoped GlideAggregate - getTableName\(\)

Retrieves the table name associated with this GlideAggregate object.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|Table name.|

```
var count = new GlideAggregate('incident');
count.addAggregate('MIN', 'sys_mod_count');
count.addAggregate('MAX', 'sys_mod_count');
count.addAggregate('AVG', 'sys_mod_count');
count.groupBy('category');
count.query();
gs.info(count.getTableName());
```

## Scoped GlideAggregate - getValue\(String name\)

Returns the value of the specified field.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the field within the current table to return.|

|Type|Description|
|----|-----------|
|String|Value of the specified field. Returns null if invalid \(not part of result set\).|

```
var count = new GlideAggregate('incident');
count.addAggregate('MAX', 'sys_mod_count');
count.groupBy('category');
count.query();   
while (count.next()) {  
  gs.info(count.getValue('category') + " category had " + count.getAggregate('MAX', 'sys_mod_count') + " updates");  
}
```

Output:

```
category had 12 updates
hardware category had 15 updates
inquiry category had 36 updates
network category had 37 updates
software category had 95 updates
```

## Scoped GlideAggregate - groupBy\(String name\)

Provides the name of a field to use in grouping the aggregates.

May be called numerous times to set multiple group fields.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the field.|

|Type|Description|
|----|-----------|
|None| |

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
     gs.info(category + " Update counts: MIN = " + min + " MAX = " + max + " AVG = " + avg);
}
```

Output:

```
Database Update counts: MIN = 8 MAX = 48 AVG = 28.0000
Hardware Update counts: MIN = 4 MAX = 14 AVG = 6.6250
Inquiry / Help Update counts: MIN = 0 MAX = 34 AVG = 6.5714
Network Update counts: MIN = 3 MAX = 37 AVG = 18.6000
Request Update counts: MIN = 5 MAX = 39 AVG = 13.4000
Software Update counts: MIN = 4 MAX = 98 AVG = 24.0000

```

## Scoped GlideAggregate - hasNext\(\)

Determines if there are any more records in the GlideAggregate object.

|Name|Type|Description|
|----|----|-----------|
|none| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there are more results in the query set.

 Possible values:

-   true: More results are in the query set.
-   false: No more results in the query set.

</td></tr></tbody>
</table>```
var agg = new GlideAggregate('incident');
agg.addAggregate('AVG', 'sys_mod_count');
agg.groupBy('category');
agg.query();
while (agg.hasNext()) {
    agg.next();
    var avg = agg.getAggregate('AVG', 'sys_mod_count');
    var category = agg.category.getDisplayValue();
    gs.info(category + ': AVG = ' + avg);
}
```

Output:

```
Database: AVG = 32.5000
Hardware: AVG = 12.0000
Inquiry / Help: AVG = 7.6667
Network: AVG = 24.0000
Request: AVG = 16.4000
Software: AVG = 27.0833
```

## Scoped GlideAggregate - next\(\)

Moves to the next record in the GlideAggregate.

|Name|Type|Description|
|----|----|-----------|
|none| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there are more results in the query set.

 Possible values:

-   true: More results are in the query set.
-   false: No more results in the query set.

</td></tr></tbody>
</table>```
var count = new GlideAggregate('incident');
count.addAggregate('COUNT');
count.query();
var incidents = 0;
if (count.next()) {
   incidents = count.getAggregate('COUNT');
   gs.info(incidents);
}
```

## Scoped GlideAggregate - orderBy\(String name\)

Orders the aggregates using the value of the specified field. The field is also added to the group-by list.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

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

Name of the field to order the aggregates by.Alternatively, you can provide a glidefunction to order the aggregates, such as `glidefunction:length(short_description)`. For more information about glidefunctions, see [glidefunction operations](https://www.servicenow.com/docs/access?context=platform-support-functions&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count', 'category'); 
agg.orderBy('category'); 
agg.query(); 
while (agg.next()) { 
  var category = agg.category;
  var count = agg.getAggregate('count', 'category');
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count', 'category');
  agg2.orderBy('category');
  gs.info(category + ": Current number of incidents:" + count);
}
```

Output:

```
database: Current number of incidents:2
hardware: Current number of incidents:8
inquiry: Current number of incidents:28
network: Current number of incidents:5
request: Current number of incidents:5
software: Current number of incidents:11
```

## Scoped GlideAggregate - orderByAggregate\(String agg, String fieldName\)

Orders the aggregates based on the specified aggregate and field.

|Name|Type|Description|
|----|----|-----------|
|agg|String|Type of aggregation.|
|fieldName|String|Name of the field to aggregate.|

|Type|Description|
|----|-----------|
|void| |

```
ga.addAggregate('COUNT', 'category');
ga.orderByAggregate('count', 'category');
ga.query();
while(ga.next()) {
  gs.info('Category: ' + ga.category + ' ' + ga.getAggregate('COUNT', 'category'));
}
```

Output:

```
Category: inquiry 18
Category: software 11
Category: hardware 7
Category: network 5
Category: request 5
Category:  4
Category: database 2
```

## Scoped GlideAggregate - orderByDesc\(String name\)

Sorts the aggregates in descending order based on the specified field. The field will also be added to the group-by list.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the field.|

|Type|Description|
|----|-----------|
|None| |

```
var agg = new GlideAggregate('incident');
agg.addAggregate('count', 'category'); 
agg.orderByDesc('category'); 
agg.query(); 
while (agg.next()) { 
  var category = agg.category;
  var count = agg.getAggregate('count', 'category');
  var agg2 = new GlideAggregate('incident');   
  agg2.addAggregate('count', 'category');
  agg2.orderBy('category');
  gs.info(category + ": Current number of incidents:" + count);
}
```

Output:

```
software: Current number of incidents:11
request: Current number of incidents:5
network: Current number of incidents:5
inquiry: Current number of incidents:28
hardware: Current number of incidents:8
database: Current number of incidents:2

```

## Scoped GlideAggregate - query\(\)

Issues the query and gets the results.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

```
var count = new GlideAggregate('incident');
count.addAggregate('COUNT');
count.query();
var incidents = 0;
if (count.next()) {
   incidents = count.getAggregate('COUNT');
}
gs.info('Number of incidents: ' + incidents);
```

## Scoped GlideAggregate - setAggregateWindow\(Number firstRow, Number lastRow\)

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

## Scoped GlideAggregate - setAggregateWorkflow\(Boolean workflow\)

Activates or deactivates the running of business rules for aggregate queries.

The session-level workflow setting \(`gs.getSession().setWorkflow()`\) overrides this method. When you deactivate the session workflow, query business rules do not run regardless of this method's setting.

**Warning:** Disabling the running of business rules, script engines, and audit can have a significant impact on your ServiceNow® instance and how it operates. Ensure that you thoroughly test this change before deploying it to production.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

workflow

</td><td>

Boolean

</td><td>

Flag that indicates whether business rules are active for the current GlideAggregate query.Valid values:

-   `true`: Activates business rules for the current query.
-   `false`: Deactivates business rules for the current query.

Default: `false`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to activate business rules for an aggregate query.

```
var incidentGA = new GlideAggregate('incident');
incidentGA.setAggregateWorkflow(true); // activate business rules for this aggregate
incidentGA.addAggregate('COUNT', 'sys_mod_count');
incidentGA.query();
```

The output includes business rule execution logs if the glide.businessrule.callstack property is in the System Properties \[sys\_properties\] table and set to `true`. Set this property to `false` when not needed to avoid performance impact.

```
BUSINESS RULE - About to execute business rule 'incident query' on incident:<span class = "session-log-bold-text"> </span>
BUSINESS RULE - Finished executing business rule 'incident query' on incident:<span class = "session-log-bold-text"> </span>
```

## Scoped GlideAggregate - setGroup\(Boolean b\)

Sets whether to group the return results.

<table id="table_w24_dxt_vr" class="parameters"><thead><tr><th>

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

Flag that indicates whether to group the results.

 Valid values:

-   true: Group the results.
-   false: Do not group the results.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var ga = new GlideAggregate('incident');
ga.addAggregate('COUNT', 'category');
 
ga.setGroup(true);
ga.groupBy("category");
 
ga.query();
 
while(ga.next()) {
  gs.info('Category ' + ga.category + ' ' + ga.getAggregate('COUNT', 'category'));
  }
```

Output:

```
Category database 2
Category hardware 7
Category inquiry 18
Category network 5
Category request 5
Category software 11
```

## Scoped GlideAggregate - setIntervalYearIncluded\(Boolean b\)

Sets whether to group results by year for day-of-week trends. These trends are created using the addTrend\(\) method with the **dayofweek** time interval.

Dependency: [Scoped GlideAggregate - addTrend\('&lt;fieldName&gt;', 'dayofweek'\)](c_GlideAggregateScopedAPI.md#).

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

