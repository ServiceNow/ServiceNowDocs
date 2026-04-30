---
title: CI Lifecycle Management API
description: The CI Lifecycle Management API provides endpoints to manipulate configuration item \(CI\) operational states and apply CI actions.Removes a configuration item \(CI\) action for a list of CIs.Unregisters an operator for non-workflow users.Returns a list of active configuration item \(CI\) actions for the specified CI.Determines whether two specified configuration item \(CI\) actions are compatible.Determines whether the lease has expired for the requestor of a configuration item \(CI\) action applied to the specified CI.Determines whether a specified configuration item \(CI\) action is not allowed for a CI of a specified class when in a specified operational state.Determines whether a configuration item \(CI\) from a specified class can transition from a specified operational state to a second specified operational state.Determines whether the specified active workflow user or registered user is a valid requestor.Returns the current operational state for the specified configuration item \(CI\).Extends the specified configuration item \(CI\) action's lease expiration time for the specified user.Adds a specified configuration item \(CI\) action to a specified list of CIs.Registers an operator for a non-workflow user.Sets the operational state for a specified list of configuration items \(CIs\).
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 33
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CI Lifecycle Management API

The CI Lifecycle Management API provides endpoints to manipulate configuration item \(CI\) operational states and apply CI actions.

The API interfaces adhere to restrictions and allowances specified by not allowed CI actions, compatible CI actions, and not allowed operational transitions. If an interface attempts a restricted operation, the operation is blocked, an error is logged, and a task is created if appropriate.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CI Lifecycle Management - DELETE /now/cilifecyclemgmt/actions

Removes a configuration item \(CI\) action for a list of CIs.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/actions`

Default URL: `/api/now/cilifecyclemgmt/actions`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

actionName

</td><td>

Required. Configuration item action name.Data type: String

</td></tr><tr><td id="requestor-id-query-param-name-entry">

requestorId

</td><td id="requestor-id-query-param-desc-entry">

Required. Sys\_id of a workflow context, or an operator user ID returned from the [CI Lifecycle Management - POST /now/cilifecyclemgmt/operators](ci-lifecycle-management-api.md#) endpoint. Operator user IDs are located in the CI State Registered Users \[statemgmt\_register\_users\] table.

 Data type: String

</td></tr><tr><td>

sysIds

</td><td>

Required. Comma-separated list of CI sys\_ids.Data type: String

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

<table id="table_od5_2wf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the CI action was successfully removed.Possible values:

-   true: CI action was removed.
-   false: CI action was not removed.

 Data type: String

</td></tr></tbody>
</table>### cURL request

Remove a CI action from two CIs.

```
curl --request DELETE \
'https://instance.service-now.com/api/now/cilifecyclemgmt/actions?actionName=Patching&requestorId=621b5a09309e5010f877773aa7167c0a&sysIds=00a9a80d3790200044e0bfc8bcbe5d1c,d0fdbc8437201000deeabfc8bcbe5d33' \
--header 'Accept: application/json' \
--user "username":"password"
```

The response body confirms that the CI action was removed from the CIs.

```
{
  "result": {
    "result": true
  }
}
```

## CI Lifecycle Management - DELETE /now/cilifecyclemgmt/operators/\{req\_id\}

Unregisters an operator for non-workflow users.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/operators/{req_id}`

Default URL: `/api/now/cilifecyclemgmt/operators/{req_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td id="req-id-name-entry">

req\_id

</td><td id="req-id-desc-entry">

Sys\_id of a workflow context, or an operator user ID returned from the [CI Lifecycle Management - POST /now/cilifecyclemgmt/operators](ci-lifecycle-management-api.md#) endpoint. Operator user IDs are located in the CI State Registered Users \[statemgmt\_register\_users\] table.

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

<table id="table_hsj_2wf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_kkt_tlk_lmb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the operator was successfully unregistered.Possible values:

-   true: Operator was successfully unregistered.
-   false: Operator was not successfully unregistered.

 Data type: String

</td></tr></tbody>
</table>### cURL request

Unregister an operator by user ID.

```
curl --request DELETE \
"https://instance.service-now.com/api/now/cilifecyclemgmt/operators/3cf1b3cc30121010f877773aa7167c6e" \
--header "Accept: application/json" \
--user "username":"password"
```

The response body verifies that the operator was unregistered.

```
{
  "result": {
    "result": true
  }
}
```

## CI Lifecycle Management - GET /now/cilifecyclemgmt/actions/\{sys\_id\}

Returns a list of active configuration item \(CI\) actions for the specified CI.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/actions/{sys_id}`

Default URL: `/api/now/cilifecyclemgmt/actions/{sys_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the CI for which to return associated CI actions.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

<table id="table_lrs_cwf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.ciActions** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.ciActions

</td><td>

Comma-separated list of active CI actions for the CI, or `no_active_action` if none were found.Data type: String

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the list of active CI actions was returned for all specified CIs.Possible values:

-   true: List of active CI actions was returned.
-   false: List of active CI actions was not returned.

 Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl --request GET \
'https://instance.service-now.com/api/now/cilifecyclemgmt/actions/00a9a80d3790200044e0bfc8bcbe5d1c' \
--header 'Accept: application/json' \
--user "username":"password"
```

The response body shows that no CI actions are active for the specified CI.

```
{
  "result": {
    "ciActions": [
      "no_active_action"
    ],
    "result": true
  }
}
```

## CI Lifecycle Management - GET /now/cilifecyclemgmt/compatActions

Determines whether two specified configuration item \(CI\) actions are compatible.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/compatActions`

Default URL: `/api/now/cilifecyclemgmt/compatActions`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

actionName

</td><td>

Required. Name of CI action to compare. Data type: String

</td></tr><tr><td>

otherActionName

</td><td>

Required. Name of CI action to compare. Data type: String

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

<table id="table_vz1_cwf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Flag indicating whether the two specified CI actions are compatible.Possible values:

-   true: CI actions are compatible.
-   false: CI actions are not compatible.

 Data type: String

</td></tr></tbody>
</table>### cURL request

Check compatibility of Patching and Provisioning CI actions.

```
curl --request GET \
'https://instance.service-now.com/api/now/cilifecyclemgmt/compatActions?actionName=Patching&otherActionName=Provisioning' \
--header 'Accept: application/json' \
--user "username":"password"
```

The response body confirms that the two CI actions are compatible.

```
{
  "result": true
}
```

## CI Lifecycle Management - GET /now/cilifecyclemgmt/leases/\{sys\_id\}/expired

Determines whether the lease has expired for the requestor of a configuration item \(CI\) action applied to the specified CI.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/leases/{sys_id}/expired`

Default URL: `/api/now/cilifecyclemgmt/leases/{sys_id}/expired`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the CI that is the target of the applied CI action.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

actionName

</td><td>

Required. Name of the CI action applied to the specified CI.Data type: String

</td></tr><tr><td id="requestor-id-query-param-name-entry">

requestorId

</td><td id="requestor-id-query-param-desc-entry">

Required. Sys\_id of a workflow context, or an operator user ID returned from the [CI Lifecycle Management - POST /now/cilifecyclemgmt/operators](ci-lifecycle-management-api.md#) endpoint. Operator user IDs are located in the CI State Registered Users \[statemgmt\_register\_users\] table.

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

<table id="table_hwr_bwf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the lease for the requestor of the applied CI action has expired.Possible values:

-   true: Requestor's lease has expired.
-   false: Requestor's lease has not expired.

 Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl --request GET \
'https://instance.service-now.com/api/now/cilifecyclemgmt/leases/00a9a80d3790200044e0bfc8bcbe5d1c/expired?actionName=Patching&requestorId=621b5a09309e5010f877773aa7167c0a' \
--header 'Accept: application/json' \
--user "username":"password"
```

The response body shows that the lease for the requestor of the applied CI action has not expired.

```
{
  "result": {
    "result": false
  }
}
```

## CI Lifecycle Management - GET /now/cilifecyclemgmt/notAllowedAction

Determines whether a specified configuration item \(CI\) action is not allowed for a CI of a specified class when in a specified operational state.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/notAllowedAction`

Default URL: `/api/now/cilifecyclemgmt/notAllowedAction`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

actionName

</td><td>

Required. Name of the CI action to check.Data type: String

</td></tr><tr><td>

ciClass

</td><td>

Required. CI class.Data type: String

</td></tr><tr><td>

opsLabel

</td><td>

Required. Operational state to check.Data type: String

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

<table id="table_qqg_bwf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Flag indicating whether the CI action is restricted \(not allowed\) for CIs of the specified type when in the specified operational state.Possible values:

-   true: CI action is restricted \(not allowed\).
-   false: CI action is unrestricted \(allowed\).

 Data type: String

</td></tr></tbody>
</table>### cURL request

Check whether the Patching CI action is restricted \(not allowed\) for computers in the DR Standby operational state.

```
curl --request GET \
"https://instance.service-now.com/api/now/cilifecyclemgmt/notAllowedAction?actionName=Patching&ciClass=cmdb_ci_computer&opsLabel=DR+Standby" \
--header "Accept: application/json" \
--user "username":"password"
```

The response body confirms that this action is restricted \(not allowed\) for the specified CI class when in the specified operational state.

```
{
  "result": true
}
```

## CI Lifecycle Management - GET /now/cilifecyclemgmt/notAllowedOpsTransition

Determines whether a configuration item \(CI\) from a specified class can transition from a specified operational state to a second specified operational state.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/notAllowedOpsTransition`

Default URL: `/api/now/cilifecyclemgmt/notAllowedOpsTransition`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ciClass

</td><td>

Required. CI class to check transition restrictions for.Data type: String

</td></tr><tr><td>

opsLabel

</td><td>

Required. Label of current CI operational state.Data type: String

</td></tr><tr><td>

transitionOpsLabel

</td><td>

Required. Label of operational state that is the target of the transition.Data type: String

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

<table id="table_clt_1wf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Flag indicating whether the specified operational state transition is restricted \(not allowed\) for the specified CI class.Possible values:

-   true: Operational state transition is restricted \(not allowed\).
-   false: Operational state transition is unrestricted \(allowed\).

 Data type: String

</td></tr></tbody>
</table>### cURL request

Check whether transition from Retired operational state to DR Standby operational state is restricted \(not allowed\) for Linux server CIs.

```
curl --request GET \
"https://instance.service-now.com/api/now/cilifecyclemgmt/notAllowedOpsTransition?ciClass=cmdb_ci_computer&opsLabel=Retired&transitionOpsLabel=DR+Standby" \
--header "Accept: application/json" \
--user "username":"password"
```

The response body shows that the specified operational state transition is unrestricted \(allowed\) for this CI class.

```
{
  "result": false
}
```

## CI Lifecycle Management - GET /now/cilifecyclemgmt/requestors/\{req\_id\}/valid

Determines whether the specified active workflow user or registered user is a valid requestor.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/requestors/{req_id}/valid`

Default URL: `/api/now/cilifecyclemgmt/requestors/{req_id}/valid`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td id="req-id-name-entry">

req\_id

</td><td id="req-id-desc-entry">

Sys\_id of a workflow context, or an operator user ID returned from the [CI Lifecycle Management - POST /now/cilifecyclemgmt/operators](ci-lifecycle-management-api.md#) endpoint. Operator user IDs are located in the CI State Registered Users \[statemgmt\_register\_users\] table.

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

<table id="table_mbj_1wf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the specified active workflow user or registered user is a valid requestor.Possible values:

-   true: Valid requestor.
-   false: Invalid requestor.

 Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl --request GET \
'https://instance.service-now.com/api/now/cilifecyclemgmt/requestors/4cab9b95301a9010f877773aa7167ca9/valid' \
--header 'Accept: application/json' \
--user "username":"password"
```

```
{
  "result": {
    "result": true
  }
}
```

## CI Lifecycle Management - GET /now/cilifecyclemgmt/statuses/\{sys\_id\}

Returns the current operational state for the specified configuration item \(CI\).

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/statuses/{sys_id}`

Default URL: `/api/now/cilifecyclemgmt/statuses/{sys_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the CI.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

<table id="table_pdp_yvf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.operationalStates

</td><td>

Operational state for the specified CI or `unknown` if no state is specified.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl --request GET 'https://instance.service-now.com/api/now/cilifecyclemgmt/statuses/aac0b1213784200044e0bfc8bcbe5de3' \
--header 'Accept: application/json' \
--user "username":"password"
```

```
{
  "result": {
    "operationalState": "Repair in Progress",
    "result": true
  }
}
```

## CI Lifecycle Management - PATCH /now/cilifecyclemgmt/leases/\{sys\_id\}

Extends the specified configuration item \(CI\) action's lease expiration time for the specified user.

If the previous lease has expired, the new lease time starts immediately.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/leases/{sys_id}`

Default URL: `/api/now/cilifecyclemgmt/leases/{sys_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the CI for which to extend the lease.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

actionName

</td><td>

Required. Name of the associated CI action.Data type: String

</td></tr><tr><td>

leaseTime

</td><td>

Required. Time duration for which the lease is valid for the CI action specified in **actionName**.Data type: String

 Format: HH:MM:SS

</td></tr><tr><td id="requestor-id-query-param-name-entry">

requestorId

</td><td id="requestor-id-query-param-desc-entry">

Required. Sys\_id of a workflow context, or an operator user ID returned from the [CI Lifecycle Management - POST /now/cilifecyclemgmt/operators](ci-lifecycle-management-api.md#) endpoint. Operator user IDs are located in the CI State Registered Users \[statemgmt\_register\_users\] table.

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

<table id="table_rwq_xvf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the lease time was extended.Possible values:

-   true: Lease time was extended.
-   false: Lease time was not extended.

 Data type: String

</td></tr></tbody>
</table>### cURL request

Extend the duration of a Patching CI action requestor lease by 24 hours.

```
curl --request PATCH 'https://instance.service-now.com/api/now/cilifecyclemgmt/leases/affd3c8437201000deeabfc8bcbe5dc3?actionName=Patching&leaseTime=24:00:00&requestorId=e7c3402d305a9010f877773aa7167c2a' \
--header 'Accept: application/json' \
--header 'Content-Type: application/json' \
--user "username":"password"
```

```
{
  "result": {
    "result": true
  }
}
```

## CI Lifecycle Management - POST /now/cilifecyclemgmt/actions

Adds a specified configuration item \(CI\) action to a specified list of CIs.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/actions`

Default URL: `/api/now/cilifecyclemgmt/actions`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

actionName

</td><td>

Required. Name of the CI action to add to the list.Data type: String

</td></tr><tr><td>

leaseTime

</td><td>

Time duration for which the lease is valid for specified CI action.Data type: String

 Format: HH:MM:SS

</td></tr><tr><td>

oldActionNames

</td><td>

Comma-separated list of old CI actions that all CIs should be in.Data type: String

</td></tr><tr><td id="requestor-id-query-param-name-entry">

requestorId

</td><td id="requestor-id-query-param-desc-entry">

Required. Sys\_id of a workflow context, or an operator user ID returned from the [CI Lifecycle Management - POST /now/cilifecyclemgmt/operators](ci-lifecycle-management-api.md#) endpoint. Operator user IDs are located in the CI State Registered Users \[statemgmt\_register\_users\] table.

 Data type: String

</td></tr><tr><td>

sysIds

</td><td>

Required. Comma-separated list of CI sys\_ids to which to add the CI action. Data type: String

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

<table id="table_wj1_xvf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the CI action was set for all CIs in the list.Possible values:

-   true: CI actions were set.
-   false: CI actions were not set.

 Data type: String

</td></tr></tbody>
</table>### cURL request

Add a Patching CI action to two CIs.

```
curl --request POST \
"https://instance.service-now.com/api/now/cilifecyclemgmt/actions?actionName=Patching&requestorId=621b5a09309e5010f877773aa7167c0a&sysIds=00a9a80d3790200044e0bfc8bcbe5d1c,d0fdbc8437201000deeabfc8bcbe5d33" \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username":"password"
```

```
{
  "result": {
    "result": true
  }
}
```

## CI Lifecycle Management - POST /now/cilifecyclemgmt/operators

Registers an operator for a non-workflow user.

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/operators`

Default URL: `/api/now/cilifecyclemgmt/operators`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

<table id="table_oj2_wvf_mmb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.requestorId

</td><td>

GUID for the registered operator. Use this value to set CI actions and operational states.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the operator was successfully registered.Possible values:

-   true: Operator was successfully registered.
-   false: Operator was not successfully registered.

 Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl --request POST \
"https://instance.service-now.com/api/now/cilifecyclemgmt/operators" \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username":"password"
```

```
{
  "result": {
    "result": true,
    "requestorId": "6f992b8430121010f877773aa7167c42"
  }
}
```

## CI Lifecycle Management - POST /now/cilifecyclemgmt/statuses

Sets the operational state for a specified list of configuration items \(CIs\).

### URL format

Versioned URL: `/api/now/{api_version}/cilifecyclemgmt/statuses`

Default URL: `/api/now/cilifecyclemgmt/statuses`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

oldOpsLabels

</td><td>

Comma-separated list of old CI operational states in which all CIs should be included.Data type: String

</td></tr><tr><td>

opsLabel

</td><td>

Required. Label of the operational state to set for the specified CIs.Data type: String

</td></tr><tr><td id="requestor-id-query-param-name-entry">

requestorId

</td><td id="requestor-id-query-param-desc-entry">

Required. Sys\_id of a workflow context, or an operator user ID returned from the [CI Lifecycle Management - POST /now/cilifecyclemgmt/operators](ci-lifecycle-management-api.md#) endpoint. Operator user IDs are located in the CI State Registered Users \[statemgmt\_register\_users\] table.

 Data type: String

</td></tr><tr><td>

sysIds

</td><td>

Required. Comma-separated list of sys\_ids of CIs for which the operational state is to be set.Data type: String

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

</th></tr></thead><tbody><tr><td id="status-codes-200-name-entry">

200

</td><td id="status-codes-200-desc-entry">

Successful. The request was successfully processed by the endpoint. Review the response body **result.result** parameter to verify the outcome of the operation.

 If the endpoint encounters errors while processing the request, error codes and messages appear in the response body **result.errors** parameter.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object encapsulating the result of the request.Data type: Object

 ```
"result": {
  "errors": [Array],
  "result": "String"
}
```

</td></tr><tr><td>

result.errors

</td><td>

List of objects in which each object represents an error encountered while processing the request.Data type: Array

 ```
"errors": [
  {
    "error": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.errors.error

</td><td>

Identifier for a state management error encountered while processing the request.Possible values:

-   CI\_ACTION\_ALREADY\_SET
-   CI\_ACTION\_NOT\_SET
-   DUPLICATE\_CI\_ACTION\_RECORD
-   DUPLICATE\_OPS\_STATE\_RECORD
-   DUPLICATE\_SYS\_ID
-   INCOMPATIBLE\_CI\_ACTION
-   INVALID\_CI\_ACTION
-   INVALID\_DELETE
-   INVALID\_INPUT\_PARAMETERS
-   INVALID\_LEASETIME
-   INVALID\_OPS\_STATE
-   INVALID\_OPS\_STATE\_TRANSITION
-   INVALID\_REQUESTOR
-   INVALID\_REQUESTOR\_FOR\_CI
-   INVALID\_SYS\_ID
-   MUTEX\_UNAVAILABLE
-   NOT\_ALLOWED\_CI\_ACTION
-   OPS\_STATE\_NOT\_SET
-   UNPRIORITIZED\_OPS\_STATE
-   UNSUPPORTED\_SYS\_ID

 Data type: String

</td></tr><tr><td>

result.errors.message

</td><td>

Message providing details on the associated **error**.Data type: String

</td></tr><tr><td>

result.result

</td><td>

Flag indicating whether the desired state was set for all CIs included in the request.Possible values:

-   true: Operational state set.
-   false: Operational state not set.

 Data type: String

</td></tr></tbody>
</table>### cURL request

Set the `Repair in Progress` operational state for two CIs.

```
curl --request POST \
"https://instance.service-now.com/api/now/cilifecyclemgmt/statuses?opsLabel=Repair%20in%20Progress&requestorId=23d58bc030121010f877773aa7167c83&sysIds=affd3c8437201000deeabfc8bcbe5dc3,aac0b1213784200044e0bfc8bcbe5de3" \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username":"password"
```

The response body shows that the desired operational state was set for both CIs specified in the request.

```
{
  "result": {
    "result": true
  }
}
```

