---
title: CdmSharedLibraryApi
description: The CdmSharedLibraryApi provides endpoints that enable you to create and manage shared libraries and shared components. It also has endpoints that enable you to upload and export the configuration data of a shared component.Deletes the shared library with the specified name.Deletes the specified shared component from the specified library.Returns the current status of the specified shared library upload request.Creates a new shared library with the specified name.Creates the specified shared component under the specified library.Enables you to create and manage shared libraries and shared components. This endpoint creates a shared component node in the CDM Node \[sn\_cdm\_node\] table and a shared component record in the CDM Shared Component \[sn\_cdm\_shared\_component\] table.Uploads files as part of the Configuration Data Model \(CDM\) under the components folder in a shared library.Updates the shared library information. Use this endpoint to update the name, description, state of a shared library, and the user groups that can access the library.Updates the name and description of the specified shared component.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 32
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CdmSharedLibraryApi

The CdmSharedLibraryApi provides endpoints that enable you to create and manage shared libraries and shared components. It also has endpoints that enable you to upload and export the configuration data of a shared component.

This API requires the Configuration Data Management \(CDM\) plugin to be activated for these APIs to be available in the instance. In addition, you must have one of the following roles to access this API:

-   CDM Editor Role
-   CDM Admin Role

For additional information on shared libraries and shared components, see Sharing components among applications — Component libraries.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CdmSharedLibraryApi - DELETE /sn\_cdm/shared\_libraries

Deletes the shared library with the specified name.

The CDM Admin role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/shared_libraries`

Default URL: `/api/sn_cdm/shared_libraries`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

name

</td><td>

Required. Name of the shared library to delete.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how delete the shared library "javalib".

```
curl "http://instance.servicenow.com/sn_cdm/shared_libraries?name='javalib'\ 
--request DELETE\ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Response:

```
""
```

## CdmSharedLibraryApi - DELETE /sn\_cdm/shared\_libraries/components

Deletes the specified shared component from the specified library.

The CDM Editor role is required to access this endpoint.

**Note:** You can only delete a component if it is not currently being used. Also, you cannot delete a component if the associated shared library is not active.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/shared_libraries/components`

Default URL: `/api/sn_cdm/shared_libraries/components`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

changesetNumber

</td><td>

Required. Number of the changeset associated with the component.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

name

</td><td>

Required. Name of the shared component to delete.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library where the component to delete is located.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

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

Bad Request. Possible issues:

-   Shared library does not exist.
-   Shared library is not active.
-   Shared component is in use. Cannot delete it.
-   User is restricted from deleting the shared component.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to delete the component "TestComponent" under the "javalib" shared library.

```
curl "http://instance.servicenow.com/sn_cdm/shared_libraries/components?sharedLibraryName='javalib&changesetNumber='chset-8'&name='TestComponent'\ 
--request DELETE\ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

Response:

```
""
```

## CdmSharedLibraryApi - GET /sn\_cdm/shared\_libraries/upload-status/\{upload-id\}

Returns the current status of the specified shared library upload request.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/shared_libraries/upload-status/{upload-id}`

Default URL: `/api/sn_cdm/shared_libraries/upload-status/{upload-id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

upload-id

</td><td>

Sys\_id of the upload request whose status to return. This value is returned by various CdmSharedLibrary upload request endpoints.Data type: String

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td>

Description of the error\(s\) encountered during upload.Data type: String

</td></tr><tr><td>

output

</td><td>

Description of the uploaded data or if an error occurred during the upload, an error message describing the error that was encountered.Data type: Array of String

 ```
"output": {
  "auto_validate": "String",
  "cdm_application": "String",
  "committed_at": "String",
  "committed_by": "String",
  "description": "String",
  "last_conflict_detection_time": "String",
  "number": "String",
  "publish_option": "String",
  "sharedLibraryName": "String",
  "snapshot_description": "String",
  "snapshot_name": "String",
  "state": "String",
  "sys_created_by": "String",
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr><td>

output.auto\_validate

</td><td>

Indicates whether to invoke validation after the commit.Data type: String

</td></tr><tr><td>

output.cdm\_application

</td><td>

Name of application under which the upload was performed.Data type: String

</td></tr><tr><td>

output.committed\_at

</td><td>

Date and time that the uploaded content was committed.Data type: String

</td></tr><tr><td>

output.committed\_by

</td><td>

Sys\_id of the record of the entity that performed the commit.Data type: String

</td></tr><tr><td>

output.description

</td><td>

Not currently used.Data type: String

</td></tr><tr><td>

output.last\_conflict\_detection\_time

</td><td>

Date and time conflict detection invocation.Data type: String

</td></tr><tr><td>

output.number

</td><td>

Unique changeset identification value, such as Chset-124.Data type: String

</td></tr><tr><td>

output.publish\_option

</td><td>

Value of the publish option passed in the associated upload call. For additional information on publishing snapshots, see Publish or unpublish a snapshot.

 Data type: String

</td></tr><tr><td>

output.sharedLibraryName

</td><td>

Name of the shared library as passed in the original upload call.Data type: String

</td></tr><tr><td>

output.snapshot\_description

</td><td>

Description of the associated snapshot.Data type: String

</td></tr><tr><td>

output.snapshot\_name

</td><td>

Name of the associated snapshot.Data type: String

</td></tr><tr><td>

output.state

</td><td>

State of the upload.Possible values:

-   COMPLETED: Upload has completed.
-   EXPIREDERROR: Error while processing the upload request. The job ran for more than 15 minutes and was terminated by the system.
-   IN\_PROGRESS: Upload is in process.
-   NEW: Processing has not yet started.
-   READY: Request has been queued.

 Data type: String

</td></tr><tr><td>

output.sys\_created\_by

</td><td>

Sys\_id of the entity that created the record.Data type: String

</td></tr><tr><td>

output.sys\_id

</td><td>

Sys\_id of the record containing the changeset.Data type: String

</td></tr><tr><td>

output.title

</td><td>

Title of the changeset created as part of the upload.Data type: String

</td></tr><tr><td>

processing\_state

</td><td>

Current processing state of the upload request.Possible values: PROCESSED

 Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the upload request.Possible values:

-   completed
-   error

</td></tr><tr><td>

type

</td><td>

Type of upload request.Possible values: upload\_and\_commit

 Data type: String

</td></tr><tr><td>

upload\_id

</td><td>

Sys\_id of the record containing the uploaded configuration payload. Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to request the status for the upload-id 0d91d9891b2b19109524cae0604bcbe6.

```
curl "http://instance.servicenow.com/api/sn_cdm/shared_libraries/upload-status/0d91d9891b2b19109524cae0604bcbe6" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response:

```
// Successful response
{
  "result": {
    "type": "upload_and_commit",
    "state": "completed",
    "output": {
      "sys_id": "0002ea107768a1109ac0cf0bbb5a9963",
      "number": "Chset-457",
      "title": "admin8802ea107768a1109ac0cf0bbb5a9962",
      "description": null,
      "committed_at": "",
      "committed_by": null,
      "sys_created_by": "admin",
      "state": "open",
      "publish_option": "publish_none",
      "auto_validate": false,
      "snapshot_name": null,
      "snapshot_description": null,
      "cdm_application": "OracleG-Library-15",
      "last_conflict_detection_time": null
    },
    "processing_state": "PROCESSED",
    "upload_id": "00b226547768a1109ac0cf0bbb5a99f2"
  }
}

// Error response
{
  "result": {
    "type": "upload_and_commit",
    "state": "error",
    "output": "Error: Application with sys_id 87fb1ecb1be3111050fc21b0604bcb95 is in State Deleted. No data can be modified on deleted applications",
    "processing_state": "PROCESSED",
    "upload_id": "fcdfaf7f1b88211050fc21b0604bcb79"
  }
}
```

## CdmSharedLibraryApi - POST /sn\_cdm/shared\_libraries

Creates a new shared library with the specified name.

The CDM Admin role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/shared_libraries`

Default URL: `/api/sn_cdm/shared_libraries`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

description

</td><td>

Description of the shared library. Data type: String

 Default: Empty

</td></tr><tr><td>

name

</td><td>

Required. Name of the shared library to create. This name must be unique across all CDM applications and libraries.Data type: String

</td></tr><tr><td>

returnFields

</td><td>

Comma separated list of fields to return as part of the response.Data type: String

Default: All non-system fields are returned.

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

userGroupIds

</td><td id="appName-userGroupIds-entry">

Comma-separated list of sys\_ids of the user groups that can edit the associated shared library. All users with the proper roles can view the shared library.Data type: String

Default: All users with the CDM Editor role can edit data within the shared library.

Table: Group \[sys\_user\_group\]

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;fields&gt;

</td><td>

Requested fields.Data type: Variable

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint to create the shared library Java11Lib with all user groups able to access the library.

```
curl "http://instance.servicenow.com/api/sn_cdm/shared_libraries?name=Java11Lib&description=The%20new%20java%20library" \ 
--request POST \ 
--header "Accept:application/json" \ 
--user 'userName':'password
```

Response:

```
{
  "result": {
    "sdlc_component": null,
    "cdi_count": "0",
    "available": false,
    "description": "Description of LibraryA",
    "managed_by_group": null,
    "sys_updated_on": "2023-01-18 11:34:43",
    "type": "shared_library",
    "node": {
      "value": "d852b15877a4a1109ac0cf0bbb5a99aa",
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_node/d852b15877a4a1109ac0cf0bbb5a99aa"
    },
    "sys_id": "185235dc77a4a1109ac0cf0bbb5a994e",
    "sys_updated_by": "admin",
    "node_main": {
      "value": "1852b15877a4a1109ac0cf0bbb5a99aa",
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_node_main/1852b15877a4a1109ac0cf0bbb5a99aa"
    },
    "sys_created_on": "2023-01-18 11:34:43",
    "cdi_usage": "0",
    "name": "LibraryA",
    "last_committed_changeset": {
      "value": "9052b15877a4a1109ac0cf0bbb5a99aa",
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/9052b15877a4a1109ac0cf0bbb5a99aa"
    },
    "state": "active",
    "sys_created_by": "admin"
  }
}
```

## CdmSharedLibraryApi - POST /sn\_cdm/shared\_libraries/components

Creates the specified shared component under the specified library.

The CDM Editor role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/shared_libraries/components`

Default URL: `/api/sn_cdm/shared_libraries/components`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

changesetNumber

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

description

</td><td>

Description of the shared component. Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the shared component to create in the shared library. This name must be unique.Data type: String

</td></tr><tr><td>

returnFields

</td><td>

Comma separated list of fields in the CDM Node \[sn\_cdm\_node\] table to return as part of the response.Data type: String

Default: All non-internal fields are returned.

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library under which to create the component. This library must already exist and be in the active state.Data type: String

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;requested fields&gt;

</td><td>

Requested fields.Data type: Various

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr><td>

error

</td><td id="cdm_apps-error-entry">

Only returned if an error occurred during processing.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="cdm_apps-error_detail-entry">

Details about the error that occurred.Data type: String

</td></tr><tr><td>

error.message

</td><td id="cdm_apps-error_message-entry">

Message that provides an overview of the error.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example stores the component named "SharedComponent" under the shared library "javalib".

```
curl "http://instance.servicenow.com/sn_cdm/shared_libraries/components/?sharedLibraryName=javalib&changeSetNumber='Chset-9'&name='SharedComponent'\  
--request POST\  
--header "Accept:application/json" \  
--user 'username':'password'
```

Response:

```
{
  "result": {
    "changeset_id": {
      "value": "ca7e6a501b202110636e0fe0604bcb71",
      "link": "https://instance.servicenow.com/api/now/table/sn_cdm_changeset/ca7e6a501b202110636e0fe0604bcb71"
    },
    "node_path": "!2!3!:",
    "description": null,
    "sys_updated_on": "2023-01-18 16:04:52",
    "type": "sn_cdm_node_shared_component",
    "sys_class_name": "sn_cdm_node",
    "sys_id": "6d2072901b602110636e0fe0604bcbec",
    "sys_updated_by": "admin",
    "previous_version": null,
    "sys_created_on": "2023-01-18 16:04:52",
    "value": null,
    "effective_from": null,
    "linked_to": null,
    "sys_created_by": "admin",
    "restricted_to": null,
    "linked_to_version": null,
    "level": "2",
    "conflict_type": null,
    "main_id": "19",
    "effective_to": null,
    "secure_value": null,
    "node_classifier": "/shared_library/shared_components",
    "main_id_encoded": ":",
    "name": "testSharedComponent",
    "position": null,
    "reason_for_conflict": null,
    "system_folder": false,
    "status": "new",
    "conflict": false
  }
}
```

## CdmSharedLibraryApi - POST /sn\_cdm/shared\_libraries/uploads/components

Enables you to create and manage shared libraries and shared components. This endpoint creates a shared component node in the CDM Node \[sn\_cdm\_node\] table and a shared component record in the CDM Shared Component \[sn\_cdm\_shared\_component\] table.

The CDM Editor role is required to access this endpoint.

**Note:** By default, the maximum content upload size is 2MB. You can modify this default by updating the sn\_cdm.max\_allowed\_upload\_file\_size property.

**Note:** This upload method can't be used to modify nodes. Use the alternative [CdmSharedLibraryApi - POST /sn\_cdm/shared\_libraries/uploads/components/file](shared_libraries-api.md#) method to modify nodes.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/shared_libraries/uploads/components`

Default URL: `/api/sn_cdm/shared_libraries/uploads/components`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoDelete

</td><td>

Flag that indicates whether the existing nodes, that aren’t part of the upload content, are deleted after the processing is complete.Valid values:

-   true: Automatically delete existing nodes.
-   false: Don't automatically delete existing nodes.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td>

Required. String that uniquely identifies the changeset associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

dataFormat

</td><td>

Required. Format of the configuration data.Valid values:

-   csv
-   ini
-   json
-   properties
-   raw
-   xml
-   yaml

Data type: String

</td></tr><tr><td>

deleteRedundantOverrides

</td><td>

Flag that indicates whether to create an override where redundant values are present.Valid values:

-   true: If redundant values are present, an override isn’t created.
-   false: If redundant values are present, proceeds with an override.

Default: true

</td></tr><tr><td>

identifierKeys

</td><td>

List of names that indicate which key in an array child to use to identify the same node.For example, if you’re uploading:

```
[
  {"name" : "Allan, "city" : "Paris"}, 
  {"name" : "Karen, "city" : "Sydney"}
]
```

in the following existing model:

```
[
  {"name" : "Karen, "city" : "Manila"},
  {"name" : "Allan, "city" : "Brussels"}
]
```

and you set **identifierKeys** to `name`, it produces the following output:

```
[
  {"name" : "Karen, "city" : "Sydney"},
  {"name" : "Allan, "city" : "Paris"}
]
```

Otherwise, it produces the following output:

```
[
  {"name" : "Karen, "city" : "Manila"},
  {"name" : "Allan, "city" : "Brussels"},
  {"name" : "Allan, "city" : "Paris"},
  {"name" : "Karen, "city" : "Sydney"}
]
```

Data type: Array of Strings

</td></tr><tr><td>

ignoreAttributes

</td><td>

Flag that indicates whether the given data format supports attributes \(currently only XML\).Valid values:

-   true: If the given data format supports attributes, any attributes in the input data are skipped during the upload.
-   false: If the given data format supports attributes, any attributes in the input data are included in the upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr><tr><td>

publishOption

</td><td>

Publish option for the associated configured snapshots.

Valid values:

-   publish\_new\_and\_unpublish\_old: Publish the new snapshot created after the commit and unpublish the existing snapshot.
-   publish\_none: Don't publish any snapshots.

For additional information on publishing snapshots, see Publish or unpublish a snapshot.

Data type: String

Default: publish\_none

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library to create or manage.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|Variable upload data|Configuration data to upload. This can be any data in the format defined by the **dataFormat** parameter of the query parameters.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="id_fyp_pmb_fwb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **text/plain** and **application/x-www-form-urlencoded**.Default: **text/plain**

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

Bad Request. The upload request has been rejected.Possible issues:

-   Size of the configuration payload is greater that the allowed maximum - 2MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the endpoint to obtain the status of the upload.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to upload the shared library called Demo\_App1631126164773 with the configuration data being plain text.

```
curl "http://instance.servicenow.com/api/sn_cdm/sharedlibrary/component/upload?namePath=%2FSettings%2FdbSettings&dataFormat=json&appName=Demo_App1631126164773&changesetNumber=Chset-8&autoCommit=false&publishOption=publish_none&autoDelete=true" \ 
--request POST \  
--header "Accept:application/json" \  
--header "Content-Type:text/plain" \  
--data "{  
  \"dbIPAddress\": \"10.10.10.110\",  
\"dbPort\": \"8080\",  
\"dbConnectionString\": \"admin:admin server1.xyz.com:8080 dbName_payments\",  
\"dbConnectionStringBackup\": \"admin:admin server2.xyz.com dbName_payments_backup\ "}" \  
--user 'username':'password' 
```

The following return results show both a successful and an error response to this request.

```
// Successful response 
{  
"result": {  
    "upload_id": "ec1f71f45322301096edddeeff7b12b3"  
  }  
}
 
// Error response 

{  
"error": {  
   "message": "Size of uploaded data:6853632.0(bytes) is greater than max allowed upload limit of 2097152.0(bytes)",  
   "detail": ""  
},  
"status": "failure" 
} 
```

## CdmSharedLibraryApi - POST /sn\_cdm/shared\_libraries/uploads/components/file

Uploads files as part of the Configuration Data Model \(CDM\) under the components folder in a shared library.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}shared_libraries/uploads/components/file`

Default URL: `/api/sn_cdm/shared_libraries/uploads/components/file`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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
</table><table id="table_hxt_rmm_2yb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created when committed are validated.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

**Note:** This option is only available if the **autoCommit** parameter is `true`.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td>

String that uniquely identifies the changeset associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Default: Creates a changeset to use. The changeset details are returned as part of the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) results.

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

fileName

</td><td>

Name of the file to upload. This name can differ from than the actual file name and contain the file extension. For example, .txt/.scv/.jar. The fileName value is applied when downloading the file.Data type: String

</td></tr><tr><td>

fileNodeName

</td><td>

Name of the file node. This file name is used in the configuration data when exporting it. This name doesn’t require a file extension nor does it affect the download.Data type: String

</td></tr><tr><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library where the component to delete is located.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr></tbody>
</table><table id="table_j22_fgm_2yb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variable upload data

</td><td>

Configuration data to upload. By default, file size uploads are limited to 5 MB. For information about how to adjust your upload file sizes and type, see this [Now Support article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0718101).Data type: String/stream

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

</td><td>

Content Type of the file to be uploaded. Examples: application/zip, text/plain, application/json.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="id_cdq_fft_byb"><thead><tr><th>

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

Bad request.Upload request has been rejected.

Possible issues:

-   Size of configuration payload is greater that the allowed maximum - 2 MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="id_af3_kft_byb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="cdm_apps-stat-error_status-row"><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr id="cdm_apps-upload_id-row"><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

The following call demonstrates how to upload a plain text file to the components folder in the Shared Library.

```
curl "http://instance.servicenow.com/api/sn_cdm/shared_libraries/uploads/components/file?autoValidate=true&sharedLibraryName=sharedLibA &namePath=testComponent%2FfilesFolder&fileName=testFileNodeName.txt&publishOption=publish_valid&changesetNumber=Chset-108&autoCommit=true&fileNodeName=testFile.txt" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:text/plain" \ 
--data "This is sample content that will be uploaded to a plain text file."\ 
--user 'username':'password' 
```

The following return results show both a successful and an error response to this request.

```
// Successful completion of the upload request
{ 
  "result": { 
    "upload_id": "ec1f71f45322301096edddeeff7b12b3" 
  } 
} 

// Error response. Payload is too large.
{ 
  "error": { 
    "message": "Could not find active application with name: ‘testApp’ of type application", 
    "detail": "" 
  },
  "status": "failure"
}
```

## CdmSharedLibraryApi - PUT /sn\_cdm/shared\_libraries

Updates the shared library information. Use this endpoint to update the name, description, state of a shared library, and the user groups that can access the library.

The CDM Admin role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/shared_libraries`

Default URL: `/api/sn_cdm/shared_libraries`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

name

</td><td>

Required. Name of the shared library to update.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

newAvailableState

</td><td>

Flag that indicates the state of the shared library.Valid values:

-   true: The shared library is active.
-   false: The shared library is inactive. No users are allowed to access this library.

Default: true

</td></tr><tr><td>

newDescription

</td><td>

Updated description of the shared library. Data type: String

</td></tr><tr><td>

newName

</td><td>

New name of the shared library.Data type: String

</td></tr><tr><td>

newUserGroupIds

</td><td>

Comma separated list of sys\_ids of the user groups that can access the associated shared library.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

returnFields

</td><td>

Comma separated list of fields in the CDM Application \[sn\_cdm\_application\] table to return as part of the response.Data type: String

Default: All non-system fields are returned.

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;fields&gt;

</td><td>

Requested fields.Data type: Variable

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint for the shared library Java11Lib and update the library name and description.

```
curl "http://instance.servicenow.com/sn_cdm/shared_libraries?name=' javalib'&newName=’NewLibraryName’&newDescription=’new%20description%20of%20library’\ 
--request PUT\ 
--header "Accept:application/json" \ 
--user 'username':'password'  
```

Response:

```
{
  "result": {
    "sdlc_component": null,
    "cdi_count": "0",
    "available": true,
    "description": "Set new description",
    "managed_by_group": null,
    "sys_updated_on": "2023-01-18 11:51:14",
    "type": "shared_library",
    "node": {
      "value": "021635dc77a4a1109ac0cf0bbb5a9952",
      "link": "http://192.168.0.129:8080/api/now/table/sn_cdm_node/021635dc77a4a1109ac0cf0bbb5a9952"
    },
    "sys_id": "185235dc77a4a1109ac0cf0bbb5a994e",
    "sys_updated_by": "admin",
    "node_main": {
      "value": "1852b15877a4a1109ac0cf0bbb5a99aa",
      "link": "http://192.168.0.129:8080/api/now/table/sn_cdm_node_main/1852b15877a4a1109ac0cf0bbb5a99aa"
    },
    "sys_created_on": "2023-01-18 11:34:43",
    "cdi_usage": "0",
    "name": "LibraryA",
    "last_committed_changeset": {
      "value": "4a1635dc77a4a1109ac0cf0bbb5a9951",
      "link": "http://192.168.0.129:8080/api/now/table/sn_cdm_changeset/4a1635dc77a4a1109ac0cf0bbb5a9951"
    },
    "state": "active",
    "sys_created_by": "admin"
  }
}
```

## CdmSharedLibraryApi - PUT /sn\_cdm/shared\_libraries/components

Updates the name and description of the specified shared component.

The CDM Editor role is required to access this endpoint.

**Note:** Renaming is only allowed if a component has never been used, as when the component's snapshot has never been imported. The renaming scenario is primarily for the purpose of fixing typos when creating new components.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/shared_libraries/components`

Default URL: `/api/sn_cdm/shared_libraries/components`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

changesetNumber

</td><td>

Required. Name of the associated changeset.Data type: String

Table:CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

name

</td><td>

Required. Name of the shared component to update.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

newName

</td><td>

Required. Updated name of the shared component.Data type: String

</td></tr><tr><td>

newDescription

</td><td>

Updated description of the shared component. Data type: String

Default: Empty

</td></tr><tr><td>

returnFields

</td><td>

Comma separated list of fields in the CDM Shared Component \[sn\_cdm\_shared\_component\] table to return as part of the response.Data type: String

Default: All non-system fields are returned.

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;fields&gt;

</td><td>

Requested fields from the CDM Shared Component \[sn\_cdm\_shared\_component\] table.Data type: Variable

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code sample shows how to update the description of the component SharedComponentTest.

```
curl "http://instance.servicenow.com/sn_cdm/shared_libraries/components/?sharedLibraryName=javalib&changeSetNumber='chset-9'&name='SharedComponentTest'&newDescription='The shared component description'\  
--request POST\  
--header "Accept:application/json" \  
--user 'username':'password
```

Response:

```
{
  "result": {
    "changeset_id": {
      "value": "5c33311077e4a1109ac0cf0bbb5a9902",
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/5c33311077e4a1109ac0cf0bbb5a9902"
    },
    "node_path": "!(1!(2!(3",
    "description": "Changing the description only",
    "sys_updated_on": "2023-01-18 12:09:05",
    "type": "sn_cdm_node_shared_component",
    "sys_class_name": "sn_cdm_node",
    "sys_id": "9953f99077a4a1109ac0cf0bbb5a99ec",
    "sys_updated_by": "admin",
    "previous_version": null,
    "sys_created_on": "2023-01-18 11:39:09",
    "value": null,
    "effective_from": null,
    "linked_to": null,
    "sys_created_by": "admin",
    "restricted_to": null,
    "linked_to_version": null,
    "level": "2",
    "conflict_type": null,
    "main_id": "183",
    "effective_to": null,
    "secure_value": null,
    "node_classifier": "/shared_library/shared_components",
    "main_id_encoded": "(3",
    "name": "sharedComponentName",
    "position": null,
    "reason_for_conflict": null,
    "system_folder": false,
    "status": "new",
    "conflict": false
  }
}
```

