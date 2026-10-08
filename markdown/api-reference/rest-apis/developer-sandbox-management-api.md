---
title: Developer Sandbox Management API
description: The Developer Sandbox Management API provides endpoints to create, list, retrieve, and destroy developer sandboxes, and to check the status of sandbox lifecycle operations.Destroys a developer sandbox, identified by its name.Retrieves the status of an asynchronous sandbox creation or destruction operation.Retrieves the details of a single developer sandbox, identified by its sys\_id.Retrieves all developer sandboxes on the instance along with a summary of sandbox allocation.Creates a developer sandbox and assigns the specified user as its owner.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/developer-sandbox-management-api.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 27
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Developer Sandbox Management API

The Developer Sandbox Management API provides endpoints to create, list, retrieve, and destroy developer sandboxes, and to check the status of sandbox lifecycle operations.

A developer sandbox \(DSB\) is an isolated development environment within a single ServiceNow instance. Developers use a sandbox to make and test changes without affecting, or being affected by, other users of the instance.

Use this API to manage the sandbox lifecycle programmatically, such as when tooling provisions and retires developer environments at scale without administrator interaction in the UI.

Sandbox creation and destruction are asynchronous. Both operations return an `operationId` and a `trackerStatusUrl`. Poll the GET /now/dsb/management/operations/\{operationId\} endpoint with that identifier to determine when the operation completes. A sandbox must exist before you can retrieve its details or destroy it. The list and retrieve endpoints have no ordering requirements.

## Requirements

This API runs in the global `now` namespace.

The following requirements apply to all endpoints in this API.

-   The Developer Sandboxes plugin \(com.glide.dsb\) must be installed. The plugin is active by default.
-   The `glide.dev_sandbox.enabled` system property must be set to true.
-   The calling user must have one of the following roles: admin, maint, or sandbox\_manager.
-   At least one unallocated sandbox node must be available for sandbox creation to succeed.
-   A valid User \[sys\_user\] record must exist for the user that you assign as the sandbox owner. The platform does not validate the owner sys\_id that you pass in the create request.

## Call ordering and use cases

Use cases: provisioning and lifecycle management of DSBs for automation/tooling that manages developer environments at scale \(for example, internal platform tooling\), without requiring direct UI interaction.

|Endpoint|Description|
|--------|-----------|
|[Developer Sandbox Management API - DELETE /now/dsb/management/sandboxes/\{dsbName\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/developer-sandbox-management-api.md)|Destroys a developer sandbox, identified by its name. Only sandboxes in the `running` or `error` state can be destroyed.|
|[Developer Sandbox Management API - GET /now/dsb/management/operations/\{operationId\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/developer-sandbox-management-api.md)|Retrieves the status of an asynchronous sandbox creation or destruction operation.|
|[Developer Sandbox Management API - GET /now/dsb/management/sandboxes/info/\{sysId\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/developer-sandbox-management-api.md)|Retrieves all developer sandboxes on the instance along with a summary of sandbox allocation.|
|[Developer Sandbox Management API - GET /now/dsb/management/sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/developer-sandbox-management-api.md)|Retrieves the details of a single developer sandbox, identified by its sys\_id.|
|[Developer Sandbox Management API - POST /now/dsb/management/sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/developer-sandbox-management-api.md)|Creates a developer sandbox and assigns the specified user as its owner.|

Call ordering: Create and Destroy are asynchronous — both return an `operationId`/`trackerStatusUrl` that must be polled via `GET /operations/{operationId}` to determine when the operation actually completes. There is no strict ordering requirement between List/Get-info calls, but a sandbox must exist \(post-creation\) before Get-info or Destroy will succeed.

## Association with other APIs

This REST API is the external counterpart to `sn_dsb.API`, the server-side Scriptable API \(`DevSandboxJS.java`\) exposed for in-instance scripting use \(`registerDsb()`, `assignSandboxNode()`, `reassignSandboxNode()`, `destroySandbox()`\). Both front the same `IDsbManagementService`/service-locator layer described in `DevSandbox.java`. These two APIs are not meant to be used interchangeably or serve distinct audiences. `sn_dsb.API` is for internal team use. This API is for external customer use.

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/api-rest.md)

## Developer Sandbox Management API - DELETE /now/dsb/management/sandboxes/\{dsbName\}

Destroys a developer sandbox, identified by its name.

Use this endpoint to tear down a developer sandbox that is no longer needed and release its node back to the pool.

Sandbox destruction is asynchronous. This endpoint validates the request and queues the sandbox for destruction. Use the returned `operationId` with the GET /now/dsb/management/operations/\{operationId\} endpoint to poll for completion.

Only sandboxes in the `running` or `error` state can be destroyed.

Requires the Developer Sandboxes plugin \(com.glide.dsb\) and the `glide.dev_sandbox.enabled` system property set to true. The calling user must have the admin, maint, or sandbox\_manager role.

### URL format

Versioned URL: `/api/now/v1/dsb/management/sandboxes/{dsbName}`

Default URL: `/api/now/dsb/management/sandboxes/{dsbName}`

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

dsbName

</td><td>

Name of the sandbox to destroy. This value is the sandbox name, not its sys\_id. Located in the Developer Sandbox \[sys\_dsb\] table.

 Data type: String

 Maximum length: 20

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|Content-Type|Data format of the response body. Value: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Accepted. Sandbox destruction was accepted and queued for asynchronous processing. Poll the URL in `trackerStatusUrl` to determine when destruction completes.|
|400|Bad Request. The `dsbName` path parameter is missing or empty \("Sandbox name is required"\).|
|404|Not Found. No sandbox exists with the specified name \("Sandbox not found: \{dsbName\}"\), or no sandbox record could be found for the name when destruction was queued \("Unable to find a sys\_dsb record with the specified name: name=\{dsbName\}"\).|
|409|Conflict. The sandbox is already being destroyed \("Sandbox '\{dsbName\}' is already being destroyed"\), or it is in a state that cannot be destroyed \("Cannot destroy sandbox '\{dsbName\}' while it is in state: \{state\}"\). Only sandboxes in the `running` or `error` state can be destroyed.|
|500|Internal Server Error. Sandbox destruction failed. For example, the event to queue destruction could not be fired \("Failed to queue sandbox destruction event: dsbName=\{dsbName\}"\). This status code is also returned when the calling user does not have the admin, maint, or sandbox\_manager role. **\[NEEDS DEV VERIFICATION\]** Confirm whether the 500 response for a privilege failure is expected behavior for publication, or whether a fix to return 403 is planned for this release.|
|503|Service Unavailable. An upgrade that affects developer sandboxes is in progress. Retry the request later.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

displayName

</td><td>

Display name of the sandbox. Omitted from the response if the sandbox has no display name.

 Data type: String

</td></tr><tr><td>

errorMessage

</td><td>

Description of the failure. Returned only in error responses.

 Data type: String

</td></tr><tr><td>

message

</td><td>

Status message for the destruction request. For example, "Sandbox destruction queued successfully".

 Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the sandbox being destroyed.

 Data type: String

 Maximum length: 20

</td></tr><tr><td>

operationId

</td><td>

Unique identifier of the asynchronous destruction operation. Pass this value to the GET /now/dsb/management/operations/\{operationId\} endpoint to check the status of the operation.

 Data type: String

</td></tr><tr><td>

trackerStatus

</td><td>

Status of the destruction operation at the time of the response.

 Valid values:

 -   queued
-   in\_progress
-   completed
-   failed

 Data type: String

</td></tr><tr><td>

trackerStatusUrl

</td><td>

Relative URL to poll for the status of the destruction operation. For example, /api/now/dsb/management/operations/6fa459ea-ee8a-3ca4-894e-db77e160355e.

 Data type: String

</td></tr></tbody>
</table>### Effect on sandbox data

Destroying a sandbox tears down its data and releases its node. **\[NEEDS DEV VERIFICATION\]** Confirm whether sandbox data can be recovered after destruction, and whether an export should be requested first, so that the appropriate warning can be added here.

### cURL request

This example destroys the sandbox named dsb-jsmith-feature1.

```
curl -X DELETE \
  "https://instance.servicenow.com/api/now/dsb/management/sandboxes/dsb-jsmith-feature1" \
  -H "Accept: application/json" \
  -u 'username':'password'
```

The sandbox was queued for asynchronous destruction and the response returns a 202 status code.

```
{
  "operationId": "6fa459ea-ee8a-3ca4-894e-db77e160355e",
  "name": "dsb-jsmith-feature1",
  "trackerStatus": "queued",
  "message": "Sandbox destruction queued successfully",
  "trackerStatusUrl": "/api/now/dsb/management/operations/6fa459ea-ee8a-3ca4-894e-db77e160355e"
}
```

### Python request

This example destroys the sandbox named dsb-jsmith-feature1.

```
#Need to install requests package for python
#easy_install requests
import requests

# Set the request parameters
url = 'https://instance.servicenow.com/api/now/dsb/management/sandboxes/dsb-jsmith-feature1'

# Eg. User name="username", Password="password" for this code sample.
user = 'username'
pwd = 'password'

# Set proper headers
headers = {"Accept":"application/json"}

# Do the HTTP request
response = requests.delete(url, auth=(user, pwd), headers=headers)

# Check for HTTP codes other than 202
if response.status_code != 202:
    print('Status:', response.status_code, 'Headers:', response.headers, 'Error Response:', response.json())
    exit()

# Decode the JSON response into a dictionary and use the data
data = response.json()
print(data)
```

The sandbox was queued for asynchronous destruction and the response returns a 202 status code.

```
{
  "operationId": "6fa459ea-ee8a-3ca4-894e-db77e160355e",
  "name": "dsb-jsmith-feature1",
  "trackerStatus": "queued",
  "message": "Sandbox destruction queued successfully",
  "trackerStatusUrl": "/api/now/dsb/management/operations/6fa459ea-ee8a-3ca4-894e-db77e160355e"
}
```

## Developer Sandbox Management API - GET /now/dsb/management/operations/\{operationId\}

Retrieves the status of an asynchronous sandbox creation or destruction operation.

Sandbox creation and destruction are asynchronous. Use this endpoint to poll an operation returned by the POST /now/dsb/management/sandboxes or DELETE /now/dsb/management/sandboxes/\{dsbName\} endpoint until the operation completes or fails.

Requires the Developer Sandboxes plugin \(com.glide.dsb\) and the `glide.dev_sandbox.enabled` system property set to true. The calling user must have the admin, maint, or sandbox\_manager role.

### URL format

Versioned URL: `/api/now/v1/dsb/management/operations/{operationId}`

Default URL: `/api/now/dsb/management/operations/{operationId}`

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

operationId

</td><td>

Identifier of the operation to check. This value is returned as `operationId` by the POST /now/dsb/management/sandboxes and DELETE /now/dsb/management/sandboxes/\{dsbName\} endpoints.

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|Content-Type|Data format of the response body. Value: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. The `operationId` path parameter is missing or empty \("Operation ID is required"\).|
|404|Not Found. No operation exists for the specified `operationId` \("Operation not found"\).|
|500|Internal Server Error. Returned when the calling user does not have the admin, maint, or sandbox\_manager role. **\[NEEDS DEV VERIFICATION\]** Confirm whether the 500 response for a privilege failure is expected behavior for publication, or whether a fix to return 403 is planned for this release.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errorMessage

</td><td>

Description of the failure. Returned only in error responses.

 Data type: String

</td></tr><tr><td>

message

</td><td>

Status message for the operation. For example, "Initializing sandbox".

 Data type: String

</td></tr><tr><td>

operationId

</td><td>

Identifier of the operation.

 Data type: String

</td></tr><tr><td>

operationType

</td><td>

Type of sandbox lifecycle operation.

 Valid values:

 -   create
-   destroy
-   unknown

 Data type: String

</td></tr><tr><td>

percentComplete

</td><td>

Portion of the operation that has completed. The value increases incrementally as tables are processed during sandbox creation or teardown.

 Data type: Number \(integer\)

 Range: 0-100

 Unit: Percent

</td></tr><tr><td>

state

</td><td>

Status of the operation.

 Valid values:

 -   queued
-   in\_progress
-   completed
-   failed

 Data type: String

</td></tr></tbody>
</table>### Polling for completion

Continue to call this endpoint until `state` is `completed` or `failed`. When the operation fails, use `errorMessage` to identify the cause. **\[NEEDS DEV VERIFICATION\]** Confirm a recommended polling interval, and how long an operation record remains retrievable after the operation finishes.

### cURL request

This example retrieves the status of the sandbox creation operation with the specified operation ID.

```
curl -X GET \
  "https://instance.servicenow.com/api/now/dsb/management/operations/9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d" \
  -H "Accept: application/json" \
  -u 'username':'password'
```

The creation operation is still in progress and is 45 percent complete.

```
{
  "operationId": "9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d",
  "operationType": "create",
  "state": "in_progress",
  "percentComplete": 45,
  "message": "Initializing sandbox"
}
```

### Python request

This example retrieves the status of the sandbox creation operation with the specified operation ID.

```
#Need to install requests package for python
#easy_install requests
import requests

# Set the request parameters
url = 'https://instance.servicenow.com/api/now/dsb/management/operations/9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d'

# Eg. User name="username", Password="password" for this code sample.
user = 'username'
pwd = 'password'

# Set proper headers
headers = {"Accept":"application/json"}

# Do the HTTP request
response = requests.get(url, auth=(user, pwd), headers=headers)

# Check for HTTP codes other than 200
if response.status_code != 200:
    print('Status:', response.status_code, 'Headers:', response.headers, 'Error Response:', response.json())
    exit()

# Decode the JSON response into a dictionary and use the data
data = response.json()
print(data)
```

The creation operation is still in progress and is 45 percent complete.

```
{
  "operationId": "9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d",
  "operationType": "create",
  "state": "in_progress",
  "percentComplete": 45,
  "message": "Initializing sandbox"
}
```

## Developer Sandbox Management API - GET /now/dsb/management/sandboxes/info/\{sysId\}

Retrieves the details of a single developer sandbox, identified by its sys\_id.

Use this endpoint when you already have the sys\_id of a sandbox, such as from the GET /now/dsb/management/sandboxes endpoint, and need its current details.

Requires the Developer Sandboxes plugin \(com.glide.dsb\) and the `glide.dev_sandbox.enabled` system property set to true. The calling user must have the admin, maint, or sandbox\_manager role.

### URL format

Versioned URL: `/api/now/v1/dsb/management/sandboxes/info/{sysId}`

Default URL: `/api/now/dsb/management/sandboxes/info/{sysId}`

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

sysId

</td><td>

Sys\_id of the sandbox record to retrieve. Located in the Developer Sandbox \[sys\_dsb\] table. Must be a valid 32-character sys\_id or the request is rejected with a 400 status code.

 Data type: String

 Maximum length: 32

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|Content-Type|Data format of the response body. Value: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. The `sysId` path parameter is not a valid sys\_id \("Invalid sandbox sys\_id"\).|
|404|Not Found. No sandbox exists for the specified sys\_id \("Sandbox not found"\).|
|500|Internal Server Error. Returned when the calling user does not have the admin, maint, or sandbox\_manager role. **\[NEEDS DEV VERIFICATION\]** Confirm whether the 500 response for a privilege failure is expected behavior for publication, or whether a fix to return 403 is planned for this release.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aisPartitionId

</td><td>

Randomly generated identifier of the AI Search partition assigned to the sandbox. Set when AI Search is enabled on the instance. Empty when AI Search is not enabled.

 Data type: String

</td></tr><tr><td>

createdOn

</td><td>

Date and time that the sandbox record was created, in the format yyyy-MM-dd HH:mm:ss.

 Data type: String

</td></tr><tr><td>

dataUtilization

</td><td>

Amount of data consumed by the sandbox.

 Data type: Number \(integer\)

 Unit: Bytes **\[NEEDS DEV VERIFICATION\]** Confirm the unit of measure and how the value is calculated.

</td></tr><tr><td>

displayName

</td><td>

Display name of the sandbox.

 Data type: String

</td></tr><tr><td>

exportState

</td><td>

Status of the most recent export of the sandbox.

 Valid values:

 -   not\_exported
-   requested
-   scheduled
-   in\_progress
-   completed

 Data type: String

</td></tr><tr><td>

lastAccessedOn

</td><td>

Date and time that the sandbox was last accessed, in the format yyyy-MM-dd HH:mm:ss.

 Data type: String

</td></tr><tr><td>

name

</td><td>

Unique name of the sandbox.

 Data type: String

 Maximum length: 20

</td></tr><tr><td>

originInstanceName

</td><td>

Name of the instance that requested the sandbox.

 Data type: String

</td></tr><tr><td>

owner

</td><td>

Sys\_id of the user who owns the sandbox. Located in the User \[sys\_user\] table. This value is the sys\_id, not the user name or display name.

 Data type: String

 Maximum length: 32

</td></tr><tr><td>

pool

</td><td>

Name of the node pool that the sandbox belongs to.

 Data type: String

</td></tr><tr><td>

reqItemId

</td><td>

Sys\_id of the requested item that provisioned the sandbox, if the sandbox was provisioned through a catalog request. Located in the Requested Item \[sc\_req\_item\] table. Empty if the sandbox was not provisioned through a catalog request. **\[NEEDS DEV VERIFICATION\]** Confirm the referenced table.

 Data type: String

 Maximum length: 32

</td></tr><tr><td>

state

</td><td>

Lifecycle state of the sandbox.

 Valid values:

 -   queued
-   initializing
-   starting
-   running
-   retiring
-   restarting
-   error
-   upgrading

 Data type: String

</td></tr><tr><td>

sysId

</td><td>

Sys\_id of the sandbox record. Located in the Developer Sandbox \[sys\_dsb\] table.

 Data type: String

 Maximum length: 32

</td></tr><tr><td>

url

</td><td>

URL of the sandbox instance.

 Data type: String

 Maximum length: 200

</td></tr></tbody>
</table>### cURL request

This example retrieves the details of the sandbox with the specified sys\_id.

```
curl -X GET \
  "https://instance.servicenow.com/api/now/dsb/management/sandboxes/info/a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6" \
  -H "Accept: application/json" \
  -u 'username':'password'
```

The sandbox was found and its details are returned.

```
{
  "displayName": "jsmith - feature1",
  "name": "dsb-jsmith-feature1",
  "state": "running",
  "url": "https://dsb-jsmith-feature1.service-now.com",
  "pool": "default",
  "createdOn": "2026-08-01 10:15:00",
  "owner": "62826bf03710200044e0bfc8bcbe5df1",
  "originInstanceName": "dev12345",
  "sysId": "a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6",
  "dataUtilization": 104857600,
  "lastAccessedOn": "2026-08-13 09:00:00",
  "reqItemId": "",
  "exportState": "not_exported",
  "aisPartitionId": ""
}
```

### Python request

This example retrieves the details of the sandbox with the specified sys\_id.

```
#Need to install requests package for python
#easy_install requests
import requests

# Set the request parameters
url = 'https://instance.servicenow.com/api/now/dsb/management/sandboxes/info/a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6'

# Eg. User name="username", Password="password" for this code sample.
user = 'username'
pwd = 'password'

# Set proper headers
headers = {"Accept":"application/json"}

# Do the HTTP request
response = requests.get(url, auth=(user, pwd), headers=headers)

# Check for HTTP codes other than 200
if response.status_code != 200:
    print('Status:', response.status_code, 'Headers:', response.headers, 'Error Response:', response.json())
    exit()

# Decode the JSON response into a dictionary and use the data
data = response.json()
print(data)
```

The sandbox was found and its details are returned.

```
{
  "displayName": "jsmith - feature1",
  "name": "dsb-jsmith-feature1",
  "state": "running",
  "url": "https://dsb-jsmith-feature1.service-now.com",
  "pool": "default",
  "createdOn": "2026-08-01 10:15:00",
  "owner": "62826bf03710200044e0bfc8bcbe5df1",
  "originInstanceName": "dev12345",
  "sysId": "a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6",
  "dataUtilization": 104857600,
  "lastAccessedOn": "2026-08-13 09:00:00",
  "reqItemId": "",
  "exportState": "not_exported",
  "aisPartitionId": ""
}
```

## Developer Sandbox Management API - GET /now/dsb/management/sandboxes

Retrieves all developer sandboxes on the instance along with a summary of sandbox allocation.

Use this endpoint to retrieve a full inventory of the developer sandboxes on the instance and the current allocation counts in a single call.

The response returns every sandbox record on the instance. This endpoint does not support filtering, sorting, pagination, or field selection.

Requires the Developer Sandboxes plugin \(com.glide.dsb\) and the `glide.dev_sandbox.enabled` system property set to true. The calling user must have the admin, maint, or sandbox\_manager role.

### URL format

Versioned URL: `/api/now/v1/dsb/management/sandboxes`

Default URL: `/api/now/dsb/management/sandboxes`

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

None

</td><td>

 

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|Content-Type|Data format of the response body. Value: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|500|Internal Server Error. Returned when the calling user does not have the admin, maint, or sandbox\_manager role. **\[NEEDS DEV VERIFICATION\]** Confirm whether the 500 response for a privilege failure is expected behavior for publication, or whether a fix to return 403 is planned for this release.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

allocated

</td><td>

Number of sandboxes assigned to the user pool. A sandbox counts as allocated once its `pool` value is `user`, regardless of its lifecycle state.

 Data type: Number \(integer\)

</td></tr><tr><td>

available

</td><td>

Number of sandboxes that can still be allocated, calculated as `total` minus `allocated`. The value is never less than 0. This value is not derived from sandbox lifecycle state.

 Data type: Number \(integer\)

 Minimum value: 0

</td></tr><tr><td>

dsbs

</td><td>

List of the developer sandboxes on the instance, one object per sandbox.

 Data type: Array of objects

 ```
"dsbs": [
  {
    "aisPartitionId": "String",
    "createdOn": "String",
    "dataUtilization": Number,
    "displayName": "String",
    "exportState": "String",
    "lastAccessedOn": "String",
    "name": "String",
    "originInstanceName": "String",
    "owner": "String",
    "pool": "String",
    "reqItemId": "String",
    "state": "String",
    "sysId": "String",
    "url": "String"
  }
]
```

</td></tr><tr><td>

dsbs.aisPartitionId

</td><td>

Randomly generated identifier of the AI Search partition assigned to the sandbox. Set when AI Search is enabled on the instance. Empty when AI Search is not enabled.

 Data type: String

</td></tr><tr><td>

dsbs.createdOn

</td><td>

Date and time that the sandbox record was created, in the format yyyy-MM-dd HH:mm:ss.

 Data type: String

</td></tr><tr><td>

dsbs.dataUtilization

</td><td>

Amount of data consumed by the sandbox.

 Data type: Number \(integer\)

 Unit: Bytes **\[NEEDS DEV VERIFICATION\]** Confirm the unit of measure and how the value is calculated.

</td></tr><tr><td>

dsbs.displayName

</td><td>

Display name of the sandbox.

 Data type: String

</td></tr><tr><td>

dsbs.exportState

</td><td>

Status of the most recent export of the sandbox.

 Valid values:

 -   not\_exported
-   requested
-   scheduled
-   in\_progress
-   completed

 Data type: String

</td></tr><tr><td>

dsbs.lastAccessedOn

</td><td>

Date and time that the sandbox was last accessed, in the format yyyy-MM-dd HH:mm:ss.

 Data type: String

</td></tr><tr><td>

dsbs.name

</td><td>

Unique name of the sandbox.

 Data type: String

 Maximum length: 20

</td></tr><tr><td>

dsbs.originInstanceName

</td><td>

Name of the instance that requested the sandbox.

 Data type: String

</td></tr><tr><td>

dsbs.owner

</td><td>

Sys\_id of the user who owns the sandbox. Located in the User \[sys\_user\] table. This value is the sys\_id, not the user name or display name.

 Data type: String

 Maximum length: 32

</td></tr><tr><td>

dsbs.pool

</td><td>

Name of the node pool that the sandbox belongs to.

 Data type: String

</td></tr><tr><td>

dsbs.reqItemId

</td><td>

Sys\_id of the requested item that provisioned the sandbox, if the sandbox was provisioned through a catalog request. Located in the Requested Item \[sc\_req\_item\] table. Empty if the sandbox was not provisioned through a catalog request. **\[NEEDS DEV VERIFICATION\]** Confirm the referenced table.

 Data type: String

 Maximum length: 32

</td></tr><tr><td>

dsbs.state

</td><td>

Lifecycle state of the sandbox.

 Valid values:

 -   queued
-   initializing
-   starting
-   running
-   retiring
-   restarting
-   error
-   upgrading

 Data type: String

</td></tr><tr><td>

dsbs.sysId

</td><td>

Sys\_id of the sandbox record. Located in the Developer Sandbox \[sys\_dsb\] table.

 Data type: String

 Maximum length: 32

</td></tr><tr><td>

dsbs.url

</td><td>

URL of the sandbox instance.

 Data type: String

 Maximum length: 200

</td></tr><tr><td>

total

</td><td>

Total sandbox capacity of the instance, calculated as the lower of the sandbox node count and the licensed sandbox count. This value is a capacity ceiling, not a count of existing sandbox records.

 Data type: Number \(integer\)

</td></tr></tbody>
</table>### Allocation counts compared to sandbox state

The `total`, `available`, and `allocated` values describe license capacity and pool assignment. They do not describe the lifecycle state of individual sandboxes. To evaluate sandbox health or readiness, use the `state` value of each object in the `dsbs` array.

### cURL request

This example retrieves all developer sandboxes on the instance and the current allocation summary.

```
curl -X GET \
  "https://instance.servicenow.com/api/now/dsb/management/sandboxes" \
  -H "Accept: application/json" \
  -u 'username':'password'
```

The instance has capacity for two sandboxes, one of which is allocated.

```
{
  "total": 2,
  "available": 1,
  "allocated": 1,
  "dsbs": [
    {
      "displayName": "jsmith - feature1",
      "name": "dsb-jsmith-feature1",
      "state": "running",
      "url": "https://dsb-jsmith-feature1.service-now.com",
      "pool": "default",
      "createdOn": "2026-08-01 10:15:00",
      "owner": "62826bf03710200044e0bfc8bcbe5df1",
      "originInstanceName": "dev12345",
      "sysId": "a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6",
      "dataUtilization": 104857600,
      "lastAccessedOn": "2026-08-13 09:00:00",
      "reqItemId": "",
      "exportState": "not_exported",
      "aisPartitionId": ""
    }
  ]
}
```

### Python request

This example retrieves all developer sandboxes on the instance and the current allocation summary.

```
#Need to install requests package for python
#easy_install requests
import requests

# Set the request parameters
url = 'https://instance.servicenow.com/api/now/dsb/management/sandboxes'

# Eg. User name="username", Password="password" for this code sample.
user = 'username'
pwd = 'password'

# Set proper headers
headers = {"Accept":"application/json"}

# Do the HTTP request
response = requests.get(url, auth=(user, pwd), headers=headers)

# Check for HTTP codes other than 200
if response.status_code != 200:
    print('Status:', response.status_code, 'Headers:', response.headers, 'Error Response:', response.json())
    exit()

# Decode the JSON response into a dictionary and use the data
data = response.json()
print(data)
```

The instance has capacity for two sandboxes, one of which is allocated.

```
{
  "total": 2,
  "available": 1,
  "allocated": 1,
  "dsbs": [
    {
      "displayName": "jsmith - feature1",
      "name": "dsb-jsmith-feature1",
      "state": "running",
      "url": "https://dsb-jsmith-feature1.service-now.com",
      "pool": "default",
      "createdOn": "2026-08-01 10:15:00",
      "owner": "62826bf03710200044e0bfc8bcbe5df1",
      "originInstanceName": "dev12345",
      "sysId": "a1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6",
      "dataUtilization": 104857600,
      "lastAccessedOn": "2026-08-13 09:00:00",
      "reqItemId": "",
      "exportState": "not_exported",
      "aisPartitionId": ""
    }
  ]
}
```

## Developer Sandbox Management API - POST /now/dsb/management/sandboxes

Creates a developer sandbox and assigns the specified user as its owner.

A developer sandbox is an isolated development environment within a single ServiceNow instance. Developers use a sandbox to make and test changes without affecting, or being affected by, other users of the instance.

This endpoint validates the request body, claims a sandbox from the pool of available sandbox nodes, and queues the sandbox for creation. Sandbox creation is asynchronous. Use the returned `operationId` with the GET /now/dsb/management/operations/\{operationId\} endpoint to poll for completion.

Requires the Developer Sandboxes plugin \(com.glide.dsb\) and the `glide.dev_sandbox.enabled` system property set to true. The calling user must have the admin, maint, or sandbox\_manager role.

### URL format

Versioned URL: `/api/now/v1/dsb/management/sandboxes`

Default URL: `/api/now/dsb/management/sandboxes`

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

None

</td><td>

 

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

Required. Name to assign to the new developer sandbox. Must be unique across the instance. A duplicate name is rejected with a 400 status code and the message "Alias already in use. Try a different one."

 Data type: String

 Format: Lowercase alphanumeric characters and hyphens only. Must contain at least one letter. Must start and end with an alphanumeric character.

 Minimum length: 1

 Maximum length: 20

</td></tr><tr><td>

ownerId

</td><td>

Required. Sys\_id of the user to assign as the owner of the new sandbox. Located in the User \[sys\_user\] table.

 The platform does not verify that the specified sys\_id corresponds to an existing user record. Any non-empty value is accepted and written to the sandbox record. Validate the sys\_id before calling this endpoint.

 Data type: String

 Maximum length: 32

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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

</td><td>

Required. Data format of the request body. Supported value: application/json.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Value: application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|202|Accepted. Sandbox creation was accepted and queued for asynchronous processing. This is the typical response. Poll the URL in `trackerStatusUrl` to determine when creation completes.|
|400|Bad Request. One of the following conditions occurred: the request body is missing or malformed \("Invalid request body"\); `ownerId` is missing \("Owner is required"\); `name` is missing or does not meet the format requirements; `name` is already in use \("Alias already in use. Try a different one."\); or the licensed sandbox count is exceeded and no idle sandbox is available in the pool.|
|500|Internal Server Error. Sandbox registration failed. For example, the sandbox record could not be inserted, or a sandbox claimed from the pool had no corresponding tracker record. This status code is also returned when the calling user does not have the admin, maint, or sandbox\_manager role. **\[NEEDS DEV VERIFICATION\]** Confirm whether the 500 response for a privilege failure is expected behavior for publication, or whether a fix to return 403 is planned for this release.|
|503|Service Unavailable. One of the following conditions occurred: an upgrade that affects developer sandboxes is in progress; no sandbox node is available \("No available nodes. Please increase your total sandbox count or retire an existing sandbox."\); or a concurrent request claimed the same pooled sandbox first \("Failed to acquire claim lock for displayName=\{name\}"\). Retry the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

displayName

</td><td>

Display name of the sandbox. Omitted from the response if the sandbox has no display name.

 Data type: String

</td></tr><tr><td>

errorMessage

</td><td>

Description of the failure. Returned only in error responses.

 Data type: String

</td></tr><tr><td>

message

</td><td>

Status message for the creation request. The value depends on how the sandbox was provisioned.

 Possible values:

 -   Sandbox creation queued successfully: A new sandbox was queued for creation.
-   Sandbox is running: An already-running sandbox was claimed from the pool.
-   Sandbox initialization in progress: A sandbox that is still initializing was claimed from the pool.

 Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the sandbox being created.

 Data type: String

 Maximum length: 20

</td></tr><tr><td>

operationId

</td><td>

Unique identifier of the asynchronous creation operation. Pass this value to the GET /now/dsb/management/operations/\{operationId\} endpoint to check the status of the operation.

 Data type: String

</td></tr><tr><td>

trackerStatus

</td><td>

Status of the creation operation at the time of the response.

 Valid values:

 -   queued
-   in\_progress
-   completed
-   failed

 Data type: String

</td></tr><tr><td>

trackerStatusUrl

</td><td>

Relative URL to poll for the status of the creation operation. For example, /api/now/dsb/management/operations/9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d.

 Data type: String

</td></tr></tbody>
</table>### Asynchronous processing

This endpoint returns before sandbox creation finishes. A 202 status code indicates only that the request was accepted and queued. A 200 status code indicates that `trackerStatus` is already `completed`, which occurs when the request claimed an already-running sandbox from the pool.

To determine the final outcome of the operation, poll the GET /now/dsb/management/operations/\{operationId\} endpoint with the returned `operationId` until `state` is `completed` or `failed`. **\[NEEDS DEV VERIFICATION\]** Confirm a recommended polling interval and maximum expected creation time to publish as guidance.

### cURL request

This example creates a developer sandbox named dsb-jsmith and assigns it to the user with the specified sys\_id.

```
curl -X POST \
  "https://instance.servicenow.com/api/now/dsb/management/sandboxes" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -u 'username':'password' \
  -d '{
        "name": "dsb-jsmith",
        "ownerId": "62826bf03710200044e0bfc8bcbe5df1"
      }'
```

The sandbox was queued for asynchronous creation and the response returns a 202 status code.

```
{
  "operationId": "9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d",
  "name": "dsb-jsmith",
  "trackerStatus": "queued",
  "message": "Sandbox creation queued successfully",
  "trackerStatusUrl": "/api/now/dsb/management/operations/9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d"
}
```

### Python request

This example creates a developer sandbox named dsb-jsmith and assigns it to the user with the specified sys\_id.

```
#Need to install requests package for python
#easy_install requests
import requests
import json

# Set the request parameters
url = 'https://instance.servicenow.com/api/now/dsb/management/sandboxes'

# Eg. User name="username", Password="password" for this code sample.
user = 'username'
pwd = 'password'

# Set proper headers
headers = {"Content-Type":"application/json","Accept":"application/json"}

# Set the request body
body = {"name":"dsb-jsmith","ownerId":"62826bf03710200044e0bfc8bcbe5df1"}

# Do the HTTP request
response = requests.post(url, auth=(user, pwd), headers=headers, data=json.dumps(body))

# Check for HTTP codes other than 200 or 202
if response.status_code not in (200, 202):
    print('Status:', response.status_code, 'Headers:', response.headers, 'Error Response:', response.json())
    exit()

# Decode the JSON response into a dictionary and use the data
data = response.json()
print(data)
```

The sandbox was queued for asynchronous creation and the response returns a 202 status code.

```
{
  "operationId": "9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d",
  "name": "dsb-jsmith",
  "trackerStatus": "queued",
  "message": "Sandbox creation queued successfully",
  "trackerStatusUrl": "/api/now/dsb/management/operations/9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d"
}
```

