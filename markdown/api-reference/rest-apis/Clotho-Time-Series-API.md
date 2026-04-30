---
title: MetricBase Time Series API
description: The MetricBase Time Series API provides endpoints to insert data into, retrieve information from, and to run transforms against a MetricBase database.Retrieves specified time series data from the MetricBase database.Transforms the specified data based on the specified parameters.Accumulates metric values at specified timestamp and saves the result to the database rather than overwriting the value.Retrieves and optionally groups time series data for one or more metrics after applying a specified list of transforms that form a linear pipeline.Returns a stream of transformed time series data for one or more metrics after applying the specified list of transforms.Adds time series data to the MetricBase database.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 56
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# MetricBase Time Series API

The MetricBase Time Series API provides endpoints to insert data into, retrieve information from, and to run transforms against a MetricBase database.

This API can only be used when the MetricBase plugin \(com.snc.clotho\) is installed and activated.

Role required to write to this API: clotho\_rest\_put.

The examples in this section were created using data in the MetricBase \(com.snc.clotho\) plugin.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## MetricBase Time Series - GET /now/clotho/table/\{table\}/\{subject\}/\{metric\}

Retrieves specified time series data from the MetricBase database.

### URL format

Versioned URL: `/api/now/{api_version}/clotho/table/{table}/{subject}/{metric}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

 

</td></tr><tr><td>

metric

</td><td id="entry-metric-metricbase">

Name of the column in the table identified in the **subject** parameter to use as the metric.Data type: String

</td></tr><tr><td>

subject

</td><td>

Sys\_id of the GlideRecord associated with this series.Data type: String

</td></tr><tr><td>

table

</td><td id="entry-table-metricbase">

Name of the table containing the GlideRecord associated with this series.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_display\_value

</td><td id="entry-sysparm_display_value-metricbase">

Flag that indicates whether to label the result data with the subject record display value if no other label is specified.Valid values:

-   true: Result data is labeled with the subject record display value.
-   false: Result data is not labeled with the subject record display value.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_end

</td><td id="entry-sysparm_end-metricbase">

Required. End time of the evaluation period. An empty or missing value is treated as the current time. Time values are inclusive of this end time.Data type: String

Format: ISO 8601 \(UTC\), either:

-   Absolute date format \[YYYY-MM-DDThh:mm:ss\], such as `2019-03-20T17:04:55`.
-   Relative to current time duration format`[P(n)Y(n)M(n)DT(n)H(n)M(n)S]`, such as `P1M`.

</td></tr><tr><td>

sysparm\_start

</td><td id="entry-sysparm_start-metricbase">

Required. Start time of the evaluation period. The special value `all` can be used to set the start time as the current time minus the maximum retention period for the specified metrics. An empty or missing value is treated as an implicit `all`. Time values are inclusive of this start time.Data type: String

Format: ISO 8601 \(UTC\), either:

-   Absolute date format \[YYYY-MM-DDThh:mm:ss\], such as `2019-03-20T17:04:55`
-   Relative to current time duration format`[P(n)Y(n)M(n)DT(n)H(n)M(n)S]`, such as `P1M`.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
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

<table id="table_avx_j1g_rlb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

Label used to identify this metric’s result set. Data type: String

</td></tr><tr><td>

seriesRef

</td><td>

Data series results. Data type: Array of Objects

```
"seriesRef": [
  {
    "metric": "String",
    "subject": "String",
    "table": "String"
  }
]
```

</td></tr><tr><td>

seriesRef.metric

</td><td>

Name of the metric from which the data series was obtained. Only appears if the **metrics** object is passed in the request.Data type: String

</td></tr><tr><td>

seriesRef.subject

</td><td>

Sys\_id of the data series record. Located in the table specified in **seriesRef.table**.Data type: String

</td></tr><tr><td>

seriesRef.table

</td><td>

Name of the table from where the data series was obtained.Data type: String

</td></tr><tr><td>

values

</td><td>

Transformed series values.Data type: Array of Objects

```
"values": [
  {
    "timestamp": "String",
    "value": Number
  }
]
```

</td></tr><tr><td>

values.timestamp

</td><td>

Timestamp of the value.Data type: String

Format: ISO 8601

</td></tr><tr><td>

values.value

</td><td>

Metric values.Data type: Number

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/v1/clotho/
  table/mb_demo_drone/626b051787333200a328c5b836cb0b99/
  mb_demo_mt_altitude?sysparm_start=2019-03-20T17%3A04%3A55
  &sysparm_end=2019-03-20T17%3A09%3A55" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "seriesRef": {
    "subject": "626b051787333200a328c5b836cb0b99",
    "table": "mb_demo_drone",
    "metric": "mb_demo_mt_altitude"
  },
  "label": "626b051787333200a328c5b836cb0b99:
            mb_demo_drone|mb_demo_mt_altitude",
  "values": [
    {
      "timestamp": "2019-03-20T17:05:00Z",
      "value": 83.150185
    },
    {
      "timestamp": "2019-03-20T17:06:00Z",
      "value": 83.46074
    },
    {
      "timestamp": "2019-03-20T17:07:00Z",
      "value": 83.83104
    },
    {
      "timestamp": "2019-03-20T17:08:00Z",
      "value": 84.260635
    },
    {
      "timestamp": "2019-03-20T17:09:00Z",
      "value": 84.749
    }
  ]
}

```

## MetricBase Time Series - GET /now/clotho/transform/\{table\}/\{metric\}

Transforms the specified data based on the specified parameters.

### URL format

Versioned URL: `/api/now/{api_version}/clotho/transform/{table}/{metric}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

 

</td></tr><tr><td>

metric

</td><td id="entry-metric-metricbase">

Name of the column in the table identified in the **subject** parameter to use as the metric.Data type: String

</td></tr><tr><td>

table

</td><td id="entry-table-metricbase">

Name of the table containing the GlideRecord associated with this series.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_display\_value

</td><td id="entry-sysparm_display_value-metricbase">

Flag that indicates whether to label the result data with the subject record display value if no other label is specified.Valid values:

-   true: Result data is labeled with the subject record display value.
-   false: Result data is not labeled with the subject record display value.

Data type: Boolean

Default: false

</td></tr><tr><td>

sysparm\_end

</td><td id="entry-sysparm_end-metricbase">

Required. End time of the evaluation period. An empty or missing value is treated as the current time. Time values are inclusive of this end time.Data type: String

Format: ISO 8601 \(UTC\), either:

-   Absolute date format \[YYYY-MM-DDThh:mm:ss\], such as `2019-03-20T17:04:55`.
-   Relative to current time duration format`[P(n)Y(n)M(n)DT(n)H(n)M(n)S]`, such as `P1M`.

</td></tr><tr><td>

sysparm\_query

</td><td>

Encoded query string for finding the subject records.Data type: String

 Default: None

</td></tr><tr><td>

sysparm\_start

</td><td id="entry-sysparm_start-metricbase">

Required. Start time of the evaluation period. The special value `all` can be used to set the start time as the current time minus the maximum retention period for the specified metrics. An empty or missing value is treated as an implicit `all`. Time values are inclusive of this start time.Data type: String

Format: ISO 8601 \(UTC\), either:

-   Absolute date format \[YYYY-MM-DDThh:mm:ss\], such as `2019-03-20T17:04:55`
-   Relative to current time duration format`[P(n)Y(n)M(n)DT(n)H(n)M(n)S]`, such as `P1M`.

</td></tr><tr><td>

sysparm\_subject\_limit

</td><td>

Limit size of the subject query result. Data type: Number

 Default: 10,000

</td></tr><tr><td>

sysparm\_transforms

</td><td>

Comma separated list of transforms. Valid transforms:

-   add
-   avg
-   label
-   mul
-   resample
-   sum
-   top

 Data type: String

 Default: None

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

<table id="table_ak1_l1g_rlb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

Label used to identify this metric’s result set. Data type: String

</td></tr><tr><td>

seriesRef

</td><td>

Data series results. Data type: Array of Objects

```
"seriesRef": [
  {
    "metric": "String",
    "subject": "String",
    "table": "String"
  }
]
```

</td></tr><tr><td>

seriesRef.metric

</td><td>

Name of the metric from which the data series was obtained. Only appears if the **metrics** object is passed in the request.Data type: String

</td></tr><tr><td>

seriesRef.subject

</td><td>

Sys\_id of the data series record. Located in the table specified in **seriesRef.table**.Data type: String

</td></tr><tr><td>

seriesRef.table

</td><td>

Name of the table from where the data series was obtained.Data type: String

</td></tr><tr><td>

values

</td><td>

Transformed series values.Data type: Array of Objects

```
"values": [
  {
    "timestamp": "String",
    "value": Number
  }
]
```

</td></tr><tr><td>

values.timestamp

</td><td>

Timestamp of the value.Data type: String

Format: ISO 8601

</td></tr><tr><td>

values.value

</td><td>

Metric values.Data type: Number

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/v1/clotho/
  transform/mb_demo_drone/mb_demo_mt_speed?
  sysparm_query=model%3DKingfisher%20Phantom&
  sysparm_start=2019-03-25T17%3A04%3A55&
  sysparm_end=2019-03-25T17%3A05%3A10" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Output:

```
[
  {
    "seriesRef": {
      "subject": "2a6b051787333200a328c5b836cb0b92",
      "table": "mb_demo_drone",
      "metric": "mb_demo_mt_speed"
    },
    "label": "2a6b051787333200a328c5b836cb0b92:mb_demo_drone
             |mb_demo_mt_speed",
    "values": [
      {
        "timestamp": "2019-03-25T17:05:00Z",
        "value": 33.67892
      }
    ]
  },
  {
    "seriesRef": {
      "subject": "666b051787333200a328c5b836cb0b92",
      "table": "mb_demo_drone",
      "metric": "mb_demo_mt_speed"
    },
    "label": "666b051787333200a328c5b836cb0b92:mb_demo_drone
             |mb_demo_mt_speed",
    "values": [
      {
        "timestamp": "2019-03-25T17:05:00Z",
        "value": 41.94985
      }
    ]
  },
  {
    "seriesRef": {
      "subject": "a26b051787333200a328c5b836cb0b92",
      "table": "mb_demo_drone",
      "metric": "mb_demo_mt_speed"
    },
    "label": "a26b051787333200a328c5b836cb0b92:mb_demo_drone
             |mb_demo_mt_speed",
    "values": [
      {
        "timestamp": "2019-03-25T17:05:00Z",
        "value": 37.74187
      }
    ]
  },
  {
    "seriesRef": {
      "subject": "ea6b051787333200a328c5b836cb0b92",
      "table": "mb_demo_drone",
      "metric": "mb_demo_mt_speed"
    },
    "label": "ea6b051787333200a328c5b836cb0b92:mb_demo_drone
             |mb_demo_mt_speed",
    "values": [
      {
        "timestamp": "2019-03-25T17:05:00Z",
        "value": 34.914192
      }
    ]
  },
  {
    "seriesRef": {
      "subject": "ee6b051787333200a328c5b836cb0b91",
      "table": "mb_demo_drone",
      "metric": "mb_demo_mt_speed"
    },
    "label": "ee6b051787333200a328c5b836cb0b91:mb_demo_drone
             |mb_demo_mt_speed",
    "values": [
      {
        "timestamp": "2019-03-25T17:05:00Z",
        "value": 44.170887
      }
    ]
  }
]

```

## MetricBase Time Series - POST /now/clotho/accumulate

Accumulates metric values at specified timestamp and saves the result to the database rather than overwriting the value.

Use this API to handle metrics that can be summed for an accumulation, such as kilowatt-hours \(kWhs\) of electricity. Accumulate makes a call for each metric at the provided timestamp. For example, collected kilowatts for a heater, electric kettle, and washing machine would result in three calls to accumulate.

### URL format

Versioned URL: `/api/now/{api_version}/clotho/accumulate`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

default\_value

</td><td>

Default value for accumulation at a given timestamp. Used only during the first call to accumulate if a value is unavailable for a given timestamp. A use case could be accumulating a watts metric for a total\_power. You want to accumulate watts for a router connected to an outlet without a power meter to measure it. If you know the consumption value and it is constant\), you can use the constant value as a default value to accumulate total\_power. For example, you would use 20 if the router is constantly plugged in and consumes 20 Watts.

Data type: String

Default: 0

</td></tr><tr><td>

sysparm\_ignore\_unknown\_series

</td><td>

Flag that indicates whether to ignore an unknown series and continue the transaction without returning an error.Valid values:

-   true: Ignore unknown series.
-   false: Don't ignore unknown series.

Default: true

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

seriesRef

</td><td>

List of strings representing data series information to update.Data type: Array

```
"seriesRef": [
  {
    "metric": "String",
    "subject": "String",
    "table": "String"
  }
]
```

</td></tr><tr><td>

seriesRef.metric

</td><td>

Required. Name of the accumulating metric to update.Data type: String

</td></tr><tr><td>

seriesRef.subject

</td><td>

Required. Sys\_id of the record in which to update the data.Data type: String

Table: Specified in **seriesRef.table**

</td></tr><tr><td>

seriesRef.table

</td><td>

Required. Name of the table in which to save the data.Data type: String

</td></tr><tr><td>

values

</td><td>

Required. Series values to accumulate and store. Values with the same timestamp are summed up with the **default\_value** query parameter.Data type: Array

```
"values": [
  {
    "timestamp": "String",
    "value": Number
  }
]
```

</td></tr><tr><td>

values.timestamp

</td><td>

Required. ISO 8601 timestamp of the value.Data type: String

Format: YYYY-MM-ddTHH:mm:ddZ

The character represented by 'Z' denotes the UTC time zone in an ISO-formatted timestamp. This portion of the timestamp format is optional.

Example: `2019-03-21T17:05:00Z`

</td></tr><tr><td>

values.value

</td><td>

Required. Metric value.Data type: Number

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
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
|message|Message indicating success \(OK\) or error.|

### cURL request

This example shows how to accumulate metric values at a given timestamp.

```
curl "https://instance.servicenow.com/api/now/v1/clotho/accumulate" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"seriesRef\": {
    \"subject\": \"3D666b051787333200a328c5b836cb0b92\",
    \"table\": \"power_monitoring\",
    \"metric\": \"total_power\"
  },
  \"values\": [
    {
      \"timestamp\": \"2019-03-21T17:05:00Z\",
      \"value\": 0.150185
    },
    {
      \"timestamp\": \"2019-03-21T17:05:00Z \",
      \"value\": 0.46074
    },
    {
      \"timestamp\": \"2019-03-21T17:05:00Z \",
      \"value\": 0.83104
    },
    {
      \"timestamp\": \"2019-03-21T17:05:00Z \",
      \"value\": 1.260635
    },
    {
      \"timestamp\": \"2019-03-21T17:05:00Z \",
      \"value\": 1.749
    }
  ]
}" \
--user "username":"password"
```

Output provided with successful results.

```
{
    "result": {
        "message": "ok"
    }
}
```

## MetricBase Time Series - POST /now/clotho/transform

Retrieves and optionally groups time series data for one or more metrics after applying a specified list of transforms that form a linear pipeline.

### URL format

Versioned URL: `/api/now/{api_version}/clotho/transform`

### Supported request parameters

<table id="table_md4_gb5_ssb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_display\_value

</td><td id="entry-sysparm_display_value-metricbase">

Flag that indicates whether to label the result data with the subject record display value if no other label is specified.Valid values:

-   true: Result data is labeled with the subject record display value.
-   false: Result data is not labeled with the subject record display value.

Data type: Boolean

Default: false

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

end

</td><td>

Required. End time of the evaluation period. An empty or missing value is treated as the current time. Time values are inclusive of this end time.Data type: String

Format: ISO 8601 \(UTC\), either:

-   Absolute date format \[YYYY-MM-DDThh:mm:ss\], such as `2019-03-20T17:04:55`.
-   Relative to current time duration format`[P(n)Y(n)M(n)DT(n)H(n)M(n)S]`, such as `P1M`.

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. Unusually large values can impact system performance.Data type: Number

Default: 10,000

</td></tr><tr><td>

metrics

</td><td>

List of metrics objects to use in the transform. For more information on metrics, see [Metrics](https://www.servicenow.com/docs/access?context=c_MetricDefinitionSupport&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).Data type: Array

 ```
"metrics": [
  {
    "groupBy": "String"
    "label": "String",
    "metric": "String",
    "transforms": [Array]
  }
]
```

</td></tr><tr><td>

metrics.groupBy

</td><td>

Comma-separated list of fields, contained in the table specified in the **table** parameter, to group the series by before collecting or applying aggregated transformations.The order of the items in the list is the order in which the data is grouped by. For example, if there are two items in the list, "state, zip code", then the series is first grouped by state and then by zip code within the state.

 Data type: String

 Default: Data is not grouped.

</td></tr><tr><td>

metrics.label

</td><td>

Label to use for this metric’s result set. It replaces any labels generated by the transform chain.Data type: String

Default: Generated default label.

</td></tr><tr><td>

metrics.metric

</td><td>

Required if **metrics** object is passed. Metric field to use in the transform. This field must be in the table specified in the **table** parameter. Data type: String

</td></tr><tr><td>

metrics.transforms

</td><td>

List of transforms \(transform chain\) to apply to the retrieved time series data. Each transform builds on the results of the previous transform. For a list of available transforms, see [Supported Transforms](Clotho-Time-Series-API.md#Supported_transforms) below.Data type: Array of Objects

```
"transforms": [
  {
    "arg": {Object},
    "name": "String"
  }
]
```

</td></tr><tr><td>

metrics.transforms.arg

</td><td>

Dependent on the transform. Parameter or parameters to pass into the transform.General guidelines:

-   Don't use the **arg** parameter when specifying transformations that do not take a parameter.
-   Use Number, String, or Boolean for transforms that take a single parameter.
-   Use a JSON object, with the appropriate name-value pairs, for transforms that take more than one parameter.

Data type: Number, String, Boolean, or JSON object, depending on transform. \(For a list of available transforms, refer to the table [Supported transforms](Clotho-Time-Series-API.md#Supported_transforms) below.\)

</td></tr><tr><td>

metrics.transforms.name

</td><td>

Required if a **transforms** object is specified. Name of the transform.For a list of available transforms, refer to the table [Supported transforms](Clotho-Time-Series-API.md#Supported_transforms) below.

 Data type: String

</td></tr><tr><td>

query

</td><td>

Encoded query to use to filter the result set. You can compose the query using the specified table’s filter editor. Once created, select **Copy URL** from the filter’s breadcrumbs context menu.

Data type: String

Default: None

</td></tr><tr><td>

start

</td><td>

Required. Start time of the evaluation period. The special value `all` can be used to set the start time as the current time minus the maximum retention period for the specified metrics. An empty or missing value is treated as an implicit `all`. Time values are inclusive of this start time.Data type: String

Format: ISO 8601 \(UTC\), either:

-   Absolute date format \[YYYY-MM-DDThh:mm:ss\], such as `2019-03-20T17:04:55`
-   Relative to current time duration format`[P(n)Y(n)M(n)DT(n)H(n)M(n)S]`, such as `P1M`.

</td></tr><tr><td>

table

</td><td>

Required. Name of the table that contains the GlideRecord associated with this series.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

results

</td><td>

Zero or more return result objects that satisfy the query. Contains either a **series** array or a **grouped** array.Data type: Array

 ```
"results":[
  {
    "grouped": [Array],
    "marker": "String",
    "series": [Array]
  }
]
```

</td></tr><tr><td>

results.grouped

</td><td>

List of grouped result objects where each **grouped** result object corresponds to a specific group. This format is returned when the **metrics.groupBy** parameter is passed in the request body.Data type: Array

 ```
"grouped": [
  {
    "groupingBy": "String",
    "groups": [Array]
  }
]
```

</td></tr><tr><td>

results.grouped.groupingBy

</td><td>

Value passed in the **metrics.groupBy** parameter in the request.Data type: String

</td></tr><tr><td>

results.grouped.groups

</td><td>

List of generated groups based on the content of the **metrics.groupBy** parameter in the request.Data type: Array

 ```
"groups": [
  {
    "group": "String",
    "label": "String",
    "series": {Object}
  }
]
```

</td></tr><tr><td>

results.grouped.groups.group

</td><td>

Name of the group.Data type: String

</td></tr><tr><td>

results.grouped.groups.label

</td><td>

Label of the group.Data type: String

</td></tr><tr><td>

results.grouped.groups.series

</td><td>

Transformed values for the group's result.Data type: Array

 ```
"series": [
  {
    "label": "String",
    "seriesRef": {Object},
    "values": [Array]
  }
]
```

</td></tr><tr><td>

results.grouped.groups.series.label

</td><td>

Label of the series.Data type: String

</td></tr><tr><td>

results.grouped.groups.series.seriesRef

</td><td>

Results of a single data series. Does not appear if there are multiple data series in the response.Data type: Object

 ```
"seriesRef": {
  "metric": "String",
  "subject": "String",
  "table": "String"
}
```

</td></tr><tr><td>

results.grouped.groups.series.seriesRef.metric

</td><td>

Name of the metric from which the data series was obtained. Only appears if the **metrics** object is passed in the request.Data type: String

</td></tr><tr><td>

results.grouped.groups.series.seriesRef.subject

</td><td>

Sys\_id of the data series record..Data type: String

Table: Table specified the in **results.series.seriesRef.table** parameter.

</td></tr><tr><td>

results.grouped.groups.series.seriesRef.table

</td><td>

Name of the table from where the data series was obtained.Data type: String

</td></tr><tr><td>

results.grouped.groups.series.values

</td><td>

List of result values for the group.Data type: Array

```
"values": [
  {
    "timestamp": "String",
    "value": Number
  }
]
```

</td></tr><tr><td>

results.grouped.groups.series.values.timestamp

</td><td>

ISO 8601 timestamp of the value.Data type: String

</td></tr><tr><td>

results.grouped.groups.series.values.value

</td><td>

Transformed value.Data type: Number

</td></tr><tr><td>

results.marker

</td><td>

Unique identifier for the corresponding results.Data type: String

</td></tr><tr><td>

results.series

</td><td>

List of ungrouped series of result objects.Data type: Array of Objects

```
"series": [
  {
    "label": "String",
    "seriesRef": {Object},
    "values": [Array]
  }
]
```

</td></tr><tr><td>

results.series.label

</td><td>

Data series label. This value is either generated by the endpoint or is the value passed in the **metrics.label** parameter.Data type: String

</td></tr><tr><td>

results.series.seriesRef

</td><td>

Results of a single data series. Does not appear if there are multiple data series in the response.Data type: Object

```
"seriesRef": {
  "metric": "String",
  "subject": "String",
  "table": "String"
}
```

</td></tr><tr><td>

results.series.seriesRef.metric

</td><td>

Name of the metric from which the data series was obtained. Only appears if the **metrics** object is passed in the request.Data type: String

</td></tr><tr><td>

results.series.seriesRef.subject

</td><td>

Sys\_id of the data series record.Data type: String

Table: Secified in the **results.series.seriesRef.table** parameter.

</td></tr><tr><td>

results.series.seriesRef.table

</td><td>

Name of the table from where the data series was obtained.Data type: String

</td></tr><tr><td>

results.series.values

</td><td>

Transformed series values.Data type: Array of Objects

```
"values": [
  {
    "timestamp": "String",
    "value": Number
  }
]
```

</td></tr><tr><td>

results.series.values.timestamp

</td><td>

ISO 8601 timestamp of the value.Data type: String

</td></tr><tr><td>

results.series.values.value

</td><td>

Transformed value.Data type: Number

</td></tr></tbody>
</table>### Supported transforms

<table id="id_abm_vgl_2tb"><thead><tr><th>

Transform

</th><th>

Description

</th></tr></thead><tbody><tr id="version-row-RESTAPI"><td>

add

</td><td>

Adds the specified number to each timestamp value.Argument: arg \(Decimal data type\) – Number to add.

For example:

```
"transforms": [
  {
    "name": "add",
    "arg": 8
  }
]
```

</td></tr><tr><td>

autocorrelate

</td><td>

Calculates the correlation between timestamp values separated by an increasing number of periods starting at 1.

</td></tr><tr><td>

avg

</td><td>

Aggregates the time series into one series containing the average value for each corresponding timestamp across the input.

</td></tr><tr><td>

bottom

</td><td>

Returns the specified number of series that have the lowest values.Argument: `arg` \(Integer\) – The number of series to return.

For example, the following returns the two time series that contain the lowest sets of values.

```
"transforms": [
  {
     "name": "bottom",
     "arg": 2
  }
]
```

</td></tr><tr><td>

ceil

</td><td>

Rounds the value in each timestamp up to the specified precision: `ceil(value / <arg>) * <arg>)` Argument: arg \(Decimal data type\) – Decimal precision to round up to.

</td></tr><tr><td>

collect

</td><td>

Displays the transform results of the transform chain up to the point of the collect transform call. Collect transform results contain a unique marker, but you may want to also define a label.For example:

```
{
  "start": "PT1H",
  "end": "",
  "table": "mb_demo_drone",
  "limit": 5000,
  "metrics": [
    {
      "metric": "mb_demo_mt_altitude",
      "transforms": [
        {
          "name": "label",
          "arg": "Series Timestamp Values"
        },
        {
          "name": "collect"
        },
        {
          "name": "avg"
        },
        {
          "name": "label",
          "arg": "Average Timestamp Values"
        }
      ]
    }
  ]
}
```

</td></tr><tr><td>

constrainValues

</td><td>

Replaces any value outside the specified range with the corresponding maximum or minimum value.For example, if you specified the following, the transform replaces any value that is less than 0 with 0, and any value that is more than 100 with 100.

```
"transforms": [
  {
    "name": "constrainValues",
    "val1": 0,
    "val2": 100
  }
]
```

Arguments:

-   val1 \(Decimal data type\): Minimum or maximum value.
-   val2 \(Decimal data type\): Minimum or maximum value.

</td></tr><tr><td>

count

</td><td>

Aggregates the time series into one series. The new series contains the number of values that are not NaN \(Not a Number\) for each corresponding timestamp across the series.

</td></tr><tr><td>

derivative

</td><td>

Determines the rate of change between timestamps. Divides the difference between the value in each timestamp and the value in the next timestamp by the timestamp’s period.**Note:** This transform returns one less value than the number of values in the series.

</td></tr><tr><td>

div

</td><td>

Divides the value in each timestamp by the specified number \(arg\).Argument: arg \(Decimal – The number by which to divide the value of each timestamp.

</td></tr><tr><td>

envelope

</td><td>

Returns two time series, where, at any point in time, one contains the largest value and the other contains the smallest value.**Note:** NaNs are ignored, but are returned if there are no other return values.

</td></tr><tr><td>

exp

</td><td>

Raises the value of the specified base to the power of the value in each timestamp.Argument: arg \(Decimal data type\) – The base value.

</td></tr><tr><td>

filter

</td><td>

Applies an aggregator to the contents of a sliding window, such as producing a moving average.Arguments:

-   aggregator \(Aggregator data type\): Type of aggregation to perform.
-   window \(Duration data type\): The duration of the sliding window.

</td></tr><tr><td>

floor

</td><td>

Rounds the value in each timestamp down to the specified precision: `floor(value / <arg>) * <arg>` Argument: arg \(Decimal data type\) – The decimal precision to round down to.

</td></tr><tr><td>

fractiles

</td><td>

Returns a time series for each fraction in the specified array. Each timestamp value is the value at which the specified fraction of values, for the corresponding timestamp across the input series, is below the specified percentage. For example, if the fraction is 0.5, then the value in the timestamp is the value where half the values in the input series are below 0.5.Argument: arg \(Array of Decimal\) – The fractions to use on the input series.

For example:

```
"transforms": [
  {
    "name": "fractiles",
    "arg": [0.25, 0.5, 0.75, 1]
  }
]
```

</td></tr><tr><td>

groupBy

</td><td>

Groups data by the specified fields before collecting or applying aggregated transformations.Argument: arg \(String\) - A comma separated list of fields in the table to use to group the transform results.

For example:

```
 "transforms": [
  {
    "name": "groupBy",
    "arg": "model"
  },
  {
    "name": "avg"
  },
  {
    "name": "label",
    "arg": "Model: %g"
  }
]
```

</td></tr><tr><td>

integrate

</td><td>

Multiplies the value in each timestamp by its period.

</td></tr><tr><td>

interpolate

</td><td>

Creates a data value for a NaN data item by interpolating from adjacent data values.Argument: arg \(Integer\) – Number of data samples in each direction to check for a non-NaN value. If a non-NaN value is not found, then NaN is used.

</td></tr><tr><td>

inverse

</td><td>

Computes the inverse of each timestamp value.

</td></tr><tr><td>

iqr

</td><td>

Performs an interquartile range transform and creates a result set that contains four series: 1.  -IQR: The median of all entries below `Q1 - (1.5 * IQR)`.
2.  Q1: The median of the smallest half of entries.
3.  Q3: The median of the largest half of entries.
4.  +IQR: The median of all entries above `Q3 + (1.5 * IQR)`.

**Note:** `IQR = Q3 - Q1`

</td></tr><tr><td>

label

</td><td>

Labels a transformation chain.**Note:** Subsequent transformations may modify or replace the label.

Argument: arg \(String\) – Text of the label. Can contain the following formatting expressions:

-   %%: Escape a "%" literal.
-   %l: Current label that is being replaced.
-   %s: Series subject.
-   %g: Value of the group by field. If this is a referenced record, then the value of the record’s name field. If multiple groups are specified in the **groupBy** transform, labels are comma separated.
-   %G: Value of the group by field. If this is a referenced record, then the record’s sys\_id. If multiple groups are selected, values are comma separated.

For example:

```
"transforms": [
  {
    "name": "label",
    "arg": "Series Timestamp Values"
  },
]
```

```
"transforms": [
  {
    "name": "groupBy",
    "arg": "model"
  },
  {
    "name": "avg"
  },
  {
    "name": "label",
    "arg": "Model: %g"
  }
]
```

</td></tr><tr><td>

limit

</td><td>

Returns, at most, the specified duration or number of values, starting with the most recently saved value.Arguments:

-   arg \(Integer\): Number of timestamp values to return for each time series.

OR

-   arg \(Duration data type\): Duration to limit each time series to.

</td></tr><tr><td>

log

</td><td>

Runs a logarithm on the value in each timestamp where the result is the log of the specified base for the timestamp value.Argument: arg \(Decimal data type\) – Base for the logarithm calculation.

</td></tr><tr><td>

mapValues

</td><td>

Replaces any values within the specified range \(inclusive\) with the specified value. If both **lowerBound** and **upperBound** are specified as NaN, then it replaces any NaN value with the **targetValue**.Arguments:

-   lowerBound \(Decimal data type\): The lowest value in the range.
-   upperBound \(Decimal data type\): The highest value in the range.
-   targetValue \(Decimal data type\): Replacement value.

For example, the following changes all values in the time series that are between .1 and .9 to 1:

```
"transforms": [
  {
    "name": "mapValues",
    "lowerBound": .1,
    "upperBound": .9,
    "targetValue": 1
  }
]
```

</td></tr><tr><td>

max

</td><td>

Returns a series that contains the maximum value for each corresponding timestamp across the input.

</td></tr><tr><td>

median

</td><td>

Creates a series that contains the median of values for each timestamp across a set of series.If there are `n` series:

-   If `n` is odd, the median is the `(n / 2 + 1)` value for a timestamp.
-   If `n` is even, the median is the average of the `(n / 2)` and `(n / 2 + 1)` values for a timestamp.

</td></tr><tr><td>

min

</td><td>

Returns a series that contains the minimum value for each corresponding timestamp across the input.

</td></tr><tr><td>

mul

</td><td>

Multiplies the value in each timestamp by the specified number.Argument: arg \(Decimal data type\) – Number by which to multiply the value of each timestamp.

</td></tr><tr><td>

partition

</td><td>

Produces a new series with values filtered by applying a specified aggregator to a non-overlapping window.

 Arguments:

-   aggregator \(Aggregator data type\): Type of aggregation to perform.
-   base \(DateTime data type\): The zero offset to use for partitioning. For example, to partition by day \(24h\), set this value to Monday at midnight in your time zone. To partition by a 30-day period, set this value to the first day of the most recent month.

Default: Beginning of the EPOCH.

-   window \(Duration data type\): The duration of the non-overlapping window to apply the aggregator.

</td></tr><tr><td>

pow

</td><td>

Raises each timestamp value to the specified power.Argument: arg \(Decimal data type\) – Power to which to raise each value.

</td></tr><tr><td>

product

</td><td>

Aggregates the selected metric series into a single series that contains the product of all values for each timestamp. NaNs are excluded. If all numbers in the series are NaN, the output is also NaN.

</td></tr><tr><td>

resample

</td><td>

Resamples a time series to either a fixed number of points or from one frequency to another.Use the resample transformation to reduce the number of samples in the result set to more closely match the number of samples that you want to display.

Arguments: You can pass various arguments for this transform. Below is a list of each of the possible argument groups. Only one of these argument groups can be passed within a single transform. The following argument groups are delineated by AND/OR. AND meaning the argument is part of the current group; OR meaning it is the start of a new argument group.

-   arg \(Integer\): Number of samples to include in the result set. If available samples are less than this number, the endpoint uses interpolation to create additional samples. If there are more samples than this number, they are reduced by averaging them.

OR

-   arg \(Duration data type\): The frequency at which to resample. If available samples are less than this number, the endpoint uses interpolation to create additional samples. If there are more samples than this number, they are reduced by averaging them.

OR

-   minValues \(Integer\): The minimum number of samples to include in the result set. If available samples are less than this number, the endpoint uses interpolation to create additional samples.

AND

-   maxValues \(Integer\): The maximum number of samples to include in the result set. If there are more samples than this number, they are reduced by averaging them.

OR

-   aggregator \(Aggregator data type\): The aggregator to use when resampling.

AND

-   values \(Integer\): The number of samples to include in the result set. If available samples are less than this number, the endpoint uses interpolation to create additional samples. If there are more samples than this number, they are reduced by applying the specified **aggregator** to them.

OR

-   aggregator \(Aggregator data type\): The aggregator to use when resampling.

AND

-   period \(Duration data type\): The frequency at which to resample. If available samples are less than this number, the endpoint uses interpolation to create additional samples. If there are more samples than this number, they are reduced by applying the specified **aggregator** to them.

OR

-   aggregator \(Aggregator data type\): The aggregator to use when resampling.

AND

-   minValues \(Integer\): The minimum number of samples to include in the result set. If available samples are less than this number, the endpoint uses interpolation to create additional samples.

AND

-   maxValues \(Integer\): The maximum number of samples to include in the result set. If there are more samples than this number, they are reduced by averaging them.

</td></tr><tr><td>

round

</td><td>

Rounds the value in each timestamp up to the specified precision: `(value / <arg>) * <arg>` Argument: arg \(Decimal data type\) – The decimal precision to round up to.

</td></tr><tr><td>

root

</td><td>

Calculates the root of each timestamp value using the specified index.Argument: arg \(Decimal data type\) – The index of the root.

For example, the following returns the square root of each timestamp:

```
"transforms": [
  {
    "name": "root",
    "arg": "2"
  },
]
```

</td></tr><tr><td>

stddev

</td><td>

Creates a series that contains the standard deviation of values for each timestamp across a set of series.

</td></tr><tr><td>

sub

</td><td>

Subtracts the specified number from the value in each timestamp.Argument: arg \(Number\) – The number to subtract from the value in each timestamp.

</td></tr><tr><td>

sum

</td><td>

Aggregates the selected metric series into one series that contains the sum of all values for each timestamp, excluding any NaNs. If all numbers in the series are NaN, the output is NaN.

</td></tr><tr><td>

timeshift

</td><td>

Shifts the time range by adding the specified offset to a value’s timestamp without modifying the value. Use this transform to shift timestamps to another timezone.Argument: arg \(Duration data type\) – The amount of time to shift by.

</td></tr><tr><td>

top

</td><td>

Returns the specified number of series that have the highest values.Argument: arg \(Integer\) – The number of series to return.

For example, the following returns the two time series that contain the highest sets of values.

```
"transforms": [
  {
     "name": "top",
     "arg": 2
  }
]
```

</td></tr></tbody>
</table><table id="id_uq3_hhl_2tb"><thead><tr><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td id="Aggregator">

Aggregator

</td><td>

Available aggregators to use within the transform.-   AVG: Calculates the arithmetic mean of all currently selected series.
-   CHISQUARE: Shows how well a statistical model fits the metric dataset.
-   LAST: Returns the last defined value in the period window.
-   MAX: Shows the largest value for the metric dataset, at each point in time.
-   MEDIAN: Shows the median of the metric dataset. The median separates the higher values of the metric dataset from the lower values.
-   MIN: Shows the smallest value for the metric dataset, at each point in time.
-   STDDEV: Calculates the standard deviation across the underlying data. Used to quantify the variation or dispersion of a set of data values in the metric dataset.
-   SUM: Calculates the sum across all currently selected series.

</td></tr><tr><td id="DateTime">

DateTime

</td><td>

Absolute date/time values are specified by the ISO 8601 date and time format: `YYYY-MM-DDThh:mm:ss`. For example: 2020-02-28T13:10:42.Where:

-   \[YYYY\]: Four-digit year.
-   \[MM\]: Zero-padded month between 01 and 12.
-   \[DD\]: Zero-padded day between 01 and 31.
-   T: Represents time and is mandatory before any of the time components are specified.
-   \[hh\]: Zero-padded hour between 00 and 23.
-   \[mm\]: Zero-padded minutes between 00 and 59.
-   \[ss\]: Zero-padded seconds between 00 and 59. Note that leap seconds are spread out evenly across the previous 1,000 seconds.

Relative date/time values are specified using a duration \(Duration data type\), which is subtracted from the current time.

For example: P7D = seven days ago.

</td></tr><tr><td id="Decimal">

Decimal

</td><td>

Decimal value that can either be: -   A signed decimal number of arbitrary precision that can use exponential notation.

Such as:

    -   2
    -   1.7
    -   -3.47
    -   1.0E+2
-   A string representation of:
    -   A signed decimal number that may use exponential notation and is guaranteed to be a double-precision 64-bit IEEE 754 floating-point number.
    -   "NaN"
    -   "-Infinity"
    -   "+Infinity"

</td></tr><tr><td id="Duration">

Duration

</td><td>

Amount of time in a time interval. Duration values are specified by the ISO 8601 duration format: `P[n]Y[n]M[n]DT[n]H[n]M[n]S` Where:

-   P: Duration designator, referred to as "period", and is always placed at the beginning of the duration.
-   \[n\]Y: Number of years.
-   \[n\]M: Number of months.
-   \[n\]D: Number of days.
-   T: Time designator and is mandatory before any of the time components are specified.
-   \[n\]H: Number of hours.
-   \[n\]M: Number of minutes.
-   \[n\]S: Number of seconds.

For example:

-   P7D: Period of seven days.
-   P1M: Period of one month.
-   PT15M: Period of 15 minutes.
-   P1DT12H: Period of one day and twelve hours.

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/v1/clotho/transform \
--request POST \
--header "Accept:application/json", "Content-Type:application/json" \
--user "username":"password"
-d {\
  "start": "PT15M",\
  "end": "",\
  "table": "mb_demo_drone",\
  "query": "fleet.nameSTARTSWITHB",\
  "limit": 5000,\
  "metrics": [\
    {\
      "metric": "mb_demo_mt_altitude",\
      "label": "Series - Avg",\
      "transforms": [\
        {\
          "name": "partition",\
          "arg": {\
            "aggregator": "AVG",\
            "window": "PT5M"\
          }\
        },
        {\
          "name": "avg"\
        }\
      ]\
    },
    {\
      "metric": "mb_demo_mt_altitude",\
      "groupBy": "fleet",\
      "label": "Fleet - AVG",\
      "transforms": [\
        {\
          "name": "partition",\
          "arg": {\
            "aggregator": "AVG",\
            "window": "PT5M"\
          }\
        },
        {\
          "name": "avg"\
        }\
      ]\
    }\
  ]\
} \
```

Output:

```
"results:" [
  {
    "marker": "674d86ba-a810-4065-942b-0b7ca2f95db2",
    "series": [
      {
        "label": "Series - Avg",
        "values": [
          {
            "timestamp": "2020-05-01T21:05:00Z",
            "value": 157.43086
          },
          {
            "timestamp": "2020-05-01T21:10:00Z",
            "value": 162.92278
          }
        ]
      }
    ]
  },
  {
    "marker": "846aa334-232a-4015-b033-d18ebc4b1d23",
    "grouped": [
      {
        "groupingBy": "fleet",
        "groups": [
          {
            "group": "86fac11787333200a328c5b836cb0b4e",
            "label": "Bantams",
            "series": {
              "label": "Fleet - AVG",
              "values": [
                {
                  "timestamp": "2020-05-01T21:05:00Z",
                  "value": 159.70201
                },
                {
                  "timestamp": "2020-05-01T21:10:00Z",
                  "value": 165.1136
                }
              ]
            }
          },
          {
            "group": "4afac11787333200a328c5b836cb0b4e",
            "label": "Bumble Untd",
            "series": {
              "label": "Fleet - AVG",
              "values": [
                {
                  "timestamp": "2020-05-01T21:05:00Z",
                  "value": 154.5403
                },
                {
                  "timestamp": "2020-05-01T21:10:00Z",
                  "value": 160.13445
                }
              ]
            }
          }
        ]
      }
    ]
  }
]
```

## MetricBase Time Series - POST /now/clotho/transform/stream

Returns a stream of transformed time series data for one or more metrics after applying the specified list of transforms.

Streaming data in this manner allows you to process the data as individual transforms are completed and returned, rather than waiting for all transform results to be completed and downloaded. If large amounts of data need to be processed by the client, this type of processing reduces the end-to-end processing time and potentially reduces the memory usage on the client.

By setting the corresponding Accept header value in your request, you can:

-   Specify the streamed data to be encoded in a binary format,
-   Serialize streamed data into a JSON array, or
-   Stream data back to the client in a wide or narrow CSV format.

The endpoint streams the data as transforms are completed on the MetricBase server, without groupings or a predetermined ordering. Data streamed in binary format is smaller in size than the JSON representation returned by the [MetricBase Time Series - POST /now/clotho/transform](Clotho-Time-Series-API.md#) endpoint.

### URL format

Versioned URL: `/api/now/{api_version}/clotho/transform/stream`

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

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_display\_value

</td><td id="entry-sysparm_display_value-metricbase">

Flag that indicates whether to label the result data with the subject record display value if no other label is specified.Valid values:

-   true: Result data is labeled with the subject record display value.
-   false: Result data is not labeled with the subject record display value.

Data type: Boolean

Default: false

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

end

</td><td>

Required. End time of the evaluation period. An empty or missing value is treated as the current time. Time values are inclusive of this end time.Data type: String

Format: ISO 8601 \(UTC\), either:

-   Absolute date format \[YYYY-MM-DDThh:mm:ss\], such as `2019-03-20T17:04:55`.
-   Relative to current time duration format`[P(n)Y(n)M(n)DT(n)H(n)M(n)S]`, such as `P1M`.

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. Unusually large values can impact system performance.Data type: Number

Default: 10,000

</td></tr><tr><td>

metrics

</td><td>

List of metrics objects to use in the transform. For more information on metrics, see [Metrics](https://www.servicenow.com/docs/access?context=c_MetricDefinitionSupport&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).Data type: Array

 ```
"metrics": [
  {
    "label": "String",
    "metric": "String",
    "transforms": [Array]
  }
]
```

</td></tr><tr><td>

metrics.label

</td><td>

Label to use for this metric’s result set. It replaces any labels generated by the transform chain.Data type: String

Default: Generated default label.

</td></tr><tr><td>

metrics.metric

</td><td>

Required if **metrics** object is passed. Metric field to use in the transform. This field must be in the table specified in the **table** parameter. Data type: String

</td></tr><tr><td>

metrics.transforms

</td><td>

List of transforms \(transform chain\) to apply to the retrieved time series data. Each transform builds on the results of the previous transform. For a list of available transforms, see [Supported Transforms](Clotho-Time-Series-API.md#Supported_transforms) below.Data type: Array of Objects

```
"transforms": [
  {
    "arg": {Object},
    "name": "String"
  }
]
```

</td></tr><tr><td>

metrics.transforms.arg

</td><td>

Dependent on the transform. Parameter or parameters to pass into the transform.General guidelines:

-   Don't use the **arg** parameter when specifying transformations that do not take a parameter.
-   Use Number, String, or Boolean for transforms that take a single parameter.
-   Use a JSON object, with the appropriate name-value pairs, for transforms that take more than one parameter.

Data type: Number, String, Boolean, or JSON object, depending on transform. \(For a list of available transforms, refer to the table [Supported transforms](Clotho-Time-Series-API.md#Supported_transforms) below.\)

</td></tr><tr><td>

metrics.transforms.name

</td><td>

Required if a **transforms** object is specified. Name of the transform.For a list of available transforms, refer to the table [Supported transforms](Clotho-Time-Series-API.md#Supported_transforms) below.

Data type: String

</td></tr><tr><td>

query

</td><td>

Encoded query to use to filter the result set. You can compose the query using the specified table’s filter editor. Once created, select **Copy URL** from the filter’s breadcrumbs context menu.

Data type: String

Default: None

</td></tr><tr><td>

start

</td><td>

Required. Start time of the evaluation period. The special value `all` can be used to set the start time as the current time minus the maximum retention period for the specified metrics. An empty or missing value is treated as an implicit `all`. Time values are inclusive of this start time.Data type: String

Format: ISO 8601 \(UTC\), either:

-   Absolute date format \[YYYY-MM-DDThh:mm:ss\], such as `2019-03-20T17:04:55`
-   Relative to current time duration format`[P(n)Y(n)M(n)DT(n)H(n)M(n)S]`, such as `P1M`.

</td></tr><tr><td>

table

</td><td>

Required. Name of the table that contains the GlideRecord associated with this series.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Supports the following: -   **application/json**
-   **application/octet-stream** or
-   **text/csv**

 To specify the CSV format, use `text/csv;format=narrow` or `text/csv;format=wide`.

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

Data format of the response body. Based on the specified Accept values of the request, use:-   **application/json**
-   **application/octet-stream** or
-   **text/csv**

If multiple Accept types are specified, the first supported type is returned.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed and data will begin streaming.**Note:** A 200 response can still incur a processing error midstream as the transforms are computed.

</td></tr><tr><td>

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

405

</td><td id="entry-405-status-code">

Invalid method. The functionality is disabled.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(Octet-stream or JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Output Stream \(Octet-Stream\)

</td><td>

If the Accept request header is set to **application/octet-stream**, the matching MetricBase data is returned as a binary serialized stream. The Clotho-Util for Java applications provide a deserializer that enables you to parse this data.The stream consists of a binary serialization of each datum, preceded by an integer representing its length. The following entries describe the data within the binary representation and the order of that data.

</td></tr><tr><td>

CSV Stream \(UTF-8 Stream\)

</td><td>

If the Accept request header is set to **text/csv**, the matching MetricBase data is returned as UTF-8 encoded CSV data in wide or narrow formats.A narrow format returns subject and time stamp columns and a column for each returned metric. A wide format returns a time stamp column with a separate column for each metric-subject pair.

</td></tr><tr><td>

Subject

</td><td>

Source of the data. For example, if the metric for the data is drone altitudes, this value may be the ID of a specific drone. If a colon is included in the value, the parts after the subject represent the metric that the data is a part of. Null values are represented by an encoded empty string.Data type: String \(Java Modified UTF\)

Size: 2+ bytes

</td></tr><tr><td>

Dimension

</td><td>

Metric that the data is from. Null values are represented by an encoded empty string. Data type: String \(Java Modified UTF\)

Size: 2+ bytes

</td></tr><tr><td>

Label

</td><td>

Label of the data. Null values are represented by an encoded empty string.Data type: String \(Java Modified UTF\)

Size: 2+ bytes

</td></tr><tr><td>

Type

</td><td>

Type of data encoded into a byte.Possible values:

-   Float Mode
-   Float Signal
-   Double Model
-   Double Signal

Data type: Byte

Size: 1 byte

</td></tr><tr><td>

Flags

</td><td>

Encoded **serializeFlags** variable. If **serializeTags** is true and the data contains tags, the value is 2, otherwise it is 0.Data type: Byte

Size: 1 byte

</td></tr><tr><td>

Period

</td><td>

Period associated with the data. Data type: Number \(Integer\)

Size: 4 bytes

</td></tr><tr><td>

Number of Tags

</td><td>

If **serializeTags** is true, then this is the number of tags stored in the data. Data type: Number \(Integer\)

Size: 4 bytes

</td></tr><tr><td>

Tags

</td><td>

If **serializeTags** is true, each tag is stored in the data.Data type: String \(Java modified UTF\)

Size: Depends on number of tags \(2+ bytes\).

</td></tr><tr><td>

Start Epoch Second

</td><td>

Epoch UTC time representing the start time of this data series. Data type: Number \(Long\)

Size: 8 bytes

</td></tr><tr><td>

Number of Values

</td><td>

Number of values stored in this data. Data type: Number \(Integer\)

Size: 4 bytes

</td></tr><tr><td>

Values

</td><td>

If **Type** is `Float Signal`, then the remainder consists of float values.Size: **Number of Values** \* 4

Data type: Number \(Float\)

</td></tr><tr><td>

Values

</td><td>

If **Type** is `Double Signal`, then the remainder consists of double values. Data type: Number \(Double\)

Size: **Number of Values** \* 4 bytes

</td></tr><tr><td>

Model Json \(Model\)

</td><td>

If **Type** is `Float Model` or `Double Model`, the remainder is a Java Modified UTF String representing the model as JSON. Data type: String \(Java Modified UTF\)

Size: 2+ bytes

</td></tr><tr><td>

Big Model Marker \(Big Model\)

</td><td>

If the length of the model’s JSON is greater than 65,535 bytes, then this field is written instead of the **Model Json**. Data type: String \(Java Modified UTF\)

Size: 5

</td></tr><tr><td>

Big Model Size \(Big Model\)

</td><td>

Length of the JSON representation of the big model. Data type: Number \(Integer\)

Size: 4 bytes

</td></tr><tr><td>

Big Model Json \(Big Model\)

</td><td>

JSON representation of the model as a series of UTF characters, The size is dictated by the **Big Model Size** field.Data type: String \(UTF chars\)

Size: 65535-256000 bytes

</td></tr><tr><td>

JSON Stream \(JSON\)

</td><td>

If the Accept request header is set to **application/json**, the matching MetricBase data is returned as a stream of new line separated JSON objects. The following entries describe the possible elements in each returned object.

</td></tr><tr><td>

label

</td><td>

Data’s label. This value is either generated by the endpoint or is the value passed in the **metrics.label** parameter.Data type: String

</td></tr><tr><td>

period

</td><td>

Amount of time between each value. For example, a period of 60 would mean that each value is a minute apart. Data type: Number

Unit: Seconds

</td></tr><tr><td>

range

</td><td>

Start and end times of the data Data type: Array

Format: ISO 8601 \(UTC\)

</td></tr><tr><td>

series

</td><td>

Identifies the individual data. If present, is typically in the form of `[glide record id]:[metric]`. This may not be present when using transforms.Data type: String

</td></tr><tr><td>

species

</td><td>

Type of return data. For a series of either float or double values, this is either FLOAT\_SIGNAL or DOUBLE\_SIGNAL. For a model meant to analyze float or double data, this is either FLOAT\_MODEL or DOUBLE\_MODEL.Data type: String

</td></tr><tr><td>

tags

</td><td>

Tags associated with the data.Data type: Array of Strings

</td></tr><tr><td>

value

</td><td>

Float or Double values for the data.Data type: Array of Numbers

</td></tr><tr><td>

error

</td><td>

Error message if the transformation of the specified data series fails.Data type: String

</td></tr></tbody>
</table>### Supported transforms

<table id="id_abm_vgl_2tb"><thead><tr><th>

Transform

</th><th>

Description

</th></tr></thead><tbody><tr id="version-row-RESTAPI"><td>

add

</td><td>

Adds the specified number to each timestamp value.Argument: arg \(Decimal data type\) – Number to add.

For example:

```
"transforms": [
  {
    "name": "add",
    "arg": 8
  }
]
```

</td></tr><tr><td>

autocorrelate

</td><td>

Calculates the correlation between timestamp values separated by an increasing number of periods starting at 1.

</td></tr><tr><td>

avg

</td><td>

Aggregates the time series into one series containing the average value for each corresponding timestamp across the input.

</td></tr><tr><td>

bottom

</td><td>

Returns the specified number of series that have the lowest values.Argument: `arg` \(Integer\) – The number of series to return.

For example, the following returns the two time series that contain the lowest sets of values.

```
"transforms": [
  {
     "name": "bottom",
     "arg": 2
  }
]
```

</td></tr><tr><td>

ceil

</td><td>

Rounds the value in each timestamp up to the specified precision: `ceil(value / <arg>) * <arg>)` Argument: arg \(Decimal data type\) – Decimal precision to round up to.

</td></tr><tr><td>

collect

</td><td>

Displays the transform results of the transform chain up to the point of the collect transform call. Collect transform results contain a unique marker, but you may want to also define a label.For example:

```
{
  "start": "PT1H",
  "end": "",
  "table": "mb_demo_drone",
  "limit": 5000,
  "metrics": [
    {
      "metric": "mb_demo_mt_altitude",
      "transforms": [
        {
          "name": "label",
          "arg": "Series Timestamp Values"
        },
        {
          "name": "collect"
        },
        {
          "name": "avg"
        },
        {
          "name": "label",
          "arg": "Average Timestamp Values"
        }
      ]
    }
  ]
}
```

</td></tr><tr><td>

constrainValues

</td><td>

Replaces any value outside the specified range with the corresponding maximum or minimum value.For example, if you specified the following, the transform replaces any value that is less than 0 with 0, and any value that is more than 100 with 100.

```
"transforms": [
  {
    "name": "constrainValues",
    "val1": 0,
    "val2": 100
  }
]
```

Arguments:

-   val1 \(Decimal data type\): Minimum or maximum value.
-   val2 \(Decimal data type\): Minimum or maximum value.

</td></tr><tr><td>

count

</td><td>

Aggregates the time series into one series. The new series contains the number of values that are not NaN \(Not a Number\) for each corresponding timestamp across the series.

</td></tr><tr><td>

derivative

</td><td>

Determines the rate of change between timestamps. Divides the difference between the value in each timestamp and the value in the next timestamp by the timestamp’s period.**Note:** This transform returns one less value than the number of values in the series.

</td></tr><tr><td>

div

</td><td>

Divides the value in each timestamp by the specified number \(arg\).Argument: arg \(Decimal – The number by which to divide the value of each timestamp.

</td></tr><tr><td>

envelope

</td><td>

Returns two time series, where, at any point in time, one contains the largest value and the other contains the smallest value.**Note:** NaNs are ignored, but are returned if there are no other return values.

</td></tr><tr><td>

exp

</td><td>

Raises the value of the specified base to the power of the value in each timestamp.Argument: arg \(Decimal data type\) – The base value.

</td></tr><tr><td>

filter

</td><td>

Applies an aggregator to the contents of a sliding window, such as producing a moving average.Arguments:

-   aggregator \(Aggregator data type\): Type of aggregation to perform.
-   window \(Duration data type\): The duration of the sliding window.

</td></tr><tr><td>

floor

</td><td>

Rounds the value in each timestamp down to the specified precision: `floor(value / <arg>) * <arg>` Argument: arg \(Decimal data type\) – The decimal precision to round down to.

</td></tr><tr><td>

fractiles

</td><td>

Returns a time series for each fraction in the specified array. Each timestamp value is the value at which the specified fraction of values, for the corresponding timestamp across the input series, is below the specified percentage. For example, if the fraction is 0.5, then the value in the timestamp is the value where half the values in the input series are below 0.5.Argument: arg \(Array of Decimal\) – The fractions to use on the input series.

For example:

```
"transforms": [
  {
    "name": "fractiles",
    "arg": [0.25, 0.5, 0.75, 1]
  }
]
```

</td></tr><tr><td>

groupBy

</td><td>

Groups data by the specified fields before collecting or applying aggregated transformations.Argument: arg \(String\) - A comma separated list of fields in the table to use to group the transform results.

For example:

```
 "transforms": [
  {
    "name": "groupBy",
    "arg": "model"
  },
  {
    "name": "avg"
  },
  {
    "name": "label",
    "arg": "Model: %g"
  }
]
```

</td></tr><tr><td>

integrate

</td><td>

Multiplies the value in each timestamp by its period.

</td></tr><tr><td>

interpolate

</td><td>

Creates a data value for a NaN data item by interpolating from adjacent data values.Argument: arg \(Integer\) – Number of data samples in each direction to check for a non-NaN value. If a non-NaN value is not found, then NaN is used.

</td></tr><tr><td>

inverse

</td><td>

Computes the inverse of each timestamp value.

</td></tr><tr><td>

iqr

</td><td>

Performs an interquartile range transform and creates a result set that contains four series: 1.  -IQR: The median of all entries below `Q1 - (1.5 * IQR)`.
2.  Q1: The median of the smallest half of entries.
3.  Q3: The median of the largest half of entries.
4.  +IQR: The median of all entries above `Q3 + (1.5 * IQR)`.

**Note:** `IQR = Q3 - Q1`

</td></tr><tr><td>

label

</td><td>

Labels a transformation chain.**Note:** Subsequent transformations may modify or replace the label.

Argument: arg \(String\) – Text of the label. Can contain the following formatting expressions:

-   %%: Escape a "%" literal.
-   %l: Current label that is being replaced.
-   %s: Series subject.
-   %g: Value of the group by field. If this is a referenced record, then the value of the record’s name field. If multiple groups are specified in the **groupBy** transform, labels are comma separated.
-   %G: Value of the group by field. If this is a referenced record, then the record’s sys\_id. If multiple groups are selected, values are comma separated.

For example:

```
"transforms": [
  {
    "name": "label",
    "arg": "Series Timestamp Values"
  },
]
```

```
"transforms": [
  {
    "name": "groupBy",
    "arg": "model"
  },
  {
    "name": "avg"
  },
  {
    "name": "label",
    "arg": "Model: %g"
  }
]
```

</td></tr><tr><td>

limit

</td><td>

Returns, at most, the specified duration or number of values, starting with the most recently saved value.Arguments:

-   arg \(Integer\): Number of timestamp values to return for each time series.

OR

-   arg \(Duration data type\): Duration to limit each time series to.

</td></tr><tr><td>

log

</td><td>

Runs a logarithm on the value in each timestamp where the result is the log of the specified base for the timestamp value.Argument: arg \(Decimal data type\) – Base for the logarithm calculation.

</td></tr><tr><td>

mapValues

</td><td>

Replaces any values within the specified range \(inclusive\) with the specified value. If both **lowerBound** and **upperBound** are specified as NaN, then it replaces any NaN value with the **targetValue**.Arguments:

-   lowerBound \(Decimal data type\): The lowest value in the range.
-   upperBound \(Decimal data type\): The highest value in the range.
-   targetValue \(Decimal data type\): Replacement value.

For example, the following changes all values in the time series that are between .1 and .9 to 1:

```
"transforms": [
  {
    "name": "mapValues",
    "lowerBound": .1,
    "upperBound": .9,
    "targetValue": 1
  }
]
```

</td></tr><tr><td>

max

</td><td>

Returns a series that contains the maximum value for each corresponding timestamp across the input.

</td></tr><tr><td>

median

</td><td>

Creates a series that contains the median of values for each timestamp across a set of series.If there are `n` series:

-   If `n` is odd, the median is the `(n / 2 + 1)` value for a timestamp.
-   If `n` is even, the median is the average of the `(n / 2)` and `(n / 2 + 1)` values for a timestamp.

</td></tr><tr><td>

min

</td><td>

Returns a series that contains the minimum value for each corresponding timestamp across the input.

</td></tr><tr><td>

mul

</td><td>

Multiplies the value in each timestamp by the specified number.Argument: arg \(Decimal data type\) – Number by which to multiply the value of each timestamp.

</td></tr><tr><td>

partition

</td><td>

Produces a new series with values filtered by applying a specified aggregator to a non-overlapping window.

 Arguments:

-   aggregator \(Aggregator data type\): Type of aggregation to perform.
-   base \(DateTime data type\): The zero offset to use for partitioning. For example, to partition by day \(24h\), set this value to Monday at midnight in your time zone. To partition by a 30-day period, set this value to the first day of the most recent month.

Default: Beginning of the EPOCH.

-   window \(Duration data type\): The duration of the non-overlapping window to apply the aggregator.

</td></tr><tr><td>

pow

</td><td>

Raises each timestamp value to the specified power.Argument: arg \(Decimal data type\) – Power to which to raise each value.

</td></tr><tr><td>

product

</td><td>

Aggregates the selected metric series into a single series that contains the product of all values for each timestamp. NaNs are excluded. If all numbers in the series are NaN, the output is also NaN.

</td></tr><tr><td>

resample

</td><td>

Resamples a time series to either a fixed number of points or from one frequency to another.Use the resample transformation to reduce the number of samples in the result set to more closely match the number of samples that you want to display.

Arguments: You can pass various arguments for this transform. Below is a list of each of the possible argument groups. Only one of these argument groups can be passed within a single transform. The following argument groups are delineated by AND/OR. AND meaning the argument is part of the current group; OR meaning it is the start of a new argument group.

-   arg \(Integer\): Number of samples to include in the result set. If available samples are less than this number, the endpoint uses interpolation to create additional samples. If there are more samples than this number, they are reduced by averaging them.

OR

-   arg \(Duration data type\): The frequency at which to resample. If available samples are less than this number, the endpoint uses interpolation to create additional samples. If there are more samples than this number, they are reduced by averaging them.

OR

-   minValues \(Integer\): The minimum number of samples to include in the result set. If available samples are less than this number, the endpoint uses interpolation to create additional samples.

AND

-   maxValues \(Integer\): The maximum number of samples to include in the result set. If there are more samples than this number, they are reduced by averaging them.

OR

-   aggregator \(Aggregator data type\): The aggregator to use when resampling.

AND

-   values \(Integer\): The number of samples to include in the result set. If available samples are less than this number, the endpoint uses interpolation to create additional samples. If there are more samples than this number, they are reduced by applying the specified **aggregator** to them.

OR

-   aggregator \(Aggregator data type\): The aggregator to use when resampling.

AND

-   period \(Duration data type\): The frequency at which to resample. If available samples are less than this number, the endpoint uses interpolation to create additional samples. If there are more samples than this number, they are reduced by applying the specified **aggregator** to them.

OR

-   aggregator \(Aggregator data type\): The aggregator to use when resampling.

AND

-   minValues \(Integer\): The minimum number of samples to include in the result set. If available samples are less than this number, the endpoint uses interpolation to create additional samples.

AND

-   maxValues \(Integer\): The maximum number of samples to include in the result set. If there are more samples than this number, they are reduced by averaging them.

</td></tr><tr><td>

round

</td><td>

Rounds the value in each timestamp up to the specified precision: `(value / <arg>) * <arg>` Argument: arg \(Decimal data type\) – The decimal precision to round up to.

</td></tr><tr><td>

root

</td><td>

Calculates the root of each timestamp value using the specified index.Argument: arg \(Decimal data type\) – The index of the root.

For example, the following returns the square root of each timestamp:

```
"transforms": [
  {
    "name": "root",
    "arg": "2"
  },
]
```

</td></tr><tr><td>

stddev

</td><td>

Creates a series that contains the standard deviation of values for each timestamp across a set of series.

</td></tr><tr><td>

sub

</td><td>

Subtracts the specified number from the value in each timestamp.Argument: arg \(Number\) – The number to subtract from the value in each timestamp.

</td></tr><tr><td>

sum

</td><td>

Aggregates the selected metric series into one series that contains the sum of all values for each timestamp, excluding any NaNs. If all numbers in the series are NaN, the output is NaN.

</td></tr><tr><td>

timeshift

</td><td>

Shifts the time range by adding the specified offset to a value’s timestamp without modifying the value. Use this transform to shift timestamps to another timezone.Argument: arg \(Duration data type\) – The amount of time to shift by.

</td></tr><tr><td>

top

</td><td>

Returns the specified number of series that have the highest values.Argument: arg \(Integer\) – The number of series to return.

For example, the following returns the two time series that contain the highest sets of values.

```
"transforms": [
  {
     "name": "top",
     "arg": 2
  }
]
```

</td></tr></tbody>
</table><table id="id_uq3_hhl_2tb"><thead><tr><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td id="Aggregator">

Aggregator

</td><td>

Available aggregators to use within the transform.-   AVG: Calculates the arithmetic mean of all currently selected series.
-   CHISQUARE: Shows how well a statistical model fits the metric dataset.
-   LAST: Returns the last defined value in the period window.
-   MAX: Shows the largest value for the metric dataset, at each point in time.
-   MEDIAN: Shows the median of the metric dataset. The median separates the higher values of the metric dataset from the lower values.
-   MIN: Shows the smallest value for the metric dataset, at each point in time.
-   STDDEV: Calculates the standard deviation across the underlying data. Used to quantify the variation or dispersion of a set of data values in the metric dataset.
-   SUM: Calculates the sum across all currently selected series.

</td></tr><tr><td id="DateTime">

DateTime

</td><td>

Absolute date/time values are specified by the ISO 8601 date and time format: `YYYY-MM-DDThh:mm:ss`. For example: 2020-02-28T13:10:42.Where:

-   \[YYYY\]: Four-digit year.
-   \[MM\]: Zero-padded month between 01 and 12.
-   \[DD\]: Zero-padded day between 01 and 31.
-   T: Represents time and is mandatory before any of the time components are specified.
-   \[hh\]: Zero-padded hour between 00 and 23.
-   \[mm\]: Zero-padded minutes between 00 and 59.
-   \[ss\]: Zero-padded seconds between 00 and 59. Note that leap seconds are spread out evenly across the previous 1,000 seconds.

Relative date/time values are specified using a duration \(Duration data type\), which is subtracted from the current time.

For example: P7D = seven days ago.

</td></tr><tr><td id="Decimal">

Decimal

</td><td>

Decimal value that can either be: -   A signed decimal number of arbitrary precision that can use exponential notation.

Such as:

    -   2
    -   1.7
    -   -3.47
    -   1.0E+2
-   A string representation of:
    -   A signed decimal number that may use exponential notation and is guaranteed to be a double-precision 64-bit IEEE 754 floating-point number.
    -   "NaN"
    -   "-Infinity"
    -   "+Infinity"

</td></tr><tr><td id="Duration">

Duration

</td><td>

Amount of time in a time interval. Duration values are specified by the ISO 8601 duration format: `P[n]Y[n]M[n]DT[n]H[n]M[n]S` Where:

-   P: Duration designator, referred to as "period", and is always placed at the beginning of the duration.
-   \[n\]Y: Number of years.
-   \[n\]M: Number of months.
-   \[n\]D: Number of days.
-   T: Time designator and is mandatory before any of the time components are specified.
-   \[n\]H: Number of hours.
-   \[n\]M: Number of minutes.
-   \[n\]S: Number of seconds.

For example:

-   P7D: Period of seven days.
-   P1M: Period of one month.
-   PT15M: Period of 15 minutes.
-   P1DT12H: Period of one day and twelve hours.

</td></tr></tbody>
</table>### cURL request

The following example shows how to call this endpoint to return a JSON stream for metrics on the mb\_demo\_drone table. Note: While the objects in this example are expanded to multiple lines for legibility, in an actual result each returned object is on its own line. You can make the same call and return an octet stream by setting `--header "Accept:application/octet-stream" \`.

```
curl "localhost:8080/api/now/v1/clotho/transform/stream" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user "username":"password" \
-d "{\
  \"start\": \"PT5M\",\
  \"end\": \"\",\
  \"table\": \"mb_demo_drone\",\
  \"query\": \"fleet.nameSTARTSWITHB\",\
  \"limit\": 5000,\
  \"metrics\": [\
    {\
      \"metric\": \"mb_demo_mt_altitude\",\
      \"label\": \"Series - Avg\",\
      \"transforms\": [\
        {\
          \"name\": \"partition\",\
          \"arg\": {\
            \"aggregator\": \"AVG\",\
            \"window\": \"PT5M\"\
          }\
        },
        {\
          \"name\": \"avg\"\
        }\
      ]\
    },
    {\
      \"metric\": \"mb_demo_mt_altitude\",\
      \"groupBy\": \"fleet\",\
      \"label\": \"Fleet - AVG\",\
      \"transforms\": [\
        {\
          \"name\": \"partition\",\
          \"arg\": {\
            \"aggregator\": \"AVG\",\
            \"window\": \"PT5M\"\
          }\
        },
        {\
          \"name\": \"avg\"\
        }\
      ]\
    }\
  ]\
}"
```

Response:

```
[
  {
    "label": "Series - Avg",
    "tags": [
      "#4fb1114f-2426-4acb-8e3e-6435dd62134c"
    ],
    "species": "DOUBLE_SIGNAL",
    "range": [
      "2022-06-16T17:50:00Z",
      "2022-06-16T17:50:00Z"
    ],
    "values": [
      132.86805196126303
    ],
    "period": 300
  },
  {
    "label": "Fleet - AVG",
    "tags": [
      ":fleet:86fac11787333200a328c5b836cb0b4e:Bantams",
      "#6641aab4-c55f-4d11-8846-26b0b706ec1c"
    ],
    "species": "DOUBLE_SIGNAL",
    "range": [
      "2022-06-16T17:50:00Z",
      "2022-06-16T17:50:00Z"
    ],
    "values": [
      134.3775875908988
    ],
    "period": 300
  },
  {
    "label": "Fleet - AVG",
    "tags": [
      "#6641aab4-c55f-4d11-8846-26b0b706ec1c",
      ":fleet:4afac11787333200a328c5b836cb0b4e:Bumble Untd"
    ],
    "species": "DOUBLE_SIGNAL",
    "range": [
      "2022-06-16T17:50:00Z",
      "2022-06-16T17:50:00Z"
    ],
    "values": [
      129.02530271356756
    ],
    "period": 300
  }
]
```

The following cURL example uses the CSV format option to stream back the altitude values \(stored in the database as "mb\_demo\_mt\_altitude"\) of the last day for each drone stored in the mb\_demo\_drone \[Drones\] table of the Metricbase Demo plugin. In the example, the data is returned in a narrow table format with three columns: the Sys\_id of the subject identifying the drone, the time stamp of value, and the altitude value.

```
curl "https://instance.servicenow.com/api/now/v1/clotho/transform/stream" \
--request POST \
--header "Accept:text/csv;format=narrow" \
--header "Content-Type:application/json" \
--user "user name":"password" \
-d "{\
  \"start\": \"P1D\",\
  \"end\": \"\",\
  \"table\": \"mb_demo_drone\",\
  \"metrics\": [\
    {\
      \"metric\": \"mb_demo_mt_altitude\",\
      \"transforms\": []\
    }]\
}"
```

Output:

```
Subject, Timestamp,"mb_demo_drone|mb_demo_mt_altitude"
"a66b051787333200a328c5b836cb0b97",2022-11-07T22:35:00Z,92.84400939941406
"a66b051787333200a328c5b836cb0b94",2022-11-07T22:35:00Z,92.2428970336914
"6a6b051787333200a328c5b836cb0b97",2022-11-07T22:35:00Z,92.0076904296875
"ea6b051787333200a328c5b836cb0b92",2022-11-07T22:35:00Z,97.3113021850586
"a66b051787333200a328c5b836cb0b91",2022-11-07T22:35:00Z,108.49791717529297
"6a6b051787333200a328c5b836cb0b94",2022-11-07T22:35:00Z,109.04239654541016
"6a6b051787333200a328c5b836cb0b91",2022-11-07T22:35:00Z,93.72159576416016
"ee6b051787333200a328c5b836cb0b91",2022-11-07T22:35:00Z,107.69989776611328
"ee6b051787333200a328c5b836cb0b97",2022-11-07T22:35:00Z,100.86473083496094
"ee6b051787333200a328c5b836cb0b94",2022-11-07T22:35:00Z,95.77774047851562
"666b051787333200a328c5b836cb0b92",2022-11-07T22:35:00Z,105.19712829589844
"666b051787333200a328c5b836cb0b95",2022-11-07T22:35:00Z,105.92308807373047
"6e6b051787333200a328c5b836cb0b99",2022-11-07T22:35:00Z,93.59339141845703
"666b051787333200a328c5b836cb0b98",2022-11-07T22:35:00Z,94.51266479492188
"e26b051787333200a328c5b836cb0b94",2022-11-07T22:35:00Z,105.4367904663086
"6e6b051787333200a328c5b836cb0b96",2022-11-07T22:35:00Z,94.64836883544922
"6e6b051787333200a328c5b836cb0b93",2022-11-07T22:35:00Z,94.78523254394531
"e26b051787333200a328c5b836cb0b97",2022-11-07T22:35:00Z,96.99283599853516
"aa6b051787333200a328c5b836cb0b96",2022-11-07T22:35:00Z,106.67017364501953
"e26b051787333200a328c5b836cb0b91",2022-11-07T22:35:00Z,94.2446517944336
"aa6b051787333200a328c5b836cb0b93",2022-11-07T22:35:00Z,91.659912109375
"226b051787333200a328c5b836cb0b94",2022-11-07T22:35:00Z,99.5401840209961
"226b051787333200a328c5b836cb0b97",2022-11-07T22:35:00Z,98.13501739501953
"226b051787333200a328c5b836cb0b91",2022-11-07T22:35:00Z,92.2428970336914
"226b051787333200a328c5b836cb0b90",2022-11-07T22:35:00Z,106.41876983642578
"aa6b051787333200a328c5b836cb0b99",2022-11-07T22:35:00Z,107.69989776611328
"626b051787333200a328c5b836cb0b93",2022-11-07T22:35:00Z,92.96666717529297
"e66b051787333200a328c5b836cb0b99",2022-11-07T22:35:00Z,93.85079193115234
"e66b051787333200a328c5b836cb0b93",2022-11-07T22:35:00Z,96.07303619384766
"e66b051787333200a328c5b836cb0b96",2022-11-07T22:35:00Z,98.47595977783203
"2a6b051787333200a328c5b836cb0b92",2022-11-07T22:35:00Z,95.9247055053711
"226b051787333200a328c5b836cb0b9a",2022-11-07T22:35:00Z,99.5401840209961
"2a6b051787333200a328c5b836cb0b98",2022-11-07T22:35:00Z,103.1417465209961
"2a6b051787333200a328c5b836cb0b95",2022-11-07T22:35:00Z,96.99283599853516
"ae6b051787333200a328c5b836cb0b95",2022-11-07T22:35:00Z,94.64836883544922
"ae6b051787333200a328c5b836cb0b98",2022-11-07T22:35:00Z,101.8689956665039
"ae6b051787333200a328c5b836cb0b92",2022-11-07T22:35:00Z,107.4388198852539
"a26b051787333200a328c5b836cb0b98",2022-11-07T22:35:00Z,94.78523254394531
"266b051787333200a328c5b836cb0b93",2022-11-07T22:35:00Z,94.51266479492188
"2e6b051787333200a328c5b836cb0b97",2022-11-07T22:35:00Z,108.49791717529297
"2e6b051787333200a328c5b836cb0b91",2022-11-07T22:35:00Z,97.15129852294922
"2e6b051787333200a328c5b836cb0b94",2022-11-07T22:35:00Z,103.36128997802734
"a26b051787333200a328c5b836cb0b92",2022-11-07T22:35:00Z,100.47681427001953
"266b051787333200a328c5b836cb0b96",2022-11-07T22:35:00Z,103.5830078125
"266b051787333200a328c5b836cb0b99",2022-11-07T22:35:00Z,97.3113021850586
"a26b051787333200a328c5b836cb0b95",2022-11-07T22:35:00Z,105.92308807373047
"ea6b051787333200a328c5b836cb0b98",2022-11-07T22:35:00Z,95.34477996826172
"ea6b051787333200a328c5b836cb0b95",2022-11-07T22:35:00Z,100.47681427001953
"626b051787333200a328c5b836cb0b99",2022-11-07T22:35:00Z,100.86473083496094
"626b051787333200a328c5b836cb0b96",2022-11-07T22:35:00Z,106.9239730834961
```

## MetricBase Time Series - POST /now/clotho/put

Adds time series data to the MetricBase database.

### URL format

Versioned URL: `/api/now/{api_version}/clotho/put`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_ignore\_unknown\_series

</td><td>

Flag that indicates whether to ignore unknown series and continue the transaction without returning an error. Valid values:

-   true: Ignore unknown series.
-   false: Do not ignore unknown series.

 Default: true

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

seriesRef

</td><td>

Required. Information to update.Data type: Array of Objects

```
"seriesRef": [
  {
    "metric": "String",
    "subject": "String",
    "table": "String"
  }
]
```

</td></tr><tr><td>

seriesRef.metric

</td><td>

Required. Name of the metric to update.Data type: String

</td></tr><tr><td>

seriesRef.subject

</td><td>

Required. Sys\_id of the record in which to update the data.Data type: String

Table: Specified in the **seriesRef.table** parameter.

</td></tr><tr><td>

seriesRef.table

</td><td>

Required. Name of the table in which to save the data.Data type: String

</td></tr><tr><td>

values

</td><td>

Required. Series values to store.Data type: Array

```
"values": [
  {
    "timestamp": "String",
    "value": Number
  }
]
```

</td></tr><tr><td>

values.timestamp

</td><td>

Required. ISO 8601 timestamp of the value.Data type: String

Format: `YYYY-MM-ddTHH:mm:ddZ`

The ending ‘Z’, which denotes the UTC time zone in an ISO-formatted timestamp, is optional.

</td></tr><tr><td>

values.value

</td><td>

Required. Metric value.Data type: Number

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
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
|message|Message that indicates the status of the request, such as `ok` if the request processed successfully.|

### cURL request

```
curl "https://instance.servicenow.com/api/now/v1/clotho/put" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"seriesRef\": {
    \"subject\": \"3D666b051787333200a328c5b836cb0b92\",
    \"table\": \"mb_demo_drone\",
    \"metric\": \"mb_demo_mt_altitude\"
  },
  \"values\": [
    {
      \"timestamp\": \"2019-03-21T17:05:00Z\",
      \"value\": 0.150185
    },
    {
      \"timestamp\": \"2019-03-21T17:06:00Z\",
      \"value\": 0.46074
    },
    {
      \"timestamp\": \"2019-03-21T17:07:00Z\",
      \"value\": 0.83104
    },
    {
      \"timestamp\": \"2019-03-21T17:08:00Z\",
      \"value\": 1.260635
    },
    {
      \"timestamp\": \"2019-03-21T17:09:00Z\",
      \"value\": 1.749
    }
  ]
}" \
--user "username":"password"
```

```
{
    "result": {
        "message": "ok"
    }
}
```

