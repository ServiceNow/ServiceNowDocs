---
title: Cloud Runner Test Generation REST API
description: Manages test job generation to be executed in a cloud runner for Automated Test Framework \(ATF\).Provides the status of each generated test for a provided Browser Orchestration Queue \(BOQ\) record.Sets the test generation job and its associated update set record to complete status. Cancels the root trackers of any generated tests that are running. If any test jobs are in progress on cancellation, this method sets any of the in-progress test records generated to skipped.Inserts a record into the Browser Orchestration Queue \(BOQ\) \[sn\_atf\_tg\_sn\_boq\] table to start a test job.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Cloud Runner Test Generation REST API

Manages test job generation to be executed in a cloud runner for Automated Test Framework \(ATF\).

The Cloud Runner Test Generation API requires the ATF Test Generator and Cloud Runner \(sn\_atf\_tg\) plugin. The methods available with this API run in the **now** namespace and can be called using API Name, **One-click regression testing for ATF**, in the REST API Explorer. The admin role is required to access this API.

You can use this API for the following tasks:

-   Start the test generation job.
-   Check the progress of the test generation job.
-   Cancel the test generation job.

The Cloud Runner Test Generation API may be used in tandem with the [Cloud Runner Test Runner REST API](cloudrunner-testrunner-api.md#) and [Cloud Runner Test User REST API](cloudrunner-testuser-api.md#). For instance, you can call the Test Generation API to run a test and then get the progress of the test in the browser orchestration queue \(Cloud Runner TEST Generation API\) and then check the number of tests that passed or failed.

To view the Server API reference documentation of this API, see [Cloud Runner TestGenerationApi – Scoped, Global](../../../app-store/dev_portal/API_reference/CloudRunnerAPI-TestGenerationAPIScoped/concept/cloudrnr-TestGenerationAPI-scoped.md#).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Cloud Runner Test Generation - GET /now/sn\_atf\_tg/test\_generation\_progress

Provides the status of each generated test for a provided Browser Orchestration Queue \(BOQ\) record.

### URL format

Default URL: GET `/api/now/sn_atf_tg/test_generation_progress`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_pdy_gwz_31c" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

snboqId

</td><td>

Required. The BOQ record sys\_id of the test generation job to get the progress of.Data type: String

Table: BOQ \[sn\_atf\_tg\_sn\_boq\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_sdy_gwz_31c" class="rest_api_request_headers"><thead><tr><th>

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

<table id="table_xdy_gwz_31c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the progress results of the generated test job or a message explaining why the request failed.Data type: Object

```
"result": { 
    "testsSucceeded": Number, 
    "testsFailed": Number, 
    "testsPending": Number, 
    "testsInProgress": Number, 
    "testsSkipped": Number 
  } 
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

Error message detailing why the test generation progress cannot be retrieved. The message parameter is not returned in a successful response.Data type: String

</td></tr><tr><td>

result.testsSucceeded

</td><td>

Number of generated tests that passed.Data type: Number

</td></tr><tr><td>

result.testsFailed

</td><td>

Number of generated tests that failed.Data type: Number

</td></tr><tr><td>

result.testsPending

</td><td>

Number of use cases that are waiting for generated tests.Data type: Number

</td></tr><tr><td>

result.testsInProgress

</td><td>

Number of use cases that tests are created for.Data type: Number

</td></tr><tr><td>

result.testsSkipped

</td><td>

Number of tests skipped due to the job cancellation.Data type: Number

</td></tr></tbody>
</table>### cURL request

The following GET call returns progress information about generated tests associated with the snboqId 1234.

```
curl "https://instance.service-now.com/api/now/sn_atf_tg/test_generation_progress?snboqId=1234" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user "username":"password"
```

Output:

```
{ 
  "result": { 
    "testsSucceeded": 0, 
    "testsFailed": 0, 
    "testsPending": 0, 
    "testsInProgress": 0, 
    "testsSkipped": 161 
  } 
}
```

The following example returns a 400 error message when no BOQ ID is passed.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/test_generation_progress" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
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
curl "http://instance.service-now.com/api/now/sn_atf_tg/test_generation_progress?snboqId=invalid_sys_id" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Response:

```
{
  "result": {
    "message": "Invalid SNBOQ sys_id passed in"
  }
}
```

## Cloud Runner Test Generation - POST /now/sn\_atf\_tg/cancel\_test\_generation

Sets the test generation job and its associated update set record to complete status. Cancels the root trackers of any generated tests that are running. If any test jobs are in progress on cancellation, this method sets any of the in-progress test records generated to skipped.

Tests can fail or cancel automatically due to business rules or access control rule \(ACL\) issues. View the generated test table for more details about failed or canceled tests.

### URL format

Default URL: POST `/api/now/sn_atf_tg/cancel_test_generation`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="table_o1y_cwz_31c" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

snboqId

</td><td>

Required. Sys\_id of the Browser Orchestration Queue \(BOQ\) record to cancel.Data type: String

Table: BOQ \[sn\_atf\_tg\_sn\_boq\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

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

Successfully canceled the BOQ job.

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

Object containing the results of the cancellation request.Data type: Object

```
"result": { 
    "message": "String"
}
```

</td></tr><tr><td>

result.message

</td><td>

Message detailing whether the test cancellation was successful.Data type: String

</td></tr></tbody>
</table>### cURL request

The following request cancels the test generation job of a specified BOQ record.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/cancel_test_generation" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"snboqId\":\"<sys_id of BOQ record>\"}" \ 
--user "username":"password"
```

The response body returns a success message of the cancellation.

```
{ 
  "result": { 
    "message": "success" 
  } 
}
```

The following example returns a 400 error message when no BOQ ID is passed.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/cancel_test_generation" \
--request POST \
--header "Accept:application/json" \
--user "username":"password"
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
curl "http://instance.service-now.com/api/now/sn_atf_tg/cancel_test_generation" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"snboqId\":\"invalid_sys_id\"}" \
--user "username":"password"
```

Response:

```
{
  "result": {
    "message": "No SNBOQ ID passed in, add snboqId to request body"
  }
}
```

## Cloud Runner Test Generation - POST /now/sn\_atf\_tg/test\_generation

Inserts a record into the Browser Orchestration Queue \(BOQ\) \[sn\_atf\_tg\_sn\_boq\] table to start a test job.

### URL format

Default URL: POST `/api/now/sn_atf_tg/test_generation`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="table_o1y_cwz_31c" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalogEncodedQuery

</td><td>

Encoded query specifying which catalog items to generate tests on. An empty string defaults to all catalog items. For more information about forming encoded queries, see Encoded query strings.Data type: String

</td></tr><tr><td>

email

</td><td>

Email address to alert when test generation is complete.Data type: String

</td></tr><tr><td>

maxTestCount

</td><td>

Number of overall tests to generate.Accepted values: Any number between 1 and 9999.

Data type: Number

Default: 9999

</td></tr><tr><td>

maxTestCountPerItem

</td><td>

Number of tests to generate per catalog item. Accepted values: Any number between 1 and 10.

Data type: Number

Default: 10

</td></tr><tr><td>

maxTestCountPerTable

</td><td>

Number of tests to generate per table. Accepted values: Any number between 1 and 10.

Data type: Number

Default: 10

</td></tr><tr><td>

scopeForGeneratingTests

</td><td>

Required when **separateUpdateSetPerScope** is set to false. Sys\_id of the scope in which to place all generated tests. Data type: String

</td></tr><tr><td>

separateUpdateSetPerScope

</td><td>

Flag that indicates whether to separate generated tests into respective suites, update sets, and scopes, or to place tests into one suite, update set, and scope.Valid values:

-   true: Tests are placed into their respective suite and update set according to the scope of each table or catalog item.
-   false: All generated tests are placed in the same suite, update set, and scope. If false, **scopeForGeneratingTests** is required in the request.

Data type: Boolean

Default: true

</td></tr><tr><td>

testSuite

</td><td>

Optional. Sets the name of the test suite to create via test generation.Data type: String

Default: ATF Generated Suite - &lt;time\_stamp&gt;

</td></tr><tr><td>

tableEncodedQuery

</td><td>

Encoded query specifying the tables on which to generate tests. An empty string defaults to all tables. For more information about forming encoded queries, see Encoded query strings.Data type: String

</td></tr><tr><td>

userEncodedQuery

</td><td>

Encoded query specifying which users to generate tests on. An empty string input defaults to all tables. For more information about forming encoded queries, see Encoded query strings.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_krf_y2j_41c" class="rest_api_request_headers"><thead><tr><th>

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

|Status code|Description|
|-----------|-----------|
|200|Successfully inserted a test generation BOQ job. Any errors are shown in the BOQ record logs during processing. All inputs default to generate the maximum number of tests for all tables and service catalog items.|
|403|Error granting user access to the endpoint. Ensure that the user has the admin role.|

### Response body parameters \(JSON or XML\)

<table id="table_v1y_cwz_31c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the results of the request.```

  "result": { 
    "snboqId": String
  }
```

Data type: Object

</td></tr><tr><td>

result.snboqId

</td><td>

Sys\_id of the record inserted in the sn\_atf\_tg\_sn\_boq table when the test generation starts.Data type: String

</td></tr></tbody>
</table>### cURL request

The following request example starts a new test job in the instance without any request parameters and inserts the job in the BOQ table.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/test_generation" \ 
--request POST \ 
--header "Accept:application/json" \ 
--user "username":"password"
```

Response body:

```
{ 
  "result": { 
    "snboqId": <sys_id of newly inserted BOQ record> 
  } 
}
```

The following request example starts a new test job with a maximum test count of 2 and filters the tests to the Incident table, and then inserts the job in the BOQ table.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/test_generation" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"maxTestCount\":\"2\",\"tableEncodedQuery\":\"name=incident\",\"testSuite\":\"Suite123\"}" \ 
--user "username":"password"
```

Response body:

```
{ 
  "result": { 
    "snboqId": <sys_id of newly inserted BOQ record> 
  } 
}
```

