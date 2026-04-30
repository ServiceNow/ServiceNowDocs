---
title: Cloud Runner Test User REST API
description: Manages test user jobs to be executed in a cloud runner for Automated Test Framework \(ATF\).Provides the status of the test user job for a provided Browser Orchestration Queue \(BOQ\) record.Checks whether a provided user is a valid cloud user.Inserts a test user job into the BOQ \[sn\_atf\_tg\_sn\_boq\] table for a given user name, which is then run on cloud runner.Sets the test user job status in the Browser Orchestration Queue \(BOQ\) \[sn\_atf\_tg\_sn\_boq\] table to complete.Starts an end-to-end test user job on cloud runner. If the user is able to log in with the admin role, the cloud user property defaults to this user for future test runs and test generations.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Cloud Runner Test User REST API

Manages test user jobs to be executed in a cloud runner for Automated Test Framework \(ATF\).

The Cloud Runner Test User API requires the [ATF Test Generator and Cloud Runner](https://www.servicenow.com/docs/access?context=atf-tg-cr-intro&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) \(sn\_atf\_tg\) plugin. The methods available with this API run in the **now** namespace and can be called using API Name, **One-click regression testing for ATF**, in the REST API Explorer. The admin role is required to access this API.

You can use this API for the following tasks:

-   Start the user test job.
-   Set the cloud user.
-   Check if the user specified is valid.
-   Check the progress of the user test job.
-   Cancel the test job.

The Cloud Runner Test Runner API may be used in tandem with the [Cloud Runner Test Generation REST API](cloudrunner-testgeneration-api.md#) and [Cloud Runner Test User REST API](cloudrunner-testuser-api.md#). For instance, you can generate a test \(Cloud Runner Test Generation API\) and then get the progress of the test in the browser orchestration queue \(Cloud Runner TEST Generation API\) and check the number of tests that passed or failed.

To view the Server API reference documentation of this API, see [Cloud Runner TestUserApi – Scoped, Global](../../../app-store/dev_portal/API_reference/CloudRunnerAPI-TestUserAPIScoped/concept/cloudrnr-TestUserAPI-scoped.md#).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Cloud Runner Test User - GET /now/sn\_atf\_tg/test\_user\_progress

Provides the status of the test user job for a provided Browser Orchestration Queue \(BOQ\) record.

### URL format

Default URL: GET `/api/now/sn_atf_tg/test_user_progress`

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

Required. BOQ record sys\_id of the test user job to get the progress of.Data Type: String

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

<table id="table_u3v_zh3_j1c"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Successfully retrieved the progress of the test user job.

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

Object containing the progress results of the test runner job or a message explaining why the request failed.```
"result": { 
    "progress": 100, 
    "state": "completed" 
  }
```

Or:

```
"result": { 
    "message": "String"
}
```

Data type: Object

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

Current status of the BOQ record.Possible values:

-   Browsers requested: A request has been sent to the cloud infrastructure to start browsers for test generation or test running.
-   Completed: The test task is complete.
-   Failed state: The test task failed.
-   Pending: The requested test activity has been created and waiting to be executed.
-   Processing: The instance is scanning for records to ensure that the execution trackers are marked for cloud runner before the request is sent to the cloud infrastructure.
-   Running: The cloud infrastructure browsers find and execute pending tests.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following request example shows how to check the progress of a test user job.

```
curl "https://instance.service-now.com/api/now/sn_atf_tg/test_user_progress?snboqId=<sys_id of SNBOQ record>" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user "username:password"
```

Response body:

```
{ 
  "result": { 
    "progress": 100, 
    "state": "completed" 
  } 
}
```

## Cloud Runner Test User - GET /now/sn\_atf\_tg/is\_valid\_cloud\_user

Checks whether a provided user is a valid cloud user.

This method checks if the user passes the following criteria:

-   Exists,
-   Is active,
-   Is not locked out,
-   Needs a password reset,
-   Is an admin,
-   Is read-only,
-   Is web services-only

### URL format

Default URL: GET `/api/now/sn_atf_tg/is_valid_cloud_user`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

username

</td><td>

Required. User name of the sys\_user to check if the user passes the following baseline criteria.-   Exists,
-   Is active,
-   Is not locked out,
-   Needs a password reset,
-   Is an admin,
-   Is read-only,
-   Is web services-only

If any of these conditions fail, the API returns a false boolean with a message about which criteria failed.

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
|200|Returns true or false if the user is valid and satisfies cloud user criteria.|
|403|Error granting user access to the endpoint. Ensure that the user has the admin role.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the results of the request.```

  "result": { 
    "validUser": Boolean 
  }
```

Data type: Object

</td></tr><tr><td>

result.validUser

</td><td>

Flag that indicates whether the user satisfies cloud user criteria. When true, the user satisfies the criteria.Data type: Boolean

</td></tr></tbody>
</table>### cURL request

The following request checks if the provided sys\_user meets the criteria to use cloud functionality.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/is_valid_cloud_user?username=<username of sys_user to check>" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user "username:password"
```

Response body:

```
{ 
  "result": { 
    "validUser": <Boolean value indicating whether user is valid cloud user> 
  } 
}
```

## Cloud Runner Test User - POST /now/sn\_atf\_tg/test\_user

Inserts a test user job into the BOQ \[sn\_atf\_tg\_sn\_boq\] table for a given user name, which is then run on cloud runner.

### URL format

Default URL: POST `/api/now/sn_atf_tg/test_user`

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

username

</td><td>

Required. Username of the sys\_user to test the end-to-end infrastructure of the cloud runner.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_xh4_cfj_41c" class="rest_api_request_headers"><thead><tr><th>

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

Successfully inserted a test user BOQ job.

</td></tr><tr><td>

400

</td><td>

Error starting test user job.If an empty user name is provided or a user can’t be found in sys\_user table, the server throws an error.

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
    "snboqId": String
  }
```

Or:

```
"result": { 
    "message": "String"
}
```

Data type: Object

</td></tr><tr><td>

result.message

</td><td>

Error message detailing why the username cannot be assigned test capabilities. The message parameter is not returned in a successful response.Data type: String

</td></tr><tr><td>

result.snboqId

</td><td>

Sys\_id of the BOQ record that is inserted when test user job starts successfully.Data type: String

Table: BOQ \[sn\_atf\_tg\_sn\_boq\]

</td></tr></tbody>
</table>### cURL request

The following request example shows how to insert a test user job into the BOQ \[sn\_atf\_tg\_sn\_boq\] table for a given username.

```
curl "http://instance.service-now.com/api/now/sn_atf_tg/test_user" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"username\":\"<username of sys_user to test cloud infrastructure>\"}" \ 
--user "username:password"
```

The response returns a sys\_id of the BOQ record that is inserted when test user job starts.

```
{ 
  "result": { 
    "snboqId": "<sys_id of newly inserted BOQ record>" 
  } 
}
```

The following example returns a 400 error message when no user name or an invalid user name is passed.

```
curl "https://instance.service-now.com/api/now/sn_atf_tg/test_user" \
--request POST \
--header "Accept:application/json" \
--user "username:password"
```

Response:

```
{
  "result": {
    "message": "Unable to set cloud user as cloud user not valid"
  }
}
```

## Cloud Runner Test User - POST /now/sn\_atf\_tg/cancel\_test\_user

Sets the test user job status in the Browser Orchestration Queue \(BOQ\) \[sn\_atf\_tg\_sn\_boq\] table to complete.

### URL format

Default URL: POST `/api/now/sn_atf_tg/cancel_test_user`

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

Required. Sys\_id of the BOQ record to cancel associated with the test user job.Data Type: String

Table: SNBOQ \[sn\_atf\_tg\_sn\_boq\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_m4k_dfj_41c" class="rest_api_request_headers"><thead><tr><th>

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

<table id="table_u3v_zh3_j1c"><thead><tr><th>

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

Object containing the results of the request.```

  "result": { 
    "message": String
  }
```

Data type: Object

</td></tr><tr><td>

result.message

</td><td>

Message detailing whether the test user cancellation was successful.Data type: String

</td></tr></tbody>
</table>### cURL request

The following request demonstrates how to cancel a test user job in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.

```
curl "https://instance.service-now.com/api/now/sn_atf_tg/cancel_test_user" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"snboqId\":\"<sys_id of BOQ record>\"}" \ 
--user "username:password"
```

Successful response body:

```
{ 
  "result": { 
    "message": "success" 
  } 
}
```

## Cloud Runner Test User - POST /now/sn\_atf\_tg/select\_cloud\_user

Starts an end-to-end test user job on cloud runner. If the user is able to log in with the admin role, the cloud user property defaults to this user for future test runs and test generations.

### URL format

Default URL: POST `/api/now/sn_atf_tg/select_cloud_user`

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

username

</td><td>

Required. User name of the sys\_user to test and set the cloud user for future test runner and test generation jobs.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_g43_2fj_41c" class="rest_api_request_headers"><thead><tr><th>

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
|200|Successfully tested the end to end cloud runner infrastructure and set the cloud user for future test run and test generation jobs.|
|400|Error testing the full end to end cloud runner infrastructure and setting the cloud user. Ensure that the user name isn’t empty or that the user exists in the sys\_user table for a given user name.|
|403|Error granting user access to the endpoint. Ensure that the user has the admin role.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the results of the request.```

  "result": { 
    "message": "String"
  }
```

Data type: Object

</td></tr><tr><td>

result.message

</td><td>

Message detailing whether the user was successfully selected for future test runs and test generations on the cloud runner infrastructure.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to request a specific user to be selected for future test runs and test generations on the cloud runner infrastructure.

```
curl "https://instance.service-now.com/api/now/sn_atf_tg/select_cloud_user" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"username\":\"<username of sys_user to set as cloud user>\"}" \ 
--user "username:password"
```

The response body returns a success message indicating that the cloud user is successfully selected for test runs and generations.

```
{ 
  "result": { 
    "message": "success" 
  } 
}
```

