---
title: SyntheticsBulkCreate API
description: The SyntheticsBulkCreate API provides an endpoint to create multiple synthetic monitors in a single synchronous operation.Creates multiple synthetic monitors in a single synchronous operation.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# SyntheticsBulkCreate API

The SyntheticsBulkCreate API provides an endpoint to create multiple synthetic monitors in a single synchronous operation.

Use Cases:

-   Post-Incident Monitoring - After resolving an incident, create monitors for discovered endpoints to prevent recurrence.
-   Service Onboarding - Quickly establish baseline monitoring for new services or applications.
-   Gap Closure - Create monitors for unmonitored critical endpoints identified through discovery.
-   Automated Workflows - Integrate with incident management or discovery workflows to automate monitor provisioning.

This API requires the [Synthetic monitoring](https://www.servicenow.com/docs/access?context=synthetic-monitoring-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) plugin \(com.snc.uib.sow\_synthetics\) and the calling user must have the x\_snc\_sow\_synthetics.synthetics\_editor role. Before calling this API, at least one MID Server location must be configured for synthetic monitoring. For instructions, see [Create synthetic monitoring locations](https://www.servicenow.com/docs/access?context=create-synthetic-monitoring-locations&version=australia&pubname=australia-it-operations-management&ft:locale=en-US). Additionally, configuration items \(CIs\) for the endpoints being monitored should exist in the [Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=c_ITILConfigurationManagement&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## SyntheticsBulkCreate - POST /sn\_sow\_synthetics/synthetics\_bulk\_create

Creates multiple synthetic monitors in a single synchronous operation.

Use this endpoint for incident-driven workflows and smaller batch operations where immediate validation and results are required. This endpoint supports creating up to 50 monitors per request. To create more than 50 monitors per request, use the SyntheticsAsyncBulkCreate API.

This endpoint links monitors to incidents for post-incident observability and provides automatic MID server location selection. Endpoints are evaluated through a 6-phase process: exact URL match, same-host endpoints, same-subnet endpoints, same-region endpoints, any available location, and fallback to default. This ensures optimal monitoring coverage without requiring manual location assignment.

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

incident\_id

</td><td>

Sys\_id of the incident that triggered monitor creation. Used for tracking and correlation in post-incident analysis.If provided, created monitors are linked to this incident.

Table: Incident \[incident\]

Data type: String

</td></tr><tr><td>

idempotency\_key

</td><td>

Required. Unique identifier \(key\) to prevent duplicate monitor creation if the same API request is submitted multiple times.Keys are retained in the system for 24 hours.

Format: Any string up to 200 characters, such as the **correlation\_id** or the pattern `INC-{incident_number}-{timestamp}`.

Data type: String

</td></tr><tr><td>

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
      "endpoint_id": "String",
      "name": "String",
      "url": "https://api.payment.example.com/v2/transactions",
      "method": "POST",
      "interval": 5,
      "enabled": true,
      "parent_service_sys_id": "s1t2u3v4w5x6789012345678",
      "support_group_sys_id": "g1h2i3j4k5l6789012345678",
      "valid_http_code": "200,201",
      "max_latency_ms": 1000,
      "headers": [Array],
      "body": "String"
    }
]
```

</td></tr><tr><td>

endpoints.endpoint\_id

</td><td>

Required. Sys\_id of the CMDB endpoint configuration item \(CI\).Table: HTTP Endpoint \[cmdb\_ci\_endpoint\_http\]

Data type: String

</td></tr><tr><td>

endpoints.name

</td><td>

Display name for the monitor. For incident-driven monitor creation, an example format is `[INC{number}] {endpoint_name} - {service_name}`.Maximum length: 100 characters

Default: Monitor name is automatically generated from the endpoint name.

Data type: String

</td></tr><tr><td>

endpoints.url

</td><td>

Required. Full HTTP or HTTPS URL to monitor. Must begin with `http://` or `https://`. For example, `https://api.example.com/health`.Maximum length: 2048 characters

Data type: String

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

endpoints.interval

</td><td>

Frequency of monitor execution in minutes.ServiceNow-hosted locations are limited to 6 tests per minute per monitor.

Valid values: 1-60

Default: 5 \(executes once every five minutes\)

Data type: Number

</td></tr><tr><td>

endpoints.enabled

</td><td>

Flag that indicates whether the monitor will start executing immediately after creation.Valid values:

-   true: The monitor starts executing immediately after creation.
-   false: The monitor won't start executing until it is enabled.

Default: true

Data type: Boolean

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

endpoints.valid\_http\_code

</td><td>

Expected HTTP status codes for a successful response, provided as a single value or a comma-separated list such as `'200,201,204'`. The monitor checks against these values when testing, and the test fails if the actual status code doesn't match a value in the list.

Default: 200

Data type: String

</td></tr><tr><td>

endpoints.max\_latency\_ms

</td><td>

Maximum acceptable response time in milliseconds. The general guideline is 500-5000ms depending on the endpoint type. The monitor checks against this value when testing, and the test fails if the response time exceeds this value.

Default: null \(no latency threshold\)

Data type: Number

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

endpoints.body

</td><td>

Request body for POST, PUT, or PATCH endpoints. Must be a valid JSON or XML string depending on the `Content-Type` header. Maximum size is 10KB.Data type: String

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
|X-Request-ID|Unique identifier for the API request. Used for troubleshooting and log correlation.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

```

```

```

```

### Python request

```

```

```

```

