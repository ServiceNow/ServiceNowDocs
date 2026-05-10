---
title: Copy Assessments API
description: The Copy Assessments API provides an endpoint to create a copy of an assessment metric type or survey definition in the Assessment Metric Type \[asmt\_metric\_type\] table.Creates a copy of an assessment metric type or survey definition in the Assessment Metric Type \[asmt\_metric\_type\] table.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-19"
reading_time_minutes: 2
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Copy Assessments API

The Copy Assessments API provides an endpoint to create a copy of an assessment metric type or survey definition in the Assessment Metric Type \[asmt\_metric\_type\] table.

This API is included in the [Assessments and Surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/assessments-surveys-landing-page.md) application, which is available by default.

The calling user must have the assessment\_admin role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Copy Assessments - POST /now/copy\_assessments/copy

Creates a copy of an assessment metric type or survey definition in the Assessment Metric Type \[asmt\_metric\_type\] table.

All associated questions \(type\), configurations, categories, metrics, domain separation rules, and role-based categories are copied. Assigned users, category users, instances, and trigger conditions are not copied.

### URL format

Default URL: `/api/now/copy_assessments/copy`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysID

</td><td>

Required. Sys\_id of the assessment metric type or survey definition to copy.Table: Assessment Metric Type \[asmt\_metric\_type\]

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json;charset=UTF-8**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request.Data type: Object

```
"result": {
   "name": "String",
   "sysID": "String"
}
```

</td></tr><tr><td>

result.name

</td><td>

Name of the copy of the assessment metric type or survey definition. Copies are named using the format `Copy of <original name>`.Data type: String

</td></tr><tr><td>

result.sysID

</td><td>

Sys\_id of the copy of the assessment metric type or survey definition.Table: Assessment Metric Type \[asmt\_metric\_type\]

Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a copy of an assessment metric type.

```
curl "https://instance.service-now.com/api/now/copy_assessments/copy" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"sysID\":\"d2fbde248f033300e7e16c7827bdee11\"}" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "sysID": "19d54d2447f336d027d48b41516d43ee",
    "name": "Copy of Assessment: Basic flow"
  }
}
```

