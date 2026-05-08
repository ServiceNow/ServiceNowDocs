---
title: PAScorecard - Scoped
description: The PAScorecard API enables you to fetch data about indicators and their associated records, such as breakdowns.Adds a query parameter to filter the returned scores.Perform a query based on the specified parameters and return the results as an object.Get the last query result as an object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PAScorecard- Scoped

The PAScorecard API enables you to fetch data about indicators and their associated records, such as breakdowns.

This API requires the Performance Analytics \(com.snc.pa.analytics\_center\) application and runs in the `SNC` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PAScorecard - addParam\(String parameter, String value\)

Adds a query parameter to filter the returned scores.

Call this method multiple times on the same PAScorecard object to pass multiple parameters, such as the indicator sys\_id and a breakdown sys\_id. After specifying all parameters, call query\(\) to run the query.

If you query a PAScorecard object with no parameters, the API returns a list of all indicators that are displayed on the Analytics Hub, with their scores.

<table id="table_pascorecard_parms" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

breakdown

</td><td>

String

</td><td>

Sys\_id of a breakdown to return chart information organized as defined by the breakdown. For example, the sys\_id of a priority breakdown to return separate task chart information for each priority value, such as the number of open incidents / Priority / 2 - High.

</td></tr><tr><td>

breakdown\_relation

</td><td>

String

</td><td>

Specify the sys\_id of a breakdown relation to break down the returned data using that relation. You can view available breakdown relations by setting the **include\_available\_breakdowns** parameter to `true`.

</td></tr><tr><td>

contains

</td><td>

String

</td><td>

Comma-separated list of names or descriptions to return results only from indicators with a matching value. All the comma-separated list items must match, or no results are returned: The list follows AND logic, not OR logic.

</td></tr><tr><td>

display

</td><td>

String

</td><td>

Flag that indicates the type of indicators to return.Valid values:

-   true: Return only indicators that display on the Analytics Hub.
-   all: Return all indicators.

Default: true

</td></tr><tr><td>

display\_value

</td><td>

String

</td><td>

Data retrieval operation for reference and choice fields.Based on this value, the display value and/or the actual value in the database are retrieved.

-   true returns display values for all of the fields.
-   false returns actual values from the database.
-   all returns both actual and display values.

Default: false

</td></tr><tr><td>

elements\_filter

</td><td>

String

</td><td>

Specify the sys\_id of an elements filter to apply that filter to the returned data.Data type: String

</td></tr><tr><td>

exclude\_reference\_link

</td><td>

Boolean

</td><td>

Flag that indicates whether to hide additional information provided for reference fields, such as the URI to the reference resource.Valid values:

-   true: Hide additional information provided for reference fields.
-   false: Do not hide additional information provided for reference fields.

Default: false

</td></tr><tr><td>

favorites

</td><td>

Boolean

</td><td>

Flag that indicates whether to return only indicators that are favorites of the querying user.Valid values:

-   true: Return only indicators that are favorites of the querying user.
-   false: Return all indicators.

Default: false

</td></tr><tr><td>

from

</td><td>

String

</td><td>

Earliest date to return scores from. Only scores from this date or later are returned. This parameter requires that **include\_scores** is set to `true`.

Format: ISO-8601 standard

</td></tr><tr><td>

include\_available\_aggregates

</td><td>

String

</td><td>

Flag that indicates whether to return all available aggregates for an indicator when no aggregate has been applied.Valid values:

-   true: Return all available aggregates for an indicator when no aggregate has been applied.
-   false: Return no aggregates.

Default: false

</td></tr><tr><td>

include\_available\_breakdowns

</td><td>

Boolean

</td><td>

Flag that indicates whether to return all available breakdowns for an indicator.Valid values:

-   true: Return all available breakdowns for an indicator.
-   false: Return no breakdowns.

Default: false

</td></tr><tr><td>

include\_forecast\_scores

</td><td>

Boolean

</td><td>

Flag that indicates whether to return the forecast\_scores element that contains an array of date-value pairs that define the forecast data for the Analytics Hub. This parameter requires that **include\_scores** is set to `true`.

Valid values:

-   true: Return the forecast\_scores element.
-   false: Do not return the forecast\_scores element.

Default: false

</td></tr><tr><td>

include\_realtime

</td><td>

Boolean

</td><td>

Flag that indicates whether to return the realtime\_enabled element which indicates if real-time scores are enabled for the indicator, and the realtime\_value element which contains the real-time score value. This parameter is not supported for formula indicators.Valid values:

-   true: Return the realtime\_enabled element.
-   false: Do not return the realtime\_enabled element.

Default: false

</td></tr><tr><td>

include\_scores

</td><td>

Boolean

</td><td>

Flag that indicates whether to return indicator scores for the entire time range selected on the Analytics Hub. If a value is not specified, this parameter defaults to false and returns only the most recent score value.To constrain the date range of the scores that are returned, combine this parameter with **from** and **to**.

Valid values:

-   true: Return indicator scores for the entire selected time range.
-   false: Do not return indicator scores for the entire selected time range.

Default: false

</td></tr><tr><td>

include\_target\_color\_scheme

</td><td>

Boolean

</td><td>

Flag that indicates whether to return the target\_color\_scheme element that contains the minimum and maximum values, and the color of each section of the target color scheme for the Analytics Hub.Valid values:

-   true: Return the target\_color\_scheme element.
-   false: Do not return the target\_color\_scheme element.

Default: false

</td></tr><tr><td>

include\_trendline\_scores

</td><td>

String

</td><td>

Flag that indicates whether to return the trendline\_scores element that contains an array of date-value pairs that define the Analytics Hub trendline.This parameter requires that **include\_scores** is set to `true`.

</td></tr><tr><td>

key

</td><td>

Boolean

</td><td>

Flag that indicates whether to return results only for key indicators.Valid values:

-   true: Return the trendline\_scores element.
-   false: Do not return the trendline\_scores element .

Default: false

</td></tr><tr><td>

limit

</td><td>

Number

</td><td>

Maximum number of scores to return.

</td></tr><tr><td>

page

</td><td>

String

</td><td>

Specify the page number. For example, when querying 20 indicators in the Analytics Hub with the default per\_page value \(10\), specify a page value of 2 to retrieve the Analytics Hub for 11-20.

</td></tr><tr><td>

per\_page

</td><td>

Number

</td><td>

Maximum number of indicators each query can return on a page.Default: 10

Maximum: 100

</td></tr><tr><td>

sortby

</td><td>

String

</td><td>

Value to use when sorting results.Valid values:

-   bullet
-   change
-   changeperc
-   date
-   default
-   direction
-   duedate
-   frequency
-   gap
-   gapperc
-   group
-   indicator\_group
-   name
-   order
-   target
-   trend
-   value

Default: value

</td></tr><tr><td>

sortdir

</td><td>

String

</td><td>

Sort direction.Valid values:

-   asc: Denotes ascending
-   des: Denotes descending

Default: Descending

</td></tr><tr><td>

step

</td><td>

Number

</td><td>

Numeric value to skip scores, based on the indicator frequency. For example, specify a value of 3 to return only scores from every third day for a daily indicator, or from every third week for a weekly indicator.

</td></tr><tr><td>

tags

</td><td>

String

</td><td>

Enter an indicator group sys\_id to return the indicators in that group. Do not use **uuid** with this parameter.

</td></tr><tr><td>

target

</td><td>

Boolean

</td><td>

Flag that indicates whether to return results only for indicators that have a target set on the Analytics Hub.Valid values:

-   true: Only return results for indicators that have a target set.
-   false: Return results for all applicable indicators.

Default: false

</td></tr><tr><td>

to

</td><td>

String

</td><td>

Latest date from which to return scores. Only scores from this date or earlier are returned.This parameter requires that **include\_scores** is set to `true`.

</td></tr><tr><td>

uuid

</td><td>

String

</td><td>

Enter a colon-separated list of sys\_id values to specify which indicators, breakdowns, aggregates, and domains to query. The parameter follows this format:&lt;indicator\_sys\_id&gt;:&lt;breakdown\_sys\_id&gt;:&lt;elements\_filter\_sys\_id or element\_sys\_ids&gt;:&lt;lvl-2 breakdown\_sys\_id&gt;:&lt;lvl-2 elements\_filter\_sys\_id or element\_sys\_ids&gt;:&lt;aggregate\_sys\_id&gt;;&lt;domain\_sys\_id&gt;

The parameter must begin with the sys\_id of an indicator record. Optionally, you can append the sys\_id values of a breakdown and breakdown element to group the response based on the breakdown, and the sys\_id of an aggregate to apply that aggregate. You can use a breakdown with an aggregate, or use only one.

For information about obtaining the sys\_id values of records, see Unique record identifier \(sys\_id\).

**Note:** If an indicator is configured to use a **Default time series**, all Analytics Hub values for that indicator use that time series aggregation.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

In this example, the uuid parameter specifies the Number of open incidents indicator, and the breakdown parameter specifies the Priority breakdown. Both parameters have the sys\_id of the respective records as their values. The query\(\) function returns the results as an object.

```
var sc = new SNC.PAScorecard(); //in a scoped app, do not use the SNC namespace
sc.addParam('uuid', 'fb007202d7130100b96d45a3ce6103b4');       // Number of open incidents
sc.addParam('breakdown', '0df47e02d7130100b96d45a3ce610399');  // by Priority
var result = sc.query();  // Query results, which are returned as an object
for (var i = 0; i < result.length; i++)
gs.info(result[i].name + ': ' + result[i].value + ' ' + result[i].unit.display_value);

```

## PAScorecard - query\(\)

Perform a query based on the specified parameters and return the results as an object.

Before calling this method, configure parameters for the PAScorecard object by calling addParam\(String parameter, String value\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The PAScorecard object.|

## PAScorecard - result\(\)

Get the last query result as an object.

This method does not perform a query. To perform a query before returning the result, use query\(\).

This function cannot run in a scope other than global.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The results from the last query, returned as a JS object.|

