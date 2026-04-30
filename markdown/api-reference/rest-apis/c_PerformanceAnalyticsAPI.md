---
title: Scorecards API
description: The Scorecards API provides endpoints that enable you to query data about Performance Analytics indicators. The query parameters equate to the functions available on the Analytics Hub for drilling down into an indicator.Retrieves details about indicators from the Analytics Hub .
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 23
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Scorecards API

The Scorecards API provides endpoints that enable you to query data about Performance Analytics indicators. The query parameters equate to the functions available on the Analytics Hub for drilling down into an indicator.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Scorecards - GET /now/pa/scorecards

Retrieves details about indicators from the Analytics Hub.

Access to tables through the REST API is restricted by BasicAuth. Access control lists defined for tables are enforced to restrict access to data.

To make queries using the Performance Analytics API, you must also have the pa\_viewer role.

Almost all queries use the **sysparm\_uuid** parameter. This parameter consists of the indicator sys\_id followed by a colon-separated list of additional, optional sys\_ids. The **sysparm\_uuid** is always the first parameter.

### URL format

Versioned URL: `/api/now/{api_version}/pa/scorecards`

Default URL: `/api/now/pa/scorecards`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_breakdown

</td><td id="entry_rlx_4v3_pw">

Sys\_id of a breakdown to return chart information organized as defined by the breakdown. For example, the sys\_id of a priority breakdown to return separate task chart information for each priority value, such as the number of open incidents / Priority / 2 - High.Data type: String

</td></tr><tr><td>

sysparm\_breakdown\_relation

</td><td id="entry_w2s_xw3_pw">

Sys\_id of a breakdown relation to break down the returned data using that relation.Data type: String

</td></tr><tr><td>

sysparm\_contains

</td><td id="entry_vqh_rv3_pw">

Comma-separated list of names or descriptions to return results only from indicators with a matching value. All the comma-separated list items must match, or no results are returned: The list follows AND logic, not OR logic.Data type: String

</td></tr><tr><td>

sysparm\_display

</td><td>

Flag that indicates the type of indicators to return.Valid values:

-   true: Return only indicators that display on the Analytics Hub.
-   all: Return all indicators.

Data type: String

Default: true

</td></tr><tr id="rest_api_sysparm_display_value_prm"><td>

sysparm\_display\_value

</td><td>

Determines the type of data returned, either the actual values from the database or the display values of the fields. Display values are manipulated based on the actual value in the database and user or system settings and preferences.If returning display values, the value that is returned is dependent on the field type.

-   Choice fields: The database value may be a number, but the display value will be more descriptive.
-   Date fields: The database value is in UTC format, while the display value is based on the user's time zone.
-   Encrypted text: The database value is encrypted, while the displayed value is unencrypted based on the user's encryption context.
-   Reference fields: The database value is sys\_id, but the display value is a display field of the referenced record.

Data type: String

Valid values:

-   true: Returns the display values for all fields.
-   false: Returns the actual values from the database.
-   all: Returns both actual and display values.

Default: false

**Note:** There is no preferred method for setting this parameter. However, specifying the display value may cause performance issues since it is not reading directly from the database and may include referencing other fields and records. For more information on display values and actual values, see [Table API FAQs \(KB0534905\).](https://support.servicenow.com/kb_view.do?sysparm_article=KB0534905)

</td></tr><tr><td>

sysparm\_elements\_filter

</td><td id="entry_mbq_xw3_pw">

Sys\_id of an elements filter to apply to the returned data.Data type: String

</td></tr><tr><td>

sysparm\_exclude\_reference\_link

</td><td>

Flag that indicates whether to hide additional information provided for reference fields, such as the URI to the reference resource.Valid values:

-   true: Hide additional information provided for reference fields.
-   false: Do not hide additional information provided for reference fields.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_favorites

</td><td>

Flag that indicates whether to return only indicators that are favorites of the querying user.Valid values:

-   true: Return only indicators that are favorites of the querying user.
-   false: Return all indicators.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_from

</td><td>

Earliest date to return scores from. Only scores from this date or later are returned. This parameter requires that **include\_scores** is set to `true`.

Format: ISO-8601 standard

Date type: String

</td></tr><tr><td>

sysparm\_include\_aggregates

</td><td>

Flag that indicates whether to return all possible aggregates for an indicator, including aggregates that have already been applied.Valid values:

-   true: Return all possible aggregates for an indicator, including aggregates that have already been applied.
-   false: Return no aggregates.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_include\_available\_aggregates

</td><td>

Flag that indicates whether to return all available aggregates for an indicator when no aggregate has been applied.Valid values:

-   true: Return all available aggregates for an indicator when no aggregate has been applied.
-   false: Return no aggregates.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_include\_available\_breakdowns

</td><td>

Flag that indicates whether to return all available breakdowns for an indicator.Valid values:

-   true: Return all available breakdowns for an indicator.
-   false: Return no breakdowns.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_include\_forecast\_scores

</td><td>

Flag that indicates whether to return the forecast\_scores element that contains an array of date-value pairs that define the forecast data for the Analytics Hub. This parameter requires that the **include\_scores** parameter is also set to `true`.

Valid values:

-   true: Return the forecast\_scores element.
-   false: Do not return the forecast\_scores element.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_include\_realtime

</td><td>

Flag that indicates whether to return the realtime\_enabled element which indicates if real-time scores are enabled for the indicator, and the realtime\_value element which contains the real-time score value. This parameter is not supported for formula indicators.Valid values:

-   true: Return the realtime\_enabled element.
-   false: Do not return the realtime\_enabled element.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_include\_score\_notes

</td><td>

Flag that indicates whether to return all notes associated with the score. The note element contains the note text as well as the author and timestamp when the note was added.Valid values:

-   true: Return all notes associated with the score.
-   false: Do not return all notes associated with the score.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_include\_scores

</td><td>

Flag that indicates whether to return indicator scores for the entire time range selected on the Analytics Hub. If a value is not specified, this parameter defaults to false and returns only the most recent score value. To constrain the date range of the scores that are returned, combine this parameter with **from** and **to**.

Valid values:

-   true: Return indicator scores for the entire selected time range.
-   false: Do not return indicator scores for the entire selected time range.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_include\_target\_color\_scheme

</td><td>

Flag that indicates whether to return the target\_color\_scheme element that contains the minimum and maximum values, and the color of each section of the target color scheme for the Analytics Hub.Valid values:

-   true: Return the target\_color\_scheme element.
-   false: Do not return the target\_color\_scheme element.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_include\_trendline\_scores

</td><td>

Flag that indicates whether to return the trendline\_scores element that contains an array of date-value pairs that define the Analytics Hub trendline. This parameter requires that the **include\_scores** parameter is also set to `true`.

Valid values:

-   true: Return the trendline\_scores element.
-   false: Do not return the trendline\_scores element.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_key

</td><td>

Flag that indicates whether to return results only for key indicators.Valid values:

-   true: Return the trendline\_scores element.
-   false: Do not return the trendline\_scores element .

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of scores to return.Data type: Number

</td></tr><tr><td>

sysparm\_page

</td><td id="entry_fpc_xw3_pw">

Page number. For example, when querying 20 indicators with the default sysparm\_per\_page value \(10\), specify a sysparm\_page value of 2 to retrieve indicators 11-20.Data type: Number

</td></tr><tr><td>

sysparm\_per\_page

</td><td>

Maximum number of indicators each query can return on a page.Default: 10

Maximum: 100

Data type: Number

</td></tr><tr><td>

sysparm\_sortby

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

Data type: String

Default: value

</td></tr><tr><td>

sysparm\_sortdir

</td><td>

Sort direction.Valid values:

-   asc: Denotes ascending
-   des: Denotes descending

Data type: String

Default: Descending

</td></tr><tr><td>

sysparm\_step

</td><td>

Numeric value to skip scores, based on the indicator frequency. For example, specify a value of 3 to return only scores from every third day for a daily indicator, or from every third week for a weekly indicator.Data type: Number

</td></tr><tr><td>

sysparm\_tags

</td><td id="entry_c3k_rv3_pw">

Indicator group sys\_id in which to return the indicators of that group. Do not use **sysparm\_uuid** with this parameter.You cannot obtain the sys\_id of an indicator group through this API. Instead, get the sys\_id from the indicator group record. For more information about obtaining sys\_ids from records, see [Unique record identifier \(sys\_id\)](https://servicenow.com/docs?context=platform_unique-record-id&version=sandiego).

 Data type: String

</td></tr><tr><td>

sysparm\_target

</td><td>

Flag that indicates whether to return results only for indicators that have a target set on the Analytics Hub.Valid values:

-   true: Only return results for indicators that have a target set.
-   false: Return results for all applicable indicators.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_to

</td><td>

Latest date from which to return scores. Only scores from this date or earlier are returned. This parameter requires that **include\_scores** is set to `true`.

Data type: String

Format: ISO-8601 standard

</td></tr><tr><td>

sysparm\_uuid

</td><td id="entry_p2r_4v3_pw">

Colon-separated list of sys\_id values to specify which indicators, breakdowns, aggregates, and domains to query. The parameter follows this format:&lt;indicator\_sys\_id&gt;:&lt;breakdown\_sys\_id&gt;:&lt;elements\_filter\_sys\_id or element\_sys\_ids&gt;:&lt;lvl-2 breakdown\_sys\_id&gt;:&lt;lvl-2 elements\_filter\_sys\_id or element\_sys\_ids&gt;:&lt;aggregate\_sys\_id&gt;;&lt;domain\_sys\_id&gt;

 The parameter must begin with the sys\_id of an indicator record. Optionally, you can append the sys\_id values of a breakdown and breakdown element to group the response based on the breakdown, and the sys\_id of an aggregate to apply that aggregate. You can use a breakdown with an aggregate, or use only one.

 **Note:** If an indicator is configured to use a **Default time series**, all values that this API retrieves for that indicator use the selected aggregate.

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|Depends on request parameters.||

### Retrieving all indicators on the Analytics Hub

```
# Request a list of all indicators that
# are displayed in the Analytics Hub,
# including their unique record identifiers.

curl --verbose --user "user:password" \
–-header "Accept:application/json" \
"https://instance.service-now.com/api/now/v1/pa/scorecards"
```

```
// The following response is truncated
// to show only the Number of open incidents
// indicator, which is used in the other
// examples on this page.
{
  "result" : [
...
  
    {
      "change_formatted" : "",
      "key" : false,
      "value_unit" : "",
      "value_formatted" : "",
      "period_title" : null,
      "gapperc" : null,
      "gap" : null,
      "target" : null,
      "period" : null,
      "target_formatted" : "",
      "favorite" : false,
      "direction_label" : "Minimize",
      "uuid" : "fb007202d7130100b96d45a3ce6103b4",
      "name" : "Number of open incidents",
      "value_color" : "#000000",
      "frequency_label" : "Daily",
      "change" : null,
      "gap_formatted" : "",
      "gapperc_formatted" : "",
      "value" : null,
      "unit" : {
        "display_value" : "#",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value" : "17b365e2d7320100ba986f14ce6103ad"
      },
      "changeperc_formatted" : "",
      "direction" : 2,
      "frequency" : 10,
      "precision" : 0,
      "changeperc" : null,
      "indicator" : {
        "display_value" : "Number of open incidents",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value" : "fb007202d7130100b96d45a3ce6103b4"
      },
      "description" : "Number of incidents open based on resolved date is empty."
    },
...
    
  ]
}
```

### Return indicator details

You can query the Analytics Hub for a particular indicator by providing the **sysparm\_uuid** parameter with an indicator sys\_id value.

```

# In this example, you use the sys ID for the 
# Number of open incidents indicator,
# which you retrieved in the first example, 
# when you got all the indicators in the 
# Analytics Hub:
# "uuid" : "fb007202d7130100b96d45a3ce6103b4",
# "name" : "Number of open incidents"

curl --verbose --user "user:password" \
--header "Accept:application/json" \
"https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4"
```

```
{
  "result" : [
    {
      "change_formatted" : "",
      "key" : false,
      "value_unit" : "",
      "value_formatted" : "",
      "period_title" : null,
      "gapperc" : null,
      "gap" : null,
      "target" : null,
      "period" : null,
      "target_formatted" : "",
      "favorite" : false,
      "direction_label" : "Minimize",
      "uuid" : "fb007202d7130100b96d45a3ce6103b4",
      "name" : "Number of open incidents",
      "value_color" : "#000000",
      "frequency_label" : "Daily",
      "change" : null,
      "gap_formatted" : "",
      "gapperc_formatted" : "",
      "value" : null,
      "unit" : {
        "display_value" : "#",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value" : "17b365e2d7320100ba986f14ce6103ad"
      },
      "changeperc_formatted" : "",
      "direction" : 2,
      "frequency" : 10,
      "precision" : 0,
      "changeperc" : null,
      "indicator" : {
        "display_value" : "Number of open incidents",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value" : "fb007202d7130100b96d45a3ce6103b4"
      },
      "description" : "Number of incidents open based on resolved date is empty."
    }
  ]
}
```

### Return all breakdowns and aggregates for an indicator

Query a list of available breakdowns and aggregates for an indicator by setting the **sysparm\_include\_available\_breakdowns** and **sysparm\_include\_available\_aggregates** parameters to true.

```
curl -v -u "user:password" -H "Accept:application/json" \
"https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_include_available_breakdowns=true&sysparm_include_available_aggregates=true"
```

```
{
  "result" : [
    {
      "key" : false,
      "change_formatted" : "",
      "aggregates" : [
        {
          "display_value" : "7d running SUM",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_aggregates/89ea4c11d7001100ba986f14ce6103dc",
          "value" : "89ea4c11d7001100ba986f14ce6103dc"
        },
        {
          "display_value" : "28d running SUM",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_aggregates/4dfa4c11d7001100ba986f14ce6103e2",
          "value" : "4dfa4c11d7001100ba986f14ce6103e2"
        },
        {
          "display_value" : "30d running SUM",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_aggregates/3e409011d7001100ba986f14ce610319",
          "value" : "3e409011d7001100ba986f14ce610319"
        },
        // Aggregates truncated for brevity
        
      ],
      "changeperc" : null,
      "value_formatted" : "",
      "period_title" : null,
      "gapperc" : null,
      "value_unit" : "",
      "target" : null,
      "period" : null,
      "target_formatted" : "",
      "favorite" : false,
      "gap" : null,
      "direction_label" : "Minimize",
      "uuid" : "fb007202d7130100b96d45a3ce6103b4",
      "name" : "Number of open incidents",
      "value_color" : "#000000",
      "frequency_label" : "Daily",
      "change" : null,
      "gap_formatted" : "",
      "gapperc_formatted" : "",
      "value" : null,
      "unit" : {
        "display_value" : "#",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value" : "17b365e2d7320100ba986f14ce6103ad"
      },
      "breakdowns" : [
        {
          "display_value" : "Priority",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_breakdowns/0df47e02d7130100b96d45a3ce610399",
          "value" : "0df47e02d7130100b96d45a3ce610399"
        },
        {
          "display_value" : "Category",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_breakdowns/1f918835d7231100b96d45a3ce6103fe",
          "value" : "1f918835d7231100b96d45a3ce6103fe"
        },
        {
          "display_value" : "Assignment Group",
          "link" : "https://instance.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
          "value" : "baec0752bf130100b96dac808c0739ed"
        },
        // Information for State and Age indicators truncated
        
      ],
      "changeperc_formatted" : "",
      "frequency" : 10,
      "precision" : 0,
      "direction" : 2,
      "indicator" : {
        "display_value" : "Number of open incidents",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value" : "fb007202d7130100b96d45a3ce6103b4"
      },
      "description" : "Number of incidents open based on resolved date is empty."
    }
  ]
}
```

### Return a time series aggregation of indicator scores

```
# Apply the 7d running SUM aggregate returned in
# the previous response to the
# Analytics Hub using the
# **sysparm\_uuid** value
# with the sys_id of the aggregate.

curl -v -u "user:password" -H "Accept:application/json" \
"https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:89ea4c11d7001100ba986f14ce6103dc"
```

```
{
  "result" : [
    {
      "key" : false,
      "change_formatted" : "",
      "value_unit" : "",
      "value_formatted" : "",
      "period_title" : null,
      "aggregate" : {
        "display_value" : "7d running SUM",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_aggregates/89ea4c11d7001100ba986f14ce6103dc",
        "value" : "89ea4c11d7001100ba986f14ce6103dc"
      },
      "gapperc" : null,
      "target" : null,
      "period" : null,
      "target_formatted" : "",
      "favorite" : false,
      "gap" : null,
      "direction_label" : "Minimize",
      "uuid" : "fb007202d7130100b96d45a3ce6103b4:89ea4c11d7001100ba986f14ce6103dc",
      "name" : "Number of open incidents / 7d running SUM",
      "value_color" : "#000000",
      "frequency_label" : "Daily",
      "change" : null,
      "gap_formatted" : "",
      "gapperc_formatted" : "",
      "value" : null,
      "unit" : {
        "display_value" : "#",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value" : "17b365e2d7320100ba986f14ce6103ad"
      },
      "changeperc_formatted" : "",
      "direction" : 2,
      "frequency" : 10,
      "precision" : 0,
      "changeperc" : null,
      "indicator" : {
        "display_value" : "Number of open incidents",
        "link" : "https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value" : "fb007202d7130100b96d45a3ce6103b4"
      },
      "description" : "Number of incidents open based on resolved date is empty."
    }
  ]
}
```

### Return the elements for a breakdown

```
# To get the scores associated with
# each element of a breakdown and
# the sys_ids of those elements, pass
# the **sysparm\_breakdown**
# parameter with the sys_id of the breakdown.
# In this example, you get the elements of
# the Assignment Group breakdown for the
# Number of open incidents indicator.
# From the previous example, you have the
# sys_id of `fb007202d7130100b96d45a3ce6103b4`
# for the Number of open incidents indicator and the
# sys_id of `baec0752bf130100b96dac808c0739ed`
# for the Assignment Group breakdown.

curl -v -u "user:password" -H "Accept:application/json" \
"https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_breakdown=baec0752bf130100b96dac808c0739ed"
```

```
// The response consists of a set of
// `indicator` objects, each
// containing one `element` object.
// The `element` objects each
// contain the name and sys_id of an object.
// Because the information about the indicator
// is the same for each `indicator`
// object, in this example only the first 
// `indicator` object is given
// in detail.
{
  "result":[
    { 
      "indicator": {
        "display_value":"Number of open incidents",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value":"fb007202d7130100b96d45a3ce6103b4"
      },
      "gap_formatted":"",
      "benchmarking":false,
      "frequency_label":"Daily",
      "changeperc_formatted":"0.0%",
      "direction_label":"Minimize",
      "precision":0,
      "breakdown": {
        "display_value":"Assignment Group",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value":"baec0752bf130100b96dac808c0739ed"
      },
      "personal_target":null,
      "description":"Number of incidents open based on resolved date is empty.",
      "value_color":"#455464",
      "uuid":"fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:unmatched",
      "frequency":10,
      "gap":null,
      "value_unit":"14",
      "indicator_frequency":10,
      "value":14.0,
      "indicator_aggregate":1,
      "facts_table": {
        "name":"incident",
        "label":"Incidents"
      },
      "key":false,
      "indicator_frequency_label":"Daily",
      "direction":2,
      "element": {
        "display_value":"Unassigned",      //Element name
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/unmatched",
        "value":"unmatched"                //No sys_id for unmatched scores
      },
      "period_title":"Jul 22",
      "period":"Jul 22",
      "target_formatted":"",
      "change":0.0,
      "gapperc_formatted":"",
      "query":"opened_atONToday@javascript:gs.beginningOfToday()@javascript:gs.endOfToday()^ORopened_at<javascript:gs.beginningOfToday()^resolved_atISEMPTY^ORresolved_at>javascript:gs.endOfToday()^state!=8",
      "realtime_enabled":true,
      "changeperc":0.0,
      "target":null,
      "unit": {
        "display_value":"#",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "type":"formatted",
        "value":"17b365e2d7320100ba986f14ce6103ad"
      },
      "value_formatted":"14",             // Score where Assignment Group=Unassigned
      "name":"Number of open incidents > Assignment Group = Unassigned",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
    {"indicator": {
      
      "element": {
        "display_value":"Software",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/8a4dde73c6112278017a6a4baf547aa7",
        "value":"8a4dde73c6112278017a6a4baf547aa7"    // sys_id of element Software
      },
      ...
  
      "value_formatted":"6",                         // Score where Assignment Group: Software
      "name":"Number of open incidents > Assignment Group = Software",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
    {"indicator": {
      ...
   
      "element": {
        "display_value":"Service Desk",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/d625dccec0a8016700a222a0f7900d06",
        "value":"d625dccec0a8016700a222a0f7900d06"   // sys_id of element Service Desk
      },
  
      ...
      
      "value_formatted":"5",                        // Score for Assignment Group: Service Desk
      "name":"Number of open incidents > Assignment Group = Service Desk",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
    {"indicator": {
  
      ...
      
      "element": {
        "display_value":"Hardware",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/8a5055c9c61122780043563ef53438e3",
        "value":"8a5055c9c61122780043563ef53438e3"   // sys_id for element Hardware
      },
  
      ...
      
      "value_formatted":"3",                         // Score for Assignment Group: Hardware
      "name":"Number of open incidents > Assignment Group = Hardware",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
    {"indicator": {
  
  ...

      "element": {
        "display_value":"Network",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/287ebd7da9fe198100f92cc8d1d2154e",
        "value":"287ebd7da9fe198100f92cc8d1d2154e"},  // sys_id for element Network
  
... 

      "value_formatted":"3",                          // Score for Assignment Group: Network
      "name":"Number of open incidents > Assignment Group = Network",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    },
  ...
  ]
...
}

```

### Return an indicator filtered by a breakdown and element

```
# The GET request gets the details for 
# the indicator Number of open
# incidents, where the Priority of the
# incident is 1 - Critical. The sys_id
# values for the indicator, the 
# Priority breakdown, and the  1 - 
# Critical element are all passed in
# the sysparm_uuid parameter.

curl --verbose --user "username":"password" \
--header "Accept:application/json" \
"https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3"
```

```
{
// The request is made Dec 12. The
// score is 76, which is unchanged from
// Dec 11, and which exceeds the
// target of 70.
  "result": [ 
    { 
      "indicator": {
        "display_value":"Number of open incidents",
        "link":"https://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value":"fb007202d7130100b96d45a3ce6103b4"
      },
      "gap_formatted":"-6",
      "benchmarking":false,
      "frequency_label":"Daily",
      "changeperc_formatted":"0.0%",
      "direction_label":"Minimize",
      "precision":0,
      "breakdown": {
        "display_value":"Priority",
        "link":"https://instance.service-now.com/api/now/v1/table/pa_breakdowns/0df47e02d7130100b96d45a3ce610399",
        "value":"0df47e02d7130100b96d45a3ce610399"
      },
      "personal_target":null,
      "description":"Number of incidents open based on resolved date is empty.",
      "value_color":"#ff8c00",
      "uuid":"fb007202d7130100b96d45a3ce6103b4:0df47e02d7130100b96d45a3ce610399:5f012106db5123003ee8f93baf9619bd",
      "frequency":10,
      "gap":-6.0,
      "value_unit":"76",
      "indicator_frequency":10,
      "value":76.0,
      "indicator_aggregate":1,
      "facts_table": {
        "name":"incident",
        "label":"Incidents"
      },
      "key":false,
      "indicator_frequency_label":"Daily",
      "direction":2,
      "element": {
        "display_value":"1 - Critical",
        "link":"https://instance.service-now.com/api/now/v1/table/sys_choice/5f012106db5123003ee8f93baf9619bd",
        "value":"5f012106db5123003ee8f93baf9619bd"
      },
      "period_title":"Dec 12",
      "period":"Dec 12",
      "target_formatted":"70",
      "change":0.0,
      "gapperc_formatted":"-8.6%",
      "query":"opened_atONToday@javascript:gs.beginningOfToday()@javascript:gs.endOfToday()^ORopened_at<javascript:gs.beginningOfToday()^resolved_atISEMPTY^ORresolved_at>javascript:gs.endOfToday()^state!=8^priority=1^EQ",
      "realtime_enabled":true,
      "changeperc":0.0,
      "target":70.0,
      "unit": {
        "display_value":"#",
        "link":"https://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "type":"formatted","value":"17b365e2d7320100ba986f14ce6103ad"
      },
      "value_formatted":"76",
      "name":"Number of open incidents > Priority = 1 - Critical",
      "gapperc":-0.08571428571428572,
      "change_formatted":"0",
      "favorite":true,
      "personal_target_formatted":""
    }
  ]
}
```

### Return the indicator broken down by location

```
curl -v -u "user:password" -H "Accept:application/json" \
"https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_breakdown=656d5662eb23310065deac6aa206fee7"
```

```
{
  "result": [
    {
      ...
      "element": {
        "display_value": "San Diego",
        "link": "https://<instance>.service-now.com/api/now/v1/table/cmn_location/108752c8c611227501d4ab0e392ba97f",
        "value": "108752c8c611227501d4ab0e392ba97f",
        "longitude": -117.15726,
        "latitude": 32.71533
      },
      ...
    }
    {
      ...
      "element": {
        "display_value": "Florida",
        "link": "https://<instance>.service-now.com/api/now/v1/table/cmn_location/8e3e85f037d0200044e0bfc8bcbe5d14",
        "value": "8e3e85f037d0200044e0bfc8bcbe5d14",
        "longitude": -95.71289,
        "latitude": 37.09024
      },
      ...
    }
  ]
}
```

### Return first- and second-level breakdown scores

To apply multiple breakdowns, append multiple breakdown sys\_ids to the sysparm\_uuid parameter.

```
# In this example, the data is broken
# down by priority to show priority 1
# incidents, and by category to show
# database incidents.

curl -v -u "user:password" -H "Accept:application/json" \
"https://instance.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3:1f918835d7231100b96d45a3ce6103fe:9e418d40200331007665978299a805c1"
```

```
{
  "result": [
    {
      "value_formatted": "",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "http://instance.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      "gapperc": null,
      "change": null,
      "value_color": "#000000",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "",
      "direction_label": "Minimize",
      "period_title": null,
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Priority / 1 - Critical / Category / Database",
      "value": null,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "1 - Critical",
        "link": "http://instance.service-now.com/api/now/v1/table/sys_choice/e5900140200331007665978299a805f3",
        "value": "e5900140200331007665978299a805f3"
      },
      "precision": 0,
      "element_level2": {
        "display_value": "Database",
        "link": "http://instance.service-now.com/api/now/v1/table/sys_choice/9e418d40200331007665978299a805c1",
        "value": "9e418d40200331007665978299a805c1"
      },
      "breakdown": {
        "display_value": "Priority",
        "link": "http://instance.service-now.com/api/now/v1/table/pa_breakdowns/0df47e02d7130100b96d45a3ce610399",
        "value": "0df47e02d7130100b96d45a3ce610399"
      },
      "period": null,
      "favorite": false,
      "change_formatted": "",
      "unit": {
        "display_value": "#",
        "link": "http://instance.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "breakdown_level2": {
        "display_value": "Category",
        "link": "http://instance.service-now.com/api/now/v1/table/pa_breakdowns/1f918835d7231100b96d45a3ce6103fe",
        "value": "1f918835d7231100b96d45a3ce6103fe"
      },
      "target": null,
      "changeperc": null,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3:1f918835d7231100b96d45a3ce6103fe:9e418d40200331007665978299a805c1",
      "gapperc_formatted": "",
      "value_unit": "",
      "gap": null
    }
  ]
}
```

### Return scores across a range of dates for two levels of breakdown

To request a list of individual scores for all available dates, set the sysparm\_include\_scores parameter to true.

To specify the date range of scores, also use the **sysparm\_from** and **sysparm\_to** parameters.

```
# In this example, the level 1 breakdown and
# element are Assignment Group: Software
# (sys_id `baec0752bf130100b96dac808c0739ed`
# and `8a4dde73c6112278017a6a4baf547aa7`).
# The level 2 breakdown and element are Priority: 1 -
# Critical (sys_id `0df47e02d7130100b96d45a3ce610399`
# and `e5900140200331007665978299a805f3`).
# Only scores on and after 30 November 2018 are returned.

curl -v -u "resttest:resttest" -H "Accept:application/json" \
"https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3&sysparm_include_scores=true&sysparm_from=2018-11-30"
```

```
{
  "result": [
    { "indicator": {
        "display_value":"Number of open incidents",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value":"fb007202d7130100b96d45a3ce6103b4"
      },
      "gap_formatted":"",
      "benchmarking":false,
      "frequency_label":"Daily",
      "scores": [
        { "end_at":"2018-12-04",
          "period":"Dec 04",
          "value_formatted":"2",
          "start_at":"2018-12-04",
          "value":2.0
        },

        ...
       
        { "end_at":"2018-11-30",
          "period":"Nov 30",
          "value_formatted":"0",
          "start_at":"2018-11-30",
          "value":0.0
        }
      ],
      "changeperc_formatted":"",
      "direction_label":"Minimize",
      "precision":0,
      "breakdown": {                      //First-level breakdown
        "display_value":"Assignment Group",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value":"baec0752bf130100b96dac808c0739ed"
      },
      "personal_target":null,
      "description":"Number of incidents open based on resolved date is empty.",
      "value_color":"#455464",
      "uuid":"fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7:0df47e02d7130100b96d45a3ce610399:e5900140200331007665978299a805f3",
      "frequency":10,
      "gap":null,
      "value_unit":"2",
      "indicator_frequency":10,
      "value":2.0,
      "indicator_aggregate":1,
      "key":false,
      "indicator_frequency_label":"Daily",
      "direction":2,
      "element": {                        //First-level breakdown element
        "display_value":"Software",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/8a4dde73c6112278017a6a4baf547aa7",
        "value":"8a4dde73c6112278017a6a4baf547aa7"
      },
      "period_title":"Dec 04",
      "period":"Dec 04",
      "target_formatted":"",
      "change":2.0,
      "gapperc_formatted":"",
      "realtime_enabled":false,
      "changeperc":null,
      "target":null,
      "unit":{ 
        "display_value":"#",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "type":"formatted",
        "value":"17b365e2d7320100ba986f14ce6103ad"
      },
      "value_formatted":"2",               //Second-level breakdown and element
      "name":"Number of open incidents > Assignment Group = Software > Priority = e5900140200331007665978299a805f3",
      "gapperc":null,
      "change_formatted":"2",
      "favorite":false,
      "breakdown_level2": {
        "display_value":"Priority",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/0df47e02d7130100b96d45a3ce610399",
        "value":"0df47e02d7130100b96d45a3ce610399"
      },
      "personal_target_formatted":""
    }
  ]
}
```

### Return breakdown relations for a breakdown and element

To obtain the sys\_id values for all breakdown relations associated with an indicator, use the **sysparm\_include\_available\_breakdowns** parameter. In the **sysparm\_uuid**parameter, include the sys\_ids of the first-level breakdown and element whose relations you want to find.

```
# In this example, the **sysparm\_uuid**
# parameter includes the sys_id for the 
# Assignment Group breakdown and the
# sys_id for the Software element.
# The sys_id of the Assignment Group
# was obtained in the example where all
# breakdowns and aggregates were returned.
# The sys_id of the Software element was
# obtained in the previous example, where
# all the elements of Assignment Group were
# returned. The sys_id of the Assignment
# Group breakdown is
# `baec0752bf130100b96dac808c0739ed`
# and of the Software element is
# `8a4dde73c6112278017a6a4baf547aa7`.
# The breakdown relation is obtained for the
# Number of open incidents indicator,
# whose sys_id is
# `fb007202d7130100b96d45a3ce6103b4`.

curl -v -u "user:password" -H "Accept:application/json" "https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7&sysparm_include_available_breakdowns=true"
```

```
{
  "result": [
    {
      "value_formatted": "37",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      "gapperc": null,
      "change": 9.0,
      "value_color": "#455464",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "32.1%",
      "direction_label": "Minimize",
      "period_title": "Jul 22",
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Assignment Group / Software",
      "value": 37.0,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "Software",
        "link": "https://<instance>.service-now.com/api/now/v1/table/sys_user_group/287ee6fea9fe198100ada7950d0b1b73",
        "value": "8a4dde73c6112278017a6a4baf547aa7"
      },
      "precision": 0,
      "breakdowns": [
        // Information about each breakdown
        
      ],
      "breakdown_relations": [
        {
          "display_value": "Child Groups",
          "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdown_relations/301fd511eb23310065deac6aa206fe31",
          "value": "301fd511eb23310065deac6aa206fe31"
        },
        {
          "display_value": "Parent Group",
          "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdown_relations/790b6e11eb23310065deac6aa206fe1c",
          "value": "790b6e11eb23310065deac6aa206fe1c"
        },
        {
          "display_value": "Sibling Groups",
          "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdown_relations/15e15a12eb233100871aac6aa206fe59",
          "value": "15e15a12eb233100871aac6aa206fe59"
        }
      ],
      "breakdown": {
        "display_value": "Assignment Group",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value": "baec0752bf130100b96dac808c0739ed"
      },
      "period": "Jul 22",
      "favorite": false,
      "change_formatted": "9",
      "unit": {
        "display_value": "#",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "target": null,
      "changeperc": 0.32142857142857145,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7",
      "gapperc_formatted": "",
      "value_unit": "6",
      "gap": null
    }
  ]
}
```

### Return indicator using a breakdown relation

To use a breakdown relation, include the sys\_id values of the indicator, breakdown, and element in the **sysparm\_uuid** parameter, and the sys\_id of the breakdown relation in the **sysparm\_breakdown\_relation** parameter.

```
# This example returns the
# Sibling Group values for Assignment
# Group: Software from the previous example.

curl -v -u "user:password" -H "Accept:application/json" \
"https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:8a4dde73c6112278017a6a4baf547aa7&sysparm_breakdown_relation=15e15a12eb233100871aac6aa206fe59"
```

```
{
  "result": [
    {
      "indicator": {
      "gap_formatted":"",
      "benchmarking":false,
      "frequency_label":"Daily",
      "changeperc_formatted":"0.0%",
      "direction_label":"Minimize",
      "precision":0,
      "breakdown": {
        "display_value":"Assignment Group",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value":"baec0752bf130100b96dac808c0739ed"
      },
      "personal_target":null,
      "description":"Number of incidents open based on resolved date is empty",
      "value_color":"#455464",
      "uuid":"fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:0a52d3dcd7011200f2d224837e6103f2",
      "frequency":10,
      "gap":null,
      "value_unit":"0",
      "indicator_frequency":10,
      "value":0.0,
      "indicator_aggregate":1,
      "facts_table": {
        "name":"incident",
        "label":"Incidents"
      },
      "key":false,
      "indicator_frequency_label":"Daily",
      "direction":2,
      "element": {
        "display_value":"Application Development",
        "link":"https://<instance>.service-now.com/api/now/v1/table/sys_user_group/0a52d3dcd7011200f2d224837e6103f2",
        "value":"0a52d3dcd7011200f2d224837e6103f2"
      },
      "period_title":"Dec 03",
      "period":"Dec 03",
      "target_formatted":"",
      "change":0.0,
      "gapperc_formatted":"",
      "query":"opened_atONToday@javascript:gs.beginningOfToday()@javascript:gs.endOfToday()^ORopened_at<javascript:gs.beginningOfToday()^resolved_atISEMPTY^ORresolved_at>javascript:gs.endOfToday()^state!=8^assignment_group=0a52d3dcd7011200f2d224837e6103f2^EQ",
      "realtime_enabled":true,
      "changeperc":0.0,
      "target":null,
      "unit": {
        "display_value":"#",
        "link":"https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "type":"formatted",
        "value":"17b365e2d7320100ba986f14ce6103ad"
      },
      "value_formatted":"0",
      "name":"Number of open incidents > Assignment Group = Application Development",
      "gapperc":null,
      "change_formatted":"0",
      "favorite":false,
      "personal_target_formatted":""
    }
    // Followed by an indicator object with an element object for every element in the Sibling Group
  ]
}
```

### Return a filtered set of elements for a breakdown

To apply an elements filter to the Analytics Hub data, use the **sysparm\_elements\_filter** parameter with the sys\_id of a Performance Analytics element filter record.

```
# In this example, the element filter applies
# to the Groups breakdown source, with the
# condition [[Parent][is][Database]].
# The sys_id of this element filter is
# `7b9eb563eb11020065deac6aa206fe11`.
# The example gets the elements of the Assignment
# Group breakdown that have the element Database
# as a parent.

curl -v -u "user:password" -H "Accept:application/json" \
"https://<instance>.service-now.com/api/now/v1/pa/scorecards?sysparm_uuid=fb007202d7130100b96d45a3ce6103b4&sysparm_breakdown=baec0752bf130100b96dac808c0739ed&sysparm_elements_filter=7b9eb563eb11020065deac6aa206fe11"
```

```
{
  "result": [
    {
      "value_formatted": "37",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      "gapperc": null,
      "change": 9.0,
      "value_color": "#455464",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "32.1%",
      "direction_label": "Minimize",
      "period_title": "Jul 22",
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Assignment Group / Database",
      "value": 37.0,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "Database",
        "link": "https://<instance>.service-now.com/api/now/v1/table/sys_user_group/287ee6fea9fe198100ada7950d0b1b73",
        "value": "287ee6fea9fe198100ada7950d0b1b73"
      },
      "precision": 0,
      "breakdown": {
        "display_value": "Assignment Group",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value": "baec0752bf130100b96dac808c0739ed"
      },
      "period": "Jul 22",
      "favorite": false,
      "change_formatted": "9",
      "unit": {
        "display_value": "#",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "target": null,
      "changeperc": 0.32142857142857145,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:287ee6fea9fe198100ada7950d0b1b73",
      "gapperc_formatted": "",
      "value_unit": "37",
      "gap": null
    },
    {
      "value_formatted": "20",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      // Database Atlanta
      "gapperc": null,
      "change": 4.0,
      "value_color": "#455464",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "25.0%",
      "direction_label": "Minimize",
      "period_title": "Jul 22",
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Assignment Group / Database Atlanta",
      "value": 20.0,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "Database Atlanta",
        "link": "https://<instance>.service-now.com/api/now/v1/table/sys_user_group/db53580b0a0a0a6501aa37c294a2ba6b",
        "value": "db53580b0a0a0a6501aa37c294a2ba6b"
      },
      "precision": 0,
      "breakdown": {
        "display_value": "Assignment Group",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value": "baec0752bf130100b96dac808c0739ed"
      },
      "period": "Jul 22",
      "favorite": false,
      "change_formatted": "4",
      "unit": {
        "display_value": "#",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "target": null,
      "changeperc": 0.25,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:db53580b0a0a0a6501aa37c294a2ba6b",
      "gapperc_formatted": "",
      "value_unit": "20",
      "gap": null
    },
    {
      "value_formatted": "19",
      "indicator": {
        "display_value": "Number of open incidents",
        "link": "https://<instance>.service-now.com/api/now/v1/table/pa_indicators/fb007202d7130100b96d45a3ce6103b4",
        "value": "fb007202d7130100b96d45a3ce6103b4"
      },
      ...
      
      // Database San Diego
      "gapperc": null,
      "change": 0.0,
      "value_color": "#455464",
      "direction": 2,
      "target_formatted": "",
      "frequency": 10,
      "changeperc_formatted": "0.0%",
      "direction_label": "Minimize",
      "period_title": "Jul 22",
      "description": "Number of incidents open based on resolved date is empty.",
      "name": "Number of open incidents / Assignment Group / Database San Diego",
      "value": 10.0,
      "key": false,
      "gap_formatted": "",
      "element": {
        "display_value": "Database San Diego",
        "link": "https://<instance>.service-now.com/api/now/v1/table/sys_user_group/db53a9290a0a0a650091abebccf833c6",
        "value": "db53a9290a0a0a650091abebccf833c6"
      },
      "precision": 0,
      "breakdown": {
        "display_value": "Assignment Group",
        "link": "http://localhost:8080/api/now/v1/table/pa_breakdowns/baec0752bf130100b96dac808c0739ed",
        "value": "baec0752bf130100b96dac808c0739ed"
      },
      "period": "Jul 22",
      "favorite": false,
      "change_formatted": "0",
      "unit": {
        "display_value": "#",
        "link": "http://<instance>.service-now.com/api/now/v1/table/pa_units/17b365e2d7320100ba986f14ce6103ad",
        "value": "17b365e2d7320100ba986f14ce6103ad"
      },
      "frequency_label": "Daily",
      "target": null,
      "changeperc": 0.0,
      "uuid": "fb007202d7130100b96d45a3ce6103b4:baec0752bf130100b96dac808c0739ed:db53a9290a0a0a650091abebccf833c6",
      "gapperc_formatted": "",
      "value_unit": "10",
      "gap": null
    }
  ]
}
```

