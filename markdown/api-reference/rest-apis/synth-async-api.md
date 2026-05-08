---
title: SyntheticsAsyncBulkCreate API
description: The SyntheticsAsyncBulkCreate API provides endpoints to manage asynchronous synthetic monitor creation.Checks the progress of a bulk monitor creation job.Creates multiple synthetic monitors in a single asynchronous operation.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-04-20"
reading_time_minutes: 14
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# SyntheticsAsyncBulkCreate API

The SyntheticsAsyncBulkCreate API provides endpoints to manage asynchronous synthetic monitor creation.

Use this API to create up to 5,000 monitors per request. For smaller batch operations where immediate validation and results are required, or to link monitors to incidents, use the [SyntheticsBulkCreate](synthetics-bulk-create-api.md#) API which supports creating up to 50 monitors per request.

Monitors can be created using data in JSON or CSV format. For more information about using JSON or CSV files with Postman or Terminal, see the [Synthetic Monitoring Developer Guide](../../guides/SyntheticMonitoring/concept/synth-monitor_dev-guide.md#).

This API requires the Synthetic monitoring application \(com.snc.uib.sow\_synthetics\), which is available on the ServiceNow Store. Before calling this API, at least one MID Server location must be configured for synthetic monitoring. For instructions, see Create synthetic monitoring locations. Additionally, configuration items \(CIs\) for the endpoints being monitored must exist in the Configuration Management Database \(CMDB\).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## SyntheticsAsyncBulkCreate - GET /sn\_sow\_synthetics/synthetics\_async\_bulk\_create/\{job\_id\}

Checks the progress of a bulk monitor creation job.

To call this endpoint, the user must have the x\_snc\_sow\_synthetics.synthetics\_viewer role.

### URL format

Versioned URL: `/api/sn_sow_synthetics/{api_version}/synthetics_async_bulk_create/{job_id}`

Default URL: `/api/sn_sow_synthetics/synthetics_async_bulk_create/{job_id}`

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

job\_id

</td><td>

ID of the monitor creation job.Table: Synthetics Bulk Job \[sn\_sow\_synthetics\_bulk\_job\]

Column: Job ID

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_ahp_vlg_1jc" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

HTTP basic authentication or OAuth bearer token.Basic authentication format:

```
Authorization: Basic <base64-encoded-username:password>
```

OAuth format:

```
Authorization: Bearer <access-token>
```

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Accepted. Job status successfully retrieved.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user must have the x\_snc\_sow\_synthetics.synthetics\_viewer role to check job status.|
|404|Not found. A job with the provided ID was not found in table Synthetics Bulk Job \[sn\_sow\_synthetics\_bulk\_job\].|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_glp_cmg_1jc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Object returned if the API request failed.Data type: Object

```
"error": {
   "code": "String",
   "details": {Object},
   "message": "String"
}
```

</td></tr><tr><td>

error.code

</td><td>

Error code. Possible values:

-   AUTHENTICATION\_FAILED
-   AUTHORIZATION\_FAILED
-   JOB\_NOT\_FOUND
-   INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

error.details

</td><td>

Additional details about the error. The elements included in this object vary based on the type of error.

Data type: Object

</td></tr><tr><td>

error.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

result

</td><td>

Object containing information about the status of the monitor creation job.Data type: Object

```
"result": {
   "errors": [Array],
   "job_id": "String",
   "message": "String",
   "status": "String",
   "summary": {Object}
}
```

</td></tr><tr><td>

result.job\_id

</td><td>

ID of the monitor creation job.Table: Synthetics Bulk Job \[sn\_sow\_synthetics\_bulk\_job\]

Column: Job ID

Data type: String

</td></tr><tr><td>

result.message

</td><td>

Message about the status of the monitor creation job.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the monitor creation job.Possible values:

-   pending
-   processing
-   completed
-   failed

Data type: String

</td></tr><tr><td>

result.summary

</td><td>

Current summary data for the monitor creation job.Data type: Object

```
"summary": {
   "created": Number,
   "failed": Number,
   "processed": Number,
   "successful": Number,
   "total": Number,
   "updated": Number
}
```

</td></tr><tr><td>

result.summary.created

</td><td>

Number of monitors successfully created.Data type: Number

</td></tr><tr><td>

result.summary.failed

</td><td>

Number of monitors that couldn't be created or updated.Data type: Number

</td></tr><tr><td>

result.summary.processed

</td><td>

Number of monitors processed by the job.Data type: Number

</td></tr><tr><td>

result.summary.successful

</td><td>

Number of monitors successfully created or updated.Data type: Number

</td></tr><tr><td>

result.summary.total

</td><td>

Total number of monitors included in the job.Data type: Number

</td></tr><tr><td>

result.summary.updated

</td><td>

Number of monitors successfully updated.Data type: Number

</td></tr><tr><td>

result.errors

</td><td>

Error information for failed monitors.Data type: Array

```
"errors": [
   {
      "check_number": Number,
      "error_code": "String",
      "error_message": "String",
      "name": "String"      
   }
]
```

</td></tr><tr><td>

result.errors.check\_number

</td><td>

Order of the monitor in the **checks** array provided in the request body for [POST /sn\_sow\_synthetics/synthetics\_async\_bulk\_create](synth-async-api.md#).Data type: Number

</td></tr><tr><td>

result.errors.error\_code

</td><td>

Error code.Possible values:

-   CREATE\_FAILED
-   UPDATE\_FAILED

Data type: String

</td></tr><tr><td>

result.errors.error\_message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

result.errors.name

</td><td>

Name of the monitor.Data type: String

</td></tr></tbody>
</table>### cURL request

This example checks the status of a monitor creation job.

```
curl "https://instance.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create/BCJ-1776889518281-0baf339f" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body - job processing.

```
{
   "result": {
      "job_id": "BCJ-1776889518281-0baf339f",
      "status": "processing",
      "message": "Processing in progress: 150/500 (30%)",
      "summary": {
         "total": 500,
         "processed": 150,
         "successful": 148,
         "created": 145,
         "updated": 3,
         "failed": 2
      }
   }
}
```

Response body - job successfully completed.

```
{
   "result": {
      "job_id": "BCJ-1776889518281-0baf339f",
      "status": "completed",
      "message": "Job completed successfully. 497 monitors created, 3 updated, 0 failed out of 500 total.",
      "summary": {
         "total": 500,
         "processed": 500,
         "successful": 500,
         "created": 497,
         "updated": 3,
         "failed": 0
      }
   }
}
```

Response body - job completed with errors.

```
{
   "result": {
      "job_id": "BCJ-1776889518281-0baf339f",
      "status": "completed",
      "message": "Job completed. 98 monitors created, 0 updated, 2 failed out of 100 total.",
      "summary": {
         "total": 100,
         "processed": 100,
         "successful": 98,
         "created": 98,
         "updated": 0,
         "failed": 2
      },
      "errors": [
         {
            "check_number": 23,
            "name": "Invalid Monitor",
            "error_code": "CREATE_FAILED",
            "error_message": "cmdb_ci is required"
         },
         {
            "check_number": 45,
            "name": "Bad Location Monitor",
            "error_code": "CREATE_FAILED",
            "error_message": "Location not found: invalid_sys_id"
         }
      ]
   }
}
```

## SyntheticsAsyncBulkCreate - POST /sn\_sow\_synthetics/synthetics\_async\_bulk\_create

Creates multiple synthetic monitors in a single asynchronous operation.

This endpoint supports creating up to 5,000 monitors per request, with a maximum payload size of 10MB. Calling this endpoint submits a job to asynchronously create the monitors in batches of 500. Check the job status by calling the endpoint [GET /sn\_sow\_synthetics/v1/synthetics\_async\_bulk\_create/\{job\_id\}](synth-async-api.md#).

To call this endpoint, the user must have the x\_snc\_sow\_synthetics.synthetics\_editor role.

### URL format

Versioned URL: `/api/sn_sow_synthetics/{api_version}/synthetics_async_bulk_create`

Default URL: `/api/sn_sow_synthetics/synthetics_async_bulk_create`

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
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_nk2_21q_z3c" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

checks

</td><td>

Required. Array of endpoint configuration objects to create monitors for. This array can contain a maximum of 5,000 objects per API request.Data type: Array

```
"checks": [
   {
      "alert_severity": Number,
      "alert_tags": {Object},
      "body": "String",
      "body_condition": {Object},
      "cmdb_ci": "String",
      "credential": "String",
      "description": "String",
      "enabled": Boolean,
      "headers": [Array],
      "interval": Number,
      "locations": [Array],
      "max_latency_ms": Number,
      "method": "String",
      "name": "String",
      "parent_service_sys_id": "String",
      "query_string": "String",
      "should_create_alert": Boolean,
      "single_api_check_sys_id": "String",
      "support_group_sys_id": "String",
      "valid_http_code": "String",
      "valid_http_code_type": "String"
   }
]
```

</td></tr><tr><td>

checks.alert\_severity

</td><td>

Severity level of alerts created for failed monitor tests. Only use this parameter if **checks.should\_create\_alert** is set to `true`.Valid values:

-   `1`: Critical
-   `2`: Major
-   `3`: Minor
-   `4`: Warning
-   `5`: OK

Default: 1

Data type: Number

</td></tr><tr><td>

checks.alert\_tags

</td><td>

Custom tags to use for alerts created for failed monitor tests. Only use this parameter if **checks.should\_create\_alert** is set to `true`.The elements contained in this object vary based on the tags used. For example, tags could be used for the environment or team as shown below.

```
//Example custom tags
"alert_tags": {
   "environment": "production",     
   "team": "platform"     
}
```

Default: Empty object

Data type: Object

</td></tr><tr><td>

checks.body

</td><td>

Request body for POST, PUT, or PATCH endpoints. Must be a valid JSON or XML string depending on the `Content-Type` header. Maximum size is 10KB.Default: Null

Data type: String

</td></tr><tr><td>

checks.body\_condition

</td><td>

Response body validation.Data type: Object

```
"body_condition": {     
   "expression": "String",
   "type": "String"     
}
```

</td></tr><tr><td>

checks.body\_condition.expression

</td><td>

Expression to check the response body against. The expression can be any string value, including support for regex, JSONPath, and XPath.Default: Null

Data type: String

</td></tr><tr><td>

checks.body\_condition.type

</td><td>

Type of validation used to evaluate the response body against **checks.body\_condition.expression**.Valid values \(case-sensitive\):

-   `equals`: Exact match.
-   `not_equals`: Not equal to.
-   `contains`: Contains substring.
-   `not_contains`: Does not contain substring.
-   `regex`: Regular expression match.
-   `jsonpath`: JSONPath expression match.
-   `xpath`: XPath expression match. Used for XML responses.

Default: Null

Data type: String

</td></tr><tr><td>

checks.cmdb\_ci

</td><td>

Required. Sys\_id of the CMDB endpoint configuration item \(CI\).Table: HTTP Endpoint \[cmdb\_ci\_endpoint\_http\]

Data type: String

</td></tr><tr><td>

checks.credential

</td><td>

Sys\_id of the credential for the monitor to include in the endpoint request.Table:

Default: Null

Data type: String

</td></tr><tr><td>

checks.description

</td><td>

Description of the monitor.Data type: String

</td></tr><tr><td>

checks.enabled

</td><td>

Flag that indicates whether the monitor will start executing immediately after creation.Valid values:

-   true: The monitor starts executing immediately after creation.
-   false: The monitor won't start executing until it is enabled.

Default: true

Data type: Boolean

</td></tr><tr><td>

checks.headers

</td><td>

Array of HTTP headers for the monitor to include in the endpoint request.Data type: Array

Default: Empty array \(no headers\)

```
"headers": [
   {
      "name": "String",
      "value": "String"
   }
]
```

</td></tr><tr><td>

checks.headers.name

</td><td>

Name of the HTTP header, such as `Authorization` or `Content-Type`.Data type: String

</td></tr><tr><td>

checks.headers.value

</td><td>

Value of the HTTP header, such as `Bearer token` or `application/json`.Data type: String

</td></tr><tr><td>

checks.interval

</td><td>

Required. Frequency of monitor execution in minutes.ServiceNow hosted locations are limited to 6 tests per minute per monitor.

Valid values: 1-60

For example, a value of `5` sets the monitor to execute once every five minutes.

Data type: Number

</td></tr><tr><td>

checks.locations

</td><td>

Required. List of sys\_ids of MID Server locations to use for the monitor.Table: Synthetic Location \[sn\_sow\_synthetics\_location\]

Data type: String

</td></tr><tr><td>

checks.max\_latency\_ms

</td><td>

Maximum acceptable response time in milliseconds. The general guideline is 500-5000ms depending on the endpoint type. The monitor checks against this value when testing, and the test fails if the response time exceeds this value.

Default: Null \(no latency threshold\)

Data type: Number

</td></tr><tr><td>

checks.method

</td><td>

Required. HTTP method to use. Valid values \(case-insensitive\):

-   DELETE
-   GET
-   HEAD
-   PATCH
-   POST
-   PUT

Data type: String

</td></tr><tr><td>

checks.name

</td><td>

Required. Display name for the monitor.Maximum length: 100 characters

Data type: String

</td></tr><tr><td>

checks.parent\_service\_sys\_id

</td><td>

Required. Sys\_id of the business service this endpoint supports. Used for service-level reporting and impact analysis.Table: Business Service \[cmdb\_ci\_service\]

Data type: String

</td></tr><tr><td>

checks.query\_string

</td><td>

Query parameters for the monitor to include in the endpoint request.Default: Null

Data type: String

</td></tr><tr><td>

checks.should\_create\_alert

</td><td>

Flag that indicates whether the monitor will create an alert if a test fails.Valid values:

-   true: Alerts are created if monitor tests fail.
-   false: Alerts aren't created if monitor tests fail.

Default: false

Data type: Boolean

</td></tr><tr><td>

checks.single\_api\_check\_sys\_id

</td><td>

Sys\_id of the monitor for the endpoint. Use this parameter to update an existing monitor.Table: Single API \[sn\_sow\_synthetics\_check\_single\_api\]

Default: Null

Data type: String

</td></tr><tr><td>

checks.support\_group\_sys\_id

</td><td>

Required. Sys\_id of the support group responsible for this endpoint. Used for alert routing and assignment.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

checks.valid\_http\_code

</td><td>

Expected HTTP status codes for a successful response. Valid formats:

-   Single value, such as `200`.
-   Range of values, such as `200-202`.
-   Comma-separated list of values, such as `'200,201,204'`.

The monitor checks against these values when testing, and the test fails if the actual status code doesn't match a value in the list.

Default: Null

Data type: String

</td></tr><tr><td>

checks.valid\_http\_code\_type

</td><td>

Type of validation used to check the HTTP status code from a response.Valid values \(case-sensitive\):

-   `equals`: Checks for an exact match with **checks.valid\_http\_code**.
-   `in_range`: Checks that the status code is within the range of values provided in **checks.valid\_http\_code**.
-   Regex: Provide a regular expression to check the status code against. For example, `2[0-9]{2}` matches codes 200-299.

Default: Null

Data type: String

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

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

HTTP basic authentication or OAuth bearer token.Basic authentication format:

```
Authorization: Basic <base64-encoded-username:password>
```

OAuth format:

```
Authorization: Bearer <access-token>
```

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **application/json** or **text/csv**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_cqm_nqf_1jc"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

202

</td><td>

Accepted. A bulk monitor creation job was submitted.

</td></tr><tr><td>

400

</td><td>

Bad request. Request validation failed. Check **error.code** and **error.message** in the response body for error details.Common causes:

-   Malformed JSON or CSV payload.
-   Required field not provided.
-   Field value out of range or not valid.
-   Referenced endpoint CI not found in table HTTP Endpoint \[cmdb\_ci\_endpoint\_http\].
-   Referenced MID Server location not found in table Synthetic Location \[sn\_sow\_synthetics\_location\].
-   Referenced service not found in table Business Service \[cmdb\_ci\_service\].
-   Duplicate monitor. A monitor already exists for the endpoint.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td>

Forbidden. The user must have the x\_snc\_sow\_synthetics.synthetics\_editor role to create monitors.

</td></tr><tr><td>

413

</td><td>

Payload too large. Request body exceeds 10MB limit.

</td></tr><tr><td>

415

</td><td>

Unsupported media type. The payload must be formatted as JSON or CSV.

</td></tr><tr><td>

429

</td><td>

Too many requests or too many active monitor creation jobs. Wait and retry. Check **error.code** and **error.message** in the response body for more information.Rate limits:

-   10 requests per minute
-   100 requests per hour
-   1000 requests per day

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Object returned if the API request failed.Data type: Object

```
"error": {
   "code": "String",
   "details": {Object},
   "message": "String"
}
```

</td></tr><tr><td>

error.code

</td><td>

Error code. Possible values:

-   INVALID\_JSON\_FORMAT
-   INVALID\_CSV\_FORMAT
-   MISSING\_REQUIRED\_FIELD
-   INVALID\_FIELD\_VALUE
-   CMDB\_CI\_NOT\_FOUND
-   LOCATION\_NOT\_FOUND
-   SERVICE\_NOT\_FOUND
-   DUPLICATE\_MONITOR
-   PAYLOAD\_TOO\_LARGE
-   UNSUPPORTED\_MEDIA\_TYPE
-   RATE\_LIMIT\_EXCEEDED
-   CONCURRENT\_JOB\_LIMIT
-   AUTHENTICATION\_FAILED
-   AUTHORIZATION\_FAILED
-   JOB\_NOT\_FOUND
-   INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

error.details

</td><td>

Additional details about the error. The elements included in this object vary based on the type of error.

Data type: Object

</td></tr><tr><td>

error.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

result

</td><td>

Object containing information about the monitor creation job.Data type: Object

```
"result": {
   "job_id": "String",
   "job_sys_id": "String",
   "message": "String",
   "status": "String",
   "status_check_url": "String"
}
```

</td></tr><tr><td>

result.job\_id

</td><td>

ID of the monitor creation job.Table: Synthetics Bulk Job \[sn\_sow\_synthetics\_bulk\_job\]

Column: Job ID

Data type: String

</td></tr><tr><td>

result.job\_sys\_id

</td><td>

Sys\_id of the monitor creation job.Table: Synthetics Bulk Job \[sn\_sow\_synthetics\_bulk\_job\]

Data type: String

</td></tr><tr><td>

result.message

</td><td>

Message about the status of the monitor creation job.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the monitor creation job.For a successful API request \(status code `202 Accepted`\), the value of this parameter is `pending`.

Data type: String

</td></tr><tr><td>

result.status\_check\_url

</td><td>

Endpoint for tracking the current status of the monitor creation job. For more information, see [GET /sn\_sow\_synthetics/v1/synthetics\_async\_bulk\_create/\{job\_id\}](synth-async-api.md#).Data type: String

</td></tr></tbody>
</table>### cURL request

This example submits a job to create monitors for two API endpoints.

```
curl "https://instance.service-now.com/api/sn_sow_synthetics/v1/synthetics_async_bulk_create" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "checks": [
    {
      "name": "Production API Health Check",
      "method": "GET",
      "description": "Monitors the main API health endpoint",
      "interval": 5,
      "cmdb_ci": "21d4073087807610f13cbbf7cebb3500",
      "enabled": true,
      "should_create_alert": true,
      "alert_severity": 1,
      "locations": [
        "0fd0279b87003210f13cbbf7cebb3552",
        "2244a48d87cc7610f13cbbf7cebb3554"
      ],
      "headers": [
        {
          "name": "Accept",
          "value": "application/json"
        }
      ],
      "query_string": null,
      "credential": "",
      "body": null,
      "parent_service_sys_id": "6731133c87c07610f13cbbf7cebb35d8",
      "support_group_sys_id": "019ad92ec7230010393d265c95c260dd",
      "alert_tags": {
        "environment": "production",
        "team": "platform"
      },
      "valid_http_code_type": "equals",
      "valid_http_code": "200",
      "max_latency_ms": 5000,
      "body_condition": {
        "type": "jsonpath",
        "expression": "$.status == 'ok'"
      }
    },
    {
      "name": "User Service POST Test",
      "method": "POST",
      "description": "Tests user creation endpoint",
      "interval": 10,
      "cmdb_ci": "21d4073087807610f13cbbf7cebb3503",
      "enabled": true,
      "should_create_alert": true,
      "alert_severity": 2,
      "locations": [
        "2244a48d87cc7610f13cbbf7cebb3554"
      ],
      "headers": [
        {
          "name": "Content-Type",
          "value": "application/json"
        }
      ],
      "body": "{\"test\": true}",
      "parent_service_sys_id": "6731133c87c07610f13cbbf7cebb35e1",
      "support_group_sys_id": "0762d92db72422103a858bbb4e11a928",
      "valid_http_code_type": "in_range",
      "valid_http_code": "200-201",
      "max_latency_ms": 3000
    }
  ]
}" \
--user 'username':'password'
```

Response body - job successfully created.

```
{
  "result": {
    "job_id": "BCJ-1706789123456-a1b2c3d4",
    "job_sys_id": "abc123def456abc123def456",
    "status": "pending",
    "message": "Job created successfully. File uploaded. Processing will begin shortly.",
    "status_check_url": "/api/sn_sow_synthetics/v1/synthetics_async_bulk_create/BCJ-1706789123456-a1b2c3d4"
  }
}
```

Response body - concurrent monitor creation job limit error.

```
{
  "error": {
    "code": "CONCURRENT_JOB_LIMIT",
    "message": "Maximum concurrent jobs exceeded. Please wait for existing jobs to complete."
  }
}
```

Response body - rate limit error.

```
{
  "error": {
    "code": "RATE_LIMIT_EXCEEDED",
    "message": "Rate limit exceeded. Please try again later.",
    "details": {
      "remaining_per_minute": 0,
      "remaining_per_hour": 5,
      "remaining_per_day": 100
    }
  }
}
```

