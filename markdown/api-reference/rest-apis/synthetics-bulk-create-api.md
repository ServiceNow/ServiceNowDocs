---
title: SyntheticsBulkCreate API
description: The SyntheticsBulkCreate API provides an endpoint to create multiple synthetic monitors in a single synchronous operation.Creates multiple synthetic monitors in a single synchronous operation.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 11
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# SyntheticsBulkCreate API

The SyntheticsBulkCreate API provides an endpoint to create multiple synthetic monitors in a single synchronous operation.

Use Cases:

-   Post-Incident Monitoring - After resolving an incident, create monitors for discovered endpoints to prevent recurrence.
-   Service Onboarding - Quickly establish baseline monitoring for new services or applications.
-   Gap Closure - Create monitors for unmonitored critical endpoints identified through discovery.
-   Automated Workflows - Integrate with incident management or discovery workflows to automate monitor provisioning.

Use this API to create up to 50 monitors per request. To create more than 50 monitors per request, use the [SyntheticsAsyncBulkCreate](synth-async-api.md#) API.

This API requires the [Synthetic monitoring](https://www.servicenow.com/docs/access?context=synthetic-monitoring-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) application \(com.snc.uib.sow\_synthetics\), which is available on the ServiceNow Store. The calling user must have the x\_snc\_sow\_synthetics.synthetics\_editor role. Before calling this API, at least one MID Server location must be configured for synthetic monitoring. For instructions, see [Create synthetic monitoring locations](https://www.servicenow.com/docs/access?context=create-synthetic-monitoring-locations&version=australia&pubname=australia-it-operations-management&ft:locale=en-US). Additionally, configuration items \(CIs\) for the endpoints being monitored must exist in the [Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=c_ITILConfigurationManagement&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## SyntheticsBulkCreate - POST /sn\_sow\_synthetics/synthetics\_bulk\_create

Creates multiple synthetic monitors in a single synchronous operation.

Use this endpoint for incident-driven workflows and smaller batch operations where immediate validation and results are required. This endpoint supports creating up to 50 monitors per request, with a maximum payload size of 10MB.

This endpoint links monitors to incidents for post-incident observability and provides automatic MID Server location selection. Endpoints are evaluated through a six-phase process: exact URL match, same-host endpoints, same-subnet endpoints, same-region endpoints, any available location, and fallback to default. This ensures optimal monitoring coverage without requiring manual location assignment.

### URL format

Versioned URL: `/api/sn_sow_synthetics/{api_version}/synthetics_bulk_create`

Default URL: `/api/sn_sow_synthetics/synthetics_bulk_create`

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

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

correlation\_id

</td><td>

Required. Correlation identifier for tracking and telemetry that links all monitors created in the same request. You can use [gs.generateGUID\(\)](../../../app-store/dev_portal/API_reference/glideSystemScoped/concept/c_GlideSystemScopedAPI.md#) to generate the id.

Maximum length: 200 characters

Data type: String

</td></tr><tr><td>

endpoints

</td><td>

Required. Array of endpoint configuration objects to create monitors for. This array can contain a maximum of 50 objects per API request.Data type: Array

```
"endpoints": [
   {
      "body": "String",
      "enabled": Boolean,
      "endpoint_id": "String",
      "headers": [Array],
      "interval": Number,
      "max_latency_ms": Number,
      "method": "String",
      "name": "String",
      "parent_service_sys_id": "String",
      "support_group_sys_id": "String",
      "url": "String",
      "valid_http_code": "String"
   }
]
```

</td></tr><tr><td>

endpoints.body

</td><td>

Request body for POST, PUT, or PATCH endpoints. Must be a valid JSON or XML string depending on the `Content-Type` header. Maximum size is 10KB.Data type: String

</td></tr><tr><td>

endpoints.enabled

</td><td>

Flag that indicates whether the monitor will start executing immediately after creation.Valid values:

-   true: The monitor starts executing immediately after creation.
-   false: The monitor won't start executing until it is enabled.

Default: true

Data type: Boolean

</td></tr><tr><td>

endpoints.endpoint\_id

</td><td>

Required. Sys\_id of the CMDB endpoint configuration item \(CI\).Table: HTTP Endpoint \[cmdb\_ci\_endpoint\_http\]

Data type: String

</td></tr><tr><td>

endpoints.headers

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

endpoints.headers.name

</td><td>

Name of the HTTP header, such as `Authorization` or `Content-Type`.Data type: String

</td></tr><tr><td>

endpoints.headers.value

</td><td>

Value of the HTTP header, such as `Bearer token` or `application/json`.Data type: String

</td></tr><tr><td>

endpoints.interval

</td><td>

Frequency of monitor execution in minutes.ServiceNow hosted locations are limited to 6 tests per minute per monitor.

Valid values: 1-60

Default: 5 \(executes once every five minutes\)

Data type: Number

</td></tr><tr><td>

endpoints.max\_latency\_ms

</td><td>

Maximum acceptable response time in milliseconds. The general guideline is 500-5000ms depending on the endpoint type. The monitor checks against this value when testing, and the test fails if the response time exceeds this value.

Default: null \(no latency threshold\)

Data type: Number

</td></tr><tr><td>

endpoints.method

</td><td>

HTTP method to use. Valid values \(case-insensitive\):

-   DELETE
-   GET
-   HEAD
-   OPTIONS
-   PATCH
-   POST
-   PUT

Default: GET

Data type: String

</td></tr><tr><td>

endpoints.name

</td><td>

Display name for the monitor. For incident-driven monitor creation, an example format is `[INC{number}] {endpoint_name} - {service_name}`.Maximum length: 100 characters

Default: Monitor name is automatically generated from the endpoint name.

Data type: String

</td></tr><tr><td>

endpoints.parent\_service\_sys\_id

</td><td>

Sys\_id of the business service this endpoint supports. Used for service-level reporting and impact analysis.Table: Business Service \[cmdb\_ci\_service\]

Default: null

Data type: String

</td></tr><tr><td>

endpoints.support\_group\_sys\_id

</td><td>

Sys\_id of the support group responsible for this endpoint. Used for alert routing and assignment.Table: Group \[sys\_user\_group\]

Default: null

Data type: String

</td></tr><tr><td>

endpoints.url

</td><td>

Required. Full HTTP or HTTPS URL to monitor. Must begin with `http://` or `https://`. For example, `https://api.example.com/health`.Maximum length: 2048 characters

Data type: String

</td></tr><tr><td>

endpoints.valid\_http\_code

</td><td>

Expected HTTP status codes for a successful response, provided as a single value or a comma-separated list such as `'200,201,204'`. The monitor checks against these values when testing, and the test fails if the actual status code doesn't match a value in the list.

Default: 200

Data type: String

</td></tr><tr><td>

idempotency\_key

</td><td>

Required. Unique identifier \(key\) to prevent duplicate monitor creation if the same API request is submitted multiple times.Keys are retained in the system for 24 hours.

Format: Any string up to 200 characters, such as the **correlation\_id** or the pattern `INC-{incident_number}-{timestamp}`.

Data type: String

</td></tr><tr><td>

incident\_id

</td><td>

Sys\_id of the incident that triggered monitor creation. Used for tracking and correlation in post-incident analysis.If provided, created monitors are linked to this incident.

Table: Incident \[incident\]

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_anx_lhs_v3c" class="rest_api_request_headers"><thead><tr><th>

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

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|
|Retry-After|Returned with `503` status code. Number of seconds to wait before retrying the request.|
|X-Request-ID|Unique identifier for the API request. Used for troubleshooting and log correlation.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Successful. All or some monitors were created. Check **results** in the response body for individual monitor creation status.

</td></tr><tr><td>

400

</td><td>

Bad request. Request validation failed. Check **error.code** and **error.message** in the response body for error details.Common causes:

-   Invalid JSON request body.
-   Missing required parameters \(**correlation\_id**, **endpoints**, or **idempotency\_key**\).
-   Empty **endpoints** array.
-   More than 50 endpoints included in **endpoints** array.
-   Invalid values in **endpoints** objects \(**endpoint\_id**, **url**, or **method**\).
-   Duplicate **idempotency\_key** \(request already processed\).

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td>

Forbidden. The user must have the x\_snc\_sow\_synthetics.synthetics\_editor role to create monitors.

</td></tr><tr><td>

404

</td><td>

Not found. The API endpoint path is incorrect or the Synthetic Monitoring plugin is not installed or activated.

</td></tr><tr><td>

413

</td><td>

Payload too large. Request body exceeds 10MB limit. Reduce the number of objects in the **endpoints** array or remove large request body content.

</td></tr><tr><td>

429

</td><td>

Too many requests. Rate limit exceeded, wait and retry. Check **error.details.retry\_after\_seconds** in the response body for the number of seconds until the rate limit window resets.User has exceeded one of the following:

-   10 requests per minute
-   100 requests per hour
-   1000 requests per day

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr><tr><td>

503

</td><td>

Service unavailable. Synthetic monitoring service temporarily unavailable due to maintenance or high load. Retry the request after the delay indicated in the `Retry-After` header.

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

-   AUTHENTICATION\_FAILED
-   INSUFFICIENT\_PRIVILEGES
-   INVALID\_REQUEST\_STRUCTURE
-   MISSING\_REQUIRED\_FIELD
-   RATE\_LIMIT\_EXCEEDED
-   TOO\_MANY\_ENDPOINTS

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

message

</td><td>

Message about the result of the API request.Data type: String

</td></tr><tr><td>

results

</td><td>

Array of objects containing the monitor creation result for each endpoint. Endpoint results are listed in the same order provided in the **endpoints** array in the request body.

Data type: Array

```
"results": [
   {
      "endpoint_id": "String",
      "error_code": "String",
      "error_message": "String",
      "location": {Object},
      "monitor_name": "String",
      "monitor_sys_id": "String",
      "status": "String"
   }
]
```

</td></tr><tr><td>

results.endpoint\_id

</td><td>

Sys\_id of the CMDB endpoint configuration item \(CI\).Table: HTTP Endpoint \[cmdb\_ci\_endpoint\_http\]

Data type: String

</td></tr><tr><td>

results.error\_code

</td><td>

Error code if the monitor creation **status** is `failed`.Possible values:

-   DUPLICATE\_MONITOR
-   INVALID\_ENDPOINT\_ID
-   INVALID\_METHOD
-   INVALID\_URL
-   NO\_LOCATION\_AVAILABLE
-   VALIDATION\_ERROR

Data type: String

</td></tr><tr><td>

results.error\_message

</td><td>

Error message if the monitor creation **status** is `failed`.Data type: String

</td></tr><tr><td>

results.location

</td><td>

MID Server location selected for the monitor.Data type: Object

```
"location": {
   "name": "String",
   "selection_phase": Number,
   "sys_id": "String"  
}
```

</td></tr><tr><td>

results.location.name

</td><td>

Name of the MID Server location.Data type: String

</td></tr><tr><td>

results.location.selection\_phase

</td><td>

Phase number used to select the MID Server location.Each endpoint is evaluated against the following phases, beginning with phase `1` and continuing until an applicable phase is found.

Possible values:

-   `1`: Use the MID Server location from an existing monitor for the same endpoint or host.
-   `2`: Use the MID Server location from an existing monitor for the same subnet.
-   `3`: Use the MID Server location from an existing monitor for the same region.
-   `4`: Use the MID Server location from an existing monitor for the same service.
-   `5`: Use the default MID Server location set by the **sn\_sow\_synthetics.default\_mid\_location** system property. If no MID Servers are available at the default location, the first available MID Server location is used instead.
-   `6`: Use ServiceNow hosted execution.

Data type: Number

</td></tr><tr><td>

results.location.sys\_id

</td><td>

Sys\_id of the MID Server location.Table: Synthetic Location \[sn\_sow\_synthetics\_location\]

Data type: String

</td></tr><tr><td>

results.monitor\_name

</td><td>

Display name of the created monitor.Data type: String

</td></tr><tr><td>

results.monitor\_sys\_id

</td><td>

Sys\_id of the created monitor.Table: Check \[sn\_sow\_synthetics\_check\]

Data type: String

</td></tr><tr><td>

results.status

</td><td>

Monitor creation status for the endpoint. Possible values:

-   `created`: Monitor successfully created.
-   `failed`: Monitor creation failed.
-   `skipped`: Duplicate idempotency key. The **idempotency\_key** provided in the request body was already used in a previous API request.

Data type: String

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the API request was successful.Possible value: `true`. All or some monitors were created.

**Note:** This parameter is only included when the response status code is `200` so this value is always `true`.

Data type: Boolean

</td></tr><tr><td>

summary

</td><td>

Object summarizing the result of the API request.Data type: Object

</td></tr><tr><td>

summary.failed

</td><td>

Number of monitors that couldn't be created.Data type: Number

</td></tr><tr><td>

summary.successful

</td><td>

Number of monitors that were successfully created.Data type: Number

</td></tr><tr><td>

summary.total\_requested

</td><td>

Total number of endpoints included in the API request.Data type: Number

</td></tr></tbody>
</table>### cURL request

This example creates monitors for three HTTP endpoints discovered from a resolved incident.

```
curl -X POST 'https://instance.service-now.com/api/sn_sow_synthetics/bulk_create' \ 
-H 'Content-Type: application/json' \ 
-H 'Accept: application/json' \ 
-u 'username:password' \ 
-d '{
  "incident_id": "a1b2c3d4e5f6789012345678",
  "idempotency_key": "INC-INC0012345-20260401T120000",
  "correlation_id": "550e8400-e29b-41d4-a716-446655440000",
  "endpoints": [
    {
      "endpoint_id": "e1f2g3h4i5j6789012345678",
      "name": "[INC0012345] Payment API Health - Payment Gateway",
      "url": "https://api.payment.example.com/health",
      "method": "GET",
      "interval": 2,
      "enabled": true,
      "parent_service_sys_id": "s1t2u3v4w5x6789012345678",
      "support_group_sys_id": "g1h2i3j4k5l6789012345678",
      "valid_http_code": "200",
      "max_latency_ms": 500
    },
    {
      "endpoint_id": "k1l2m3n4o5p6789012345678",
      "name": "[INC0012345] Payment Transaction API - Payment Gateway",
      "url": "https://api.payment.example.com/v2/transactions",
      "method": "POST",
      "interval": 5,
      "enabled": true,
      "parent_service_sys_id": "s1t2u3v4w5x6789012345678",
      "support_group_sys_id": "g1h2i3j4k5l6789012345678",
      "valid_http_code": "200,201",
      "max_latency_ms": 1000,
      "headers": [
        {
          "name": "Authorization",
          "value": "Bearer test-token"
        },
        {
          "name": "Content-Type",
          "value": "application/json"
        }
      ],
      "body": "{\"amount\": 100, \"currency\": \"USD\"}"
    },
    {
      "endpoint_id": "q1r2s3t4u5v6789012345678",
      "name": "[INC0012345] Customer Portal Status - Payment Gateway",
      "url": "https://portal.payment.example.com/status",
      "method": "GET",
      "interval": 10,
      "enabled": true,
      "parent_service_sys_id": "s1t2u3v4w5x6789012345678",
      "valid_http_code": "200"
    }
  ]
}'
```

Response body - all monitors created successfully.

```
{
  "success": true,
  "message": "Bulk creation completed. 3 monitors created successfully, 0 failed validation.",
  "summary": {
    "total_requested": 3,
    "successful": 3,
    "failed": 0
  },
  "results": [
    {
      "endpoint_id": "e1f2g3h4i5j6789012345678",
      "status": "created",
      "monitor_sys_id": "m1n2o3p4q5r6789012345678",
      "monitor_name": "[INC0012345] Payment API Health - Payment Gateway",
      "location": {
        "sys_id": "l1m2n3o4p5q6789012345678",
        "name": "US-East-1 MID Server",
        "selection_phase": 2
      },
      "error_message": null,
      "error_code": null
    },
    {
      "endpoint_id": "k1l2m3n4o5p6789012345678",
      "status": "created",
      "monitor_sys_id": "r1s2t3u4v5w6789012345678",
      "monitor_name": "[INC0012345] Payment Transaction API - Payment Gateway",
      "location": {
        "sys_id": "l1m2n3o4p5q6789012345678",
        "name": "US-East-1 MID Server",
        "selection_phase": 2
      },
      "error_message": null,
      "error_code": null
    },
    {
      "endpoint_id": "q1r2s3t4u5v6789012345678",
      "status": "created",
      "monitor_sys_id": "x1y2z3a4b5c6789012345678",
      "monitor_name": "[INC0012345] Customer Portal Status - Payment Gateway",
      "location": {
        "sys_id": "l1m2n3o4p5q6789012345678",
        "name": "US-East-1 MID Server",
        "selection_phase": 2
      },
      "error_message": null,
      "error_code": null
    }
  ]
}
```

Response body - partial success.

```
{
  "success": true,
  "message": "Bulk creation completed. 2 monitors created successfully, 1 failed validation.",
  "summary": {
    "total_requested": 3,
    "successful": 2,
    "failed": 1
  },
  "results": [
    {
      "endpoint_id": "e1f2g3h4i5j6789012345678",
      "status": "created",
      "monitor_sys_id": "m1n2o3p4q5r6789012345678",
      "monitor_name": "[INC0012345] Payment API Health - Payment Gateway",
      "location": {
        "sys_id": "l1m2n3o4p5q6789012345678",
        "name": "US-East-1 MID Server",
        "selection_phase": 2
      },
      "error_message": null,
      "error_code": null
    },
    {
      "endpoint_id": "invalid-endpoint-id",
      "status": "failed",
      "monitor_sys_id": null,
      "monitor_name": null,
      "location": null,
      "error_message": "Invalid endpoint_id: No endpoint found with sys_id 'invalid-endpoint-id' in cmdb_ci_endpoint_http table.",
      "error_code": "INVALID_ENDPOINT_ID"
    },
    {
      "endpoint_id": "q1r2s3t4u5v6789012345678",
      "status": "created",
      "monitor_sys_id": "x1y2z3a4b5c6789012345678",
      "monitor_name": "[INC0012345] Customer Portal Status - Payment Gateway",
      "location": {
        "sys_id": "w1x2y3z4a5b6789012345678",
        "name": "EU-West-1 MID Server",
        "selection_phase": 4
      },
      "error_message": null,
      "error_code": null
    }
  ]
}
```

Response body - rate limit error.

```
{
  "error": {
    "code": "RATE_LIMIT_EXCEEDED",
    "message": "Rate limit exceeded. You have made 11 requests in the last minute. Limit is 10 requests per minute.",
    "details": {
      "limit": 10,
      "window": "per_minute",
      "retry_after_seconds": 45
    }
  }
}
```

