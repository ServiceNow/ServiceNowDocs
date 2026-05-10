---
title: Cloud Runner Test Runner REST API
description: Manages tests to be executed in a cloud runner for Automated Test Framework \(ATF\).Provides the status of each test ran for a provided Browser Orchestration Queue \(BOQ\) record.Sets the test runner job to complete status and cancels the root trackers of any generated tests that are running.Inserts a test runner job into the BOQ \[sn\_atf\_tg\_sn\_boq\] table for given test or test suite, which is then run on the cloud runner.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Cloud Runner Test Runner REST API

Manages tests to be executed in a cloud runner for Automated Test Framework \(ATF\).

The Cloud Runner Test Runner API requires the [ATF Test Generator and Cloud Runner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/atf-test-generator-and-cloud-runner/atf-tg-cr-intro.md) \(sn\_atf\_tg\) plugin. The methods available with this API run in the **now** namespace and can be called using API Name, **One-click regression testing for ATF**, in the REST API Explorer. The admin role is required to access this API.

You can use this API for the following tasks:

-   Start an ATF test or test suite in the Cloud Runner browser.
-   Check the progress of the test job.
-   Cancel the test job.

The Cloud Runner Test Runner API may be used in tandem with the [Cloud Runner Test Generation REST API](cloudrunner-testgeneration-api.md#) and [Cloud Runner Test User REST API](cloudrunner-testuser-api.md#). For instance, you can generate a test \(Cloud Runner Test Generation API\) and then get the progress of the test in the browser orchestration queue \(Cloud Runner TEST Generation API\) and check the number of tests that passed or failed.

To view the Server API reference documentation of this API, see [Cloud Runner TestRunnerApi – Scoped, Global](../../../app-store/dev_portal/API_reference/CloudRunnerAPI-TestRunnerAPIScoped/concept/cloudrnr-TestRunnerAPI-scoped.md#).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Cloud Runner Test Runner - GET /now/sn\_atf\_tg/test\_runner\_progress

Provides the status of each test ran for a provided Browser Orchestration Queue \(BOQ\) record.

### URL format

Default URL: GET `/api/now/sn_atf_tg/test_runner_progress`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

snboqId

</td><td>

Required. The BOQ record sys\_id of the test runner job to get the progress of.Data type: String

Table: BOQ \[sn\_atf\_tg\_sn\_boq\]

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

<table id="table_vdy_gwz_31c"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Successfully retrieved the progress of the BOQ job.

</td></tr><tr><td>

400

</td><td>

Error getting BOQ record status. Returns one of the following messages:-   No BOQ ID passed in – No BOQ ID was provided. Add the BOQ ID to the request body.
-   Unable to find BOQ record – Invalid Sys ID. Verify that the sys\_id of the BOQ record is valid and the record exists.

</td></tr><tr><td>

403

</td><td>

Error granting user access to the endpoint. Ensure that the user has the admin role.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the progress results of the test runner job or a message explaining why the request failed.Data type: Object

```
"result": { 
    "progress": 100, 
    "state": "completed" 
  }
```

Or:

```
{
  "result": { 
    "message": "String" 
  } 
}
```

</td></tr><tr><td>

result.message

</td><td>

Error message detailing why the test runner progress cannot be retrieved. The message parameter is not returned in a successful response.Data type: String

</td></tr><tr><td>

result.progress

</td><td>

Percentage that indicates how close to completion a test is while in a running state.Data type: Number

</td></tr><tr><td>

result.state

</td><td>

Current status of the BOQ record. Possible values:

-   Browsers requested: A request has been sent to the cloud infrastructure to start browsers for test generation or test running.
-   Completed: The test task is complete.
-   Failed state: The test task failed.
-   Pending: The requested test activity has been created and waiting to be executed.
-   Processing: The instance is scanning for records to ensure that the execution trackers are marked for cloud runner before the request is sent to the cloud infrastructure.
-   Running: The cloud infrastructure browsers find and execute pending tests.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following request retrieves the test runner job progress of the BOQ record.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/test_runner_progress?snboqId=<sys_id of SNBOQ record>" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user "username:password"
```

The response indicates that the test is 100% complete.

```
{ 
  "result": { 
    "progress": 100, 
    "state": "completed" 
  } 
}
```

The following example returns a 400 error message when no BOQ ID is passed.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/test_runner_progress" \
--request GET \
--header "Accept:application/json" \
--user "username:password"
```

Response:

```
{
  "result": {
    "message": "No SNBOQ ID passed in, add snboqId to request body"
  }
}
```

The following example returns a 400 error message when an invalid BOQ ID is passed.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/test_runner_progress?snboqId=invalid_sys_id" \
--request GET \
--header "Accept:application/json" \
--user "username:password"
```

Response:

```
{
  "result": {
    "message": "Invalid SNBOQ sys_id passed in"
  }
}
```

## Cloud Runner Test Runner - POST /now/sn\_atf\_tg/cancel\_test\_runner

Sets the test runner job to complete status and cancels the root trackers of any generated tests that are running.

### URL format

Default URL: GET `/now/sn_atf_tg/cancel_test_runner`

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

snboqId

</td><td>

Sys\_id of the Browser Orchestration Queue \(BOQ\) record \(sn\_atf\_tg\_sn\_boq\) associated with the test runner job to cancel.Data type: String

Table: BOQ \[sn\_atf\_tg\_sn\_boq\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_ism_z2j_41c" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Error canceling job. Returns one of the following messages:-   No BOQ ID passed in – No BOQ ID was provided. Add the BOQ ID to the request body.
-   Unable to find BOQ record – Invalid Sys ID. Verify that the sys\_id of the BOQ record is valid and the record exists.

</td></tr><tr><td>

403

</td><td>

Error granting user access to the endpoint. Ensure that the user has the admin role.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the results of the request.```

  "result": { 
    "message": String
  }
```

Data type: Object

</td></tr><tr><td>

result.message

</td><td>

Message detailing whether the test cancellation was successful.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to form a cancel test runner request according to the sys\_id of the BOQ record.

```
curl "https://instance.service-now.com/api/now/sn_atf_tg/cancel_test_runner" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"snboqId\":\"<sys_id of BOQ record>\"}" \ 
--user "username:password"
```

The response message indicating that the test runner is successfully canceled.

```
{ 
  "result": { 
    "message": "success" 
  } 
} 
```

## Cloud Runner Test Runner - POST /now/sn\_atf\_tg/test\_runner

Inserts a test runner job into the BOQ \[sn\_atf\_tg\_sn\_boq\] table for given test or test suite, which is then run on the cloud runner.

### URL format

Default URL: POST `api/now/sn_atf_tg/test_runner`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|testId|Sys\_id of the test \[sys\_atf\_test\] or test suite \[sys\_atf\_test\_suite\] to run on the cloud runner.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_gcx_1fj_41c" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Successfully inserted a test runner BOQ job.

</td></tr><tr><td>

400

</td><td>

Error starting the test runner job. Returns one of the following messages:-   Unable to find test or test suite with Sys ID &lt;testId&gt; – Invalid test ID. Ensure that the sys\_id of the test \(sys\_atf\_test\) or test suite \(sys\_atf\_test\_suite\) record is valid and the record exists.
-   No Test ID passed in – No test ID was passed. Add the test ID to the request body.

</td></tr><tr><td>

403

</td><td>

Error granting user access to the endpoint. Ensure that the user has the admin role.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the results of the request.Data type: Object

```
{ 
  "result": { 
    "snboqId": "String" 
  } 
}
```

Or:

```

  "result": { 
    "message": "String"
  }
```

</td></tr><tr><td>

result.snboqId

</td><td>

Sys\_id of the BOQ record that is inserted when test runner starts.Data type: String

Table: BOQ \[sn\_atf\_tg\_sn\_boq\]

</td></tr><tr><td>

result.message

</td><td>

Error message detailing why the test runner cannot be started.Data type: String

</td></tr></tbody>
</table>### cURL request

The following request inserts a test runner job into the BOQ \[sn\_atf\_tg\_sn\_boq\] table.

```
curl "https://instance.service-now.com/api/now/sn_atf_tg/test_runner" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"testId\":\"<sys_id of ATF test or test suite>\"}" \ 
--user "username:password"
```

The response body returns the sys\_id of the test runner job that was successfully inserted.

```
{ 
  "result": { 
    "snboqId": "<sys_id of newly inserted SNBOQ record>" 
  } 
}
```

