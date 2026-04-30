---
title: Aggregate API
description: The Aggregate API provides endpoints that allow you to compute aggregate statistics about existing table and column data.Retrieves records for the specified table and performs aggregate functions on the returned values.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Aggregate API

The Aggregate API provides endpoints that allow you to compute aggregate statistics about existing table and column data.

For Aggregate API requests, you must have read access for all records in the table you query. If an ACL prevents the requesting user from accessing any record in the table, the request returns a 403 Forbidden error.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Aggregate - GET /now/stats/\{tableName\}

Retrieves records for the specified table and performs aggregate functions on the returned values.

You can specify which aggregate functions to perform by using either the **sysparm\_&lt;aggregate&gt;\_fields** parameter or **sysparm\_having=&lt;aggregate&gt;^field^operator^value** parameter, substituting **&lt;aggregate&gt;** for one of these aggregate functions:

-   avg
-   max
-   min
-   sum

### URL format

Versioned URL: `/api/now/{api_version}/stats/{tableName}`

Default URL: `/api/now/stats/{tableName}`

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

</td></tr><tr><td>

tableName

</td><td>

Name of the table for which to retrieve records.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

An alternative to using the **sysparm\_query** parameter. You can filter a query using key-value pairs where the key is the name of a field.For example, instead of using the parameter `&sysparm_query=active=true`, you can use `&active=true`. You can use the display value when the field is a choice or reference type field, such as `&state=closed` instead of `&state=7`. To specify multiple key-value pairs, separate each with an ampersand, such as `&active=true&assigned_to=john.smith`.

Data type: String

</td></tr><tr><td>

sysparm\_&lt;aggregate&gt;\_fields

</td><td>

List of fields on which to perform each aggregate operation. You can specify multiple fields by separating each with a comma. For example, to get the average values from the duration and priority fields, use `sysparm_avg_fields=duration,priority`.**Note:** Specify this parameter, the **sysparm\_count** parameter, or both for your query to return meaningful results. If neither parameter is passed, no aggregate operation is performed.

Data type: String

</td></tr><tr><td>

sysparm\_count

</td><td>

Flag that determines whether to return the number of records returned by the query.**Note:** Specify this parameter, the **sysparm\_&lt;aggregate&gt;\_fields** parameter, or both for your query to return meaningful results. If neither parameter is passed, no aggregate operation is performed.

Data type: String

</td></tr><tr><td>

sysparm\_display\_value

</td><td>

Data retrieval operation when grouping by reference or choice fields. Based on this value, the query returns either the display value, the actual value in the database, or both.-   true: Returns display values for all fields.
-   false: Returns actual values from the database. If a value is not specified, this parameter defaults to false.
-   all: Returns both actual and display values.

There is no preferred method for setting this parameter. However, specifying the display value may cause performance issues as they are not read from the database and may reference other fields and records. For more information on display values and actual values, see [Table API FAQs \(KB0534905\)](https://support.servicenow.com/kb_view.do?sysparm_article=KB0534905).Data type: String

</td></tr><tr><td>

sysparm\_group\_by

</td><td>

Fields by which to group the returned data. You can specify multiple fields by separating each field with a comma, such as `sysparm_group_by=priority,state`.Data type: String

</td></tr><tr><td>

sysparm\_having

</td><td>

Additional query that enables you to filter the data based on an aggregate operation. The value for this parameter must follow the syntax `aggregate^field^operator^value`, such as `count^priority^>^3` to obtain the number of records within the query results with a priority greater than 3. You can specify multiple queries by separating each with a comma, such `ascount^state^=^1,avg^priority^>^3`.Data type: String

</td></tr><tr><td>

sysparm\_order\_by

</td><td>

List of values by which to order grouped results. You can specify an order using a field or an aggregate. For example, if you specify `sysparm_order_by=AVG^state`, groups of results with lower average state values are returned first. You can also order by COUNT to arrange groups of records by the number of records in each group.When you specify an order, groups are ordered in ascending order by default. Use `^DESC` to sort in descending order, such as `sysparm_order_by=state^DESC`.

Data type: String

</td></tr><tr><td>

sysparm\_query

</td><td>

An encoded query.For example: `(sysparm_query=active=true)(sysparm_query=caller_id=javascript:gs.getUserID()^active=true)`

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
|Depends on specified table and specified request parameters.||

### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/stats/incident?sysparm_avg_fields=reassignment_count%2Cbusiness_stc&sysparm_group_by=assignment_group" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": [
    {
      "stats": {
        "avg": {
          "business_stc": "804162.7143",
          "reassignment_count": "1.0000"
        }
      },
      "groupby_fields": [
        {
          "value": "",
          "field": "assignment_group"
        }
      ]
    },
    {
      "stats": {
        "avg": {
          "business_stc": "2037371.0000",
          "reassignment_count": "1.5000"
        }
      },
      "groupby_fields": [
        {
          "value": "287ee6fea9fe198100ada7950d0b1b73",
          "field": "assignment_group"
        }
      ]
    },
    {
      "stats": {
        "avg": {
          "business_stc": "1821488.2857",
          "reassignment_count": "1.1111"
        }
      },
      "groupby_fields": [
        {
          "value": "8a5055c9c61122780043563ef53438e3",
          "field": "assignment_group"
        }
      ]
    },
    {
      "stats": {
        "avg": {
          "business_stc": "1730322.0000",
          "reassignment_count": "1.2500"
        }
      },
      "groupby_fields": [
        {
          "value": "287ebd7da9fe198100f92cc8d1d2154e",
          "field": "assignment_group"
        }
      ]
    },
    {
      "stats": {
        "avg": {
          "business_stc": "1564478.6250",
          "reassignment_count": "1.2500"
        }
      },
      "groupby_fields": [
        {
          "value": "d625dccec0a8016700a222a0f7900d06",
          "field": "assignment_group"
        }
      ]
    },
    {
      "stats": {
        "avg": {
          "business_stc": "1512202.2500",
          "reassignment_count": "1.1111"
        }
      },
      "groupby_fields": [
        {
          "value": "8a4dde73c6112278017a6a4baf547aa7",
          "field": "assignment_group"
        }
      ]
    }
  ]
}
```

